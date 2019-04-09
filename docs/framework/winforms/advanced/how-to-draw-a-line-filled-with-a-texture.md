---
title: 'Procédure : dessiner une ligne remplie par une texture'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], texture
- drawing lines [Windows Forms], texture
ms.assetid: dc9118cc-f3c2-42e5-8173-f46d41d18fd5
ms.openlocfilehash: c0f90c298f48aeb96893bb09241faddc08d8a49d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186901"
---
# <a name="how-to-draw-a-line-filled-with-a-texture"></a>Procédure : dessiner une ligne remplie par une texture
Au lieu de dessiner une ligne avec une couleur unie, vous pouvez dessiner une ligne avec une texture. Pour dessiner des lignes et des courbes avec une texture, créez un <xref:System.Drawing.TextureBrush> de l’objet et la transmettre <xref:System.Drawing.TextureBrush> de l’objet à un <xref:System.Drawing.Pen.%23ctor%2A> constructeur. L’image bitmap associée au pinceau de la texture est utilisé à la vignette du plan (de façon invisible), et lorsque le stylet dessine une ligne ou la courbe, le trait du stylet permet de récupérer certains pixels de la texture en mosaïque.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un <xref:System.Drawing.Bitmap> objet à partir du fichier `Texture1.jpg`. Cette bitmap est utilisée pour construire un <xref:System.Drawing.TextureBrush> objet et le <xref:System.Drawing.TextureBrush> objet est utilisé pour construire un <xref:System.Drawing.Pen> objet. L’appel à <xref:System.Drawing.Graphics.DrawImage%2A> Dessine l’image bitmap avec son coin supérieur gauche à (0, 0). L’appel à <xref:System.Drawing.Graphics.DrawEllipse%2A> utilise le <xref:System.Drawing.Pen> objet sur lequel dessiner une ellipse texturée.  
  
 L’illustration suivante montre l’image bitmap et l’ellipse texturée :  
  
 ![Capture d’écran montrant la bitmap et l’ellipse texturée.](./media/how-to-draw-a-line-filled-with-a-texture/bitmap-textured-ellipse.png)  
  
 [!code-csharp[System.Drawing.UsingAPen#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.UsingAPen#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Créer un formulaire Windows et de gérer le formulaire <xref:System.Windows.Forms.Control.Paint> événement. Collez le code précédent dans le <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements. Remplacez `Texture.jpg` avec une image valide sur votre système.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
- [Graphiques et dessins dans les Windows Forms](graphics-and-drawing-in-windows-forms.md)
