---
title: ENCRYPTBYASYMKEY (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- ENCRYPTBYASYMKEY
- ENCRYPTBYASYMKEY_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- ENCRYPTBYASYMKEY function
- encryption [SQL Server], asymmetric keys
- asymmetric keys [SQL Server], ENCRYPTBYASYMKEY function
ms.assetid: 86bb2588-ab13-4db2-8f3c-42c9f572a67b
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 6ef212d976ca8f84881695d85e56f5ab1cbca020
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="encryptbyasymkey-transact-sql"></a>ENCRYPTBYASYMKEY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Chiffre les données avec une clé asymétrique.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
EncryptByAsymKey ( Asym_Key_ID , { 'plaintext' | @plaintext } )  
```  
  
## <a name="arguments"></a>Arguments  
 *Asym_Key_ID*  
 ID d'une clé asymétrique dans la base de données. **int**.  
  
 *cleartext*  
 Chaîne de données qui seront chiffrées avec la clé asymétrique.  
  
 **@plaintext**  
 Variable de type **nvarchar**, **char**, **varchar**, **binary**, **varbinary** ou **nchar** qui contient des données à chiffrer avec la clé asymétrique.  
  
## <a name="return-types"></a>Types de retour  
 **varbinary** d’une taille maximale de 8 000 octets.  
  
## <a name="remarks"></a>Notes   
 Le chiffrement et le déchiffrement avec une clé asymétrique sont coûteux par rapport au chiffrement et au déchiffrement avec une clé symétrique. Il est déconseillé d'utiliser une clé asymétrique pour chiffrer des ensembles de données volumineux ; par exemple, des données utilisateur issues de tables. Utilisez plutôt une clé symétrique forte pour chiffrer les données, et chiffrez la clé symétrique à l'aide d'une clé asymétrique.  
  
 **EncryptByAsymKey** renvoie **NULL** si l'entrée dépasse un certain nombre d'octets, selon l'algorithme. Les limites sont : une clé RSA de 512 bits peut chiffrer jusqu'à 53 octets, une clé de 1 024 bits peut chiffrer jusqu'à 117 octets, et une clé de 2 048 bits peut chiffrer jusqu'à 245 octets. (Notez que dans [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], les certificats et les clés asymétriques sont des wrappers de clés RSA.)  
  
## <a name="examples"></a>Exemples  
 L'exemple suivant chiffre le texte stocké dans `@cleartext` à l'aide de la clé asymétrique `JanainaAsymKey02`. Les données chiffrées sont insérées dans la table `ProtectedData04`.  
  
```  
INSERT INTO AdventureWorks2012.Sales.ProtectedData04   
    VALUES( N'Data encrypted by asymmetric key ''JanainaAsymKey02''',  
    EncryptByAsymKey(AsymKey_ID('JanainaAsymKey02'), @cleartext) );  
GO  
```  
  
## <a name="see-also"></a> Voir aussi  
 [DECRYPTBYASYMKEY &#40;Transact-SQL&#41;](../../t-sql/functions/decryptbyasymkey-transact-sql.md)   
 [CREATE ASYMMETRIC KEY &#40;Transact-SQL&#41;](../../t-sql/statements/create-asymmetric-key-transact-sql.md)   
 [Hiérarchie de chiffrement](../../relational-databases/security/encryption/encryption-hierarchy.md)  
  
  
