---
title: 'Procédure : aligner du texte dessiné'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], aligning
- Windows Forms, aligning drawn text
ms.assetid: 83c10a81-1a90-4b5c-98aa-2c6c4b280079
ms.openlocfilehash: 5214ef2c69349514f05ba68cc023a7622e119e3a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210449"
---
# <a name="how-to-align-drawn-text"></a>Procédure : aligner du texte dessiné
Lorsque vous effectuez un dessin personnalisé, vous souhaiterez souvent centrer le texte dessiné sur un formulaire ou contrôle. Vous pouvez facilement aligner le texte dessiné avec la <xref:System.Drawing.Graphics.DrawString%2A> ou <xref:System.Windows.Forms.TextRenderer.DrawText%2A> méthodes en créant l’objet de mise en forme correcte et en définissant les indicateurs de format approprié.  
  
### <a name="to-draw-centered-text-with-gdi-drawstring"></a>Pour dessiner un texte centré avec GDI + (DrawString)  
  
1.  Utilisez un <xref:System.Drawing.StringFormat> avec le bon <xref:System.Drawing.Graphics.DrawString%2A> méthode pour spécifier le texte centré.  
  
     [!code-csharp[System.Drawing.AlignDrawnText#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#10)]
     [!code-vb[System.Drawing.AlignDrawnText#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#10)]  
  
### <a name="to-draw-centered-text-with-gdi-drawtext"></a>Pour dessiner un texte centré avec GDI (DrawText)  
  
1.  Utilisez le <xref:System.Windows.Forms.TextFormatFlags> énumération pour habiller ainsi que centrer verticalement et horizontalement le texte avec le bon <xref:System.Windows.Forms.TextRenderer.DrawText%2A> (méthode).  
  
     [!code-csharp[System.Drawing.AlignDrawnText#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#20)]
     [!code-vb[System.Drawing.AlignDrawnText#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#20)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Les exemples de code précédents sont conçus pour une utilisation avec Windows Forms, et ils nécessitent <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : dessiner du texte avec GDI](how-to-draw-text-with-gdi.md)
- [Utilisation de polices et de texte](using-fonts-and-text.md)
- [Procédure : construire des familles de polices et des polices](how-to-construct-font-families-and-fonts.md)
