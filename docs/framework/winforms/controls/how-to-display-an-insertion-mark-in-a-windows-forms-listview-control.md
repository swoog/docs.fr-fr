---
title: 'Procédure : Afficher une marque d’Insertion dans un contrôle de ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ListView control [Windows Forms], drag operations
- graphics [Windows Forms], insertion marks
- drop and drag [Windows Forms], insertion marks
- insertion marks
ms.assetid: 88d0a15b-25fd-4dc3-a685-297351311940
ms.openlocfilehash: 1c588053f9603a796d74fd706254ea150d21573a
ms.sourcegitcommit: 15ab532fd5e1f8073a4b678922d93b68b521bfa0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58654157"
---
# <a name="how-to-display-an-insertion-mark-in-a-windows-forms-listview-control"></a><span data-ttu-id="3bdd3-102">Procédure : Afficher une marque d’Insertion dans un contrôle de ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3bdd3-102">How to: Display an Insertion Mark in a Windows Forms ListView Control</span></span>
<span data-ttu-id="3bdd3-103">La marque d'insertion dans le contrôle <xref:System.Windows.Forms.ListView> indique aux utilisateurs l'emplacement où les éléments déplacés seront insérés.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-103">The insertion mark in the <xref:System.Windows.Forms.ListView> control shows users the point where dragged items will be inserted.</span></span> <span data-ttu-id="3bdd3-104">Quand un utilisateur fait glisser un élément vers un point entre deux autres éléments, la marque d'insertion indique le nouvel emplacement prévu de l'élément.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-104">When a user drags an item to a point between two other items, the insertion mark shows the item's expected new location.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3bdd3-105">La fonctionnalité de marque d’insertion est disponible uniquement sur [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] quand votre application appelle la méthode <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-105">The insertion mark feature is available only on [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] when your application calls the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="3bdd3-106">Sur les systèmes d'exploitation antérieurs, tout code relatif à la marque d'insertion n'a aucun effet et la marque d'insertion n'apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-106">On earlier operating systems, any code relating to the insertion mark has no effect and the insertion mark will not appear.</span></span> <span data-ttu-id="3bdd3-107">Pour plus d'informations, consultez <xref:System.Windows.Forms.ListViewInsertionMark>.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-107">For more information, see <xref:System.Windows.Forms.ListViewInsertionMark>.</span></span>  
  
 <span data-ttu-id="3bdd3-108">L'illustration suivante montre une marque d'insertion :</span><span class="sxs-lookup"><span data-stu-id="3bdd3-108">The following image shows an insertion mark:</span></span>  
  
 <span data-ttu-id="3bdd3-109">![Capture d’écran montre une marque d’insertion ListView. ](./media/how-to-display-an-insertion-mark-in-a-windows-forms-listview-control/listview-insertion-mark.gif "ListViewInsertion")</span><span class="sxs-lookup"><span data-stu-id="3bdd3-109">![Screenshot that shows a ListView insertion mark.](./media/how-to-display-an-insertion-mark-in-a-windows-forms-listview-control/listview-insertion-mark.gif "ListViewInsertion")</span></span>  
  
 <span data-ttu-id="3bdd3-110">L’exemple de code suivant montre comment utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-110">The following code example demonstrates how to use this feature.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3bdd3-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="3bdd3-111">Example</span></span>  
 [!code-cpp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CPP/listviewinsertionmarkexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/CS/listviewinsertionmarkexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.InsertionMark#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.InsertionMark/VB/listviewinsertionmarkexample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3bdd3-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3bdd3-112">Compiling the Code</span></span>  
 <span data-ttu-id="3bdd3-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="3bdd3-113">This example requires:</span></span>  
  
-   <span data-ttu-id="3bdd3-114">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="3bdd3-114">References to the System and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="3bdd3-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="3bdd3-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="3bdd3-116">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="3bdd3-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3bdd3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bdd3-117">See also</span></span>
- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.InsertionMark%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ListViewInsertionMark>
- [<span data-ttu-id="3bdd3-118">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="3bdd3-118">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="3bdd3-119">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="3bdd3-119">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="3bdd3-120">Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3bdd3-120">Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms</span></span>](../advanced/walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md)
