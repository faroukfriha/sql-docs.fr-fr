---
title: "Actualiser à partir de la base de données (MySQLToSQL) | Documents Microsoft"
ms.prod: sql-non-specified
ms.prod_service: sql-tools
ms.service: 
ms.component: ssma-mysql
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.technology: sql-ssma
ms.tgt_pltfrm: 
ms.topic: article
applies_to:
- Azure SQL Database
- SQL Server
ms.assetid: 59a6db8f-2db6-4071-9005-928a7231de92
caps.latest.revision: "4"
author: Shamikg
ms.author: Shamikg
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 18656f8929e52d23e10ccc5fafe8139544bf44a5
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="refresh-from-database-mysqltosql"></a>Actualiser à partir de la base de données (MySQLToSQL)
Le **Actualiser à partir de la base de données** boîte de dialogue vous permet de sélectionner les objets à actualiser à partir de la base de données MySQL. Lignes dans la boîte de dialogue sont codées par couleur en fonction de l’état des métadonnées :  
  
-   Si les métadonnées de l’objet a été modifié localement et dans la base de données MySQL, la ligne est bleue.  
  
-   Si les métadonnées de l’objet a été modifié dans la base de données MySQL, mais pas dans SSMA, la ligne est jaune.  
  
-   Si les métadonnées de l’objet a été modifié localement, mais pas dans la base de données MySQL, la ligne est verte.  
  
-   Si l’objet est nouveau dans la base de données MySQL, la ligne est rose.  
  
Vous pouvez spécifier des paramètres d’actualisation objet par défaut dans le **les paramètres de projet** boîte de dialogue. Pour plus d’informations, consultez [paramètres du projet &#40; Synchronisation &#41; &#40; MySQLToSQL &#41;](../../ssma/mysql/project-settings-synchronization-mysqltosql.md)  
  
Pour accéder à la **Actualiser à partir de la base de données** boîte de dialogue, avec le bouton droit, un objet dans l’Explorateur de métadonnées MySQL et cliquez sur **Actualiser à partir de la base de données**.  
  
## <a name="options"></a>Options  
  
|||  
|-|-|  
|**Terme**|**Définition**|  
|**Réduction (-)**|Réduire tous les groupes d’objets pour masquer les objets individuels.|  
|**Développement (+)**|Développez tous les groupes d’objets pour afficher les objets individuels.|  
|**Afficher/masquer les objets égales**|Masquer les objets dans la liste si les métadonnées de l’objet sont le même dans la base de données MySQL et SSMA.|  
|**Actualiser à partir de la base de données (flèche)**|Utilisez le bouton fléché pour spécifier que les métadonnées pour les objets sélectionnés doivent être mis à jour dans SSMA.|  
|**Effectuez pas actualiser à partir de la base de données (bouton) X**|Utilisez le bouton X pour spécifier que les métadonnées pour les objets sélectionnés ne doivent pas mis à jour dans SSMA.|  
|**Légende**|Affiche un **légende** boîte de dialogue. La légende contient le mappage entre les États de métadonnées et les couleurs de ligne.<br /><br />Pour conserver le **légende** boîte de dialogue sur le **Actualiser à partir de la base de données** boîte de dialogue, sélectionnez le **afficher en haut** case à cocher.|  
  
