---
title: "GeomFromGml (type de données geometry) | Microsoft Docs"
ms.custom: 
ms.date: 08/03/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|spatial-geography
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- GeomFromGML_TSQL
- GeomFromGML
dev_langs:
- TSQL
helpviewer_keywords:
- GeomFromGML (geometry Data Type)
ms.assetid: a3f2c84b-a49f-4ce3-ba25-b903fb0c99b4
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5b3c279f25c0de73040d6069362f7763b5330132
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2018
---
# <a name="geomfromgml-geometry-data-type"></a>GeomFromGml (type de données geometry)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

Construit une instance **geometry** en fonction d’une représentation du sous-ensemble [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] du langage GML (Geography Markup Language).
  
Pour plus d'informations sur le langage GML, consultez les spécifications Open Geospatial Consortium à l'adresse suivante :
  
[Spécifications OGC, Geography Markup Language](http://go.microsoft.com/fwlink/?LinkId=93629)
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
GeomFromGml ( GML_input, SRID )  
```  
  
## <a name="arguments"></a>Arguments  
 *GML_input*  
 Entrée XML à partir de laquelle le GML renverra une valeur.  
  
 *SRID*  
 Expression **int** qui représente le SRID (ID de référence spatiale) de l’instance **geometry** à retourner.  
  
## <a name="return-types"></a>Types de retour  
 Type de retour [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] : **geometry**  
  
 Type de retour CLR : **SqlGeometry**  
  
## <a name="remarks"></a>Notes   
 Cette méthode lève **FormatException** si l’entrée n’est pas au format approprié.  
  
## <a name="examples"></a>Exemples  
 L'exemple suivant utilise la méthode `GeomFromGml()` pour créer une instance `geometry`.  
  
```  
DECLARE @g geometry;  
DECLARE @x xml;  
SET @x = '<LineString xmlns="http://www.opengis.net/gml"> <posList>100 100 20 180 180 180</posList> </LineString>';  
SET @g = geometry::GeomFromGml(@x, 0);  
SELECT @g.ToString();  
```  
  
## <a name="see-also"></a> Voir aussi  
 [Méthodes geometry statiques étendues](../../t-sql/spatial-geometry/extended-static-geometry-methods.md)  
  
  

