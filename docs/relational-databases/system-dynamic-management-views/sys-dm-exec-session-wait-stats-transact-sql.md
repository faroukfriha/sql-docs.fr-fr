---
title: sys.dm_exec_session_wait_stats (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 02/01/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: dmv's
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- sys.dm_exec_session_wait_stats
- sys.dm_exec_session_wait_stats_tsql
- dm_exec_session_wait_stats
- dm_exec_session_wait_stats_tsql
helpviewer_keywords:
- sys.dm_exec_session_wait_stats
ms.assetid: df84842a-71eb-4fda-b448-5953cf9985dc
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: 73dcc552a70ba68d7beff38ed0476b1970feefca
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="sysdmexecsessionwaitstats-transact-sql"></a>sys.dm_exec_session_wait_stats (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2016-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2016-xxxx-xxxx-xxx-md.md)]

  Retourne des informations sur toutes les attentes des threads exécutés pour chaque session. Vous pouvez utiliser cette vue pour diagnostiquer les problèmes de performances avec la [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] session ainsi qu’avec des requêtes spécifiques et des traitements.  Cette vue renvoie session les mêmes informations rassemblées pour [sys.dm_os_wait_stats &#40; Transact-SQL &#41; ](../../relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql.md) , mais elles fournissent le **session_id** également.  
  
**S’applique à**: [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] (de[!INCLUDE[ssSQL15](../../includes/sssql15-md.md)] à [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)]).  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|session_id|**smallint**|L’id de la session.|  
|wait_type|**nvarchar(60)**|Nom du type d'attente. Pour plus d’informations, consultez [sys.dm_os_wait_stats &#40; Transact-SQL &#41; ](../../relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql.md).|  
|waiting_tasks_count|**bigint**|Nombre d'attentes sur ce type d'attente. Ce compteur est incrémenté au début de chaque attente.|  
|wait_time_ms|**bigint**|Temps d'attente total en millisecondes pour ce type d'attente. Ce temps comprend signal_wait_time_ms.|  
|max_wait_time_ms|**bigint**|Temps d'attente maximal sur ce type d'attente.|  
|signal_wait_time_ms|**bigint**|Différence entre le moment où le thread qui attend a été signalé et le moment où il a commencé à s'exécuter.|  
  
## <a name="remarks"></a>Notes  
 Cette DMV réinitialise les informations pour une session lorsque la session est ouverte, ou lorsque la session est réinitialisée (si le regroupement de connexions),  
  
 Pour plus d’informations sur les types d’attente, consultez [sys.dm_os_wait_stats &#40; Transact-SQL &#41; ](../../relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql.md).  
  
## <a name="permissions"></a>Autorisations  
 Si l’utilisateur a **VIEW SERVER STATE** autorisation sur le serveur, l’utilisateur voit en cours d’exécution toutes les sessions sur l’instance de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]; sinon, l’utilisateur voit uniquement la session active.  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions et vues de gestion dynamique &#40;Transact-SQL&#41;](~/relational-databases/system-dynamic-management-views/system-dynamic-management-views.md)   
 [Système d’exploitation de serveur SQL relatives des vues de gestion dynamique &#40; Transact-SQL &#41;](../../relational-databases/system-dynamic-management-views/sql-server-operating-system-related-dynamic-management-views-transact-sql.md)   
 [sys.dm_os_wait_stats &#40;Transact-SQL&#41;](../../relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql.md)  
 
