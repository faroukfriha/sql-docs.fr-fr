---
title: Utilisez le pilote ODBC de FoxPro VFP avec votre Application Visual Basic | Documents Microsoft
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
- Visual FoxPro ODBC driver [ODBC], visual basic applications
- Visual Basic applications [ODBC]
- FoxPro ODBC driver [ODBC], visual basic applications
- Visual FoxPro data [ODBC], visual basic applications
ms.assetid: 5223ca23-5df6-4ebc-aa3b-70682ff27a8c
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 266577d54e579956fcc2435283a9835c19f9ef36
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="using-the-vfp-foxpro-odbc-driver-with-your-visual-basic-application"></a>À l’aide du pilote ODBC de FoxPro VFP avec votre Application Visual Basic
Application de votre Microsoft® Visual Basic® peut communiquer avec les données Visual FoxPro en créant un contrôle de données qui se connecte à une source de données Visual FoxPro.  
  
#### <a name="to-connect-to-visual-foxpro-data-using-the-data-control-in-visual-basic"></a>Se connecter aux données Visual FoxPro à l’aide du contrôle de données en Visual Basic  
  
1.  Créer une source de données nommée « test » qui se connecte à la base de données exemple TasTrade inclus dans Visual FoxPro. L’installation de Visual FoxPro par défaut place la base de données exemple TasTrade dans l’emplacement :  
  
    ```  
    c:\vfp\samples\mainsamp\data\tastrade.dbc  
    ```  
  
2.  En Visual Basic, créez un nouveau formulaire et placez une zone de texte et un contrôle de données sur ce dernier.  
  
3.  Modifiez la propriété de connexion du contrôle de données comme suit :  
  
    ```  
    ODBC;DATABASE=tastrade;DSN=test  
    ```  
  
4.  Modifiez la propriété RecordsetType comme suit :  
  
    ```  
    2 - Snapshot  
    ```  
  
5.  Modifiez la propriété source comme suit :  
  
    ```  
    customer  
    ```  
  
6.  Modifier la propriété de source de données pour la zone de texte pour le nom par défaut pour le contrôle de données pour les éléments suivants :  
  
    ```  
    data1  
    ```  
  
7.  Modifier la propriété DataField de la zone de texte pour les éléments suivants :  
  
    ```  
    customer_id  
    ```  
  
8.  Exécutez le formulaire et utilisez le contrôle de données à ignorer dans les champs d’id de client à partir de la base de données Visual FoxPro TasTrade.
