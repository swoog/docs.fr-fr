---
title: "Comment : implémenter un modèle de flux de données producteur-consommateur"
ms.date: 03/30/2017
ms.prod: .net
ms.technology: dotnet-standard
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TPL dataflow library, implementing producer-consumer pattern
- Task Parallel Library, dataflows
- producer-consumer patterns, implementing [TPL]
ms.assetid: 47a1d38c-fe9c-44aa-bd15-937bd5659b0b
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 3758ec77a722a66c6faa287d299e5e9c38858be5
ms.sourcegitcommit: 6a9030eb5bd0f00e1d144f81958adb195cfb1f6f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/10/2018
---
# <a name="how-to-implement-a-producer-consumer-dataflow-pattern"></a><span data-ttu-id="3ffa0-102">Comment : implémenter un modèle de flux de données producteur-consommateur</span><span class="sxs-lookup"><span data-stu-id="3ffa0-102">How to: Implement a Producer-Consumer Dataflow Pattern</span></span>
<span data-ttu-id="3ffa0-103">Ce document décrit comment utiliser la bibliothèque de flux de données TPL pour implémenter un modèle producteur-consommateur.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-103">This document describes how to use the TPL Dataflow Library to implement a producer-consumer pattern.</span></span> <span data-ttu-id="3ffa0-104">Dans ce modèle, le *producteur* envoie des messages à un bloc de message et le *consommateur* lit les messages de ce bloc.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-104">In this pattern, the *producer* sends messages to a message block, and the *consumer* reads messages from that block.</span></span>  

[!INCLUDE [tpl-install-instructions](../../../includes/tpl-install-instructions.md)]
  
