---
title: 'Procédure : exécuter une opération en arrière-plan'
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
ms.openlocfilehash: 5ccbb6e4c09f5417f6c2766824ec7ed9722eed52
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217989"
---
# <a name="how-to-run-an-operation-in-the-background"></a><span data-ttu-id="d403b-102">Procédure : exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="d403b-102">How to: Run an Operation in the Background</span></span>
<span data-ttu-id="d403b-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="d403b-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>  
  
 <span data-ttu-id="d403b-104">L'exemple de code suivant montre comment exécuter une longue opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d403b-104">The following code example shows how to run a time-consuming operation in the background.</span></span> <span data-ttu-id="d403b-105">Le formulaire possède des boutons **Démarrer** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="d403b-105">The form has **Start** and **Cancel** buttons.</span></span> <span data-ttu-id="d403b-106">Cliquez sur le bouton **Démarrer** pour exécuter une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d403b-106">Click the **Start** button to run an asynchronous operation.</span></span> <span data-ttu-id="d403b-107">Cliquez sur le bouton **Annuler** pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d403b-107">Click the **Cancel** button to stop a running asynchronous operation.</span></span> <span data-ttu-id="d403b-108">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="d403b-108">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
 <span data-ttu-id="d403b-109">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d403b-109">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="d403b-110">Consultez également [procédure pas à pas : Exécution d’une opération en arrière-plan](walkthrough-running-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="d403b-110">Also see [Walkthrough: Running an Operation in the Background](walkthrough-running-an-operation-in-the-background.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d403b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="d403b-111">Example</span></span>  
 [!code-csharp[System.ComponentModel.BackgroundWorker.Example#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.Example#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d403b-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="d403b-112">Compiling the Code</span></span>  
 <span data-ttu-id="d403b-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="d403b-113">This example requires:</span></span>  
  
-   <span data-ttu-id="d403b-114">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="d403b-114">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="d403b-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="d403b-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="d403b-116">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="d403b-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d403b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d403b-117">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="d403b-118">Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="d403b-118">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
- [<span data-ttu-id="d403b-119">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="d403b-119">BackgroundWorker Component</span></span>](backgroundworker-component.md)
