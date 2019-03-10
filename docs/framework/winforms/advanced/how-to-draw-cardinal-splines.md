---
title: 'Procédure : Dessiner des splines cardinales'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cardinal splines [Windows Forms], drawing
- drawing [Windows Forms], cardinal splines
- graphics [Windows Forms], cardinal splines
ms.assetid: a4a41e80-4461-4b47-b6bd-2c5e68881994
ms.openlocfilehash: 687143273a07acba4b4d60acb1be25eee165b91d
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710483"
---
# <a name="how-to-draw-cardinal-splines"></a>Procédure : Dessiner des splines cardinales
Une spline cardinale est une courbe qui traverse facilement un ensemble donné de points. Pour dessiner une spline cardinale, créez un <xref:System.Drawing.Graphics> de l’objet et passez l’adresse d’un tableau de points à la <xref:System.Drawing.Graphics.DrawCurve%2A> (méthode).  
  
### <a name="drawing-a-bell-shaped-cardinal-spline"></a>Dessin d’une Spline cardinale en forme de cloche  
  
-   L’exemple suivant dessine une spline cardinale en forme de cloche qui passe par cinq points définis. L’illustration suivante montre la courbe et cinq points.  
  
     ![Spline cardinale](./media/cardinalspline1.png "CardinalSpline1")  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#21)]  
  
### <a name="drawing-a-closed-cardinal-spline"></a>Dessiner une Spline cardinale fermée  
  
-   Utilisez le <xref:System.Drawing.Graphics.DrawClosedCurve%2A> méthode de la <xref:System.Drawing.Graphics> classe pour dessiner une spline cardinale fermée. Dans une spline cardinale fermée, la courbe se poursuit jusqu’au dernier point dans le tableau et se connecte avec le premier point dans le tableau. L’exemple suivant dessine une spline cardinale fermée qui passe par six points définis. L’illustration suivante montre la spline fermée avec les six points.  
  
 ![Spline cardinale](./media/cardinalspline1a.png "CardinalSpline1A")  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#22)]  
  
### <a name="changing-the-bend-of-a-cardinal-spline"></a>Modification de la courbure d’une Spline cardinale  
  
-   Modifier la courbure d’une spline cardinale en passant un argument de tension à le <xref:System.Drawing.Graphics.DrawCurve%2A> (méthode). L’exemple suivant dessine trois splines cardinales qui passent par le même ensemble de points. L’illustration suivante montre les trois splines, ainsi que leurs valeurs de tension. Notez que lorsque la tension est 0, les points sont reliés par des lignes droites.  
  
 ![Spline cardinale](./media/cardinalspline2.png "CardinalSpline2")  
  
 [!code-csharp[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/CS/Class1.cs#23)]
 [!code-vb[System.Drawing.ConstructingDrawingCurves#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingCurves/VB/Class1.vb#23)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Les exemples précédents sont conçus pour une utilisation avec Windows Forms, et ils nécessitent <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Génération et dessin de courbes](constructing-and-drawing-curves.md)
