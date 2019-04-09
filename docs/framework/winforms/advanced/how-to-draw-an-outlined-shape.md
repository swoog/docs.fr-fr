---
title: 'Procédure : dessiner une forme avec contour'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.DrawEllipse
helpviewer_keywords:
- ellipses [Windows Forms], drawing
- circles [Windows Forms], drawing
- drawing [Windows Forms], shapes
- circular shapes
- forms [Windows Forms], drawing circular shapes
- circles
- outlined shapes [Windows Forms], examples
- outlined shapes [Windows Forms], drawing
- drawing [Windows Forms], circular shapes
- shapes [Windows Forms], drawing
ms.assetid: f4f9214c-607e-407d-8cdd-6549f0278451
ms.openlocfilehash: 019bbc19cc4b26c42f8539eccd93ec4ff87fab12
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59192201"
---
# <a name="how-to-draw-an-outlined-shape"></a><span data-ttu-id="9bd85-102">Procédure : dessiner une forme avec contour</span><span class="sxs-lookup"><span data-stu-id="9bd85-102">How to: Draw an Outlined Shape</span></span>
<span data-ttu-id="9bd85-103">Cet exemple dessine avec contour ellipses et rectangles dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="9bd85-103">This example draws outlined ellipses and rectangles on a form.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9bd85-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9bd85-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#6)]
 [!code-csharp[System.Drawing.ConceptualHowTos#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#6)]
 [!code-vb[System.Drawing.ConceptualHowTos#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9bd85-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9bd85-105">Compiling the Code</span></span>  
 <span data-ttu-id="9bd85-106">Vous ne pouvez pas appeler cette méthode le <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="9bd85-106">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="9bd85-107">Le contenu dessiné ne sera pas redessiné si le formulaire est redimensionné ou masqué par un autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="9bd85-107">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="9bd85-108">Pour que votre contenu repeindre automatiquement, vous devez substituer la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="9bd85-108">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="9bd85-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="9bd85-109">Robust Programming</span></span>  
 <span data-ttu-id="9bd85-110">Vous devez toujours appeler <xref:System.IDisposable.Dispose%2A> sur tous les objets qui consomment des ressources système, telles que <xref:System.Drawing.Pen> et <xref:System.Drawing.Graphics> objets.</span><span class="sxs-lookup"><span data-stu-id="9bd85-110">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Pen> and <xref:System.Drawing.Graphics> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9bd85-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bd85-111">See also</span></span>

- <xref:System.Drawing.Graphics.DrawEllipse%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- <xref:System.Drawing.Graphics.DrawRectangle%2A>
- [<span data-ttu-id="9bd85-112">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="9bd85-112">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="9bd85-113">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="9bd85-113">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="9bd85-114">Graphiques et dessins dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9bd85-114">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
