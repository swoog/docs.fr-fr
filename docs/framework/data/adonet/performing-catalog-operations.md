---
title: Exécution d'opérations du catalogue
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e60f542f-6271-495b-a9e4-48553481c2a3
ms.openlocfilehash: beb5d2db898df1c98662d53190ac1432acc746e7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61878221"
---
# <a name="performing-catalog-operations"></a>Exécution d'opérations du catalogue
Pour exécuter une commande pour modifier une base de données ou un catalogue, telles que l’instruction CREATE TABLE ou CREATE PROCEDURE, créez un **commande** de l’objet à l’aide d’instructions SQL appropriées et un **connexion** objet. Exécutez la commande avec le **ExecuteNonQuery** méthode de la **commande** objet.  
  
 L'exemple de code suivant crée une procédure stockée dans une base de données Microsoft SQL Server.  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim queryString As String = "CREATE PROCEDURE InsertCategory " & _  
    "@CategoryName nchar(15), " & _  
    "@Identity int OUT " & _  
    "AS " & _  
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " & _  
    "SET @Identity = @@Identity " & _  
    "RETURN @@ROWCOUNT"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
string queryString = "CREATE PROCEDURE InsertCategory  " +   
    "@CategoryName nchar(15), " +  
    "@Identity int OUT " +  
    "AS " +   
    "INSERT INTO Categories (CategoryName) VALUES(@CategoryName) " +   
    "SET @Identity = @@Identity " +  
    "RETURN @@ROWCOUNT";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
command.ExecuteNonQuery();  
```  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation des commandes pour modifier les données](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)
- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
