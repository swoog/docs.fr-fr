---
title: Restrictions de schéma
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 73d2980e-e73c-4987-913a-8ddc93d09144
ms.openlocfilehash: 040ecd8a2ce223f89601de735b77ccc81638c7af
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44079706"
---
# <a name="schema-restrictions"></a><span data-ttu-id="9c17a-102">Restrictions de schéma</span><span class="sxs-lookup"><span data-stu-id="9c17a-102">Schema Restrictions</span></span>
<span data-ttu-id="9c17a-103">Le deuxième paramètre facultatif de la **GetSchema** méthode est retournée les restrictions qui sont utilisées pour limiter la quantité d’informations de schéma, et il est transmis à la **GetSchema** sous forme de tableau de chaînes (méthode) .</span><span class="sxs-lookup"><span data-stu-id="9c17a-103">The second optional parameter of the **GetSchema** method is the restrictions that are used to limit the amount of schema information returned, and it is passed to the **GetSchema** method as an array of strings.</span></span> <span data-ttu-id="9c17a-104">La position dans le tableau détermine les valeurs que vous pouvez passer et équivaut au numéro de restriction.</span><span class="sxs-lookup"><span data-stu-id="9c17a-104">The position in the array determines the values that you can pass, and this is equivalent to the restriction number.</span></span>  
  
 <span data-ttu-id="9c17a-105">Par exemple, le tableau suivant décrit les restrictions prises en charge par la collection de schémas « Tables » utilisant le fournisseur de données .NET Framework pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9c17a-105">For example, the following table describes the restrictions supported by the "Tables" schema collection using the .NET Framework Data Provider for SQL Server.</span></span> <span data-ttu-id="9c17a-106">Des restrictions supplémentaires pour les collections de schémas SQL Server figurent à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9c17a-106">Additional restrictions for SQL Server schema collections are listed at the end of this topic.</span></span>  
  
|<span data-ttu-id="9c17a-107">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-107">Restriction Name</span></span>|<span data-ttu-id="9c17a-108">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-108">Parameter Name</span></span>|<span data-ttu-id="9c17a-109">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-109">Restriction Default</span></span>|<span data-ttu-id="9c17a-110">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-110">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-111">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-111">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-112">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-112">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-113">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-113">1</span></span>|  
|<span data-ttu-id="9c17a-114">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-114">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-115">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-115">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-116">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-116">2</span></span>|  
|<span data-ttu-id="9c17a-117">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-117">Table</span></span>|@Name|<span data-ttu-id="9c17a-118">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-118">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-119">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-119">3</span></span>|  
|<span data-ttu-id="9c17a-120">TableType</span><span class="sxs-lookup"><span data-stu-id="9c17a-120">TableType</span></span>|@TableType|<span data-ttu-id="9c17a-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9c17a-121">TABLE_TYPE</span></span>|<span data-ttu-id="9c17a-122">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-122">4</span></span>|  
  
