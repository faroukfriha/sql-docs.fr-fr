---
title: Sys.dm_cryptographic_provider_sessions (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 06/10/2016
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
- sys.dm_cryptographic_provider_sessions
- dm_cryptographic_provider_sessions_TSQL
- sys.dm_cryptographic_provider_sessions_TSQL
- dm_cryptographic_provider_sessions
dev_langs:
- TSQL
helpviewer_keywords:
- sys.dm_cryptographic_provider_sessions dynamic management function
ms.assetid: 9a4de02b-1a07-4850-979a-0861fddb7f9d
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 8b60590005ab185f4f03256a0e3845d9a4a61bee
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="sysdmcryptographicprovidersessions-transact-sql"></a>sys.dm_cryptographic_provider_sessions (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Retourne des informations sur les sessions ouvertes d'un fournisseur de chiffrement.  
 
## <a name="syntax"></a>Syntaxe  
  
```  
  
sys.dm_cryptographic_provider_sessions(session_identifier)  
```  
  
## <a name="arguments"></a>Arguments  
 *session_identifier*  
 Entier indiquant les sessions à retourner.  
  
 0 = connexion en cours uniquement  
  
 1 = toutes les connexions de chiffrement  
  
## <a name="table-returned"></a>Table retournée  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**provider_id**|**int**|Numéro d'identification du fournisseur de services de chiffrement.|  
|**session_handle**|**varbytes(8)**|Descripteur de session de chiffrement.|  
|**identity**|**nvarchar(128)**|Identité utilisée pour l'authentification auprès du fournisseur de chiffrement.|  
|**spid**|**short**|ID de session (SPID) de la connexion. Pour plus d’informations, consultez [@@SPID &#40; Transact-SQL &#41; ](../../t-sql/functions/spid-transact-sql.md).|  
  
## <a name="remarks"></a>Notes  
 Le **sys.dm_cryptographic_provider_sessions** est visible au public pour la connexion actuelle. Pour afficher toutes les connexions de chiffrement, vous devez avoir le **contrôle** autorisation de serveur.  
  
## <a name="see-also"></a>Voir aussi  
 [Affichages catalogue de sécurité &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/security-catalog-views-transact-sql.md)   
 [Gestion de clés extensible &#40;EKM&#41;](../../relational-databases/security/encryption/extensible-key-management-ekm.md)   
 [CREATE CRYPTOGRAPHIC PROVIDER &#40;Transact-SQL&#41;](../../t-sql/statements/create-cryptographic-provider-transact-sql.md)   
 [Hiérarchie de chiffrement](../../relational-databases/security/encryption/encryption-hierarchy.md)  
  
  
