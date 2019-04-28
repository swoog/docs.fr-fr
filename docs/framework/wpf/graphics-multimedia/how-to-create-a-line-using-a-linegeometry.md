---
title: 'Procédure : Créer une ligne à l’aide d’un LineGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], lines
ms.assetid: 41231b22-1f74-4c26-a8e7-a55b29f8f6bd
ms.openlocfilehash: f8c334a54f78aec7af91064a447fd18f23dcfbdc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61905201"
---
# <a name="how-to-create-a-line-using-a-linegeometry"></a>Procédure : Créer une ligne à l’aide d’un LineGeometry
Cet exemple montre comment utiliser le <xref:System.Windows.Media.LineGeometry> classe pour décrire une ligne. Un <xref:System.Windows.Media.LineGeometry> est défini par son début et de points de terminaison.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer et afficher un <xref:System.Windows.Media.LineGeometry>.  Un <xref:System.Windows.Shapes.Path> élément est utilisé pour restituer la ligne.  Dans la mesure où une ligne n’a pas de zone, le <xref:System.Windows.Shapes.Path> l’objet <xref:System.Windows.Shapes.Shape.Fill%2A> n’est pas spécifié ; au lieu de cela la <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> propriétés sont utilisées.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 ![A LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")  
Une LineGeometry tracée de (10,20) à (100,130)  
  
 Autres classes de géométrie simple incluent <xref:System.Windows.Media.LineGeometry> et <xref:System.Windows.Media.EllipseGeometry>. Ces géométries, ainsi que celles qui sont plus complexes, peut également être créés à l’aide un <xref:System.Windows.Media.PathGeometry> ou <xref:System.Windows.Media.StreamGeometry>. Pour plus d’informations, consultez le [vue d’ensemble de Geometry](geometry-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de Geometry](geometry-overview.md)
- [Créer une forme composite](how-to-create-a-composite-shape.md)
- [Créer une forme à l’aide d’un PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
