---
title: Diagnostics | Documents Microsoft
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
- diagnostic information [ODBC]
- functions [ODBC], diagnostic information
- diagnostic information [ODBC], about diagnostic information
ms.assetid: 450abd88-90a1-4fbc-b417-8efbdd8e1dea
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: efbc34be3dc532b329863a98305952d90adcc9f5
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="diagnostics"></a>Diagnostics
Fonctions dans ODBC retournent des informations de diagnostic de deux manières. Le code de retour indique la réussite ou l’échec de la fonction globale, tandis que les enregistrements de diagnostic fournissent des informations détaillées sur la fonction. Au moins un enregistrement de diagnostic : l’enregistrement d’en-tête, est retourné même si la fonction réussit.  
  
 Informations de diagnostic sont utilisées au moment du développement pour intercepter les erreurs de programmation telles que les handles non valides et des erreurs de syntaxe dans les instructions SQL codées en dur. Il est utilisé au moment de l’exécution pour intercepter les erreurs d’exécution et les avertissements telles que la troncation de données, les violations d’accès et les erreurs de syntaxe dans les instructions SQL saisies par l’utilisateur.  
  
 Cette section contient les rubriques suivantes.  
  
-   [Codes de retour](../../../odbc/reference/develop-app/return-codes-odbc.md)  
  
-   [Enregistrements de diagnostic](../../../odbc/reference/develop-app/diagnostic-records.md)  
  
-   [Utilisation de SQLGetDiagRec et de SQLGetDiagField](../../../odbc/reference/develop-app/using-sqlgetdiagrec-and-sqlgetdiagfield.md)  
  
-   [Implémentation de SQLGetDiagRec et de SQLGetDiagField](../../../odbc/reference/develop-app/implementing-sqlgetdiagrec-and-sqlgetdiagfield.md)  
  
-   [Exemples de gestion des diagnostics](../../../odbc/reference/develop-app/diagnostic-handling-examples.md)
