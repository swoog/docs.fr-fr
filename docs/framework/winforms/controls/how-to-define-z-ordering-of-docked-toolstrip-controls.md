---
title: 'Procédure : Définir l’ordre Z de contrôles ToolStrip ancrés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], specifying z-order
- z-order
ms.assetid: 8b595429-ba9f-46af-9c55-3d5cc53f7fff
ms.openlocfilehash: 1ae7e6f63488d2dbb6b408cdf255f111f929298f
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722661"
---
# <a name="how-to-define-z-ordering-of-docked-toolstrip-controls"></a><span data-ttu-id="e1b3e-102">Procédure : Définir l’ordre Z de contrôles ToolStrip ancrés</span><span class="sxs-lookup"><span data-stu-id="e1b3e-102">How to: Define Z-Ordering of Docked ToolStrip Controls</span></span>
<span data-ttu-id="e1b3e-103">Pour positionner un contrôle <xref:System.Windows.Forms.ToolStrip> correctement avec l'ancrage, vous devez positionner le contrôle correctement dans l'ordre de plan du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-103">To position a <xref:System.Windows.Forms.ToolStrip> control correctly with docking, you must position the control correctly in the form's z-order.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e1b3e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1b3e-104">Example</span></span>  
 <span data-ttu-id="e1b3e-105">L'exemple de code suivant montre comment organiser un contrôle <xref:System.Windows.Forms.ToolStrip> et un contrôle <xref:System.Windows.Forms.MenuStrip> ancré en spécifiant l'ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-105">The following code example demonstrates how to arrange a <xref:System.Windows.Forms.ToolStrip> control and a docked <xref:System.Windows.Forms.MenuStrip> control by specifying the z-order.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#21)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#21)]  
  
 <span data-ttu-id="e1b3e-106">L'ordre de plan est déterminé par l'ordre dans lequel les contrôles <xref:System.Windows.Forms.ToolStrip> et <xref:System.Windows.Forms.MenuStrip></span><span class="sxs-lookup"><span data-stu-id="e1b3e-106">The z-order is determined by the order in which the <xref:System.Windows.Forms.ToolStrip> and <xref:System.Windows.Forms.MenuStrip></span></span>  
  
 <span data-ttu-id="e1b3e-107">sont ajoutés à la collection <xref:System.Windows.Forms.Control.Controls%2A> du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-107">controls are added to the form's <xref:System.Windows.Forms.Control.Controls%2A> collection.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#23)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#23)]  
  
 <span data-ttu-id="e1b3e-108">Inversez l'ordre de ces appels à la méthode <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> et observez l'effet sur la disposition.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-108">Reverse the order of these calls to the <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> method and view the effect on the layout.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e1b3e-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e1b3e-109">Compiling the Code</span></span>  
 <span data-ttu-id="e1b3e-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="e1b3e-110">This example requires:</span></span>  
  
-   <span data-ttu-id="e1b3e-111">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-111">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="e1b3e-112">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="e1b3e-112">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="e1b3e-113">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="e1b3e-113">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1b3e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1b3e-114">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.Control.ControlCollection.Add%2A>
- <xref:System.Windows.Forms.Control.Controls%2A>
- <xref:System.Windows.Forms.Control.Dock%2A>
- [<span data-ttu-id="e1b3e-115">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="e1b3e-115">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
