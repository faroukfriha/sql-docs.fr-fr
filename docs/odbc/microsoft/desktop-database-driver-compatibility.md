---
title: "Compatibilité des pilotes de bureau de base de données | Documents Microsoft"
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
- compatibility [ODBC], Unicode
- Unicode [ODBC], desktop database drivers
- ODBC desktop database drivers [ODBC], Unicode
- backward compatibility [ODBC], Unicode
- desktop database drivers [ODBC], Unicode
- Jet-based ODBC drivers [ODBC], Unicode
ms.assetid: dd695638-1a0b-4e27-8a6a-9510ebb5a5ee
caps.latest.revision: "7"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: fcb8ad39a2ba24890394bb05cb30f1ddb5b63d2e
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="desktop-database-driver-compatibility"></a>Compatibilité de pilote de base de données de bureau
Unicode est une méthode d’encodage de caractères logiciel traite tous les caractères comme ayant une largeur fixe de deux octets. Cette méthode est utilisée comme alternative à l’encodage de caractères Windows ANSI, qui, car il représente les caractères dans un seul octet, est limitée à 256 caractères. Étant donné que Unicode peut représenter plus de 65 000 caractères, il prend en charge plusieurs langues dont les caractères ne sont pas représentés au format ANSI.  
  
 Le Gestionnaire de pilotes ODBC 3.5 (ou version ultérieure) prend en charge Unicode. Cela affecte les deux zones principales : appels de fonction et les types de données string. Arguments de chaîne du Gestionnaire de pilotes maps (fonction) les données de type chaîne comme requis par l’application et le pilote, qui peuvent être soit compatibles Unicode ou compatible ANSI.  
  
 Le Gestionnaire de pilotes ODBC 3.5 (ou version ultérieure) prend en charge l’utilisation d’un pilote Unicode avec une application Unicode et une application ANSI. Il prend également en charge l’utilisation d’un pilote ANSI avec une application ANSI. Le Gestionnaire de pilotes fournit un mappage de Unicode en ANSI limitée pour une application Unicode fonctionne avec un pilote ANSI. Cela permet d’accéder aux bases de données Jet 3.5 et prise en charge de tous les types de fichier ISAM existants.  
  
 Quand une application ANSI utilise le pilote de base de données ODBC Desktop 4.0 et accède à Microsoft Access 4.0 ou une version ultérieure, le pilote présente le type de données en tant que SQL_CHAR, SQL_VARCHAR ou SQL_LONGVARCHAR bien Jet 4.0 prend en charge la version large. Des versions antérieures de Jet ne prennent pas en charge SQL_WCHAR, SQL_WVARCHAR et SQL_WLONGVARCHAR. Cette restriction s’applique également dans les cas où les anciens formats sont utilisés avec le moteur de base de données Jet 4.0.  
  
 Pour plus d’informations concernant les problèmes d’Unicode avec ODBC, consultez [Unicode](../../odbc/reference/develop-app/unicode.md) dans les considérations relatives à la programmation.