## <a name="example"></a><span data-ttu-id="3ffa0-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ffa0-105">Example</span></span>  
 <span data-ttu-id="3ffa0-106">L’exemple suivant montre un modèle producteur-consommateur de base qui utilise des flux de données.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-106">The following example demonstrates a basic producer- consumer model that uses dataflow.</span></span> <span data-ttu-id="3ffa0-107">La méthode `Produce` écrit des tableaux contenant les octets aléatoires de données dans un objet <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601?displayProperty=nameWithType>, et la méthode `Consume` lit les octets à partir d’un objet <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-107">The `Produce` method writes arrays that contain random bytes of data to a <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601?displayProperty=nameWithType> object and the `Consume` method reads bytes from a <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601?displayProperty=nameWithType> object.</span></span> <span data-ttu-id="3ffa0-108">En utilisant les interfaces <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> et <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601>, et non leurs types dérivés, vous pouvez écrire du code réutilisable sur une variété de types de blocs de flux de données.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-108">By acting on the <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> and <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601> interfaces, instead of their derived types, you can write reusable code that can act on a variety of dataflow block types.</span></span> <span data-ttu-id="3ffa0-109">Cet exemple utilise la classe <xref:System.Threading.Tasks.Dataflow.BufferBlock%601>.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-109">This example uses the <xref:System.Threading.Tasks.Dataflow.BufferBlock%601> class.</span></span> <span data-ttu-id="3ffa0-110">Dans la mesure où la classe <xref:System.Threading.Tasks.Dataflow.BufferBlock%601> agit à la fois en tant que source et cible, le producteur et le consommateur peuvent utiliser un objet partagé pour transférer les données.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-110">Because the <xref:System.Threading.Tasks.Dataflow.BufferBlock%601> class acts as both a source block and as a target block, the producer and the consumer can use a shared object to transfer data.</span></span>  
  
 <span data-ttu-id="3ffa0-111">La méthode `Produce` appelle la méthode <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Post%2A> dans une boucle pour écrire de façon synchrone des données vers le bloc cible.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-111">The `Produce` method calls the <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Post%2A> method in a loop to synchronously write data to the target block.</span></span> <span data-ttu-id="3ffa0-112">Dès que la méthode `Produce` a écrit toutes les données dans le bloc cible, celle-ci appelle la méthode <xref:System.Threading.Tasks.Dataflow.IDataflowBlock.Complete%2A> pour indiquer que le bloc n’aura jamais aucune donnée supplémentaire disponible.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-112">After the `Produce` method writes all data to the target block, it calls the <xref:System.Threading.Tasks.Dataflow.IDataflowBlock.Complete%2A> method to indicate that the block will never have additional data available.</span></span> <span data-ttu-id="3ffa0-113">La méthode `Consume` utilise les opérateurs [async](~/docs/csharp/language-reference/keywords/async.md) et [await](~/docs/csharp/language-reference/keywords/await.md) ([Async](~/docs/visual-basic/language-reference/modifiers/async.md) et [Await](~/docs/visual-basic/language-reference/operators/await-operator.md) dans [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]) pour calculer de façon asynchrone le nombre total d’octets provenant de l’objet <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601>.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-113">The `Consume` method uses the [async](~/docs/csharp/language-reference/keywords/async.md) and [await](~/docs/csharp/language-reference/keywords/await.md) operators ([Async](~/docs/visual-basic/language-reference/modifiers/async.md) and [Await](~/docs/visual-basic/language-reference/operators/await-operator.md) in [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]) to asynchronously compute the total number of bytes that are received from the <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> object.</span></span> <span data-ttu-id="3ffa0-114">Pour agir de façon asynchrone, la méthode `Consume` appelle la méthode <xref:System.Threading.Tasks.Dataflow.DataflowBlock.OutputAvailableAsync%2A> pour recevoir une notification lorsque le bloc source possède des données disponibles et lorsque le bloc source n’aura jamais aucune donnée supplémentaire disponible.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-114">To act asynchronously, the `Consume` method calls the <xref:System.Threading.Tasks.Dataflow.DataflowBlock.OutputAvailableAsync%2A> method to receive a notification when the source block has data available and when the source block will never have additional data available.</span></span>  
  
 [!code-csharp[TPLDataflow_ProducerConsumer#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_producerconsumer/cs/dataflowproducerconsumer.cs#1)]
 [!code-vb[TPLDataflow_ProducerConsumer#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_producerconsumer/vb/dataflowproducerconsumer.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3ffa0-115">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3ffa0-115">Compiling the Code</span></span>  
 <span data-ttu-id="3ffa0-116">Copiez l’exemple de code et collez-le dans un projet Visual Studio, ou collez-le dans un fichier nommé `DataflowProducerConsumer.cs` (`DataflowProducerConsumer.vb` pour [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), puis exécutez la commande suivante dans une fenêtre d’invite de commandes Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-116">Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `DataflowProducerConsumer.cs` (`DataflowProducerConsumer.vb` for [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), and then run the following command in a Visual Studio Command Prompt window.</span></span>  
  
 [!INCLUDE[csprcs](../../../includes/csprcs-md.md)]  
  
 <span data-ttu-id="3ffa0-117">**csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowProducerConsumer.cs**</span><span class="sxs-lookup"><span data-stu-id="3ffa0-117">**csc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowProducerConsumer.cs**</span></span>  
  
 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]  
  
 <span data-ttu-id="3ffa0-118">**vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowProducerConsumer.vb**</span><span class="sxs-lookup"><span data-stu-id="3ffa0-118">**vbc.exe /r:System.Threading.Tasks.Dataflow.dll DataflowProducerConsumer.vb**</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="3ffa0-119">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="3ffa0-119">Robust Programming</span></span>  
 <span data-ttu-id="3ffa0-120">Cet exemple utilise un seul consommateur pour traiter les données source.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-120">This example uses just one consumer to process the source data.</span></span> <span data-ttu-id="3ffa0-121">Si votre application dispose de plusieurs consommateurs, utilisez la méthode <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceive%2A> pour lire des données à partir du bloc source, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-121">If you have multiple consumers in your application, use the <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceive%2A> method to read data from the source block, as shown in the following example.</span></span>  
  
 [!code-csharp[TPLDataflow_ProducerConsumer#2](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_producerconsumer/cs/dataflowproducerconsumer.cs#2)]
 [!code-vb[TPLDataflow_ProducerConsumer#2](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_producerconsumer/vb/dataflowproducerconsumer.vb#2)]  
  
 <span data-ttu-id="3ffa0-122">La méthode <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceive%2A> retourne `False` si donnée n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-122">The <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceive%2A> method returns `False` when no data is available.</span></span> <span data-ttu-id="3ffa0-123">Lorsque plusieurs consommateurs doivent accéder simultanément au bloc source, ce mécanisme garantit que les données sont toujours disponibles après l’appel à <xref:System.Threading.Tasks.Dataflow.DataflowBlock.OutputAvailableAsync%2A>.</span><span class="sxs-lookup"><span data-stu-id="3ffa0-123">When multiple consumers must access the source block concurrently, this mechanism guarantees that data is still available after the call to <xref:System.Threading.Tasks.Dataflow.DataflowBlock.OutputAvailableAsync%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ffa0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ffa0-124">See Also</span></span>  
 [<span data-ttu-id="3ffa0-125">Le flux de données</span><span class="sxs-lookup"><span data-stu-id="3ffa0-125">Dataflow</span></span>](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)
