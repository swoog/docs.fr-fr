---
title: "Blocage de l'exécution d'applications en mettant fin à une opération asynchrone"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- blocks, asynchronous operations
- AsyncWaitHandle property
- asynchronous programming, blocking applications
- blocking application execution
ms.assetid: cc5e2834-a65b-4df8-b750-7bdb79997fee
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
dev_langs:
- csharp
- vb
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 3ec7bfe6fe2cef20a6d74030802113a47e8679e1
ms.sourcegitcommit: 957c696f25e39f923a827fc3ad5e8ab72768838c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2018
---
# <a name="blocking-application-execution-by-ending-an-async-operation"></a><span data-ttu-id="16edc-102">Blocage de l'exécution d'applications en mettant fin à une opération asynchrone</span><span class="sxs-lookup"><span data-stu-id="16edc-102">Blocking Application Execution by Ending an Async Operation</span></span>
<span data-ttu-id="16edc-103">Les applications qui ne peuvent pas continuer à effectuer d’autres tâches en attendant les résultats d’une opération asynchrone doivent se bloquer jusqu'à ce que cette opération se termine.</span><span class="sxs-lookup"><span data-stu-id="16edc-103">Applications that cannot continue to do other work while waiting for the results of an asynchronous operation must block until the operation completes.</span></span> <span data-ttu-id="16edc-104">Pour bloquer le thread principal de votre application en attendant la fin d’une opération asynchrone, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="16edc-104">Use one of the following options to block your application's main thread while waiting for an asynchronous operation to complete:</span></span>  
  
-   <span data-ttu-id="16edc-105">Appelez la méthode **End***NomOpération* de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="16edc-105">Call the asynchronous operations **End***OperationName* method.</span></span> <span data-ttu-id="16edc-106">Cette approche est illustrée dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="16edc-106">This approach is demonstrated in this topic.</span></span>  
  
-   <span data-ttu-id="16edc-107">Utilisez la propriété <xref:System.IAsyncResult.AsyncWaitHandle%2A> du <xref:System.IAsyncResult> retourné par la méthode **Begin***NomOpération* de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="16edc-107">Use the <xref:System.IAsyncResult.AsyncWaitHandle%2A> property of the <xref:System.IAsyncResult> returned by the asynchronous operation's **Begin***OperationName* method.</span></span> <span data-ttu-id="16edc-108">Vous trouverez un exemple illustrant cette approche sur la page [Bloquer l'exécution d'applications avec un AsyncWaitHandle](../../../docs/standard/asynchronous-programming-patterns/blocking-application-execution-using-an-asyncwaithandle.md).</span><span class="sxs-lookup"><span data-stu-id="16edc-108">For an example that demonstrates this approach, see [Blocking Application Execution Using an AsyncWaitHandle](../../../docs/standard/asynchronous-programming-patterns/blocking-application-execution-using-an-asyncwaithandle.md).</span></span>  
  
 <span data-ttu-id="16edc-109">Les applications qui utilisent la méthode **End***NomOpération* pour se bloquer jusqu'à la fin d’une opération asynchrone appellent généralement la méthode **Begin***NomOpération*, effectuent tout le travail réalisable sans les résultats de l’opération, puis appellent **End***NomOpération*.</span><span class="sxs-lookup"><span data-stu-id="16edc-109">Applications that use the **End***OperationName* method to block until an asynchronous operation is complete will typically call the **Begin***OperationName* method, perform any work that can be done without the results of the operation, and then call **End***OperationName*.</span></span>  
  
## <a name="example"></a><span data-ttu-id="16edc-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="16edc-110">Example</span></span>  
 <span data-ttu-id="16edc-111">L’exemple de code suivant montre comment utiliser des méthodes asynchrones dans la classe <xref:System.Net.Dns> afin de récupérer les informations DNS (Domain Name System) pour un ordinateur spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16edc-111">The following code example demonstrates using asynchronous methods in the <xref:System.Net.Dns> class to retrieve Domain Name System information for a user-specified computer.</span></span> <span data-ttu-id="16edc-112">Notez que `null` (`Nothing` en Visual Basic) est transmis aux paramètres <xref:System.Net.Dns.BeginGetHostByName%2A>`requestCallback` et `stateObject`, car ces arguments ne sont pas requis dans cette approche.</span><span class="sxs-lookup"><span data-stu-id="16edc-112">Note that `null` (`Nothing` in Visual Basic) is passed for the <xref:System.Net.Dns.BeginGetHostByName%2A>`requestCallback` and `stateObject` parameters because these arguments are not required when using this approach.</span></span>  
  
 [!code-csharp[AsyncDesignPattern#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AsyncDesignPattern/CS/Async_EndBlock.cs#1)]
 [!code-vb[AsyncDesignPattern#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AsyncDesignPattern/VB/Async_EndBlock.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="16edc-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16edc-113">See Also</span></span>  
 [<span data-ttu-id="16edc-114">Modèle asynchrone basé sur les événements (EAP)</span><span class="sxs-lookup"><span data-stu-id="16edc-114">Event-based Asynchronous Pattern (EAP)</span></span>](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md)  
 [<span data-ttu-id="16edc-115">Vue d’ensemble du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="16edc-115">Event-based Asynchronous Pattern Overview</span></span>](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
