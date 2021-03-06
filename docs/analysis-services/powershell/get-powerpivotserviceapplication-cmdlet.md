---
title: Applet de commande Get-PowerPivotServiceApplication | Documents Microsoft
ms.custom: 
ms.date: 03/01/2017
ms.prod: analysis-services
ms.prod_service: analysis-services
ms.service: 
ms.component: 
ms.reviewer: 
ms.suite: pro-bi
ms.technology: 
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 99e4faa1-2f87-43c6-b7ec-a97d4112c5ac
caps.latest.revision: 
author: Minewiskan
ms.author: owend
manager: kfile
ms.workload: Inactive
ms.openlocfilehash: 00ec7bd0c6ffe655e77cb8543216053697733fad
ms.sourcegitcommit: 7519508d97f095afe3c1cd85cf09a13c9eed345f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2018
---
# <a name="get-powerpivotserviceapplication-cmdlet"></a>Applet de commande Get-PowerPivotServiceApplication
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
Retourne une ou plusieurs applications de service [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] .  

>[!NOTE] 
>Cet article peut contenir des exemples et des informations obsolètes. Utilisez l’applet de commande Get-Help pour la dernière version.
  
 **S'applique à :** SharePoint 2010 et SharePoint 2013.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Get-PowerPivotServiceApplication [[-Identity] <SPGeminiServiceApplicationPipeBind>] [<CommonParameters>]  
```  
  
## <a name="description"></a> Description  
 L'applet de commande Get-PowerPivotServiceApplication retourne l'application de service spécifiée par le paramètre Identity. Si aucun paramètre n’est spécifié, l’applet de commande retourne toutes les applications de service [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] de la batterie. Chaque application est identifiée par son nom complet, son type d'application et son GUID. Pour afficher les autres propriétés d’une application de service [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] , ajoutez l’option format-list à l’applet de commande.  
  
## <a name="parameters"></a>Paramètres  
  
### <a name="-identity-spgeminiserviceapplicationpipebind"></a>-Identité \<SPGeminiServiceApplicationPipeBind >  
 Spécifie l'application de service à obtenir. La valeur doit être un GUID valide qui identifie l'objet de manière unique dans la batterie.  
  
|||  
|-|-|  
|Requis ?|false|  
|Position ?|0|  
|Valeur par défaut||  
|Accepter l'entrée de pipeline ?|true|  
|Accepter les caractères génériques ?|false|  
  
### <a name="commonparameters"></a>\<CommonParameters>  
 Cette applet de commande prend en charge les paramètres communs : Verbose, Debug, ErrorAction, ErrorVariable, WarningAction, WarningVariable, OutBuffer et OutVariable. Pour plus d’informations, consultez [About_Commonparameters](http://go.microsoft.com/fwlink/?linkID=227825).  
  
## <a name="inputs-and-outputs"></a>Entrées et sorties  
 Le type d'entrée correspond au type des objets que vous pouvez canaliser vers l'applet de commande. Le type de retour correspond au type des objets retournés par l'applet de commande.  
  
|||  
|-|-|  
|Entrées|Aucun.|  
|Sorties|Aucun.|  
  
## <a name="example-1"></a>Exemple 1  
  
```  
C:\PS>Get-PowerPivotServiceApplication  
```  
  
 Cet exemple retourne une ou plusieurs applications de service de la batterie.  
  
## <a name="example-2"></a>Exemple 2  
  
```  
C:\PS>Get-PowerPivotServiceApplication | format-list  
```  
  
 Cet exemple retourne toutes les propriétés d’une application de service [!INCLUDE[ssGemini](../../includes/ssgemini-md.md)] .  
  
## <a name="example-3"></a>Exemple 3  
  
```  
C:\PS>get-PowerPivotServiceApplication -Identity 1234567-890a-bcde-fghijklm  
```  
  
 Cet exemple retourne une seule application de service, en indiquant son nom complet, son type d'application et son GUID. Si le nom complet est long, il sera tronqué. Utilisez l'option format-list pour afficher le nom entier.  
  
  