## <a name="specifying-restriction-values"></a><span data-ttu-id="9c17a-123">Spécification des valeurs de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-123">Specifying Restriction Values</span></span>  
 <span data-ttu-id="9c17a-124">Pour utiliser l’une des restrictions de la collection de schémas « Tables », créez simplement un tableau de chaînes contenant quatre éléments, puis placez une valeur dans l’élément correspondant au numéro de restriction.</span><span class="sxs-lookup"><span data-stu-id="9c17a-124">To use one of the restrictions of the "Tables" schema collection, simply create an array of strings with four elements, then place a value in the element that matches the restriction number.</span></span> <span data-ttu-id="9c17a-125">Par exemple, pour restreindre les tables retournées par la **GetSchema** méthode exclusivement aux tables dans le schéma « Ventes », définissez le second élément du tableau sur « Sales » avant de le transmettre à la **GetSchema** (méthode).</span><span class="sxs-lookup"><span data-stu-id="9c17a-125">For example, to restrict the tables returned by the **GetSchema** method to only those tables in the "Sales" schema, set the second element of the array to "Sales" before passing it to the **GetSchema** method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9c17a-126">Les collections de restrictions pour `SqlClient` et `OracleClient` comportent une colonne `ParameterName` supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9c17a-126">The restrictions collections for `SqlClient` and `OracleClient` have an additional `ParameterName` column.</span></span> <span data-ttu-id="9c17a-127">La colonne par défaut de la restriction est encore là pour la compatibilité ascendante, mais est désormais ignorée.</span><span class="sxs-lookup"><span data-stu-id="9c17a-127">The restriction default column is still there for backwards compatibility, but is currently ignored.</span></span> <span data-ttu-id="9c17a-128">Il convient d'utiliser des requêtes paramétrées plutôt qu'un remplacement de chaîne afin de minimiser le risque d'attaque par injection SQL lors de la spécification de valeurs de restriction.</span><span class="sxs-lookup"><span data-stu-id="9c17a-128">Parameterized queries rather than string replacement should be used to minimize the risk of an SQL injection attack when specifying restriction values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9c17a-129">Le nombre d'éléments du tableau doit être inférieur ou égal au nombre de restrictions prises en charge pour la collection de schémas spécifiée, sans quoi une exception <xref:System.ArgumentException> est levée.</span><span class="sxs-lookup"><span data-stu-id="9c17a-129">The number of elements in the array must be less than or equal to the number of restrictions supported for the specified schema collection else an <xref:System.ArgumentException> will be thrown.</span></span> <span data-ttu-id="9c17a-130">Il peut y avoir moins de restrictions que le nombre maximal de restrictions.</span><span class="sxs-lookup"><span data-stu-id="9c17a-130">There can be fewer than the maximum number of restrictions.</span></span> <span data-ttu-id="9c17a-131">Les restrictions manquantes sont supposées avoir la valeur null (aucune restriction).</span><span class="sxs-lookup"><span data-stu-id="9c17a-131">The missing restrictions are assumed to be null (unrestricted).</span></span>  
  
 <span data-ttu-id="9c17a-132">Vous pouvez interroger un fournisseur .NET Framework managé afin de déterminer la liste des restrictions prises en charge en appelant le **GetSchema** méthode portant le nom de la collection de schémas de restrictions, « restrictions ».</span><span class="sxs-lookup"><span data-stu-id="9c17a-132">You can query a .NET Framework managed provider to determine the list of supported restrictions by calling the **GetSchema** method with the name of the restrictions schema collection, which is "Restrictions".</span></span> <span data-ttu-id="9c17a-133">Cette opération retourne un <xref:System.Data.DataTable> contenant une liste des noms de collections, des noms de restriction, des valeurs de restriction par défaut et des numéros de restriction.</span><span class="sxs-lookup"><span data-stu-id="9c17a-133">This will return a <xref:System.Data.DataTable> with a list of the collection names, the restriction names, the default restriction values, and the restriction numbers.</span></span>  
  
### <a name="example"></a><span data-ttu-id="9c17a-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c17a-134">Example</span></span>  
 <span data-ttu-id="9c17a-135">Les exemples suivants montrent comment utiliser le <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> méthode du fournisseur de données .NET Framework pour SQL Server <xref:System.Data.SqlClient.SqlConnection> classe à récupérer les informations de schéma sur toutes les tables contenues dans le **AdventureWorks**exemple de base de données, et pour restreindre les informations retournées exclusivement aux tables dans le schéma « Sales » :</span><span class="sxs-lookup"><span data-stu-id="9c17a-135">The following examples demonstrate how to use the <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of the .NET Framework Data Provider for the SQL Server <xref:System.Data.SqlClient.SqlConnection> class to retrieve schema information about all of the tables contained in the **AdventureWorks** sample database, and to restrict the information returned to only those tables in the "Sales" schema:</span></span>  
  
```vb  
Imports System.Data.SqlClient  
  
Module Module1  
Sub Main()  
  Dim connectionString As String = _  
    "Data Source=(local);Database=AdventureWorks;" & _  
       "Integrated Security=true;";  
  
  Dim restrictions(3) As String  
  Using connection As New SqlConnection(connectionString)  
    connection.Open()  
  
    'Specify the restrictions.  
    restrictions(1) = "Sales"  
    Dim table As DataTable = connection.GetSchema("Tables", _  
       restrictions)  
  
    ' Display the contents of the table.  
      For Each row As DataRow In table.Rows  
         For Each col As DataColumn In table.Columns  
            Console.WriteLine("{0} = {1}", col.ColumnName, row(col))  
         Next  
         Console.WriteLine("============================")  
      Next  
    Console.WriteLine("Press any key to continue.")  
    Console.ReadKey()  
  End Using  
End Sub  
End Module  
```  
  
