---
title: Tracés graphiques dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], paths
- GDI+, drawing paths
- paths [Windows Forms], drawing
- drawing [Windows Forms], paths
ms.assetid: a5500dec-666c-41fd-9da3-2169dd89c5eb
ms.openlocfilehash: c9a43065210f5ef0fffcae01cc7eb88349696b6b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59140502"
---
# <a name="graphics-paths-in-gdi"></a>Tracés graphiques dans GDI+
Chemins d’accès sont formés en combinant les lignes, des rectangles et des courbes simples. Nous avons vu dans la [vue d’ensemble des graphismes vectoriels](vector-graphics-overview.md) que les blocs de construction de base suivantes se sont avérées les plus utiles pour dessiner des images :  
  
-   Lignes  
  
-   Rectangles  
  
-   Points de suspension  
  
-   Arcs  
  
-   Polygones  
  
-   Splines cardinales  
  
-   Splines de Bézier  
  
 Dans GDI +, le <xref:System.Drawing.Drawing2D.GraphicsPath> objet vous permet de collecter une séquence de ces blocs de construction en une seule unité. La séquence entière de lignes, des rectangles, des polygones et des courbes peut ensuite être dessinée avec un seul appel à la <xref:System.Drawing.Graphics.DrawPath%2A> méthode de la <xref:System.Drawing.Graphics> classe. L’illustration suivante montre un chemin d’accès créé en combinant une ligne, un arc, une spline de Bézier et une spline cardinale.  
  
 ![Path](./media/aboutgdip02-art14.gif "Aboutgdip02_art14")  
  
## <a name="using-a-path"></a>À l’aide d’un chemin d’accès  
 Le <xref:System.Drawing.Drawing2D.GraphicsPath> classe fournit les méthodes suivantes pour la création d’une séquence d’éléments à dessiner : <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangle%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddEllipse%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddPolygon%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> (pour les splines cardinales), et <xref:System.Drawing.Drawing2D.GraphicsPath.AddBezier%2A>. Chacune de ces méthodes est surchargée ; Autrement dit, chaque méthode prend en charge différentes listes de paramètres. Par exemple, une variante de la <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> reçoit quatre entiers et une autre variante de la <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> méthode reçoit deux <xref:System.Drawing.Point> objets.  
  
 Les méthodes pour l’ajout des lignes, des rectangles et des splines de Bézier à un chemin d’accès ont des méthodes au pluriel qui ajoutent plusieurs éléments pour le chemin d’accès dans un seul appel : <xref:System.Drawing.Drawing2D.GraphicsPath.AddLines%2A>, <xref:System.Drawing.Drawing2D.GraphicsPath.AddRectangles%2A>, et <xref:System.Drawing.Drawing2D.GraphicsPath.AddBeziers%2A>. En outre, le <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A> et <xref:System.Drawing.Drawing2D.GraphicsPath.AddArc%2A> méthodes ont des méthodes, <xref:System.Drawing.Drawing2D.GraphicsPath.AddClosedCurve%2A> et <xref:System.Drawing.Drawing2D.GraphicsPath.AddPie%2A>, qui ajoutent une courbe fermée ou un graphique à secteurs pour le chemin d’accès.  
  
 Pour dessiner un chemin d’accès, vous devez un <xref:System.Drawing.Graphics> objet, un <xref:System.Drawing.Pen> objet et un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Le <xref:System.Drawing.Graphics> objet fournit les <xref:System.Drawing.Graphics.DrawPath%2A> (méthode) et le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour restituer le chemin d’accès. Le <xref:System.Drawing.Drawing2D.GraphicsPath> objet stocke la séquence de lignes et courbes qui forment le chemin d’accès. Le <xref:System.Drawing.Pen> objet et le <xref:System.Drawing.Drawing2D.GraphicsPath> objet sont passées comme arguments à la <xref:System.Drawing.Graphics.DrawPath%2A> (méthode). L’exemple suivant dessine un chemin d’accès qui se compose d’une ligne, une ellipse et une spline de Bézier :  
  
 [!code-csharp[LinesCurvesAndShapes#101](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#101)]
 [!code-vb[LinesCurvesAndShapes#101](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#101)]  
  
 L’illustration suivante montre le chemin d’accès.  
  
 ![Path](./media/aboutgdip02-art15.gif "Aboutgdip02_art15")  
  
 Outre l’ajout des lignes, des rectangles et des courbes à un chemin d’accès, vous pouvez ajouter des chemins d’accès à un chemin d’accès. Cela vous permet de combiner des tracés existants pour former des chemins d’accès de vastes et complexes.  
  
 [!code-csharp[LinesCurvesAndShapes#102](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#102)]
 [!code-vb[LinesCurvesAndShapes#102](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#102)]  
  
 Il existe deux autres éléments que vous pouvez ajouter à un chemin d’accès : chaînes et des secteurs. Un graphique à secteurs est une partie de l’intérieur d’une ellipse. L’exemple suivant crée un chemin d’accès à partir d’un arc, une spline cardinale, une chaîne et un graphique en secteurs :  
  
 [!code-csharp[LinesCurvesAndShapes#103](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#103)]
 [!code-vb[LinesCurvesAndShapes#103](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#103)]  
  
 L’illustration suivante montre le chemin d’accès. Notez qu’un chemin d’accès ne doit pas nécessaire être connecté ; l’arc, spline cardinale, chaîne et à secteurs sont séparés.  
  
 ![Paths](./media/aboutgdip02-art16.gif "Aboutgdip02_Art16")  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Guide pratique pour Créer des objets graphiques pour le dessin](how-to-create-graphics-objects-for-drawing.md)
- [Génération et dessin de tracés](constructing-and-drawing-paths.md)
