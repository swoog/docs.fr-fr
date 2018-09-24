---
title: 'Comment : exposer des modèles EAP à l’aide d’une tâche'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to wrap EAP patterns
ms.assetid: f11ed467-af2f-4504-8a2e-299a6c36d44e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a4287879bd95f7bc1e1dc99f74fa0d7cc0fe737f
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46004258"
---
# <a name="how-to-wrap-eap-patterns-in-a-task"></a><span data-ttu-id="100da-102">Comment : exposer des modèles EAP à l’aide d’une tâche</span><span class="sxs-lookup"><span data-stu-id="100da-102">How to: Wrap EAP Patterns in a Task</span></span>
<span data-ttu-id="100da-103">L’exemple suivant montre comment exposer une séquence arbitraire d’opérations EAP (modèle asynchrone basé sur des événements) comme une seule tâche à l’aide d’un <xref:System.Threading.Tasks.TaskCompletionSource%601>.</span><span class="sxs-lookup"><span data-stu-id="100da-103">The following example shows how to expose an arbitrary sequence of Event-Based Asynchronous Pattern (EAP) operations as one task by using a <xref:System.Threading.Tasks.TaskCompletionSource%601>.</span></span> <span data-ttu-id="100da-104">L’exemple montre également comment utiliser un <xref:System.Threading.CancellationToken> pour appeler les méthodes d’annulation intégrées sur les objets <xref:System.Net.WebClient>.</span><span class="sxs-lookup"><span data-stu-id="100da-104">The example also shows how to use a <xref:System.Threading.CancellationToken> to invoke the built-in cancellation methods on the <xref:System.Net.WebClient> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="100da-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="100da-105">Example</span></span>  
 [!code-csharp[FromAsync#08](../../../samples/snippets/csharp/VS_Snippets_Misc/fromasync/cs/fromasync.cs#08)]
 [!code-vb[FromAsync#08](../../../samples/snippets/visualbasic/VS_Snippets_Misc/fromasync/vb/module1.vb#08)]  
  
## <a name="see-also"></a><span data-ttu-id="100da-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="100da-106">See also</span></span>

- [<span data-ttu-id="100da-107">Bibliothèque parallèle de tâches (TPL) et programmation asynchrone .NET Framework</span><span class="sxs-lookup"><span data-stu-id="100da-107">TPL and Traditional .NET Framework Asynchronous Programming</span></span>](../../../docs/standard/parallel-programming/tpl-and-traditional-async-programming.md)
