---
title: "Comment : animer des modifications de taille à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- key frames [WPF], animating size changes with
- animation [WPF], size changes with key frames
- size changes [WPF], animating with key frames
ms.assetid: 86bd2950-d4c9-4ec4-aa8d-7dc3ccadded4
ms.openlocfilehash: 69845d1d75f81042bbeb20ee6b1015f5c2f53b81
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43672556"
---
# <a name="how-to-animate-size-changes-by-using-key-frames"></a>Comment : animer des modifications de taille à l'aide d'images clés
Cet exemple explique comment animer des modifications de taille à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.ArcSegment.Size%2A> propriété d’un <xref:System.Windows.Media.ArcSegment>. Cette animation utilise trois images clés de la manière suivante :  
  
1.  Pendant la première demi-seconde de l’animation, utilise une instance de la <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> classe pour augmenter progressivement la taille de l’arc. Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> créent une transition linéaire fluide entre les valeurs.  
  
2.  À la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> classe pour augmenter soudainement la taille de l’arc. Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> créent des changements soudains entre les valeurs, autrement dit, les modifications de taille se produisent soudainement et ne sont pas subtiles.  
  
3.  Sur les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> classe pour augmenter la taille de l’arc. Les images clés spline comme <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineSizeKeyFrame.KeySpline%2A> propriété. Dans cet exemple, la taille de l’arc augmente lentement dans un premier temps, puis augmente de façon exponentielle vers la fin du segment temporel.  
  
 [!code-xaml[keyframes_snip#SizeAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/SizeAnimationUsingKeyFramesExample.xaml#sizeanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames>  
 <xref:System.Windows.Media.ArcSegment.Size%2A>  
 <xref:System.Windows.Media.ArcSegment>  
 <xref:System.Windows.Media.Animation.LinearSizeKeyFrame>  
 <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame>  
 <xref:System.Windows.Media.Animation.SplineSizeKeyFrame>  
 [Vue d'ensemble des animations d'image clé](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Guides pratiques relatifs aux images clés](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
