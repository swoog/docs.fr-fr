---
title: 'Procédure : Effectuer un test de positionnement avec Geometry comme paramètre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects using Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], hit tests on visual objects [WPF]
ms.assetid: 6c8bdbf2-19e0-4fbb-bf89-c1252b2ebc61
ms.openlocfilehash: d52f8da891ecdf632952c441f94aab4c0b56da7f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564251"
---
# <a name="how-to-hit-test-using-geometry-as-a-parameter"></a>Procédure : Effectuer un test de positionnement avec Geometry comme paramètre
Cet exemple montre comment effectuer un test de positionnement sur un objet visuel à l’aide un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment configurer un test de positionnement à l’aide <xref:System.Windows.Media.GeometryHitTestParameters> pour le <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> (méthode). Le <xref:System.Windows.Point> valeur qui est passée à la `OnMouseDown` méthode est utilisée pour créer un <xref:System.Windows.Media.Geometry> objet afin d’étendre la plage du test d’atteinte.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet10)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet10)]  
  
 Le <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété du <xref:System.Windows.Media.GeometryHitTestResult> fournit des informations sur les résultats d’un test d’atteinte qui utilise un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre. L’illustration suivante montre la relation entre la géométrie du test de positionnement (le cercle bleu) et le contenu restitué de l’objet visuel cible (le carré rouge).  
  
 ![Diagramme du IntersectionDetail utilisé dans le test de positionnement](../../../../docs/framework/wpf/graphics-multimedia/media/intersectiondetail01.png "IntersectionDetail01")  
Intersection entre la géométrie du test de positionnement et l’objet visuel cible  
  
 L’exemple suivant montre comment implémenter un rappel de test de positionnement lorsqu’un <xref:System.Windows.Media.Geometry> est utilisé comme un paramètre de test de positionnement. Le `result` paramètre est casté en un <xref:System.Windows.Media.GeometryHitTestResult> afin de récupérer la valeur de la <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété. La valeur de propriété vous permet de déterminer si le <xref:System.Windows.Media.Geometry> paramètre de test de positionnement est entièrement ou partiellement contenu dans le contenu restitué de la cible du test d’atteinte. Dans ce cas, l’exemple de code ajoute à la liste les résultats du test de positionnement uniquement pour les objets visuels qui sont entièrement contenus dans les limites de la cible.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet11)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet11)]  
  
> [!NOTE]
>  Le <xref:System.Windows.Media.HitTestResult> rappel ne doit pas être appelé lorsque le détail de l’intersection est <xref:System.Windows.Media.IntersectionDetail.Empty>.  
  
## <a name="see-also"></a>Voir aussi
- [Test de positionnement dans la couche visuelle](../../../../docs/framework/wpf/graphics-multimedia/hit-testing-in-the-visual-layer.md)
- [Effectuer un test de positionnement avec Geometry dans un Visual](../../../../docs/framework/wpf/graphics-multimedia/how-to-hit-test-geometry-in-a-visual.md)
