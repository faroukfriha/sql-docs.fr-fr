---
title: "Élément Member (XMLA) | Documents Microsoft"
ms.custom: 
ms.date: 03/06/2017
ms.prod: analysis-services
ms.prod_service: analysis-services, azure-analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
apiname: Member Element
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords:
- urn:schemas-microsoft-com:xml-analysis#Member
- microsoft.xml.analysis.member
- http://schemas.microsoft.com/analysisservices/2003/engine#Member
helpviewer_keywords: Member element
ms.assetid: 5cc33a1f-192e-4821-a4ef-9a5f2bb7a9f0
caps.latest.revision: "11"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 82690ec66dfcb96787ea592a8d32c3826ee8776f
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2018
---
# <a name="member-element-xmla"></a>Élément Member (XMLA)
[!INCLUDE[ssas-appliesto-sqlas-aas](../../../includes/ssas-appliesto-sqlas-aas.md)]Représente un membre unique dans un parent [membres](../../../analysis-services/xmla/xml-elements-properties/members-element-xmla.md) ou [Tuple](../../../analysis-services/xmla/xml-elements-properties/tuple-element-xmla.md) élément.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
  
<Members>  
   ...  
   <Member>  
      <UName>...</UName>  
      <Caption>...</Caption>  
      <LName>...</LName>  
      <LNum>...</LNum>  
      <DisplayInfo>...</DisplayInfo>  
   </Member>  
   ...  
</Members>  
<!-- or -->  
<Tuple>  
   ...  
   <Member Hierarchy="string">  
      <UName>...</UName>  
      <Caption>...</Caption>  
      <LName>...</LName>  
      <LNum>...</LNum>  
      <DisplayInfo>...</DisplayInfo>  
   </Member>  
   ...  
</Tuple>  
```  
  
## <a name="element-characteristics"></a>Caractéristiques de l'élément  
  
|Caractéristique|Description|  
|--------------------|-----------------|  
|Type de données et longueur|None|  
|Valeur par défaut|None|  
|Cardinalité|0-n : élément facultatif pouvant apparaître plusieurs fois.|  
  
## <a name="element-relationships"></a>Relations entre les éléments  
  
|Relation|Élément|  
|------------------|-------------|  
|Éléments parents|[Members](../../../analysis-services/xmla/xml-elements-properties/members-element-xmla.md), [Tuple](../../../analysis-services/xmla/xml-elements-properties/tuple-element-xmla.md)|  
|Éléments enfants|[Caption](../../../analysis-services/xmla/xml-elements-properties/caption-element-xmla.md), [DisplayInfo](../../../analysis-services/xmla/xml-elements-properties/displayinfo-element-xmla.md), [LName](../../../analysis-services/xmla/xml-elements-properties/lname-element-xmla.md), [LNum](../../../analysis-services/xmla/xml-elements-properties/lnum-element-xmla.md), [UName](../../../analysis-services/xmla/xml-elements-properties/uname-element-xmla.md)|  
  
## <a name="attributes"></a>Attributs  
  
|Attribute|Description|  
|---------------|-----------------|  
|Hiérarchie|Attribut **String** requis (pour les éléments **Tuple** parents uniquement). Nom de la hiérarchie dont font partie les membres représentés par l'élément **Member** .|  
  
## <a name="remarks"></a>Notes   
 L'élément **Member** contient les informations nécessaires pour identifier et afficher un membre dans une hiérarchie donnée. Pour les éléments **Members** parents, la hiérarchie est déjà spécifiée par l'attribut **Hierarchy** de l'élément parent. Pour les éléments **Tuple** parents, la hiérarchie est spécifiée à l'aide de l'attribut **Hierarchy** de l'élément **Member** .  
  
## <a name="see-also"></a>Voir aussi  
 [Propriétés &#40; XMLA &#41;](../../../analysis-services/xmla/xml-elements-properties/xml-elements-properties.md)  
  
  
