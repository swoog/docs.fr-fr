---
title: 'Procédure : Accumuler des valeurs d’animation pendant des cycles de répétition'
ms.date: 03/30/2017
helpviewer_keywords:
- accumulating animation values across repeating cycles [WPF]
- animation [WPF], accumulating values across repeating cycles
ms.assetid: 548df369-c7cc-4dab-b569-08b95ced2e7e
ms.openlocfilehash: 4b739883322751e2df86e13bfd07249abdb10a08
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59146014"
---
# <a name="how-to-accumulate-animation-values-during-repeat-cycles"></a>Procédure : Accumuler des valeurs d’animation pendant des cycles de répétition
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> propriété à accumuler des valeurs d’animation des cycles de répétition.  
  
## <a name="example"></a>Exemple  
 Utilisez le <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> propriété à accumuler des valeurs de base d’une animation sur des cycles de répétition. Par exemple, si vous définissez une animation se répète 9 fois (<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> = « 9 x ») et que vous définissez la propriété à animer entre 10 et 15 (de = 10 à = 15), la propriété s’anime de 10 à 15 pendant le premier cycle, de 15 à 20 pendant le deuxième cycle , de 20 à 25 pendant le troisième cycle et ainsi de suite. Par conséquent, chaque cycle d’animation utilise la valeur de l’animation de fin du cycle d’animation précédente comme sa valeur de base.  
  
 Vous pouvez utiliser le `IsCumulative` propriété avec des animations plus simples et la plupart des animations d’image clé. Pour plus d’informations, consultez [vue d’ensemble de l’Animation](animation-overview.md) et [vue d’ensemble des Animations image clé](key-frame-animations-overview.md).  
  
 L’exemple suivant illustre ce comportement en animant la largeur de quatre rectangles. L’exemple :  
  
-   Anime le premier rectangle avec <xref:System.Windows.Media.Animation.DoubleAnimation> et définit le <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> propriété `true`.  
  
-   Anime le deuxième rectangle avec <xref:System.Windows.Media.Animation.DoubleAnimation> et définit le <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> propriété à la valeur par défaut de `false`.  
  
-   Anime le troisième rectangle avec <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> et définit le <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> propriété `true`.  
  
-   Anime le dernier rectangle avec <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> et définit le <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> propriété `false`.  
  
 [!code-xaml[timingbehaviors_snip#IsCumulativeWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsCumulativeExample.xaml#iscumulativewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Ajouter une valeur de sortie d'animation à une valeur de départ d'animation](how-to-add-an-animation-output-value-to-an-animation-starting-value.md)
- [Répéter une animation](how-to-repeat-an-animation.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Rubriques de guide pratique](animation-and-timing-how-to-topics.md)
