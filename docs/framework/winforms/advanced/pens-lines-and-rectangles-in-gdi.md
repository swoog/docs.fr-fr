---
title: Stylets, lignes et rectangles dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines
- GDI+, lines
- drawing [Windows Forms], rectangles
- rectangles
- drawing [Windows Forms], lines
- GDI+, pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- GDI+, rectangles
- examples [Windows Forms], GDI+
- lines [Windows Forms], dashed
ms.assetid: 30b25aae-e3eb-4479-bdb8-187cf651fc84
ms.openlocfilehash: 84752773c0b56d9684dc31620d463d4ddccf9dad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61641395"
---
# <a name="pens-lines-and-rectangles-in-gdi"></a><span data-ttu-id="4a3aa-102">Stylets, lignes et rectangles dans GDI+</span><span class="sxs-lookup"><span data-stu-id="4a3aa-102">Pens, Lines, and Rectangles in GDI+</span></span>
<span data-ttu-id="4a3aa-103">Pour dessiner des lignes avec [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] vous devez créer un <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-103">To draw lines with [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] you need to create a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="4a3aa-104">Le <xref:System.Drawing.Graphics> objet fournit les méthodes qui effectuent réellement le dessin, et le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la couleur de ligne, la largeur et le style.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-104">The <xref:System.Drawing.Graphics> object provides the methods that actually do the drawing, and the <xref:System.Drawing.Pen> object stores attributes, such as line color, width, and style.</span></span>  
  
