---
title: "Référence d’API du pilote SQLSRV | Documents Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: php
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0b55da26-ddeb-4e89-872a-91e0aba57103
caps.latest.revision: "42"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: On Demand
ms.openlocfilehash: 48d43c13a850e057d675d3abaaec612bc51723e1
ms.sourcegitcommit: 2713f8e7b504101f9298a0706bacd84bf2eaa174
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2017
---
# <a name="sqlsrv-driver-api-reference"></a>référence d’API du pilote SQLSRV
[!INCLUDE[Driver_PHP_Download](../../includes/driver_php_download.md)]

Le nom de l’API pour le pilote SQLSRV dans [!INCLUDE[ssDriverPHP](../../includes/ssdriverphp_md.md)] est **sqlsrv**. Tous les **sqlsrv** fonctions commencent par **sqlsrv_** suivi d’un verbe ou d’un substantif. Celles qui sont suivies d’un verbe effectuent une action tandis que celles qui sont suivies d’un substantif retournent des métadonnées.  
  
## <a name="in-this-section"></a>Dans cette section  
Le pilote SQLSRV contient les fonctions suivantes :  
  
|Fonction| Description|  
|------------|---------------|  
|[sqlsrv_begin_transaction](../../connect/php/sqlsrv-begin-transaction.md)|Commence une transaction.|  
|[sqlsrv_cancel](../../connect/php/sqlsrv-cancel.md)|Annule une instruction ; ignore les résultats en attente de l’instruction.|  
|[sqlsrv_client_info](../../connect/php/sqlsrv-client-info.md)|Fournit des informations sur le client.|  
|[sqlsrv_close](../../connect/php/sqlsrv-close.md)|Ferme une connexion. Libère toutes les ressources associées à la connexion.|  
|[sqlsrv_commit](../../connect/php/sqlsrv-commit.md)|Valide une transaction.|  
|[sqlsrv_configure](../../connect/php/sqlsrv-configure.md)|Modifie la gestion des erreurs et les configurations de journalisation.|  
|[sqlsrv_connect](../../connect/php/sqlsrv-connect.md)|Crée et ouvre une connexion.|  
|[sqlsrv_errors](../../connect/php/sqlsrv-errors.md)|Retourne des informations d’erreur et/ou d’avertissement sur la dernière opération.|  
|[sqlsrv_execute](../../connect/php/sqlsrv-execute.md)|Exécute une instruction préparée.|  
|[sqlsrv_fetch](../../connect/php/sqlsrv-fetch.md)|Rend la ligne suivante de données disponible pour la lecture.|  
|[sqlsrv_fetch_array](../../connect/php/sqlsrv-fetch-array.md)|Récupère la ligne suivante de données sous la forme d’un tableau indexé numériquement, de tableau associatif ou les deux.|  
|[sqlsrv_fetch_object](../../connect/php/sqlsrv-fetch-object.md)|Récupère la ligne suivante de données sous la forme d’un objet.|  
|[sqlsrv_field_metadata](../../connect/php/sqlsrv-field-metadata.md)|Retourne les métadonnées de champ.|  
|[sqlsrv_free_stmt](../../connect/php/sqlsrv-free-stmt.md)|Ferme une instruction. Libère toutes les ressources associées à l’instruction.|  
|[sqlsrv_get_config](../../connect/php/sqlsrv-get-config.md)|Retourne la valeur du paramètre de configuration spécifié.|  
|[sqlsrv_get_field](../../connect/php/sqlsrv-get-field.md)|Récupère un champ dans la ligne actuelle par index. Le type de retour PHP peut être spécifié.|  
|[sqlsrv_has_rows](../../connect/php/sqlsrv-has-rows.md)|Détecte si un jeu de résultats comporte une ou plusieurs lignes.|  
|[sqlsrv_next_result](../../connect/php/sqlsrv-next-result.md)|Rend le résultat suivant disponible pour le traitement.|  
|[sqlsrv_num_rows](../../connect/php/sqlsrv-num-rows.md)|Indique le nombre de lignes dans un jeu de résultats.|  
|[sqlsrv_num_fields](../../connect/php/sqlsrv-num-fields.md)|Récupère le nombre de champs dans un jeu de résultats actif.|  
|[sqlsrv_prepare](../../connect/php/sqlsrv-prepare.md)|Prépare une requête Transact-SQL sans l’exécuter. Lie implicitement des paramètres.|  
|[sqlsrv_query](../../connect/php/sqlsrv-query.md)|Prépare et exécute une requête Transact-SQL.|  
|[sqlsrv_rollback](../../connect/php/sqlsrv-rollback.md)|Restaure une transaction.|  
|[sqlsrv_rows_affected](../../connect/php/sqlsrv-rows-affected.md)|Retourne le nombre de lignes modifiées.|  
|[sqlsrv_send_stream_data](../../connect/php/sqlsrv-send-stream-data.md)|Envoie jusqu’à huit kilo-octets (8 Ko) de données au serveur à chaque appel à la fonction.|  
|[sqlsrv_server_info](../../connect/php/sqlsrv-server-info.md)|Fournit des informations sur le serveur.|  
  
## <a name="reference"></a>Référence  
[Manuel PHP](http://go.microsoft.com/fwlink/?LinkId=105500)  
  
## <a name="see-also"></a>Voir aussi  
[Vue d’ensemble du pilote SQL PHP](../../connect/php/overview-of-the-php-sql-driver.md)
[constantes &#40; Microsoft Drivers for PHP for SQL Server &#41;](../../connect/php/constants-microsoft-drivers-for-php-for-sql-server.md)  
[Guide de programmation pour le pilote SQL PHP](../../connect/php/programming-guide-for-php-sql-driver.md)
[Prise en main du pilote SQL PHP](../../connect/php/getting-started-with-the-php-sql-driver.md)
  
