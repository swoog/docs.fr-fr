---
title: 'Procédure : Dessiner une ligne remplie d’une Texture'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], texture
- drawing lines [Windows Forms], texture
ms.assetid: dc9118cc-f3c2-42e5-8173-f46d41d18fd5
ms.openlocfilehash: fd7a2aa2f6d930b0de29d8b8cbd3feacdb7a81e3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718595"
---
# <a name="how-to-draw-a-line-filled-with-a-texture"></a>Procédure : Dessiner une ligne remplie d’une Texture
Au lieu de dessiner une ligne avec une couleur unie, vous pouvez dessiner une ligne avec une texture. Pour dessiner des lignes et des courbes avec une texture, créez un <xref:System.Drawing.TextureBrush> de l’objet et la transmettre <xref:System.Drawing.TextureBrush> de l’objet à un <xref:System.Drawing.Pen.%23ctor%2A> constructeur. L’image bitmap associée au pinceau de la texture est utilisé à la vignette du plan (de façon invisible), et lorsque le stylet dessine une ligne ou la courbe, le trait du stylet permet de récupérer certains pixels de la texture en mosaïque.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un <xref:System.Drawing.Bitmap> objet à partir du fichier `Texture1.jpg`. Cette bitmap est utilisée pour construire un <xref:System.Drawing.TextureBrush> objet et le <xref:System.Drawing.TextureBrush> objet est utilisé pour construire un <xref:System.Drawing.Pen> objet. L’appel à <xref:System.Drawing.Graphics.DrawImage%2A> Dessine l’image bitmap avec son coin supérieur gauche à (0, 0). L’appel à <xref:System.Drawing.Graphics.DrawEllipse%2A> utilise le <xref:System.Drawing.Pen> objet sur lequel dessiner une ellipse texturée.  
  
 L’illustration suivante montre l’image bitmap et l’ellipse texturée.  
  
 ![Stylets](./media/pens7.png "pens7")  
  
 [!code-csharp[System.Drawing.UsingAPen#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.UsingAPen#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Créer un formulaire Windows et de gérer le formulaire <xref:System.Windows.Forms.Control.Paint> événement. Collez le code précédent dans le <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements. Remplacez `Texture.jpg` avec une image valide sur votre système.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
