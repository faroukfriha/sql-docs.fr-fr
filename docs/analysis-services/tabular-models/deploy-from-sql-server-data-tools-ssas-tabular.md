---
title: "Déployer à partir de SQL Server Data Tools | Documents Microsoft"
ms.custom: 
ms.date: 02/22/2018
ms.prod: analysis-services
ms.prod_service: analysis-services, azure-analysis-services
ms.service: 
ms.component: data-mining
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.asvs.bidtoolset.deploystatus.f1
ms.assetid: 67dde3fe-ba43-41f3-b56c-c656029ee93f
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: c009ba69247d754c95f98732f41e4023db0fcaa4
ms.sourcegitcommit: d8ab09ad99e9ec30875076acee2ed303d61049b7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2018
---
# <a name="deploy-from-sql-server-data-tools"></a>Déployer à partir de SQL Server Data Tools
[!INCLUDE[ssas-appliesto-sqlas-aas](../../includes/ssas-appliesto-sqlas-aas.md)]
Utilisez les tâches de cette rubrique pour déployer une solution de modèle tabulaire à l’aide de la commande déployer dans SSDT.  
  
##  <a name="bkmk_deploy"></a> Configurer les propriétés Options de déploiement et Serveur de déploiement  
 Avant de déployer votre solution de modèle tabulaire, vous devez spécifier les propriétés Options de déploiement et Serveur de déploiement. Pour plus d’informations sur les propriétés de déploiement et les paramètres, consultez [déploiement de solutions de modèle tabulaire](../../analysis-services/tabular-models/tabular-model-solution-deployment-ssas-tabular.md).  
  
#### <a name="to-configure-options-and-properties"></a>Pour configurer des options et des propriétés  
  
1.  Dans SSDT, dans **l’Explorateur de solutions**, cliquez sur le nom du projet, puis cliquez sur **propriétés**.  
  
2.  Dans le  **\<nom du projet > Propriétés** boîte de dialogue, dans **Options de déploiement**, spécifiez les paramètres de propriété si différents des paramètres par défaut.  
  
    > [!NOTE]  
    >  Pour les modèles en mode mis en cache, **Mode de requête** a toujours la valeur **In-Memory**.  
  
    > [!NOTE]  
    >  Vous ne pouvez pas spécifier de **Paramètres d’emprunt d’identité** pour les modèles en mode DirectQuery.  
  
3.  Dans **Serveur de déploiement**, spécifiez les paramètres de propriété **Serveur** (nom), **Édition**, **Base de données** (nom) et **Nom du cube** , s’ils sont différents des paramètres par défaut, puis cliquez sur **OK**.  
  
> [!NOTE]  
>  Vous pouvez également spécifier le paramètre de propriété Serveur de déploiement par défaut afin que tous les nouveaux projets que vous créez soient automatiquement déployés sur le serveur spécifié. Pour plus d’informations, consultez [configurer les propriétés de déploiement et de modélisation de données par défaut](../../analysis-services/tabular-models/configure-default-data-modeling-and-deployment-properties-ssas-tabular.md).  
  
##  <a name="bkmk_deploy_proc"></a> Déployer un modèle tabulaire  
  
#### <a name="to-deploy-a-tabular-model"></a>Pour déployer un modèle tabulaire
  
-   Dans SSDT, sur le **générer** menu, cliquez sur **déployer \<nom du projet >**.  
  
     La boîte de dialogue **Déployer** apparaît et indique l’état du déploiement des métadonnées et du traitement (sauf si la propriété Option de traitement a la valeur Ne pas traiter) de chaque table incluse dans le modèle. Une fois le processus de déploiement est terminé, utilisez SSMS pour vous connecter à l’instance Analysis Services et vérifiez que le nouvel objet de base de données model a été créé ou un client d’application pour se connecter au modèle déployé reporting.  
  
##  <a name="bkmk_deploy_status"></a> État du déploiement  
 La boîte de dialogue **Déployer** vous permet de surveiller la progression d'une opération de déploiement. Une opération de déploiement peut également être arrêtée.  
  
 **État**  
 Indique si l'opération de déploiement a abouti.  
  
 **Détails**  
 Répertorie les éléments de métadonnées déployés, l'état pour chaque élément de métadonnées, et affiche un message en cas de problèmes.  
  
 **Arrêter le déploiement**  
 Cliquez pour arrêter l'opération de déploiement. Cette option est utile si l'opération de déploiement prend trop de temps ou génère trop d'erreurs.  
  
## <a name="see-also"></a>Voir aussi  
 [Déploiement de solutions de modèle tabulaire](../../analysis-services/tabular-models/tabular-model-solution-deployment-ssas-tabular.md)   
 [Configurer les propriétés de déploiement et de modélisation de données par défaut](../../analysis-services/tabular-models/configure-default-data-modeling-and-deployment-properties-ssas-tabular.md)  
  
  
