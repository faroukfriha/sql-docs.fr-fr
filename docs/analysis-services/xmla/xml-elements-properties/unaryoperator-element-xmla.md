---
title: "Élément UnaryOperator (XMLA) | Documents Microsoft"
ms.custom: 
ms.date: 03/17/2017
ms.prod: analysis-services
ms.prod_service: analysis-services, azure-analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
apiname: UnaryOperator Element
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords:
- http://schemas.microsoft.com/analysisservices/2003/engine#UnaryOperator
- urn:schemas-microsoft-com:xml-analysis#UnaryOperator
- microsoft.xml.analysis.unaryoperator
helpviewer_keywords: UnaryOperator element
ms.assetid: 4dc9cfbe-6f8b-42bc-8d3a-42f48ca5d299
caps.latest.revision: "11"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 98f83a138787d29126b922ecb5059c696f7d795b
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2018
---
# <a name="unaryoperator-element-xmla"></a>Élément UnaryOperator (XMLA)
[!INCLUDE[ssas-appliesto-sqlas-aas](../../../includes/ssas-appliesto-sqlas-aas.md)]Contient l’opérateur unaire pour un membre d’attribut représenté par le parent [attribut](../../../analysis-services/xmla/xml-elements-properties/attribute-element-xmla.md) élément.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
  
<Attribute>  
   ...  
   <UnaryOperator>...</UnaryOperator>  
   ...  
</Attribute>  
```  
  
## <a name="element-characteristics"></a>Caractéristiques de l'élément  
  
|Caractéristique|Description|  
|--------------------|-----------------|  
|Type de données et longueur|String|  
|Valeur par défaut|None|  
|Cardinalité|0-1 : élément facultatif qui peut apparaître une fois et une seule.|  
  
## <a name="element-relationships"></a>Relations entre les éléments  
  
|Relation|Élément|  
|------------------|-------------|  
|Éléments parents|[Attribute](../../../analysis-services/xmla/xml-elements-properties/attribute-element-xmla.md)|  
|Éléments enfants|None|  
  
## <a name="remarks"></a>Notes   
 L'élément **UnaryOperator** contient une expression MDX (Multidimensional Expressions) qui définit l'opérateur unaire du membre d'attribut défini par l'élément **Attribute** parent.  
  
 Pour plus d’informations sur les expressions MDX, consultez [Expressions &#40; MDX &#41; ](../../../mdx/expressions-mdx.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Insérer un élément &#40; XMLA &#41;](../../../analysis-services/xmla/xml-elements-commands/insert-element-xmla.md)   
 [Mettre à jour, élément &#40; XMLA &#41;](../../../analysis-services/xmla/xml-elements-commands/update-element-xmla.md)   
 [Propriétés &#40; XMLA &#41;](../../../analysis-services/xmla/xml-elements-properties/xml-elements-properties.md)  
  
  
