---
title: 'Procédure : Utiliser des déclencheurs d’événements pour contrôler une table de montage séquentiel après son démarrage'
ms.date: 03/30/2017
helpviewer_keywords:
- triggers [WPF], controlling Storyboards
- event triggers [WPF], controlling Storyboards
- Storyboards [WPF], controlling after start
ms.assetid: 3b115594-6a93-4972-b24d-61aa16f1c15f
ms.openlocfilehash: e0bc019ee361cba6a28ac573da3d2ee09e2168ed
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663303"
---
# <a name="how-to-use-event-triggers-to-control-a-storyboard-after-it-starts"></a>Procédure : Utiliser des déclencheurs d’événements pour contrôler une table de montage séquentiel après son démarrage
Cet exemple montre comment contrôler un <xref:System.Windows.Media.Animation.Storyboard> après son démarrage. Pour démarrer un <xref:System.Windows.Media.Animation.Storyboard> à l’aide de [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], utilisez <xref:System.Windows.Media.Animation.BeginStoryboard>, qui distribue les animations aux objets et aux propriétés qu’ils animent, puis démarre le storyboard. Si vous donnez <xref:System.Windows.Media.Animation.BeginStoryboard> un nom en spécifiant son <xref:System.Windows.Media.Animation.BeginStoryboard.Name%2A> propriété, vous rendiez une table de montage séquentiel contrôlable. Vous pouvez ensuite contrôler interactivement la table de montage séquentiel après son démarrage.  
  
 Utilisez les actions suivantes de la table de montage séquentiel avec <xref:System.Windows.EventTrigger> objets pour contrôler un storyboard.  
  
- <xref:System.Windows.Media.Animation.PauseStoryboard>: Suspend le storyboard.  
  
- <xref:System.Windows.Media.Animation.ResumeStoryboard>: Reprend un storyboard suspendu.  
  
- <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>: Modifie la vitesse de la table de montage séquentiel.  
  
- <xref:System.Windows.Media.Animation.SkipStoryboardToFill>: Fait avancer une table de montage séquentiel à la fin de sa période de remplissage, le cas échéant.  
  
- <xref:System.Windows.Media.Animation.StopStoryboard>: Arrête le storyboard.  
  
- <xref:System.Windows.Media.Animation.RemoveStoryboard>: Supprime la table de montage séquentiel, libérant ainsi des ressources.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise des actions de la table de montage séquentiel contrôlable pour contrôler un storyboard de façon interactive.  
  
 **Remarque :** Pour voir un exemple de contrôle d’une table de montage séquentiel à l’aide de code, consultez [contrôler un Storyboard après qu’il démarre à l’aide de ses méthodes interactives](how-to-control-a-storyboard-after-it-starts.md).  
  
 [!code-xaml[timingbehaviors_snip#ControlStoryboardExampleUsingWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/ControlStoryboardExample.xaml#controlstoryboardexampleusingwholepage)]  
  
 Pour obtenir des exemples supplémentaires, consultez le [Galerie d’exemples d’Animation](https://go.microsoft.com/fwlink/?LinkID=159969).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.ResumeStoryboard>
- <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>
- <xref:System.Windows.Media.Animation.SkipStoryboardToFill>
- <xref:System.Windows.Media.Animation.PauseStoryboard>
- <xref:System.Windows.Media.Animation.StopStoryboard>
- <xref:System.Windows.Media.Animation.SeekStoryboard>
- [Contrôler un storyboard après son démarrage à l'aide de ses méthodes interactives](how-to-control-a-storyboard-after-it-starts.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des plans conceptuels](storyboards-overview.md)
