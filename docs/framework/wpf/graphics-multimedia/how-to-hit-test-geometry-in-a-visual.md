---
title: 'Procédure : Effectuer un test de positionnement avec Geometry dans un Visual'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects comprising Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], visual objects comprising
ms.assetid: 8bf2643f-d7f9-4cb4-9ea6-5b893c23200d
ms.openlocfilehash: 87b626e575d889447ef061d1ed62ef28efe5dfeb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947340"
---
# <a name="how-to-hit-test-geometry-in-a-visual"></a>Procédure : Effectuer un test de positionnement avec Geometry dans un Visual
Cet exemple montre comment effectuer un test de positionnement sur un objet visuel composé d’un ou plusieurs <xref:System.Windows.Media.Geometry> objets.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment récupérer le <xref:System.Windows.Media.DrawingGroup> à partir d’un objet visuel qui utilise le <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> (méthode). Un test de positionnement est ensuite effectué sur le contenu rendu de chaque dessin dans le <xref:System.Windows.Media.DrawingGroup> pour déterminer la géométrie atteinte.  
  
> [!NOTE]
>  Dans la plupart des cas, vous utiliseriez le <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> méthode pour déterminer si un point croise le contenu rendu d’un objet visuel.  
  
 [!code-csharp[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsOverview/CSharp/Window1.xaml.cs#visualsoverviewsnippet4)]
 [!code-vb[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsOverview/visualbasic/window1.xaml.vb#visualsoverviewsnippet4)]  
  
 Le <xref:System.Windows.Media.Geometry.FillContains%2A> méthode est une méthode surchargée qui vous permet de test de positionnement en utilisant un <xref:System.Windows.Point> ou <xref:System.Windows.Media.Geometry>. Si une géométrie est barrée, le trait peut s’étendre en dehors des limites du remplissage. Dans ce cas, vous souhaitez appeler <xref:System.Windows.Media.Geometry.StrokeContains%2A> outre <xref:System.Windows.Media.Geometry.FillContains%2A>.  
  
 Vous pouvez également fournir un <xref:System.Windows.Media.ToleranceType> qui est utilisé dans le cadre de la mise à plat de Bézier.  
  
> [!NOTE]
>  Cet exemple ne prend pas en compte les transformations ou les découpages qui peuvent être appliqués à la géométrie. En outre, cet exemple ne fonctionnera pas avec un contrôle sur lequel est appliqué un style, car aucun dessin ne lui est directement associé.  
  
## <a name="see-also"></a>Voir aussi

- [Test de positionnement dans la couche visuelle](hit-testing-in-the-visual-layer.md)
- [Effectuer un test de positionnement avec Geometry comme paramètre](how-to-hit-test-using-geometry-as-a-parameter.md)
