---
title: 'Procédure : Personnaliser les couleurs dans les Applications ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], customizing colors
- colors [Windows Forms], customizing in ToolStrip controls [Windows Forms]
- ToolStrip control [Windows Forms], custom colors
ms.assetid: e2752fe2-1afb-489e-ab96-b7805acd96bc
ms.openlocfilehash: 0a7679624d375fac610f6c74f124881d7235eab8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585430"
---
# <a name="how-to-customize-colors-in-toolstrip-applications"></a><span data-ttu-id="eb5c3-102">Procédure : Personnaliser les couleurs dans les Applications ToolStrip</span><span class="sxs-lookup"><span data-stu-id="eb5c3-102">How to: Customize Colors in ToolStrip Applications</span></span>
<span data-ttu-id="eb5c3-103">Vous pouvez personnaliser l'apparence de votre <xref:System.Windows.Forms.ToolStrip> en utilisant la classe <xref:System.Windows.Forms.ToolStripProfessionalRenderer> pour appliquer des couleurs personnalisées.</span><span class="sxs-lookup"><span data-stu-id="eb5c3-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> by using the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class to use customized colors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb5c3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb5c3-104">Example</span></span>  
 <span data-ttu-id="eb5c3-105">L'exemple de code suivant montre comment utiliser un <xref:System.Windows.Forms.ToolStripProfessionalRenderer> pour définir des couleurs personnalisées au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="eb5c3-105">The following code example demonstrates how to use a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> to define custom colors at run time.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#20](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#20)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#20](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#20)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="eb5c3-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="eb5c3-106">Compiling the Code</span></span>  
 <span data-ttu-id="eb5c3-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="eb5c3-107">This example requires:</span></span>  
  
-   <span data-ttu-id="eb5c3-108">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="eb5c3-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="eb5c3-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="eb5c3-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="eb5c3-110">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="eb5c3-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="eb5c3-111">Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="eb5c3-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb5c3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb5c3-112">See also</span></span>
- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.ProfessionalColorTable>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
