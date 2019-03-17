---
title: 'Procédure : Dessiner un B unique&#233;Spline de Bézier'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines [Windows Forms], drawing
- drawing [Windows Forms], Bezier splines
ms.assetid: f4f3fe30-f0a6-4743-ac91-11310cebea9f
ms.openlocfilehash: 0731595dc25b1afb4b3dbcc7eedbfb92ef32d267
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "58126277"
---
# <a name="how-to-draw-a-single-b233zier-spline"></a>Procédure : Dessiner un B unique&#233;Spline de Bézier
Une spline de Bézier est définie par quatre points : un point de départ, deux points de contrôle et un point de terminaison.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant dessine une spline de Bézier avec le point de départ (10, 100) et de point de terminaison (200, 100). Les points de contrôle sont (100, 10) et (150, 150).  
  
 L’illustration suivante montre la spline de Bézier qui en résulte, ainsi que son point de départ, les points de contrôle et point de terminaison. L’illustration montre également forme convexe de spline, qui est un polygone formé en reliant les quatre points avec des lignes droites.  
  
 ![Illustration d’une Spline de Bézier.](./media/how-to-draw-a-single-bezier-spline/bezier-spline-illustration.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Graphics.DrawBezier%2A>
- [Splines de Bézier dans GDI+](bezier-splines-in-gdi.md)
- [Guide pratique pour Dessiner une séquence de Splines de Bézier](how-to-draw-a-sequence-of-bezier-splines.md)
