---
title: "CRÉER INDEX instruction Limitations | Documents Microsoft"
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
- CREATE INDEX statement limitations [ODBC]
- ODBC SQL grammar, CREATE INDEX statement limitations
ms.assetid: 832dcda1-e452-48e6-8adb-7fb33c4fb4ff
caps.latest.revision: "5"
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: c3923fdf02d70fe87b0748b7a861cac85ec4b786
ms.sourcegitcommit: cc71f1027884462c359effb898390c8d97eaa414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2017
---
# <a name="create-index-statement-limitations"></a>CRÉER INDEX instruction Limitations
L’instruction CREATE INDEX n’est pas prise en charge pour les pilotes Microsoft Excel ou texte.  
  
 Un index peut être défini sur un maximum de 10 colonnes. Si plus de 10 colonnes sont inclus dans une instruction CREATE INDEX, l’index n’est pas reconnue et la table est traitée comme si aucun index ont été créés.  
  
 Le pilote dBASE ne peut pas créer un index sur une colonne logique.  
  
 Lorsque le pilote dBASE est utilisé, le temps de réponse sur des fichiers volumineux peuvent être amélioré en créant un index .mdx (ou .ndx) sur la colonne (champ) spécifié dans les clauses WHERE d’une instruction SELECT. Index .mdx existants sont automatiquement appliquées pour =, >, \<, > =, = < et entre les opérateurs dans une clause WHERE et les prédicats LIKE, ainsi que dans les prédicats de jointure.  
  
 Lorsque le pilote dBASE est utilisé, l’index créé par une instruction CREATE UNIQUE INDEX n’est pas réellement non unique, et des valeurs en double peuvent être insérées dans la colonne indexée. Qu’un seul enregistrement d’un ensemble de valeurs clés identiques peut être ajouté à l’index.  
  
 Lorsque le pilote Paradox est utilisé, un index unique doit être défini sur un sous-ensemble contigu de colonnes dans une table, y compris la première colonne. Une table ne peut pas être mis à jour par le pilote Paradox si un index unique n’est pas défini sur la table ou le pilote Paradox est utilisée sans l’implémentation du moteur de base de données Borland.
