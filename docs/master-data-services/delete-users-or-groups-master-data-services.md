---
title: Supprimer des utilisateurs ou des groupes (Master Data Services) | Microsoft Docs
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-non-specified
ms.prod_service: mds
ms.service: 
ms.component: non-specific
ms.reviewer: 
ms.suite: sql
ms.technology:
- master-data-services
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- deleting groups [Master Data Services]
- groups [Master Data Services], deleting
- users [Master Data Services], deleting
- deleting users [Master Data Services]
ms.assetid: 0bbf9d2c-b826-48bb-8aa9-9905db6e717f
caps.latest.revision: 
author: leolimsft
ms.author: lle
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 23f33792f899a61c95f2fd05e1875facfe27690d
ms.sourcegitcommit: 6ac1956307d8255dc544e1063922493b30907b80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2018
---
# <a name="delete-users-or-groups-master-data-services"></a>Supprimer des utilisateurs ou des groupes (Master Data Services)
  Vos pouvez supprimer des utilisateurs ou des groupes lorsque vous ne souhaitez plus qu'ils accèdent à [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)].  
  
 Notez le comportement suivant lors de la suppression d'utilisateurs et de groupes :  
  
-   Si vous supprimez un utilisateur qui est membre d’un groupe ayant accès à [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)], l’utilisateur peut toujours accéder à [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] tant que vous ne le supprimez pas du groupe Active Directory ou du groupe local.  
  
-   Si vous supprimez un groupe, tous les utilisateurs de ce groupe qui ont accédé à [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)] sont affichés dans la liste **Utilisateurs** tant que vous ne les supprimez pas.  
  
-   Les modifications apportées à la sécurité ne sont pas propagées à MDS [!INCLUDE[ssMDSXLS](../includes/ssmdsxls-md.md)] pendant 20 minutes.  
  
## <a name="prerequisites"></a>Prerequisites  
 Pour effectuer cette procédure :  
  
-   Vous devez avoir l'autorisation d'accéder à la zone fonctionnelle **Autorisations d'accès** .  
  
### <a name="to-delete-users-or-groups"></a>Pour supprimer des utilisateurs ou des groupes  
  
1.  Dans [!INCLUDE[ssMDSmdm](../includes/ssmdsmdm-md.md)], cliquez sur **Autorisations d'accès**.  
  
2.  Pour supprimer un utilisateur, restez dans la page **Utilisateurs** . Pour supprimer un groupe, dans la barre de menus, cliquez sur **Gérer les groupes**.  
  
3.  Dans la grille, sélectionnez la ligne correspondant à l’utilisateur ou au groupe à supprimer.  
  
4.  Cliquez sur **Supprimer l’utilisateur sélectionné** ou **Supprimer le groupe sélectionné**.  
  
5.  Dans la boîte de dialogue de confirmation, cliquez sur **OK**.  
  
## <a name="see-also"></a> Voir aussi  
 [Sécurité &#40;Master Data Services&#41;](../master-data-services/security-master-data-services.md)  
  
  
