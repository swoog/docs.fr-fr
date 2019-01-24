---
title: 'Procédure : Configuration de la vérification MenuStrip marges de sélection et Image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- margins [Windows Forms], setting in MenuStrip controls
- menus [Windows Forms], setting margins
- MenuStrip control [Windows Forms], configuring check and image margins
ms.assetid: 45a9075d-4bea-4ce2-9b2c-7619aa39f8ce
ms.openlocfilehash: 49c228fef387a7c2a18cf8cecd5081e7b5519ab3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54530773"
---
# <a name="how-to-configure-menustrip-check-margins-and-image-margins"></a><span data-ttu-id="cdee6-102">Procédure : Configuration de la vérification MenuStrip marges de sélection et Image</span><span class="sxs-lookup"><span data-stu-id="cdee6-102">How to: Configure MenuStrip Check Margins and Image Margins</span></span>
<span data-ttu-id="cdee6-103">Vous pouvez personnaliser un <xref:System.Windows.Forms.MenuStrip> en définissant les propriétés <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A> et <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A> dans différentes combinaisons.</span><span class="sxs-lookup"><span data-stu-id="cdee6-103">You can customize a <xref:System.Windows.Forms.MenuStrip> by setting the <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A> and <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A> properties in various combinations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cdee6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cdee6-104">Example</span></span>  
 <span data-ttu-id="cdee6-105">L'exemple de code suivant montre comment définir et personnaliser les marges d'image et de sélection de <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="cdee6-105">The following code example demonstrates how to set and customize the <xref:System.Windows.Forms.ContextMenuStrip> check margins and image margins.</span></span> <span data-ttu-id="cdee6-106">La procédure est identique pour <xref:System.Windows.Forms.ContextMenuStrip> et <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="cdee6-106">The procedure is the same for a <xref:System.Windows.Forms.ContextMenuStrip> or a <xref:System.Windows.Forms.MenuStrip>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#60](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="cdee6-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="cdee6-107">Compiling the Code</span></span>  
 <span data-ttu-id="cdee6-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="cdee6-108">This example requires:</span></span>  
  
-   <span data-ttu-id="cdee6-109">des références aux assemblys System, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="cdee6-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="cdee6-110">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="cdee6-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="cdee6-111">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="cdee6-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="cdee6-112">Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="cdee6-112">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdee6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdee6-113">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [<span data-ttu-id="cdee6-114">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="cdee6-114">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
- [<span data-ttu-id="cdee6-115">Guide pratique pour Activer les marges de sélection et Image dans les contrôles ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="cdee6-115">How to: Enable Check Margins and Image Margins in ContextMenuStrip Controls</span></span>](../../../../docs/framework/winforms/controls/how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls.md)
