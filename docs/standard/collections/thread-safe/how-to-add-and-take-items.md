---
title: "Comment : ajouter et prendre des éléments individuellement dans un BlockingCollection"
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
- thread-safe collections, blocking dictionary
ms.assetid: 38f2f3d8-15e5-4bf4-9c83-2b5b6f22bad1
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c19e78ca05b339898a27a1e5f98412224586aae9
ms.sourcegitcommit: c3ebb11a66e85a465c9ba2c42592222630b7ff9e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2018
---
# <a name="how-to-add-and-take-items-individually-from-a-blockingcollection"></a><span data-ttu-id="8f02e-102">Comment : ajouter et prendre des éléments individuellement dans un BlockingCollection</span><span class="sxs-lookup"><span data-stu-id="8f02e-102">How to: Add and Take Items Individually from a BlockingCollection</span></span>
<span data-ttu-id="8f02e-103">Cet exemple montre comment ajouter et supprimer des éléments dans un <xref:System.Collections.Concurrent.BlockingCollection%601> de manière bloquante et non bloquante.</span><span class="sxs-lookup"><span data-stu-id="8f02e-103">This example shows how to add and remove items from a <xref:System.Collections.Concurrent.BlockingCollection%601> in both a blocking and a non-blocking manner.</span></span> <span data-ttu-id="8f02e-104">Pour plus d’informations sur <xref:System.Collections.Concurrent.BlockingCollection%601>, consultez [Vue d’ensemble de BlockingCollection](../../../../docs/standard/collections/thread-safe/blockingcollection-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8f02e-104">For more information on <xref:System.Collections.Concurrent.BlockingCollection%601>, see [BlockingCollection Overview](../../../../docs/standard/collections/thread-safe/blockingcollection-overview.md).</span></span>  
  
 <span data-ttu-id="8f02e-105">Pour obtenir un exemple de la marche à suivre pour énumérer un <xref:System.Collections.Concurrent.BlockingCollection%601> jusqu’à ce qu’il soit vide et qu’aucun autre élément ne soit ajouté, consultez [Guide pratique : utiliser la boucle ForEach pour supprimer les éléments d’un BlockingCollection](../../../../docs/standard/collections/thread-safe/how-to-use-foreach-to-remove.md).</span><span class="sxs-lookup"><span data-stu-id="8f02e-105">For an example of how to enumerate a <xref:System.Collections.Concurrent.BlockingCollection%601> until it is empty and no more elements will be added, see [How to: Use ForEach to Remove Items in a BlockingCollection](../../../../docs/standard/collections/thread-safe/how-to-use-foreach-to-remove.md).</span></span>
  
## <a name="example"></a><span data-ttu-id="8f02e-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f02e-106">Example</span></span>  
 <span data-ttu-id="8f02e-107">Ce premier exemple montre comment ajouter et prendre des éléments pour que les opérations soient bloquées si la collection est temporairement vide (lors de la prise) ou à la capacité maximale (lors de l’ajout), ou si un délai d’expiration spécifié s’est écoulé.</span><span class="sxs-lookup"><span data-stu-id="8f02e-107">This first example shows how to add and take items so that the operations will block if the collection is either temporarily empty (when taking) or at maximum capacity (when adding), or if a specified timeout period has elapsed.</span></span> <span data-ttu-id="8f02e-108">Notez que le blocage en cas de capacité maximale est activé uniquement quand le BlockingCollection a été créé avec une capacité maximale spécifiée dans le constructeur.</span><span class="sxs-lookup"><span data-stu-id="8f02e-108">Note that blocking on maximum capacity is only enabled when the BlockingCollection has been created with a maximum capacity specified in the constructor.</span></span>  
  
 [!code-csharp[CDS_BlockingCollection#01](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example01.cs#01)]
 [!code-vb[CDS_BlockingCollection#01](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/simpleblocking.vb#01)]  
  
## <a name="example"></a><span data-ttu-id="8f02e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f02e-109">Example</span></span>  
 <span data-ttu-id="8f02e-110">Ce deuxième exemple montre comment ajouter et prendre des éléments pour que les opérations ne soient pas bloquées.</span><span class="sxs-lookup"><span data-stu-id="8f02e-110">This second example shows how to add and take items so that the operations will not block.</span></span> <span data-ttu-id="8f02e-111">Si aucun élément n’est présent, si la capacité maximale sur une collection limitée a été atteinte ou si le délai d’expiration s’est écoulé, l’opération <xref:System.Collections.Concurrent.BlockingCollection%601.TryAdd%2A> ou <xref:System.Collections.Concurrent.BlockingCollection%601.TryTake%2A> retourne false.</span><span class="sxs-lookup"><span data-stu-id="8f02e-111">If no item is present, maximum capacity on a bounded collection has been reached, or the timeout period has elapsed, then the <xref:System.Collections.Concurrent.BlockingCollection%601.TryAdd%2A> or <xref:System.Collections.Concurrent.BlockingCollection%601.TryTake%2A> operation returns false.</span></span> <span data-ttu-id="8f02e-112">Cela permet au thread d’effectuer un autre travail utile pendant ce temps-là, puis de réessayer ultérieurement de récupérer un élément ou d’ajouter l’élément qui n’a pas pu être ajouté précédemment.</span><span class="sxs-lookup"><span data-stu-id="8f02e-112">This allows the thread to do some other useful work for a while and then try again later to either retrieve a new item, or try to add the same item that could not be added previously.</span></span> <span data-ttu-id="8f02e-113">Le programme montre aussi comment implémenter l’annulation lors de l’accès à un <xref:System.Collections.Concurrent.BlockingCollection%601>.</span><span class="sxs-lookup"><span data-stu-id="8f02e-113">The program also demonstrates how to implement cancellation when accessing a <xref:System.Collections.Concurrent.BlockingCollection%601>.</span></span>  
  
 [!code-csharp[CDS_BlockingCollection#02](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example02.cs#02)]
 [!code-vb[CDS_BlockingCollection#02](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/nonblockingbc.vb#02)]  
  
## <a name="see-also"></a><span data-ttu-id="8f02e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f02e-114">See Also</span></span>  
 <xref:System.Collections.Concurrent?displayProperty=nameWithType>  
 [<span data-ttu-id="8f02e-115">Vue d'ensemble de BlockingCollection</span><span class="sxs-lookup"><span data-stu-id="8f02e-115">BlockingCollection Overview</span></span>](../../../../docs/standard/collections/thread-safe/blockingcollection-overview.md)
