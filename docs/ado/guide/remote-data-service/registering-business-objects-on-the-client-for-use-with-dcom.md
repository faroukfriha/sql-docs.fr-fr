---
title: "L’inscription des objets métier sur le Client pour une utilisation avec DCOM | Documents Microsoft"
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
- business objects in RDS [ADO]
ms.assetid: 75a21910-607f-463a-ae18-a17130dafb7e
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: adba9240c501136d891686da3e5361be96e80ee0
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2018
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>L’enregistrement des objets métier sur le Client pour une utilisation avec DCOM
Les objets métier personnalisés doivent faire en sorte que le côté client peut mapper son nom de programme (ProgId) à un identificateur (CLSID) qui peut être utilisé via DCOM. Pour cette raison, le ProgID de l’objet DCOM doit être dans le Registre côté client et mapper à l’ID de classe de l’objet métier côté serveur. Pour les autres protocoles pris en charge (HTTP, HTTPS et en cours), cela n’est pas nécessaire.  
  
> [!IMPORTANT]
>  À compter de Windows 8 et Windows Server 2012, les composants de serveur Services Bureau à distance ne sont plus inclus dans le système d’exploitation Windows (consultez Windows 8 et [Cookbook de compatibilité de Windows Server 2012](https://www.microsoft.com/en-us/download/details.aspx?id=27416) pour plus de détails). Composants du client Bureau à distance seront supprimées dans une future version de Windows. Évitez d'utiliser cette fonctionnalité dans de nouveaux travaux de développement, et prévoyez de modifier les applications qui utilisent actuellement cette fonctionnalité. La migration vers les applications qui utilisent des services Bureau à distance [Service de données WCF](http://go.microsoft.com/fwlink/?LinkId=199565).  
  
 Par exemple, si vous exposez un objet métier côté serveur appelé MyBObj associé à un ID de classe spécifique, par exemple, « {00112233-4455-6677-8899-00AABBCCDDEE} », assurez-vous que les entrées suivantes sont ajoutées au Registre côté client :  
  
```  
[HKEY_CLASSES_ROOT]  
\MyBObj\Clsid\(Default) "{00112233-4455-6677-8899-00AABBCCDDEE}"  
```


