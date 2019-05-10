---
title: 'Procédure : Contrôler un Storyboard après son démarrage'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Storyboards [WPF], controlling after start
ms.assetid: 040f13f0-69f9-4ab5-be2b-079f4f80c7c0
ms.openlocfilehash: 680676921e14ad69d97f3ee1c39e3ec955e66dec
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662140"
---
# <a name="how-to-control-a-storyboard-after-it-starts"></a>Procédure : Contrôler un Storyboard après son démarrage
Cet exemple montre comment utiliser le code pour contrôler un <xref:System.Windows.Media.Animation.Storyboard> après qu’elle a démarré. Pour contrôler un storyboard dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], utilisez <xref:System.Windows.Trigger> et <xref:System.Windows.TriggerAction> objets ; pour obtenir un exemple, consultez [utiliser déclencheurs d’événements pour contrôler un Storyboard après son démarrage](how-to-use-event-triggers-to-control-a-storyboard-after-it-starts.md).  
  
 Pour démarrer un storyboard, vous utilisez sa <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> (méthode), qui distribue les animations de la table de montage séquentiel aux propriétés animées et démarre le storyboard.  
  
 Pour rendre une table de montage séquentiel contrôlable, vous utilisez le <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> (méthode) et spécifiez **true** comme deuxième paramètre. Vous pouvez ensuite utiliser des méthodes interactives de la table de montage séquentiel à suspendre, reprendre, rechercher, arrêter, accélérer, ralentir l’animation ou avancer à sa période de remplissage. Voici une liste des méthodes interactives de la table de montage séquentiel :  
  
- <xref:System.Windows.Media.Animation.Storyboard.Pause%2A>: Suspend le storyboard.  
  
- <xref:System.Windows.Media.Animation.Storyboard.Resume%2A>: Reprend un storyboard suspendu.  
  
- <xref:System.Windows.Media.Animation.Storyboard.SetSpeedRatio%2A>: Définit la vitesse interactive de la table de montage séquentiel.  
  
- <xref:System.Windows.Media.Animation.Storyboard.Seek%2A>: Recherche la table de montage séquentiel l’emplacement spécifié.  
  
- <xref:System.Windows.Media.Animation.Storyboard.SeekAlignedToLastTick%2A>: Recherche la table de montage séquentiel à l’emplacement spécifié. Contrairement à la <xref:System.Windows.Media.Animation.Storyboard.Seek%2A> (méthode), cette opération est traitée avant le battement suivant.  
  
- <xref:System.Windows.Media.Animation.Storyboard.SkipToFill%2A>: Fait avancer le storyboard à sa période de remplissage, le cas échéant.  
  
- <xref:System.Windows.Media.Animation.Storyboard.Stop%2A>: Arrête le storyboard.  
  
 Dans l’exemple suivant, plusieurs méthodes de storyboard permet de contrôler un storyboard de façon interactive.  
  
 **Remarque :** Pour voir un exemple de contrôle d’une table de montage séquentiel à l’aide de déclencheurs avec [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], consultez [utiliser les déclencheurs d’événements pour contrôler un Storyboard après son démarrage](how-to-use-event-triggers-to-control-a-storyboard-after-it-starts.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[timingbehaviors_procedural_snip#ControlStoryboardExampleUsingWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ControlStoryboardExample.cs#controlstoryboardexampleusingwholepage)]
 [!code-vb[timingbehaviors_procedural_snip#ControlStoryboardExampleUsingWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/controlstoryboardexample.vb#controlstoryboardexampleusingwholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Utiliser des déclencheurs d’événements pour contrôler un storyboard après son démarrage](how-to-use-event-triggers-to-control-a-storyboard-after-it-starts.md)
