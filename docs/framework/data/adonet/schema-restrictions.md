---
title: Restrictions de schéma
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 73d2980e-e73c-4987-913a-8ddc93d09144
ms.openlocfilehash: b5044d39d1dc5d2fa7d2ce691cdda7075fa0e32a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61878408"
---
# <a name="schema-restrictions"></a><span data-ttu-id="64885-102">Restrictions de schéma</span><span class="sxs-lookup"><span data-stu-id="64885-102">Schema Restrictions</span></span>
<span data-ttu-id="64885-103">Le deuxième paramètre facultatif de la **GetSchema** méthode est retournée les restrictions qui sont utilisées pour limiter la quantité d’informations de schéma, et il est transmis à la **GetSchema** sous forme de tableau de chaînes (méthode) .</span><span class="sxs-lookup"><span data-stu-id="64885-103">The second optional parameter of the **GetSchema** method is the restrictions that are used to limit the amount of schema information returned, and it is passed to the **GetSchema** method as an array of strings.</span></span> <span data-ttu-id="64885-104">La position dans le tableau détermine les valeurs que vous pouvez passer et équivaut au numéro de restriction.</span><span class="sxs-lookup"><span data-stu-id="64885-104">The position in the array determines the values that you can pass, and this is equivalent to the restriction number.</span></span>  
  
 <span data-ttu-id="64885-105">Par exemple, le tableau suivant décrit les restrictions prises en charge par la collection de schémas « Tables » utilisant le fournisseur de données .NET Framework pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64885-105">For example, the following table describes the restrictions supported by the "Tables" schema collection using the .NET Framework Data Provider for SQL Server.</span></span> <span data-ttu-id="64885-106">Des restrictions supplémentaires pour les collections de schémas SQL Server figurent à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="64885-106">Additional restrictions for SQL Server schema collections are listed at the end of this topic.</span></span>  
  
|<span data-ttu-id="64885-107">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-107">Restriction Name</span></span>|<span data-ttu-id="64885-108">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-108">Parameter Name</span></span>|<span data-ttu-id="64885-109">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-109">Restriction Default</span></span>|<span data-ttu-id="64885-110">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-110">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-111">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-111">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-112">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-112">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-113">1</span><span class="sxs-lookup"><span data-stu-id="64885-113">1</span></span>|  
|<span data-ttu-id="64885-114">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-114">Owner</span></span>|@Owner|<span data-ttu-id="64885-115">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-115">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-116">2</span><span class="sxs-lookup"><span data-stu-id="64885-116">2</span></span>|  
|<span data-ttu-id="64885-117">Table</span><span class="sxs-lookup"><span data-stu-id="64885-117">Table</span></span>|@Name|<span data-ttu-id="64885-118">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-118">TABLE_NAME</span></span>|<span data-ttu-id="64885-119">3</span><span class="sxs-lookup"><span data-stu-id="64885-119">3</span></span>|  
|<span data-ttu-id="64885-120">TableType</span><span class="sxs-lookup"><span data-stu-id="64885-120">TableType</span></span>|@TableType|<span data-ttu-id="64885-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="64885-121">TABLE_TYPE</span></span>|<span data-ttu-id="64885-122">4</span><span class="sxs-lookup"><span data-stu-id="64885-122">4</span></span>|  
  
