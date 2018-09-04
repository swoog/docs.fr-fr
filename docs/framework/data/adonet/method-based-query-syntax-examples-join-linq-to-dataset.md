---
title: 'Exemples de syntaxe de requête fondée sur une méthode : jointure (LINQ to DataSet)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4fd5ed2c-b03a-4054-a3ed-3ddb380d7d9d
ms.openlocfilehash: 6ec65cad0070bdbd1d510bcc822f3b71f9cf69dc
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43560472"
---
# <a name="method-based-query-syntax-examples-join-linq-to-dataset"></a><span data-ttu-id="77610-102">Exemples de syntaxe de requête fondée sur une méthode : jointure (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="77610-102">Method-Based Query Syntax Examples: Join (LINQ to DataSet)</span></span>
<span data-ttu-id="77610-103">La jointure est une opération importante dans les requêtes qui ciblent des sources de données qui n'ont pas de relations explorables les unes avec les autres, comme les tables de base de données relationnelles.</span><span class="sxs-lookup"><span data-stu-id="77610-103">Joining is an important operation in queries that target data sources that have no navigable relationships to each other, such as relational database tables.</span></span> <span data-ttu-id="77610-104">Une jointure de deux sources de données est l'association d'objets dans une source de données avec des objets qui partagent un attribut commun dans l'autre source de données.</span><span class="sxs-lookup"><span data-stu-id="77610-104">A join of two data sources is the association of objects in one data source with objects that share a common attribute in the other data source.</span></span> <span data-ttu-id="77610-105">Pour plus d’informations, consultez [vue d’ensemble des opérateurs de requête Standard](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2).</span><span class="sxs-lookup"><span data-stu-id="77610-105">For more information, see [Standard Query Operators Overview](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2).</span></span>  
  
 <span data-ttu-id="77610-106">Les exemples de cette rubrique montrent comment utiliser la méthode <xref:System.Linq.Enumerable.Join%2A> pour interroger un <xref:System.Data.DataSet> à l'aide de la syntaxe d'interrogation de méthode.</span><span class="sxs-lookup"><span data-stu-id="77610-106">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Join%2A> method to query a <xref:System.Data.DataSet> using the method query syntax.</span></span>  
  
 <span data-ttu-id="77610-107">Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="77610-107">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="77610-108">Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="77610-108">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="77610-109">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="77610-109">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="77610-110">Pour plus d’informations, consultez [Comment : créer un LINQ to DataSet Project dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span><span class="sxs-lookup"><span data-stu-id="77610-110">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="join"></a><span data-ttu-id="77610-111">Join</span><span class="sxs-lookup"><span data-stu-id="77610-111">Join</span></span>  
  
### <a name="example"></a><span data-ttu-id="77610-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="77610-112">Example</span></span>  
 <span data-ttu-id="77610-113">Cet exemple effectue une jointure sur les tables `Contact` et `SalesOrderHeader`.</span><span class="sxs-lookup"><span data-stu-id="77610-113">This example performs a join over the `Contact` and `SalesOrderHeader` tables.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#JoinSimple_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#joinsimple_mq)]
 [!code-vb[DP LINQ to DataSet Examples#JoinSimple_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#joinsimple_mq)]  
  
### <a name="example"></a><span data-ttu-id="77610-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="77610-114">Example</span></span>  
 <span data-ttu-id="77610-115">Cet exemple effectue une jointure sur les tables `Contact` et `SalesOrderHeader`, en regroupant les résultats par ID de contact.</span><span class="sxs-lookup"><span data-stu-id="77610-115">This example performs a join over the `Contact` and `SalesOrderHeader` tables, grouping the results by contact ID.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#JoinWithGroupedResults_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#joinwithgroupedresults_mq)]
 [!code-vb[DP LINQ to DataSet Examples#JoinWithGroupedResults_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#joinwithgroupedresults_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="77610-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77610-116">See Also</span></span>  
 [<span data-ttu-id="77610-117">Chargement de données dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="77610-117">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)  
 [<span data-ttu-id="77610-118">Exemples LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="77610-118">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)  
 [<span data-ttu-id="77610-119">Vue d’ensemble des opérateurs de requête standard</span><span class="sxs-lookup"><span data-stu-id="77610-119">Standard Query Operators Overview</span></span>](https://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2)  
 [<span data-ttu-id="77610-120">Exemples de jointure</span><span class="sxs-lookup"><span data-stu-id="77610-120">Join Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=187357)  
 [<span data-ttu-id="77610-121">Exemples de DataSet</span><span class="sxs-lookup"><span data-stu-id="77610-121">Dataset Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=187358)