```csharp  
using System;  
using System.Data;  
using System.Data.SqlClient;  
  
class Program  
{  
  static void Main()  
  {  
    string connectionString =   
       "Data Source=(local);Database=AdventureWorks;" +  
       "Integrated Security=true;";  
    using (SqlConnection connection =  
       new SqlConnection(connectionString))  
    {  
        connection.Open();  
  
        // Specify the restrictions.  
        string[] restrictions = new string[4];  
        restrictions[1] = "Sales";  
        System.Data.DataTable table = connection.GetSchema(  
          "Tables", restrictions);  
  
        // Display the contents of the table.  
        foreach (System.Data.DataRow row in table.Rows)  
        {  
            foreach (System.Data.DataColumn col in table.Columns)  
            {  
                Console.WriteLine("{0} = {1}",   
                  col.ColumnName, row[col]);  
            }  
            Console.WriteLine("============================");  
        }  
        Console.WriteLine("Press any key to continue.");  
        Console.ReadKey();  
    }  
  }  
  
  private static string GetConnectionString()  
  {  
     // To avoid storing the connection string in your code,  
     // you can retrieve it from a configuration file.  
     return "Data Source=(local);Database=AdventureWorks;" +  
        "Integrated Security=true;";  
  }  
  
  private static void DisplayData(System.Data.DataTable table)  
  {  
     foreach (System.Data.DataRow row in table.Rows)  
     {  
        foreach (System.Data.DataColumn col in table.Columns)  
        {  
           Console.WriteLine("{0} = {1}", col.ColumnName, row[col]);  
        }  
     Console.WriteLine("============================");  
     }  
  }  
}  
```  
  
## <a name="sql-server-schema-restrictions"></a><span data-ttu-id="9c17a-136">Restrictions de schéma SQL Server</span><span class="sxs-lookup"><span data-stu-id="9c17a-136">SQL Server Schema Restrictions</span></span>  
 <span data-ttu-id="9c17a-137">Les tableaux suivants énumèrent les restrictions pour les collections de schémas SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9c17a-137">The following tables list the restrictions for SQL Server schema collections.</span></span>  
  
### <a name="users"></a><span data-ttu-id="9c17a-138">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9c17a-138">Users</span></span>  
  
|<span data-ttu-id="9c17a-139">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-139">Restriction Name</span></span>|<span data-ttu-id="9c17a-140">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-140">Parameter Name</span></span>|<span data-ttu-id="9c17a-141">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-141">Restriction Default</span></span>|<span data-ttu-id="9c17a-142">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-142">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-143">User_Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-143">User_Name</span></span>|@Name|<span data-ttu-id="9c17a-144">name</span><span class="sxs-lookup"><span data-stu-id="9c17a-144">name</span></span>|<span data-ttu-id="9c17a-145">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-145">1</span></span>|  
  
### <a name="databases"></a><span data-ttu-id="9c17a-146">Bases de données</span><span class="sxs-lookup"><span data-stu-id="9c17a-146">Databases</span></span>  
  
|<span data-ttu-id="9c17a-147">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-147">Restriction Name</span></span>|<span data-ttu-id="9c17a-148">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-148">Parameter Name</span></span>|<span data-ttu-id="9c17a-149">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-149">Restriction Default</span></span>|<span data-ttu-id="9c17a-150">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-150">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-151">Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-151">Name</span></span>|@Name|<span data-ttu-id="9c17a-152">Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-152">Name</span></span>|<span data-ttu-id="9c17a-153">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-153">1</span></span>|  
  
### <a name="tables"></a><span data-ttu-id="9c17a-154">Tables</span><span class="sxs-lookup"><span data-stu-id="9c17a-154">Tables</span></span>  
  
|<span data-ttu-id="9c17a-155">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-155">Restriction Name</span></span>|<span data-ttu-id="9c17a-156">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-156">Parameter Name</span></span>|<span data-ttu-id="9c17a-157">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-157">Restriction Default</span></span>|<span data-ttu-id="9c17a-158">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-158">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-159">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-159">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-160">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-160">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-161">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-161">1</span></span>|  
|<span data-ttu-id="9c17a-162">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-162">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-163">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-163">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-164">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-164">2</span></span>|  
|<span data-ttu-id="9c17a-165">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-165">Table</span></span>|@Name|<span data-ttu-id="9c17a-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-166">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-167">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-167">3</span></span>|  
|<span data-ttu-id="9c17a-168">TableType</span><span class="sxs-lookup"><span data-stu-id="9c17a-168">TableType</span></span>|@TableType|<span data-ttu-id="9c17a-169">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9c17a-169">TABLE_TYPE</span></span>|<span data-ttu-id="9c17a-170">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-170">4</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="9c17a-171">Columns</span><span class="sxs-lookup"><span data-stu-id="9c17a-171">Columns</span></span>  
  
