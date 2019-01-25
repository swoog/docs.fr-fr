---
title: 'Procédure : Implémenter un ToolStripRenderer personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c66fd3f7-2377-4553-8f1b-006527f08f32
ms.openlocfilehash: e99ffc45f3762ee816583a5294d56be30dfbff1a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577345"
---
# <a name="how-to-implement-a-custom-toolstriprenderer"></a><span data-ttu-id="89c95-102">Procédure : Implémenter un ToolStripRenderer personnalisé</span><span class="sxs-lookup"><span data-stu-id="89c95-102">How to: Implement a Custom ToolStripRenderer</span></span>
<span data-ttu-id="89c95-103">Vous pouvez personnaliser l'apparence d'un contrôle <xref:System.Windows.Forms.ToolStrip> en implémentant une classe qui dérive de <xref:System.Windows.Forms.ToolStripRenderer>.</span><span class="sxs-lookup"><span data-stu-id="89c95-103">You can customize the appearance of a <xref:System.Windows.Forms.ToolStrip> control by implementing a class that derives from <xref:System.Windows.Forms.ToolStripRenderer>.</span></span> <span data-ttu-id="89c95-104">Cela offre la flexibilité nécessaire pour créer une apparence qui diffère de celle fournie par les classes <xref:System.Windows.Forms.ToolStripProfessionalRenderer> et <xref:System.Windows.Forms.ToolStripSystemRenderer>.</span><span class="sxs-lookup"><span data-stu-id="89c95-104">This gives you the flexibility to create an appearance that differs from the appearance provided the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> and <xref:System.Windows.Forms.ToolStripSystemRenderer> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="89c95-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="89c95-105">Example</span></span>  
 <span data-ttu-id="89c95-106">L'exemple de code suivant montre comment implémenter une classe <xref:System.Windows.Forms.ToolStripRenderer> personnalisée.</span><span class="sxs-lookup"><span data-stu-id="89c95-106">The following code example demonstrates how to implement a custom <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span> <span data-ttu-id="89c95-107">Dans cet exemple, le contrôle `GridStrip` implémente un puzzle à mosaïques coulissantes qui permet à l'utilisateur de déplacer des mosaïques dans une disposition de table pour former une image.</span><span class="sxs-lookup"><span data-stu-id="89c95-107">In this example, the `GridStrip` control implements a sliding-tile puzzle, which allows the user to move tiles in a table layout to form an image.</span></span> <span data-ttu-id="89c95-108">Un contrôle <xref:System.Windows.Forms.ToolStrip> personnalisé réorganise ses contrôles <xref:System.Windows.Forms.ToolStripButton> dans une disposition de grille.</span><span class="sxs-lookup"><span data-stu-id="89c95-108">A custom <xref:System.Windows.Forms.ToolStrip> control arranges its <xref:System.Windows.Forms.ToolStripButton> controls in a grid layout.</span></span> <span data-ttu-id="89c95-109">La disposition contient une cellule vide, dans laquelle l'utilisateur peut glisser une mosaïque adjacente à l'aide d'une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="89c95-109">The layout contains one empty cell, into which the user can slide an adjacent tile by using a drag-and-drop operation.</span></span> <span data-ttu-id="89c95-110">Les mosaïques que l'utilisateur peut déplacer sont mises en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="89c95-110">Tiles that the user can move are highlighted.</span></span>  
  
 <span data-ttu-id="89c95-111">La classe `GridStripRenderer` personnalise trois aspects de l'apparence du contrôle `GridStrip` :</span><span class="sxs-lookup"><span data-stu-id="89c95-111">The `GridStripRenderer` class customizes three aspects of the `GridStrip` control's appearance:</span></span>  
  
-   <span data-ttu-id="89c95-112">la bordure `GridStrip` ;</span><span class="sxs-lookup"><span data-stu-id="89c95-112">`GridStrip` border</span></span>  
  
-   <span data-ttu-id="89c95-113">la bordure <xref:System.Windows.Forms.ToolStripButton> ;</span><span class="sxs-lookup"><span data-stu-id="89c95-113"><xref:System.Windows.Forms.ToolStripButton> border</span></span>  
  
-   <span data-ttu-id="89c95-114">l'image <xref:System.Windows.Forms.ToolStripButton>.</span><span class="sxs-lookup"><span data-stu-id="89c95-114"><xref:System.Windows.Forms.ToolStripButton> image</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/CS/GridStrip.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.GridStrip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/VB/GridStrip.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="89c95-115">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="89c95-115">Compiling the Code</span></span>  
 <span data-ttu-id="89c95-116">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="89c95-116">This example requires:</span></span>  
  
-   <span data-ttu-id="89c95-117">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="89c95-117">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="89c95-118">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="89c95-118">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="89c95-119">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="89c95-119">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="89c95-120">Voir également [Guide pratique pour Compiler et exécuter un exemple de Code complet de Windows Forms à l’aide de Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="89c95-120">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89c95-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89c95-121">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripRenderer>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- <xref:System.Windows.Forms.ToolStripSystemRenderer>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="89c95-122">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="89c95-122">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
