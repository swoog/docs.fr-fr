---
title: Récupération de données à l'aide d'un DataReader
ms.date: 10/259/2018
dev_langs:
- csharp
- vb
ms.assetid: 97afc121-fb8b-465b-bab3-6d844420badb
ms.openlocfilehash: 134bb68b9cf60cc5082afefdd9eb87d991b6e0ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692754"
---
# <a name="retrieve-data-using-a-datareader"></a>Récupérer des données à l’aide d’un DataReader
Pour récupérer des données à l’aide un **DataReader**, créez une instance de la **commande** de l’objet, puis créez un **DataReader** en appelant **Command.ExecuteReader**  pour extraire des lignes à partir d’une source de données. Le **DataReader** fournit un flux sans tampon de données qui permet la logique procédurale de traiter efficacement les résultats à partir d’une source de données de manière séquentielle. Le **DataReader** constitue un bon choix lorsque vous récupérez les grandes quantités de données, car les données ne sont pas mis en cache en mémoire.

L’exemple suivant illustre l’utilisation un **DataReader**, où `reader` représente un DataReader valid et `command` représente un objet de commande valide.  

```csharp
reader = command.ExecuteReader();  
```

```vb
reader = command.ExecuteReader()
```  

Utilisez le **DataReader.Read** méthode pour obtenir une ligne des résultats de requête. Vous pouvez accéder à chaque colonne de la ligne retournée en passant le nom ou le nombre ordinal de la colonne à la **DataReader**. Toutefois, pour de meilleures performances, le **DataReader** fournit une série de méthodes qui vous permettent d’accéder aux valeurs de colonne dans leurs types de données natifs (**GetDateTime**, **GetDouble**, **GetGuid**, **GetInt32**, et ainsi de suite). Pour obtenir la liste des méthodes d’accesseur typées pour les données spécifiques au fournisseur **DataReaders**, consultez <xref:System.Data.OleDb.OleDbDataReader> et <xref:System.Data.SqlClient.SqlDataReader>. À l’aide des méthodes d’accesseur typées lorsque vous savez que les données sous-jacentes type réduit la quantité de conversion de type requise lors de la récupération de la valeur de colonne.  
  
 L’exemple suivant effectue une itération dans un **DataReader** de l’objet et retourne deux colonnes à partir de chaque ligne.  
  
 [!code-csharp[DataWorks SqlClient.HasRows#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.HasRows/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.HasRows#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.HasRows/VB/source.vb#1)]  
  
## <a name="closing-the-datareader"></a>Fermeture du DataReader  
 Appelez toujours le **fermer** méthode lorsque vous avez fini d’utiliser le **DataReader** objet.  
  
 Si votre **commande** contient la sortie paramètres ou valeurs de retour, ces valeurs ne sont pas disponibles tant que le **DataReader** est fermé.  
  
 Pendant un **DataReader** est ouvert, le **connexion** est utilisé exclusivement par cet **DataReader**. Vous ne pouvez pas exécuter de commandes pour le **connexion**, y compris la création d’un autre **DataReader**, jusqu'à ce que l’original **DataReader** est fermé.  
  
> [!NOTE]
>  N’appelez pas **fermer** ou **Dispose** sur un **connexion**, un **DataReader**, ou tout autre objet managé dans le **Finalize**  méthode de votre classe. Dans un finaliseur, libérez seulement les ressources non managées que votre classe possède directement. Si votre classe ne possède pas les ressources non managées, n’incluez pas une **Finalize** méthode dans votre définition de classe. Pour plus d’informations, consultez [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).  
  
## <a name="retrieving-multiple-result-sets-using-nextresult"></a>Récupération des résultats multiples définit à l’aide de NextResult  
 Si le **DataReader** retourne plusieurs jeux de résultats, appel le **NextResult** méthode pour effectuer une itération dans le résultat définit séquentiellement. L'exemple suivant montre l'objet <xref:System.Data.SqlClient.SqlDataReader> traitant les résultats de deux instructions SELECT utilisant la méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A>.  
  
 [!code-csharp[DataWorks SqlClient.NextResult#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.NextResult/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.NextResult#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.NextResult/VB/source.vb#1)]  
  
## <a name="getting-schema-information-from-the-datareader"></a>Obtention d’informations de schéma à partir du DataReader  
 Pendant un **DataReader** est ouvert, vous pouvez récupérer des informations de schéma sur le résultat actuel à l’aide de la **GetSchemaTable** (méthode). **GetSchemaTable** retourne un <xref:System.Data.DataTable> objet rempli avec des lignes et colonnes qui contiennent les informations de schéma pour le jeu de résultats actuel. Le **DataTable** contient une ligne pour chaque colonne du jeu de résultats. Chaque colonne de la table de schéma mappe à une propriété des colonnes retournées dans les lignes du résultat de la valeur, où le **ColumnName** est le nom de la propriété et la valeur de la colonne est la valeur de la propriété. L’exemple suivant écrit les informations de schéma pour **DataReader**.  
  
 [!code-csharp[DataWorks SqlClient.GetSchemaTable#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.GetSchemaTable/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.GetSchemaTable#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.GetSchemaTable/VB/source.vb#1)]  
  
## <a name="working-with-ole-db-chapters"></a>Utilisation de chapitres OLE DB  
 Ensembles de lignes hiérarchiques ou chapitres (type OLE DB **DBTYPE_HCHAPTER**, type ADO **adChapter**), peut être récupéré en utilisant la <xref:System.Data.OleDb.OleDbDataReader>. Quand une requête comprenant un chapitre est retournée comme un **DataReader**, le chapitre est retourné en tant que colonne dans ce **DataReader** et est exposé comme un **DataReader** objet.  
  
 ADO.NET **DataSet** peut également être utilisé pour représenter des ensembles de lignes hiérarchiques à l’aide de relations parent-enfant entre les tables. Pour plus d’informations, consultez [DataSets, DataTables et DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md).  
  
 L'exemple de code suivant utilise le fournisseur MSDataShape pour générer une colonne chapitre de commandes pour chaque client d'une liste de clients.  
  
```vb  
Using connection As OleDbConnection = New OleDbConnection(
    "Provider=MSDataShape;Data Provider=SQLOLEDB;" &
    "Data Source=localhost;Integrated Security=SSPI;Initial Catalog=northwind")

    Using custCMD As OleDbCommand = New OleDbCommand(
        "SHAPE {SELECT CustomerID, CompanyName FROM Customers} " &
        "APPEND ({SELECT CustomerID, OrderID FROM Orders} AS CustomerOrders " &
        "RELATE CustomerID TO CustomerID)", connection)

        connection.Open()

        Using custReader As OleDbDataReader = custCMD.ExecuteReader()

            Do While custReader.Read()
                Console.WriteLine("Orders for " & custReader.GetString(1))
                ' custReader.GetString(1) = CompanyName  

                Using orderReader As OleDbDataReader = custReader.GetValue(2)
                    ' custReader.GetValue(2) = Orders chapter as DataReader  

                    Do While orderReader.Read()
                        Console.WriteLine(vbTab & orderReader.GetInt32(1))
                        ' orderReader.GetInt32(1) = OrderID  
                    Loop
                    orderReader.Close()
                End Using
            Loop
            ' Make sure to always close readers and connections.  
            custReader.Close()
        End Using
    End Using
End Using
```  
  
```csharp  
using (OleDbConnection connection = new OleDbConnection(
    "Provider=MSDataShape;Data Provider=SQLOLEDB;" +
    "Data Source=localhost;Integrated Security=SSPI;Initial Catalog=northwind"))
{
    using (OleDbCommand custCMD = new OleDbCommand(
        "SHAPE {SELECT CustomerID, CompanyName FROM Customers} " +
        "APPEND ({SELECT CustomerID, OrderID FROM Orders} AS CustomerOrders " +
        "RELATE CustomerID TO CustomerID)", connection))
    {
        connection.Open();

        using (OleDbDataReader custReader = custCMD.ExecuteReader())
        {

            while (custReader.Read())
            {
                Console.WriteLine("Orders for " + custReader.GetString(1));
                // custReader.GetString(1) = CompanyName  

                using (OleDbDataReader orderReader = (OleDbDataReader)custReader.GetValue(2))
                {
                    // custReader.GetValue(2) = Orders chapter as DataReader  

                    while (orderReader.Read())
                        Console.WriteLine("\t" + orderReader.GetInt32(1));
                    // orderReader.GetInt32(1) = OrderID  
                    orderReader.Close();
                }
            }
            // Make sure to always close readers and connections.  
            custReader.Close();
        }
    }
}
```  
  
## <a name="returning-results-with-oracle-ref-cursors"></a>Renvoi de résultats avec des REF CURSOR Oracle  
 Le fournisseur de données .NET Framework pour Oracle prend en charge l'utilisation des REF CURSOR Oracle pour retourner le résultat d'une requête. Un REF CURSOR Oracle est retourné en tant qu'objet <xref:System.Data.OracleClient.OracleDataReader>.  
  
 Vous pouvez récupérer un <xref:System.Data.OracleClient.OracleDataReader> objet qui représente un REF CURSOR Oracle à l’aide de la <xref:System.Data.OracleClient.OracleCommand.ExecuteReader%2A> (méthode). Vous pouvez également spécifier un <xref:System.Data.OracleClient.OracleCommand> qui retourne un ou plusieurs REF CURSOR Oracle en tant que le **SelectCommand** pour un <xref:System.Data.OracleClient.OracleDataAdapter> utilisé pour remplir un <xref:System.Data.DataSet>.  
  
 Pour accéder à un REF CURSOR retourné à partir d’une source de données Oracle, créez un <xref:System.Data.OracleClient.OracleCommand> pour votre requête et ajoutez un paramètre de sortie qui référence le REF CURSOR à la <xref:System.Data.OracleClient.OracleCommand.Parameters> collection de votre <xref:System.Data.OracleClient.OracleCommand>. Le nom du paramètre doit correspondre à celui du paramètre REF CURSOR de votre requête. Définissez le type du paramètre à <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType>. Le <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> méthode de votre <xref:System.Data.OracleClient.OracleCommand> retourne un <xref:System.Data.OracleClient.OracleDataReader> pour REF CURSOR.  
  
 Si votre <xref:System.Data.OracleClient.OracleCommand> retourne plusieurs REF CURSOR, ajoutez plusieurs paramètres de sortie. Vous pouvez accéder aux différents REF CURSOR en appelant le <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> (méthode). L’appel à <xref:System.Data.OracleClient.OracleCommand.ExecuteReader> retourne un <xref:System.Data.OracleClient.OracleDataReader> qui référence le premier REF CURSOR. Vous pouvez ensuite appeler la <xref:System.Data.OracleClient.OracleDataReader.NextResult?displayProperty=nameWithType> méthode pour accéder aux REF CURSOR suivants. Bien que les paramètres dans votre <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> paramètres de sortie de collection correspondent les REF CURSOR par nom, le <xref:System.Data.OracleClient.OracleDataReader> y accède selon l’ordre dans lequel ils ont été ajoutés à la <xref:System.Data.OracleClient.OracleCommand.Parameters> collection.  
  
 Considérez, par exemple, le package et le corps de package Oracle suivants.  
  
```sql
CREATE OR REPLACE PACKAGE CURSPKG AS   
  TYPE T_CURSOR IS REF CURSOR;   
  PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,   
    DEPTCURSOR OUT T_CURSOR);   
END CURSPKG;  
  
CREATE OR REPLACE PACKAGE BODY CURSPKG AS   
  PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,   
    DEPTCURSOR OUT T_CURSOR)   
  IS   
  BEGIN   
    OPEN EMPCURSOR FOR SELECT * FROM DEMO.EMPLOYEE;   
    OPEN DEPTCURSOR FOR SELECT * FROM DEMO.DEPARTMENT;   
  END OPEN_TWO_CURSORS;   
END CURSPKG;   
```  
  
 Le code suivant crée un <xref:System.Data.OracleClient.OracleCommand> qui retourne les REF CURSOR d’un précédent package Oracle en ajoutant deux paramètres de type <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType> à la <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> collection.  
  
```vb  
Dim cursCmd As OracleCommand = New OracleCommand("CURSPKG.OPEN_TWO_CURSORS", oraConn)  
cursCmd.Parameters.Add("EMPCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output  
cursCmd.Parameters.Add("DEPTCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output  
```  
  
```csharp  
OracleCommand cursCmd = new OracleCommand("CURSPKG.OPEN_TWO_CURSORS", oraConn);  
cursCmd.Parameters.Add("EMPCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output;  
cursCmd.Parameters.Add("DEPTCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output;  
```  
  
 Le code suivant retourne les résultats de la commande précédente à l’aide du <xref:System.Data.OracleClient.OracleDataReader.Read> et <xref:System.Data.OracleClient.OracleDataReader.NextResult> méthodes de la <xref:System.Data.OracleClient.OracleDataReader>. Les paramètres REF CURSOR sont retournés dans l'ordre.  
  
```vb  
oraConn.Open()  
  
Dim cursCmd As OracleCommand = New OracleCommand("CURSPKG.OPEN_TWO_CURSORS", oraConn)  
cursCmd.CommandType = CommandType.StoredProcedure  
cursCmd.Parameters.Add("EMPCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output  
cursCmd.Parameters.Add("DEPTCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output  
  
Dim reader As OracleDataReader = cursCmd.ExecuteReader()  
  
Console.WriteLine(vbCrLf & "Emp ID" & vbTab & "Name")  
  
Do While reader.Read()  
  Console.WriteLine("{0}" & vbTab & "{1}, {2}", reader.GetOracleNumber(0), reader.GetString(1), reader.GetString(2))  
Loop  
  
reader.NextResult()  
  
Console.WriteLine(vbCrLf & "Dept ID" & vbTab & "Name")  
  
Do While reader.Read()  
  Console.WriteLine("{0}" & vbTab & "{1}", reader.GetOracleNumber(0), reader.GetString(1))  
Loop  
' Make sure to always close readers and connections.  
reader.Close()  
oraConn.Close()  
```  
  
```csharp  
oraConn.Open();  
  
OracleCommand cursCmd = new OracleCommand("CURSPKG.OPEN_TWO_CURSORS", oraConn);  
cursCmd.CommandType = CommandType.StoredProcedure;  
cursCmd.Parameters.Add("EMPCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output;  
cursCmd.Parameters.Add("DEPTCURSOR", OracleType.Cursor).Direction = ParameterDirection.Output;  
  
OracleDataReader reader = cursCmd.ExecuteReader();  
  
Console.WriteLine("\nEmp ID\tName");  
  
while (reader.Read())  
  Console.WriteLine("{0}\t{1}, {2}", reader.GetOracleNumber(0), reader.GetString(1), reader.GetString(2));  
  
reader.NextResult();  
  
Console.WriteLine("\nDept ID\tName");  
  
while (reader.Read())  
  Console.WriteLine("{0}\t{1}", reader.GetOracleNumber(0), reader.GetString(1));  
// Make sure to always close readers and connections.  
reader.Close();  
oraConn.Close();  
```  
  
 L’exemple suivant utilise la commande précédente pour remplir un <xref:System.Data.DataSet> avec les résultats du package Oracle.  
  
```vb  
Dim ds As DataSet = New DataSet()  
  
Dim adapter As OracleDataAdapter = New OracleDataAdapter(cursCmd)  
adapter.TableMappings.Add("Table", "Employees")  
adapter.TableMappings.Add("Table1", "Departments")  
  
adapter.Fill(ds)  
```  
  
```csharp  
DataSet ds = new DataSet();  
  
OracleDataAdapter adapter = new OracleDataAdapter(cursCmd);  
adapter.TableMappings.Add("Table", "Employees");  
adapter.TableMappings.Add("Table1", "Departments");  
  
adapter.Fill(ds);  
```

> [!NOTE]
>  Pour éviter un **OverflowException**, nous recommandons que vous gérez également toute conversion à partir du type Oracle NUMBER en un type .NET Framework valide avant de stocker la valeur dans un <xref:System.Data.DataRow>. Vous pouvez utiliser la <xref:System.Data.Common.DataAdapter.FillError> événement pour déterminer si un **OverflowException** s’est produite. Pour plus d’informations sur la <xref:System.Data.Common.DataAdapter.FillError> événement, consultez [gestion des événements DataAdapter](../../../../docs/framework/data/adonet/handling-dataadapter-events.md).  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de DataReaders](https://msdn.microsoft.com/library/126a966a-d08d-4d22-a19f-f432908b2b54)
- [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [Récupération des informations de schéma de base de données](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
