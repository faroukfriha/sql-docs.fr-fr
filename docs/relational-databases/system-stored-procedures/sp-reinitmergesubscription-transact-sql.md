---
title: sp_reinitmergesubscription (Transact-SQL) | Documents Microsoft
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
- sp_reinitmergesubscription_TSQL
- sp_reinitmergesubscription
helpviewer_keywords:
- sp_reinitmergesubscription
ms.assetid: 249a4048-e885-48e0-a92a-6577f59de751
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 5b801376850844a0e1cba0e5b53b72114c0199f7
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="spreinitmergesubscription-transact-sql"></a>sp_reinitmergesubscription (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Signale un abonnement de fusion en vue de sa réinitialisation lors de la prochaine exécution de l’Agent de fusion. Cette procédure stockée est exécutée dans la base de données de publication du serveur de publication.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
sp_reinitmergesubscription [ [ @publication = ] 'publication'  
    [ , [ @subscriber = ] 'subscriber'  
    [ , [ @subscriber_db = ] 'subscriber_db'  
    [ , [ @upload_first = ] 'upload_first'  
```  
  
## <a name="arguments"></a>Arguments  
 [  **@publication =** ] **'***publication***'**  
 Nom de la publication. *publication* est **sysname**, avec une valeur par défaut **tous les**.  
  
 [  **@subscriber =** ] **'***abonné***'**  
 Nom de l'Abonné. *abonné* est **sysname**, avec une valeur par défaut **tous les**.  
  
 [  **@subscriber_db =** ] **'***bd_abonné***'**  
 Nom de la base de données de l'Abonné. *bd_abonné* est **sysname**, avec une valeur par défaut **tous les**.  
  
 [  **@upload_first =** ] **'***upload_first***'**  
 Indique si les modifications effectuées sur l'Abonné sont chargées avant la réinitialisation de l'abonnement. *upload_first* est **nvarchar (5)**, avec FALSE comme valeur par défaut. Si **true**, modifications sont téléchargées avant la réinitialisation de l’abonnement. Si **false**, modifications ne sont pas téléchargées.  
  
## <a name="return-code-values"></a>Valeurs des codes de retour  
 **0** (réussite) ou **1** (échec)  
  
## <a name="remarks"></a>Notes  
 **sp_reinitmergesubscription** est utilisé dans la réplication de fusion.  
  
 **sp_reinitmergesubscription** peut être appelée à partir du serveur de publication pour réinitialiser les abonnements de fusion. Il est recommandé de réexécuter également l'Agent d'instantané.  
  
 Si vous ajoutez, supprimez ou modifiez un filtre paramétré, les modifications en attente chez l'abonné ne peuvent pas être chargées sur le serveur de publication pendant la réinitialisation. Si vous voulez télécharger les modifications en attente, synchronisez tous les abonnements avant de modifier le filtre.  
  
## <a name="example"></a>Exemple  
 [!code-sql[HowTo#sp_reinitmergepushsub](../../relational-databases/replication/codesnippet/tsql/sp-reinitmergesubscripti_1.sql)]  
  
## <a name="example"></a>Exemple  
 [!code-sql[HowTo#sp_reinitmergepushsubwithupload](../../relational-databases/replication/codesnippet/tsql/sp-reinitmergesubscripti_2.sql)]  
  
## <a name="permissions"></a>Permissions  
 Seuls les membres de la **sysadmin** rôle serveur fixe ou **db_owner** du rôle de base de données fixe peut exécuter **sp_reinitmergesubscription**.  
  
## <a name="see-also"></a>Voir aussi  
 [Réinitialiser des abonnements](../../relational-databases/replication/reinitialize-subscriptions.md)   
 [Procédures stockées système &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md)  
  
  
