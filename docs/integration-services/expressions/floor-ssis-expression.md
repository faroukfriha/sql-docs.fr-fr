---
title: FLOOR (expression SSIS) | Microsoft Docs
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: integration-services
ms.service: 
ms.component: expressions
ms.reviewer: 
ms.suite: sql
ms.technology:
- integration-services
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- largest integer less than or equal to expression
- FLOOR function [SSIS]
ms.assetid: 168084db-badd-40f2-87b4-1f5bc45c3e24
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 69e498a3c182cb15f1acf53cc16720088af9b65f
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2018
---
# <a name="floor-ssis-expression"></a>FLOOR (expression SSIS)
  Renvoie l'entier le plus élevé inférieur ou égal à une expression numérique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
FLOOR(numeric_expression)  
```  
  
## <a name="arguments"></a>Arguments  
 *numeric_expression*  
 Expression numérique valide.  
  
## <a name="result-types"></a>Types des résultats  
 Type de données numérique de l'expression de l'argument. Le résultat est la partie entière de la valeur calculée dans le même type de données que *numeric_expression.*  
  
## <a name="remarks"></a>Notes   
 La fonction FLOOR renvoie un résultat NULL si l'argument est NULL.  
  
## <a name="expression-examples"></a>Exemples d'expressions  
 Les exemples suivants appliquent la fonction FLOOR à une valeur successivement positive, négative et nulle.  
  
```  
FLOOR(123.45)  
```  
  
 Retourne 123.00  
  
```  
FLOOR(-123.45)  
```  
  
 Retourne -124.00  
  
```  
FLOOR(0.00)  
```  
  
 Renvoie 0,00  
  
## <a name="see-also"></a> Voir aussi  
 [CEILING &#40;expression SSIS&#41;](../../integration-services/expressions/ceiling-ssis-expression.md)   
 [Fonctions &#40;expression SSIS&#41;](../../integration-services/expressions/functions-ssis-expression.md)  
  
  
