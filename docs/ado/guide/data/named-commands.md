---
title: "Nommé commandes | Documents Microsoft"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- named commands [ADO]
- commands [ADO]
ms.assetid: 5a0ec8f9-5ba3-4f9f-b80d-2073aa049586
caps.latest.revision: 14
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 21d9575ef237a01b97f4d272abb96e85fd5786f6
ms.contentlocale: fr-fr
ms.lasthandoff: 09/09/2017

---
# <a name="named-commands"></a>Commandes nommées
[Création et exécution d’une commande Simple](../../../ado/guide/data/creating-and-executing-a-simple-command.md) montre une manière d’exécuter une commande. Une autre façon : vous pouvez rendre une commande nommée et ensuite appeler ce nommé commande directement sur le **connexion** objet (affecté à la **ActiveConnection** propriété de la **commande** objet). Une commande d’affectation de noms signifie l’affectation d’un nom pour le **nom** propriété d’un **commande** objet. Par exemple :  
  
```  
objCmd.Name = "GetCustomers"  
objCmd.ActiveConnection = objConn  
objConn.GetCustomers objRs  
```  
  
 La commande nommée agit comme s’il s’agissait d’une méthode « personnalisée » sur le **connexion** objet. Le résultat de la commande est retourné comme paramètre de sortie de cette « méthode personnalisée ».  
  
 L’exemple suivant illustre cette fonctionnalité.  
  
```  
'BeginNamedCmd  
    On Error GoTo ErrHandler:  
  
    Dim objConn As New ADODB.Connection  
    Dim objCmd As New ADODB.Command  
    Dim objRs As New ADODB.Recordset  
  
    ' Connect to the data source.  
    Set objConn = GetNewConnection  
  
    objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers"  
    objCmd.CommandType = adCmdText  
  
    'Name the command.  
    objCmd.Name = "GetCustomers"  
  
    objCmd.ActiveConnection = objConn  
  
    ' Execute using Command.Name from the Connection.  
    objConn.GetCustomers objRs  
  
    ' Display.  
    Do While Not objRs.EOF  
        Debug.Print objRs(0) & vbTab & objRs(1)  
        objRs.MoveNext  
    Loop  
  
    'clean up  
    objRs.Close  
    objConn.Close  
    Set objRs = Nothing  
    Set objConn = Nothing  
    Set objCmd = Nothing  
    Exit Sub  
  
ErrHandler:  
    'clean up  
    If objRs.State = adStateOpen Then  
        objRs.Close  
    End If  
  
    If objConn.State = adStateOpen Then  
        objConn.Close  
    End If  
  
    Set objRs = Nothing  
    Set objConn = Nothing  
    Set objCmd = Nothing  
  
    If Err <> 0 Then  
        MsgBox Err.Source & "-->" & Err.Description, , "Error"  
    End If  
'EndNamedCmd  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Objet de connexion (ADO)](../../../ado/reference/ado-api/connection-object-ado.md)