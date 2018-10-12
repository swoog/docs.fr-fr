---
title: Écrire un programme parallèle simple à l’aide de Parallel.ForEach
ms.date: 09/12/2018
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- foreach, parallel version
- parallel programming, foreach
ms.assetid: cb5fab92-1c19-499e-ae91-8b7525dd875f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cdf4aeb6de027e26687d41d6311b6d7da49e7948
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562214"
---
# <a name="how-to-write-a-simple-parallelforeach-loop"></a><span data-ttu-id="a538a-102">Comment : écrire une boucle Parallel.ForEach simple</span><span class="sxs-lookup"><span data-stu-id="a538a-102">How to: Write a Simple Parallel.ForEach Loop</span></span>

<span data-ttu-id="a538a-103">Cet exemple montre comment utiliser une boucle <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> pour activer le parallélisme des données sur n’importe quelle source de données <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="a538a-103">This example shows how to use a <xref:System.Threading.Tasks.Parallel.ForEach%2A?displayProperty=nameWithType> loop to enable data parallelism over any <xref:System.Collections.IEnumerable?displayProperty=nameWithType> or <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType> data source.</span></span>

> [!NOTE]
> <span data-ttu-id="a538a-104">Cette documentation utilise des expressions lambda pour définir les délégués en PLINQ.</span><span class="sxs-lookup"><span data-stu-id="a538a-104">This documentation uses lambda expressions to define delegates in PLINQ.</span></span> <span data-ttu-id="a538a-105">Si les expressions lambda en C# ou Visual Basic ne vous sont pas familières, consultez la page [Expressions lambda en PLINQ et dans la bibliothèque parallèle de tâches](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md).</span><span class="sxs-lookup"><span data-stu-id="a538a-105">If you are not familiar with lambda expressions in C# or Visual Basic, see [Lambda Expressions in PLINQ and TPL](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md).</span></span>

## <a name="example"></a><span data-ttu-id="a538a-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="a538a-106">Example</span></span>

