---
title: "Connexion à SQL Server | Microsoft Docs"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: integration-services
ms.service: 
ms.component: change-data-capture
ms.reviewer: 
ms.suite: sql
ms.technology:
- integration-services
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5bb582f9-68d3-4c1e-ab02-6fc16807f1a5
caps.latest.revision: 
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 407f460db78042ace1a13052b561fb678f451f86
ms.sourcegitcommit: 9e6a029456f4a8daddb396bc45d7874a43a47b45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2018
---
# <a name="connection-to-sql-server"></a>Connexion à SQL Server
  Quand une connexion sans rôle de base de données qui inclut l’autorisation d’accès en écriture (par exemple le rôle **db_owner**) à la base de données MSXDBCDC tente de créer une instance Oracle CDC, la boîte de dialogue Connexion à SQL Server s’affiche.  
  
 Dans cette boîte de dialogue, vous devez entrer les informations d’identification pour une connexion qui dispose d’une autorisation d’accès en écriture à la base de données MSXDBCDC (tel est notamment le cas du rôle de base de données **db_owner** ) pour créer l’instance Oracle CDC.  
  
 Dans la boîte de dialogue Connexion à SQL Server, entrez les informations suivantes :  
  
### <a name="server-name"></a>Nom du serveur  
 Tapez le nom du serveur où se trouve [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] .  
  
### <a name="authentication"></a>Authentification  
 Sélectionnez l'une des options suivantes :  
  
-   Authentification Windows  
  
-   **Authentification SQL Server**: si vous sélectionnez cette option, vous devez taper **l’identifiant** et le **mot de passe** de l’utilisateur dans l’instance [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] à laquelle vous vous connectez.  
  
### <a name="options"></a>Options  
 Cliquez sur la flèche pour afficher les options disponibles à configurer. Vous pouvez choisir de conserver ces options avec leur valeur par défaut. Options disponibles :  
  
-   **Délai de connexion**: Tapez le délai (en secondes) pendant lequel le programme attend une connexion à [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] avant de générer une erreur de délai d’expiration. La valeur par défaut est **15**.  
  
-   **Délai d’exécution**: Tapez le délai (en secondes) pendant lequel le programme attend la fin d’exécution d’une commande SQL avant de générer une erreur de délai d’expiration. La valeur par défaut est **30**.  
  
-   **Chiffrer la connexion**: Sélectionnez **Chiffrer la connexion** pour garantir que la connexion [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] établie est chiffrée afin d’assurer la protection des données.  
  
-   **Avancé**: cliquez sur **Avancé** et tapez toutes les propriétés de connexion supplémentaires dans la boîte de dialogue Propriétés avancées de connexion, si nécessaire.  
  
## <a name="see-also"></a> Voir aussi  
 [Autorisations de connexion SQL Server requises pour le service de capture de données modifiées](../../integration-services/change-data-capture/sql-server-connection-required-permissions-for-the-cdc-service.md)  
  
  
