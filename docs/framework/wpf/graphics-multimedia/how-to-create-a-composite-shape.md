---
title: 'Procédure : Créer une forme composite'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- shapes [WPF], composite
- composite shapes [WPF]
- graphics [WPF], composite shapes
ms.assetid: 8e5c7ef4-d7ed-4c43-afc9-ca01325c300b
ms.openlocfilehash: de9f7972c7a51ea623c3630fe62bb48f6109317e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052896"
---
# <a name="how-to-create-a-composite-shape"></a>Procédure : Créer une forme composite
Cet exemple montre comment créer des formes composites à l’aide de <xref:System.Windows.Media.Geometry> objets et les afficher à l’aide un <xref:System.Windows.Shapes.Path> élément. Dans l’exemple suivant, un <xref:System.Windows.Media.LineGeometry>, <xref:System.Windows.Media.EllipseGeometry>et un <xref:System.Windows.Media.RectangleGeometry> sont utilisés avec un <xref:System.Windows.Media.GeometryGroup> pour créer une forme composite. Les géométries sont ensuite dessinés à l’aide un <xref:System.Windows.Shapes.Path> élément.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[GeometrySample#19](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#19)]  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/CompositeShapeExample.cs#compositeshapecodeexampleinline1)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/compositeshapeexample.vb#compositeshapecodeexampleinline1)]  
  
 L’illustration suivante montre la forme créée dans l’exemple précédent.  
  
 ![Géométrie composée créée à l’aide de GeometryGroup](./media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")  
Géométrie composite  
  
 Des formes plus complexes, telles que les polygones et des formes avec des segments courbés, peuvent être créés à l’aide un <xref:System.Windows.Media.PathGeometry>. Pour obtenir un exemple montrant comment créer une forme en utilisant un <xref:System.Windows.Media.PathGeometry>, consultez [créer une forme à l’aide d’un PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md).  Bien que cet exemple restitue une forme à l’écran à l’aide un <xref:System.Windows.Shapes.Path> élément, <xref:System.Windows.Media.Geometry> objets peuvent également être utilisés pour décrire le contenu d’un <xref:System.Windows.Media.GeometryDrawing> ou un <xref:System.Windows.Media.DrawingContext>. Ils peuvent également être utilisés pour le découpage et le test de positionnement.  
  
 Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).
