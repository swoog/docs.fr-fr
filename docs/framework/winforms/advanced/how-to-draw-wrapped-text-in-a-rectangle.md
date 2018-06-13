---
title: 'Comment : écrire du texte renvoyé à la ligne dans un rectangle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drawing text in a rectangle
- text [Windows Forms], drawing in a rectangle
- strings [Windows Forms], drawing in a rectangle
ms.assetid: e1fb432a-dc90-48b5-9b6b-acc14507133d
ms.openlocfilehash: c753be6a200f166e59e1330c7dbcf1fadc7588a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524971"
---
# <a name="how-to-draw-wrapped-text-in-a-rectangle"></a><span data-ttu-id="64d9b-102">Comment : écrire du texte renvoyé à la ligne dans un rectangle</span><span class="sxs-lookup"><span data-stu-id="64d9b-102">How to: Draw Wrapped Text in a Rectangle</span></span>
<span data-ttu-id="64d9b-103">Vous pouvez dessiner du texte encapsulé dans un rectangle à l’aide de la <xref:System.Drawing.Graphics.DrawString%2A> surchargées de la <xref:System.Drawing.Graphics> classe qui prend un <xref:System.Drawing.Rectangle> ou <xref:System.Drawing.RectangleF> paramètre.</span><span class="sxs-lookup"><span data-stu-id="64d9b-103">You can draw wrapped text in a rectangle by using the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method of the <xref:System.Drawing.Graphics> class that takes a <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF> parameter.</span></span> <span data-ttu-id="64d9b-104">Vous pouvez également utiliser un <xref:System.Drawing.Brush> et un <xref:System.Drawing.Font>.</span><span class="sxs-lookup"><span data-stu-id="64d9b-104">You will also use a <xref:System.Drawing.Brush> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="64d9b-105">Vous pouvez également dessiner du texte encapsulé dans un rectangle à l’aide de la <xref:System.Windows.Forms.TextRenderer.DrawText%2A> surchargées de la <xref:System.Windows.Forms.TextRenderer> qui accepte un <xref:System.Drawing.Rectangle> et un <xref:System.Windows.Forms.TextFormatFlags> paramètre.</span><span class="sxs-lookup"><span data-stu-id="64d9b-105">You can also draw wrapped text in a rectangle by using the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method of the <xref:System.Windows.Forms.TextRenderer> that takes a <xref:System.Drawing.Rectangle> and a <xref:System.Windows.Forms.TextFormatFlags> parameter.</span></span> <span data-ttu-id="64d9b-106">Vous pouvez également utiliser un <xref:System.Drawing.Color> et un <xref:System.Drawing.Font>.</span><span class="sxs-lookup"><span data-stu-id="64d9b-106">You will also use a <xref:System.Drawing.Color> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="64d9b-107">L’illustration suivante montre la sortie du texte dessiné dans le rectangle lorsque vous utilisez la <xref:System.Drawing.Graphics.DrawString%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="64d9b-107">The following illustration shows the output of text drawn in the rectangle when you use the <xref:System.Drawing.Graphics.DrawString%2A> method.</span></span>  
  
 <span data-ttu-id="64d9b-108">![Polices du texte](../../../../docs/framework/winforms/advanced/media/csfontstext2.png "csfontstext2")</span><span class="sxs-lookup"><span data-stu-id="64d9b-108">![Fonts Text](../../../../docs/framework/winforms/advanced/media/csfontstext2.png "csfontstext2")</span></span>  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="64d9b-109">Inclus pour dessiner le texte dans un rectangle avec GDI +</span><span class="sxs-lookup"><span data-stu-id="64d9b-109">To draw wrapped text in a rectangle with GDI+</span></span>  
  
1.  <span data-ttu-id="64d9b-110">Utilisez le <xref:System.Drawing.Graphics.DrawString%2A> méthode surchargée, en passant le texte que vous le souhaitez, <xref:System.Drawing.Rectangle> ou <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> et <xref:System.Drawing.Brush>.</span><span class="sxs-lookup"><span data-stu-id="64d9b-110">Use the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> and <xref:System.Drawing.Brush>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#50](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#50)]
     [!code-vb[System.Drawing.AlignDrawnText#50](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#50)]  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="64d9b-111">Inclus pour dessiner le texte dans un rectangle avec GDI</span><span class="sxs-lookup"><span data-stu-id="64d9b-111">To draw wrapped text in a rectangle with GDI</span></span>  
  
1.  <span data-ttu-id="64d9b-112">Utilisez le <xref:System.Windows.Forms.TextFormatFlags> valeur d’énumération pour spécifier le texte doit être ajusté à la <xref:System.Windows.Forms.TextRenderer.DrawText%2A> méthode surchargée, en passant le texte que vous le souhaitez, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> et <xref:System.Drawing.Color>.</span><span class="sxs-lookup"><span data-stu-id="64d9b-112">Use the <xref:System.Windows.Forms.TextFormatFlags> enumeration value to specify the text should be wrapped with the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> and <xref:System.Drawing.Color>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#60](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#60)]
     [!code-vb[System.Drawing.AlignDrawnText#60](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="64d9b-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="64d9b-113">Compiling the Code</span></span>  
 <span data-ttu-id="64d9b-114">Les exemples précédents nécessitent :</span><span class="sxs-lookup"><span data-stu-id="64d9b-114">The previous examples require:</span></span>  
  
-   <span data-ttu-id="64d9b-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="64d9b-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64d9b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d9b-116">See Also</span></span>  
 [<span data-ttu-id="64d9b-117">Guide pratique pour écrire du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="64d9b-117">How to: Draw Text with GDI</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)  
 [<span data-ttu-id="64d9b-118">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="64d9b-118">Using Fonts and Text</span></span>](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)  
 [<span data-ttu-id="64d9b-119">Guide pratique pour construire des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="64d9b-119">How to: Construct Font Families and Fonts</span></span>](../../../../docs/framework/winforms/advanced/how-to-construct-font-families-and-fonts.md)  
 [<span data-ttu-id="64d9b-120">Guide pratique pour écrire du texte à un emplacement spécifié</span><span class="sxs-lookup"><span data-stu-id="64d9b-120">How to: Draw Text at a Specified Location</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-at-a-specified-location.md)
