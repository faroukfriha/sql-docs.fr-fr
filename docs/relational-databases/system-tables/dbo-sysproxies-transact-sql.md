---
title: dbo.sysproxies (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-tables
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- dbo.sysproxies_TSQL
- sysproxies_TSQL
- dbo.sysproxies
- sysproxies
dev_langs:
- TSQL
helpviewer_keywords:
- sysproxies system table
ms.assetid: a73da875-be22-45fc-b5e2-ea7ebd48e2d6
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 9a1e16809177b6bec502493d03527343fecf6923
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="dbosysproxies-transact-sql"></a>dbo.sysproxies (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Définit les attributs d'un compte proxy de l'agent [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Cette table est stockée dans le **msdb** base de données.  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**proxy_id**|**int**|ID du compte proxy.|  
|**nom**|**sysname**|Nom du compte proxy.|  
|**credential_id**|**int**|ID des informations d'identification utilisées par le compte proxy.|  
|**enabled**|**tinyint**|État du compte proxy :<br /><br /> **0** = désactivé. **1** = activé.|  
|**description**|**nvarchar(512)**|Description entrée par l'utilisateur lors de la création du compte proxy.|  
|**user_sid**|**varbinary(85)**|Microsoft Windows *identificateur_sécurisé* de l’utilisateur ou le groupe associé à l’information d’identification de proxy.|  
|**credential_date_created**|**datetime**|Date et heure de création des informations d'identification.|  
  
## <a name="remarks"></a>Notes  
 Seuls les membres de la **sysadmin** rôle serveur fixe peut accéder à la **sysproxies** table.  
  
## <a name="see-also"></a>Voir aussi  
 [dbo.sysproxylogin &#40;Transact-SQL&#41;](../../relational-databases/system-tables/dbo-sysproxylogin-transact-sql.md)   
 [dbo.sysproxysubsystem &#40;Transact-SQL&#41;](../../relational-databases/system-tables/dbo-sysproxysubsystem-transact-sql.md)   
 [dbo.syssubsystems &#40;Transact-SQL&#41;](../../relational-databases/system-tables/dbo-syssubsystems-transact-sql.md)  
  
  
