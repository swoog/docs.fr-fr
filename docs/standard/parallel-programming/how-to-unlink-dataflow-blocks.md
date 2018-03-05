---
title: "Comment : dissocier des blocs de flux de données"
ms.date: 03/30/2017
ms.prod: .net
ms.technology: dotnet-standard
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dataflow blocks, unlinking in TPL
- Task Parallel Library, dataflows
- TPL dataflow library, unlinking dataflow blocks
ms.assetid: 40f0208d-4618-47f7-85cf-4913d07d2d7d
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: db3c0d3a6d94e2e9eb65046267f14feff0c056cb
ms.sourcegitcommit: 6a9030eb5bd0f00e1d144f81958adb195cfb1f6f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/10/2018
---
# <a name="how-to-unlink-dataflow-blocks"></a><span data-ttu-id="7f48e-102">Comment : dissocier des blocs de flux de données</span><span class="sxs-lookup"><span data-stu-id="7f48e-102">How to: Unlink Dataflow Blocks</span></span>
<span data-ttu-id="7f48e-103">Ce document explique comment dissocier un bloc de flux de données cible de sa source.</span><span class="sxs-lookup"><span data-stu-id="7f48e-103">This document describes how to unlink a target dataflow block from its source.</span></span>

[!INCLUDE [tpl-install-instructions](../../../includes/tpl-install-instructions.md)]

