---
title: SUSER_NAME (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: sql-data-warehouse, sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- SUSER_NAME
- SUSER_NAME_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- security identification names [SQL Server]
- logins [SQL Server], users
- identification names for logins [SQL Server]
- users [SQL Server], logins
- SUSER_NAME function
- logins [SQL Server], names
- names [SQL Server], logins
ms.assetid: ae598d9f-9baa-49b8-b1c1-042854206de4
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: cb236dc3ae7f74ad77ba398e328d4a0bf93a079b
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="susername-transact-sql"></a>SUSER_NAME (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-asdw-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-asdw-xxx-md.md)]

  Retourne le nom d'identification de l'utilisateur pour la connexion.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
SUSER_NAME ( [ server_user_id ] )   
```  
  
## <a name="arguments"></a>Arguments  
 *server_user_id*  
 Correspond au numéro d'identification de la connexion de l'utilisateur. *server_user_id*, facultatif, est de type **int**. *server_user_id* peut être le numéro d’identification d’une connexion [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ou d’un utilisateur ou d’un groupe Windows [!INCLUDE[msCoName](../../includes/msconame-md.md)] quelconque qui a l’autorisation de se connecter à une instance de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]. Si *server_user_id* n’est pas spécifié, le nom d’identification de connexion de l’utilisateur actuel est renvoyé. Si le paramètre contient le mot NULL, retourne NULL.  
  
## <a name="return-types"></a>Types de retour  
 **nvarchar(128)**  
  
## <a name="remarks"></a>Notes   
 Dans [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 7.0, le numéro d'identification de sécurité (SID, Security Identification Number) remplace le numéro d'identification de l'utilisateur du serveur (SUID, Server User Identification Number).  
  
 La fonction SUSER_NAME renvoie un nom de connexion seulement pour une connexion comportant une entrée dans la table système **syslogins**.  
  
 SUSER_NAME peut être utilisée dans la liste de sélection, au sein d'une clause WHERE et n'importe où une expression est autorisée, et doit toujours être suivie par des parenthèses (même si aucun paramètre n'est indiqué).  
  
## <a name="examples"></a>Exemples  
 Dans l'exemple suivant, la procédure retourne le nom d'identification de la connexion utilisateur `1`.  
  
```  
SELECT SUSER_NAME(1);  
```  
  
## <a name="see-also"></a> Voir aussi  
 [SUSER_ID &#40;Transact-SQL&#41;](../../t-sql/functions/suser-id-transact-sql.md)   
 [Principaux &#40;moteur de base de données&#41;](../../relational-databases/security/authentication-access/principals-database-engine.md)  
  
  
