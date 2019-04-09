---
title: 'Procédure : Spécifier l’origine d’une transformation à l’aide de valeurs relatives'
ms.date: 03/30/2017
helpviewer_keywords:
- origins of Transforms [WPF]
- Transforms [WPF], origins of
- graphics [WPF], origins of Transforms
ms.assetid: f4dbc29d-93c7-41cd-96d8-5cfd8624b470
ms.openlocfilehash: 48b3b0df8dab8516873495a996074eae57ffe00f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59082956"
---
# <a name="how-to-specify-the-origin-of-a-transform-by-using-relative-values"></a>Procédure : Spécifier l’origine d’une transformation à l’aide de valeurs relatives
Cet exemple montre comment utiliser des valeurs relatives pour spécifier l’origine d’un <xref:System.Windows.UIElement.RenderTransform%2A> qui est appliqué à un <xref:System.Windows.FrameworkElement>.  
  
 Lorsque vous faites pivoter, mettre à l’échelle ou incliner un <xref:System.Windows.FrameworkElement> à l’aide de la <xref:System.Windows.UIElement.RenderTransform%2A> propriété, le paramètre par défaut applique la transformation à l’angle supérieur gauche de l’élément. Si vous souhaitez effectuer un pivotement, une mise à l’échelle ou une inclinaison à partir du centre de l’élément, vous pouvez compenser en définissant le centre de la transformation sur le centre de l’élément. Cette solution suppose toutefois de connaître la taille de l’élément. Un moyen plus simple d’appliquer une transformation au centre d’un élément consiste à définir son <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété à (0,5, 0,5), au lieu de définir une valeur de centre sur la transformation elle-même.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.RotateTransform> pour faire pivoter un <xref:System.Windows.Controls.Button> 45 degrés dans le sens horaire. L’exemple ne spécifie pas de centre, donc le bouton pivote autour du point (0, 0), qui se trouve dans le coin supérieur gauche. Le <xref:System.Windows.Media.RotateTransform> est appliqué à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété.  
  
 L’illustration suivante montre le résultat de la transformation pour l’exemple qui suit.  
  
 ![Bouton transformé à l’aide de RenderTransform](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")  
Rotation de 45 degrés dans le sens des aiguilles d’une montre à l’aide de la propriété RenderTransform  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample1)]  
  
 L’exemple suivant utilise également un <xref:System.Windows.Media.RotateTransform> pour faire pivoter un <xref:System.Windows.Controls.Button> 45 degrés dans le sens horaire ; Toutefois, cet exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> du bouton à (0,5, 0,5). Par conséquent, la rotation est appliquée au centre du bouton et non sur son coin supérieur gauche.  
  
 L’illustration suivante montre le résultat de la transformation pour l’exemple qui suit.  
  
 ![Bouton transformé autour de son centre](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")  
Rotation de 45 degrés à l’aide de la propriété RenderTransform avec un RenderTransformOrigin de (0,5, 0,5)  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample2)]  
  
 Pour plus d’informations sur la transformation <xref:System.Windows.FrameworkElement> , voir la [transforme la vue d’ensemble](transforms-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Transform>
- [Vue d'ensemble des transformations](transforms-overview.md)
- [Rubriques Comment](transformations-how-to-topics.md)