## <a name="drawing-a-line"></a><span data-ttu-id="4a3aa-105">Dessiner une ligne</span><span class="sxs-lookup"><span data-stu-id="4a3aa-105">Drawing a Line</span></span>  
 <span data-ttu-id="4a3aa-106">Pour dessiner une ligne, appelez le <xref:System.Drawing.Graphics.DrawLine%2A> méthode de la <xref:System.Drawing.Graphics> objet.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-106">To draw a line, call the <xref:System.Drawing.Graphics.DrawLine%2A> method of the <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="4a3aa-107">Le <xref:System.Drawing.Pen> objet est passé en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawLine%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4a3aa-107">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawLine%2A> method.</span></span> <span data-ttu-id="4a3aa-108">L’exemple suivant dessine une ligne à partir du point (4, 2) au point (12, 6) :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-108">The following example draws a line from the point (4, 2) to the point (12, 6):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#41](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#41)]
 [!code-vb[LinesCurvesAndShapes#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#41)]  
  
 <span data-ttu-id="4a3aa-109"><xref:System.Drawing.Graphics.DrawLine%2A> est une méthode surchargée de la <xref:System.Drawing.Graphics> classe, il existe plusieurs façons, vous pouvez lui fournir arguments.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-109"><xref:System.Drawing.Graphics.DrawLine%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="4a3aa-110">Par exemple, vous pouvez construire deux <xref:System.Drawing.Point> objets et passez le <xref:System.Drawing.Point> en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawLine%2A> méthode :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-110">For example, you can construct two <xref:System.Drawing.Point> objects and pass the <xref:System.Drawing.Point> objects as arguments to the <xref:System.Drawing.Graphics.DrawLine%2A> method:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#42](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#42)]
 [!code-vb[LinesCurvesAndShapes#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#42)]  
  
## <a name="constructing-a-pen"></a><span data-ttu-id="4a3aa-111">Construction d’un stylet</span><span class="sxs-lookup"><span data-stu-id="4a3aa-111">Constructing a Pen</span></span>  
 <span data-ttu-id="4a3aa-112">Vous pouvez spécifier certains attributs lorsque vous construisez un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-112">You can specify certain attributes when you construct a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="4a3aa-113">Par exemple, un `Pen` constructeur vous permet de spécifier la couleur et la largeur.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-113">For example, one `Pen` constructor allows you to specify color and width.</span></span> <span data-ttu-id="4a3aa-114">L’exemple suivant dessine une ligne bleue de largeur 2 à partir de (0, 0) à (60, 30) :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-114">The following example draws a blue line of width 2 from (0, 0) to (60, 30):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#43](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#43)]
 [!code-vb[LinesCurvesAndShapes#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#43)]  
  
## <a name="dashed-lines-and-line-caps"></a><span data-ttu-id="4a3aa-115">Lignes en pointillés et embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="4a3aa-115">Dashed Lines and Line Caps</span></span>  
 <span data-ttu-id="4a3aa-116">Le <xref:System.Drawing.Pen> objet expose également des propriétés, telles que <xref:System.Drawing.Pen.DashStyle%2A>, que vous pouvez utiliser pour spécifier les fonctionnalités de la ligne.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-116">The <xref:System.Drawing.Pen> object also exposes properties, such as <xref:System.Drawing.Pen.DashStyle%2A>, that you can use to specify features of the line.</span></span> <span data-ttu-id="4a3aa-117">L’exemple suivant dessine une ligne en pointillés à partir de (100, 50) à (300, 80) :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-117">The following example draws a dashed line from (100, 50) to (300, 80):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#44](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#44)]
 [!code-vb[LinesCurvesAndShapes#44](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#44)]  
  
 <span data-ttu-id="4a3aa-118">Vous pouvez utiliser les propriétés de la <xref:System.Drawing.Pen> objet à définir beaucoup d’autres attributs de la ligne.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-118">You can use the properties of the <xref:System.Drawing.Pen> object to set many more attributes of the line.</span></span> <span data-ttu-id="4a3aa-119">Le <xref:System.Drawing.Pen.StartCap%2A> et <xref:System.Drawing.Pen.EndCap%2A> propriétés spécifient l’apparence des extrémités de la ligne ; les extrémités peuvent être plat, carré, arrondi, triangulaire, ou une forme personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-119">The <xref:System.Drawing.Pen.StartCap%2A> and <xref:System.Drawing.Pen.EndCap%2A> properties specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="4a3aa-120">Le <xref:System.Drawing.Pen.LineJoin%2A> propriété vous permet de spécifier si les lignes reliées entre elles forment (jointes avec des angles aigus), en relief, arrondis ou découpés.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-120">The <xref:System.Drawing.Pen.LineJoin%2A> property lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="4a3aa-121">L’illustration suivante montre les lignes avec différents styles d’extrémité et de jointure.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-121">The following illustration shows lines with various cap and join styles.</span></span>  
  
 <span data-ttu-id="4a3aa-122">![Lines](./media/aboutgdip02-art04.gif "Aboutgdip02_art04")</span><span class="sxs-lookup"><span data-stu-id="4a3aa-122">![Lines](./media/aboutgdip02-art04.gif "Aboutgdip02_art04")</span></span>  
  
## <a name="drawing-a-rectangle"></a><span data-ttu-id="4a3aa-123">Dessin d’un Rectangle</span><span class="sxs-lookup"><span data-stu-id="4a3aa-123">Drawing a Rectangle</span></span>  
 <span data-ttu-id="4a3aa-124">Dessiner des rectangles avec [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] est similaire au dessin de lignes.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-124">Drawing rectangles with [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] is similar to drawing lines.</span></span> <span data-ttu-id="4a3aa-125">Pour dessiner un rectangle, vous avez besoin une <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-125">To draw a rectangle, you need a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="4a3aa-126">Le <xref:System.Drawing.Graphics> objet fournit un <xref:System.Drawing.Graphics.DrawRectangle%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la largeur de ligne et la couleur.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-126">The <xref:System.Drawing.Graphics> object provides a <xref:System.Drawing.Graphics.DrawRectangle%2A> method, and the <xref:System.Drawing.Pen> object stores attributes, such as line width and color.</span></span> <span data-ttu-id="4a3aa-127">Le <xref:System.Drawing.Pen> objet est passé en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawRectangle%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4a3aa-127">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawRectangle%2A> method.</span></span> <span data-ttu-id="4a3aa-128">L’exemple suivant dessine un rectangle avec son coin supérieur gauche à (100, 50), une largeur de 80 et une hauteur de 40 :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-128">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#45](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#45)]
 [!code-vb[LinesCurvesAndShapes#45](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#45)]  
  
 <span data-ttu-id="4a3aa-129"><xref:System.Drawing.Graphics.DrawRectangle%2A> est une méthode surchargée de la <xref:System.Drawing.Graphics> classe, il existe plusieurs façons, vous pouvez lui fournir arguments.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-129"><xref:System.Drawing.Graphics.DrawRectangle%2A> is an overloaded method of the <xref:System.Drawing.Graphics> class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="4a3aa-130">Par exemple, vous pouvez construire un <xref:System.Drawing.Rectangle> de l’objet et de transmettre le <xref:System.Drawing.Rectangle> de l’objet à la <xref:System.Drawing.Graphics.DrawRectangle%2A> méthode en tant qu’argument :</span><span class="sxs-lookup"><span data-stu-id="4a3aa-130">For example, you can construct a <xref:System.Drawing.Rectangle> object and pass the <xref:System.Drawing.Rectangle> object to the <xref:System.Drawing.Graphics.DrawRectangle%2A> method as an argument:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#46](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#46)]
 [!code-vb[LinesCurvesAndShapes#46](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#46)]  
  
 <span data-ttu-id="4a3aa-131">Un <xref:System.Drawing.Rectangle> objet possède des méthodes et propriétés permettant de manipuler et de collecter des informations sur le rectangle.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-131">A <xref:System.Drawing.Rectangle> object has methods and properties for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="4a3aa-132">Par exemple, le <xref:System.Drawing.Rectangle.Inflate%2A> et <xref:System.Drawing.Rectangle.Offset%2A> les méthodes de modifier la taille et la position du rectangle.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-132">For example, the <xref:System.Drawing.Rectangle.Inflate%2A> and <xref:System.Drawing.Rectangle.Offset%2A> methods change the size and position of the rectangle.</span></span> <span data-ttu-id="4a3aa-133">Le <xref:System.Drawing.Rectangle.IntersectsWith%2A> méthode vous indique si le rectangle coupe un rectangle donné et la <xref:System.Drawing.Rectangle.Contains%2A> méthode vous indique si un point donné se trouve à l’intérieur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="4a3aa-133">The <xref:System.Drawing.Rectangle.IntersectsWith%2A> method tells you whether the rectangle intersects another given rectangle, and the <xref:System.Drawing.Rectangle.Contains%2A> method tells you whether a given point is inside the rectangle.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a3aa-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a3aa-134">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Rectangle?displayProperty=nameWithType>
- [<span data-ttu-id="4a3aa-135">Guide pratique pour Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="4a3aa-135">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
- [<span data-ttu-id="4a3aa-136">Guide pratique pour Dessiner une ligne dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="4a3aa-136">How to: Draw a Line on a Windows Form</span></span>](how-to-draw-a-line-on-a-windows-form.md)
- [<span data-ttu-id="4a3aa-137">Guide pratique pour Dessiner une forme avec contour</span><span class="sxs-lookup"><span data-stu-id="4a3aa-137">How to: Draw an Outlined Shape</span></span>](how-to-draw-an-outlined-shape.md)