## <a name="specifying-restriction-values"></a><span data-ttu-id="64885-123">Spécification des valeurs de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-123">Specifying Restriction Values</span></span>  
 <span data-ttu-id="64885-124">Pour utiliser l’une des restrictions de la collection de schémas « Tables », créez simplement un tableau de chaînes contenant quatre éléments, puis placez une valeur dans l’élément correspondant au numéro de restriction.</span><span class="sxs-lookup"><span data-stu-id="64885-124">To use one of the restrictions of the "Tables" schema collection, simply create an array of strings with four elements, then place a value in the element that matches the restriction number.</span></span> <span data-ttu-id="64885-125">Par exemple, pour restreindre les tables retournées par la **GetSchema** méthode exclusivement aux tables dans le schéma « Ventes », définissez le second élément du tableau sur « Sales » avant de le transmettre à la **GetSchema** (méthode).</span><span class="sxs-lookup"><span data-stu-id="64885-125">For example, to restrict the tables returned by the **GetSchema** method to only those tables in the "Sales" schema, set the second element of the array to "Sales" before passing it to the **GetSchema** method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="64885-126">Les collections de restrictions pour `SqlClient` et `OracleClient` comportent une colonne `ParameterName` supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="64885-126">The restrictions collections for `SqlClient` and `OracleClient` have an additional `ParameterName` column.</span></span> <span data-ttu-id="64885-127">La colonne par défaut de la restriction est encore là pour la compatibilité ascendante, mais est désormais ignorée.</span><span class="sxs-lookup"><span data-stu-id="64885-127">The restriction default column is still there for backwards compatibility, but is currently ignored.</span></span> <span data-ttu-id="64885-128">Il convient d'utiliser des requêtes paramétrées plutôt qu'un remplacement de chaîne afin de minimiser le risque d'attaque par injection SQL lors de la spécification de valeurs de restriction.</span><span class="sxs-lookup"><span data-stu-id="64885-128">Parameterized queries rather than string replacement should be used to minimize the risk of an SQL injection attack when specifying restriction values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="64885-129">Le nombre d'éléments du tableau doit être inférieur ou égal au nombre de restrictions prises en charge pour la collection de schémas spécifiée, sans quoi une exception <xref:System.ArgumentException> est levée.</span><span class="sxs-lookup"><span data-stu-id="64885-129">The number of elements in the array must be less than or equal to the number of restrictions supported for the specified schema collection else an <xref:System.ArgumentException> will be thrown.</span></span> <span data-ttu-id="64885-130">Il peut y avoir moins de restrictions que le nombre maximal de restrictions.</span><span class="sxs-lookup"><span data-stu-id="64885-130">There can be fewer than the maximum number of restrictions.</span></span> <span data-ttu-id="64885-131">Les restrictions manquantes sont supposées avoir la valeur null (aucune restriction).</span><span class="sxs-lookup"><span data-stu-id="64885-131">The missing restrictions are assumed to be null (unrestricted).</span></span>  
  
 <span data-ttu-id="64885-132">Vous pouvez interroger un fournisseur .NET Framework managé afin de déterminer la liste des restrictions prises en charge en appelant le **GetSchema** méthode portant le nom de la collection de schémas de restrictions, « restrictions ».</span><span class="sxs-lookup"><span data-stu-id="64885-132">You can query a .NET Framework managed provider to determine the list of supported restrictions by calling the **GetSchema** method with the name of the restrictions schema collection, which is "Restrictions".</span></span> <span data-ttu-id="64885-133">Cette opération retourne un <xref:System.Data.DataTable> contenant une liste des noms de collections, des noms de restriction, des valeurs de restriction par défaut et des numéros de restriction.</span><span class="sxs-lookup"><span data-stu-id="64885-133">This will return a <xref:System.Data.DataTable> with a list of the collection names, the restriction names, the default restriction values, and the restriction numbers.</span></span>  
  
### <a name="example"></a><span data-ttu-id="64885-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="64885-134">Example</span></span>  
 <span data-ttu-id="64885-135">Les exemples suivants montrent comment utiliser le <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> méthode du fournisseur de données .NET Framework pour SQL Server <xref:System.Data.SqlClient.SqlConnection> classe à récupérer les informations de schéma sur toutes les tables contenues dans le **AdventureWorks**exemple de base de données, et pour restreindre les informations retournées exclusivement aux tables dans le schéma « Sales » :</span><span class="sxs-lookup"><span data-stu-id="64885-135">The following examples demonstrate how to use the <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of the .NET Framework Data Provider for the SQL Server <xref:System.Data.SqlClient.SqlConnection> class to retrieve schema information about all of the tables contained in the **AdventureWorks** sample database, and to restrict the information returned to only those tables in the "Sales" schema:</span></span>  
  
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
  
