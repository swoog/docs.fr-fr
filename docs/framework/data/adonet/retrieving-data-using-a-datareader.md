---
title: Récupération de données à l'aide d'un DataReader
ms.date: 10/29/2018
dev_langs:
- csharp
- vb
ms.assetid: 97afc121-fb8b-465b-bab3-6d844420badb
ms.openlocfilehash: 8063f239123ec1a2f2650adf9d76f7ceaaa50673
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59128678"
---
# <a name="retrieve-data-using-a-datareader"></a><span data-ttu-id="cfc97-102">Récupérer des données à l’aide d’un DataReader</span><span class="sxs-lookup"><span data-stu-id="cfc97-102">Retrieve data using a DataReader</span></span>
<span data-ttu-id="cfc97-103">Pour récupérer des données à l’aide un **DataReader**, créez une instance de la **commande** de l’objet, puis créez un **DataReader** en appelant **Command.ExecuteReader**  pour extraire des lignes à partir d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="cfc97-103">To retrieve data using a **DataReader**, create an instance of the **Command** object, and then create a **DataReader** by calling **Command.ExecuteReader** to retrieve rows from a data source.</span></span> <span data-ttu-id="cfc97-104">Le **DataReader** fournit un flux sans tampon de données qui permet la logique procédurale de traiter efficacement les résultats à partir d’une source de données de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="cfc97-104">The **DataReader** provides an unbuffered stream of data that allows procedural logic to efficiently process results from a data source sequentially.</span></span> <span data-ttu-id="cfc97-105">Le **DataReader** constitue un bon choix lorsque vous récupérez les grandes quantités de données, car les données ne sont pas mis en cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="cfc97-105">The **DataReader** is a good choice when you're retrieving large amounts of data because the data is not cached in memory.</span></span>

<span data-ttu-id="cfc97-106">L’exemple suivant illustre l’utilisation un **DataReader**, où `reader` représente un DataReader valid et `command` représente un objet de commande valide.</span><span class="sxs-lookup"><span data-stu-id="cfc97-106">The following example illustrates using a **DataReader**, where `reader` represents a valid DataReader and `command` represents a valid Command object.</span></span>  

```csharp
reader = command.ExecuteReader();  
```

```vb
reader = command.ExecuteReader()
```  

