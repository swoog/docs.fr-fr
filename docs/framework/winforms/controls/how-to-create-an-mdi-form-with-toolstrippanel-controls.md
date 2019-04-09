---
title: 'Procédure : créer un formulaire MDI avec des contrôles ToolStripPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripPanel control [Windows Forms]
- MDI [Windows Forms], creating forms
- multiple document interface forms
- MDI forms [Windows Forms]
- ToolStrip control [Windows Forms]
- MDI forms [Windows Forms], creating
ms.assetid: d198ef8e-f7c4-4b3f-a7f5-ce858cb90cec
ms.openlocfilehash: 55c2294496800fb8692d3c8215c1c13f7dac9b01
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59096964"
---
# <a name="how-to-create-an-mdi-form-with-toolstrippanel-controls"></a><span data-ttu-id="cea52-102">Procédure : créer un formulaire MDI avec des contrôles ToolStripPanel</span><span class="sxs-lookup"><span data-stu-id="cea52-102">How to: Create an MDI Form with ToolStripPanel Controls</span></span>
<span data-ttu-id="cea52-103">Vous pouvez créer un formulaire d'interface multidocument (MDI) ayant des contrôles <xref:System.Windows.Forms.ToolStrip> qui l'encadrent sur les quatre côtés.</span><span class="sxs-lookup"><span data-stu-id="cea52-103">You can create a multiple document interface (MDI) form that has <xref:System.Windows.Forms.ToolStrip> controls framing it on all four sides.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cea52-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cea52-104">Example</span></span>  
 <span data-ttu-id="cea52-105">L'exemple de code suivant montre comment utiliser des contrôles <xref:System.Windows.Forms.ToolStripPanel> ancrés pour encadrer une fenêtre MDI avec quatre contrôles <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="cea52-105">The following code example demonstrates how to use docked <xref:System.Windows.Forms.ToolStripPanel> controls to frame an MDI window with four <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="cea52-106">Dans l'exemple, la méthode <xref:System.Windows.Forms.ToolStripPanel.Join%2A> attache les contrôles <xref:System.Windows.Forms.ToolStrip> aux contrôles <xref:System.Windows.Forms.ToolStripPanel> correspondants.</span><span class="sxs-lookup"><span data-stu-id="cea52-106">In the example, the <xref:System.Windows.Forms.ToolStripPanel.Join%2A> method attaches the <xref:System.Windows.Forms.ToolStrip> controls to the corresponding <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#10)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="cea52-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="cea52-107">Compiling the Code</span></span>  
 <span data-ttu-id="cea52-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="cea52-108">This example requires:</span></span>  
  
-   <span data-ttu-id="cea52-109">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="cea52-109">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="cea52-110">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="cea52-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="cea52-111">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="cea52-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cea52-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cea52-112">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripPanel>
- <xref:System.Windows.Forms.ToolStripPanel.Join%2A>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [<span data-ttu-id="cea52-113">ToolStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="cea52-113">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