## <a name="sql-server-schema-restrictions"></a><span data-ttu-id="64885-136">Restrictions de schéma SQL Server</span><span class="sxs-lookup"><span data-stu-id="64885-136">SQL Server Schema Restrictions</span></span>  
 <span data-ttu-id="64885-137">Les tableaux suivants énumèrent les restrictions pour les collections de schémas SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64885-137">The following tables list the restrictions for SQL Server schema collections.</span></span>  
  
### <a name="users"></a><span data-ttu-id="64885-138">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="64885-138">Users</span></span>  
  
|<span data-ttu-id="64885-139">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-139">Restriction Name</span></span>|<span data-ttu-id="64885-140">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-140">Parameter Name</span></span>|<span data-ttu-id="64885-141">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-141">Restriction Default</span></span>|<span data-ttu-id="64885-142">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-142">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-143">User_Name</span><span class="sxs-lookup"><span data-stu-id="64885-143">User_Name</span></span>|@Name|<span data-ttu-id="64885-144">name</span><span class="sxs-lookup"><span data-stu-id="64885-144">name</span></span>|<span data-ttu-id="64885-145">1</span><span class="sxs-lookup"><span data-stu-id="64885-145">1</span></span>|  
  
### <a name="databases"></a><span data-ttu-id="64885-146">Bases de données</span><span class="sxs-lookup"><span data-stu-id="64885-146">Databases</span></span>  
  
|<span data-ttu-id="64885-147">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-147">Restriction Name</span></span>|<span data-ttu-id="64885-148">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-148">Parameter Name</span></span>|<span data-ttu-id="64885-149">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-149">Restriction Default</span></span>|<span data-ttu-id="64885-150">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-150">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-151">Nom</span><span class="sxs-lookup"><span data-stu-id="64885-151">Name</span></span>|@Name|<span data-ttu-id="64885-152">Nom</span><span class="sxs-lookup"><span data-stu-id="64885-152">Name</span></span>|<span data-ttu-id="64885-153">1</span><span class="sxs-lookup"><span data-stu-id="64885-153">1</span></span>|  
  
### <a name="tables"></a><span data-ttu-id="64885-154">Tables</span><span class="sxs-lookup"><span data-stu-id="64885-154">Tables</span></span>  
  
|<span data-ttu-id="64885-155">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-155">Restriction Name</span></span>|<span data-ttu-id="64885-156">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-156">Parameter Name</span></span>|<span data-ttu-id="64885-157">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-157">Restriction Default</span></span>|<span data-ttu-id="64885-158">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-158">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-159">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-159">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-160">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-160">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-161">1</span><span class="sxs-lookup"><span data-stu-id="64885-161">1</span></span>|  
|<span data-ttu-id="64885-162">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-162">Owner</span></span>|@Owner|<span data-ttu-id="64885-163">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-163">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-164">2</span><span class="sxs-lookup"><span data-stu-id="64885-164">2</span></span>|  
|<span data-ttu-id="64885-165">Table</span><span class="sxs-lookup"><span data-stu-id="64885-165">Table</span></span>|@Name|<span data-ttu-id="64885-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-166">TABLE_NAME</span></span>|<span data-ttu-id="64885-167">3</span><span class="sxs-lookup"><span data-stu-id="64885-167">3</span></span>|  
|<span data-ttu-id="64885-168">TableType</span><span class="sxs-lookup"><span data-stu-id="64885-168">TableType</span></span>|@TableType|<span data-ttu-id="64885-169">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="64885-169">TABLE_TYPE</span></span>|<span data-ttu-id="64885-170">4</span><span class="sxs-lookup"><span data-stu-id="64885-170">4</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="64885-171">Colonnes</span><span class="sxs-lookup"><span data-stu-id="64885-171">Columns</span></span>  
  
