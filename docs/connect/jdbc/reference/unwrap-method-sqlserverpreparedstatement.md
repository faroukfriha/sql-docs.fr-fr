---
title: "Méthode Unwrap (SQLServerPreparedStatement) | Documents Microsoft"
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
ms.assetid: 8e3ec950-3ac1-4c28-9e97-ddce3bd46578
caps.latest.revision: "14"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: e78cd05244991952001f1dfc71785160227a528f
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2017
---
# <a name="unwrap-method-sqlserverpreparedstatement"></a>Méthode unwrap (SQLServerPreparedStatement)
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Retourne un objet qui implémente l’interface spécifiée pour autoriser l’accès à la [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)]-des méthodes spécifiques.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
public <T> T unwrap(Class<T> iface)  
```  
  
#### <a name="parameters"></a>Paramètres  
 *iface*  
  
 Une classe de type **T** définissant une interface.  
  
## <a name="return-value"></a>Valeur retournée  
 Objet qui implémente l'interface spécifiée.  
  
## <a name="exceptions"></a>Exceptions  
 [SQLServerException](../../../connect/jdbc/reference/sqlserverexception-class.md)  
  
## <a name="remarks"></a>Notes  
 Le [unwrap](../../../connect/jdbc/reference/unwrap-method-sqlserverpreparedstatement.md) méthode est définie par l’interface java.sql.Wrapper, introduite dans les spécifications de JDBC 4.0.  
  
 Les applications devront peut-être accéder à des extensions de l’API JDBC qui sont spécifiques à la [!INCLUDE[jdbcNoVersion](../../../includes/jdbcnoversion_md.md)]. La méthode unwrap prend en charge la Désencapsulation dans les classes publiques par cet objet, si les classes exposent des extensions de fournisseur.  
  
 Lorsque cette méthode est appelée, l’objet se désencapsule dans les classes suivantes : [SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-class.md) et [SQLServerPreparedStatement](../../../connect/jdbc/reference/sqlserverpreparedstatement-class.md).  
  
 Par exemple de code, consultez [unwrap méthode &#40; SQLServerCallableStatement &#41; ](../../../connect/jdbc/reference/unwrap-method-sqlservercallablestatement.md).  
  
 Pour plus d’informations, consultez [Wrappers et Interfaces](../../../connect/jdbc/wrappers-and-interfaces.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Méthode isWrapperFor &#40; SQLServerPreparedStatement &#41;](../../../connect/jdbc/reference/iswrapperfor-method-sqlserverpreparedstatement.md)   
 [Membres de SQLServerPreparedStatement](../../../connect/jdbc/reference/sqlserverpreparedstatement-members.md)   
 [SQLServerPreparedStatement, classe](../../../connect/jdbc/reference/sqlserverpreparedstatement-class.md)  
  
  
