---
title: 'Comment : convertir un type en IEnumerable générique'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 64774fb5-7447-4296-ad3b-8a94346f99a1
ms.openlocfilehash: d75c9b9123b52b3e241bea1bbd1d302c406715e8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59190377"
---
# <a name="convert-a-type-to-a-generic-ienumerable"></a><span data-ttu-id="29346-102">Comment : convertir un type en IEnumerable générique</span><span class="sxs-lookup"><span data-stu-id="29346-102">Convert a Type to a Generic IEnumerable</span></span>
<span data-ttu-id="29346-103">Utilisez <xref:System.Linq.Enumerable.AsEnumerable%2A> pour retourner l'argument typé comme un `IEnumerable` générique.</span><span class="sxs-lookup"><span data-stu-id="29346-103">Use <xref:System.Linq.Enumerable.AsEnumerable%2A> to return the argument typed as a generic `IEnumerable`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29346-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="29346-104">Example</span></span>  
 <span data-ttu-id="29346-105">Dans cet exemple, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] (à l'aide du `Query` générique par défaut) tente de convertir la requête en SQL et de l'exécuter sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="29346-105">In this example, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] (using the default generic `Query`) would try to convert the query to SQL and execute it on the server.</span></span> <span data-ttu-id="29346-106">Toutefois, la clause `where` fait référence à une méthode côté client définie par l'utilisateur (`isValidProduct`) qui ne peut pas être convertie en SQL.</span><span class="sxs-lookup"><span data-stu-id="29346-106">But the `where` clause references a user-defined client-side method (`isValidProduct`), which cannot be converted to SQL.</span></span>  
  
 <span data-ttu-id="29346-107">La solution consiste à spécifier l'implémentation <xref:System.Collections.Generic.IEnumerable%601> générique côté client de `where` pour remplacer le <xref:System.Linq.IQueryable%601> générique.</span><span class="sxs-lookup"><span data-stu-id="29346-107">The solution is to specify the client-side generic <xref:System.Collections.Generic.IEnumerable%601> implementation of `where` to replace the generic <xref:System.Linq.IQueryable%601>.</span></span> <span data-ttu-id="29346-108">Vous pouvez pour cela appeler l'opérateur <xref:System.Linq.Enumerable.AsEnumerable%2A>.</span><span class="sxs-lookup"><span data-stu-id="29346-108">You do this by invoking the <xref:System.Linq.Enumerable.AsEnumerable%2A> operator.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#46](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#46)]
 [!code-vb[DLinqQueryExamples#46](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#46)]  
  
## <a name="see-also"></a><span data-ttu-id="29346-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29346-109">See also</span></span>

- [<span data-ttu-id="29346-110">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="29346-110">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
