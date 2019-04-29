---
title: 'Procédure : Animer l’épaisseur d’une bordure à l’aide d’images clés'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: 101fd077bf125faadbd9a0186c2282e4b20ee78f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699030"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a>Procédure : Animer l’épaisseur d’une bordure à l’aide d’images clés
Cet exemple montre comment animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>. Cette animation utilise trois images clés de la manière suivante :  
  
1. Pendant la première demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> classe pour augmenter progressivement l’épaisseur de la bordure. L’exemple utilise <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> pour créer une augmentation linéaire fluide entre les valeurs.  
  
2. À la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> classe pour augmenter soudainement l’épaisseur de la bordure. Les images clés discrètes comme celles dérivées de <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> créent des changements soudains entre les valeurs, autrement dit, le déplacement de l’animation est saccadé.  
  
3. Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> classe pour diminuer l’épaisseur de la bordure. Images clés spline comme celles dérivées de <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> propriété. Dans cette image clé, l’animation commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Guides pratiques relatifs aux images clés](key-frame-animation-how-to-topics.md)
- [Animer une valeur BorderThickness](../controls/how-to-animate-a-borderthickness-value.md)
