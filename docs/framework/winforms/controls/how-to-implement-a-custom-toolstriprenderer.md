---
title: 'Procédure : implémenter un ToolStripRenderer personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: c66fd3f7-2377-4553-8f1b-006527f08f32
ms.openlocfilehash: ec74528ecb3d2ca1fca78c3a81e71a0093843b4d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64651656"
---
# <a name="how-to-implement-a-custom-toolstriprenderer"></a><span data-ttu-id="9d43f-102">Procédure : implémenter un ToolStripRenderer personnalisé</span><span class="sxs-lookup"><span data-stu-id="9d43f-102">How to: Implement a Custom ToolStripRenderer</span></span>
<span data-ttu-id="9d43f-103">Vous pouvez personnaliser l'apparence d'un contrôle <xref:System.Windows.Forms.ToolStrip> en implémentant une classe qui dérive de <xref:System.Windows.Forms.ToolStripRenderer>.</span><span class="sxs-lookup"><span data-stu-id="9d43f-103">You can customize the appearance of a <xref:System.Windows.Forms.ToolStrip> control by implementing a class that derives from <xref:System.Windows.Forms.ToolStripRenderer>.</span></span> <span data-ttu-id="9d43f-104">Cela offre la flexibilité nécessaire pour créer une apparence qui diffère de celle fournie par les classes <xref:System.Windows.Forms.ToolStripProfessionalRenderer> et <xref:System.Windows.Forms.ToolStripSystemRenderer>.</span><span class="sxs-lookup"><span data-stu-id="9d43f-104">This gives you the flexibility to create an appearance that differs from the appearance provided the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> and <xref:System.Windows.Forms.ToolStripSystemRenderer> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9d43f-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d43f-105">Example</span></span>  
 <span data-ttu-id="9d43f-106">L'exemple de code suivant montre comment implémenter une classe <xref:System.Windows.Forms.ToolStripRenderer> personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9d43f-106">The following code example demonstrates how to implement a custom <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span> <span data-ttu-id="9d43f-107">Dans cet exemple, le contrôle `GridStrip` implémente un puzzle à mosaïques coulissantes qui permet à l'utilisateur de déplacer des mosaïques dans une disposition de table pour former une image.</span><span class="sxs-lookup"><span data-stu-id="9d43f-107">In this example, the `GridStrip` control implements a sliding-tile puzzle, which allows the user to move tiles in a table layout to form an image.</span></span> <span data-ttu-id="9d43f-108">Un contrôle <xref:System.Windows.Forms.ToolStrip> personnalisé réorganise ses contrôles <xref:System.Windows.Forms.ToolStripButton> dans une disposition de grille.</span><span class="sxs-lookup"><span data-stu-id="9d43f-108">A custom <xref:System.Windows.Forms.ToolStrip> control arranges its <xref:System.Windows.Forms.ToolStripButton> controls in a grid layout.</span></span> <span data-ttu-id="9d43f-109">La disposition contient une cellule vide, dans laquelle l'utilisateur peut glisser une mosaïque adjacente à l'aide d'une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="9d43f-109">The layout contains one empty cell, into which the user can slide an adjacent tile by using a drag-and-drop operation.</span></span> <span data-ttu-id="9d43f-110">Les mosaïques que l'utilisateur peut déplacer sont mises en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="9d43f-110">Tiles that the user can move are highlighted.</span></span>  
  
 <span data-ttu-id="9d43f-111">La classe `GridStripRenderer` personnalise trois aspects de l'apparence du contrôle `GridStrip` :</span><span class="sxs-lookup"><span data-stu-id="9d43f-111">The `GridStripRenderer` class customizes three aspects of the `GridStrip` control's appearance:</span></span>  
  
- <span data-ttu-id="9d43f-112">la bordure `GridStrip` ;</span><span class="sxs-lookup"><span data-stu-id="9d43f-112">`GridStrip` border</span></span>  
  
- <span data-ttu-id="9d43f-113">la bordure <xref:System.Windows.Forms.ToolStripButton> ;</span><span class="sxs-lookup"><span data-stu-id="9d43f-113"><xref:System.Windows.Forms.ToolStripButton> border</span></span>  
  
- <span data-ttu-id="9d43f-114">l'image <xref:System.Windows.Forms.ToolStripButton>.</span><span class="sxs-lookup"><span data-stu-id="9d43f-114"><xref:System.Windows.Forms.ToolStripButton> image</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.GridStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/CS/GridStrip.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.GridStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.GridStrip/VB/GridStrip.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9d43f-115">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9d43f-115">Compiling the Code</span></span>  
 <span data-ttu-id="9d43f-116">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="9d43f-116">This example requires:</span></span>  
  
- <span data-ttu-id="9d43f-117">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="9d43f-117">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="9d43f-118">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="9d43f-118">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="9d43f-119">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="9d43f-119">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d43f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d43f-120">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripRenderer>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- <xref:System.Windows.Forms.ToolStripSystemRenderer>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="9d43f-121">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="9d43f-121">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
