---
title: Section Logs du fichier de personnalisation | Documents Microsoft
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
- logs section in RDS [ADO]
- customization file in RDS [ADO]
ms.assetid: a368e264-865c-41ee-be00-d9097255c2ea
caps.latest.revision: 
author: MightyPen
ms.author: genemi
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 10f6e47bcf8cede8c59a406fef4951a11cbd56bd
ms.sourcegitcommit: acab4bcab1385d645fafe2925130f102e114f122
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2018
---
# <a name="customization-file-logs-section"></a>Section de personnalisation de fichiers journaux
Le **journaux** section contient une entrée de fichier journal, qui spécifie le nom d’un fichier qui enregistre les erreurs pendant l’opération de le **DataFactory**.  
  
> [!IMPORTANT]
>  À compter de Windows 8 et Windows Server 2012, les composants de serveur Services Bureau à distance ne sont plus inclus dans le système d’exploitation Windows (consultez Windows 8 et [Cookbook de compatibilité de Windows Server 2012](https://www.microsoft.com/en-us/download/details.aspx?id=27416) pour plus de détails). Composants du client Bureau à distance seront supprimées dans une future version de Windows. Évitez d'utiliser cette fonctionnalité dans de nouveaux travaux de développement, et prévoyez de modifier les applications qui utilisent actuellement cette fonctionnalité. La migration vers les applications qui utilisent des services Bureau à distance [Service de données WCF](http://go.microsoft.com/fwlink/?LinkId=199565).  
  
## <a name="syntax"></a>Syntaxe  
 Une entrée de fichier journal est au format :  
  
```  
  
err=  
FileName  
  
```  
  
## <a name="remarks"></a>Notes  
  
|Élément| Description|  
|----------|-----------------|  
|**err**|Une chaîne littérale qui indique qu’il est une entrée de fichier journal.|  
|*FileName*|Un nom de fichier et le chemin complet. Le nom de fichier par défaut est **c:\msdfmap.log**.|  
  
 Le fichier journal contient le nom d’utilisateur, un HRESULT, une date et une heure de chaque erreur.  
  
## <a name="see-also"></a>Voir aussi  
 [Section Connect du fichier de personnalisation](../../../ado/guide/remote-data-service/customization-file-connect-section.md)   
 [Section de personnalisation de fichier SQL](../../../ado/guide/remote-data-service/customization-file-sql-section.md)   
 [Section du fichier de personnalisation UserList](../../../ado/guide/remote-data-service/customization-file-userlist-section.md)   
 [DataFactory, personnalisation](../../../ado/guide/remote-data-service/datafactory-customization.md)   
 [Paramètres Client requis](../../../ado/guide/remote-data-service/required-client-settings.md)   
 [Présentation du fichier de personnalisation](../../../ado/guide/remote-data-service/understanding-the-customization-file.md)   
 [Écriture d’un gestionnaire personnalisé](../../../ado/guide/remote-data-service/writing-your-own-customized-handler.md)


