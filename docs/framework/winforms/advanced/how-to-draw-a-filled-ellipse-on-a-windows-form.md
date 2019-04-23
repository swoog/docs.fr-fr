---
title: 'Procédure : dessiner une ellipse pleine dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillEllipse
helpviewer_keywords:
- ellipses [Windows Forms], drawing
- circles [Windows Forms], drawing
- circular shapes
- drawing [Windows Forms], ellipses
- shapes [Windows Forms], drawing
- forms [Windows Forms], drawing ellipses
ms.assetid: 781db806-950d-4c5b-b022-493f7fd0c4a8
ms.openlocfilehash: 2e7be3f2c4c710bb24568dd2e70f6f5cc4706c63
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171001"
---
# <a name="how-to-draw-a-filled-ellipse-on-a-windows-form"></a><span data-ttu-id="e2ff3-102">Procédure : dessiner une ellipse pleine dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="e2ff3-102">How to: Draw a Filled Ellipse on a Windows Form</span></span>
<span data-ttu-id="e2ff3-103">Cet exemple dessine une ellipse remplie dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="e2ff3-103">This example draws a filled ellipse on a form.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2ff3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e2ff3-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e2ff3-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e2ff3-105">Compiling the Code</span></span>  
 <span data-ttu-id="e2ff3-106">Vous ne pouvez pas appeler cette méthode le <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="e2ff3-106">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="e2ff3-107">Le contenu dessiné ne sera pas redessiné si le formulaire est redimensionné ou masqué par un autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e2ff3-107">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="e2ff3-108">Pour que votre contenu repeindre automatiquement, vous devez substituer la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="e2ff3-108">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="e2ff3-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="e2ff3-109">Robust Programming</span></span>  
 <span data-ttu-id="e2ff3-110">Vous devez toujours appeler <xref:System.IDisposable.Dispose%2A> sur tous les objets qui consomment des ressources système, telles que <xref:System.Drawing.Brush> et <xref:System.Drawing.Graphics> objets.</span><span class="sxs-lookup"><span data-stu-id="e2ff3-110">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Brush> and <xref:System.Drawing.Graphics> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2ff3-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2ff3-111">See also</span></span>

- [<span data-ttu-id="e2ff3-112">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e2ff3-112">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="e2ff3-113">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="e2ff3-113">Getting Started with Graphics Programming</span></span>](getting-started-with-graphics-programming.md)
- [<span data-ttu-id="e2ff3-114">Fusion alpha de lignes et de remplissages</span><span class="sxs-lookup"><span data-stu-id="e2ff3-114">Alpha Blending Lines and Fills</span></span>](alpha-blending-lines-and-fills.md)
- [<span data-ttu-id="e2ff3-115">Utilisation d'un pinceau pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="e2ff3-115">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
