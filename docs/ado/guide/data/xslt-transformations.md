---
title: Transformations XSLT | Documents Microsoft
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- XSLT transformations in ADO
ms.assetid: 1a46196e-839f-4734-a59e-2c64609ffb9e
caps.latest.revision: 3
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 36b39d14a4856d882add1e9bafdc9457fa3b8bc1
ms.contentlocale: fr-fr
ms.lasthandoff: 09/09/2017

---
# <a name="xslt-transformations"></a>Transformations XSLT
XSLT peut être appliqué au XML généré pour le transformer en un autre format. Présentation du format XML dans ADO permet de développer des modèles XSLT, qui peuvent transformer en une forme plus conviviale.  
  
 Par exemple, vous savez que chaque ligne de l’objet Recordset est enregistré en tant qu’élément z : row dans l’élément rs : data. De même, chaque champ de l’objet Recordset est enregistrée comme une paire attribut-valeur pour cet élément.  
  
## <a name="remarks"></a>Notes  
 Le script XSLT suivant peut être appliqué pour le code XML indiqué dans la section précédente pour le transformer en une table HTML à afficher dans le navigateur :  
  
```  
<?xml version="1.0" encoding="ISO-8859-1"?>  
<html xmlns:xsl="http://www.w3.org/TR/WD-xsl">  
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white">  
<table border="1" style="table-layout:fixed" width="600">  
  <col width="200"></col>  
  <tr bgcolor="teal">  
    <th><font color="white">CustomerId</font></th>  
    <th><font color="white">CompanyName</font></th>  
    <th><font color="white">ContactName</font></th>  
  </tr>  
<xsl:for-each select="xml/rs:data/z:row">  
  <tr bgcolor="navy">  
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td>  
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td>  
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>   
  </tr>  
</xsl:for-each>  
</table>  
</body>  
</html>  
```  
  
 XSLT convertit le flux XML généré par la méthode ADO enregistrer dans une table HTML qui affiche chaque champ de l’ensemble d’enregistrements, ainsi que le titre de la table. En-têtes des colonnes et les lignes sont également affectés différentes polices et couleurs.  
  
## <a name="see-also"></a>Voir aussi  
 [Maintien d’enregistrements au Format XML](../../../ado/guide/data/persisting-records-in-xml-format.md)