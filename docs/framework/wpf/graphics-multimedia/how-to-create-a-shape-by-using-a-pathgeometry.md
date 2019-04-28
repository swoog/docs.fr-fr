---
title: 'Procédure : Créer une forme à l’aide d’un PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], creating with PathGeometry class
- graphics [WPF], shapes
ms.assetid: 49a4a8b7-e738-45be-8dac-b54a6d8f5b21
ms.openlocfilehash: b0ab703596612524881ab892a1095b0f49cd1551
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61904309"
---
# <a name="how-to-create-a-shape-by-using-a-pathgeometry"></a>Procédure : Créer une forme à l’aide d’un PathGeometry
Cet exemple montre comment créer une forme à l’aide de la <xref:System.Windows.Media.PathGeometry> classe. <xref:System.Windows.Media.PathGeometry> les objets sont composés d’un ou plusieurs <xref:System.Windows.Media.PathFigure> objets ; chaque <xref:System.Windows.Media.PathFigure> représente un autre « figure » ou une forme. Chaque <xref:System.Windows.Media.PathFigure> est elle-même composée d’un ou plusieurs <xref:System.Windows.Media.PathSegment> d’objets, chacun représentant une partie connectée de l’illustration ou d’une forme. Types de segment sont <xref:System.Windows.Media.LineSegment>, <xref:System.Windows.Media.ArcSegment>, et <xref:System.Windows.Media.BezierSegment>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.PathGeometry> pour créer un triangle. Le <xref:System.Windows.Media.PathGeometry> est affichée en utilisant un <xref:System.Windows.Shapes.Path> élément.  
  
 [!code-xaml[GeometrySample#49](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#49)]  
  
 L’illustration suivante montre la forme créée dans l’exemple précédent.  
  
 ![Une PathGeometry](./media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")  
Un triangle créé avec un PathGeometry  
  
 L’exemple précédent a montré comment créer une forme relativement simple, un triangle. Un <xref:System.Windows.Media.PathGeometry> peut également être utilisé pour créer des formes plus complexes, y compris les arcs et courbes. Pour obtenir des exemples, consultez [créer un Arc elliptique](how-to-create-an-elliptical-arc.md), [créer une courbe de Bézier cubique](how-to-create-a-cubic-bezier-curve.md), et [créer une courbe de Bézier quadratique](how-to-create-a-quadratic-bezier-curve.md).  
  
 Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.GeometryDrawing>
- [Vue d’ensemble de Geometry](geometry-overview.md)
- [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989)
