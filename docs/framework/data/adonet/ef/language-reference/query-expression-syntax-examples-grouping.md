---
title: "Exemples de syntaxe d'expression de requête : regroupement"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2d83d7c0-b3be-4c92-a630-25cd1285de31
ms.openlocfilehash: 519f9073954e8f7710c9e73b61f40b4fcfefd25b
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44129363"
---
# <a name="query-expression-syntax-examples-grouping"></a><span data-ttu-id="ba631-102">Exemples de syntaxe d'expression de requête : regroupement</span><span class="sxs-lookup"><span data-stu-id="ba631-102">Query Expression Syntax Examples: Grouping</span></span>
<span data-ttu-id="ba631-103">Les exemples de cette rubrique montrent comment utiliser le `GroupBy` méthode pour interroger le [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) à l’aide de la syntaxe d’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="ba631-103">The examples in this topic demonstrate how to use the `GroupBy` method to query the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) using query expression syntax.</span></span> <span data-ttu-id="ba631-104">Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="ba631-104">The AdventureWorks Sales model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="ba631-105">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="ba631-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="ba631-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba631-106">Example</span></span>  
 <span data-ttu-id="ba631-107">L'exemple ci-dessous retourne des objets `Address` regroupés selon le code postal.</span><span class="sxs-lookup"><span data-stu-id="ba631-107">The following example returns `Address` objects grouped by postal code.</span></span> <span data-ttu-id="ba631-108">Les résultats sont projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="ba631-108">The results are projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple3)]
 [!code-vb[DP L2E Examples#GroupBySimple3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple3)]  
  
## <a name="example"></a><span data-ttu-id="ba631-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba631-109">Example</span></span>  
 <span data-ttu-id="ba631-110">L'exemple ci-dessous retourne des objets `Contact` regroupés selon la première lettre du nom de famille des contacts.</span><span class="sxs-lookup"><span data-stu-id="ba631-110">The following example returns `Contact` objects grouped by the first letter of the contact's last name.</span></span> <span data-ttu-id="ba631-111">Les résultats sont également triés selon la première lettre du nom de famille et projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="ba631-111">The results are also sorted by the first letter of last name and projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple2)]
 [!code-vb[DP L2E Examples#GroupBySimple2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple2)]  
  
## <a name="example"></a><span data-ttu-id="ba631-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba631-112">Example</span></span>  
 <span data-ttu-id="ba631-113">L'exemple ci-dessous retourne des objets `SalesOrderHeader` regroupés par code client (Customer ID).</span><span class="sxs-lookup"><span data-stu-id="ba631-113">The following example returns `SalesOrderHeader` objects grouped by customer ID.</span></span> <span data-ttu-id="ba631-114">Le nombre de ventes réalisées pour chaque client est également retourné.</span><span class="sxs-lookup"><span data-stu-id="ba631-114">The number of sales for each customer is also returned.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbycount)]
 [!code-vb[DP L2E Examples#GroupByCount](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbycount)]  
  
## <a name="see-also"></a><span data-ttu-id="ba631-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba631-115">See Also</span></span>  
 [<span data-ttu-id="ba631-116">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="ba631-116">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
