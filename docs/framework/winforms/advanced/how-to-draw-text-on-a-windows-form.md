---
title: 'Procédure : Dessiner du texte dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- forms [Windows Forms], drawing text
- text [Windows Forms], drawing
ms.assetid: 5d2447a9-21a1-4adc-b954-5516f2bb9b2c
ms.openlocfilehash: 07aef6619468b957d6f2aa46482be3de0411cd40
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512386"
---
# <a name="how-to-draw-text-on-a-windows-form"></a><span data-ttu-id="53066-102">Procédure : Dessiner du texte dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="53066-102">How to: Draw Text on a Windows Form</span></span>
<span data-ttu-id="53066-103">L’exemple de code suivant montre comment utiliser le <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> pour dessiner du texte dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="53066-103">The following code example shows how to use the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> to draw text on a form.</span></span> <span data-ttu-id="53066-104">Vous pouvez également utiliser <xref:System.Windows.Forms.TextRenderer> pour dessiner du texte sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="53066-104">Alternatively, you can use <xref:System.Windows.Forms.TextRenderer> for drawing text on a form.</span></span> <span data-ttu-id="53066-105">Pour plus d'informations, voir [Procédure : Dessiner du texte avec GDI](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="53066-105">For more information, see [How to: Draw Text with GDI](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="53066-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="53066-106">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#7)]
 [!code-csharp[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#7)]
 [!code-vb[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#7)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="53066-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="53066-107">Compiling the Code</span></span>  
 <span data-ttu-id="53066-108">Vous ne pouvez pas appeler le <xref:System.Drawing.Graphics.DrawString%2A> méthode dans le <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="53066-108">You cannot call the <xref:System.Drawing.Graphics.DrawString%2A> method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="53066-109">Le contenu dessiné ne sera pas redessiné si le formulaire est redimensionné ou masqué par un autre formulaire.</span><span class="sxs-lookup"><span data-stu-id="53066-109">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="53066-110">Pour que votre contenu repeindre automatiquement, vous devez substituer la <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="53066-110">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="53066-111">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="53066-111">Robust Programming</span></span>  
 <span data-ttu-id="53066-112">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="53066-112">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="53066-113">La police Arial n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="53066-113">The Arial font is not installed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53066-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53066-114">See also</span></span>
- <xref:System.Drawing.Graphics.DrawString%2A>
- <xref:System.Windows.Forms.TextRenderer.DrawText%2A>
- <xref:System.Drawing.StringFormat.FormatFlags%2A>
- <xref:System.Drawing.StringFormatFlags>
- <xref:System.Windows.Forms.TextFormatFlags>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- [<span data-ttu-id="53066-115">Mise en route de la programmation graphique</span><span class="sxs-lookup"><span data-stu-id="53066-115">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)
- [<span data-ttu-id="53066-116">Guide pratique pour Dessiner du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="53066-116">How to: Draw Text with GDI</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
