---
title: 'Procédure : Définir un rectangle à l’aide d’un RectangleGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rectangles
- rectangles [WPF], creating with RectangleGeometry class
ms.assetid: e40b8a8e-54b8-416b-a9f2-be6dca9fdf0b
ms.openlocfilehash: 146ca7017ee38ad5c1065e59662ac441e7bfbfe2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075794"
---
# <a name="how-to-define-a-rectangle-using-a-rectanglegeometry"></a>Procédure : Définir un rectangle à l’aide d’un RectangleGeometry
Cet exemple explique comment utiliser le <xref:System.Windows.Media.RectangleGeometry> classe pour décrire un rectangle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer et afficher un <xref:System.Windows.Media.RectangleGeometry>.  La position relative et les dimensions du rectangle sont définies par un <xref:System.Windows.Rect> structure. La position relative est `50,50` et la hauteur et la largeur sont toutes deux `25` création d’un carré. L’intérieur du rectangle est peint avec un <xref:System.Windows.Media.Brushes.LemonChiffon%2A> pinceau et son contour est peint avec un <xref:System.Windows.Media.Brushes.Black%2A> trait avec une épaisseur de `1`.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmrectanglegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmrectanglegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmrectanglegeometryexample)]  
  
 ![A RectangleGeometry](./media/graphicsmm-rectangle.gif "graphicsmm_rectangle")  
RectangleGeometry  
  
 Bien que cet exemple utilise un <xref:System.Windows.Shapes.Path> élément à restituer le <xref:System.Windows.Media.RectangleGeometry>, il existe d’autres façons d’utiliser <xref:System.Windows.Media.RectangleGeometry> objets. Par exemple, un <xref:System.Windows.Media.RectangleGeometry> peut être utilisé pour spécifier le <xref:System.Windows.UIElement.Clip%2A> d’un <xref:System.Windows.UIElement> ou le <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> d’un <xref:System.Windows.Media.GeometryDrawing>.  
  
 Autres classes de géométrie simple incluent <xref:System.Windows.Media.LineGeometry> et <xref:System.Windows.Media.EllipseGeometry>. Ces géométries, ainsi que celles qui sont plus complexes, peut également être créés à l’aide un <xref:System.Windows.Media.PathGeometry> ou <xref:System.Windows.Media.StreamGeometry>.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de Geometry](geometry-overview.md)
- [Créer une forme composite](how-to-create-a-composite-shape.md)
- [Créer une forme à l’aide d’un PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
