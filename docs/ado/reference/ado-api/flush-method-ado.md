---
title: "Flush (méthode) (ADO) | Documents Microsoft"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- _Stream::Flush
- _Stream::raw_Flush
helpviewer_keywords:
- Flush method [ADO]
ms.assetid: 938522b4-f836-4c80-8d27-a598a000f0ee
caps.latest.revision: 13
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: dc0e90c43b2f691f1dff705e813ffe77fe5fc35a
ms.contentlocale: fr-fr
ms.lasthandoff: 09/09/2017

---
# <a name="flush-method-ado"></a>Flush (méthode) (ADO)
Force le contenu de la [flux](../../../ado/reference/ado-api/stream-object-ado.md) restants dans la mémoire tampon d’ADO à l’objet sous-jacent avec lequel le **flux** est associé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
Stream.Flush  
```  
  
## <a name="remarks"></a>Notes  
 Cette méthode peut être utilisée pour envoyer le contenu de la mémoire tampon de flux de données à l’objet sous-jacent : par exemple, le nœud ou le fichier représenté par l’URL qui est la source de la **flux** objet. Cette méthode doit être appelée lorsque vous souhaitez vous assurer que toutes les modifications qui ont été apportées au contenu d’un **flux** ont été écrits. Toutefois, avec ADO il est généralement pas nécessaire d’appeler **vider**, comme ADO vide continuellement sa mémoire tampon autant que possible en arrière-plan. Modifications du contenu d’un **flux** sont effectuées automatiquement, non mis en cache jusqu'à ce que **vider** est appelée.  
  
 Fermeture un **flux** avec la [fermer](../../../ado/reference/ado-api/close-method-ado.md) méthode vide le contenu d’un **flux** automatiquement ; il n’est pas nécessaire d’appeler explicitement **vider**immédiatement avant **fermer**.  
  
## <a name="applies-to"></a>S'applique à  
 [Objet de flux de données (ADO)](../../../ado/reference/ado-api/stream-object-ado.md)