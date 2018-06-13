---
title: 'Comment : ajouter un ToolStripContainer à un formulaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStrip control [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], adding to Windows Forms
ms.assetid: d0f55095-a833-453e-be5a-644906d75d54
ms.openlocfilehash: 7e9b12505c0e80cdafe56967321f46d41305b799
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524678"
---
# <a name="how-to-add-a-toolstripcontainer-to-a-form"></a><span data-ttu-id="6a931-102">Comment : ajouter un ToolStripContainer à un formulaire</span><span class="sxs-lookup"><span data-stu-id="6a931-102">How to: Add a ToolStripContainer to a Form</span></span>
<span data-ttu-id="6a931-103">Vous pouvez ajouter par programmation un <xref:System.Windows.Forms.ToolStripContainer> à un Windows Form et le remplir avec des contrôles.</span><span class="sxs-lookup"><span data-stu-id="6a931-103">You can programmatically add a <xref:System.Windows.Forms.ToolStripContainer> to a Windows Form and populate it with controls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6a931-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a931-104">Example</span></span>  
 <span data-ttu-id="6a931-105">L'exemple de code suivant montre comment ajouter un <xref:System.Windows.Forms.ToolStripContainer> et un <xref:System.Windows.Forms.ToolStrip> à un Windows Forms, comment ajouter des éléments au <xref:System.Windows.Forms.ToolStrip> et comment ajouter le <xref:System.Windows.Forms.ToolStrip> au <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> du <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="6a931-105">The following code example demonstrates how to add a <xref:System.Windows.Forms.ToolStripContainer> and a <xref:System.Windows.Forms.ToolStrip> to a Windows Forms, how to add items to the <xref:System.Windows.Forms.ToolStrip>, and how to add the <xref:System.Windows.Forms.ToolStrip> to the <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/cs/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/vb/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6a931-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="6a931-106">Compiling the Code</span></span>  
 <span data-ttu-id="6a931-107">Cet exemple de code nécessite :</span><span class="sxs-lookup"><span data-stu-id="6a931-107">This code example requires:</span></span>  
  
-   <span data-ttu-id="6a931-108">Références aux assemblys System.Drawing, System.Text et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="6a931-108">References to the System.Drawing, System.Text, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="6a931-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="6a931-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="6a931-110">Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="6a931-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="6a931-111">Consultez également [Guide pratique pour compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) ou [Tâches ToolStripContainer, boîte de dialogue](http://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="6a931-111">See also [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) or [ToolStripContainer Tasks Dialog Box](http://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a931-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a931-112">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStripContainer>  
 [<span data-ttu-id="6a931-113">ToolStripContainer, contrôle</span><span class="sxs-lookup"><span data-stu-id="6a931-113">ToolStripContainer Control</span></span>](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)  
 [<span data-ttu-id="6a931-114">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="6a931-114">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
