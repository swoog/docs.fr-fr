---
title: Annulation de threads de façon coopérative
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- threads, cancellation
ms.assetid: d2d6d5fd-e263-4fa0-847b-2fc3e0d82337
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd32deb9c8719a12b76aaea8ec91a17471cf18f9
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44259858"
---
# <a name="canceling-threads-cooperatively"></a><span data-ttu-id="47f55-102">Annulation de threads de façon coopérative</span><span class="sxs-lookup"><span data-stu-id="47f55-102">Canceling threads cooperatively</span></span>

<span data-ttu-id="47f55-103">Avant .NET Framework 4, .NET Framework n’offrait aucune fonction intégrée permettant d’annuler, de manière coopérative, un thread après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="47f55-103">Prior to the .NET Framework 4, the .NET Framework provided no built-in way to cancel a thread cooperatively after it was started.</span></span> <span data-ttu-id="47f55-104">À compter de .NET Framework 4, vous pouvez utiliser un jeton <xref:System.Threading.CancellationToken?displayProperty=nameWithType> pour annuler des threads, tout comme vous pouvez les utiliser pour annuler des objets <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> ou des requêtes PLINQ.</span><span class="sxs-lookup"><span data-stu-id="47f55-104">However, starting with the .NET Framework 4, you can use a <xref:System.Threading.CancellationToken?displayProperty=nameWithType> to cancel threads, just as you can use them to cancel <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> objects or PLINQ queries.</span></span> <span data-ttu-id="47f55-105">Bien que la classe <xref:System.Threading.Thread?displayProperty=nameWithType> n’offre pas de prise en charge intégrée pour les jetons d’annulation, vous pouvez transmettre un jeton à une procédure de thread à l’aide du constructeur <xref:System.Threading.Thread> qui prend un délégué <xref:System.Threading.ParameterizedThreadStart>.</span><span class="sxs-lookup"><span data-stu-id="47f55-105">Although the <xref:System.Threading.Thread?displayProperty=nameWithType> class does not offer built-in support for cancellation tokens, you can pass a token to a thread procedure by using the <xref:System.Threading.Thread> constructor that takes a <xref:System.Threading.ParameterizedThreadStart> delegate.</span></span> <span data-ttu-id="47f55-106">L'exemple suivant illustre la procédure à suivre pour réaliser cette opération.</span><span class="sxs-lookup"><span data-stu-id="47f55-106">The following example demonstrates how to do this.</span></span>  
  
 [!code-csharp[Cancellation#14](../../../samples/snippets/csharp/VS_Snippets_Misc/cancellation/cs/CooperativeThreads.cs#14)]
 [!code-vb[Cancellation#14](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cancellation/vb/CooperativeThreads.vb#14)]  
  
## <a name="see-also"></a><span data-ttu-id="47f55-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47f55-107">See also</span></span>

- [<span data-ttu-id="47f55-108">Utilisation des threads et du threading</span><span class="sxs-lookup"><span data-stu-id="47f55-108">Using Threads and Threading</span></span>](using-threads-and-threading.md)
