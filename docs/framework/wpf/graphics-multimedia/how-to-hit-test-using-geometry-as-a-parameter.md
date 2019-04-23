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
ms.openlocfilehash: 73420d6ae1386676ed900e91b3951df9e0934db8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59100962"
---
# <a name="how-to-hit-test-using-geometry-as-a-parameter"></a>Procédure : Effectuer un test de positionnement avec Geometry comme paramètre
Cet exemple montre comment effectuer un test de positionnement sur un objet visuel à l’aide un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment configurer un test de positionnement à l’aide <xref:System.Windows.Media.GeometryHitTestParameters> pour le <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> (méthode). Le <xref:System.Windows.Point> valeur qui est passée à la `OnMouseDown` méthode est utilisée pour créer un <xref:System.Windows.Media.Geometry> objet afin d’étendre la plage du test d’atteinte.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet10)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet10)]  
  
 Le <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété du <xref:System.Windows.Media.GeometryHitTestResult> fournit des informations sur les résultats d’un test d’atteinte qui utilise un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre. L’illustration suivante montre la relation entre la géométrie du test de positionnement (le cercle bleu) et le contenu restitué de l’objet visuel cible (le carré rouge).  
  
 ![Diagramme illustrant IntersectionDetail utilisé dans le test de positionnement.](./media/how-to-hit-test-using-geometry-as-a-parameter/intersectiondetail-hit-test.png)  
  
 L’exemple suivant montre comment implémenter un rappel de test de positionnement lorsqu’un <xref:System.Windows.Media.Geometry> est utilisé comme un paramètre de test de positionnement. Le `result` paramètre est casté en un <xref:System.Windows.Media.GeometryHitTestResult> afin de récupérer la valeur de la <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété. La valeur de propriété vous permet de déterminer si le <xref:System.Windows.Media.Geometry> paramètre de test de positionnement est entièrement ou partiellement contenu dans le contenu restitué de la cible du test d’atteinte. Dans ce cas, l’exemple de code ajoute à la liste les résultats du test de positionnement uniquement pour les objets visuels qui sont entièrement contenus dans les limites de la cible.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet11)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet11)]  
  
> [!NOTE]
>  Le <xref:System.Windows.Media.HitTestResult> rappel ne doit pas être appelé lorsque le détail de l’intersection est <xref:System.Windows.Media.IntersectionDetail.Empty>.  
  
## <a name="see-also"></a>Voir aussi

- [Test de positionnement dans la couche visuelle](hit-testing-in-the-visual-layer.md)
- [Effectuer un test de positionnement avec Geometry dans un Visual](how-to-hit-test-geometry-in-a-visual.md)
