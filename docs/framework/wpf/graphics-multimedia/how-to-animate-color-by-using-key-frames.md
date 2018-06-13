---
title: "Comment : animer une couleur à l'aide d'images clés"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [WPF], animating with key frames
- animation [WPF], colors with key frames
- key frames [WPF], animating colors with
ms.assetid: ab04ffa6-4de9-4d5b-a3b4-4e35d5b2ef35
ms.openlocfilehash: 7d89a1f9c24c93bd6b05265092bde09e8cf6eff5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33560330"
---
# <a name="how-to-animate-color-by-using-key-frames"></a>Comment : animer une couleur à l'aide d'images clés
Cet exemple montre comment animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> d’un <xref:System.Windows.Media.SolidColorBrush> à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> propriété d’un <xref:System.Windows.Media.SolidColorBrush>. Cette animation utilise trois images clés de la manière suivante :  
  
1.  Pendant les deux premières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.LinearColorKeyFrame> classe à modifier progressivement la couleur du vert au rouge. Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearColorKeyFrame> créer une transition linéaire fluide entre les valeurs.  
  
2.  À la fin de la prochaine demi-seconde, utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> classe permettant de rapidement changer la couleur du rouge au jaune. Les images clés discrètes telles que <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> créer des changements soudains entre les valeurs, autrement dit, le changement de couleur dans cette partie de l’animation se produit rapidement et n’est pas subtil.  
  
3.  Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame> classe pour modifier la couleur à nouveau, cette fois du jaune en vert. Les images clés spline comme <xref:System.Windows.Media.Animation.SplineColorKeyFrame> créer une transition entre des valeurs en fonction des valeurs de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame.KeySpline%2A> propriété. Dans cet exemple, le changement de couleur commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-csharp[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/ColorAnimationUsingKeyFramesExample.cs#coloranimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/coloranimationusingkeyframesexample.vb#coloranimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ColorAnimationUsingKeyFramesExample.xaml#coloranimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](http://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.SolidColorBrush.Color%2A>  
 <xref:System.Windows.Media.SolidColorBrush>  
 <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames>  
 [Vue d'ensemble des animations d'image clé](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Guides pratiques relatifs aux images clés](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