|<span data-ttu-id="64885-172">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-172">Restriction Name</span></span>|<span data-ttu-id="64885-173">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-173">Parameter Name</span></span>|<span data-ttu-id="64885-174">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-174">Restriction Default</span></span>|<span data-ttu-id="64885-175">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-175">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-176">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-176">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-177">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-177">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-178">1</span><span class="sxs-lookup"><span data-stu-id="64885-178">1</span></span>|  
|<span data-ttu-id="64885-179">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-179">Owner</span></span>|@Owner|<span data-ttu-id="64885-180">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-180">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-181">2</span><span class="sxs-lookup"><span data-stu-id="64885-181">2</span></span>|  
|<span data-ttu-id="64885-182">Table</span><span class="sxs-lookup"><span data-stu-id="64885-182">Table</span></span>|@Table|<span data-ttu-id="64885-183">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-183">TABLE_NAME</span></span>|<span data-ttu-id="64885-184">3</span><span class="sxs-lookup"><span data-stu-id="64885-184">3</span></span>|  
|<span data-ttu-id="64885-185">Colonne</span><span class="sxs-lookup"><span data-stu-id="64885-185">Column</span></span>|@Column|<span data-ttu-id="64885-186">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-186">COLUMN_NAME</span></span>|<span data-ttu-id="64885-187">4</span><span class="sxs-lookup"><span data-stu-id="64885-187">4</span></span>|  
  
### <a name="structuredtypemembers"></a><span data-ttu-id="64885-188">StructuredTypeMembers</span><span class="sxs-lookup"><span data-stu-id="64885-188">StructuredTypeMembers</span></span>  
  
|<span data-ttu-id="64885-189">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-189">Restriction Name</span></span>|<span data-ttu-id="64885-190">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-190">Parameter Name</span></span>|<span data-ttu-id="64885-191">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-191">Restriction Default</span></span>|<span data-ttu-id="64885-192">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-192">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-193">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-193">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-194">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-194">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-195">1</span><span class="sxs-lookup"><span data-stu-id="64885-195">1</span></span>|  
|<span data-ttu-id="64885-196">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-196">Owner</span></span>|@Owner|<span data-ttu-id="64885-197">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-197">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-198">2</span><span class="sxs-lookup"><span data-stu-id="64885-198">2</span></span>|  
|<span data-ttu-id="64885-199">Table</span><span class="sxs-lookup"><span data-stu-id="64885-199">Table</span></span>|@Table|<span data-ttu-id="64885-200">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-200">TABLE_NAME</span></span>|<span data-ttu-id="64885-201">3</span><span class="sxs-lookup"><span data-stu-id="64885-201">3</span></span>|  
|<span data-ttu-id="64885-202">Colonne</span><span class="sxs-lookup"><span data-stu-id="64885-202">Column</span></span>|@Column|<span data-ttu-id="64885-203">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-203">COLUMN_NAME</span></span>|<span data-ttu-id="64885-204">4</span><span class="sxs-lookup"><span data-stu-id="64885-204">4</span></span>|  
  
### <a name="views"></a><span data-ttu-id="64885-205">Affichages</span><span class="sxs-lookup"><span data-stu-id="64885-205">Views</span></span>  
  
|<span data-ttu-id="64885-206">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-206">Restriction Name</span></span>|<span data-ttu-id="64885-207">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-207">Parameter Name</span></span>|<span data-ttu-id="64885-208">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-208">Restriction Default</span></span>|<span data-ttu-id="64885-209">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-209">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-210">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-210">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-211">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-211">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-212">1</span><span class="sxs-lookup"><span data-stu-id="64885-212">1</span></span>|  
|<span data-ttu-id="64885-213">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-213">Owner</span></span>|@Owner|<span data-ttu-id="64885-214">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-214">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-215">2</span><span class="sxs-lookup"><span data-stu-id="64885-215">2</span></span>|  
|<span data-ttu-id="64885-216">Table</span><span class="sxs-lookup"><span data-stu-id="64885-216">Table</span></span>|@Table|<span data-ttu-id="64885-217">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-217">TABLE_NAME</span></span>|<span data-ttu-id="64885-218">3</span><span class="sxs-lookup"><span data-stu-id="64885-218">3</span></span>|  
  
