---
title: "Fonctions statistiques système (Transact-SQL) | Microsoft Docs"
ms.custom: 
ms.date: 03/15/2017
ms.prod: sql-non-specified
ms.prod_service: sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- statistical functions [SQL Server]
- system statistical functions [SQL Server]
- functions [SQL Server], statistical
ms.assetid: 45828c67-1b9a-4653-bb24-86246084d8ba
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: On Demand
ms.openlocfilehash: c5b437038aa63c4e0ae1a5d5f0a8ef2b435cde66
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="system-statistical-functions-transact-sql"></a>Fonctions statistiques système (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-xxxx-xxxx-xxx-md](../../includes/tsql-appliesto-ss2012-xxxx-xxxx-xxx-md.md)]

  Les fonctions scalaires suivantes retournent des informations statistiques relatives au système :  
  
|||  
|-|-|  
|[@@CONNECTIONS](../../t-sql/functions/connections-transact-sql.md)|[@@PACK_RECEIVED](../../t-sql/functions/pack-received-transact-sql.md)|  
|[@@CPU_BUSY](../../t-sql/functions/cpu-busy-transact-sql.md)|[@@PACK_SENT](../../t-sql/functions/pack-sent-transact-sql.md)|  
|[fn_virtualfilestats](../../relational-databases/system-functions/sys-fn-virtualfilestats-transact-sql.md)|[@@TIMETICKS](../../t-sql/functions/timeticks-transact-sql.md)|  
|[@@IDLE](../../t-sql/functions/idle-transact-sql.md)|[@@TOTAL_ERRORS](../../t-sql/functions/total-errors-transact-sql.md)|  
|[@@IO_BUSY](../../t-sql/functions/io-busy-transact-sql.md)|[@@TOTAL_READ](../../t-sql/functions/total-read-transact-sql.md)|  
|[@@PACKET_ERRORS](../../t-sql/functions/packet-errors-transact-sql.md)|[@@TOTAL_WRITE](../../t-sql/functions/total-write-transact-sql.md)|  
  
 Toutes les fonctions statistiques système sont non déterministes. Cela signifie qu'elles ne renvoient pas toujours les mêmes résultats chaque fois qu'elles sont appelées, même avec un ensemble identique de valeurs d'entrée. Pour plus d’informations sur le déterminisme des fonctions, consultez [Fonctions déterministes et non déterministes](../../relational-databases/user-defined-functions/deterministic-and-nondeterministic-functions.md).  
  
## <a name="see-also"></a> Voir aussi  
 [Fonctions intégrées &#40;Transact-SQL&#41;](~/t-sql/functions/functions.md)  
  
  
