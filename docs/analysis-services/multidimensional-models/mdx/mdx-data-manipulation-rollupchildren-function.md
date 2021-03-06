---
title: Utilisation de la fonction RollupChildren (MDX) | Documents Microsoft
ms.custom: 
ms.date: 03/16/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: data-mining
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- queries [MDX], RollupChildren function
- RollupChildren function
- custom member properties [MDX]
- IIf function
ms.assetid: 03c624d4-f277-451d-9995-623a07ea2f86
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 1fb9052d74a19941a41a915e12acec04bfc38f1c
ms.sourcegitcommit: 7519508d97f095afe3c1cd85cf09a13c9eed345f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2018
---
# <a name="mdx-data-manipulation---rollupchildren-function"></a>Manipulation de données MDX - fonction RollupChildren
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
La fonction MDX (Multidimensional Expressions) [RollupChildren](../../../mdx/rollupchildren-mdx.md) effectue le cumul des enfants d’un membre, en appliquant un opérateur unaire différent à chaque enfant, et retourne la valeur de ce cumul sous la forme d’un nombre. L'opérateur unaire peut être fourni par une propriété de membre associée au membre enfant, ou être une expression de type chaîne directement fournie à la fonction.  
  
## <a name="rollupchildren-function-examples"></a>Exemples de fonctions RollupChildren  
 L’utilisation de la fonction **RollupChildren** dans les instructions MDX (Multidimensional Expressions) est simple à expliquer, mais elle peut avoir d’importantes répercussions sur les requêtes MDX.  
  
 L’effet de la fonction **RollupChildren** est perceptible dans les requêtes MDX conçues pour effectuer des analyses sélectives portant sur des données de cube existantes. Par exemple, le tableau suivant contient une liste de membres enfants du membre parent Net Sales, ainsi que leurs opérateurs unaires entre parenthèses (représentés par la propriété de membre **UNARY_OPERATOR** ).  
  
|Membre parent|Membre enfant|  
|-------------------|------------------|  
|Ventes nettes|Domestic Sales (+)<br /><br /> Domestic Returns (-)<br /><br /> Foreign Sales (+)<br /><br /> Foreign Returns (-)|  
  
 Dans le cadre du cumul, le total des ventes nettes fourni en l'occurrence par le membre parent Net Sales est exprimé par les valeurs des ventes brutes réalisées sur le marché national et à l'étranger, moins les invendus réalisés sur le marché national et à l'étranger.  
  
 Cependant, vous souhaitez fournir une estimation rapide et simple des ventes brutes réalisées sur le marché national et à l'étranger majorées de 10 %, sans tenir compte des invendus réalisés sur le marché national et à l'étranger. Pour calculer cette valeur, vous pouvez utiliser la fonction **RollupChildren** des deux manières suivantes : avec une propriété de membre personnalisée ou avec la fonction **IIf** .  
  
### <a name="using-a-custom-member-property"></a>Utilisation d'une propriété de membre personnalisée  
 Si le calcul de cumuls est appelé à être souvent utilisé, une méthode consiste à créer pour une fonction donnée une propriété de membre qui stocke les opérateurs à utiliser pour chaque enfant. Le tableau suivant présente les opérateurs unaires corrects et décrit le résultat attendu.  
  
|Opérateur|Résultat|  
|--------------|------------|  
|+|total = total + enfant actuel|  
|-|total = total - enfant actuel|  
|*|total = total * enfant actuel|  
|/|total = total / enfant actuel|  
|~|L'enfant n'est pas utilisé dans le cumul. La valeur de l'enfant est ignorée.|  
  
 Par exemple, une propriété de membre appelée **SALES_OPERATOR** est créée, à laquelle sont affectés des opérateurs unaires, comme le montre le tableau suivant.  
  
|Membre parent|Membre enfant|  
|-------------------|------------------|  
|Ventes nettes|Domestic Sales (+)<br /><br /> Domestic Returns (~)<br /><br /> Foreign Sales (+)<br /><br /> Foreign Returns (~)|  
  
 Grâce à cette nouvelle propriété de membre, l'instruction MDX suivante effectue l'estimation des ventes brutes rapidement et efficacement (en ignorant les invendus réalisés sur le marché national et à l'étranger) :  
  
```  
RollupChildren([Net Sales], [Net Sales].CurrentMember.Properties("SALES_OPERATOR")) * 1.1  
```  
  
 Lorsque la fonction est appelée, la valeur de chaque enfant s'applique à un total à l'aide de l'opérateur stocké dans la propriété de membre. Les membres correspondant aux invendus réalisés sur le marché national et à l’étranger sont ignorés, et le total du cumul renvoyé par la fonction **RollupChildren** est multiplié par 1,1.  
  
### <a name="using-the-iif-function"></a>Utilisation de la fonction IIf  
 Si l’opération de cet exemple n’est pas souvent utilisée ou si elle ne s’applique qu’à une seule requête MDX, la fonction [IIf](../../../mdx/iif-mdx.md) peut être utilisée avec la fonction **RollupChildren** pour fournir le même résultat. La requête MDX suivante fournit le même résultat que l'instruction MDX précédente, mais sans avoir recours à une propriété de membre personnalisée :  
  
```  
RollupChildren([Net Sales], IIf([Net Sales].CurrentMember.Properties("UNARY_OPERATOR") = "-", "~", [Net Sales].CurrentMember.Properties("UNARY_OPERATOR))) * 1.1  
```  
  
 L'instruction MDX examine l'opérateur unaire du membre enfant. S’il est utilisé pour une soustraction (comme dans le cas des membres correspondant aux invendus réalisés sur le marché national et à l’étranger), l’opérateur unaire tilde (~) est remplacé par la fonction **IIf** . Sinon, la fonction **IIf** utilise l’opérateur unaire du membre enfant. Enfin, le total du cumul renvoyé est multiplié par 1,1 afin de fournir la valeur estimée des ventes brutes sur le marché national et à l'étranger.  
  
## <a name="see-also"></a>Voir aussi  
 [Manipulation de données &#40; MDX &#41;](../../../analysis-services/multidimensional-models/mdx/mdx-data-manipulation-manipulating-data.md)  
  
  
