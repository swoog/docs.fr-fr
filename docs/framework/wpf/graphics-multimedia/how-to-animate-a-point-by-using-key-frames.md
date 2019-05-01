---
title: 'Procédure : Animer un point à l’aide d’images clés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating Points with
- Points [WPF], animating with key frames
- animation [WPF], Points with key frames
ms.assetid: d2e2ef10-0773-4133-856e-d41c09f60ded
ms.openlocfilehash: b706568a0e8221aac737780592882f728f0f9e9c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62010161"
---
# <a name="how-to-animate-a-point-by-using-key-frames"></a>Procédure : Animer un point à l’aide d’images clés
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> classe pour animer un <xref:System.Windows.Point>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déplace une ellipse sur un tracé triangulaire. L’exemple utilise le <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété d’un <xref:System.Windows.Media.EllipseGeometry>. Cette animation utilise trois images clés de la manière suivante :  
  
1. Pendant la première demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.LinearPointKeyFrame> classe pour déplacer l’ellipse le long d’un chemin d’accès à une vitesse constante depuis sa position de départ. Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearPointKeyFrame> créent une interpolation linéaire fluide entre les valeurs.  
  
2. Lors de la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> classe pour déplacer soudainement l’ellipse le long du chemin d’accès à la position suivante. Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscretePointKeyFrame> créent des changements soudains entre les valeurs.  
  
3. Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplinePointKeyFrame> classe pour ramener l’ellipse à sa position de départ. Les images clés spline comme <xref:System.Windows.Media.Animation.SplinePointKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplinePointKeyFrame.KeySpline%2A> propriété. Dans cet exemple, l’animation commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-csharp[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/PointAnimationUsingKeyFramesExample.cs#pointanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/pointanimationusingkeyframesexample.vb#pointanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#PointAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/PointAnimationUsingKeyFramesExample.xaml#pointanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
 Par souci de cohérence avec d’autres exemples d’animation, les versions de code de cet exemple utilisent un <xref:System.Windows.Media.Animation.Storyboard> objet pour appliquer le <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>. Toutefois, lorsque vous appliquez une seule animation dans le code, il est plus simple d’utiliser le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> méthode au lieu d’utiliser un <xref:System.Windows.Media.Animation.Storyboard>. Si vous voulez voir un exemple, consultez l’article [Comment : animer une propriété sans utiliser de storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.PointAnimationUsingKeyFrames>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A?displayProperty=nameWithType>
- <xref:System.Windows.Media.EllipseGeometry>
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Guides pratiques relatifs aux images clés](key-frame-animation-how-to-topics.md)
