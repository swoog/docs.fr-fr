---
title: Retourner l'union définie de deux séquences
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8b8bd3cb-86d4-4a3b-9906-61f68726dd1f
ms.openlocfilehash: 5aa05384cba826f9cdd7a948a31b2860eaad7f18
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358075"
---
# <a name="return-the-set-union-of-two-sequences"></a><span data-ttu-id="31499-102">Retourner l'union définie de deux séquences</span><span class="sxs-lookup"><span data-stu-id="31499-102">Return the Set Union of Two Sequences</span></span>
<span data-ttu-id="31499-103">Utilisez l'opérateur <xref:System.Linq.Queryable.Union%2A> pour retourner l'union définie de deux séquences.</span><span class="sxs-lookup"><span data-stu-id="31499-103">Use the <xref:System.Linq.Queryable.Union%2A> operator to return the set union of two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="31499-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="31499-104">Example</span></span>  
 <span data-ttu-id="31499-105">Cet exemple utilise <xref:System.Linq.Queryable.Union%2A> pour retourner une séquence de tous les pays comportant des `Customers` ou des `Employees`.</span><span class="sxs-lookup"><span data-stu-id="31499-105">This example uses <xref:System.Linq.Queryable.Union%2A> to return a sequence of all countries in which there are either `Customers` or `Employees`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#43](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#43)]
 [!code-vb[DLinqQueryExamples#43](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#43)]  
  
 <span data-ttu-id="31499-106">Dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], le <xref:System.Linq.Queryable.Union%2A> opérateur est défini pour les multijeux comme la concaténation non ordonnée des multijeux (le résultat de la `UNION ALL` clause dans SQL).</span><span class="sxs-lookup"><span data-stu-id="31499-106">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Union%2A> operator is defined for multisets as the unordered concatenation of the multisets (effectively the result of the `UNION ALL` clause in SQL).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31499-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31499-107">See Also</span></span>  
 [<span data-ttu-id="31499-108">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="31499-108">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)  
 [<span data-ttu-id="31499-109">Traduction des opérateurs de requête standard</span><span class="sxs-lookup"><span data-stu-id="31499-109">Standard Query Operator Translation</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)
