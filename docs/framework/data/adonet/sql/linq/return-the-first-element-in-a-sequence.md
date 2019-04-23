---
title: Retourner le premier élément d'une séquence
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ccdc3777-b2c2-44e3-a627-abef8d79a555
ms.openlocfilehash: dca917b3c12b0f9923cc9ea34a2568c412a09831
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59081819"
---
# <a name="return-the-first-element-in-a-sequence"></a><span data-ttu-id="4c8b9-102">Retourner le premier élément d'une séquence</span><span class="sxs-lookup"><span data-stu-id="4c8b9-102">Return the First Element in a Sequence</span></span>
<span data-ttu-id="4c8b9-103">Utilisez l'opérateur <xref:System.Linq.Enumerable.First%2A> pour retourner le premier élément d'une séquence.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-103">Use the <xref:System.Linq.Enumerable.First%2A> operator to return the first element in a sequence.</span></span> <span data-ttu-id="4c8b9-104">Les requêtes qui utilisent <xref:System.Linq.Enumerable.First%2A> sont exécutées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-104">Queries that use <xref:System.Linq.Enumerable.First%2A> are executed immediately.</span></span>  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="4c8b9-105">ne prend pas en charge l'opérateur <xref:System.Linq.Enumerable.Last%2A>.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-105">does not support the <xref:System.Linq.Enumerable.Last%2A> operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c8b9-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c8b9-106">Example</span></span>  
 <span data-ttu-id="4c8b9-107">Le code suivant recherche le premier `Shipper` dans une table :</span><span class="sxs-lookup"><span data-stu-id="4c8b9-107">The following code finds the first `Shipper` in a table:</span></span>  
  
 <span data-ttu-id="4c8b9-108">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="4c8b9-108">If you run this query against the Northwind sample database, the results are</span></span>  
  
 <span data-ttu-id="4c8b9-109">`ID = 1, Company = Speedy Express`.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-109">`ID = 1, Company = Speedy Express`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#14](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#14)]
 [!code-vb[DLinqQueryExamples#14](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="4c8b9-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c8b9-110">Example</span></span>  
 <span data-ttu-id="4c8b9-111">Le code suivant recherche le seul `Customer` qui a BONAP comme `CustomerID`.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-111">The following code finds the single `Customer` that has the `CustomerID` BONAP.</span></span>  
  
 <span data-ttu-id="4c8b9-112">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez `ID = BONAP, Contact = Laurence Lebihan`.</span><span class="sxs-lookup"><span data-stu-id="4c8b9-112">If you run this query against the Northwind sample database, the results are `ID = BONAP, Contact = Laurence Lebihan`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#15](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#15)]
 [!code-vb[DLinqQueryExamples#15](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="4c8b9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c8b9-113">See also</span></span>

- [<span data-ttu-id="4c8b9-114">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="4c8b9-114">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
- [<span data-ttu-id="4c8b9-115">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="4c8b9-115">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
