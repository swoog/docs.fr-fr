---
title: 'Comment : définir des taquets de tabulation dans du texte dessiné'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing with tab stops
- tabs [Windows Forms], drawn text
ms.assetid: 64878f98-39ba-4303-b63f-0859ab682eeb
ms.openlocfilehash: e7f3fe9757db26bcc9dc9735f3d3d854edb7c099
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-set-tab-stops-in-drawn-text"></a>Comment : définir des taquets de tabulation dans du texte dessiné
Vous pouvez définir des taquets de tabulation pour le texte en appelant le <xref:System.Drawing.StringFormat.SetTabStops%2A> méthode d’un <xref:System.Drawing.StringFormat> objet et en passant ensuite cet <xref:System.Drawing.StringFormat> de l’objet à la <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> classe.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> fait pas en charge l’ajout des taquets de tabulation au texte dessiné, bien que vous pouvez développer onglet existant s’arrête à l’aide de la <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> indicateur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit des taquets de tabulation à 150, 250 et 350. Ensuite, le code affiche une liste avec onglets des noms et des scores de test.  
  
 L’illustration suivante montre le texte à onglets.  
  
 ![Polices du texte](../../../../docs/framework/winforms/advanced/media/fontstext4.png "fontstext4")  
  
 Le code suivant passe deux arguments à la <xref:System.Drawing.StringFormat.SetTabStops%2A> (méthode). Le deuxième argument est un tableau qui contient les offsets de tabulation. Le premier argument passé à <xref:System.Drawing.StringFormat.SetTabStops%2A> est 0, ce qui indique que le premier offset dans le tableau est mesuré à partir de la position 0, le bord gauche du rectangle englobant.  
  
 [!code-csharp[System.Drawing.FontsAndText#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.FontsAndText#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
  
-   L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation de polices et de texte](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)  
 [Guide pratique pour écrire du texte avec GDI](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
