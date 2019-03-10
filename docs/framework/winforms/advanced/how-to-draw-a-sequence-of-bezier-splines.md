---
title: 'Procédure : Dessiner une séquence de B&#233;Splines de Bézier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], drawing Bezier
- Bezier splines [Windows Forms], drawing sequence of
ms.assetid: 37a0bedb-20c2-4cf0-91fa-a5509e826b30
ms.openlocfilehash: 1de2f44be189cb2ff874a748ae6093c945120178
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711788"
---
# <a name="how-to-draw-a-sequence-of-b233zier-splines"></a><span data-ttu-id="768e0-102">Procédure : Dessiner une séquence de B&#233;Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="768e0-102">How to: Draw a Sequence of B&#233;zier Splines</span></span>
<span data-ttu-id="768e0-103">Vous pouvez utiliser la <xref:System.Drawing.Graphics.DrawBeziers%2A> méthode de la <xref:System.Drawing.Graphics> classe pour dessiner une séquence de splines de Bézier reliées.</span><span class="sxs-lookup"><span data-stu-id="768e0-103">You can use the <xref:System.Drawing.Graphics.DrawBeziers%2A> method of the <xref:System.Drawing.Graphics> class to draw a sequence of connected Bézier splines.</span></span>  
  
## <a name="example"></a><span data-ttu-id="768e0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="768e0-104">Example</span></span>  
 <span data-ttu-id="768e0-105">L’exemple suivant dessine une courbe qui se compose de deux splines de Bézier connectées.</span><span class="sxs-lookup"><span data-stu-id="768e0-105">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="768e0-106">Le point de terminaison de la première spline de Bézier est le point de départ de la seconde.</span><span class="sxs-lookup"><span data-stu-id="768e0-106">The endpoint of the first Bézier spline is the start point of the second Bézier spline.</span></span>  
  
 <span data-ttu-id="768e0-107">L’illustration suivante montre les splines connectés, ainsi que les sept points.</span><span class="sxs-lookup"><span data-stu-id="768e0-107">The following illustration shows the connected splines along with the seven points.</span></span>  
  
 <span data-ttu-id="768e0-108">![Spline de Bézier](./media/bezierspline2.png "BezierSpline2")</span><span class="sxs-lookup"><span data-stu-id="768e0-108">![Bezier Spline](./media/bezierspline2.png "BezierSpline2")</span></span>  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="768e0-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="768e0-109">Compiling the Code</span></span>  
 <span data-ttu-id="768e0-110">L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.</span><span class="sxs-lookup"><span data-stu-id="768e0-110">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="768e0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="768e0-111">See also</span></span>
- [<span data-ttu-id="768e0-112">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="768e0-112">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="768e0-113">Splines de Bézier dans GDI+</span><span class="sxs-lookup"><span data-stu-id="768e0-113">Bézier Splines in GDI+</span></span>](bezier-splines-in-gdi.md)
- [<span data-ttu-id="768e0-114">Génération et dessin de courbes</span><span class="sxs-lookup"><span data-stu-id="768e0-114">Constructing and Drawing Curves</span></span>](constructing-and-drawing-curves.md)
