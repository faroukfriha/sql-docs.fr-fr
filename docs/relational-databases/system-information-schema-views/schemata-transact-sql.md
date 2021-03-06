---
title: "SCHÉMAS (Transact-SQL) | Documents Microsoft"
ms.custom: 
ms.date: 09/08/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: system-information-schema-views
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- SCHEMATA_TSQL
- SCHEMATA
dev_langs:
- TSQL
helpviewer_keywords:
- INFORMATION_SCHEMA.SCHEMATA view
- SCHEMATA view
ms.assetid: 69617642-0f54-4b25-b62f-5f39c8909601
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: ac71e5f401f0eb411f7356d8bc4c15fa0a57c901
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="schemata-transact-sql"></a>SCHEMATA (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all-md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Renvoie une ligne pour chaque schéma de la base de données active. Pour récupérer des informations à partir de ces vues, spécifiez le nom qualifié complet de **INFORMATION_SCHEMA.** *view_name*. Pour récupérer des informations sur toutes les bases de données dans une instance de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)], requête le [sys.databases &#40; Transact-SQL &#41; ](../../relational-databases/system-catalog-views/sys-databases-transact-sql.md) affichage catalogue.  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**CATALOG_NAME**|**sysname**|Nom de la base de données active|  
|**SCHEMA_NAME**|**nvarchar (**128**)**|Renvoie le nom du schéma|  
|**SCHEMA_OWNER**|**nvarchar (**128**)**|Nom du propriétaire du schéma<br /><br /> **\*\*Important \* \***  n’utilisez pas les vues INFORMATION_SCHEMA pour déterminer le schéma d’un objet. La seule méthode fiable pour rechercher le schéma d'un objet est d'interroger l'affichage catalogue sys.objects.|  
|**DEFAULT_CHARACTER_SET_CATALOG**|**varchar (**6**)**|Retourne toujours la valeur Null.|  
|**DEFAULT_CHARACTER_SET_SCHEMA**|**varchar (**3**)**|Retourne toujours la valeur Null.|  
|**DEFAULT_CHARACTER_SET_NAME**|**sysname**|Renvoie le nom du jeu de caractères par défaut|  

**Exemple**  
L’exemple suivant, retourne des informations sur les schémas dans la base de données master :  
```sql  
SELECT * FROM master.INFORMATION_SCHEMA.SCHEMATA;
```  

## <a name="see-also"></a>Voir aussi  
 [Vues système &#40; Transact-SQL &#41;](http://msdn.microsoft.com/library/35a6161d-7f43-4e00-bcd3-3091f2015e90)   
 [Vues de schémas d’informations &#40; Transact-SQL &#41;](~/relational-databases/system-information-schema-views/system-information-schema-views-transact-sql.md)   
 [sys.databases &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-databases-transact-sql.md)   
 [Sys.Schemas &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/schemas-catalog-views-sys-schemas.md)   
 [Sys.syscharsets &#40; Transact-SQL &#41;](../../relational-databases/system-compatibility-views/sys-syscharsets-transact-sql.md)  
  
  
