---
title: MSrepl_version (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/04/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-tables
ms.reviewer: 
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- MSrepl_version
- MSrepl_version_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSrepl_version system table
ms.assetid: c1330f03-940b-4564-ac42-6030c6e21173
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 1a170e197a11ac002584ea8083cd4ec4a3f089bd
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="msreplversion-transact-sql"></a>MSrepl_version (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Le **MSrepl_version** table contient une ligne avec la version actuelle de la réplication installée. Cette table est stockée dans la base de données de distribution.  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**version_principale**|**int**|Numéro de version majeure de la base de données de distribution|  
|**version_secondaire**|**int**|Numéro de version mineure de la base de données de distribution|  
|**révision**|**int**|Numéro de révision.|  
|**db_existed**|**bit**|Indique si la base de données de distribution existe avant **sp_adddistributiondb** est appelée.|  
  
## <a name="see-also"></a>Voir aussi  
 [Tables de réplication &#40; Transact-SQL &#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Vues de réplication &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
