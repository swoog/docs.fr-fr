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
ms.openlocfilehash: 94abd36affdccec1d01c030fcff4c6de93ca6c72
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43395379"
---
# <a name="how-to-run-an-operation-in-the-background"></a><span data-ttu-id="f795f-102">Comment : exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="f795f-102">How to: Run an Operation in the Background</span></span>
<span data-ttu-id="f795f-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="f795f-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>  
  
 <span data-ttu-id="f795f-104">L'exemple de code suivant montre comment exécuter une longue opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f795f-104">The following code example shows how to run a time-consuming operation in the background.</span></span> <span data-ttu-id="f795f-105">Le formulaire possède des boutons **Démarrer** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="f795f-105">The form has **Start** and **Cancel** buttons.</span></span> <span data-ttu-id="f795f-106">Cliquez sur le bouton **Démarrer** pour exécuter une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f795f-106">Click the **Start** button to run an asynchronous operation.</span></span> <span data-ttu-id="f795f-107">Cliquez sur le bouton **Annuler** pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f795f-107">Click the **Cancel** button to stop a running asynchronous operation.</span></span> <span data-ttu-id="f795f-108">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="f795f-108">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
 <span data-ttu-id="f795f-109">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f795f-109">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="f795f-110">Consultez également l’article [Procédure pas à pas : exécution d’une opération en arrière-plan](walkthrough-running-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="f795f-110">Also see [Walkthrough: Running an Operation in the Background](walkthrough-running-an-operation-in-the-background.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f795f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f795f-111">Example</span></span>  
 [!code-csharp[System.ComponentModel.BackgroundWorker.Example#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.Example#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f795f-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f795f-112">Compiling the Code</span></span>  
 <span data-ttu-id="f795f-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="f795f-113">This example requires:</span></span>  
  
-   <span data-ttu-id="f795f-114">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="f795f-114">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="f795f-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="f795f-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="f795f-116">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="f795f-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="f795f-117">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="f795f-117">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f795f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f795f-118">See Also</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 <xref:System.ComponentModel.DoWorkEventArgs>  
 [<span data-ttu-id="f795f-119">Comment : implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="f795f-119">How to: Implement a Form That Uses a Background Operation</span></span>](../../../../docs/framework/winforms/controls/how-to-implement-a-form-that-uses-a-background-operation.md)  
 [<span data-ttu-id="f795f-120">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="f795f-120">BackgroundWorker Component</span></span>](../../../../docs/framework/winforms/controls/backgroundworker-component.md)
