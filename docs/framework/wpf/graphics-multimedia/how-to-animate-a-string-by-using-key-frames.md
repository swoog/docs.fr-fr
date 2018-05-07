---
title: "Comment : animer une chaîne à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], strings with key frames
- strings [WPF], animating with key frames
- key frames [WPF], animating strings with
ms.assetid: c62bc9fd-c09a-4227-bce0-0a1ab82049dd
ms.openlocfilehash: 5219ce11667c84d3ceca380d5a4ddd52695736b9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-animate-a-string-by-using-key-frames"></a>Comment : animer une chaîne à l'aide d'images clés
Cet exemple montre comment animer une chaîne qui, dans cet exemple est la <xref:System.Windows.Controls.ContentControl.Content%2A> propriété d’un <xref:System.Windows.Controls.Button> contrôle, à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Controls.ContentControl.Content%2A> propriété d’un <xref:System.Windows.Controls.Button>.  
  
 Toutes les images clés de cet exemple montre comment utilisent une instance de la <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> classe car une animation de chaîne qui est créée avec des images clés peut uniquement utiliser des images clés discrètes. Les images clés discrètes telles que <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> créer soudains entre les valeurs, autrement dit, les modifications apportées à l’animation se produisent rapidement et ne sont pas subtiles.  
  
 [!code-xaml[keyframes_snip#StringAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/StringAnimationUsingKeyFramesExample.xaml#stringanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](http://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>  
 <xref:System.Windows.Controls.ContentControl.Content%2A>  
 <xref:System.Windows.Controls.Button>  
 <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>  
 [Vue d'ensemble des animations d'image clé](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Guides pratiques relatifs aux images clés](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