<span data-ttu-id="cfc97-107">Utilisez le **DataReader.Read** méthode pour obtenir une ligne des résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="cfc97-107">Use the **DataReader.Read** method to obtain a row from the query results.</span></span> <span data-ttu-id="cfc97-108">Vous pouvez accéder à chaque colonne de la ligne retournée en passant le nom ou le nombre ordinal de la colonne à la **DataReader**.</span><span class="sxs-lookup"><span data-stu-id="cfc97-108">You can access each column of the returned row by passing the name or ordinal number of the column to the **DataReader**.</span></span> <span data-ttu-id="cfc97-109">Toutefois, pour de meilleures performances, le **DataReader** fournit une série de méthodes qui vous permettent d’accéder aux valeurs de colonne dans leurs types de données natifs (**GetDateTime**, **GetDouble**, **GetGuid**, **GetInt32**, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="cfc97-109">However, for best performance, the **DataReader** provides a series of methods that allow you to access column values in their native data types (**GetDateTime**, **GetDouble**, **GetGuid**, **GetInt32**, and so on).</span></span> <span data-ttu-id="cfc97-110">Pour obtenir la liste des méthodes d’accesseur typées pour les données spécifiques au fournisseur **DataReaders**, consultez <xref:System.Data.OleDb.OleDbDataReader> et <xref:System.Data.SqlClient.SqlDataReader>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-110">For a list of typed accessor methods for data provider-specific **DataReaders**, see <xref:System.Data.OleDb.OleDbDataReader> and <xref:System.Data.SqlClient.SqlDataReader>.</span></span> <span data-ttu-id="cfc97-111">À l’aide des méthodes d’accesseur typées lorsque vous savez que les données sous-jacentes type réduit la quantité de conversion de type requise lors de la récupération de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="cfc97-111">Using the typed accessor methods when you know the underlying data type reduces the amount of type conversion required when retrieving the column value.</span></span>  
  
 <span data-ttu-id="cfc97-112">L’exemple suivant effectue une itération dans un **DataReader** de l’objet et retourne deux colonnes à partir de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="cfc97-112">The following example iterates through a **DataReader** object and returns two columns from each row.</span></span>  
  
 [!code-csharp[DataWorks SqlClient.HasRows#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.HasRows/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.HasRows#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.HasRows/VB/source.vb#1)]  
  
## <a name="closing-the-datareader"></a><span data-ttu-id="cfc97-113">Fermeture du DataReader</span><span class="sxs-lookup"><span data-stu-id="cfc97-113">Closing the DataReader</span></span>  
 <span data-ttu-id="cfc97-114">Appelez toujours le **fermer** méthode lorsque vous avez fini d’utiliser le **DataReader** objet.</span><span class="sxs-lookup"><span data-stu-id="cfc97-114">Always call the **Close** method when you have finished using the **DataReader** object.</span></span>  
  
 <span data-ttu-id="cfc97-115">Si votre **commande** contient la sortie paramètres ou valeurs de retour, ces valeurs ne sont pas disponibles tant que le **DataReader** est fermé.</span><span class="sxs-lookup"><span data-stu-id="cfc97-115">If your **Command** contains output parameters or return values, those values are not available until the **DataReader** is closed.</span></span>  
  
 <span data-ttu-id="cfc97-116">Pendant un **DataReader** est ouvert, le **connexion** est utilisé exclusivement par cet **DataReader**.</span><span class="sxs-lookup"><span data-stu-id="cfc97-116">While a **DataReader** is open, the **Connection** is in use exclusively by that **DataReader**.</span></span> <span data-ttu-id="cfc97-117">Vous ne pouvez pas exécuter de commandes pour le **connexion**, y compris la création d’un autre **DataReader**, jusqu'à ce que l’original **DataReader** est fermé.</span><span class="sxs-lookup"><span data-stu-id="cfc97-117">You cannot execute any commands for the **Connection**, including creating another **DataReader**, until the original **DataReader** is closed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cfc97-118">N’appelez pas **fermer** ou **Dispose** sur un **connexion**, un **DataReader**, ou tout autre objet managé dans le **Finalize**  méthode de votre classe.</span><span class="sxs-lookup"><span data-stu-id="cfc97-118">Do not call **Close** or **Dispose** on a **Connection**, a **DataReader**, or any other managed object in the **Finalize** method of your class.</span></span> <span data-ttu-id="cfc97-119">Dans un finaliseur, libérez seulement les ressources non managées que votre classe possède directement.</span><span class="sxs-lookup"><span data-stu-id="cfc97-119">In a finalizer, only release unmanaged resources that your class owns directly.</span></span> <span data-ttu-id="cfc97-120">Si votre classe ne possède pas les ressources non managées, n’incluez pas une **Finalize** méthode dans votre définition de classe.</span><span class="sxs-lookup"><span data-stu-id="cfc97-120">If your class does not own any unmanaged resources, do not include a **Finalize** method in your class definition.</span></span> <span data-ttu-id="cfc97-121">Pour plus d’informations, consultez [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).</span><span class="sxs-lookup"><span data-stu-id="cfc97-121">For more information, see [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).</span></span>  
  
## <a name="retrieving-multiple-result-sets-using-nextresult"></a><span data-ttu-id="cfc97-122">Récupération des résultats multiples définit à l’aide de NextResult</span><span class="sxs-lookup"><span data-stu-id="cfc97-122">Retrieving multiple result sets using NextResult</span></span>  
 <span data-ttu-id="cfc97-123">Si le **DataReader** retourne plusieurs jeux de résultats, appel le **NextResult** méthode pour effectuer une itération dans le résultat définit séquentiellement.</span><span class="sxs-lookup"><span data-stu-id="cfc97-123">If the **DataReader** returns multiple result sets, call the **NextResult** method to iterate through the result sets sequentially.</span></span> <span data-ttu-id="cfc97-124">L'exemple suivant montre l'objet <xref:System.Data.SqlClient.SqlDataReader> traitant les résultats de deux instructions SELECT utilisant la méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-124">The following example shows the <xref:System.Data.SqlClient.SqlDataReader> processing the results of two SELECT statements using the <xref:System.Data.SqlClient.SqlCommand.ExecuteReader%2A> method.</span></span>  
  
 [!code-csharp[DataWorks SqlClient.NextResult#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.NextResult/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.NextResult#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.NextResult/VB/source.vb#1)]  
  
## <a name="getting-schema-information-from-the-datareader"></a><span data-ttu-id="cfc97-125">Obtention d’informations de schéma à partir du DataReader</span><span class="sxs-lookup"><span data-stu-id="cfc97-125">Getting schema information from the DataReader</span></span>  
 <span data-ttu-id="cfc97-126">Pendant un **DataReader** est ouvert, vous pouvez récupérer des informations de schéma sur le résultat actuel à l’aide de la **GetSchemaTable** (méthode).</span><span class="sxs-lookup"><span data-stu-id="cfc97-126">While a **DataReader** is open, you can retrieve schema information about the current result set using the **GetSchemaTable** method.</span></span> <span data-ttu-id="cfc97-127">**GetSchemaTable** retourne un <xref:System.Data.DataTable> objet rempli avec des lignes et colonnes qui contiennent les informations de schéma pour le jeu de résultats actuel.</span><span class="sxs-lookup"><span data-stu-id="cfc97-127">**GetSchemaTable** returns a <xref:System.Data.DataTable> object populated with rows and columns that contain the schema information for the current result set.</span></span> <span data-ttu-id="cfc97-128">Le **DataTable** contient une ligne pour chaque colonne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="cfc97-128">The **DataTable** contains one row for each column of the result set.</span></span> <span data-ttu-id="cfc97-129">Chaque colonne de la table de schéma mappe à une propriété des colonnes retournées dans les lignes du résultat de la valeur, où le **ColumnName** est le nom de la propriété et la valeur de la colonne est la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cfc97-129">Each column of the schema table maps to a property of the columns returned in the rows of the result set, where the **ColumnName** is the name of the property and the value of the column is the value of the property.</span></span> <span data-ttu-id="cfc97-130">L’exemple suivant écrit les informations de schéma pour **DataReader**.</span><span class="sxs-lookup"><span data-stu-id="cfc97-130">The following example writes out the schema information for **DataReader**.</span></span>  
  
 [!code-csharp[DataWorks SqlClient.GetSchemaTable#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.GetSchemaTable/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.GetSchemaTable#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.GetSchemaTable/VB/source.vb#1)]  
  
## <a name="working-with-ole-db-chapters"></a><span data-ttu-id="cfc97-131">Utilisation de chapitres OLE DB</span><span class="sxs-lookup"><span data-stu-id="cfc97-131">Working with OLE DB chapters</span></span>  
 <span data-ttu-id="cfc97-132">Ensembles de lignes hiérarchiques ou chapitres (type OLE DB **DBTYPE_HCHAPTER**, type ADO **adChapter**), peut être récupéré en utilisant la <xref:System.Data.OleDb.OleDbDataReader>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-132">Hierarchical rowsets, or chapters (OLE DB type **DBTYPE_HCHAPTER**, ADO type **adChapter**), can be retrieved using the <xref:System.Data.OleDb.OleDbDataReader>.</span></span> <span data-ttu-id="cfc97-133">Quand une requête comprenant un chapitre est retournée comme un **DataReader**, le chapitre est retourné en tant que colonne dans ce **DataReader** et est exposé comme un **DataReader** objet.</span><span class="sxs-lookup"><span data-stu-id="cfc97-133">When a query that includes a chapter is returned as a **DataReader**, the chapter is returned as a column in that **DataReader** and is exposed as a **DataReader** object.</span></span>  
  
 <span data-ttu-id="cfc97-134">ADO.NET **DataSet** peut également être utilisé pour représenter des ensembles de lignes hiérarchiques à l’aide de relations parent-enfant entre les tables.</span><span class="sxs-lookup"><span data-stu-id="cfc97-134">The ADO.NET **DataSet** can also be used to represent hierarchical rowsets by using parent-child relationships between tables.</span></span> <span data-ttu-id="cfc97-135">Pour plus d’informations, consultez [DataSets, DataTables et DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md).</span><span class="sxs-lookup"><span data-stu-id="cfc97-135">For more information, see [DataSets, DataTables, and DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md).</span></span>  
  
 <span data-ttu-id="cfc97-136">L'exemple de code suivant utilise le fournisseur MSDataShape pour générer une colonne chapitre de commandes pour chaque client d'une liste de clients.</span><span class="sxs-lookup"><span data-stu-id="cfc97-136">The following code example uses the MSDataShape Provider to generate a chapter column of orders for each customer in a list of customers.</span></span>  
  
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
  
## <a name="returning-results-with-oracle-ref-cursors"></a><span data-ttu-id="cfc97-137">Renvoi de résultats avec des REF CURSOR Oracle</span><span class="sxs-lookup"><span data-stu-id="cfc97-137">Returning results with Oracle REF CURSORs</span></span>  
 <span data-ttu-id="cfc97-138">Le fournisseur de données .NET Framework pour Oracle prend en charge l'utilisation des REF CURSOR Oracle pour retourner le résultat d'une requête.</span><span class="sxs-lookup"><span data-stu-id="cfc97-138">The .NET Framework Data Provider for Oracle supports the use of Oracle REF CURSORs to return a query result.</span></span> <span data-ttu-id="cfc97-139">Un REF CURSOR Oracle est retourné en tant qu'objet <xref:System.Data.OracleClient.OracleDataReader>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-139">An Oracle REF CURSOR is returned as an <xref:System.Data.OracleClient.OracleDataReader>.</span></span>  
  
 <span data-ttu-id="cfc97-140">Vous pouvez récupérer un <xref:System.Data.OracleClient.OracleDataReader> objet qui représente un REF CURSOR Oracle à l’aide de la <xref:System.Data.OracleClient.OracleCommand.ExecuteReader%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="cfc97-140">You can retrieve an <xref:System.Data.OracleClient.OracleDataReader> object that represents an Oracle REF CURSOR by using the <xref:System.Data.OracleClient.OracleCommand.ExecuteReader%2A> method.</span></span> <span data-ttu-id="cfc97-141">Vous pouvez également spécifier un <xref:System.Data.OracleClient.OracleCommand> qui retourne un ou plusieurs REF CURSOR Oracle en tant que le **SelectCommand** pour un <xref:System.Data.OracleClient.OracleDataAdapter> utilisé pour remplir un <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-141">You can also specify an <xref:System.Data.OracleClient.OracleCommand> that returns one or more Oracle REF CURSORs as the **SelectCommand** for an <xref:System.Data.OracleClient.OracleDataAdapter> used to fill a <xref:System.Data.DataSet>.</span></span>  
  
 <span data-ttu-id="cfc97-142">Pour accéder à un REF CURSOR retourné à partir d’une source de données Oracle, créez un <xref:System.Data.OracleClient.OracleCommand> pour votre requête et ajoutez un paramètre de sortie qui référence le REF CURSOR à la <xref:System.Data.OracleClient.OracleCommand.Parameters> collection de votre <xref:System.Data.OracleClient.OracleCommand>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-142">To access a REF CURSOR returned from an Oracle data source, create an <xref:System.Data.OracleClient.OracleCommand> for your query and add an output parameter that references the REF CURSOR to the <xref:System.Data.OracleClient.OracleCommand.Parameters> collection of your <xref:System.Data.OracleClient.OracleCommand>.</span></span> <span data-ttu-id="cfc97-143">Le nom du paramètre doit correspondre à celui du paramètre REF CURSOR de votre requête.</span><span class="sxs-lookup"><span data-stu-id="cfc97-143">The name of the parameter must match the name of the REF CURSOR parameter in your query.</span></span> <span data-ttu-id="cfc97-144">Définissez le type du paramètre à <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-144">Set the type of the parameter to <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType>.</span></span> <span data-ttu-id="cfc97-145">Le <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> méthode de votre <xref:System.Data.OracleClient.OracleCommand> retourne un <xref:System.Data.OracleClient.OracleDataReader> pour REF CURSOR.</span><span class="sxs-lookup"><span data-stu-id="cfc97-145">The <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> method of your <xref:System.Data.OracleClient.OracleCommand> returns an <xref:System.Data.OracleClient.OracleDataReader> for the REF CURSOR.</span></span>  
  
 <span data-ttu-id="cfc97-146">Si votre <xref:System.Data.OracleClient.OracleCommand> retourne plusieurs REF CURSOR, ajoutez plusieurs paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="cfc97-146">If your <xref:System.Data.OracleClient.OracleCommand> returns multiple REF CURSORS, add multiple output parameters.</span></span> <span data-ttu-id="cfc97-147">Vous pouvez accéder aux différents REF CURSOR en appelant le <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="cfc97-147">You can access the different REF CURSORs by calling the <xref:System.Data.OracleClient.OracleCommand.ExecuteReader?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="cfc97-148">L’appel à <xref:System.Data.OracleClient.OracleCommand.ExecuteReader> retourne un <xref:System.Data.OracleClient.OracleDataReader> qui référence le premier REF CURSOR.</span><span class="sxs-lookup"><span data-stu-id="cfc97-148">The call to <xref:System.Data.OracleClient.OracleCommand.ExecuteReader> returns an <xref:System.Data.OracleClient.OracleDataReader> referencing the first REF CURSOR.</span></span> <span data-ttu-id="cfc97-149">Vous pouvez ensuite appeler la <xref:System.Data.OracleClient.OracleDataReader.NextResult?displayProperty=nameWithType> méthode pour accéder aux REF CURSOR suivants.</span><span class="sxs-lookup"><span data-stu-id="cfc97-149">You can then call the <xref:System.Data.OracleClient.OracleDataReader.NextResult?displayProperty=nameWithType> method to access subsequent REF CURSORs.</span></span> <span data-ttu-id="cfc97-150">Bien que les paramètres dans votre <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> paramètres de sortie de collection correspondent les REF CURSOR par nom, le <xref:System.Data.OracleClient.OracleDataReader> y accède selon l’ordre dans lequel ils ont été ajoutés à la <xref:System.Data.OracleClient.OracleCommand.Parameters> collection.</span><span class="sxs-lookup"><span data-stu-id="cfc97-150">Although the parameters in your <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> collection match the REF CURSOR output parameters by name, the <xref:System.Data.OracleClient.OracleDataReader> accesses them in the order in which they were added to the <xref:System.Data.OracleClient.OracleCommand.Parameters> collection.</span></span>  
  
 <span data-ttu-id="cfc97-151">Considérez, par exemple, le package et le corps de package Oracle suivants.</span><span class="sxs-lookup"><span data-stu-id="cfc97-151">For example, consider the following Oracle package and package body.</span></span>  
  
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
  
 <span data-ttu-id="cfc97-152">Le code suivant crée un <xref:System.Data.OracleClient.OracleCommand> qui retourne les REF CURSOR d’un précédent package Oracle en ajoutant deux paramètres de type <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType> à la <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> collection.</span><span class="sxs-lookup"><span data-stu-id="cfc97-152">The following code creates an <xref:System.Data.OracleClient.OracleCommand> that returns the REF CURSORs from the previous Oracle package by adding two parameters of type <xref:System.Data.OracleClient.OracleType.Cursor?displayProperty=nameWithType> to the <xref:System.Data.OracleClient.OracleCommand.Parameters?displayProperty=nameWithType> collection.</span></span>  
  
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
  
 <span data-ttu-id="cfc97-153">Le code suivant retourne les résultats de la commande précédente à l’aide du <xref:System.Data.OracleClient.OracleDataReader.Read> et <xref:System.Data.OracleClient.OracleDataReader.NextResult> méthodes de la <xref:System.Data.OracleClient.OracleDataReader>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-153">The following code returns the results of the previous command using the <xref:System.Data.OracleClient.OracleDataReader.Read> and <xref:System.Data.OracleClient.OracleDataReader.NextResult> methods of the <xref:System.Data.OracleClient.OracleDataReader>.</span></span> <span data-ttu-id="cfc97-154">Les paramètres REF CURSOR sont retournés dans l'ordre.</span><span class="sxs-lookup"><span data-stu-id="cfc97-154">The REF CURSOR parameters are returned in order.</span></span>  
  
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
  
 <span data-ttu-id="cfc97-155">L’exemple suivant utilise la commande précédente pour remplir un <xref:System.Data.DataSet> avec les résultats du package Oracle.</span><span class="sxs-lookup"><span data-stu-id="cfc97-155">The following example uses the previous command to populate a <xref:System.Data.DataSet> with the results of the Oracle package.</span></span>  
  
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
>  <span data-ttu-id="cfc97-156">Pour éviter un **OverflowException**, nous recommandons que vous gérez également toute conversion à partir du type Oracle NUMBER en un type .NET Framework valide avant de stocker la valeur dans un <xref:System.Data.DataRow>.</span><span class="sxs-lookup"><span data-stu-id="cfc97-156">To avoid an **OverflowException**, we recommend that you also handle any conversion from the Oracle NUMBER type to a valid .NET Framework type before storing the value in a <xref:System.Data.DataRow>.</span></span> <span data-ttu-id="cfc97-157">Vous pouvez utiliser la <xref:System.Data.Common.DataAdapter.FillError> événement pour déterminer si un **OverflowException** s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cfc97-157">You can use the <xref:System.Data.Common.DataAdapter.FillError> event to determine if an **OverflowException** has occurred.</span></span> <span data-ttu-id="cfc97-158">Pour plus d’informations sur la <xref:System.Data.Common.DataAdapter.FillError> événement, consultez [gestion des événements DataAdapter](../../../../docs/framework/data/adonet/handling-dataadapter-events.md).</span><span class="sxs-lookup"><span data-stu-id="cfc97-158">For more information on the <xref:System.Data.Common.DataAdapter.FillError> event, see [Handling DataAdapter Events](../../../../docs/framework/data/adonet/handling-dataadapter-events.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfc97-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc97-159">See also</span></span>

- [<span data-ttu-id="cfc97-160">DataAdapters et DataReaders</span><span class="sxs-lookup"><span data-stu-id="cfc97-160">DataAdapters and DataReaders</span></span>](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [<span data-ttu-id="cfc97-161">Commandes et paramètres</span><span class="sxs-lookup"><span data-stu-id="cfc97-161">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [<span data-ttu-id="cfc97-162">Extraction des informations de schéma de base de données</span><span class="sxs-lookup"><span data-stu-id="cfc97-162">Retrieving Database Schema Information</span></span>](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)
- [<span data-ttu-id="cfc97-163">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="cfc97-163">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
