---
title: "Sources de données de fichiers | Documents Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: odbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- data sources [ODBC], file
- file data sources [ODBC]
ms.assetid: db245c80-981a-4638-bd03-69d04bc67af0
caps.latest.revision: "6"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 1fa8f72d601130df15f73e856f676b07bf8f0e52
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="file-data-sources"></a>Sources de données fichier
*Sources de données de fichiers* sont stockées dans un fichier et d’autoriser les informations de connexion à utiliser à plusieurs reprises par un utilisateur unique ou partagé par plusieurs utilisateurs. Lorsqu’une source de données de fichier est utilisée, le Gestionnaire de pilotes établit la connexion à la source de données en utilisant les informations dans un fichier .dsn. Ce fichier peut être manipulé comme tout autre fichier. Une source de données de fichier n’a pas de nom de source de données, que les sources de données machine et n’est pas inscrit à n’importe quel ordinateur ou d’un utilisateur.  
  
 Une source de données de fichiers simplifie le processus de connexion, car le fichier .dsn contient la chaîne de connexion qui aurait sinon générés pour un appel à la **SQLDriverConnect** (fonction). Un autre avantage du fichier .dsn est qu’il peut être copié vers n’importe quel ordinateur, pour les sources de données identiques puissent être utilisées par nombreux ordinateurs tant qu’ils ont le pilote approprié installé. Une source de données de fichier peut également être partagée par les applications. Une source de données de fichiers partageables permettre placée sur un réseau et utilisée simultanément par plusieurs applications.  
  
 Un fichier .dsn peut également être partageable. Un fichier .dsn partageable réside sur un seul ordinateur et pointe vers une source de données d’ordinateur. Sources de données fichier partageable existent principalement pour autorise la conversion de facile de sources de données aux sources de données de fichier afin qu’une application peut être conçue pour fonctionner uniquement avec les sources de données fichier. Lorsque le Gestionnaire de pilotes est envoyé les informations dans une source de données fichier partageable, il se connecte que nécessaire pour la source de données machine qui pointe le fichier .dsn.  
  
 Pour plus d’informations sur les sources de données de fichier, consultez [la connexion à l’aide de Sources de données](../../odbc/reference/develop-app/connecting-using-file-data-sources.md), ou [SQLDriverConnect](../../odbc/reference/syntax/sqldriverconnect-function.md) description de fonction.
