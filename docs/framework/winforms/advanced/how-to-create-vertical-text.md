---
title: 'Procédure : créer du texte vertical'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing vertical
- Windows Forms, drawing vertical text
- strings [Windows Forms], drawing vertical
- vertical text [Windows Forms], drawing
ms.assetid: 50c69046-4188-47d9-b949-cc2610ffd337
ms.openlocfilehash: 75f5d8faa4dc4b7e022cd6de2e6db49f4fa9030c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59190221"
---
# <a name="how-to-create-vertical-text"></a><span data-ttu-id="00c74-102">Procédure : créer du texte vertical</span><span class="sxs-lookup"><span data-stu-id="00c74-102">How to: Create Vertical Text</span></span>
<span data-ttu-id="00c74-103">Vous pouvez utiliser un <xref:System.Drawing.StringFormat> objet pour spécifier que le texte doit être dessiné verticalement et non horizontalement.</span><span class="sxs-lookup"><span data-stu-id="00c74-103">You can use a <xref:System.Drawing.StringFormat> object to specify that text be drawn vertically rather than horizontally.</span></span>  
  
## <a name="example"></a><span data-ttu-id="00c74-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="00c74-104">Example</span></span>  
 <span data-ttu-id="00c74-105">L’exemple suivant assigne la valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> à la <xref:System.Drawing.StringFormat.FormatFlags%2A> propriété d’un <xref:System.Drawing.StringFormat> objet.</span><span class="sxs-lookup"><span data-stu-id="00c74-105">The following example assigns the value <xref:System.Drawing.StringFormatFlags.DirectionVertical> to the <xref:System.Drawing.StringFormat.FormatFlags%2A> property of a <xref:System.Drawing.StringFormat> object.</span></span> <span data-ttu-id="00c74-106">Que <xref:System.Drawing.StringFormat> objet est passé à la <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="00c74-106">That <xref:System.Drawing.StringFormat> object is passed to the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="00c74-107">La valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> est un membre de la <xref:System.Drawing.StringFormatFlags> énumération.</span><span class="sxs-lookup"><span data-stu-id="00c74-107">The value <xref:System.Drawing.StringFormatFlags.DirectionVertical> is a member of the <xref:System.Drawing.StringFormatFlags> enumeration.</span></span>  
  
 <span data-ttu-id="00c74-108">L’illustration suivante montre le texte vertical :</span><span class="sxs-lookup"><span data-stu-id="00c74-108">The following illustration shows the vertical text:</span></span> 
  
 ![Graphique qui affiche le texte d’une police verticale.](./media/how-to-create-vertical-text/vertical-font-text-graphic.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.FontsAndText#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="00c74-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="00c74-110">Compiling the Code</span></span>  
  
-   <span data-ttu-id="00c74-111">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e` , qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="00c74-111">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e` , which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00c74-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c74-112">See also</span></span>

- [<span data-ttu-id="00c74-113">Guide pratique pour Dessiner du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="00c74-113">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
