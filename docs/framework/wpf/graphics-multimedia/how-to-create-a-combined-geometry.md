---
title: 'Procédure : Créer une géométrie combinée'
ms.date: 03/30/2017
helpviewer_keywords:
- combining geometries [WPF]
- graphics [WPF], combining geometries
- geometries [WPF], combining
ms.assetid: 54c3277c-6b6e-4b25-91be-fda0bbc706b4
ms.openlocfilehash: c5ebe87abd4c2cf70f8fa17f1fcc773293f3ad27
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910086"
---
# <a name="how-to-create-a-combined-geometry"></a>Procédure : Créer une géométrie combinée
Cet exemple montre comment combiner des géométries. Pour combiner deux géométries, utilisez un <xref:System.Windows.Media.CombinedGeometry> objet. Définir son <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> propriétés avec les deux géométries à combiner, puis définissez le <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> propriété, qui détermine la façon dont les géométries seront combinées ensemble, à `Union`, `Intersect`, `Exclude`, ou `Xor`.  
  
 Pour créer une géométrie composite à partir de deux ou plusieurs des géométries, utilisez un <xref:System.Windows.Media.GeometryGroup>.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode de géométrie combinée `Exclude`.  Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.  
  
 [!code-xaml[GeometrySample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#21)]  
  
 ![Mode de combinaison de résultats de l’exclusion](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")  
Exclusion de la géométrie combinée  
  
 Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Intersect`.  Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.  
  
 [!code-xaml[GeometrySample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#22)]  
  
 ![Mode de combinaison de résultats de l’intersection](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")  
Géométrie combinée Intersect  
  
 Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Union`.  Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.  
  
 [!code-xaml[GeometrySample#23](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#23)]  
  
 ![Résultats du mode d’association Union](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")  
Géométrie combinée Union  
  
 Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Xor`.  Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.  
  
 [!code-xaml[GeometrySample#24](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#24)]  
  
 ![Résultats du mode d’association Xor](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")  
Géométrie combinée Xor
