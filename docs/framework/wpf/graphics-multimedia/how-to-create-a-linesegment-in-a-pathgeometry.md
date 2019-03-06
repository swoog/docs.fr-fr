---
title: 'Procédure : Créer un LineSegment dans un PathGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- line segments [WPF], creating
- graphics [WPF], line segments
ms.assetid: 0155ed47-a20d-49a7-a306-186d8e07fbc4
ms.openlocfilehash: a6862ab02c288f9cfd1fac4a8c22079b0cf91016
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57356180"
---
# <a name="how-to-create-a-linesegment-in-a-pathgeometry"></a>Procédure : Créer un LineSegment dans un PathGeometry
Cet exemple indique comment créer un segment de ligne. Pour créer un segment de ligne, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.LineSegment> classes.  
  
## <a name="example"></a>Exemple  
 Les exemples suivants tracent un <xref:System.Windows.Media.LineSegment> à partir de (10, 50) à (200, 70). L’illustration suivante montre le résultat <xref:System.Windows.Media.LineSegment>; un arrière-plan de la grille a été ajouté pour afficher le système de coordonnées.  
  
 ![LineSegment dans un PathFigure](./media/graphicsmm-pathgeometrylinesegment.png "graphicsmm_pathgeometrylinesegment")  
LineSegment tracé de (10,50) à (200,70)  
  
 [xaml]  
  
 En [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe d’attribut pour décrire un tracé.  
  
```xaml  
<Path Stroke="Black" StrokeThickness="1"    
  Data="M 10,50 L 200,70" />  
```  
  
 [xaml]  
  
 (Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>. (Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)  
  
 En [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner un segment de ligne en utilisant la syntaxe d’élément objet. L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.  
  
```xaml  
<Path Stroke="Black" StrokeThickness="1">  
  <Path.Data>  
    <PathGeometry>  
      <PathFigure StartPoint="10,50">  
        <LineSegment Point="200,70" />  
      </PathFigure>  
    </PathGeometry>  
  </Path.Data>  
</Path>  
```  
  
```csharp  
PathFigure myPathFigure = new PathFigure();  
myPathFigure.StartPoint = new Point(10, 50);  
  
LineSegment myLineSegment = new LineSegment();  
myLineSegment.Point = new Point(200, 70);  
  
PathSegmentCollection myPathSegmentCollection = new PathSegmentCollection();  
myPathSegmentCollection.Add(myLineSegment);  
  
myPathFigure.Segments = myPathSegmentCollection;  
  
PathFigureCollection myPathFigureCollection = new PathFigureCollection();  
myPathFigureCollection.Add(myPathFigure);  
  
PathGeometry myPathGeometry = new PathGeometry();  
myPathGeometry.Figures = myPathFigureCollection;  
  
Path myPath = new Path();  
myPath.Stroke = Brushes.Black;  
myPath.StrokeThickness = 1;  
myPath.Data = myPathGeometry;  
```  
  
```vb  
Dim myPathFigure As New PathFigure()  
            myPathFigure.StartPoint = New Point(10, 50)  
  
            Dim myLineSegment As New LineSegment()  
            myLineSegment.Point = New Point(200, 70)  
  
            Dim myPathSegmentCollection As New PathSegmentCollection()  
            myPathSegmentCollection.Add(myLineSegment)  
  
            myPathFigure.Segments = myPathSegmentCollection  
  
            Dim myPathFigureCollection As New PathFigureCollection()  
            myPathFigureCollection.Add(myPathFigure)  
  
            Dim myPathGeometry As New PathGeometry()  
            myPathGeometry.Figures = myPathFigureCollection  
  
            Dim myPath As New Path()  
            myPath.Stroke = Brushes.Black  
            myPath.StrokeThickness = 1  
            myPath.Data = myPathGeometry  
```  
  
 Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.PathFigure>
- <xref:System.Windows.Media.PathGeometry>
- <xref:System.Windows.Media.GeometryDrawing>
- <xref:System.Windows.Shapes.Path>
- [Vue d’ensemble de Geometry](geometry-overview.md)