### <a name="viewcolumns"></a><span data-ttu-id="64885-219">ViewColumns</span><span class="sxs-lookup"><span data-stu-id="64885-219">ViewColumns</span></span>  
  
|<span data-ttu-id="64885-220">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-220">Restriction Name</span></span>|<span data-ttu-id="64885-221">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-221">Parameter Name</span></span>|<span data-ttu-id="64885-222">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-222">Restriction Default</span></span>|<span data-ttu-id="64885-223">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-223">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-224">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-224">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-225">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-225">VIEW_CATALOG</span></span>|<span data-ttu-id="64885-226">1</span><span class="sxs-lookup"><span data-stu-id="64885-226">1</span></span>|  
|<span data-ttu-id="64885-227">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-227">Owner</span></span>|@Owner|<span data-ttu-id="64885-228">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-228">VIEW_SCHEMA</span></span>|<span data-ttu-id="64885-229">2</span><span class="sxs-lookup"><span data-stu-id="64885-229">2</span></span>|  
|<span data-ttu-id="64885-230">Table</span><span class="sxs-lookup"><span data-stu-id="64885-230">Table</span></span>|@Table|<span data-ttu-id="64885-231">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-231">VIEW_NAME</span></span>|<span data-ttu-id="64885-232">3</span><span class="sxs-lookup"><span data-stu-id="64885-232">3</span></span>|  
|<span data-ttu-id="64885-233">Colonne</span><span class="sxs-lookup"><span data-stu-id="64885-233">Column</span></span>|@Column|<span data-ttu-id="64885-234">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-234">COLUMN_NAME</span></span>|<span data-ttu-id="64885-235">4</span><span class="sxs-lookup"><span data-stu-id="64885-235">4</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="64885-236">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="64885-236">ProcedureParameters</span></span>  
  
|<span data-ttu-id="64885-237">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-237">Restriction Name</span></span>|<span data-ttu-id="64885-238">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-238">Parameter Name</span></span>|<span data-ttu-id="64885-239">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-239">Restriction Default</span></span>|<span data-ttu-id="64885-240">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-240">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-241">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-241">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-242">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-242">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="64885-243">1</span><span class="sxs-lookup"><span data-stu-id="64885-243">1</span></span>|  
|<span data-ttu-id="64885-244">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-244">Owner</span></span>|@Owner|<span data-ttu-id="64885-245">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-245">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="64885-246">2</span><span class="sxs-lookup"><span data-stu-id="64885-246">2</span></span>|  
|<span data-ttu-id="64885-247">Nom</span><span class="sxs-lookup"><span data-stu-id="64885-247">Name</span></span>|@Name|<span data-ttu-id="64885-248">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-248">SPECIFIC_NAME</span></span>|<span data-ttu-id="64885-249">3</span><span class="sxs-lookup"><span data-stu-id="64885-249">3</span></span>|  
|<span data-ttu-id="64885-250">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-250">Parameter</span></span>|@Parameter|<span data-ttu-id="64885-251">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-251">PARAMETER_NAME</span></span>|<span data-ttu-id="64885-252">4</span><span class="sxs-lookup"><span data-stu-id="64885-252">4</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="64885-253">Procédures</span><span class="sxs-lookup"><span data-stu-id="64885-253">Procedures</span></span>  
  
