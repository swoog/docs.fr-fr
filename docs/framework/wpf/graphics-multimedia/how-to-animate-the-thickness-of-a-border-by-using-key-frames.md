---
title: "Comment : animer l'épaisseur d'une bordure à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: a601fd6779a4d912166366652435aff9ae37613f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43421408"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a>Comment : animer l'épaisseur d'une bordure à l'aide d'images clés
Cet exemple montre comment animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>. Cette animation utilise trois images clés de la manière suivante :  
  
1.  Pendant la première demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> classe pour augmenter progressivement l’épaisseur de la bordure. L’exemple utilise <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> pour créer une augmentation linéaire fluide entre les valeurs.  
  
2.  À la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> classe pour augmenter soudainement l’épaisseur de la bordure. Les images clés discrètes comme celles dérivées de <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> créent des changements soudains entre les valeurs, autrement dit, le déplacement de l’animation est saccadé.  
  
3.  Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> classe pour diminuer l’épaisseur de la bordure. Images clés spline comme celles dérivées de <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> propriété. Dans cette image clé, l’animation commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>  
 <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>  
 <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>  
 [Vue d'ensemble des animations d'image clé](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Guides pratiques relatifs aux images clés](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)  
 [Animer une valeur BorderThickness](../../../../docs/framework/wpf/controls/how-to-animate-a-borderthickness-value.md)
