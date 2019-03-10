---
title: 'Procédure : Dessiner une ligne avec des embouts de ligne'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
- drawing lines [Windows Forms], line caps
ms.assetid: eb68c3e1-c400-4886-8a04-76978a429cb6
ms.openlocfilehash: 05c678b25563eb7a4e2e5ce0e49138b5445b4764
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707597"
---
# <a name="how-to-draw-a-line-with-line-caps"></a><span data-ttu-id="ccc24-102">Procédure : Dessiner une ligne avec des embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="ccc24-102">How to: Draw a Line with Line Caps</span></span>
<span data-ttu-id="ccc24-103">Vous pouvez dessiner le début ou la fin d’une ligne dans plusieurs formes appelé embouts de ligne.</span><span class="sxs-lookup"><span data-stu-id="ccc24-103">You can draw the start or end of a line in one of several shapes called line caps.</span></span> [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="ccc24-104">prend en charge plusieurs embouts de ligne, tels que round, carré, losange et pointe de flèche.</span><span class="sxs-lookup"><span data-stu-id="ccc24-104">supports several line caps, such as round, square, diamond, and arrowhead.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ccc24-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="ccc24-105">Example</span></span>  
 <span data-ttu-id="ccc24-106">Vous pouvez spécifier des embouts de ligne pour le début d’une ligne (extrémité de début), la fin d’une ligne (extrémité de fin) ou les tirets d’une ligne en pointillés (cap dash).</span><span class="sxs-lookup"><span data-stu-id="ccc24-106">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>  
  
 <span data-ttu-id="ccc24-107">L’exemple suivant dessine une ligne avec une pointe de flèche à une extrémité et une extrémité arrondie à l’autre extrémité.</span><span class="sxs-lookup"><span data-stu-id="ccc24-107">The following example draws a line with an arrowhead at one end and a round cap at the other end.</span></span> <span data-ttu-id="ccc24-108">L’illustration montre la ligne résultante :</span><span class="sxs-lookup"><span data-stu-id="ccc24-108">The illustration shows the resulting line:</span></span>  
  
 <span data-ttu-id="ccc24-109">![Stylets](./media/pens4.gif "pens4")</span><span class="sxs-lookup"><span data-stu-id="ccc24-109">![Pens](./media/pens4.gif "pens4")</span></span>  
  
 [!code-csharp[System.Drawing.UsingAPen#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.UsingAPen#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ccc24-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="ccc24-110">Compiling the Code</span></span>  
  
-   <span data-ttu-id="ccc24-111">Créer un formulaire Windows et de gérer le formulaire <xref:System.Windows.Forms.Control.Paint> événement.</span><span class="sxs-lookup"><span data-stu-id="ccc24-111">Create a Windows Form and handle the form's <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="ccc24-112">Collez l’exemple de code dans le <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements en passant `e` comme <xref:System.Windows.Forms.PaintEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="ccc24-112">Paste the example code into the <xref:System.Windows.Forms.Control.Paint> event handler passing `e` as <xref:System.Windows.Forms.PaintEventArgs>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccc24-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccc24-113">See also</span></span>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LineCap?displayProperty=nameWithType>
- [<span data-ttu-id="ccc24-114">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ccc24-114">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="ccc24-115">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="ccc24-115">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
