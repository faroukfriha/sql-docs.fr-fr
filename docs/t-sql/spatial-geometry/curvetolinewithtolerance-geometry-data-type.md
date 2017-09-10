---
title: "CurveToLineWithTolerance (Type de données geometry) | Documents Microsoft"
ms.custom: 
ms.date: 08/03/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- CurveToLineWithTolerance method (geometry)
ms.assetid: 96871075-1998-4cd9-86b1-3fc55577aee4
caps.latest.revision: 16
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 5120f9c27e6157fd2f19c598ad984e1a3543db94
ms.contentlocale: fr-fr
ms.lasthandoff: 09/01/2017

---
# <a name="curvetolinewithtolerance-geometry-data-type"></a>CurveToLineWithTolerance (type de données geometry)
[!INCLUDE[tsql-appliesto-ss2012-asdb-xxxx-xxx_md](../../includes/tsql-appliesto-ss2012-asdb-xxxx-xxx-md.md)]

Retourne une approximation polygonale d’une **geometry** instance qui contient les segments d’arc de cercle.
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
.CurveToLineWithTolerance ( tolerance, relative )  
```  
  
## <a name="arguments"></a>Arguments  
 *tolérance de panne*  
 Est un **double** expression qui définit l’erreur maximale entre le segment d’arc de cercle d’origine et son approximation linéaire.  
  
 *relatif*  
 Est un **bool** expression qui indique s’il faut utiliser un maximum relatif pour l’écart. Lorsque la valeur relative est définie sur False (0), une valeur maximale absolue est définie pour l'écart d'une approximation linéaire. Si la valeur relative est True (1), la tolérance est calculée sous la forme d'un produit du paramètre de tolérance et du diamètre du rectangle englobant pour l'objet spatial.  
  
## <a name="return-types"></a>Types de retour  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]type de retour : **geometry**  
  
 Type de retour CLR : **SqlGeometry**  
  
## <a name="exceptions"></a>Exceptions  
 La définition d'une tolérance <= 0 lève une exception `ArgumentOutOfRange`.  
  
## <a name="remarks"></a>Notes  
 Cette méthode peut spécifier une valeur de tolérance d’erreur la résultante de **LineString**.  
  
 Le tableau affiche le type d'instance retourné par `CurveToLineWithTolerance()` pour différents types.  
  
|Appel du type d'instance|Type spatial retourné|  
|----------------------------|---------------------------|  
|Instance géométrique vide|Vide **GeometryCollection** instance|  
|**Point** et **MultiPoint**|**Point** instance|  
|**MultiPoint**|**Point** ou **MultiPoint** instance|  
|**CircularString**, **CompoundCurve**, ou **LineString**|**LineString** instance|  
|**MultiLineString**|**LineString** ou **MultiLineString** instance|  
|**CurvePolygon** et **polygone**|**Polygone** instance|  
|**MultiPolygon**|**Polygone** ou **MultiPolygon** instance|  
|**GeometryCollection** avec une seule instance qui ne contient-elle pas un segment d’arc de cercle|L’instance qui est contenue dans le **GeometryCollection** détermine le type de l’instance retournée.|  
|**GeometryCollection** avec une instance de segment d’arc de cercle unidimensionnelle unique (**CircularString**, **CompoundCurve**)|**LineString** instance|  
|**GeometryCollection** avec une instance de segment d’arc de cercle bidimensionnelle unique (**CurvePolygon**)|**Polygone** instance|  
|**GeometryCollection** avec plusieurs instances unidimensionnelles|**MultiLineString** instance|  
|**GeometryCollection** avec plusieurs instances bidimensionnelles|**MultiPolygon** instance|  
|**GeometryCollection** avec plusieurs instances de différentes dimensions|**GeometryCollection** instance|  
  
## <a name="examples"></a>Exemples  
  
### <a name="a-using-different-tolerance-values-on-a-circularstring-instance"></a>A. Utilisation de valeurs de tolérance différentes sur une instance CircularString  
 L’exemple suivant montre comment la définition de la tolérance affecte le `LineString`instance retournée par un `CircularString` instance :  
  
 `DECLARE @g geometry;`  
  
 `SET @g = geometry::Parse('CIRCULARSTRING(0 0, 1 2.1082, 3 6.3246, 0 7, -3 6.3246, -1 2.1082, 0 0)');`  
  
 `SELECT @g.CurveToLineWithTolerance(0.1,0).STNumPoints(), @g.CurveToLineWithTolerance(0.01, 0).STNumPoints();`  
  
### <a name="b-using-the-method-on-a-multilinestring-instance-containing-one-linestring"></a>B. Utilisation de la méthode sur une instance MultiLineString qui contient un LineString  
 L'exemple suivant montre ce qui est retourné d'une instance `MultiLineString` qui contient uniquement une instance `LineString` :  
  
 `DECLARE @g geometry;`  
  
 `SET @g = geometry::Parse('MULTILINESTRING((1 3, 4 8, 6 9))');`  
  
 `SELECT @g.CurveToLineWithTolerance(0.1,0).ToString();`  
  
### <a name="c-using-the-method-on-a-multilinestring-instance-containing-multiple-linestrings"></a>C. Utilisation de la méthode sur une instance MultiLineString qui contient plusieurs LineStrings  
 L'exemple suivant montre ce qui est retourné d'une instance `MultiLineString` qui contient plusieurs instances `LineString` :  
  
 `DECLARE @g geometry;`  
  
 `SET @g = geometry::Parse('MULTILINESTRING((1 3, 4 8, 6 9),(4 4, 9 18))');`  
  
 `SELECT @g.CurveToLineWithTolerance(0.1,0).ToString();`  
  
### <a name="d-setting-relative-to-true-for-an-invoking-curvepolygon-instance"></a>D. Définition d'une valeur relative sur True pour appeler une instance CurvePolygon  
 L’exemple suivant utilise un `CurvePolygon` instance pour appeler `CurveToLineWithTolerance()` avec *relatif* défini sur true :  
  
 `DECLARE @g geometry = 'CURVEPOLYGON(COMPOUNDCURVE(CIRCULARSTRING(0 4, 4 0, 8 4), (8 4, 0 4)))';`  
  
 `SELECT @g.CurveToLineWithTolerance(.5,1).ToString();`  
  
### <a name="e-using-the-method-on-a-geometrycollection-instance"></a>E. Utilisation de la méthode sur une instance GeometryCollection  
 L'exemple suivant appelle `CurveToLineWithTolerance()` sur une `GeometryCollection` qui contient une instance `CurvePolygon` bidimensionnelle et une instance `CircularString` unidimensionnelle. `CurveToLineWithTolerance()` convertit des types de segment d'arc de cercle en types de segment linéaire et les retourne dans un type `GeometryCollection`.  
  
 `DECLARE @g geometry;`  
  
 `SET @g = geometry::Parse('GEOMETRYCOLLECTION(CURVEPOLYGON( COMPOUNDCURVE(CIRCULARSTRING(0 2, 2 0, 4 2), (4 2, 0 2))), CIRCULARSTRING(4 4, 8 6, 9 5))');`  
  
 `SELECT @g.CurveToLineWithTolerance(0.1,0).STNumPoints(), @g.CurveToLineWithTolerance(0.1, 0).ToString();`  
  
## <a name="see-also"></a>Voir aussi  
 [CurveToLineWithTolerance &#40; Type de données geography &#41;](../../t-sql/spatial-geography/curvetolinewithtolerance-geography-data-type.md)   
 [STCurveToLine &#40; Type de données geometry &#41;](../../t-sql/spatial-geometry/stcurvetoline-geometry-data-type.md)  
  
  

