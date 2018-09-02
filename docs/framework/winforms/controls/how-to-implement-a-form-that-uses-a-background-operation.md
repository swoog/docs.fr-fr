---
title: "Comment : implémenter un formulaire qui utilise une opération d'arrière-plan"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: 8f348097223d2db4c54d9ecbba89eb8d179b6680
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404534"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="5ec44-102">Comment : implémenter un formulaire qui utilise une opération d'arrière-plan</span><span class="sxs-lookup"><span data-stu-id="5ec44-102">How to: Implement a Form That Uses a Background Operation</span></span>
<span data-ttu-id="5ec44-103">L'exemple de programme suivant crée un formulaire qui calcule les nombres de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="5ec44-103">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="5ec44-104">Le calcul s'exécute sur un thread distinct du thread d'interface utilisateur, pour que l'interface utilisateur continue de s'exécuter sans délai lors du calcul.</span><span class="sxs-lookup"><span data-stu-id="5ec44-104">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="5ec44-105">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5ec44-105">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="5ec44-106">Consultez également [Procédure pas à pas : implémentation d’un formulaire qui utilise une opération d’arrière-plan](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="5ec44-106">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](https://msdn.microsoft.com/library/b2zk6580\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ec44-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ec44-107">Example</span></span>  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5ec44-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5ec44-108">Compiling the Code</span></span>  
 <span data-ttu-id="5ec44-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="5ec44-109">This example requires:</span></span>  
  
-   <span data-ttu-id="5ec44-110">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="5ec44-110">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="5ec44-111">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="5ec44-111">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="5ec44-112">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="5ec44-112">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="5ec44-113">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="5ec44-113">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="5ec44-114">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="5ec44-114">Robust Programming</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="5ec44-115">Quand vous utilisez le multithreading, vous vous exposez potentiellement à des bogues très sérieux et complexes.</span><span class="sxs-lookup"><span data-stu-id="5ec44-115">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="5ec44-116">Consultez les [Meilleures pratiques pour le threading managé](../../../../docs/standard/threading/managed-threading-best-practices.md) avant d’implémenter une solution qui utilise le multithreading.</span><span class="sxs-lookup"><span data-stu-id="5ec44-116">Consult the [Managed Threading Best Practices](../../../../docs/standard/threading/managed-threading-best-practices.md) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ec44-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec44-117">See Also</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 <xref:System.ComponentModel.DoWorkEventArgs>  
 [<span data-ttu-id="5ec44-118">Vue d’ensemble du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="5ec44-118">Event-based Asynchronous Pattern Overview</span></span>](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)  
 [<span data-ttu-id="5ec44-119">Bonnes pratiques de threading géré</span><span class="sxs-lookup"><span data-stu-id="5ec44-119">Managed Threading Best Practices</span></span>](../../../../docs/standard/threading/managed-threading-best-practices.md)