|<span data-ttu-id="64885-254">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-254">Restriction Name</span></span>|<span data-ttu-id="64885-255">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-255">Parameter Name</span></span>|<span data-ttu-id="64885-256">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-256">Restriction Default</span></span>|<span data-ttu-id="64885-257">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-257">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-258">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-259">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-259">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="64885-260">1</span><span class="sxs-lookup"><span data-stu-id="64885-260">1</span></span>|  
|<span data-ttu-id="64885-261">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-261">Owner</span></span>|@Owner|<span data-ttu-id="64885-262">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-262">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="64885-263">2</span><span class="sxs-lookup"><span data-stu-id="64885-263">2</span></span>|  
|<span data-ttu-id="64885-264">Nom</span><span class="sxs-lookup"><span data-stu-id="64885-264">Name</span></span>|@Name|<span data-ttu-id="64885-265">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-265">SPECIFIC_NAME</span></span>|<span data-ttu-id="64885-266">3</span><span class="sxs-lookup"><span data-stu-id="64885-266">3</span></span>|  
|<span data-ttu-id="64885-267">Type</span><span class="sxs-lookup"><span data-stu-id="64885-267">Type</span></span>|@Type|<span data-ttu-id="64885-268">ROUTINE_TYPE</span><span class="sxs-lookup"><span data-stu-id="64885-268">ROUTINE_TYPE</span></span>|<span data-ttu-id="64885-269">4</span><span class="sxs-lookup"><span data-stu-id="64885-269">4</span></span>|  
  
### <a name="indexcolumns"></a><span data-ttu-id="64885-270">IndexColumns</span><span class="sxs-lookup"><span data-stu-id="64885-270">IndexColumns</span></span>  
  
|<span data-ttu-id="64885-271">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-271">Restriction Name</span></span>|<span data-ttu-id="64885-272">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-272">Parameter Name</span></span>|<span data-ttu-id="64885-273">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-273">Restriction Default</span></span>|<span data-ttu-id="64885-274">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-274">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-275">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-275">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-276">db_name()</span><span class="sxs-lookup"><span data-stu-id="64885-276">db_name()</span></span>|<span data-ttu-id="64885-277">1</span><span class="sxs-lookup"><span data-stu-id="64885-277">1</span></span>|  
|<span data-ttu-id="64885-278">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-278">Owner</span></span>|@Owner|<span data-ttu-id="64885-279">user_name()</span><span class="sxs-lookup"><span data-stu-id="64885-279">user_name()</span></span>|<span data-ttu-id="64885-280">2</span><span class="sxs-lookup"><span data-stu-id="64885-280">2</span></span>|  
|<span data-ttu-id="64885-281">Table</span><span class="sxs-lookup"><span data-stu-id="64885-281">Table</span></span>|@Table|<span data-ttu-id="64885-282">o.name</span><span class="sxs-lookup"><span data-stu-id="64885-282">o.name</span></span>|<span data-ttu-id="64885-283">3</span><span class="sxs-lookup"><span data-stu-id="64885-283">3</span></span>|  
|<span data-ttu-id="64885-284">ConstraintName</span><span class="sxs-lookup"><span data-stu-id="64885-284">ConstraintName</span></span>|@ConstraintName|<span data-ttu-id="64885-285">x.name</span><span class="sxs-lookup"><span data-stu-id="64885-285">x.name</span></span>|<span data-ttu-id="64885-286">4</span><span class="sxs-lookup"><span data-stu-id="64885-286">4</span></span>|  
|<span data-ttu-id="64885-287">Colonne</span><span class="sxs-lookup"><span data-stu-id="64885-287">Column</span></span>|@Column|<span data-ttu-id="64885-288">c.name</span><span class="sxs-lookup"><span data-stu-id="64885-288">c.name</span></span>|<span data-ttu-id="64885-289">5</span><span class="sxs-lookup"><span data-stu-id="64885-289">5</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="64885-290">Index</span><span class="sxs-lookup"><span data-stu-id="64885-290">Indexes</span></span>  
  
|<span data-ttu-id="64885-291">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-291">Restriction Name</span></span>|<span data-ttu-id="64885-292">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-292">Parameter Name</span></span>|<span data-ttu-id="64885-293">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-293">Restriction Default</span></span>|<span data-ttu-id="64885-294">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-294">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-295">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-295">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-296">db_name()</span><span class="sxs-lookup"><span data-stu-id="64885-296">db_name()</span></span>|<span data-ttu-id="64885-297">1</span><span class="sxs-lookup"><span data-stu-id="64885-297">1</span></span>|  
|<span data-ttu-id="64885-298">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-298">Owner</span></span>|@Owner|<span data-ttu-id="64885-299">user_name()</span><span class="sxs-lookup"><span data-stu-id="64885-299">user_name()</span></span>|<span data-ttu-id="64885-300">2</span><span class="sxs-lookup"><span data-stu-id="64885-300">2</span></span>|  
|<span data-ttu-id="64885-301">Table</span><span class="sxs-lookup"><span data-stu-id="64885-301">Table</span></span>|@Table|<span data-ttu-id="64885-302">o.name</span><span class="sxs-lookup"><span data-stu-id="64885-302">o.name</span></span>|<span data-ttu-id="64885-303">3</span><span class="sxs-lookup"><span data-stu-id="64885-303">3</span></span>|  
  
