---
title: 'Comment : combiner des requêtes LINQ parallèles et séquentielles'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- parallel queries, combine parallel and sequential
ms.assetid: 1167cfe6-c8aa-4096-94ba-c66c3a4edf4c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fd67d5f0cb5af33dc2b79f86148557a0dca6ec4
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45998927"
---
# <a name="how-to-combine-parallel-and-sequential-linq-queries"></a><span data-ttu-id="d5bc7-102">Comment : combiner des requêtes LINQ parallèles et séquentielles</span><span class="sxs-lookup"><span data-stu-id="d5bc7-102">How to: Combine Parallel and Sequential LINQ Queries</span></span>
<span data-ttu-id="d5bc7-103">Cet exemple montre comment utiliser la méthode <xref:System.Linq.ParallelEnumerable.AsSequential%2A> pour indiquer à PLINQ de traiter de manière séquentielle tous les opérateurs suivants dans la requête.</span><span class="sxs-lookup"><span data-stu-id="d5bc7-103">This example shows how to use the <xref:System.Linq.ParallelEnumerable.AsSequential%2A> method to instruct PLINQ to process all subsequent operators in the query sequentially.</span></span> <span data-ttu-id="d5bc7-104">Bien que le traitement séquentiel soit généralement plus lent que le traitement en parallèle, il est parfois nécessaire pour produire des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="d5bc7-104">Although sequential processing is generally slower than parallel, sometimes it is necessary to produce correct results.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="d5bc7-105">Cet exemple, destiné à illustrer l'utilisation, peut ne pas s'exécuter plus rapidement que la requête LINQ to Objects séquentielle équivalente.</span><span class="sxs-lookup"><span data-stu-id="d5bc7-105">This example is intended to demonstrate usage, and might not run faster than the equivalent sequential LINQ to Objects query.</span></span> <span data-ttu-id="d5bc7-106">Pour plus d’informations sur l’accélération, consultez [Fonctionnement de l’accélération dans PLINQ](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md).</span><span class="sxs-lookup"><span data-stu-id="d5bc7-106">For more information about speedup, see [Understanding Speedup in PLINQ](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d5bc7-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="d5bc7-107">Example</span></span>  
 <span data-ttu-id="d5bc7-108">L’exemple suivant montre un scénario dans lequel <xref:System.Linq.ParallelEnumerable.AsSequential%2A> est obligatoire, pour conserver le classement qui a été établi dans une clause précédente de la requête.</span><span class="sxs-lookup"><span data-stu-id="d5bc7-108">The following example shows one scenario in which <xref:System.Linq.ParallelEnumerable.AsSequential%2A> is required, namely to preserve the ordering that was established in a previous clause of the query.</span></span>  
  
 [!code-csharp[PLINQ#24](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#24)]
 [!code-vb[PLINQ#24](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#24)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d5bc7-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="d5bc7-109">Compiling the Code</span></span>  
 <span data-ttu-id="d5bc7-110">Pour compiler et exécuter ce code, collez-le dans le projet [PLINQ Data Sample](../../../docs/standard/parallel-programming/plinq-data-sample.md), ajoutez une ligne pour appeler la méthode à partir de `Main` et appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="d5bc7-110">To compile and run this code, paste it into the [PLINQ Data Sample](../../../docs/standard/parallel-programming/plinq-data-sample.md) project, add a line to call the method from `Main`, and press F5.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5bc7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5bc7-111">See also</span></span>

- [<span data-ttu-id="d5bc7-112">Parallel LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="d5bc7-112">Parallel LINQ (PLINQ)</span></span>](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
