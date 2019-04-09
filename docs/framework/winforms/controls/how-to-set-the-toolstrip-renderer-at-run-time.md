---
title: 'Procédure : définir le renderer ToolStrip au moment de l’exécution'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripManager class [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: 525e2347-0804-49aa-b9a3-9b2cabbf1c35
ms.openlocfilehash: f0e8668ef46de8cc073663786bcd43b740a1b2f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138579"
---
# <a name="how-to-set-the-toolstrip-renderer-at-run-time"></a><span data-ttu-id="cf687-102">Procédure : définir le renderer ToolStrip au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="cf687-102">How to: Set the ToolStrip Renderer at Run Time</span></span>
<span data-ttu-id="cf687-103">Vous pouvez personnaliser l'apparence de votre contrôle <xref:System.Windows.Forms.ToolStrip> en créant une classe `ProfessionalColorTable` personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cf687-103">You can customize the appearance of your <xref:System.Windows.Forms.ToolStrip> control by creating a custom `ProfessionalColorTable` class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cf687-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cf687-104">Example</span></span>  
 <span data-ttu-id="cf687-105">L'exemple de code suivant montre comment créer une classe `ProfessionalColorTable` personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cf687-105">The following code example demonstrates how to create a custom `ProfessionalColorTable` class.</span></span> <span data-ttu-id="cf687-106">Cette classe définit des dégradés pour un <xref:System.Windows.Forms.MenuStrip> et un contrôle <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="cf687-106">This class defines gradients for a <xref:System.Windows.Forms.MenuStrip> and a <xref:System.Windows.Forms.ToolStrip> control.</span></span>  
  
 <span data-ttu-id="cf687-107">Pour utiliser cet exemple de code, compilez et exécutez l’application, puis cliquez sur **Change Colors** pour appliquer les dégradés définis dans la classe `ProfessionalColorTable` personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cf687-107">To use this code example, compile and run the application, and then click **Change Colors** to apply the gradients defined in the custom `ProfessionalColorTable` class.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#20)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#20)]  
  
## <a name="defining-a-custom-professionalcolortable-class"></a><span data-ttu-id="cf687-108">Définition d'une classe ProfessionalColorTable personnalisée</span><span class="sxs-lookup"><span data-stu-id="cf687-108">Defining a Custom ProfessionalColorTable class</span></span>  
 <span data-ttu-id="cf687-109">Les dégradés personnalisés sont définis dans la classe `CustomProfessionalColors`.</span><span class="sxs-lookup"><span data-stu-id="cf687-109">The custom gradients are defined in the `CustomProfessionalColors` class.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#30)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#30)]  
  
## <a name="assigning-a-custom-renderer"></a><span data-ttu-id="cf687-110">Affectation d'un convertisseur personnalisé</span><span class="sxs-lookup"><span data-stu-id="cf687-110">Assigning a Custom Renderer</span></span>  
 <span data-ttu-id="cf687-111">Créez un `ToolStripProfessionalRenderer` avec une classe `CustomProfessionalColors` et assignez-le à la propriété <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cf687-111">Create a new `ToolStripProfessionalRenderer` with a `CustomProfessionalColors` class, and assign it to the <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType> property.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#22)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#22)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="cf687-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="cf687-112">Compiling the Code</span></span>  
 <span data-ttu-id="cf687-113">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="cf687-113">This example requires:</span></span>  
  
-   <span data-ttu-id="cf687-114">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="cf687-114">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="cf687-115">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="cf687-115">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="cf687-116">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="cf687-116">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cf687-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf687-117">See also</span></span>

- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.ProfessionalColorTable>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- [<span data-ttu-id="cf687-118">ToolStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="cf687-118">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
