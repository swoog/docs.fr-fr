---
title: 'Comment : définir une durée pour une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: df9e12e1bd3a365c3013d0f75df663bd46186ee2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33561373"
---
# <a name="how-to-set-a-duration-for-an-animation"></a>Comment : définir une durée pour une animation
A <xref:System.Windows.Media.Animation.Timeline> représente un segment de temps et de la longueur de ce segment sont déterminées par la chronologie <xref:System.Windows.Duration>. Lorsqu’un <xref:System.Windows.Media.Animation.Timeline> atteint la fin de sa durée, il s’arrête. Si le <xref:System.Windows.Media.Animation.Timeline> a des chronologies enfants, ils cessent de jouer également. Dans le cas d’une animation, la <xref:System.Windows.Duration> spécifie la durée nécessaire à l’animation transition à partir de sa valeur initiale à sa valeur de fin.  
  
 Vous pouvez spécifier un <xref:System.Windows.Duration> avec une durée finie spécifique ou les valeurs spéciales <xref:System.Windows.Duration.Automatic%2A> ou <xref:System.Windows.Duration.Forever%2A>. Durée d’une animation doit toujours être une valeur d’heure, car une animation doit toujours avoir une longueur finie spécifique, dans le cas contraire, l’animation ne serait pas capable d’effectuer la transition entre ses valeurs cibles. Les chronologies de conteneur (<xref:System.Windows.Media.Animation.TimelineGroup> objets), tel que <xref:System.Windows.Media.Animation.Storyboard> et <xref:System.Windows.Media.Animation.ParallelTimeline>, ont une durée par défaut de <xref:System.Windows.Duration.Automatic%2A>, ce qui signifie qu’elles se terminent automatiquement lorsque leur dernier enfant s’arrête.  
  
 Dans la couleur d’exemple, la largeur, la hauteur et remplissage suivante d’un <xref:System.Windows.Shapes.Rectangle> est animée. Les durées sont définies sur des chronologies d’animation et de conteneur entraîne des effets d’animation, y compris le contrôle de la vitesse perçue d’une animation et la substitution de la durée des chronologies enfants avec la durée d’une chronologie de conteneur.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Duration>  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
