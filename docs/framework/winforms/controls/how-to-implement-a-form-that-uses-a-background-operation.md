---
title: 'Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan'
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
ms.openlocfilehash: 9fe514cce4d4aec386f9d61cb84f3a39273c35b0
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723333"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="c5f6d-102">Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="c5f6d-102">How to: Implement a Form That Uses a Background Operation</span></span>
<span data-ttu-id="c5f6d-103">L'exemple de programme suivant crée un formulaire qui calcule les nombres de Fibonacci.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-103">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="c5f6d-104">Le calcul s'exécute sur un thread distinct du thread d'interface utilisateur, pour que l'interface utilisateur continue de s'exécuter sans délai lors du calcul.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-104">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="c5f6d-105">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-105">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="c5f6d-106">Consultez également [procédure pas à pas : Implémentation d’un formulaire qui utilise une opération d’arrière-plan](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c5f6d-106">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c5f6d-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="c5f6d-107">Example</span></span>  
 [!code-cpp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c5f6d-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c5f6d-108">Compiling the Code</span></span>  
 <span data-ttu-id="c5f6d-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="c5f6d-109">This example requires:</span></span>  
  
-   <span data-ttu-id="c5f6d-110">Références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-110">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="c5f6d-111">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="c5f6d-111">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="c5f6d-112">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-112">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="c5f6d-113">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="c5f6d-113">Robust Programming</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="c5f6d-114">Quand vous utilisez le multithreading, vous vous exposez potentiellement à des bogues très sérieux et complexes.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-114">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="c5f6d-115">Consultez les [Meilleures pratiques pour le threading managé](../../../standard/threading/managed-threading-best-practices.md) avant d’implémenter une solution qui utilise le multithreading.</span><span class="sxs-lookup"><span data-stu-id="c5f6d-115">Consult the [Managed Threading Best Practices](../../../standard/threading/managed-threading-best-practices.md) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5f6d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5f6d-116">See also</span></span>
- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="c5f6d-117">Vue d’ensemble du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="c5f6d-117">Event-based Asynchronous Pattern Overview</span></span>](../../../standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
- [<span data-ttu-id="c5f6d-118">Bonnes pratiques de threading géré</span><span class="sxs-lookup"><span data-stu-id="c5f6d-118">Managed Threading Best Practices</span></span>](../../../standard/threading/managed-threading-best-practices.md)