### <a name="userdefinedtypes"></a><span data-ttu-id="64885-304">UserDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="64885-304">UserDefinedTypes</span></span>  
  
|<span data-ttu-id="64885-305">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-305">Restriction Name</span></span>|<span data-ttu-id="64885-306">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-306">Parameter Name</span></span>|<span data-ttu-id="64885-307">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-307">Restriction Default</span></span>|<span data-ttu-id="64885-308">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-308">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-309">assembly_name</span><span class="sxs-lookup"><span data-stu-id="64885-309">assembly_name</span></span>|@AssemblyName|<span data-ttu-id="64885-310">assemblies.name</span><span class="sxs-lookup"><span data-stu-id="64885-310">assemblies.name</span></span>|<span data-ttu-id="64885-311">1</span><span class="sxs-lookup"><span data-stu-id="64885-311">1</span></span>|  
|<span data-ttu-id="64885-312">udt_name</span><span class="sxs-lookup"><span data-stu-id="64885-312">udt_name</span></span>|@UDTName|<span data-ttu-id="64885-313">types.assembly_class</span><span class="sxs-lookup"><span data-stu-id="64885-313">types.assembly_class</span></span>|<span data-ttu-id="64885-314">2</span><span class="sxs-lookup"><span data-stu-id="64885-314">2</span></span>|  
  
### <a name="foreignkeys"></a><span data-ttu-id="64885-315">ForeignKeys</span><span class="sxs-lookup"><span data-stu-id="64885-315">ForeignKeys</span></span>  
  
|<span data-ttu-id="64885-316">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-316">Restriction Name</span></span>|<span data-ttu-id="64885-317">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-317">Parameter Name</span></span>|<span data-ttu-id="64885-318">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-318">Restriction Default</span></span>|<span data-ttu-id="64885-319">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-319">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-320">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-320">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-321">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-321">CONSTRAINT_CATALOG</span></span>|<span data-ttu-id="64885-322">1</span><span class="sxs-lookup"><span data-stu-id="64885-322">1</span></span>|  
|<span data-ttu-id="64885-323">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-323">Owner</span></span>|@Owner|<span data-ttu-id="64885-324">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-324">CONSTRAINT_SCHEMA</span></span>|<span data-ttu-id="64885-325">2</span><span class="sxs-lookup"><span data-stu-id="64885-325">2</span></span>|  
|<span data-ttu-id="64885-326">Table</span><span class="sxs-lookup"><span data-stu-id="64885-326">Table</span></span>|@Table|<span data-ttu-id="64885-327">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-327">TABLE_NAME</span></span>|<span data-ttu-id="64885-328">3</span><span class="sxs-lookup"><span data-stu-id="64885-328">3</span></span>|  
|<span data-ttu-id="64885-329">Nom</span><span class="sxs-lookup"><span data-stu-id="64885-329">Name</span></span>|@Name|<span data-ttu-id="64885-330">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-330">CONSTRAINT_NAME</span></span>|<span data-ttu-id="64885-331">4</span><span class="sxs-lookup"><span data-stu-id="64885-331">4</span></span>|  
  