|<span data-ttu-id="9c17a-172">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-172">Restriction Name</span></span>|<span data-ttu-id="9c17a-173">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-173">Parameter Name</span></span>|<span data-ttu-id="9c17a-174">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-174">Restriction Default</span></span>|<span data-ttu-id="9c17a-175">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-175">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-176">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-176">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-177">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-177">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-178">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-178">1</span></span>|  
|<span data-ttu-id="9c17a-179">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-179">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-180">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-180">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-181">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-181">2</span></span>|  
|<span data-ttu-id="9c17a-182">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-182">Table</span></span>|@Table|<span data-ttu-id="9c17a-183">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-183">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-184">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-184">3</span></span>|  
|<span data-ttu-id="9c17a-185">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c17a-185">Column</span></span>|@Column|<span data-ttu-id="9c17a-186">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-186">COLUMN_NAME</span></span>|<span data-ttu-id="9c17a-187">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-187">4</span></span>|  
  
### <a name="structuredtypemembers"></a><span data-ttu-id="9c17a-188">StructuredTypeMembers</span><span class="sxs-lookup"><span data-stu-id="9c17a-188">StructuredTypeMembers</span></span>  
  
|<span data-ttu-id="9c17a-189">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-189">Restriction Name</span></span>|<span data-ttu-id="9c17a-190">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-190">Parameter Name</span></span>|<span data-ttu-id="9c17a-191">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-191">Restriction Default</span></span>|<span data-ttu-id="9c17a-192">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-192">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-193">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-193">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-194">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-194">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-195">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-195">1</span></span>|  
|<span data-ttu-id="9c17a-196">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-196">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-197">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-197">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-198">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-198">2</span></span>|  
|<span data-ttu-id="9c17a-199">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-199">Table</span></span>|@Table|<span data-ttu-id="9c17a-200">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-200">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-201">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-201">3</span></span>|  
|<span data-ttu-id="9c17a-202">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c17a-202">Column</span></span>|@Column|<span data-ttu-id="9c17a-203">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-203">COLUMN_NAME</span></span>|<span data-ttu-id="9c17a-204">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-204">4</span></span>|  
  
### <a name="views"></a><span data-ttu-id="9c17a-205">Vues</span><span class="sxs-lookup"><span data-stu-id="9c17a-205">Views</span></span>  
  
|<span data-ttu-id="9c17a-206">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-206">Restriction Name</span></span>|<span data-ttu-id="9c17a-207">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-207">Parameter Name</span></span>|<span data-ttu-id="9c17a-208">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-208">Restriction Default</span></span>|<span data-ttu-id="9c17a-209">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-209">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-210">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-210">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-211">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-211">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-212">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-212">1</span></span>|  
|<span data-ttu-id="9c17a-213">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-213">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-214">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-214">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-215">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-215">2</span></span>|  
|<span data-ttu-id="9c17a-216">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-216">Table</span></span>|@Table|<span data-ttu-id="9c17a-217">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-217">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-218">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-218">3</span></span>|  
  
### <a name="viewcolumns"></a><span data-ttu-id="9c17a-219">ViewColumns</span><span class="sxs-lookup"><span data-stu-id="9c17a-219">ViewColumns</span></span>  
  
