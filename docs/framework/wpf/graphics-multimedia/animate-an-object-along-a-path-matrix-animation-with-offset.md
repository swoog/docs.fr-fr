---
title: "Procédure : Animer un objet sur un tracé (animation de matrice avec accumulation d'offsets)"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- offset accumulation [WPF]
- animation [WPF], objects along paths (matrix animation with offset accumulation)
- matrix animation with offset accumulation [WPF]
ms.assetid: 1bca90ef-9832-4128-8ed6-62908e7ec146
ms.openlocfilehash: e5e619de8b90737136559db134a131fdc1833fb9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640093"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation-with-offset-accumulation"></a>Procédure : Animer un objet sur un tracé (animation de matrice avec accumulation d'offsets)
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> classe pour animer un objet sur un tracé et faire en sorte que cette animation accumule son décalage valeurs lorsqu’elle se répète.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet à animer le <xref:System.Windows.Media.MatrixTransform.Matrix%2A> propriété d’un <xref:System.Windows.Media.MatrixTransform> appliqué à un bouton. Le bouton se déplace alors le long d’un tracé courbe.  
  
 En outre, l’exemple définit le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> propriété `true`, ce qui entraîne le décalage de la matrice animée lorsque l’animation se répète. Étant donné que les valeurs d’offset s’accumulent, le bouton s’éloigne sur l’écran lorsque l’animation se répète, sans revenir à sa position de départ.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathOffsetCumulativeWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexampleoffsetcumulative.xaml#matrixanimationusingpathoffsetcumulativewholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathOffsetCumulativeWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExampleOffsetCumulative.cs#matrixanimationusingpathoffsetcumulativewholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathOffsetCumulativeWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExampleOffsetCumulative.vb#matrixanimationusingpathoffsetcumulativewholepage)]  
  
 Notez que, bien que le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> propriété entraîne des valeurs offset s’accumulent au fil des répétitions, elle n’entraîne pas accumuler des valeurs de rotation. Pour rendre les valeurs de rotation s’accumulent, définir l’animation <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> et <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsAngleCumulative%2A> propriétés à `true`.  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028). Pour obtenir un exemple montrant comment animer un <xref:System.Windows.Media.Matrix> valeur sur un tracé sans accumulation d’offsets, consultez [animer un objet sur un tracé (Animation de matrice)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md).  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Guides pratiques relatifs aux animations de tracés](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
