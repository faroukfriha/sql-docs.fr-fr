---
title: Les Transitions de descripteur | Documents Microsoft
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.prod_service: drivers
ms.service: 
ms.component: odbc
ms.reviewer: 
ms.suite: sql
ms.technology: drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- state transitions [ODBC], descriptor
- transitioning states [ODBC], descriptor
- descriptor transitions [ODBC]
ms.assetid: 0cf24fe6-5e3c-45fa-81b8-4f52ddf8501d
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: 2c762c4276fe236418be07dfe1fe93482d4d9a10
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="descriptor-transitions"></a>Transitions de descripteur
Les descripteurs ODBC ont trois états suivants.  
  
|État|Description|  
|-----------|-----------------|  
|D0|Descripteur non alloué|  
|D1i|Descripteur implicitement alloué|  
|D1e|Descripteur alloué de manière explicite|  
  
 Les tableaux suivants indiquent comment chaque fonction ODBC affecte l’état du descripteur.  
  
## <a name="sqlallochandle"></a>SQLAllocHandle  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|D1i [1]|--|--|  
|D1e [2]|--|--|  
  
 [1] cette ligne affiche les transitions lorsque *HandleType* a été SQL_HANDLE_STMT.  
  
 [2] de cette ligne affiche les transitions lorsque *HandleType* a été SQL_HANDLE_DESC.  
  
## <a name="sqlcopydesc"></a>SQLCopyDesc  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|(INCLUENT)|--|--|  
  
## <a name="sqlfreehandle"></a>SQLFreeHandle  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|--[1]|D0|--|  
|(INCLUENT) [2]|(HY017)|D0|  
  
 [1] cette ligne affiche les transitions lorsque *HandleType* a été SQL_HANDLE_STMT.  
  
 [2] de cette ligne affiche les transitions lorsque *HandleType* a été SQL_HANDLE_DESC.  
  
## <a name="sqlgetdescfield-and-sqlgetdescrec"></a>SQLGetDescField et SQLGetDescRec  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|(INCLUENT)|--|--|  
  
## <a name="sqlsetdescfield-and-sqlsetdescrec"></a>SQLSetDescField et SQLSetDescRec  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|(INCLUENT) [1]|--|--|  
  
 [1] cette ligne affiche les transitions lorsque *DescriptorHandle* représente le handle d’ARD, APD ou IPD, ou (pour **SQLSetDescField**) lorsque *DescriptorHandle* a été le handle d’un IRD et *FieldIdentifier* a été SQL_DESC_ARRAY_STATUS_PTR ou SQL_DESC_ROWS_PROCESSED_PTR.  
  
## <a name="all-other-odbc-functions"></a>Toutes les autres fonctions ODBC  
  
|D0<br /><br /> Non alloué|D1i<br /><br /> Implicite|D1e<br /><br /> Explicite|  
|------------------------|----------------------|----------------------|  
|--|--|--|
