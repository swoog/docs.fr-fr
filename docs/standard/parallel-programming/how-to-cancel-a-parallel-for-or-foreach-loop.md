---
title: 'Procédure : annuler une boucle Parallel.For ou ForEach'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- parallel foreach loop, how to cancel
- parallel for loops, how to cancel
ms.assetid: 9d19b591-ea95-4418-8ea7-b6266af9905b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7cdb6e059fb1c7001bbe4da60e2936b1ad40cc1d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618068"
---
# <a name="how-to-cancel-a-parallelfor-or-foreach-loop"></a><span data-ttu-id="eef47-102">Procédure : annuler une boucle Parallel.For ou ForEach</span><span class="sxs-lookup"><span data-stu-id="eef47-102">How to: Cancel a Parallel.For or ForEach Loop</span></span>
<span data-ttu-id="eef47-103">Les méthodes <xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType> et <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> prennent en charge l'annulation via l'utilisation de jetons d'annulation.</span><span class="sxs-lookup"><span data-stu-id="eef47-103">The <xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType> and <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> methods support cancellation through the use of cancellation tokens.</span></span> <span data-ttu-id="eef47-104">Pour plus d'informations sur l'annulation en général, consultez [Annulation](../../../docs/standard/threading/cancellation-in-managed-threads.md).</span><span class="sxs-lookup"><span data-stu-id="eef47-104">For more information about cancellation in general, see [Cancellation](../../../docs/standard/threading/cancellation-in-managed-threads.md).</span></span> <span data-ttu-id="eef47-105">Dans une boucle parallèle, vous fournissez <xref:System.Threading.CancellationToken> à la méthode dans le paramètre <xref:System.Threading.Tasks.ParallelOptions> et vous joignez l’appel parallèle dans un bloc try-catch.</span><span class="sxs-lookup"><span data-stu-id="eef47-105">In a parallel loop, you supply the <xref:System.Threading.CancellationToken> to the method in the <xref:System.Threading.Tasks.ParallelOptions> parameter and then enclose the parallel call in a try-catch block.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eef47-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="eef47-106">Example</span></span>  
 <span data-ttu-id="eef47-107">L'exemple suivant montre comment annuler un appel à <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="eef47-107">The following example shows how to cancel a call to <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="eef47-108">Vous pouvez appliquer la même approche à un appel <xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="eef47-108">You can apply the same approach to a <xref:System.Threading.Tasks.Parallel.For%2A?displayProperty=nameWithType> call.</span></span>  
  
 [!code-csharp[TPL_Parallel#29](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_parallel/cs/parallel_cancel.cs#29)]
 [!code-vb[TPL_Parallel#29](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_parallel/vb/cancelloop.vb#29)]  
  
 <span data-ttu-id="eef47-109">Si le jeton qui signale l’annulation est le même jeton que celui spécifié dans l’instance <xref:System.Threading.Tasks.ParallelOptions>, alors la boucle parallèle lève une seule exception <xref:System.OperationCanceledException> lors de l’annulation.</span><span class="sxs-lookup"><span data-stu-id="eef47-109">If the token that signals the cancellation is the same token that is specified in the <xref:System.Threading.Tasks.ParallelOptions> instance, then the parallel loop will throw a single <xref:System.OperationCanceledException> on cancellation.</span></span> <span data-ttu-id="eef47-110">Si un autre jeton provoque l’annulation, la boucle lève une exception <xref:System.AggregateException> avec une exception <xref:System.OperationCanceledException> comme InnerException.</span><span class="sxs-lookup"><span data-stu-id="eef47-110">If some other token causes cancellation, the loop will throw an <xref:System.AggregateException> with an <xref:System.OperationCanceledException> as an InnerException.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eef47-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eef47-111">See also</span></span>

- [<span data-ttu-id="eef47-112">Parallélisme de données</span><span class="sxs-lookup"><span data-stu-id="eef47-112">Data Parallelism</span></span>](../../../docs/standard/parallel-programming/data-parallelism-task-parallel-library.md)
- [<span data-ttu-id="eef47-113">Expressions lambda en PLINQ et dans la bibliothèque parallèle de tâches</span><span class="sxs-lookup"><span data-stu-id="eef47-113">Lambda Expressions in PLINQ and TPL</span></span>](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
