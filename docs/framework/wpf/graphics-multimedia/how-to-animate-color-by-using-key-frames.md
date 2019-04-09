---
title: 'Procédure : Animer une couleur à l’aide d’images clés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [WPF], animating with key frames
- animation [WPF], colors with key frames
- key frames [WPF], animating colors with
ms.assetid: ab04ffa6-4de9-4d5b-a3b4-4e35d5b2ef35
ms.openlocfilehash: d911b1f14cf71aebf95b566eb710fec8ec9e2a29
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59095165"
---
# <a name="how-to-animate-color-by-using-key-frames"></a>Procédure : Animer une couleur à l’aide d’images clés
Cet exemple montre comment animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> d’un <xref:System.Windows.Media.SolidColorBrush> à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> propriété d’un <xref:System.Windows.Media.SolidColorBrush>. Cette animation utilise trois images clés de la manière suivante :  
  
1.  Pendant les deux premières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.LinearColorKeyFrame> classe à modifier progressivement la couleur du vert au rouge. Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearColorKeyFrame> créent une transition linéaire fluide entre les valeurs.  
  
2.  Lors de la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> classe pour rapidement changer la couleur du rouge au jaune. Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> créent des changements soudains entre les valeurs, autrement dit, la modification de couleur dans cette partie de l’animation se produit rapidement et n’est pas subtile.  
  
3.  Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame> classe pour modifier la couleur à nouveau, cette fois du jaune au vert. Les images clés spline comme <xref:System.Windows.Media.Animation.SplineColorKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame.KeySpline%2A> propriété. Dans cet exemple, le changement de couleur commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-csharp[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/ColorAnimationUsingKeyFramesExample.cs#coloranimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/coloranimationusingkeyframesexample.vb#coloranimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ColorAnimationUsingKeyFramesExample.xaml#coloranimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.SolidColorBrush.Color%2A>
- <xref:System.Windows.Media.SolidColorBrush>
- <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames>
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Guides pratiques relatifs aux images clés](key-frame-animation-how-to-topics.md)
