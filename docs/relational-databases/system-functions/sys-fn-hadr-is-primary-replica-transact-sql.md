---
title: sys.fn_hadr_is_primary_replica (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/17/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- sys.fn_hadr_is_primary_replica
- fn_hadr_is_primary_replica_TSQL
- fn_hadr_is_primary_replica
- sys.fn_hadr_is_primary_replica_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- fn_hadr_is_primary_replica
- sys.fn_hadr_is_primary_replica
ms.assetid: c9b1969f-be1d-4dfb-a33d-551f380b9e27
caps.latest.revision: 
author: MikeRayMSFT
ms.author: mikeray
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: f2a09533a82fad640bbdc9867bf54c9edef1a0b7
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="sysfnhadrisprimaryreplica-transact-sql"></a>sys.fn_hadr_is_primary_replica (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2014-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2014-xxxx-xxxx-xxx-md.md)]

  Utilisé pour déterminer si le réplica actuel est le réplica principal par défaut.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
sys.fn_hadr_is_primary_replica ( 'dbname' )  
```  
  
## <a name="arguments"></a>Arguments  
 '*dbname*'  
 Nom de la base de données. *dbname* est de type sysname.  
  
## <a name="returns"></a>Valeur renvoyée  
 Retourne 1 si la base de données sur l'instance actuelle est le réplica principal par défaut. Dans le cas contraire, retourne la valeur 0.  
  
## <a name="remarks"></a>Notes  
 Utilisez cette fonction pour déterminer aisément si l'instance locale héberge le réplica principal de la base de données de disponibilité spécifiée. L'exemple de code devrait ressembler à ce qui suit :  
  
```  
If sys.fn_hadr_is_primary_replica ( @dbname ) <> 1   
BEGIN  
-- If this is not the primary replica, exit (probably without error).  
END  
-- If this is the primary replica, continue to do the backup.  
  
```  
  
## <a name="examples"></a>Exemples  
  
### <a name="a-using-sysfnhadrisprimaryreplica"></a>A. Utilisation de sys.fn_hadr_is_primary_replica  
 L'exemple suivant retourne 1 si la base de données spécifiée sur l'instance locale est le réplica principal.  
  
```  
SELECT sys.fn_hadr_is_primary_replica ('TestDB');  
GO  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions &#40; groupes de disponibilité AlwaysOn Transact-SQL &#41;](../../relational-databases/system-functions/always-on-availability-groups-functions-transact-sql.md)   
 [Groupes de disponibilité AlwaysOn &#40; SQL Server &#41;](../../database-engine/availability-groups/windows/always-on-availability-groups-sql-server.md)   
 [CREATE AVAILABILITY GROUP &#40;Transact-SQL&#41;](../../t-sql/statements/create-availability-group-transact-sql.md)   
 [ALTER AVAILABILITY GROUP &#40;Transact-SQL&#41;](../../t-sql/statements/alter-availability-group-transact-sql.md)   
 [Affichages catalogue &#40; groupes de disponibilité AlwaysOn Transact-SQL &#41;](../../relational-databases/system-catalog-views/always-on-availability-groups-catalog-views-transact-sql.md)  
  
  
