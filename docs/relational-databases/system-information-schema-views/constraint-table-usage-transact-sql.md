---
title: CONSTRAINT_TABLE_USAGE (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/15/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: system-information-schema-views
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- CONSTRAINT_TABLE_USAGE_TSQL
- CONSTRAINT_TABLE_USAGE
dev_langs:
- TSQL
helpviewer_keywords:
- CONSTRAINT_TABLE_USAGE view
- INFORMATION_SCHEMA.CONSTRAINT_TABLE_USAGE view
ms.assetid: 5770b696-6c04-4d5c-a8db-9eb92022fa42
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 74b4c55aafb5830eee79a2ec0498750a0f07b5dd
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="constrainttableusage-transact-sql"></a>CONSTRAINT_TABLE_USAGE (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Renvoie une ligne pour chaque table de la base de données active pour laquelle une contrainte est définie dans cette table. Cette vue de schémas d'informations renvoie des informations sur les objets pour lesquels l'utilisateur actuel dispose d'autorisations.  
  
 Pour récupérer des informations à partir de ces vues, spécifiez le nom qualifié complet de **INFORMATION_SCHEMA.** *view_name*.  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**TABLE_CATALOG**|**nvarchar (**128**)**|Qualificateur de la table.|  
|**TABLE_SCHEMA**|**nvarchar (**128**)**|Nom du schéma qui contient la table.<br /><br /> **\*\*Important \* \***  n’utilisez pas les vues INFORMATION_SCHEMA pour déterminer le schéma d’un objet. La seule méthode fiable pour rechercher le schéma d’un objet est d’interroger l’affichage catalogue sys.objects.|  
|**NOM_TABLE**|**sysname**|Nom de la table.|  
|**CONSTRAINT_CATALOG**|**nvarchar (**128**)**|Qualificateur de la contrainte.|  
|**CONSTRAINT_SCHEMA**|**nvarchar (**128**)**|Nom du schéma qui contient la contrainte.<br /><br /> **\*\*Important \* \***  n’utilisez pas les vues INFORMATION_SCHEMA pour déterminer le schéma d’un objet. La seule méthode fiable pour rechercher le schéma d’un objet est d’interroger l’affichage catalogue sys.objects.|  
|**CONSTRAINT_NAME**|**sysname**|Nom de la contrainte.|  
  
## <a name="see-also"></a>Voir aussi  
 [Vues système &#40; Transact-SQL &#41;](http://msdn.microsoft.com/library/35a6161d-7f43-4e00-bcd3-3091f2015e90)   
 [Vues de schémas d’informations &#40; Transact-SQL &#41;](~/relational-databases/system-information-schema-views/system-information-schema-views-transact-sql.md)   
 [Sys.Objects &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md)   
 [Sys.CHECK_CONSTRAINTS &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-check-constraints-transact-sql.md)   
 [Sys.key_constraints &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-key-constraints-transact-sql.md)   
 [Sys.Foreign_Keys &#40; Transact-SQL &#41;](../../relational-databases/system-catalog-views/sys-foreign-keys-transact-sql.md)  
  
  
