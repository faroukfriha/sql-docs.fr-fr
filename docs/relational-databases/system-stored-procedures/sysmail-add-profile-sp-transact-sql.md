---
title: sysmail_add_profile_sp (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-stored-procedures
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- sysmail_add_profile_sp_TSQL
- sysmail_add_profile_sp
dev_langs:
- TSQL
helpviewer_keywords:
- sysmail_add_profile_sp
ms.assetid: a828e55c-633a-41cf-9769-a0698b446e6c
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 6295b1f239f136c43e00e047186ce408ab9a4a93
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="sysmailaddprofilesp-transact-sql"></a>sysmail_add_profile_sp (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Crée un nouveau profil de messagerie de base de données.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
sysmail_add_profile_sp [ @profile_name = ] 'profile_name'  
    [ , [ @description = ] 'description' ]  
    [ , [ @profile_id = ] new_profile_id OUTPUT ]  
```  
  
## <a name="arguments"></a>Arguments  
 [  **@profile_name**  =] **'***profile_name***'**  
 Nom du nouveau profil. *profile_name* est **sysname**, sans valeur par défaut.  
  
 [ **@description** = ] **'***description***'**  
 Description facultative du nouveau profil. *Description* est **nvarchar (256)**, sans valeur par défaut.  
  
 [  **@profile_id**  =] *new_profile_id *** sortie**  
 Retourne l'ID du nouveau profil. *new_profile_id* est **int**, avec NULL comme valeur par défaut.  
  
## <a name="return-code-values"></a>Valeurs des codes de retour  
 **0** (réussite) ou **1** (échec)  
  
## <a name="remarks"></a>Notes  
 Un profil de messagerie de base de données contient un nombre quelconque de comptes de messagerie de base de données. Les procédures stockées de la messagerie de base de données peuvent faire référence à un profil par son nom ou par l'ID généré par cette procédure. Pour plus d’informations sur l’ajout d’un compte à un profil, consultez [sysmail_add_profileaccount_sp &#40; Transact-SQL &#41; ](../../relational-databases/system-stored-procedures/sysmail-add-profileaccount-sp-transact-sql.md).  
  
 Le nom du profil et la description peuvent être modifiés avec la procédure stockée **sysmail_update_profile_sp**, alors que l’id de profil reste constante pour la durée de vie du profil.  
  
 Le nom du profil doit être unique pour Microsoft [!INCLUDE[ssDEnoversion](../../includes/ssdenoversion-md.md)] ou la procédure stockée renvoie une erreur.  
  
 La procédure stockée **sysmail_add_profile_sp** est dans le **msdb** de base de données et est détenue par le **dbo** schéma. La procédure doit être exécutée avec un nom en trois parties si la base de données actuelle n’est pas **msdb**.  
  
## <a name="permissions"></a>Autorisations  
 Autorisations d’exécution de cette procédure reviennent par défaut aux membres de la **sysadmin** rôle serveur fixe.  
  
## <a name="examples"></a>Exemples  
 **A. Création d’un profil**  
  
 L'exemple ci-dessous crée un profil de messagerie de base de données nommé `AdventureWorks Administrator`.  
  
```  
EXECUTE msdb.dbo.sysmail_add_profile_sp  
       @profile_name = 'AdventureWorks Administrator',  
       @description = 'Profile used for administrative mail.' ;  
```  
  
 **B. Création d’un profil, l’enregistrement de l’id de profil dans une variable**  
  
 L'exemple ci-dessous crée un profil de messagerie de base de données nommé `AdventureWorks Administrator`. L'exemple stocke l'ID du profil dans la variable `@profileId` et retourne un jeu de résultats contenant l'ID du nouveau profil.  
  
```  
DECLARE @profileId INT ;  
  
EXECUTE msdb.dbo.sysmail_add_profile_sp  
       @profile_name = 'AdventureWorks Administrator',  
       @description = 'Profile used for administrative mail.',  
       @profile_id = @profileId OUTPUT ;  
  
SELECT @profileId ;  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Messagerie de base de données](../../relational-databases/database-mail/database-mail.md)   
 [Créer un compte de messagerie de base de données](../../relational-databases/database-mail/create-a-database-mail-account.md)   
 [Objets de Configuration de messagerie de base de données](../../relational-databases/database-mail/database-mail-configuration-objects.md)   
 [Messagerie de base de données stockée procédures &#40; Transact-SQL &#41;](../../relational-databases/system-stored-procedures/database-mail-stored-procedures-transact-sql.md)  
  
  
