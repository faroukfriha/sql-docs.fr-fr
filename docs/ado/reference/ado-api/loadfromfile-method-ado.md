---
title: "LoadFromFile, méthode (ADO) | Documents Microsoft"
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
- _Stream::raw_LoadFromFile
helpviewer_keywords:
- LoadFromFile method [ADO]
ms.assetid: b18d8d38-7354-4a94-b637-6ac035faa433
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 071ba2d6a2aa5af96af07274455a7495a9650dea
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2018
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile, méthode (ADO)
Charge le contenu d’un fichier existant dans un [flux](../../../ado/reference/ado-api/stream-object-ado.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
Stream.LoadFromFileFileName  
```  
  
#### <a name="parameters"></a>Paramètres  
 *FileName*  
 A **chaîne** valeur qui contient le nom d’un fichier doit être chargé dans le **flux**. *Nom de fichier* peut contenir un chemin d’accès valide et un nom au format UNC. Si le fichier spécifié n’existe pas, une erreur d’exécution se produit.  
  
## <a name="remarks"></a>Notes  
 Cette méthode peut être utilisée pour charger le contenu d’un fichier local dans un **flux** objet. Cela permet de télécharger le contenu d’un fichier local sur un serveur.  
  
 Le **flux** objet doit être déjà ouvert avant d’appeler **LoadFromFile**. Cette méthode ne modifie pas la liaison de la **flux** de l’objet ; il sera toujours lié à l’objet spécifié par l’URL ou **enregistrement** avec lequel le **flux** était à l’origine ouvert.  
  
 **LoadFromFile** remplace le contenu actuel de la **flux** objet avec les données lues à partir du fichier. Tous les octets dans le **flux** sont remplacés par le contenu du fichier. Tous les octets restants et précédemment existants suivant le [fin du support](../../../ado/reference/ado-api/eos-property.md) créé par **LoadFromFile**, sont tronqués.  
  
 Après un appel à **LoadFromFile**, la position actuelle est définie au début de la **flux** ([Position](../../../ado/reference/ado-api/position-property-ado.md) est 0).  
  
 Étant donné que les 2 octets peuvent être ajoutés au début du flux de données pour l’encodage, la taille du flux de données peut différer la taille du fichier à partir duquel il a été chargé.  
  
## <a name="applies-to"></a>S'applique à  
 [Stream, objet (ADO)](../../../ado/reference/ado-api/stream-object-ado.md)
