---
title: 'Procédure : Dessiner un Rectangle rempli dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillRectangle
helpviewer_keywords:
- drawing [Windows Forms], rectangles
- rectangles [Windows Forms], drawing
- drawing rectangles
ms.assetid: d656a93c-987d-4809-aafd-493fe17450f0
ms.openlocfilehash: a9722b2939e77282453743a4dea165a340412a21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587032"
---
# <a name="how-to-draw-a-filled-rectangle-on-a-windows-form"></a><span data-ttu-id="bb4b2-102">Procédure : Dessiner un Rectangle rempli dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="bb4b2-102">How to: Draw a Filled Rectangle on a Windows Form</span></span>
<span data-ttu-id="bb4b2-103">Cet exemple dessine un rectangle rempli dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-103">This example draws a filled rectangle on a form.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb4b2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb4b2-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#2)]
 [!code-csharp[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#2)]
 [!code-vb[System.Drawing.ConceptualHowTos#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bb4b2-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bb4b2-105">Compiling the Code</span></span>  
 <span data-ttu-id="bb4b2-106">Vous ne pouvez pas appeler cette méthode le <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-106">You cannot call this method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="bb4b2-107">Le contenu dessiné ne sera pas redessiné si le formulaire est redimensionné ou masqué par un autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-107">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="bb4b2-108">Pour que votre contenu repeindre automatiquement, vous devez substituer la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="bb4b2-108">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="bb4b2-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="bb4b2-109">Robust Programming</span></span>  
 <span data-ttu-id="bb4b2-110">Vous devez toujours appeler <xref:System.IDisposable.Dispose%2A> sur tous les objets qui consomment des ressources système, telles que <xref:System.Drawing.Brush> et <xref:System.Drawing.Graphics> objets.</span><span class="sxs-lookup"><span data-stu-id="bb4b2-110">You should always call <xref:System.IDisposable.Dispose%2A> on any objects that consume system resources, such as <xref:System.Drawing.Brush> and <xref:System.Drawing.Graphics> objects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb4b2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb4b2-111">See also</span></span>
- <xref:System.Drawing.Graphics.FillRectangle%2A>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="bb4b2-112">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="bb4b2-112">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [<span data-ttu-id="bb4b2-113">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bb4b2-113">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="bb4b2-114">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="bb4b2-114">Using a Pen to Draw Lines and Shapes</span></span>](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="bb4b2-115">Pinceaux et remplissage de formes dans GDI+</span><span class="sxs-lookup"><span data-stu-id="bb4b2-115">Brushes and Filled Shapes in GDI+</span></span>](../../../../docs/framework/winforms/advanced/brushes-and-filled-shapes-in-gdi.md)
