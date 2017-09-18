---
title: "Type du tampon de données | Documents Microsoft"
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- data types [ODBC], buffers
- data buffers [ODBC], types
- buffers [ODBC], data
- C data types [ODBC], buffers
ms.assetid: 58bea3e9-d552-447f-b3ad-ce1dab213b72
caps.latest.revision: 7
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 0c2ed3fb1d6a68737a894663e1b5c841d6cb1041
ms.contentlocale: fr-fr
ms.lasthandoff: 09/09/2017

---
# <a name="data-buffer-type"></a>Type de tampon de données
Le type de données C d’une mémoire tampon est spécifié par l’application. Avec une seule variable, cela se produit lorsque l’application alloue la variable. Avec une mémoire générique, autrement dit, mémoire vers laquelle pointe un pointeur de type void : cela se produit lorsque l’application effectue un cast de la mémoire à un type particulier. Le pilote détecte ce type de deux manières :  
  
-   **Argument de type de mémoire tampon de données.** Mémoires tampons permet de transférer des valeurs de paramètre et les données du jeu de résultats, telles que la mémoire tampon liée avec *TargetValuePtr* dans **SQLBindCol**, ont généralement un argument de type associé, tel que le *TargetType* argument dans **SQLBindCol**. Dans cet argument, l’application transmet l’identificateur de type C qui correspond au type de la mémoire tampon. Par exemple, dans l’exemple suivant appel à **SQLBindCol**, la valeur SQL_C_TYPE_DATE indique au pilote qui le *Date* mémoire tampon est un SQL_DATE_STRUCT :  
  
    ```  
    SQL_DATE_STRUCT Date;  
    SQLINTEGER  DateInd;  
    SQLBindCol(hstmt, 1, SQL_C_TYPE_DATE, &Date, 0, &DateInd);  
    ```  
  
     Pour plus d’informations sur les identificateurs de type, consultez la [des Types de données dans ODBC](../../../odbc/reference/develop-app/data-types-in-odbc.md) section, plus loin dans cette section.  
  
-   **Type prédéfini.** Mémoires tampons utilisées pour envoyer et récupérer des options ou des attributs, tels que la mémoire tampon vers laquelle pointe le *InfoValuePtr* argument dans **SQLGetInfo**, a un type fixe qui dépend de l’option spécifiée. Le pilote part du principe que le tampon de données est de ce type ; Il est responsable de l’application pour allouer une mémoire tampon de ce type. Par exemple, dans l’exemple suivant appel à **SQLGetInfo**, le pilote suppose que la mémoire tampon est un entier 32 bits, car il s’agit que l’option SQL_STRING_FUNCTIONS requiert :  
  
    ```  
    SQLUINTEGER StringFuncs;  
    SQLGetInfo(hdbc, SQL_STRING_FUNCTIONS, (SQLPOINTER) &StringFuncs, 0,  
                NULL);  
    ```  
  
 Le pilote utilise le type de données C pour interpréter les données dans la mémoire tampon.