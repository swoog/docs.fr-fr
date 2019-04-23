---
title: 'Procédure : Définir la durée d’une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: bdae1689ffeb8c54d756b9debbd26d57a052892d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198788"
---
# <a name="how-to-set-a-duration-for-an-animation"></a>Procédure : Définir la durée d’une animation
Un <xref:System.Windows.Media.Animation.Timeline> représente un segment de temps et la longueur de ce segment sont déterminées par la chronologie <xref:System.Windows.Duration>. Quand un <xref:System.Windows.Media.Animation.Timeline> atteint la fin de sa durée, elle s’arrête. Si le <xref:System.Windows.Media.Animation.Timeline> a des chronologies enfants, celles-ci s’arrêtent également. Dans le cas d’une animation, la <xref:System.Windows.Duration> spécifie la durée pendant laquelle l’animation nécessaire pour passer de sa valeur initiale à sa valeur finale.  
  
 Vous pouvez spécifier un <xref:System.Windows.Duration> avec une durée finie spécifique ou des valeurs spéciales <xref:System.Windows.Duration.Automatic%2A> ou <xref:System.Windows.Duration.Forever%2A>. Durée d’une animation doit toujours être une valeur de temps, car une animation doit toujours avoir une longueur finie spécifique, dans le cas contraire, l’animation ne serait pas capable d’effectuer la transition entre ses valeurs cibles. Les chronologies de conteneur (<xref:System.Windows.Media.Animation.TimelineGroup> objets), tel que <xref:System.Windows.Media.Animation.Storyboard> et <xref:System.Windows.Media.Animation.ParallelTimeline>, ont une durée par défaut de <xref:System.Windows.Duration.Automatic%2A>, ce qui signifie qu’elles se terminent automatiquement lorsque leur dernier enfant s’arrête.  
  
 Dans la couleur d’exemple, de la largeur, hauteur et remplissage suivante d’un <xref:System.Windows.Shapes.Rectangle> est animée. Les durées sont définies sur les chronologies d’animation et de conteneur entraînant des effets d’animation, y compris le contrôle de la vitesse perçue d’une animation et la substitution de la durée des chronologies enfants avec la durée d’une chronologie de conteneur.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Duration>
- [Vue d’ensemble de l’animation](animation-overview.md)