## <a name="sql-server-2008-schema-restrictions"></a><span data-ttu-id="64885-332">Restrictions de schéma SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="64885-332">SQL Server 2008 Schema Restrictions</span></span>  
 <span data-ttu-id="64885-333">Les tableaux suivants répertorient les restrictions pour les collections de schémas SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="64885-333">The following tables list the restrictions for SQL Server 2008 schema collections.</span></span> <span data-ttu-id="64885-334">Ces restrictions s'appliquent à partir de la version 3.5 SP1 de .NET Framework et SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="64885-334">These restrictions are valid beginning with version 3.5 SP1 of the .NET Framework and SQL Server 2008.</span></span> <span data-ttu-id="64885-335">Elles ne sont pas prises en charge dans les versions précédentes de .NET Framework et SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64885-335">They are not supported in earlier versions of the .NET Framework and SQL Server.</span></span>  
  
### <a name="columnsetcolumns"></a><span data-ttu-id="64885-336">ColumnSetColumns</span><span class="sxs-lookup"><span data-stu-id="64885-336">ColumnSetColumns</span></span>  
  
|<span data-ttu-id="64885-337">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-337">Restriction Name</span></span>|<span data-ttu-id="64885-338">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-338">Parameter Name</span></span>|<span data-ttu-id="64885-339">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-339">Restriction Default</span></span>|<span data-ttu-id="64885-340">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-340">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-341">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-341">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-342">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-342">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-343">1</span><span class="sxs-lookup"><span data-stu-id="64885-343">1</span></span>|  
|<span data-ttu-id="64885-344">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-344">Owner</span></span>|@Owner|<span data-ttu-id="64885-345">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-345">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-346">2</span><span class="sxs-lookup"><span data-stu-id="64885-346">2</span></span>|  
|<span data-ttu-id="64885-347">Table</span><span class="sxs-lookup"><span data-stu-id="64885-347">Table</span></span>|@Table|<span data-ttu-id="64885-348">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-348">TABLE_NAME</span></span>|<span data-ttu-id="64885-349">3</span><span class="sxs-lookup"><span data-stu-id="64885-349">3</span></span>|  
  
### <a name="allcolumns"></a><span data-ttu-id="64885-350">AllColumns</span><span class="sxs-lookup"><span data-stu-id="64885-350">AllColumns</span></span>  
  
|<span data-ttu-id="64885-351">Nom de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-351">Restriction Name</span></span>|<span data-ttu-id="64885-352">nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="64885-352">Parameter Name</span></span>|<span data-ttu-id="64885-353">Valeur par défaut de la restriction</span><span class="sxs-lookup"><span data-stu-id="64885-353">Restriction Default</span></span>|<span data-ttu-id="64885-354">Numéro de restriction</span><span class="sxs-lookup"><span data-stu-id="64885-354">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="64885-355">Catalogue</span><span class="sxs-lookup"><span data-stu-id="64885-355">Catalog</span></span>|@Catalog|<span data-ttu-id="64885-356">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="64885-356">TABLE_CATALOG</span></span>|<span data-ttu-id="64885-357">1</span><span class="sxs-lookup"><span data-stu-id="64885-357">1</span></span>|  
|<span data-ttu-id="64885-358">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="64885-358">Owner</span></span>|@Owner|<span data-ttu-id="64885-359">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="64885-359">TABLE_SCHEMA</span></span>|<span data-ttu-id="64885-360">2</span><span class="sxs-lookup"><span data-stu-id="64885-360">2</span></span>|  
|<span data-ttu-id="64885-361">Table</span><span class="sxs-lookup"><span data-stu-id="64885-361">Table</span></span>|@Table|<span data-ttu-id="64885-362">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-362">TABLE_NAME</span></span>|<span data-ttu-id="64885-363">3</span><span class="sxs-lookup"><span data-stu-id="64885-363">3</span></span>|  
|<span data-ttu-id="64885-364">Colonne</span><span class="sxs-lookup"><span data-stu-id="64885-364">Column</span></span>|@Column|<span data-ttu-id="64885-365">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="64885-365">COLUMN_NAME</span></span>|<span data-ttu-id="64885-366">4</span><span class="sxs-lookup"><span data-stu-id="64885-366">4</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="64885-367">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64885-367">See also</span></span>

- [<span data-ttu-id="64885-368">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="64885-368">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
