---
title: "State, propriété (classe SqlService) | Documents Microsoft"
ms.custom: 
ms.date: 03/04/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine
ms.service: 
ms.component: wmi
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: reference
apiname:
- State Property (SqlService Class)
apilocation:
- sqlmgmproviderxpsp2up.mof
apitype: MOFDef
helpviewer_keywords:
- State property
ms.assetid: 9e09f419-947c-4d4b-9a49-2d3396c847cd
caps.latest.revision: 
author: CarlRabeler
ms.author: carlrab
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 19751c0def878b510834b53442048562a2b5c835
ms.sourcegitcommit: 0d904c23663cebafc48609671156c5ccd8521315
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2018
---
# <a name="state-property-sqlservice-class"></a>Propriété State (classe SqlService)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx-md](../../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]
  Obtient ou définit l'état actuel du service.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
object.State [= value]  
```  
  
## <a name="parts"></a>Éléments  
 *objet*  
 Objet de [classe SqlService](../../../relational-databases/wmi-provider-configuration-classes/sqlservice-class/sqlservice-class.md) qui représente le service.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 Valeur uint32 qui spécifie l'état du service.  
  
 Il peut s'agir de l'une des valeurs suivantes.  
  
 1  
 Arrêté. Le service est arrêté.  
  
 2  
 Démarrage en attente. Le service est en attente de démarrage.  
  
 3  
 Arrêt en attente. Le service est en attente d'arrêt.  
  
 4  
 En cours d'exécution. Le service est en cours d'exécution.  
  
 5  
 Continuation en attente. Le service est en attente de continuation.  
  
 6  
 Pause en attente. Le service est en attente de pause.  
  
 7  
 Suspendu. Le service est suspendu.  
  
## <a name="remarks"></a>Notes  
  
## <a name="see-also"></a>Voir aussi  
 [Démarrage et arrêt des Services](http://technet.microsoft.com/library/ms174886\(v=sql.105\).aspx)  
  
  
