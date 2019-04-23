---
title: 'Procédure : personnaliser les couleurs dans des applications ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], customizing colors
- colors [Windows Forms], customizing in ToolStrip controls [Windows Forms]
- ToolStrip control [Windows Forms], custom colors
ms.assetid: e2752fe2-1afb-489e-ab96-b7805acd96bc
ms.openlocfilehash: 4d051085bdba41b9784d3dd7f921189c1300daf0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59980549"
---
# <a name="how-to-customize-colors-in-toolstrip-applications"></a><span data-ttu-id="0fa89-102">Procédure : personnaliser les couleurs dans des applications ToolStrip</span><span class="sxs-lookup"><span data-stu-id="0fa89-102">How to: Customize Colors in ToolStrip Applications</span></span>
<span data-ttu-id="0fa89-103">Vous pouvez personnaliser l'apparence de votre <xref:System.Windows.Forms.ToolStrip> en utilisant la classe <xref:System.Windows.Forms.ToolStripProfessionalRenderer> pour appliquer des couleurs personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0fa89-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> by using the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class to use customized colors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0fa89-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0fa89-104">Example</span></span>  
 <span data-ttu-id="0fa89-105">L'exemple de code suivant montre comment utiliser un <xref:System.Windows.Forms.ToolStripProfessionalRenderer> pour définir des couleurs personnalisées au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="0fa89-105">The following code example demonstrates how to use a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> to define custom colors at run time.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#20)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#20)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0fa89-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0fa89-106">Compiling the Code</span></span>  
 <span data-ttu-id="0fa89-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0fa89-107">This example requires:</span></span>  
  
-   <span data-ttu-id="0fa89-108">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="0fa89-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="0fa89-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="0fa89-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="0fa89-110">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="0fa89-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fa89-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fa89-111">See also</span></span>

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.ProfessionalColorTable>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
