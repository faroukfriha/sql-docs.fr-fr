---
title: syscollector_collection_items (Transact-SQL) | Documents Microsoft
ms.custom: 
ms.date: 03/03/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: system-catalog-views
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- syscollector_collection_items_TSQL
- syscollector_collection_items
dev_langs:
- TSQL
helpviewer_keywords:
- syscollector_collection_items view
- add data collector view
ms.assetid: a279ecd1-a59c-4315-9f08-bf221f00a465
caps.latest.revision: 
author: stevestein
ms.author: sstein
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: ca9b8aed18c716e235d1848d7130395cf4fe7875
ms.sourcegitcommit: c556eaf60a49af7025db35b7aa14beb76a8158c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2018
---
# <a name="syscollectorcollectionitems-transact-sql"></a>syscollector_collection_items (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Retourne des informations sur un élément dans un jeu d'éléments de collecte.  
  
|Nom de colonne|Type de données| Description|  
|-----------------|---------------|-----------------|  
|**collection_set_id**|**int**|Identifie le jeu d'éléments de collecte. N'accepte pas la valeur NULL.|  
|**collection_item_id**|**int**|Identifie un élément dans le jeu d'éléments de collecte. N'accepte pas la valeur NULL.|  
|**collector_type_uid**|**uniqueidentifier**|GUID utilisé pour identifier le type de collecteur. N'accepte pas la valeur NULL.|  
|**nom**|**nvarchar(4000)**|Nom du jeu d'éléments de collecte. Autorise la valeur NULL.|  
|**frequency**|**int**|Fréquence à laquelle les données sont recueillies par un élément de collecte. N'accepte pas la valeur NULL.|  
|**parameters**|**xml**|Décrit le paramétrage du type de collecteur associé à l'élément de collecte. Le schéma XML pour cet élément de collecte est validé avec le schéma XML (XSD) stocké dans le **parameter_schema** pour un type de collecteur particulier. Autorise la valeur NULL. Pour plus d’informations, consultez [syscollector_collector_types &#40; Transact-SQL &#41; ](../../relational-databases/system-catalog-views/syscollector-collector-types-transact-sql.md).|  
  
## <a name="permissions"></a>Autorisations  
 Nécessite l’autorisation SELECT pour **dc_operator**, **dc_proxy**.  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures stockées du collecteur de données &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/data-collector-stored-procedures-transact-sql.md)   
 [Vues du collecteur de données &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/data-collector-views-transact-sql.md)   
 [Collecte de données](../../relational-databases/data-collection/data-collection.md)  
  
  
