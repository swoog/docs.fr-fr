---
title: 'Comment : dessiner une seule B&#233;Spline de Bézier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines [Windows Forms], drawing
- drawing [Windows Forms], Bezier splines
ms.assetid: f4f3fe30-f0a6-4743-ac91-11310cebea9f
ms.openlocfilehash: 9e91b63275c37fc0cdde5721fddd114e1bf2264e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-draw-a-single-b233zier-spline"></a>Comment : dessiner une seule B&#233;Spline de Bézier
Une spline de Bézier est définie par quatre points : un point de départ, deux points de contrôle et un point de terminaison.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant dessine une spline de Bézier avec le point de départ (10, 100) et le point de terminaison (200, 100). Les points de contrôle sont (100, 10) et (150, 150).  
  
 L’illustration suivante montre la spline de Bézier qui en résulte avec son point de départ, les points de contrôle et point de terminaison. L’illustration montre également forme convexe de la spline, qui est un polygone formé en reliant les quatre points avec des lignes droites.  
  
 ![Spline de Bézier](../../../../docs/framework/winforms/advanced/media/bezierspline1.png "BezierSpline1")  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Drawing.Graphics.DrawBezier%2A>  
 [Splines de Bézier dans GDI+](../../../../docs/framework/winforms/advanced/bezier-splines-in-gdi.md)  
 [Guide pratique pour dessiner une séquence de splines de Bézier](../../../../docs/framework/winforms/advanced/how-to-draw-a-sequence-of-bezier-splines.md)
