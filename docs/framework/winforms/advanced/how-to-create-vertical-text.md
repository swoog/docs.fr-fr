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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59190221"
---
# <a name="how-to-create-vertical-text"></a>Procédure : créer du texte vertical
Vous pouvez utiliser un <xref:System.Drawing.StringFormat> objet pour spécifier que le texte doit être dessiné verticalement et non horizontalement.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant assigne la valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> à la <xref:System.Drawing.StringFormat.FormatFlags%2A> propriété d’un <xref:System.Drawing.StringFormat> objet. Que <xref:System.Drawing.StringFormat> objet est passé à la <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe. La valeur <xref:System.Drawing.StringFormatFlags.DirectionVertical> est un membre de la <xref:System.Drawing.StringFormatFlags> énumération.  
  
 L’illustration suivante montre le texte vertical : 
  
 ![Graphique qui affiche le texte d’une police verticale.](./media/how-to-create-vertical-text/vertical-font-text-graphic.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.FontsAndText#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
  
-   L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e` , qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : dessiner du texte avec GDI](how-to-draw-text-with-gdi.md)
