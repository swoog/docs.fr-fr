---
title: 'Comment : créer du texte vertical'
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
ms.openlocfilehash: 7d66bf147a220bdcdfd32a703d3407817a184a54
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33521470"
---
# <a name="how-to-create-vertical-text"></a>Comment : créer du texte vertical
Vous pouvez utiliser un <xref:System.Drawing.StringFormat> pour spécifier que le texte doit être dessiné verticalement et non horizontalement.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant affecte la valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> à la <xref:System.Drawing.StringFormat.FormatFlags%2A> propriété d’un <xref:System.Drawing.StringFormat> objet. Que <xref:System.Drawing.StringFormat> objet est passé à la <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe. La valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> est un membre de la <xref:System.Drawing.StringFormatFlags> énumération.  
  
 L’illustration suivante montre le texte vertical.  
  
 ![Polices du texte](../../../../docs/framework/winforms/advanced/media/csfontstext5.png "csfontstext5")  
  
 [!code-csharp[System.Drawing.FontsAndText#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.FontsAndText#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
  
-   L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e` , qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour écrire du texte avec GDI](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
