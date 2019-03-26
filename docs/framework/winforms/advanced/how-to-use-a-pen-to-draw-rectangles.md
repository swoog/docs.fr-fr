---
title: 'Procédure : Utiliser un stylet pour dessiner des Rectangles'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- rectangles [Windows Forms], drawing
- pens [Windows Forms], drawing rectangles
ms.assetid: 54a7fa14-3ad8-4d64-b424-2a12005b250c
ms.openlocfilehash: a29cae5a360185b7fa5e70fc0181c0cfaac8fc09
ms.sourcegitcommit: 7156c0b9e4ce4ce5ecf48ce3d925403b638b680c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58463187"
---
# <a name="how-to-use-a-pen-to-draw-rectangles"></a>Procédure : Utiliser un stylet pour dessiner des Rectangles
Pour dessiner des rectangles, vous devez un <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet. Le <xref:System.Drawing.Graphics> objet fournit les <xref:System.Drawing.Graphics.DrawRectangle%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant dessine un rectangle avec son coin supérieur gauche à (10, 10). Le rectangle a une largeur de 100 et une hauteur de 50. Le deuxième argument passé à la <xref:System.Drawing.Pen.%23ctor%2A> constructeur indique que la largeur du stylet est de 5 pixels.  
  
 Lorsque le rectangle est dessiné, le stylet est centré sur la limite du rectangle. Étant donné que la largeur du stylet est 5, les côtés du rectangle sont dessinés 5 pixels large, par exemple : 1 pixel est dessiné sur la limite proprement dite, 2 pixels sont dessinés à l’intérieur et 2 pixels sont dessinées à l’extérieur. Pour plus d’informations sur l’alignement du stylet, consultez [Comment : Définir la largeur du stylet et l’alignement](how-to-set-pen-width-and-alignment.md).  
  
 L’illustration suivante montre le rectangle résultant. Les lignes discontinues montrent où le rectangle aurait été dessiné Si la largeur du stylet avait été un pixel. L’affichage agrandi de l’angle supérieur gauche du rectangle montre que les lignes noires épaisses sont centrées sur ces lignes en pointillés.  
  
 ![Capture d’écran montrant le rectangle dessiné avec noir et les lignes en pointillés.](./media/how-to-use-a-pen-to-draw-rectangles/drawn-rectangle-black-lines-dotted-lines.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingAPen#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
