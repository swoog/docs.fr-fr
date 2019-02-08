---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Partitionnement (LINQ'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a582c53f-f203-44ae-a797-d7f169a4fbb5
ms.openlocfilehash: 05ca7defa3e070933d4c24f105fdb6fec423dc71
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904210"
---
# <a name="method-based-query-syntax-examples-partitioning-linq"></a><span data-ttu-id="71500-102">Exemples de syntaxe de requête fondée sur une méthode : Partitionnement (LINQ</span><span class="sxs-lookup"><span data-stu-id="71500-102">Method-Based Query Syntax Examples: Partitioning (LINQ</span></span>
<span data-ttu-id="71500-103">Les exemples de cette rubrique montrent comment utiliser les méthodes <xref:System.Linq.Enumerable.Skip%2A>, <xref:System.Linq.Enumerable.SkipWhile%2A>, <xref:System.Linq.Enumerable.Take%2A> et <xref:System.Linq.Enumerable.TakeWhile%2A> pour interroger un <xref:System.Data.DataSet> à l'aide de la syntaxe d'expression de requête.</span><span class="sxs-lookup"><span data-stu-id="71500-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Skip%2A>, <xref:System.Linq.Enumerable.SkipWhile%2A>, <xref:System.Linq.Enumerable.Take%2A>, and <xref:System.Linq.Enumerable.TakeWhile%2A> methods to query a <xref:System.Data.DataSet> using the query expression syntax.</span></span>  
  
 <span data-ttu-id="71500-104">Le `FillDataSet` méthode utilisé dans ces exemples est spécifiée dans [chargement des données dans un jeu de données](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="71500-104">The `FillDataSet` method used in these examples is specified in [Loading Data Into a DataSet](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md).</span></span>  
  
 <span data-ttu-id="71500-105">Les exemples de cette rubrique utilisent les tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="71500-105">The examples in this topic use the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="71500-106">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="71500-106">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 <span data-ttu-id="71500-107">Pour plus d'informations, voir [Procédure : Créer un projet LINQ to DataSet dans Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span><span class="sxs-lookup"><span data-stu-id="71500-107">For more information, see [How to: Create a LINQ to DataSet Project In Visual Studio](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md).</span></span>  
  
## <a name="skip"></a><span data-ttu-id="71500-108">Ignorer</span><span class="sxs-lookup"><span data-stu-id="71500-108">Skip</span></span>  
  
### <a name="example"></a><span data-ttu-id="71500-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-109">Example</span></span>  
 <span data-ttu-id="71500-110">Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Skip%2A> pour obtenir tous les contacts de la table `Contact`, à l'exception des cinq premiers.</span><span class="sxs-lookup"><span data-stu-id="71500-110">This example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first five contacts of the `Contact` table.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#SkipSimple](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#skipsimple)]
 [!code-vb[DP LINQ to DataSet Examples#SkipSimple](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#skipsimple)]  
  
### <a name="example"></a><span data-ttu-id="71500-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-111">Example</span></span>  
 <span data-ttu-id="71500-112">Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Skip%2A> pour obtenir toutes les adresses de Seattle, à l'exception des deux premières.</span><span class="sxs-lookup"><span data-stu-id="71500-112">This example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first two addresses in Seattle.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#SkipNested](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#skipnested)]
 [!code-vb[DP LINQ to DataSet Examples#SkipNested](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#skipnested)]  
  
## <a name="skipwhile"></a><span data-ttu-id="71500-113">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="71500-113">SkipWhile</span></span>  
  
### <a name="example"></a><span data-ttu-id="71500-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-114">Example</span></span>  
 <span data-ttu-id="71500-115">Cet exemple utilise les méthodes <xref:System.Linq.Enumerable.OrderBy%2A> et <xref:System.Linq.Enumerable.SkipWhile%2A> pour retourner des produits de la table `Product` dont le prix courant est supérieur à 300.</span><span class="sxs-lookup"><span data-stu-id="71500-115">This example uses <xref:System.Linq.Enumerable.OrderBy%2A> and <xref:System.Linq.Enumerable.SkipWhile%2A> methods to return products from the `Product` table with a list price greater than 300.00.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#SkipWhileSimple_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#skipwhilesimple_mq)]
 [!code-vb[DP LINQ to DataSet Examples#SkipWhileSimple_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#skipwhilesimple_mq)]  
  
## <a name="take"></a><span data-ttu-id="71500-116">Take</span><span class="sxs-lookup"><span data-stu-id="71500-116">Take</span></span>  
  
### <a name="example"></a><span data-ttu-id="71500-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-117">Example</span></span>  
 <span data-ttu-id="71500-118">Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Take%2A> pour obtenir uniquement les cinq premiers contacts de la table `Contact`.</span><span class="sxs-lookup"><span data-stu-id="71500-118">This example uses the <xref:System.Linq.Enumerable.Take%2A> method to get only the first five contacts from the `Contact` table.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#TakeSimple](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#takesimple)]
 [!code-vb[DP LINQ to DataSet Examples#TakeSimple](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#takesimple)]  
  
### <a name="example"></a><span data-ttu-id="71500-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-119">Example</span></span>  
 <span data-ttu-id="71500-120">Cet exemple utilise la méthode <xref:System.Linq.Enumerable.Take%2A> pour obtenir les trois premières adresses de Seattle.</span><span class="sxs-lookup"><span data-stu-id="71500-120">This example uses the <xref:System.Linq.Enumerable.Take%2A> method to get the first three addresses in Seattle.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#TakeNested](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#takenested)]
 [!code-vb[DP LINQ to DataSet Examples#TakeNested](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#takenested)]  
  
## <a name="takewhile"></a><span data-ttu-id="71500-121">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="71500-121">TakeWhile</span></span>  
  
### <a name="example"></a><span data-ttu-id="71500-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="71500-122">Example</span></span>  
 <span data-ttu-id="71500-123">Cet exemple utilise les méthodes <xref:System.Linq.Enumerable.OrderBy%2A> et <xref:System.Linq.Enumerable.TakeWhile%2A> pour retourner des produits de la table `Product` dont le prix courant est inférieur à 300.</span><span class="sxs-lookup"><span data-stu-id="71500-123">This example uses <xref:System.Linq.Enumerable.OrderBy%2A> and <xref:System.Linq.Enumerable.TakeWhile%2A> to return products from the `Product` table with a list price less than 300.00.</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#TakeWhileSimple_MQ](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#takewhilesimple_mq)]
 [!code-vb[DP LINQ to DataSet Examples#TakeWhileSimple_MQ](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#takewhilesimple_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="71500-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71500-124">See also</span></span>
- [<span data-ttu-id="71500-125">Chargement de données dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="71500-125">Loading Data Into a DataSet</span></span>](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)
- [<span data-ttu-id="71500-126">Exemples LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="71500-126">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
- [<span data-ttu-id="71500-127">Vue d’ensemble des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="71500-127">Standard Query Operators Overview (C#)</span></span>](../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="71500-128">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="71500-128">Standard Query Operators Overview (Visual Basic)</span></span>](../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
