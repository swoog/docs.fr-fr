---
title: 'Exemples de syntaxe d’expression de requête : Regroupement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2d83d7c0-b3be-4c92-a630-25cd1285de31
ms.openlocfilehash: 0a4aa57ba709852c30223598b9d1af146eaf6013
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211996"
---
# <a name="query-expression-syntax-examples-grouping"></a><span data-ttu-id="81c1c-102">Exemples de syntaxe d’expression de requête : Regroupement</span><span class="sxs-lookup"><span data-stu-id="81c1c-102">Query Expression Syntax Examples: Grouping</span></span>
<span data-ttu-id="81c1c-103">Les exemples de cette rubrique montrent comment utiliser le `GroupBy` méthode pour interroger le [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) à l’aide de la syntaxe d’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="81c1c-103">The examples in this topic demonstrate how to use the `GroupBy` method to query the [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) using query expression syntax.</span></span> <span data-ttu-id="81c1c-104">Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="81c1c-104">The AdventureWorks Sales model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="81c1c-105">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="81c1c-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="81c1c-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="81c1c-106">Example</span></span>  
 <span data-ttu-id="81c1c-107">L'exemple ci-dessous retourne des objets `Address` regroupés selon le code postal.</span><span class="sxs-lookup"><span data-stu-id="81c1c-107">The following example returns `Address` objects grouped by postal code.</span></span> <span data-ttu-id="81c1c-108">Les résultats sont projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="81c1c-108">The results are projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple3)]
 [!code-vb[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple3)]  
  
## <a name="example"></a><span data-ttu-id="81c1c-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="81c1c-109">Example</span></span>  
 <span data-ttu-id="81c1c-110">L'exemple ci-dessous retourne des objets `Contact` regroupés selon la première lettre du nom de famille des contacts.</span><span class="sxs-lookup"><span data-stu-id="81c1c-110">The following example returns `Contact` objects grouped by the first letter of the contact's last name.</span></span> <span data-ttu-id="81c1c-111">Les résultats sont également triés selon la première lettre du nom de famille et projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="81c1c-111">The results are also sorted by the first letter of last name and projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple2)]
 [!code-vb[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple2)]  
  
## <a name="example"></a><span data-ttu-id="81c1c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="81c1c-112">Example</span></span>  
 <span data-ttu-id="81c1c-113">L'exemple ci-dessous retourne des objets `SalesOrderHeader` regroupés par code client (Customer ID).</span><span class="sxs-lookup"><span data-stu-id="81c1c-113">The following example returns `SalesOrderHeader` objects grouped by customer ID.</span></span> <span data-ttu-id="81c1c-114">Le nombre de ventes réalisées pour chaque client est également retourné.</span><span class="sxs-lookup"><span data-stu-id="81c1c-114">The number of sales for each customer is also returned.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbycount)]
 [!code-vb[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbycount)]  
  
## <a name="see-also"></a><span data-ttu-id="81c1c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81c1c-115">See also</span></span>

- [<span data-ttu-id="81c1c-116">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="81c1c-116">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
