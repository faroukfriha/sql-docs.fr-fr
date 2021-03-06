---
title: "Méthode getMoreResults () | Documents Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: jdbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
apiname: SQLServerStatement.getMoreResults ()
apilocation: sqljdbc.jar
apitype: Assembly
ms.assetid: df89db50-0b2f-4094-820a-30be25ad72fe
caps.latest.revision: "8"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 2cf885b73a0d4e0f2d5b8aa1f75255f74001c59d
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2017
---
# <a name="getmoreresults-method-"></a>Méthode getMoreResults ()
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Passe au résultat suivant de ce [SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md) objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
public final boolean getMoreResults()  
```  
  
## <a name="return-value"></a>Valeur retournée  
 **true** si le résultat retourné est un jeu de résultats. Dans le cas contraire, la valeur est **false**.  
  
## <a name="exceptions"></a>Exceptions  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Notes  
 Cette méthode getMoreResults est spécifiée par la méthode getMoreResults dans l’interface java.sql.Statement.  
  
 La méthode getMoreResults implicitement ferme tous les objets de jeu de résultats actuellement ouverts qui ont été obtenus avec le [getResultSet](../../../connect/jdbc/reference/getresultset-method-sqlserverstatement.md) (méthode).  
  
## <a name="see-also"></a>Voir aussi  
 [Méthode getMoreResults &#40; SQLServerStatement &#41;](../../../connect/jdbc/reference/getmoreresults-method-sqlserverstatement.md)   
 [Membres de SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-members.md)   
 [SQLServerStatement, classe](../../../connect/jdbc/reference/sqlserverstatement-class.md)  
  
  
