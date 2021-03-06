---
title: "Type de données DataItem (ASSL) | Documents Microsoft"
ms.custom: 
ms.date: 03/14/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
apiname: DataItem Data Type
apilocation: http://schemas.microsoft.com/analysisservices/2003/engine
apitype: Schema
applies_to: SQL Server 2016 Preview
f1_keywords: DataItem
helpviewer_keywords: DataItem data type
ms.assetid: f4f5155f-9c3d-49a1-a390-a9c734fafbce
caps.latest.revision: "44"
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: ec40eca06225eef5d9c7e505e4fe2c9dee6972b1
ms.sourcegitcommit: f486d12078a45c87b0fcf52270b904ca7b0c7fc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2018
---
# <a name="dataitem-data-type-assl"></a>Type de données DataItem (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]Définit un type de données primitif qui représente les caractéristiques liées aux données d’un élément de données, tel qu’une colonne ou un attribut.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
  
<DataItem>  
   <DataType>...</DataType>  
   <DataSize>...</DataSize>  
   <MimeType>...</MimeType>  
   <NullProcessing>...</NullProcessing>  
   <Trimming>...</Trimming>  
   <InvalidXmlCharacters>...</InvalidXmlCharacters>  
      <Collation>...</Collation>  
   <Format>...</Format>  
   <Source>...</Source>  
   <Annotations>...</Annotations>  
</DataItem>  
```  
  
## <a name="data-type-characteristics"></a>Caractéristiques du type de données  
  
|Caractéristique|Description|  
|--------------------|-----------------|  
|Types de données de base|None|  
|Types de données dérivés|None|  
  
## <a name="data-type-relationships"></a>Relations du type de données  
  
|Relation|Élément|  
|------------------|-------------|  
|Éléments parents|None|  
|Éléments enfants|[Annotations](../../../analysis-services/scripting/collections/annotations-element-assl.md), [Collation](../../../analysis-services/scripting/properties/collation-element-assl.md), [DataSize](../../../analysis-services/scripting/properties/datasize-element-assl.md), [DataType](../../../analysis-services/scripting/properties/datatype-element-assl.md), [Format](../../../analysis-services/scripting/properties/format-element-assl.md), [InvalidXmlCharacters](../../../analysis-services/scripting/properties/invalidxmlcharacters-element-assl.md), [MimeType](../../../analysis-services/scripting/properties/mimetype-element-assl.md), [NullProcessing](../../../analysis-services/scripting/properties/nullprocessing-element-assl.md), [Source](../../../analysis-services/scripting/properties/source-element-binding-assl.md), [Trimming](../../../analysis-services/scripting/properties/trimming-element-assl.md)|  
|Éléments dérivés|Voir le tableau dans la section Remarques.|  
  
## <a name="remarks"></a>Notes   
 Le type de données **DataItem** est utilisé pour tous les éléments de données qu'il est possible de lier (par exemple, une mesure, une clé d'attribut et un nom d'attribut). Les détails pertinents, et les valeurs par défaut qui s'appliquent, dépendent de l'utilisation (par exemple, les noms d'attribut doivent être des chaînes).  
  
 Une instance de [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)] accepte uniquement un certain ensemble de types de données. L'utilisation d'autres résultats de types de données entraîne une erreur plutôt qu'une conversion implicite à l'un des types valides.  
  
 Le tableau suivant répertorie les éléments de type **DataItem**.  
  
|Élément parent|Élément de type **DataItem**|Commentaires|  
|--------------------|----------------------------------|--------------|  
|[AttributeTranslation](../../../analysis-services/scripting/data-type/attributetranslation-data-type-assl.md)|[CaptionColumn](../../../analysis-services/scripting/objects/captioncolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[CustomRollupColumn](../../../analysis-services/scripting/objects/customrollupcolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[CustomRollupPropertiesColumn](../../../analysis-services/scripting/objects/customrolluppropertiescolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[KeyColumn](../../../analysis-services/scripting/objects/keycolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md), [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md) ou [TimeBinding](../../../analysis-services/scripting/data-type/timebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[NameColumn](../../../analysis-services/scripting/objects/namecolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[SkippedLevelsColumn](../../../analysis-services/scripting/objects/skippedlevelscolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[DimensionAttribute](../../../analysis-services/scripting/data-type/dimensionattribute-data-type-assl.md)|[UnaryOperatorColumn](../../../analysis-services/scripting/objects/unaryoperatorcolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md) ou [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md).|  
|[Mesure](../../../analysis-services/scripting/objects/measure-element-assl.md)|[Source](../../../analysis-services/scripting/properties/source-element-binding-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [RowBinding](../../../analysis-services/scripting/data-type/rowbinding-data-type-assl.md), [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md), [MeasureBinding](../../../analysis-services/scripting/data-type/measurebinding-data-type-assl.md)ou [CubeDimensionBinding](../../../analysis-services/scripting/data-type/cubedimensionbinding-data-type-assl.md).|  
|[MeasureGroupAttribute](../../../analysis-services/scripting/data-type/measuregroupattribute-data-type-assl.md)|[KeyColumn](../../../analysis-services/scripting/objects/keycolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md), [AttributeBinding](../../../analysis-services/scripting/data-type/attributebinding-data-type-assl.md) ou [InheritedBinding](../../../analysis-services/scripting/data-type/inheritedbinding-data-type-assl.md).|  
|[ScalarMiningStructureColumn](../../../analysis-services/scripting/data-type/scalarminingstructurecolumn-data-type-assl.md)|[KeyColumn](../../../analysis-services/scripting/objects/keycolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md).|  
|[ScalarMiningStructureColumn](../../../analysis-services/scripting/data-type/scalarminingstructurecolumn-data-type-assl.md)|[NameColumn](../../../analysis-services/scripting/objects/namecolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md).|  
|[TableMiningStructureColumn](../../../analysis-services/scripting/data-type/tableminingstructurecolumn-data-type-assl.md)|[ForeignKeyColumn](../../../analysis-services/scripting/objects/foreignkeycolumn-element-assl.md)|L'élément**Source** du type de données **DataItem** doit être de type [ColumnBinding](../../../analysis-services/scripting/data-type/columnbinding-data-type-assl.md).|  
  
 L’élément correspondant dans le modèle d’objet objets AMO (Analysis Management) est <xref:Microsoft.AnalysisServices.DataItem>.  
  
## <a name="see-also"></a>Voir aussi  
 [Analysis Services script des Types de données XML Language &#40; ASSL &#41;](../../../analysis-services/scripting/data-type/analysis-services-scripting-language-xml-data-types-assl.md)  
  
  
