---
title: "Méthode getTime (int, java.util.Calendar) | Documents Microsoft"
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
apiname: SQLServerCallableStatement.getTime (int, java.util.Calendar)
apilocation: sqljdbc.jar
apitype: Assembly
ms.assetid: 87b7fbaf-7149-494f-b3b2-16b468a8ebf1
caps.latest.revision: "12"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 3907b3c90670f63abacdab741041863798e25ec4
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2017
---
# <a name="gettime-method-int-javautilcalendar"></a>Méthode getTime (int, java.util.Calendar)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Récupère la valeur du paramètre désigné en tant qu’objet java.sql.Time dans le langage de programmation donné de l’index de paramètre, à l’aide de l’objet de calendrier donné de Java.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
public java.sql.Time getTime(int index,  
                             java.util.Calendar cal)  
```  
  
#### <a name="parameters"></a>Paramètres  
 *index*  
  
 Un **int** qui indique l’index de paramètre.  
  
 *licences d’accès client*  
  
 Un objet de calendrier.  
  
## <a name="return-value"></a>Valeur retournée  
 Un objet de l’heure.  
  
## <a name="exceptions"></a>Exceptions  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Notes  
 Cette méthode getTime est spécifiée par la méthode getTime dans l’interface java.sql.CallableStatement.  
  
 Consultez le graphique intitulé « Conversions de méthode d’accesseur get » dans [présentation des Conversions de Type de données](../../../connect/jdbc/understanding-data-type-conversions.md) pour voir quelle [!INCLUDE[ssNoVersion](../../../includes/ssnoversion_md.md)] des types de données peuvent être récupérés avec cette méthode.  
  
## <a name="see-also"></a>Voir aussi  
 [Méthode getTime &#40; SQLServerCallableStatement &#41;](../../../connect/jdbc/reference/gettime-method-sqlservercallablestatement.md)   
 [Membres de SQLServerCallableStatement](../../../connect/jdbc/reference/sqlservercallablestatement-members.md)   
 [SQLServerCallableStatement, classe](../../../connect/jdbc/reference/sqlservercallablestatement-class.md)  
  
  
