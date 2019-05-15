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
ms.openlocfilehash: 77f75a7eb1d7cc536df7110ef55727fbdf789f23
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591602"
---
# <a name="how-to-run-an-operation-in-the-background"></a><span data-ttu-id="a5afc-102">Procédure : exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a5afc-102">How to: Run an Operation in the Background</span></span>
<span data-ttu-id="a5afc-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="a5afc-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>  
  
 <span data-ttu-id="a5afc-104">L'exemple de code suivant montre comment exécuter une longue opération en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a5afc-104">The following code example shows how to run a time-consuming operation in the background.</span></span> <span data-ttu-id="a5afc-105">Le formulaire possède des boutons **Démarrer** et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="a5afc-105">The form has **Start** and **Cancel** buttons.</span></span> <span data-ttu-id="a5afc-106">Cliquez sur le bouton **Démarrer** pour exécuter une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a5afc-106">Click the **Start** button to run an asynchronous operation.</span></span> <span data-ttu-id="a5afc-107">Cliquez sur le bouton **Annuler** pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a5afc-107">Click the **Cancel** button to stop a running asynchronous operation.</span></span> <span data-ttu-id="a5afc-108">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="a5afc-108">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
 <span data-ttu-id="a5afc-109">Cette tâche est très bien prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a5afc-109">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="a5afc-110">Consultez également [procédure pas à pas : Exécution d’une opération en arrière-plan](walkthrough-running-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="a5afc-110">Also see [Walkthrough: Running an Operation in the Background](walkthrough-running-an-operation-in-the-background.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a5afc-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5afc-111">Example</span></span>  
 [!code-csharp[System.ComponentModel.BackgroundWorker.Example#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.Example#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a5afc-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a5afc-112">Compiling the Code</span></span>  
 <span data-ttu-id="a5afc-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="a5afc-113">This example requires:</span></span>  
  
- <span data-ttu-id="a5afc-114">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="a5afc-114">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5afc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5afc-115">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="a5afc-116">Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="a5afc-116">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
- [<span data-ttu-id="a5afc-117">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="a5afc-117">BackgroundWorker Component</span></span>](backgroundworker-component.md)
