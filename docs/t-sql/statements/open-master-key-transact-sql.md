---
title: OPEN MASTER KEY (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- OPEN MASTER KEY DECRYPTION BY PASSWORD
- OPEN_MASTER_KEY_DECRYPTION_BY_PASSWORD_TSQL
- MASTER_KEY_TSQL
- MASTER KEY
- OPEN_MASTER_KEY_TSQL
- MASTER KEY DECRYPTION
- OPEN MASTER KEY
- MASTER_KEY_DECRYPTION_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- opening Database Master Keys
- encryption [SQL Server], Database Master Key
- cryptography [SQL Server], Database Master Key
- master key decryption
- OPEN MASTER KEY statement
- database master key [SQL Server], opening
ms.assetid: 1674753e-ca1e-4913-9ba4-b442e7106121
caps.latest.revision: 31
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 3ef9e8331c891a6087e55b4eb70b19dda4057bf2
ms.contentlocale: fr-fr
ms.lasthandoff: 09/01/2017

---
# <a name="open-master-key-transact-sql"></a>OPEN MASTER KEY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Ouvre la clé principale de base de données de la base de données active.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-- Syntax for SQL Server, Azure SQL Database, Azure SQL Data Warehouse, Parallel Data Warehouse  
  
OPEN MASTER KEY DECRYPTION BY PASSWORD = 'password'   
```  
  
## <a name="arguments"></a>Arguments  
 '*mot de passe*'  
 Mot de passe utilisé pour le chiffrement de la clé principale de la base de données.  
  
## <a name="remarks"></a>Notes  
 Si cette clé a été chiffrée avec la clé principale du service, elle est automatiquement ouverte lorsqu'elle doit être utilisée pour du chiffrement ou du déchiffrement. Dans ce cas, il n’est pas nécessaire d’utiliser le **OPEN MASTER KEY** instruction.  
  
 Lorsqu'une base de données est attachée ou restaurée pour la première fois à une nouvelle instance de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], une copie de la clé principale de la base de données (chiffrée par la clé principale du service) n'est pas encore stockée sur le serveur. Vous devez utiliser l’instruction **OPEN MASTER KEY** pour déchiffrer la clé principale de la base de données. Une fois la clé principale de la base de données déchiffrée, vous avez la possibilité d’activer le déchiffrement automatique dans le futur en exécutant l’instruction **ALTER MASTER KEY REGENERATE** pour fournir au serveur une copie de la clé principale de la base de données chiffrée avec la clé principale du service. Lorsqu'une base de données a été mise à niveau à partir d'une version antérieure, la clé DMK doit être régénérée de façon à utiliser le nouvel algorithme AES. Pour plus d’informations sur la régénération de la clé DMK, consultez [ALTER MASTER KEY &#40;Transact-SQL&#41;](../../t-sql/statements/alter-master-key-transact-sql.md). La durée nécessaire pour régénérer la clé DMK à mettre à niveau vers AES dépend du nombre d'objets protégés par la clé DMK. La régénération de la clé DMK à mettre à niveau vers AES est nécessaire une seule fois et n'a aucune incidence sur les régénérations ultérieures effectuées dans le cadre d'une stratégie de rotation de clés.  
  
 Vous pouvez exclure la clé principale d'une base de données spécifique de la gestion de clés automatique en utilisant l'instruction ALTER MASTER KEY avec l'option DROP ENCRYPTION BY SERVICE MASTER KEY. Après quoi, vous devez ouvrir explicitement la clé principale de la base de données avec un mot de passe.  
  
 Si une transaction dans laquelle la clé principale de la base de données a été explicitement ouverte est annulée, la clé reste ouverte.  
  
## <a name="permissions"></a>Permissions  
 Requiert l'autorisation CONTROL sur la base de données.  
  
## <a name="examples"></a>Exemples  
 L'exemple suivant ouvre la clé principale de la base de données `AdventureWorks2012`, chiffrée avec un mot de passe.  
  
```  
USE AdventureWorks2012;  
OPEN MASTER KEY DECRYPTION BY PASSWORD = '43987hkhj4325tsku7';  
GO  
```  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Exemples : [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] et[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
 L’exemple suivant ouvre la base de données master, ce qui a été chiffré avec un mot de passe.  
  
```  
USE master;  
OPEN MASTER KEY DECRYPTION BY PASSWORD = '43987hkhj4325tsku7';  
GO  
CLOSE MASTER KEY;  
GO  
```  
  
## <a name="see-also"></a>Voir aussi  
 [CREATE MASTER KEY &#40;Transact-SQL&#41;](../../t-sql/statements/create-master-key-transact-sql.md)   
 [CLOSE MASTER KEY &#40; Transact-SQL &#41;](../../t-sql/statements/close-master-key-transact-sql.md)   
 [BACKUP MASTER KEY &#40; Transact-SQL &#41;](../../t-sql/statements/backup-master-key-transact-sql.md)   
 [RESTORE MASTER KEY &#40; Transact-SQL &#41;](../../t-sql/statements/restore-master-key-transact-sql.md)   
 [ALTER MASTER KEY &#40;Transact-SQL&#41;](../../t-sql/statements/alter-master-key-transact-sql.md)   
 [DROP MASTER KEY &#40; Transact-SQL &#41;](../../t-sql/statements/drop-master-key-transact-sql.md)   
 [Hiérarchie de chiffrement](../../relational-databases/security/encryption/encryption-hierarchy.md)  
  
  

