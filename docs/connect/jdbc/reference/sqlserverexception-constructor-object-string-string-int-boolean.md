---
title: Constructeur SQLServerException (java.lang.Object, java.lang.String, java.lang.String, int, boolean) | Documents Microsoft
ms.custom: 
ms.date: 01/19/2018
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: jdbc
ms.reviewer: 
ms.suite: sql
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
apilocation:
- sqljdbc.jar
apitype: Assembly
ms.assetid: 
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: e9473e53d55a2d07f8b73d1efae2bfeb1be3ef98
ms.sourcegitcommit: 9d0467265e052b925547aafaca51e5a5e93b7e38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2018
---
# <a name="sqlserverexception-constructor-javalangobject-javalangstring-javalangstring-int-boolean"></a>Constructeur SQLServerException (java.lang.Object, java.lang.String, java.lang.String, int, boolean)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Initialise une nouvelle instance de la [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md) classe en fonction d’un **objet**, un **chaîne** objet, un **chaîne** (objet), un **int**et un **booléenne**.

## <a name="syntax"></a>Syntaxe  
  
```  

public SQLServerException(java.lang.Object obj,
            java.lang.String errText,
            java.lang.String errState,
            int errNum,
            boolean bStack)

            
```  
  
#### <a name="parameters"></a>Paramètres  
 *obj*  
  
 Le tampon d’e/s qui a généré l’exception.

 *errText*  
  
 Chaîne contenant le texte d’erreur.
  
 *sqlState*  
  
 Un objet d’énumération qui contient l’état SQL.
 
 *errNum*  
  
 Int qui contiennent le code d’erreur pour l’exception.
 
 *bStack*  
  
 Valeur booléenne qui indique si la trace de pile doit être générée.
  
## <a name="see-also"></a>Voir aussi  
 [Constructeurs SQLServerException](../../../connect/jdbc/reference/sqlserverexception-constructors.md)   
 [SQLServerException Members](../../../connect/jdbc/reference/sqlserverexception-members.md)   
 [SQLServerException, classe](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
  
