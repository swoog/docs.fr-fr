---
title: Retourner le premier élément d'une séquence
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ccdc3777-b2c2-44e3-a627-abef8d79a555
ms.openlocfilehash: fd228b2d7534feca3cff49586ac0d43fbf9bcb1f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361346"
---
# <a name="return-the-first-element-in-a-sequence"></a><span data-ttu-id="3cfc3-102">Retourner le premier élément d'une séquence</span><span class="sxs-lookup"><span data-stu-id="3cfc3-102">Return the First Element in a Sequence</span></span>
<span data-ttu-id="3cfc3-103">Utilisez l'opérateur <xref:System.Linq.Enumerable.First%2A> pour retourner le premier élément d'une séquence.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-103">Use the <xref:System.Linq.Enumerable.First%2A> operator to return the first element in a sequence.</span></span> <span data-ttu-id="3cfc3-104">Les requêtes qui utilisent <xref:System.Linq.Enumerable.First%2A> sont exécutées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-104">Queries that use <xref:System.Linq.Enumerable.First%2A> are executed immediately.</span></span>  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="3cfc3-105"> ne prend pas en charge l'opérateur <xref:System.Linq.Enumerable.Last%2A>.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-105"> does not support the <xref:System.Linq.Enumerable.Last%2A> operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3cfc3-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="3cfc3-106">Example</span></span>  
 <span data-ttu-id="3cfc3-107">Le code suivant recherche le premier `Shipper` dans une table :</span><span class="sxs-lookup"><span data-stu-id="3cfc3-107">The following code finds the first `Shipper` in a table:</span></span>  
  
 <span data-ttu-id="3cfc3-108">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="3cfc3-108">If you run this query against the Northwind sample database, the results are</span></span>  
  
 <span data-ttu-id="3cfc3-109">`ID = 1, Company = Speedy Express`.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-109">`ID = 1, Company = Speedy Express`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#14](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#14)]
 [!code-vb[DLinqQueryExamples#14](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="3cfc3-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="3cfc3-110">Example</span></span>  
 <span data-ttu-id="3cfc3-111">Le code suivant recherche le seul `Customer` qui a BONAP comme `CustomerID`.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-111">The following code finds the single `Customer` that has the `CustomerID` BONAP.</span></span>  
  
 <span data-ttu-id="3cfc3-112">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez `ID = BONAP, Contact = Laurence Lebihan`.</span><span class="sxs-lookup"><span data-stu-id="3cfc3-112">If you run this query against the Northwind sample database, the results are `ID = BONAP, Contact = Laurence Lebihan`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#15](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#15)]
 [!code-vb[DLinqQueryExamples#15](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="3cfc3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cfc3-113">See Also</span></span>  
 [<span data-ttu-id="3cfc3-114">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="3cfc3-114">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)  
 [<span data-ttu-id="3cfc3-115">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="3cfc3-115">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
