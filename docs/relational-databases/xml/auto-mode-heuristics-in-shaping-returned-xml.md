---
title: "Heuristique du mode AUTO permettant de définir la forme des données XML renvoyées | Microsoft Docs"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: xml
ms.reviewer: 
ms.suite: sql
ms.technology:
- dbe-xml
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- AUTO FOR XML mode, heuristics in shaping returned XML
ms.assetid: 6c5cb6c1-2921-4ba1-8100-0bf8074f9103
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: d9e8dae9ee9c8ccb9690fbe434786b6c40a31b62
ms.sourcegitcommit: 37f0b59e648251be673389fa486b0a984ce22c81
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2018
---
# <a name="auto-mode-heuristics-in-shaping-returned-xml"></a>Heuristique du mode AUTO permettant de définir la forme des données XML renvoyées
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]
Le mode AUTO détermine la forme des données XML renvoyées en fonction de la requête. Lors de la définition de l'imbrication des éléments, l'heuristique du mode AUTO compare les valeurs de colonnes de lignes adjacentes. Les colonnes de tous les types, sauf **ntext**, **text**, **image**et **xml**, sont comparées. Les colonnes de type **(n)varchar(max)** et **varbinary(max)** sont comparées.  
  
 L'exemple suivant illustre l'heuristique du mode AUTO qui détermine la forme des données XML obtenues :  
  
```  
SELECT T1.Id, T2.Id, T1.Name  
FROM   T1, T2  
WHERE ...  
FOR XML AUTO  
ORDER BY T1.Id  
```  
  
 Pour déterminer à quel endroit commence un nouvel élément <`T1`>, toutes les valeurs de colonne de T1, sauf **ntext**, **text**, **image** et **xml**, sont comparées si la clé de la table T1 n’est pas spécifiée. Ensuite, supposons que la colonne **Name** soit de type **nvarchar(40)** et que l’instruction SELECT renvoie l’ensemble de lignes suivant :  
  
```  
T1.Id  T1.Name  T2.Id  
-----------------------  
1       Andrew    2  
1       Andrew    3  
1       Nancy     4  
```  
  
 L'heuristique du mode AUTO compare toutes les valeurs de la table T1, les colonnes Id et Name. Étant donné que les deux premières lignes contiennent les mêmes valeurs pour les colonnes Id et Name, un élément \<T1> possédant deux éléments enfants \<T2> est ajouté au résultat.  
  
 Voici le document XML renvoyé :  
  
```  
<T1 Id="1" Name="Andrew">  
    <T2 Id="2" />  
    <T2 Id="3" />  
</T1>  
<T1 Id="1" Name="Nancy" >  
      <T2 Id="4" />  
</T>  
```  
  
 Supposons maintenant que la colonne Name soit de type **text** . L'heuristique du mode AUTO ne compare pas les valeurs de ce type. Au lieu de cela, elle considère que les valeurs ne sont pas identiques. Cela aboutit à la génération de données XML suivante :  
  
```  
<T1 Id="1" Name="Andrew" >  
  <T2 Id="2" />  
</T1>  
<T1 Id="1" Name="Andrew" >  
  <T2 Id="3" />  
</T1>  
<T1 Id="1" Name="Nancy" >  
  <T2 Id="4" />  
</T1>  
```  
  
## <a name="see-also"></a> Voir aussi  
 [UTiliser le mode AUTO avec FOR XML](../../relational-databases/xml/use-auto-mode-with-for-xml.md)  
  
  
