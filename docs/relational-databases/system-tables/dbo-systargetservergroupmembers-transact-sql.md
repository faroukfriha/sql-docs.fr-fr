---
title: dbo.systargetservergroupmembers (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-tables
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- dbo.systargetservergroupmembers_TSQL
- dbo.systargetservergroupmembers
- systargetservergroupmembers
- systargetservergroupmembers_TSQL
dev_langs: TSQL
helpviewer_keywords: systargetservergroupmembers system table
ms.assetid: ee1b2ebd-03cb-4b91-a5d2-98d4d38f82ec
caps.latest.revision: "24"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 4e3fa531c546d8262d91c798047cfb00413e813d
ms.sourcegitcommit: 66bef6981f613b454db465e190b489031c4fb8d3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2017
---
# <a name="dbosystargetservergroupmembers-transact-sql"></a>dbo.systargetservergroupmembers (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  Enregistre les serveurs cibles qui sont actuellement inscrits dans ce groupe multiserveur.  
  
||  
|-|  
|**S’applique à**: [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ([!INCLUDE[ssKatmai](../../includes/sskatmai-md.md)] jusqu’à [version actuelle](http://go.microsoft.com/fwlink/p/?LinkId=299658)).|  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**servergroup_id**|**int**|Identificateur du groupe de serveurs.|  
|**server_id**|**int**|ID du serveur.|  
  
  