[!code-csharp[TPL_Parallel#03](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_parallel/cs/simpleforeach.cs#03)]
[!code-vb[TPL_Parallel#03](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_parallel/vb/simpleforeach.vb#03)]

<span data-ttu-id="a538a-107">Une boule <xref:System.Threading.Tasks.Parallel.ForEach%2A> fonctionne comme une boucle <xref:System.Threading.Tasks.Parallel.For%2A>.</span><span class="sxs-lookup"><span data-stu-id="a538a-107">A <xref:System.Threading.Tasks.Parallel.ForEach%2A> loop works like a <xref:System.Threading.Tasks.Parallel.For%2A> loop.</span></span> <span data-ttu-id="a538a-108">La collection source est partitionnée et le travail est planifié sur plusieurs threads en fonction de l’environnement système.</span><span class="sxs-lookup"><span data-stu-id="a538a-108">The source collection is partitioned and the work is scheduled on multiple threads based on the system environment.</span></span> <span data-ttu-id="a538a-109">Plus il y a de processeurs sur le système, plus la méthode parallèle s’exécute rapidement.</span><span class="sxs-lookup"><span data-stu-id="a538a-109">The more processors on the system, the faster the parallel method runs.</span></span> <span data-ttu-id="a538a-110">Pour certaines collections sources, une boucle séquentielle peut être plus rapide, selon la taille de la source et le type de travail exécuté.</span><span class="sxs-lookup"><span data-stu-id="a538a-110">For some source collections, a sequential loop may be faster, depending on the size of the source, and the kind of work being performed.</span></span> <span data-ttu-id="a538a-111">Pour plus d’informations sur les performances, consultez [Pièges potentiels dans le parallélisme des données et des tâches](../../../docs/standard/parallel-programming/potential-pitfalls-in-data-and-task-parallelism.md)</span><span class="sxs-lookup"><span data-stu-id="a538a-111">For more information about performance, see [Potential Pitfalls in Data and Task Parallelism](../../../docs/standard/parallel-programming/potential-pitfalls-in-data-and-task-parallelism.md)</span></span>

<span data-ttu-id="a538a-112">Pour plus d’informations sur les boucles parallèles, consultez [Guide pratique : écrire une boucle Parallel.For simple](../../../docs/standard/parallel-programming/how-to-write-a-simple-parallel-for-loop.md).</span><span class="sxs-lookup"><span data-stu-id="a538a-112">For more information about parallel loops, see [How to: Write a Simple Parallel.For Loop](../../../docs/standard/parallel-programming/how-to-write-a-simple-parallel-for-loop.md).</span></span>

<span data-ttu-id="a538a-113">Pour utiliser <xref:System.Threading.Tasks.Parallel.ForEach%2A> avec une collection non générique, vous pouvez utiliser la méthode d’extension <xref:System.Linq.Enumerable.Cast%2A> pour convertir la collection en une collection générique, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="a538a-113">To use <xref:System.Threading.Tasks.Parallel.ForEach%2A> with a non-generic collection, you can use the <xref:System.Linq.Enumerable.Cast%2A> extension method to convert the collection to a generic collection, as shown in the following example:</span></span>

[!code-csharp[TPL_Parallel#07](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_parallel/cs/nongeneric.cs#07)]
[!code-vb[TPL_Parallel#07](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_parallel/vb/nongeneric.vb#07)]

<span data-ttu-id="a538a-114">Vous pouvez également utiliser PLINQ (Parallel LINQ) pour paralléliser le traitement des sources de données <xref:System.Collections.Generic.IEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="a538a-114">You can also use Parallel LINQ (PLINQ) to parallelize processing of <xref:System.Collections.Generic.IEnumerable%601> data sources.</span></span> <span data-ttu-id="a538a-115">PLINQ vous permet d’utiliser la syntaxe de requête déclarative pour exprimer le comportement de la boucle.</span><span class="sxs-lookup"><span data-stu-id="a538a-115">PLINQ enables you to use declarative query syntax to express the loop behavior.</span></span> <span data-ttu-id="a538a-116">Pour plus d’informations, consultez [PLINQ (Parallel LINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md).</span><span class="sxs-lookup"><span data-stu-id="a538a-116">For more information, see [Parallel LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md).</span></span>

## <a name="compile-and-run-the-code"></a><span data-ttu-id="a538a-117">Compiler et exécuter le code</span><span class="sxs-lookup"><span data-stu-id="a538a-117">Compile and run the code</span></span>

- <span data-ttu-id="a538a-118">Copiez et collez ce code dans un projet **d’application console** Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a538a-118">Copy and paste this code into a Visual Studio **Console App** project.</span></span>

- <span data-ttu-id="a538a-119">Ajoutez une référence à System.Drawing.dll</span><span class="sxs-lookup"><span data-stu-id="a538a-119">Add a reference to System.Drawing.dll</span></span>

- <span data-ttu-id="a538a-120">Appuyez sur **F5**</span><span class="sxs-lookup"><span data-stu-id="a538a-120">Press **F5**</span></span>

## <a name="see-also"></a><span data-ttu-id="a538a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a538a-121">See also</span></span>

- [<span data-ttu-id="a538a-122">Parallélisme de données</span><span class="sxs-lookup"><span data-stu-id="a538a-122">Data Parallelism</span></span>](../../../docs/standard/parallel-programming/data-parallelism-task-parallel-library.md)
- [<span data-ttu-id="a538a-123">Programmation parallèle</span><span class="sxs-lookup"><span data-stu-id="a538a-123">Parallel Programming</span></span>](../../../docs/standard/parallel-programming/index.md)
- [<span data-ttu-id="a538a-124">Parallel LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="a538a-124">Parallel LINQ (PLINQ)</span></span>](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