|<span data-ttu-id="9c17a-220">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-220">Restriction Name</span></span>|<span data-ttu-id="9c17a-221">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-221">Parameter Name</span></span>|<span data-ttu-id="9c17a-222">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-222">Restriction Default</span></span>|<span data-ttu-id="9c17a-223">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-223">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-224">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-224">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-225">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-225">VIEW_CATALOG</span></span>|<span data-ttu-id="9c17a-226">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-226">1</span></span>|  
|<span data-ttu-id="9c17a-227">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-227">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-228">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-228">VIEW_SCHEMA</span></span>|<span data-ttu-id="9c17a-229">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-229">2</span></span>|  
|<span data-ttu-id="9c17a-230">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-230">Table</span></span>|@Table|<span data-ttu-id="9c17a-231">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-231">VIEW_NAME</span></span>|<span data-ttu-id="9c17a-232">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-232">3</span></span>|  
|<span data-ttu-id="9c17a-233">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c17a-233">Column</span></span>|@Column|<span data-ttu-id="9c17a-234">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-234">COLUMN_NAME</span></span>|<span data-ttu-id="9c17a-235">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-235">4</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="9c17a-236">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="9c17a-236">ProcedureParameters</span></span>  
  
|<span data-ttu-id="9c17a-237">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-237">Restriction Name</span></span>|<span data-ttu-id="9c17a-238">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-238">Parameter Name</span></span>|<span data-ttu-id="9c17a-239">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-239">Restriction Default</span></span>|<span data-ttu-id="9c17a-240">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-240">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-241">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-241">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-242">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-242">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="9c17a-243">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-243">1</span></span>|  
|<span data-ttu-id="9c17a-244">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-244">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-245">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-245">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="9c17a-246">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-246">2</span></span>|  
|<span data-ttu-id="9c17a-247">Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-247">Name</span></span>|@Name|<span data-ttu-id="9c17a-248">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-248">SPECIFIC_NAME</span></span>|<span data-ttu-id="9c17a-249">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-249">3</span></span>|  
|<span data-ttu-id="9c17a-250">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-250">Parameter</span></span>|@Parameter|<span data-ttu-id="9c17a-251">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-251">PARAMETER_NAME</span></span>|<span data-ttu-id="9c17a-252">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-252">4</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="9c17a-253">Procédures</span><span class="sxs-lookup"><span data-stu-id="9c17a-253">Procedures</span></span>  
  
|<span data-ttu-id="9c17a-254">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-254">Restriction Name</span></span>|<span data-ttu-id="9c17a-255">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-255">Parameter Name</span></span>|<span data-ttu-id="9c17a-256">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-256">Restriction Default</span></span>|<span data-ttu-id="9c17a-257">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-257">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-258">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-259">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-259">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="9c17a-260">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-260">1</span></span>|  
|<span data-ttu-id="9c17a-261">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-261">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-262">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-262">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="9c17a-263">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-263">2</span></span>|  
|<span data-ttu-id="9c17a-264">Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-264">Name</span></span>|@Name|<span data-ttu-id="9c17a-265">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-265">SPECIFIC_NAME</span></span>|<span data-ttu-id="9c17a-266">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-266">3</span></span>|  
|<span data-ttu-id="9c17a-267">Type</span><span class="sxs-lookup"><span data-stu-id="9c17a-267">Type</span></span>|@Type|<span data-ttu-id="9c17a-268">ROUTINE_TYPE</span><span class="sxs-lookup"><span data-stu-id="9c17a-268">ROUTINE_TYPE</span></span>|<span data-ttu-id="9c17a-269">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-269">4</span></span>|  
  
### <a name="indexcolumns"></a><span data-ttu-id="9c17a-270">IndexColumns</span><span class="sxs-lookup"><span data-stu-id="9c17a-270">IndexColumns</span></span>  
  
|<span data-ttu-id="9c17a-271">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-271">Restriction Name</span></span>|<span data-ttu-id="9c17a-272">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-272">Parameter Name</span></span>|<span data-ttu-id="9c17a-273">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-273">Restriction Default</span></span>|<span data-ttu-id="9c17a-274">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-274">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-275">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-275">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-276">db_name()</span><span class="sxs-lookup"><span data-stu-id="9c17a-276">db_name()</span></span>|<span data-ttu-id="9c17a-277">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-277">1</span></span>|  
|<span data-ttu-id="9c17a-278">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-278">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-279">user_name()</span><span class="sxs-lookup"><span data-stu-id="9c17a-279">user_name()</span></span>|<span data-ttu-id="9c17a-280">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-280">2</span></span>|  
|<span data-ttu-id="9c17a-281">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-281">Table</span></span>|@Table|<span data-ttu-id="9c17a-282">o.name</span><span class="sxs-lookup"><span data-stu-id="9c17a-282">o.name</span></span>|<span data-ttu-id="9c17a-283">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-283">3</span></span>|  
|<span data-ttu-id="9c17a-284">ConstraintName</span><span class="sxs-lookup"><span data-stu-id="9c17a-284">ConstraintName</span></span>|@ConstraintName|<span data-ttu-id="9c17a-285">x.name</span><span class="sxs-lookup"><span data-stu-id="9c17a-285">x.name</span></span>|<span data-ttu-id="9c17a-286">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-286">4</span></span>|  
|<span data-ttu-id="9c17a-287">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c17a-287">Column</span></span>|@Column|<span data-ttu-id="9c17a-288">c.name</span><span class="sxs-lookup"><span data-stu-id="9c17a-288">c.name</span></span>|<span data-ttu-id="9c17a-289">5</span><span class="sxs-lookup"><span data-stu-id="9c17a-289">5</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="9c17a-290">Index</span><span class="sxs-lookup"><span data-stu-id="9c17a-290">Indexes</span></span>  
  
