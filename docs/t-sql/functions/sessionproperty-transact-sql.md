---
title: SESSIONPROPERTY (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database
ms.service: 
ms.component: t-sql|functions
ms.reviewer: 
ms.suite: sql
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- SESSIONPROPERTY
- SESSIONPROPERTY_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- SET statement, SESSIONPROPERTY function
- SESSIONPROPERTY function
- sessions [SQL Server], SET options settings
ms.assetid: 1f3730b4-1495-4d3a-af43-e57952812df9
caps.latest.revision: 
author: edmacauley
ms.author: edmaca
manager: craigg
ms.workload: Inactive
ms.openlocfilehash: 72a7770b39b985f9e438743e24f8b4c7a076572f
ms.sourcegitcommit: 45e4efb7aa828578fe9eb7743a1a3526da719555
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="sessionproperty-transact-sql"></a>SESSIONPROPERTY (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  Retourne les paramètres des options SET d'une session.  
  
 ![Icône de lien de rubrique](../../database-engine/configure-windows/media/topic-link.gif "Icône lien de rubrique") [Conventions de la syntaxe Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntaxe  
  
```  
  
SESSIONPROPERTY (option)  
```  
  
## <a name="arguments"></a>Arguments  
 *option*  
 Paramètre sélectionné pour cette session. Le paramètre *option* peut prendre l’une des valeurs suivantes.  
  
|Option|Description|  
|------------|-----------------|  
|ANSI_NULLS|Indique si la conformité à la norme ISO est appliquée ou non en ce qui concerne le comportement des opérateurs d'égalité (=) et de différence (<>) avec des valeurs nulles.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|ANSI_PADDING|Contrôle le mode de stockage par la colonne des valeurs dont la longueur est inférieure à la taille définie pour la colonne, et des espaces de fin dans les données de type caractère et binaire.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|ANSI_WARNINGS|Indique si la conformité à la norme ISO est appliquée ou non dans les messages d'erreur ou les avertissements relatifs à certaines conditions, notamment la division par zéro et le dépassement arithmétique.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|ARITHABORT|Détermine la fin ou non de la requête lorsqu'un dépassement arithmétique ou une division par zéro se produit durant son exécution.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|CONCAT_NULL_YIELDS_ NULL|Détermine si les résultats de concaténation sont considérés comme des valeurs nulles ou des chaînes vides.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|NUMERIC_ROUNDABORT|Indique si un message d'erreur ou un avertissement doit être généré lorsqu'un arrondi effectué dans une expression entraîne une perte de précision.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|QUOTED_IDENTIFIER|Indique si les règles ISO relatives à l'utilisation des guillemets pour délimiter les identificateurs et les chaînes littérales doivent être appliquées.<br /><br /> 1 = activé<br /><br /> 0 = désactivé|  
|\<Toute autre chaîne>|NULL = Entrée non valide.|  
  
## <a name="return-types"></a>Types de retour  
 **sql_variant**  
  
## <a name="remarks"></a>Notes   
 Les options SET sont représentées en combinant les options de niveau serveur, de niveau base de données, et les options spécifiées par l'utilisateur.  
  
## <a name="examples"></a>Exemples  
 L'exemple suivant renvoie le paramètre de l'option `CONCAT_NULL_YIELDS_NULL`.  
  
```  
SELECT   SESSIONPROPERTY ('CONCAT_NULL_YIELDS_NULL')  
```  
  
## <a name="see-also"></a> Voir aussi  
 [sql_variant &#40;Transact-SQL&#41;](../../t-sql/data-types/sql-variant-transact-sql.md)   
 [SET ANSI_NULLS &#40;Transact-SQL&#41;](../../t-sql/statements/set-ansi-nulls-transact-sql.md)   
 [SET ANSI_PADDING &#40;Transact-SQL&#41;](../../t-sql/statements/set-ansi-padding-transact-sql.md)   
 [SET ANSI_WARNINGS &#40;Transact-SQL&#41;](../../t-sql/statements/set-ansi-warnings-transact-sql.md)   
 [SET ARITHABORT &#40;Transact-SQL&#41;](../../t-sql/statements/set-arithabort-transact-sql.md)   
 [SET CONCAT_NULL_YIELDS_NULL &#40;Transact-SQL&#41;](../../t-sql/statements/set-concat-null-yields-null-transact-sql.md)   
 [SET NUMERIC_ROUNDABORT &#40;Transact-SQL&#41;](../../t-sql/statements/set-numeric-roundabort-transact-sql.md)   
 [SET QUOTED_IDENTIFIER &#40;Transact-SQL&#41;](../../t-sql/statements/set-quoted-identifier-transact-sql.md)  
  
  
