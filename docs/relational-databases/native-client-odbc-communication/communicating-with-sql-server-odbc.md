---
title: Communication avec SQL Server (ODBC) | Documents Microsoft
ms.custom: 
ms.date: 03/16/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: native-client-odbc-communication
ms.reviewer: 
ms.suite: sql
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- SQL Server Native Client ODBC driver, communicating with SQL Server
- ODBC applications, communicating with SQL Server
- ODBC, communicating with SQL Server
ms.assetid: cca3dcf0-2a7e-465a-84de-7ce055360eb6
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: 5f242a14087e2387ae8aa8baab91ef43a5ccca39
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2018
---
# <a name="communicating-with-sql-server-odbc"></a>Communication avec SQL Server (ODBC)
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

  Pour une application ODBC communiquer avec une instance de [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], elle doit allouer d’environnement et gère de connexion et se connecter à la source de données. Après avoir établi une connexion, l'application peut envoyer des requêtes au serveur et traiter tous les jeux de résultats. Lorsque l'application a terminé d'utiliser la source de données, elle se déconnecte de la source de données et libère le handle de connexion. Lorsque l'application a libéré tous ses handles de connexion, elle libère le handle d'environnement.  
  
 Une application peut se connecter à un nombre quelconque de sources de données. L'application peut utiliser une combinaison de pilotes et de sources de données, le même pilote et une combinaison de sources de données, voire le même pilote et plusieurs connexions à la même source de données.  
  
 Vous pouvez télécharger [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] des exemples ODBC Native Client à partir de la [téléchargements SQL Server](http://go.microsoft.com/fwlink/?LinkId=62796) page sur MSDN.  
  
## <a name="in-this-section"></a>Dans cette section  
  
-   [Allocation d’un descripteur d’environnement](../../relational-databases/native-client-odbc-communication/allocating-an-environment-handle.md)  
  
-   [Allocation d’un descripteur de connexion](../../relational-databases/native-client-odbc-communication/allocating-a-connection-handle.md)  
  
-   [Sources de données ODBC SQL Server Native Client](../../relational-databases/native-client-odbc-communication/sql-server-native-client-odbc-data-sources.md)  
  
-   [Connexion à une Source de données &#40; ODBC &#41;](../../relational-databases/native-client-odbc-communication/connecting-to-a-data-source-odbc.md)  
  
-   [Déconnexion d’une source de données](../../relational-databases/native-client-odbc-communication/disconnecting-from-a-data-source.md)  
  
## <a name="see-also"></a>Voir aussi  
 [SQL Server Native Client &#40; ODBC &#41;](../../relational-databases/native-client/odbc/sql-server-native-client-odbc.md)   
 [SQLSetEnvAttr](../../relational-databases/native-client-odbc-api/sqlsetenvattr.md)  
  
  