|<span data-ttu-id="9c17a-291">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-291">Restriction Name</span></span>|<span data-ttu-id="9c17a-292">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-292">Parameter Name</span></span>|<span data-ttu-id="9c17a-293">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-293">Restriction Default</span></span>|<span data-ttu-id="9c17a-294">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-294">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-295">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-295">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-296">db_name()</span><span class="sxs-lookup"><span data-stu-id="9c17a-296">db_name()</span></span>|<span data-ttu-id="9c17a-297">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-297">1</span></span>|  
|<span data-ttu-id="9c17a-298">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-298">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-299">user_name()</span><span class="sxs-lookup"><span data-stu-id="9c17a-299">user_name()</span></span>|<span data-ttu-id="9c17a-300">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-300">2</span></span>|  
|<span data-ttu-id="9c17a-301">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-301">Table</span></span>|@Table|<span data-ttu-id="9c17a-302">o.name</span><span class="sxs-lookup"><span data-stu-id="9c17a-302">o.name</span></span>|<span data-ttu-id="9c17a-303">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-303">3</span></span>|  
  
### <a name="userdefinedtypes"></a><span data-ttu-id="9c17a-304">UserDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="9c17a-304">UserDefinedTypes</span></span>  
  
|<span data-ttu-id="9c17a-305">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-305">Restriction Name</span></span>|<span data-ttu-id="9c17a-306">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-306">Parameter Name</span></span>|<span data-ttu-id="9c17a-307">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-307">Restriction Default</span></span>|<span data-ttu-id="9c17a-308">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-308">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-309">assembly_name</span><span class="sxs-lookup"><span data-stu-id="9c17a-309">assembly_name</span></span>|@AssemblyName|<span data-ttu-id="9c17a-310">assemblies.name</span><span class="sxs-lookup"><span data-stu-id="9c17a-310">assemblies.name</span></span>|<span data-ttu-id="9c17a-311">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-311">1</span></span>|  
|<span data-ttu-id="9c17a-312">udt_name</span><span class="sxs-lookup"><span data-stu-id="9c17a-312">udt_name</span></span>|@UDTName|<span data-ttu-id="9c17a-313">types.assembly_class</span><span class="sxs-lookup"><span data-stu-id="9c17a-313">types.assembly_class</span></span>|<span data-ttu-id="9c17a-314">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-314">2</span></span>|  
  
### <a name="foreignkeys"></a><span data-ttu-id="9c17a-315">ForeignKeys</span><span class="sxs-lookup"><span data-stu-id="9c17a-315">ForeignKeys</span></span>  
  
|<span data-ttu-id="9c17a-316">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-316">Restriction Name</span></span>|<span data-ttu-id="9c17a-317">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-317">Parameter Name</span></span>|<span data-ttu-id="9c17a-318">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-318">Restriction Default</span></span>|<span data-ttu-id="9c17a-319">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-319">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-320">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-320">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-321">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-321">CONSTRAINT_CATALOG</span></span>|<span data-ttu-id="9c17a-322">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-322">1</span></span>|  
|<span data-ttu-id="9c17a-323">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-323">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-324">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-324">CONSTRAINT_SCHEMA</span></span>|<span data-ttu-id="9c17a-325">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-325">2</span></span>|  
|<span data-ttu-id="9c17a-326">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-326">Table</span></span>|@Table|<span data-ttu-id="9c17a-327">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-327">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-328">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-328">3</span></span>|  
|<span data-ttu-id="9c17a-329">Name</span><span class="sxs-lookup"><span data-stu-id="9c17a-329">Name</span></span>|@Name|<span data-ttu-id="9c17a-330">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-330">CONSTRAINT_NAME</span></span>|<span data-ttu-id="9c17a-331">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-331">4</span></span>|  
  
