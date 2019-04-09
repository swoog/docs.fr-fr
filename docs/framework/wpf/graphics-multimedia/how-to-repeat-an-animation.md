---
title: 'Procédure : Répéter une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatBehavior property of timelines [WPF]
- repeating animating [WPF]
- Timelines RepeatBehavior property [WPF]
- animation [WPF], repeating
ms.assetid: e6f3b068-eeeb-47fd-8d40-8848c31f1e1e
ms.openlocfilehash: a80f72b0e67c13890d4befcbd5ab7c4a92a93fe7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150538"
---
# <a name="how-to-repeat-an-animation"></a>Procédure : Répéter une animation
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> afin de contrôler le comportement de répétition d’une animation.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> contrôle le nombre de fois où une animation répète sa durée simple. À l’aide de <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>, vous pouvez spécifier qu’un <xref:System.Windows.Media.Animation.Timeline> se répète pour un certain nombre de fois (nombre d’itérations) ou pour une période de temps spécifié. Dans les deux cas, l’animation passe par les exécutions de début-fin autant dont il a besoin pour remplir la durée ou au nombre demandé.  
  
 Par défaut, les chronologies ont un nombre de répétitions de 1.0, ce qui signifie qu’ils jouent une seule fois et ne se répètent pas. Toutefois, si vous définissez la <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> à <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A>, la chronologie se répète indéfiniment.  
  
 L’exemple suivant montre comment utiliser le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété pour contrôler le comportement de répétition d’une animation. L’exemple anime le <xref:System.Windows.FrameworkElement.Width%2A> propriété de cinq rectangles avec chaque rectangle à l’aide d’un autre type de comportement de répétition.  
  
 [!code-xaml[timingbehaviors_snip#RepeatBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/RepeatBehaviorExample.xaml#repeatbehaviorwholepage)]  
  
 Pour obtenir un exemple complet, consultez [comportement de minutage d’Animation exemple](https://go.microsoft.com/fwlink/?LinkID=159970).  
  
## <a name="see-also"></a>Voir aussi

- [Accumuler des valeurs d’animation pendant des cycles de répétition](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [Spécifier l’inversion automatique d’une chronologie](how-to-specify-whether-a-timeline-automatically-reverses.md)
- [Rubriques "Comment" relatives à l'animation et au minutage](animation-and-timing-how-to-topics.md)
- [Vue d'ensemble de l'animation](animation-overview.md)
- [Comportement de minutage d’animation exemple](https://go.microsoft.com/fwlink/?LinkID=159970)
