---
title: Ellipses et arcs dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- arcs
- GDI+, arcs
- drawing [Windows Forms], ellipses
- GDI+, ellipses
- ellipses
- drawing [Windows Forms], arcs
ms.assetid: 34f35133-a835-4ca4-81f6-0dfedee8b683
ms.openlocfilehash: 9f6969f9ad838ae913f049c4fc65d987e1aff9fa
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718478"
---
# <a name="ellipses-and-arcs-in-gdi"></a><span data-ttu-id="cc272-102">Ellipses et arcs dans GDI+</span><span class="sxs-lookup"><span data-stu-id="cc272-102">Ellipses and Arcs in GDI+</span></span>
<span data-ttu-id="cc272-103">Vous pouvez facilement dessiner des ellipses et arcs à l’aide de la <xref:System.Drawing.Graphics.DrawEllipse%2A> et <xref:System.Drawing.Graphics.DrawArc%2A> méthodes de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="cc272-103">You can easily draw ellipses and arcs using the <xref:System.Drawing.Graphics.DrawEllipse%2A> and <xref:System.Drawing.Graphics.DrawArc%2A> methods of the <xref:System.Drawing.Graphics> class.</span></span>  
  
## <a name="drawing-an-ellipse"></a><span data-ttu-id="cc272-104">Dessiner une Ellipse</span><span class="sxs-lookup"><span data-stu-id="cc272-104">Drawing an Ellipse</span></span>  
 <span data-ttu-id="cc272-105">Pour dessiner une ellipse, vous avez besoin une <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="cc272-105">To draw an ellipse, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="cc272-106">Le <xref:System.Drawing.Graphics> objet fournit les <xref:System.Drawing.Graphics.DrawEllipse%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour représenter l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="cc272-106">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawEllipse%2A> method, and the <xref:System.Drawing.Pen> object stores attributes, such as width and color, of the line used to render the ellipse.</span></span> <span data-ttu-id="cc272-107">Le <xref:System.Drawing.Pen> objet est passé en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawEllipse%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="cc272-107">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method.</span></span> <span data-ttu-id="cc272-108">Les autres arguments passés à la <xref:System.Drawing.Graphics.DrawEllipse%2A> méthode définissent le rectangle englobant de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="cc272-108">The remaining arguments passed to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="cc272-109">L’illustration suivante montre une ellipse, ainsi que son rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="cc272-109">The following illustration shows an ellipse along with its bounding rectangle.</span></span>  
  
 <span data-ttu-id="cc272-110">![Ellipses et arcs](./media/aboutgdip02-art05.gif "Aboutgdip02_art05")</span><span class="sxs-lookup"><span data-stu-id="cc272-110">![Ellipses and arcs](./media/aboutgdip02-art05.gif "Aboutgdip02_art05")</span></span>  
  
 <span data-ttu-id="cc272-111">L’exemple suivant dessine une ellipse ; le rectangle englobant a une largeur de 80, une hauteur de 40 et un coin supérieur gauche de (100, 50) :</span><span class="sxs-lookup"><span data-stu-id="cc272-111">The following example draws an ellipse; the bounding rectangle has a width of 80, a height of 40, and an upper-left corner of (100, 50):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#51](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#51)]
 [!code-vb[LinesCurvesAndShapes#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#51)]  
  
 <span data-ttu-id="cc272-112"><xref:System.Drawing.Graphics.DrawEllipse%2A> est une méthode surchargée de la <xref:System.Drawing.Graphics> classe, il existe plusieurs façons, vous pouvez lui fournir arguments.</span><span class="sxs-lookup"><span data-stu-id="cc272-112"><xref:System.Drawing.Graphics.DrawEllipse%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="cc272-113">Par exemple, vous pouvez construire un <xref:System.Drawing.Rectangle> et passer le <xref:System.Drawing.Rectangle> à la <xref:System.Drawing.Graphics.DrawEllipse%2A> méthode en tant qu’argument :</span><span class="sxs-lookup"><span data-stu-id="cc272-113">For example, you can construct a <xref:System.Drawing.Rectangle> and pass the <xref:System.Drawing.Rectangle> to the <xref:System.Drawing.Graphics.DrawEllipse%2A> method as an argument:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#52](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#52)]
 [!code-vb[LinesCurvesAndShapes#52](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#52)]  
  
## <a name="drawing-an-arc"></a><span data-ttu-id="cc272-114">Dessiner un Arc</span><span class="sxs-lookup"><span data-stu-id="cc272-114">Drawing an Arc</span></span>  
 <span data-ttu-id="cc272-115">Un arc est une partie d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="cc272-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="cc272-116">Pour dessiner un arc, vous appelez le <xref:System.Drawing.Graphics.DrawArc%2A> méthode de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="cc272-116">To draw an arc, you call the <xref:System.Drawing.Graphics.DrawArc%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="cc272-117">Les paramètres de la <xref:System.Drawing.Graphics.DrawArc%2A> méthode sont les mêmes que les paramètres de la <xref:System.Drawing.Graphics.DrawEllipse%2A> (méthode), à ceci près que <xref:System.Drawing.Graphics.DrawArc%2A> nécessite un angle de départ et un angle de balayage.</span><span class="sxs-lookup"><span data-stu-id="cc272-117">The parameters of the <xref:System.Drawing.Graphics.DrawArc%2A> method are the same as the parameters of the <xref:System.Drawing.Graphics.DrawEllipse%2A> method, except that <xref:System.Drawing.Graphics.DrawArc%2A> requires a starting angle and sweep angle.</span></span> <span data-ttu-id="cc272-118">L’exemple suivant dessine un arc avec un angle de 30 degrés de départ et un angle de balayage de 180 degrés :</span><span class="sxs-lookup"><span data-stu-id="cc272-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#53](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#53)]
 [!code-vb[LinesCurvesAndShapes#53](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#53)]  
  
 <span data-ttu-id="cc272-119">L’illustration suivante montre l’arc, l’ellipse et le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="cc272-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>  
  
 <span data-ttu-id="cc272-120">![Ellipses et arcs](./media/aboutgdip02-art06.gif "Aboutgdip02_art06")</span><span class="sxs-lookup"><span data-stu-id="cc272-120">![Ellipses and arcs](./media/aboutgdip02-art06.gif "Aboutgdip02_art06")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc272-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc272-121">See also</span></span>
- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="cc272-122">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="cc272-122">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="cc272-123">Guide pratique pour Créer des objets graphiques pour le dessin</span><span class="sxs-lookup"><span data-stu-id="cc272-123">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="cc272-124">Guide pratique pour Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="cc272-124">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
- [<span data-ttu-id="cc272-125">Guide pratique pour Dessiner une forme avec contour</span><span class="sxs-lookup"><span data-stu-id="cc272-125">How to: Draw an Outlined Shape</span></span>](how-to-draw-an-outlined-shape.md)
