---
title: 'Procédure : ajouter dynamiquement des éléments ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- toolbars [Windows Forms], adding items dynamically
- ToolStrip control [Windows Forms]
ms.assetid: 0e8dea56-5f46-408b-914d-7e360341a234
ms.openlocfilehash: 9426c7cb3251dbbd95727b78c57be7a0b71556e2
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64624018"
---
# <a name="how-to-add-toolstrip-items-dynamically"></a><span data-ttu-id="5369a-102">Procédure : ajouter dynamiquement des éléments ToolStrip</span><span class="sxs-lookup"><span data-stu-id="5369a-102">How to: Add ToolStrip Items Dynamically</span></span>
<span data-ttu-id="5369a-103">Vous pouvez remplir dynamiquement la collection d'éléments de menu d'un contrôle <xref:System.Windows.Forms.ToolStrip> quand le menu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5369a-103">You can dynamically populate the menu item collection of a <xref:System.Windows.Forms.ToolStrip> control when the menu opens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5369a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5369a-104">Example</span></span>  
 <span data-ttu-id="5369a-105">L'exemple de code suivant montre comment ajouter dynamiquement des éléments à un contrôle <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="5369a-105">The following code example demonstrates how to dynamically add items to a <xref:System.Windows.Forms.ContextMenuStrip> control.</span></span> <span data-ttu-id="5369a-106">Cet exemple montre également comment réutiliser le même contrôle <xref:System.Windows.Forms.ContextMenuStrip> pour trois contrôles différents du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5369a-106">The example also shows how to reuse the same <xref:System.Windows.Forms.ContextMenuStrip> for three different controls on the form.</span></span>  
  
 <span data-ttu-id="5369a-107">Dans cet exemple, un gestionnaire d’événements <xref:System.Windows.Forms.ToolStripDropDown.Opening> remplit la collection d’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="5369a-107">In the example, an <xref:System.Windows.Forms.ToolStripDropDown.Opening> event handler populates the menu item collection.</span></span> <span data-ttu-id="5369a-108">Le gestionnaire d'événements <xref:System.Windows.Forms.ToolStripDropDown.Opening> examine les propriétés <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A?displayProperty=nameWithType> et <xref:System.Windows.Forms.ToolStripItem.OwnerItem%2A?displayProperty=nameWithType>, et ajoute un <xref:System.Windows.Forms.ToolStripItem> qui décrit le contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="5369a-108">The <xref:System.Windows.Forms.ToolStripDropDown.Opening> event handler examines the <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.ToolStripItem.OwnerItem%2A?displayProperty=nameWithType> properties and adds a <xref:System.Windows.Forms.ToolStripItem> describing the source control.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#40)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#40)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5369a-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5369a-109">Compiling the Code</span></span>  
 <span data-ttu-id="5369a-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="5369a-110">This example requires:</span></span>  
  
- <span data-ttu-id="5369a-111">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="5369a-111">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="5369a-112">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="5369a-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="5369a-113">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="5369a-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5369a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5369a-114">See also</span></span>

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- [<span data-ttu-id="5369a-115">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="5369a-115">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
