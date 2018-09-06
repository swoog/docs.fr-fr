---
title: 'Comment : créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: 64992ed9-44af-4baf-b45f-863e6ab35711
ms.openlocfilehash: b2f9f2886fe97e174092bdb35c6990fbf5ea60f7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43744365"
---
# <a name="how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a><span data-ttu-id="7ddaf-102">Comment : créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip</span><span class="sxs-lookup"><span data-stu-id="7ddaf-102">How to: Create an MDI Form with Menu Merging and ToolStrip Controls</span></span>
<span data-ttu-id="7ddaf-103">L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> prend en charge plusieurs applications MDI (Multiple Document Interface) et le contrôle <xref:System.Windows.Forms.MenuStrip> prend en charge la fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-103">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace supports multiple document interface (MDI) applications, and the <xref:System.Windows.Forms.MenuStrip> control supports menu merging.</span></span> <span data-ttu-id="7ddaf-104">Les formulaires MDI peuvent également contenir des contrôles <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-104">MDI forms can also <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="7ddaf-105">Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-105">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="7ddaf-106">Consultez également [Procédure pas à pas : création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7ddaf-106">Also see [Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7ddaf-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ddaf-107">Example</span></span>  
 <span data-ttu-id="7ddaf-108">L'exemple de code suivant montre comment utiliser des contrôles <xref:System.Windows.Forms.ToolStripPanel> avec un formulaire MDI.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-108">The following code example demonstrates how to use <xref:System.Windows.Forms.ToolStripPanel> controls with an MDI form.</span></span> <span data-ttu-id="7ddaf-109">Le formulaire prend également en charge la fusion de menus avec les menus enfants.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-109">The form also supports menu merging with child menus.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7ddaf-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="7ddaf-110">Compiling the Code</span></span>  
 <span data-ttu-id="7ddaf-111">Cet exemple de code nécessite :</span><span class="sxs-lookup"><span data-stu-id="7ddaf-111">This code example requires:</span></span>  
  
-   <span data-ttu-id="7ddaf-112">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-112">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="7ddaf-113">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="7ddaf-113">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="7ddaf-114">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="7ddaf-114">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="7ddaf-115">Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="7ddaf-115">Also sssee [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ddaf-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ddaf-116">See Also</span></span>  
 [<span data-ttu-id="7ddaf-117">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="7ddaf-117">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
