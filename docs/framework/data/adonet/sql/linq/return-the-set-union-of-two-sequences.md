---
title: Retourner l'union définie de deux séquences
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8b8bd3cb-86d4-4a3b-9906-61f68726dd1f
ms.openlocfilehash: 0d0d87e2fe14553d468384dfa2cfde1d3ee0d526
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61876926"
---
# <a name="return-the-set-union-of-two-sequences"></a><span data-ttu-id="8e4e2-102">Retourner l'union définie de deux séquences</span><span class="sxs-lookup"><span data-stu-id="8e4e2-102">Return the Set Union of Two Sequences</span></span>
<span data-ttu-id="8e4e2-103">Utilisez l'opérateur <xref:System.Linq.Queryable.Union%2A> pour retourner l'union définie de deux séquences.</span><span class="sxs-lookup"><span data-stu-id="8e4e2-103">Use the <xref:System.Linq.Queryable.Union%2A> operator to return the set union of two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8e4e2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8e4e2-104">Example</span></span>  
 <span data-ttu-id="8e4e2-105">Cet exemple utilise <xref:System.Linq.Queryable.Union%2A> pour retourner une séquence de tous les pays comportant des `Customers` ou des `Employees`.</span><span class="sxs-lookup"><span data-stu-id="8e4e2-105">This example uses <xref:System.Linq.Queryable.Union%2A> to return a sequence of all countries in which there are either `Customers` or `Employees`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#43](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#43)]
 [!code-vb[DLinqQueryExamples#43](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#43)]  
  
 <span data-ttu-id="8e4e2-106">Dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], le <xref:System.Linq.Queryable.Union%2A> opérateur est défini pour des multijeux comme la concaténation non ordonnée des multijeux (le résultat de la [ `UNION ALL` ](https://docs.microsoft.com/sql/t-sql/language-elements/set-operators-union-transact-sql?view=sql-server-2017) clause dans SQL).</span><span class="sxs-lookup"><span data-stu-id="8e4e2-106">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Union%2A> operator is defined for multisets as the unordered concatenation of the multisets (effectively the result of the [`UNION ALL`](https://docs.microsoft.com/sql/t-sql/language-elements/set-operators-union-transact-sql?view=sql-server-2017) clause in SQL).</span></span>

<span data-ttu-id="8e4e2-107">Pour plus d’informations et des exemples, consultez <xref:System.Linq.Queryable.Union%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="8e4e2-107">For more info and examples, see <xref:System.Linq.Queryable.Union%2A?displayProperty=nameWithType>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e4e2-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e4e2-108">See also</span></span>

- [<span data-ttu-id="8e4e2-109">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="8e4e2-109">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
- [<span data-ttu-id="8e4e2-110">Traduction des opérateurs de requête standard</span><span class="sxs-lookup"><span data-stu-id="8e4e2-110">Standard Query Operator Translation</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)
