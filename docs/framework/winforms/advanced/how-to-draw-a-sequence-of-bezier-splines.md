---
title: 'Procédure : Dessiner une séquence de B&#233;Splines de Bézier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], drawing Bezier
- Bezier splines [Windows Forms], drawing sequence of
ms.assetid: 37a0bedb-20c2-4cf0-91fa-a5509e826b30
ms.openlocfilehash: 976787f5830282a581d05a9c24d1f83dceca4b25
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62004267"
---
# <a name="how-to-draw-a-sequence-of-b233zier-splines"></a>Procédure : Dessiner une séquence de B&#233;Splines de Bézier
Vous pouvez utiliser la <xref:System.Drawing.Graphics.DrawBeziers%2A> méthode de la <xref:System.Drawing.Graphics> classe pour dessiner une séquence de splines de Bézier reliées.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant dessine une courbe qui se compose de deux splines de Bézier connectées. Le point de terminaison de la première spline de Bézier est le point de départ de la seconde.  
  
 L’illustration suivante montre les splines connectés, ainsi que les sept points :  
  
 ![Graphique montrant les splines reliées et sept points.](./media/how-to-draw-a-sequence-of-bezier-splines/bezier-spline-seven-points.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi

- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Splines de Bézier dans GDI+](bezier-splines-in-gdi.md)
- [Génération et dessin de courbes](constructing-and-drawing-curves.md)
