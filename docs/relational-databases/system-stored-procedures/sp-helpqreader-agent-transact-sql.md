---
title: sp_helpqreader_agent (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/04/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-stored-procedures
ms.reviewer: 
ms.suite: sql
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: language-reference
applies_to:
- SQL Server
f1_keywords:
- sp_helpqreader_agent_TSQL
- sp_helpqreader_agent
helpviewer_keywords:
- sp_helpqreader_agent
ms.assetid: 8e74e1aa-e95b-4183-8017-bf123439b08d
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 50492a76e742459e7b883f9887026d0ce63d1eb1
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="sphelpqreaderagent-transact-sql"></a>sp_helpqreader_agent (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Retourne les propriétés de l'Agent de lecture de la file d'attente. Cette procédure stockée est exécutée sur la base de données de distribution du serveur de distribution ou sur toute base de données du serveur de publication.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
sp_helpqreader_agent [ [ @frompublisher = ] frompublisher ]  
```  
  
## <a name="arguments"></a>Arguments  
 [  **@frompublisher=** ] *frompublisher*  
 Indique si la procédure stockée est appelée sur le serveur de publication ou sur le serveur de distribution. *frompublisher* est de type bit, avec 0 comme valeur par défaut. **1** signifie que la procédure stockée est appelée à partir du serveur de publication, et **0** signifie que la procédure stockée est appelée depuis le serveur de distribution.  
  
## <a name="result-sets"></a>Jeux de résultats  
  
|Nom de colonne|Type de données|Description|  
|-----------------|---------------|-----------------|  
|**id**|**int**|ID de l’agent.|  
|**nom**|**nvarchar (100)**|Nom de l'Agent.|  
|**job_id**|**uniqueidentifier**|ID unique du travail de l'Agent.|  
|**job_login**|**nvarchar(512)**|Est le compte Windows sous lequel l’agent de Distribution s’exécute, ce qui est retourné sous la forme *domaine*\\*nom d’utilisateur*.|  
|**job_password**|**sysname**|Pour des raisons de sécurité, une valeur  **\* \* \* \* \* \* \* \* \* \***  est toujours retournée.|  
  
## <a name="return-code-values"></a>Valeurs des codes de retour  
 **0** (réussite) ou **1** (échec)  
  
## <a name="remarks"></a>Notes  
 **sp_helpqreader_agent** est utilisé dans la réplication transactionnelle.  
  
## <a name="permissions"></a>Permissions  
 Lorsque la valeur de *frompublisher* est **1**, seuls les membres de la **sysadmin** rôle serveur fixe sur le serveur de publication ou les membres de la **db_owner** du rôle de base de données fixe sur la base de données de publication permettre exécuter **sp_helpqreader_agent**. Sinon, seuls les membres de la **sysadmin** rôle serveur fixe sur le serveur de distribution ou les membres de la **db_owner** du rôle de base de données fixe sur la base de données de distribution permettre exécuter **sp_helpqreader_agent**.  
  
## <a name="see-also"></a>Voir aussi  
 [Activer les abonnements de mise à jour pour les publications transactionnelles](../../relational-databases/replication/publish/enable-updating-subscriptions-for-transactional-publications.md)  
  
  
