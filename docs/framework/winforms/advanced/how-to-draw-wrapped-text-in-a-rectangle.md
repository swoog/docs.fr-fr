---
title: 'Procédure : dessiner un habillage de texte dans un rectangle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drawing text in a rectangle
- text [Windows Forms], drawing in a rectangle
- strings [Windows Forms], drawing in a rectangle
ms.assetid: e1fb432a-dc90-48b5-9b6b-acc14507133d
ms.openlocfilehash: 8e5c7cab1f977bef0570b2e540d7bf3a630aceb0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59301921"
---
# <a name="how-to-draw-wrapped-text-in-a-rectangle"></a><span data-ttu-id="8f6ff-102">Procédure : dessiner un habillage de texte dans un rectangle</span><span class="sxs-lookup"><span data-stu-id="8f6ff-102">How to: Draw Wrapped Text in a Rectangle</span></span>
<span data-ttu-id="8f6ff-103">Vous pouvez dessiner du texte encapsulé dans un rectangle à l’aide de la <xref:System.Drawing.Graphics.DrawString%2A> surchargées de la <xref:System.Drawing.Graphics> classe qui prend un <xref:System.Drawing.Rectangle> ou <xref:System.Drawing.RectangleF> paramètre.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-103">You can draw wrapped text in a rectangle by using the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method of the <xref:System.Drawing.Graphics> class that takes a <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF> parameter.</span></span> <span data-ttu-id="8f6ff-104">Vous utiliserez également un <xref:System.Drawing.Brush> et un <xref:System.Drawing.Font>.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-104">You will also use a <xref:System.Drawing.Brush> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="8f6ff-105">Vous pouvez également dessiner du texte encapsulé dans un rectangle à l’aide de la <xref:System.Windows.Forms.TextRenderer.DrawText%2A> surchargées de la <xref:System.Windows.Forms.TextRenderer> qui accepte un <xref:System.Drawing.Rectangle> et un <xref:System.Windows.Forms.TextFormatFlags> paramètre.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-105">You can also draw wrapped text in a rectangle by using the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method of the <xref:System.Windows.Forms.TextRenderer> that takes a <xref:System.Drawing.Rectangle> and a <xref:System.Windows.Forms.TextFormatFlags> parameter.</span></span> <span data-ttu-id="8f6ff-106">Vous utiliserez également un <xref:System.Drawing.Color> et un <xref:System.Drawing.Font>.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-106">You will also use a <xref:System.Drawing.Color> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="8f6ff-107">L’illustration suivante montre la sortie du texte dessiné dans le rectangle lorsque vous utilisez la <xref:System.Drawing.Graphics.DrawString%2A> méthode :</span><span class="sxs-lookup"><span data-stu-id="8f6ff-107">The following illustration shows the output of text drawn in the rectangle when you use the <xref:System.Drawing.Graphics.DrawString%2A> method:</span></span>
  
 ![Capture d’écran montrant la sortie lorsque vous utilisez la méthode DrawString.](./media/how-to-draw-wrapped-text-in-a-rectangle/drawstring-method-font-text.png)  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="8f6ff-109">Inclus pour dessiner le texte dans un rectangle avec GDI +</span><span class="sxs-lookup"><span data-stu-id="8f6ff-109">To draw wrapped text in a rectangle with GDI+</span></span>  
  
1. <span data-ttu-id="8f6ff-110">Utilisez le <xref:System.Drawing.Graphics.DrawString%2A> méthode surchargée, en passant le texte que vous le souhaitez, <xref:System.Drawing.Rectangle> ou <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> et <xref:System.Drawing.Brush>.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-110">Use the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> and <xref:System.Drawing.Brush>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#50](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#50)]
     [!code-vb[System.Drawing.AlignDrawnText#50](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#50)]  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="8f6ff-111">Inclus pour dessiner le texte dans un rectangle avec GDI</span><span class="sxs-lookup"><span data-stu-id="8f6ff-111">To draw wrapped text in a rectangle with GDI</span></span>  
  
1. <span data-ttu-id="8f6ff-112">Utilisez le <xref:System.Windows.Forms.TextFormatFlags> valeur d’énumération pour spécifier le texte doit être ajusté à la <xref:System.Windows.Forms.TextRenderer.DrawText%2A> méthode surchargée, en passant le texte que vous le souhaitez, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> et <xref:System.Drawing.Color>.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-112">Use the <xref:System.Windows.Forms.TextFormatFlags> enumeration value to specify the text should be wrapped with the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> and <xref:System.Drawing.Color>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#60)]
     [!code-vb[System.Drawing.AlignDrawnText#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8f6ff-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="8f6ff-113">Compiling the Code</span></span>  
 <span data-ttu-id="8f6ff-114">Les exemples précédents nécessitent :</span><span class="sxs-lookup"><span data-stu-id="8f6ff-114">The previous examples require:</span></span>  
  
-   <span data-ttu-id="8f6ff-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="8f6ff-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f6ff-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f6ff-116">See also</span></span>

- [<span data-ttu-id="8f6ff-117">Guide pratique pour Dessiner du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="8f6ff-117">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
- [<span data-ttu-id="8f6ff-118">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="8f6ff-118">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="8f6ff-119">Guide pratique pour Construire des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="8f6ff-119">How to: Construct Font Families and Fonts</span></span>](how-to-construct-font-families-and-fonts.md)
- [<span data-ttu-id="8f6ff-120">Guide pratique pour Dessiner du texte à un emplacement spécifié</span><span class="sxs-lookup"><span data-stu-id="8f6ff-120">How to: Draw Text at a Specified Location</span></span>](how-to-draw-text-at-a-specified-location.md)