## <a name="example"></a><span data-ttu-id="7f48e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f48e-104">Example</span></span>  
 <span data-ttu-id="7f48e-105">L’exemple suivant crée trois objets <xref:System.Threading.Tasks.Dataflow.TransformBlock%602>, dont chacun appelle la méthode `TrySolution` pour calculer une valeur.</span><span class="sxs-lookup"><span data-stu-id="7f48e-105">The following example creates three <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> objects, each of which calls the `TrySolution` method to compute a value.</span></span> <span data-ttu-id="7f48e-106">Cet exemple n’a besoin que du résultat du premier appel à `TrySolution` pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="7f48e-106">This example requires only the result from the first call to `TrySolution` to finish.</span></span>  
  
 [!code-csharp[TPLDataflow_ReceiveAny#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_receiveany/cs/dataflowreceiveany.cs#1)]
 [!code-vb[TPLDataflow_ReceiveAny#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_receiveany/vb/dataflowreceiveany.vb#1)]  
  
 <span data-ttu-id="7f48e-107">Pour recevoir la valeur du premier objet <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> qui se termine, cet exemple définit la méthode `ReceiveFromAny(T)`.</span><span class="sxs-lookup"><span data-stu-id="7f48e-107">To receive the value from the first <xref:System.Threading.Tasks.Dataflow.TransformBlock%602> object that finishes, this example defines the `ReceiveFromAny(T)` method.</span></span> <span data-ttu-id="7f48e-108">La méthode `ReceiveFromAny(T)` accepte un tableau d’objets <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> et lie chacun de ces objets à un objet <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601>.</span><span class="sxs-lookup"><span data-stu-id="7f48e-108">The `ReceiveFromAny(T)` method accepts an array of <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> objects and links each of these objects to a <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> object.</span></span> <span data-ttu-id="7f48e-109">Si vous utilisez la méthode <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601.LinkTo%2A> pour lier un bloc source de flux de données à un bloc cible, le premier propage les messages auprès du second au fil de l’arrivée des données.</span><span class="sxs-lookup"><span data-stu-id="7f48e-109">When you use the <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601.LinkTo%2A> method to link a source dataflow block to a target block, the source propagates messages to the target as data becomes available.</span></span> <span data-ttu-id="7f48e-110">Étant donné que la classe <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> accepte uniquement le premier message proposé, la méthode `ReceiveFromAny(T)` produit ses résultats en appelant la méthode <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Receive%2A>.</span><span class="sxs-lookup"><span data-stu-id="7f48e-110">Because the <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> class accepts only the first message that it is offered, the `ReceiveFromAny(T)` method produces its result by calling the <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Receive%2A> method.</span></span> <span data-ttu-id="7f48e-111">Cela génère le premier message proposé à l’objet <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601>.</span><span class="sxs-lookup"><span data-stu-id="7f48e-111">This produces the first message that is offered to the <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> object.</span></span> <span data-ttu-id="7f48e-112">La méthode <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601.LinkTo%2A> a une version surchargée acceptant un paramètre <xref:System.Boolean>, `unlinkAfterOne`, qui, lorsqu’il a la valeur `True`, impose au bloc source de se dissocier du bloc cible dès que ce dernier a reçu un message provenant du bloc source.</span><span class="sxs-lookup"><span data-stu-id="7f48e-112">The <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601.LinkTo%2A> method has an overloaded version that takes a <xref:System.Boolean> parameter, `unlinkAfterOne` that, when it is set to `True`, instructs the source block to unlink from the target after the target receives one message from the source.</span></span> <span data-ttu-id="7f48e-113">Il est important que l’objet <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> se dissocie de ses sources, car la relation qu’il entretient avec le tableau de sources n’est plus nécessaire dès lors qu’il a reçu un message<xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601><xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601>.</span><span class="sxs-lookup"><span data-stu-id="7f48e-113">It is important for the <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> object to unlink from its sources because the relationship between the array of sources and the <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> object is no longer required after the <xref:System.Threading.Tasks.Dataflow.WriteOnceBlock%601> object receives a message.</span></span>  
  
 <span data-ttu-id="7f48e-114">Pour permettre aux appels restants à `TrySolution` de se terminer dès que l’un d’eux a calculé une valeur, la méthode `TrySolution` prend un objet <xref:System.Threading.CancellationToken> qui est annulé après que l’appel à `ReceiveFromAny(T)` a produit une sortie.</span><span class="sxs-lookup"><span data-stu-id="7f48e-114">To enable the remaining calls to `TrySolution` to end after one of them computes a value, the `TrySolution` method takes a <xref:System.Threading.CancellationToken> object that is canceled after the call to `ReceiveFromAny(T)` returns.</span></span> <span data-ttu-id="7f48e-115">La méthode <xref:System.Threading.SpinWait.SpinUntil%2A> produit une sortie quand cet objet <xref:System.Threading.CancellationToken> est annulé.</span><span class="sxs-lookup"><span data-stu-id="7f48e-115">The <xref:System.Threading.SpinWait.SpinUntil%2A> method returns when this <xref:System.Threading.CancellationToken> object is canceled.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7f48e-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="7f48e-116">Compiling the Code</span></span>  
 <span data-ttu-id="7f48e-117">Copiez l’exemple de code et collez-le dans un projet Visual Studio, ou collez-le dans un fichier nommé `DataflowReceiveAny.cs` (`DataflowReceiveAny.vb` pour [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), puis exécutez la commande suivante dans une fenêtre d’invite de commandes Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7f48e-117">Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `DataflowReceiveAny.cs` (`DataflowReceiveAny.vb` for [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), and then run the following command in a Visual Studio Command Prompt window.</span></span>  
  
 [!INCLUDE[csprcs](../../../includes/csprcs-md.md)]  
  
 <span data-ttu-id="7f48e-118">**csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowReceiveAny.cs**</span><span class="sxs-lookup"><span data-stu-id="7f48e-118">**csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowReceiveAny.cs**</span></span>  
  
 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]  
  
 <span data-ttu-id="7f48e-119">**vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowReceiveAny.vb**</span><span class="sxs-lookup"><span data-stu-id="7f48e-119">**vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowReceiveAny.vb**</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f48e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f48e-120">See Also</span></span>  
 [<span data-ttu-id="7f48e-121">Le flux de données</span><span class="sxs-lookup"><span data-stu-id="7f48e-121">Dataflow</span></span>](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)
