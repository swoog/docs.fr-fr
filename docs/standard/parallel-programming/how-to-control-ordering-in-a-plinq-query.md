---
title: "Comment : contrôler l'ordre dans une requête PLINQ"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- PLINQ queries, how to control ordering
ms.assetid: c67eccc7-004d-4b2f-987e-919cbbd62ef7
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 3aef90c1a1160905662f93a83d6536f6d804b179
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-control-ordering-in-a-plinq-query"></a><span data-ttu-id="37103-102">Comment : contrôler l'ordre dans une requête PLINQ</span><span class="sxs-lookup"><span data-stu-id="37103-102">How to: Control Ordering in a PLINQ Query</span></span>
<span data-ttu-id="37103-103">Ces exemples montrent comment contrôler le classement d’une requête PLINQ à l’aide de la méthode d’extension <xref:System.Linq.ParallelEnumerable.AsOrdered%2A>.</span><span class="sxs-lookup"><span data-stu-id="37103-103">These examples show how to control the ordering in a PLINQ query by using the <xref:System.Linq.ParallelEnumerable.AsOrdered%2A> extension method.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="37103-104">Ces exemples, principalement destinés à illustrer l'utilisation, peuvent ou non s'exécuter plus rapidement que les requêtes LINQ to Objects séquentielle équivalentes.</span><span class="sxs-lookup"><span data-stu-id="37103-104">These examples are primarily intended to demonstrate usage, and may or may not run faster than the equivalent sequential LINQ to Objects queries.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37103-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="37103-105">Example</span></span>  
 <span data-ttu-id="37103-106">L’exemple suivant conserve l’ordre de la séquence source.</span><span class="sxs-lookup"><span data-stu-id="37103-106">The following example preserves the ordering of the source sequence.</span></span> <span data-ttu-id="37103-107">Cela est parfois nécessaire, par exemple si certains opérateurs de requête nécessitent une séquence source classée pour produire des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="37103-107">This is sometimes necessary; for example some query operators require an ordered source sequence to produce correct results.</span></span>  
  
 [!code-csharp[PLINQ#12](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#12)]
 [!code-vb[PLINQ#12](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="37103-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="37103-108">Example</span></span>  
 <span data-ttu-id="37103-109">L’exemple suivant montre certains opérateurs de requête dont la séquence source est probablement prévue pour être classée.</span><span class="sxs-lookup"><span data-stu-id="37103-109">The following example shows some query operators whose source sequence is probably expected to be ordered.</span></span> <span data-ttu-id="37103-110">Ces opérateurs fonctionneront sur les séquences non classées, mais ils peuvent produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="37103-110">These operators will work on unordered sequences, but they might produce unexpected results.</span></span>  
  
 [!code-csharp[PLINQ#14](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#14)]
 [!code-vb[PLINQ#14](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#14)]  
  
 <span data-ttu-id="37103-111">Pour exécuter cette méthode, collez-la dans la classe PLINQDataSample du projet [Exemple de données PLINQ](../../../docs/standard/parallel-programming/plinq-data-sample.md), puis appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="37103-111">To run this method, paste it into the PLINQDataSample class in the [PLINQ Data Sample](../../../docs/standard/parallel-programming/plinq-data-sample.md) project and press F5.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37103-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="37103-112">Example</span></span>  
 <span data-ttu-id="37103-113">L’exemple suivant montre comment conserver le classement pour la première partie d’une requête, comment supprimer le classement afin d’augmenter les performances d’une clause join, puis comment réappliquer le classement à la séquence de résultat finale.</span><span class="sxs-lookup"><span data-stu-id="37103-113">The following example shows how to preserve ordering for the first part of a query, then remove the ordering to increase the performance of a join clause, and then reapply ordering to the final result sequence.</span></span>  
  
 [!code-csharp[PLINQ#15](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqsamples.cs#15)]
 [!code-vb[PLINQ#15](../../../samples/snippets/visualbasic/VS_Snippets_Misc/plinq/vb/plinqsnippets1.vb#15)]  
  
 <span data-ttu-id="37103-114">Pour exécuter cette méthode, collez-la dans la classe PLINQDataSample du projet [Exemple de données PLINQ](../../../docs/standard/parallel-programming/plinq-data-sample.md), puis appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="37103-114">To run this method, paste it into the PLINQDataSample class in the [PLINQ Data Sample](../../../docs/standard/parallel-programming/plinq-data-sample.md) project and press F5.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37103-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37103-115">See Also</span></span>  
 <xref:System.Linq.ParallelEnumerable>  
 [<span data-ttu-id="37103-116">Parallel LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="37103-116">Parallel LINQ (PLINQ)</span></span>](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
