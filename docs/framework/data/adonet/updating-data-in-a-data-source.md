---
title: Mise à jour des données dans une source de données
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 55c545e5-dcd5-4323-a5b9-3825c2157462
ms.openlocfilehash: 088dc9507f073553f8a857bd11ecd016f0d94244
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730878"
---
# <a name="updating-data-in-a-data-source"></a>Mise à jour des données dans une source de données
Les instructions SQL qui modifient les données (comme INSERT, UPDATE ou DELETE) ne retournent pas de ligne. De même, de nombreuses procédures stockées effectuent une action mais ne retournent pas de ligne. Pour exécuter des commandes qui ne retournent pas de lignes, créez un **commande** objet avec la commande SQL appropriée et un **connexion**, y compris ceux requis **paramètres**. Exécutez la commande avec le **ExecuteNonQuery** méthode de la **commande** objet.  
  
 Le **ExecuteNonQuery** méthode retourne un entier qui représente le nombre de lignes affectées par l’instruction ou une procédure stockée qui a été exécutée. Si plusieurs instructions sont exécutées, la valeur retournée est la somme des enregistrements affectés par toutes ces instructions.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant exécute une instruction INSERT pour insérer un enregistrement dans une base de données à l’aide **ExecuteNonQuery**.  
  
```vb  
' Assumes connection is a valid SqlConnection.  
connection.Open()  
  
Dim queryString As String = "INSERT INTO Customers " & _  
  "(CustomerID, CompanyName) Values('NWIND', 'Northwind Traders')"  
  
Dim command As SqlCommand = New SqlCommand(queryString, connection)  
Dim recordsAffected As Int32 = command.ExecuteNonQuery()  
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
connection.Open();  
  
string queryString = "INSERT INTO Customers " +  
  "(CustomerID, CompanyName) Values('NWIND', 'Northwind Traders')";  
  
SqlCommand command = new SqlCommand(queryString, connection);  
Int32 recordsAffected = command.ExecuteNonQuery();  
```  
  
 L’exemple de code suivant exécute la procédure stockée créée par l’exemple de code dans [exécution d’opérations de catalogue](../../../../docs/framework/data/adonet/performing-catalog-operations.md). Aucune ligne n’est retournées par la procédure stockée, par conséquent, le **ExecuteNonQuery** méthode est utilisée, mais la procédure stockée ne reçoit pas un paramètre d’entrée et retourne un paramètre de sortie et une valeur de retour.  
  
 Pour le <xref:System.Data.OleDb.OleDbCommand> objet, le **ReturnValue** paramètre doit être ajouté à la **paramètres** collection premier.  
  
```vb  
' Assumes connection is a valid SqlConnection.  
Dim command As SqlCommand = _  
   New SqlCommand("InsertCategory" , connection)  
command.CommandType = CommandType.StoredProcedure  
  
Dim parameter As SqlParameter = _  
 command.Parameters.Add("@RowCount", SqlDbType.Int)  
parameter.Direction = ParameterDirection.ReturnValue  
  
parameter = command.Parameters.Add( _  
  "@CategoryName", SqlDbType.NChar, 15)  
  
parameter = command.Parameters.Add("@Identity", SqlDbType.Int)  
parameter.Direction = ParameterDirection.Output  
  
command.Parameters("@CategoryName").Value = "New Category"  
command.ExecuteNonQuery()  
  
Dim categoryID As Int32 = CInt(command.Parameters("@Identity").Value)  
Dim rowCount As Int32 = CInt(command.Parameters("@RowCount").Value)   
```  
  
```csharp  
// Assumes connection is a valid SqlConnection.  
SqlCommand command = new SqlCommand("InsertCategory" , connection);  
command.CommandType = CommandType.StoredProcedure;  
  
SqlParameter parameter = command.Parameters.Add(  
  "@RowCount", SqlDbType.Int);  
parameter.Direction = ParameterDirection.ReturnValue;  
  
parameter = command.Parameters.Add(  
  "@CategoryName", SqlDbType.NChar, 15);  
  
parameter = command.Parameters.Add("@Identity", SqlDbType.Int);  
parameter.Direction = ParameterDirection.Output;  
  
command.Parameters["@CategoryName"].Value = "New Category";  
command.ExecuteNonQuery();  
  
Int32 categoryID = (Int32) command.Parameters["@Identity"].Value;  
Int32 rowCount = (Int32) command.Parameters["@RowCount"].Value;  
```  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation des commandes pour modifier les données](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)
- [Mise à jour de sources de données avec des DataAdapters](../../../../docs/framework/data/adonet/updating-data-sources-with-dataadapters.md)
- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
