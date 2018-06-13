---
title: 'Comment : utiliser un stylet pour dessiner des rectangles'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- rectangles [Windows Forms], drawing
- pens [Windows Forms], drawing rectangles
ms.assetid: 54a7fa14-3ad8-4d64-b424-2a12005b250c
ms.openlocfilehash: ad5b436f7162c282198c7a9d3cce4d3ce3fd3c6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524005"
---
# <a name="how-to-use-a-pen-to-draw-rectangles"></a>Comment : utiliser un stylet pour dessiner des rectangles
Pour dessiner des rectangles, vous avez besoin une <xref:System.Drawing.Graphics> objet et un <xref:System.Drawing.Pen> objet. Le <xref:System.Drawing.Graphics> objet fournit les <xref:System.Drawing.Graphics.DrawRectangle%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les fonctionnalités de la ligne, telles que la couleur et la largeur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant dessine un rectangle avec son coin supérieur gauche à (10, 10). Le rectangle a une largeur de 100 et une hauteur de 50. Le deuxième argument passé à la <xref:System.Drawing.Pen.%23ctor%2A> constructeur indique que la largeur du stylet est de 5 pixels.  
  
 Lorsque le rectangle est dessiné, le stylet est centré sur la limite du rectangle. Étant donné que la largeur du stylet est 5, les côtés du rectangle sont dessinés 5 pixels large, par exemple : 1 pixel est dessiné sur la limite proprement dite, 2 pixels sont dessinées à l’intérieur et 2 pixels sont dessinées à l’extérieur. Pour plus d’informations sur l’alignement du stylet, consultez [Comment : définir la largeur et l’alignement](../../../../docs/framework/winforms/advanced/how-to-set-pen-width-and-alignment.md).  
  
 L’illustration suivante montre le rectangle résultant. Les lignes discontinues montrent où le rectangle aurait été dessiné Si la largeur du stylet avait été un pixel. L’affichage agrandi de l’angle supérieur gauche du rectangle montre que les lignes noires épaisses sont centrées sur les lignes en pointillés.  
  
 ![Stylets](../../../../docs/framework/winforms/advanced/media/pens1.gif "pens1")  
  
 [!code-csharp[System.Drawing.UsingAPen#21](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingAPen#21](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation d'un stylet pour dessiner des lignes et des formes](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
