---
title: "Résoudre les problèmes liés aux travaux multiserveurs qui utilisent des proxys | Microsoft Docs"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: sql-tools
ms.service: 
ms.component: ssms-agent
ms.reviewer: 
ms.suite: sql
ms.technology:
- tools-ssms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- proxies [SQL Server Agent], multiserver jobs
- jobs [SQL Server Agent], multiserver jobs using proxies
ms.assetid: fc579bd3-010c-4f72-8b5c-d0cc18a1f280
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: ccf7f0b4eb9817aef38420111bb0ac2e7ce7bf2a
ms.sourcegitcommit: d8ab09ad99e9ec30875076acee2ed303d61049b7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2018
---
# <a name="troubleshoot-multiserver-jobs-that-use-proxies"></a>Résoudre les problèmes liés aux travaux multiserveurs qui utilisent des proxys
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md](../../includes/appliesto-ss-xxxx-xxxx-xxx-md.md)]
Les travaux distribués dont les étapes sont associées à un proxy s'exécutent dans le contexte du compte proxy sur le serveur cible. Si les étapes de travail utilisant des comptes proxy échouent lors du téléchargement à partir du serveur maître, consultez la colonne **error_message** de la table **sysdownloadlist** dans la base de données **msdb** pour y rechercher les messages d’erreur suivants :  
  
-   « L'étape du travail nécessite un compte proxy, cependant la mise en correspondance de proxy est désactivée sur le serveur cible. »  
  
    Pour résoudre cette erreur, définissez la sous-clé de Registre **\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server\MSSQL.***\<n*>**\SQLServerAgent\AllowDownloadedJobsToMatchProxyName** sur **1 (true)**. Par défaut, la valeur de cette sous-clé est **0** (**false**). La valeur de **MSSQL.**\<*n*> est le nom de l’instance, par exemple, **MSSQL.1** ou **MSSQL.3**.  
  
-   « Proxy introuvable. »  
  
    Un compte proxy sur le serveur cible doit porter le même nom que le compte proxy de serveur maître avec lequel l'étape du travail s'exécute.  
  
> [!CAUTION]  
> [!INCLUDE[ssNoteRegistry](../../includes/ssnoteregistry_md.md)]  
  
## <a name="see-also"></a> Voir aussi  
[Créer un environnement multi-serveur](../../ssms/agent/create-a-multiserver-environment.md)  
  
