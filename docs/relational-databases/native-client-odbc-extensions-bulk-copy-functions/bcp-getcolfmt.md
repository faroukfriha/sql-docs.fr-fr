---
title: bcp_getcolfmt | Documents Microsoft
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: native-client-odbc-extensions-bulk-copy-functions
ms.reviewer: 
ms.suite: sql
ms.technology: database-engine
ms.tgt_pltfrm: 
ms.topic: reference
apiname: bcp_getcolfmt
apilocation: sqlncli11.dll
apitype: DLLExport
helpviewer_keywords: bcp_getcolfmt function
ms.assetid: f8bdada5-7b2d-4475-8c98-f93e9d77b130
caps.latest.revision: "36"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 8056470fbe4f5ce7c6c78bf0e595a738354d0a37
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2017
---
# <a name="bcpgetcolfmt"></a>bcp_getcolfmt
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

  Utilisé pour rechercher la valeur de la propriété de format de colonne.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
RETCODE bcp_getcolfmt (  
        HDBC hdbc,  
        INT field,  
        INT property,  
        void* pValue,  
        INT cbvalue,  
        INT* pcbLen);  
```  
  
## <a name="arguments"></a>Arguments  
 *pas*  
 Handle de connexion ODBC compatible avec la copie en bloc.  
  
 *champ*  
 Numéro de colonne pour lequel la propriété est extraite.  
  
 *propriété*  
 L'une des constantes de propriété.  
  
 *pValue*  
 Pointeur vers la mémoire tampon de laquelle la valeur de la propriété doit être extraite.  
  
 *cbValue*  
 Taille de la mémoire tampon de propriété, en octets.  
  
 *pcbLen*  
 Pointeur vers la longueur des données retournées dans la mémoire tampon de propriété.  
  
## <a name="returns"></a>Valeur renvoyée  
 SUCCEED ou FAIL.  
  
## <a name="remarks"></a>Notes  
 Les valeurs de propriété de format de colonne sont répertoriées dans le [bcp_setcolfmt](../../relational-databases/native-client-odbc-extensions-bulk-copy-functions/bcp-setcolfmt.md) rubrique. Ces valeurs sont définies en appelant la fonction **bcp_setcolfmt** . La fonction **bcp_getcolfmt** est utilisée pour rechercher la valeur de la propriété de format de colonne.  
  
 Changements de comportement peuvent être observés lors de la connexion à un [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] (ou version ultérieure) ordinateur du serveur, par rapport aux versions [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] versions. Pour plus d’informations, consultez [de découverte des métadonnées](../../relational-databases/native-client/features/metadata-discovery.md).  
  
## <a name="bcpgetcolfmt-support-for-enhanced-date-and-time-features"></a>Prise en charge  par bcp_getcolfmt des fonctionnalités de date et heure améliorées  
 Les types utilisés avec les **BCP_FMT_TYPE** sont de propriété pour les types date/heure comme spécifié dans [modifications de copie en bloc pour améliorées de Date et heure Types &#40; OLE DB et ODBC &#41;](../../relational-databases/native-client-odbc-date-time/bulk-copy-changes-for-enhanced-date-and-time-types-ole-db-and-odbc.md).  
  
 Pour plus d’informations, consultez [Date et heure améliorations &#40; ODBC &#41;](../../relational-databases/native-client-odbc-date-time/date-and-time-improvements-odbc.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions de copie en bloc](../../relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions.md)  
  
  