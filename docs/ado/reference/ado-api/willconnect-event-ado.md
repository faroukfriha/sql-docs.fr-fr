---
title: "WillConnect, événement (ADO) | Documents Microsoft"
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
apitype: COM
f1_keywords:
- WillConnect
- Connection::WillConnect
helpviewer_keywords:
- WillConnect event [ADO]
ms.assetid: da561d58-eb58-446c-a4fd-1838c76073c0
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: f80b08a53784a215d58d7f36697207f4d8c3c942
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2018
---
# <a name="willconnect-event-ado"></a>WillConnect, événement (ADO)
Le **WillConnect** événement est appelé avant le début d’une connexion.  
  
 **S’applique à :** [objet de connexion (ADO)](../../../ado/reference/ado-api/connection-object-ado.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
WillConnect ConnectionString, UserID, Password, Options, adStatus, pConnection  
```  
  
#### <a name="parameters"></a>Paramètres  
 *ConnectionString*  
 A **chaîne** qui contient les informations de connexion pour la connexion en attente.  
  
 *UserID*  
 A **chaîne** qui contient un nom d’utilisateur pour la connexion en attente.  
  
 *Mot de passe*  
 A **chaîne** qui contient un mot de passe pour la connexion en attente.  
  
 *Options*  
 A **Long** valeur qui indique la manière dont le fournisseur doit évaluer le *ConnectionString*. La seule option disponible est **adAsyncOpen**.  
  
 *adStatus*  
 Un [il ne](../../../ado/reference/ado-api/eventstatusenum.md) valeur d’état.  
  
 Lorsque cet événement est appelé, ce paramètre est défini **adStatusOK** par défaut. Il est défini sur **adStatusCantDeny** si l’événement ne peut pas demander l’annulation de l’opération en attente.  
  
 Avant le retour de cet événement, définissez ce paramètre sur **adStatusUnwantedEvent** pour éviter toute notification. Définissez ce paramètre sur **adStatusCancel** pour demander l’opération de connexion qui a provoqué l’annulation de cette notification.  
  
 *pConnection*  
 Le [connexion](../../../ado/reference/ado-api/connection-object-ado.md) de l’objet pour lequel cette notification d’événement s’applique. Modifications apportées aux paramètres de la **connexion** par le **WillConnect** Gestionnaire d’événements n’a aucun effet le **connexion**.  
  
## <a name="remarks"></a>Notes  
 Lorsque **WillConnect** est appelée, le *ConnectionString*, *UserID*, *mot de passe*, et *Options* les paramètres sont définis aux valeurs établies par l’opération qui a provoqué cet événement (la connexion en attente) et peut être modifiée avant le retour de l’événement. **WillConnect** peut retourner une demande d’annulation de la connexion en attente.  
  
 Lorsque cet événement est annulé, **ConnectComplete** sera appelé avec son *ne* paramètre la valeur **contraire**.  
  
## <a name="see-also"></a>Voir aussi  
 [Exemple de modèle d’événements ADO (VC ++)](../../../ado/reference/ado-api/ado-events-model-example-vc.md)   
 [Présentation rapide du gestionnaire d’événements ADO](../../../ado/guide/data/ado-event-handler-summary.md)