## <a name="sql-server-2008-schema-restrictions"></a><span data-ttu-id="9c17a-332">Restrictions de schéma SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c17a-332">SQL Server 2008 Schema Restrictions</span></span>  
 <span data-ttu-id="9c17a-333">Les tableaux suivants répertorient les restrictions pour les collections de schémas SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9c17a-333">The following tables list the restrictions for SQL Server 2008 schema collections.</span></span> <span data-ttu-id="9c17a-334">Ces restrictions s'appliquent à partir de la version 3.5 SP1 de .NET Framework et SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9c17a-334">These restrictions are valid beginning with version 3.5 SP1 of the .NET Framework and SQL Server 2008.</span></span> <span data-ttu-id="9c17a-335">Elles ne sont pas prises en charge dans les versions précédentes de .NET Framework et SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9c17a-335">They are not supported in earlier versions of the .NET Framework and SQL Server.</span></span>  
  
### <a name="columnsetcolumns"></a><span data-ttu-id="9c17a-336">ColumnSetColumns</span><span class="sxs-lookup"><span data-stu-id="9c17a-336">ColumnSetColumns</span></span>  
  
|<span data-ttu-id="9c17a-337">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-337">Restriction Name</span></span>|<span data-ttu-id="9c17a-338">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-338">Parameter Name</span></span>|<span data-ttu-id="9c17a-339">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-339">Restriction Default</span></span>|<span data-ttu-id="9c17a-340">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-340">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-341">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-341">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-342">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-342">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-343">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-343">1</span></span>|  
|<span data-ttu-id="9c17a-344">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-344">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-345">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-345">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-346">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-346">2</span></span>|  
|<span data-ttu-id="9c17a-347">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-347">Table</span></span>|@Table|<span data-ttu-id="9c17a-348">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-348">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-349">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-349">3</span></span>|  
  
### <a name="allcolumns"></a><span data-ttu-id="9c17a-350">AllColumns</span><span class="sxs-lookup"><span data-stu-id="9c17a-350">AllColumns</span></span>  
  
|<span data-ttu-id="9c17a-351">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-351">Restriction Name</span></span>|<span data-ttu-id="9c17a-352">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="9c17a-352">Parameter Name</span></span>|<span data-ttu-id="9c17a-353">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-353">Restriction Default</span></span>|<span data-ttu-id="9c17a-354">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="9c17a-354">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="9c17a-355">Catalogue</span><span class="sxs-lookup"><span data-stu-id="9c17a-355">Catalog</span></span>|@Catalog|<span data-ttu-id="9c17a-356">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="9c17a-356">TABLE_CATALOG</span></span>|<span data-ttu-id="9c17a-357">1</span><span class="sxs-lookup"><span data-stu-id="9c17a-357">1</span></span>|  
|<span data-ttu-id="9c17a-358">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="9c17a-358">Owner</span></span>|@Owner|<span data-ttu-id="9c17a-359">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="9c17a-359">TABLE_SCHEMA</span></span>|<span data-ttu-id="9c17a-360">2</span><span class="sxs-lookup"><span data-stu-id="9c17a-360">2</span></span>|  
|<span data-ttu-id="9c17a-361">Table</span><span class="sxs-lookup"><span data-stu-id="9c17a-361">Table</span></span>|@Table|<span data-ttu-id="9c17a-362">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-362">TABLE_NAME</span></span>|<span data-ttu-id="9c17a-363">3</span><span class="sxs-lookup"><span data-stu-id="9c17a-363">3</span></span>|  
|<span data-ttu-id="9c17a-364">Colonne</span><span class="sxs-lookup"><span data-stu-id="9c17a-364">Column</span></span>|@Column|<span data-ttu-id="9c17a-365">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="9c17a-365">COLUMN_NAME</span></span>|<span data-ttu-id="9c17a-366">4</span><span class="sxs-lookup"><span data-stu-id="9c17a-366">4</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9c17a-367">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c17a-367">See Also</span></span>  
 [<span data-ttu-id="9c17a-368">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="9c17a-368">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
