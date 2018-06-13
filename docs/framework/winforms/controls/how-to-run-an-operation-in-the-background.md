---
title: 'Comment : exécuter une opération en arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- background tasks
- forms [Windows Forms], multithreading
- forms [Windows Forms], background operations
- background threads
- BackgroundWorker class [Windows Forms], examples
- threading [Windows Forms], background operations
- background operations
ms.assetid: 5b56e2aa-dc05-444f-930c-2d7b23f9ad5b
ms.openlocfilehash: 7a2ce452a1e55d0b01245c4eb7f43056031b9e2b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33533911"
---
# <a name="how-to-run-an-operation-in-the-background"></a><span data-ttu-id="692bc-102">Comment : exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="692bc-102">How to: Run an Operation in the Background</span></span>
<span data-ttu-id="692bc-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="692bc-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>  
  
 <span data-ttu-id="692bc-104">L'exemple de code suivant montre comment exécuter une longue opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="692bc-104">The following code example shows how to run a time-consuming operation in the background.</span></span> <span data-ttu-id="692bc-105">Le formulaire possède des boutons **Démarrer** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="692bc-105">The form has **Start** and **Cancel** buttons.</span></span> <span data-ttu-id="692bc-106">Cliquez sur le bouton **Démarrer** pour exécuter une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="692bc-106">Click the **Start** button to run an asynchronous operation.</span></span> <span data-ttu-id="692bc-107">Cliquez sur le bouton **Annuler** pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="692bc-107">Click the **Cancel** button to stop a running asynchronous operation.</span></span> <span data-ttu-id="692bc-108">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="692bc-108">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
 <span data-ttu-id="692bc-109">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="692bc-109">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="692bc-110">Consultez également l’article [Procédure pas à pas : exécution d’une opération en arrière-plan](http://msdn.microsoft.com/library/ms233672\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="692bc-110">Also see [Walkthrough: Running an Operation in the Background](http://msdn.microsoft.com/library/ms233672\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="692bc-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="692bc-111">Example</span></span>  
 [!code-csharp[System.ComponentModel.BackgroundWorker.Example#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.Example#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="692bc-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="692bc-112">Compiling the Code</span></span>  
 <span data-ttu-id="692bc-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="692bc-113">This example requires:</span></span>  
  
-   <span data-ttu-id="692bc-114">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="692bc-114">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="692bc-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="692bc-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="692bc-116">Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="692bc-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="692bc-117">Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="692bc-117">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="692bc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="692bc-118">See Also</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 <xref:System.ComponentModel.DoWorkEventArgs>  
 [<span data-ttu-id="692bc-119">Comment : implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="692bc-119">How to: Implement a Form That Uses a Background Operation</span></span>](../../../../docs/framework/winforms/controls/how-to-implement-a-form-that-uses-a-background-operation.md)  
 [<span data-ttu-id="692bc-120">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="692bc-120">BackgroundWorker Component</span></span>](../../../../docs/framework/winforms/controls/backgroundworker-component.md)
