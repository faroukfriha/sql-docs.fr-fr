---
title: Architecture | Documents Microsoft
ms.custom: 
ms.date: 11/03/2017
ms.reviewer: 
ms.suite: sql
ms.prod: machine-learning-services
ms.prod_service: machine-learning-services
ms.component: python
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: article
author: jeannt
ms.author: jeannt
manager: cgronlund
ms.workload: Inactive
ms.openlocfilehash: 5ca823bc7094c77a31cfd3178294cd49a360d77a
ms.sourcegitcommit: 99102cdc867a7bdc0ff45e8b9ee72d0daade1fd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2018
---
# <a name="architecture-overview-for-machine-learning-services-with-python"></a>Présentation de l’architecture de Machine Learning Services avec Python
[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-winonly](../../includes/appliesto-ss-xxxx-xxxx-xxx-md-winonly.md)]

Cette rubrique fournit une vue d’ensemble de la manière dont les Python est intégré à SQL Server, y compris le modèle de sécurité, les composants du moteur de base de données qui prennent en charge l’exécution du script externe, les nouveaux composants qui permettent l’interopérabilité de Python avec SQL Server. Pour plus d’informations, consultez les rubriques associées.

> [!IMPORTANT]
> Prise en charge pour Python est disponible à compter de SQL Server 2017 CTP 2.0. Cette fonctionnalité en version préliminaire est susceptible de changer.

## <a name="python-interoperability"></a>Interopérabilité de Python

Machine Learning Services (de-de base de données) de SQL Server installe la distribution Anaconda de Python et le runtime de Python 3.5 et l’interpréteur. Cela garantit la terminer près de la compatibilité avec les solutions de Python standards. Python s’exécute dans un processus séparé à partir de SQL Server, afin de garantir que les opérations de base de données ne sont pas compromises.

Pour plus d’informations sur l’interaction de SQL Server avec Python, consultez [l’interopérabilité de Python](../../advanced-analytics/python/python-interoperability.md)

## <a name="components-that-support-python-integration"></a>Composants qui prennent en charge l’intégration Python

L’infrastructure d’extensibilité introduite dans SQL Server 2016 maintenant prend en charge l’exécution du script Python, via l’ajout de nouveaux composants linguistiques. Ces composants améliorent la vitesse des données exchange et la compression, tout en fournissant une plateforme sécurisée et hautes performances pour l’exécution de scripts externes.

Pour une description détaillée des composants qui prennent en charge de Python, telles que la [!INCLUDE[rsql_launchpad_md](../../includes/rsql-launchpad-md.md)] et PythonLauncher, consultez [nouveaux composants](../../advanced-analytics/python/new-components-in-sql-server-to-support-python-integration.md).

## <a name="security"></a>Sécurité

Tâches de Python s’exécutent en dehors du processus SQL Server, pour fournir une plus grande facilité de gestion et de sécurité.

Toutes les tâches sont sécurisés par des objets de traitement Windows ou la sécurité de SQL Server. En appliquant la sécurité au niveau de la table, la base de données et le niveau de l’instance de SQL Server, les données sont conservées dans les limites de la conformité. L’administrateur de base de données peut contrôler qui a la possibilité d’exécuter des travaux de Python, de surveiller l’utilisation de scripts Python par les utilisateurs et d’afficher la consommation de ressources.

Pour plus d’informations, consultez [sécurité pour Python](../../advanced-analytics/python/security-overview-sql-server-python-services.md)

## <a name="resource-governance"></a>Gouvernance des ressources

Dans SQL Server Enterprise Edition, vous pouvez utiliser le gouverneur de ressources pour gérer et surveiller l’utilisation des ressources des opérations de script externe, y compris un script R et les scripts Python.

Pour plus d’informations, consultez [gouvernance des ressources pour R](../../advanced-analytics/r/resource-governance-for-r-services.md).

## <a name="next-steps"></a>Étapes suivantes

[Exécutez Python à l’aide de T-SQL](../tutorials/run-python-using-t-sql.md)
