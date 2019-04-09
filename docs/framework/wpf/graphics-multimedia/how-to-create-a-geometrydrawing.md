---
title: 'Procédure : Créer un GeometryDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
ms.openlocfilehash: f5cdcfdb68ad8030bcbd6c689f45a8baddd000e1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59179788"
---
# <a name="how-to-create-a-geometrydrawing"></a>Procédure : Créer un GeometryDrawing
Cet exemple montre comment créer et afficher un <xref:System.Windows.Media.GeometryDrawing>. Un <xref:System.Windows.Media.GeometryDrawing> vous permet de créer la forme avec un remplissage et un contour en associant un <xref:System.Windows.Media.Pen> et un <xref:System.Windows.Media.Brush> avec un <xref:System.Windows.Media.Geometry>. Le <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> décrit la structure de la forme, le <xref:System.Windows.Media.GeometryDrawing.Brush%2A> décrit le remplissage de la forme et le <xref:System.Windows.Media.GeometryDrawing.Pen%2A> décrit le contour de la forme.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.GeometryDrawing> pour rendre une forme. La forme est décrite par un <xref:System.Windows.Media.GeometryGroup> et deux <xref:System.Windows.Media.EllipseGeometry> objets. Intérieur de la forme est peint avec un <xref:System.Windows.Media.LinearGradientBrush> et son contour est dessiné avec un <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>. Le <xref:System.Windows.Media.GeometryDrawing> est affichée en utilisant un <xref:System.Windows.Media.ImageDrawing> et un <xref:System.Windows.Controls.Image> élément.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 L’illustration suivante montre le résultat <xref:System.Windows.Media.GeometryDrawing>.  
  
 ![GeometryDrawing de deux ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")  
  
 Pour créer des dessins plus complexes, vous pouvez combiner plusieurs objets de dessin dans un dessin à l’aide de composite unique un <xref:System.Windows.Media.DrawingGroup>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.DrawingGroup>
- [Vue d'ensemble des objets Drawing](drawing-objects-overview.md)
- [Vue d'ensemble de Geometry](geometry-overview.md)
- [Créer un dessin composite](how-to-create-a-composite-drawing.md)
