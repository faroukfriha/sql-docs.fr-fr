---
title: Positionnement de Recordset | Documents Microsoft
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: ado
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: sql
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- record positioning [ADO]
- Recordset object [ADO]
- repositioning record [ADO]
- AbsolutePosition property [ADO]
ms.assetid: c8f6fbcb-6675-4133-b37e-430de43949c1
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 3c5b7e11012d4efc94bf4924a6390b1cfbd68195
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2018
---
# <a name="recordset-positioning"></a>Positionnement du jeu d’enregistrements
Utilisez le **AbsolutePosition** propriété pour accéder à un enregistrement, en fonction de sa position ordinale dans la **Recordset** objet, ou pour déterminer la position ordinale de l’enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour cette propriété doit être disponible.  
  
 **AbsolutePosition** basé sur 1 et est égale à 1 lorsque l’enregistrement actif est le premier enregistrement de la **Recordset**. Comme mentionné précédemment, vous pouvez obtenir le nombre total d’enregistrements dans la **Recordset** de l’objet à partir de la **RecordCount** propriété.  
  
 Lorsque vous définissez la **AbsolutePosition** propriété, même si elle est à un enregistrement dans le cache actif, ADO recharge le cache avec un nouveau groupe d’enregistrements en commençant par l’enregistrement que vous avez spécifié. Le **CacheSize** propriété détermine la taille de ce groupe.  
  
> [!NOTE]
>  Vous ne devez pas utiliser le **AbsolutePosition** propriété en tant que numéro d’enregistrement de substitution. La position d’un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Il n’existe également aucune assurance qu’un enregistrement donné auront le même **AbsolutePosition** si le **Recordset** objet est actualisé ou rouvert. Les signets sont le moyen recommandé de conserver et revenir à une position donnée et constituent la seule manière de se positionner dans tous les types de **Recordset** objets.
