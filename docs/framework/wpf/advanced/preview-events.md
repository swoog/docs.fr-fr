---
title: Aperçu des événements
ms.date: 03/30/2017
helpviewer_keywords:
- Preview events [WPF]
- suppressing events [WPF]
- events [WPF], Preview
- events [WPF], suppressing
ms.assetid: b5032308-aa9c-4d02-af11-630ecec8df7e
ms.openlocfilehash: 75165df94aa8b508ef85cf970933efb98b9d62ca
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211390"
---
# <a name="preview-events"></a>Aperçu des événements
Événements d’aperçu, également appelés événements de tunneling, sont des événements routés où la direction de l’itinéraire sont transmises à partir de la racine de l’application vers l’élément qui a déclenché l’événement et est signalé comme étant la source de données d’événement. Pas tous les scénarios d’événements prend en charge ou exiger des événements d’aperçu. Cette rubrique décrit les situations où les événements d’aperçu existent, comment les applications ou composants doivent les gérer et les cas où la création d’événements de la version préliminaire dans des composants personnalisés ou des classes peut être approprié.  
  
## <a name="preview-events-and-input"></a>Événements d’aperçu et entrée  
 Lorsque vous gérez l’aperçu d’événements en général, soyez prudent marquer les événements gérés de l’événement données. Gestion d’un événement de la version préliminaire sur n’importe quel élément autre que l’élément qui l’a déclenché (l’élément qui est signalé comme source dans les données d’événement) a pour effet de ne pas fournir un élément de la possibilité de gérer l’événement qui a son origine. Parfois, il est le résultat souhaité, en particulier si les éléments en question existent dans les relations au sein de la composition d’un contrôle.  
  
 Pour les événements d’entrée en particulier, les événements Preview également partagent instances de données d’événement avec l’événement de propagation équivalent. Si vous utilisez un gestionnaire de classe d’événements Aperçu pour marquer l’événement d’entrée géré, le Gestionnaire de classe d’événements d’entrée par propagation ne sera pas appelé. Ou, si vous utilisez un gestionnaire d’instance événements Aperçu pour marquer l’événement géré, les gestionnaires pour l’événement de propagation ne seront pas généralement appelées. Gestionnaires de classe ou gestionnaires d’instance peuvent être inscrit ou attachés avec une option à appeler même si l’événement est marqué comme géré, mais cette technique n’est pas couramment utilisée.  
  
 Pour plus d’informations sur la gestion de classe et sa relation aux événements d’aperçu consultez [marquage des événements routés comme gérés et gestion de classe](marking-routed-events-as-handled-and-class-handling.md).  
  
### <a name="working-around-event-suppression-by-controls"></a>Résolution des problèmes liés à la suppression d’événements par des contrôles  
 Il est un scénario où les événements d’aperçu sont couramment utilisés pour la gestion de contrôle composite d’événements d’entrée. Parfois, l’auteur du contrôle supprime un certain événement proviennent de leur contrôle, peut-être pour remplacer un événement défini par le composant qui comporte plus d’informations ou implique un comportement plus spécifique. Par exemple, un [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Controls.Button> supprime <xref:System.Windows.UIElement.MouseLeftButtonDown> et <xref:System.Windows.UIElement.MouseRightButtonDown> propagation des événements déclenchés par le <xref:System.Windows.Controls.Button> ou ses éléments composites en faveur de la capture de la souris et de déclencher un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement est toujours déclenché par le <xref:System.Windows.Controls.Button> lui-même. L’événement et ses données poursuivent l’itinéraire, mais étant donné que le <xref:System.Windows.Controls.Button> marque les données d’événement en tant que <xref:System.Windows.RoutedEventArgs.Handled%2A>, seuls les gestionnaires pour l’événement qui indiquait spécifiquement qu’ils doivent agir dans le `handledEventsToo` cas sont appelées.  Si d’autres éléments vers la racine de votre application souhaitaient toujours à gérer un événement supprimé par contrôle, une solution consiste à joindre des gestionnaires dans le code avec `handledEventsToo` spécifié en tant que `true`. Mais souvent une technique plus simple consiste à modifier la direction de routage que vous gérez à l’équivalent de l’aperçu d’un événement d’entrée. Par exemple, si un contrôle supprime <xref:System.Windows.UIElement.MouseLeftButtonDown>, essayez de joindre un gestionnaire pour <xref:System.Windows.UIElement.PreviewMouseLeftButtonDown> à la place. Cette technique fonctionne uniquement pour les événements d’entrée d’élément de base telles que <xref:System.Windows.UIElement.MouseLeftButtonDown>. Ces événements d’entrée utilisent des paires de tunneling/propagation, déclenchent les deux événements et partagent les données d’événement.  
  
 Chacune de ces techniques a des effets secondaires ou des limitations. L’effet secondaire de la gestion de l’événement d’aperçu est que gérant l’événement à ce stade peut désactiver les gestionnaires qui vous attendre à gérer l’événement de propagation, et par conséquent, la limitation est qu’il n’est généralement pas une bonne idée pour marquer l’événement géré alors qu’il est toujours sur le Previ partie Nouv de l’itinéraire. La limitation de la `handledEventsToo` technique est que vous ne pouvez pas spécifier un `handledEventsToo` gestionnaire dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] en tant qu’attribut, vous devez inscrire le Gestionnaire d’événements dans le code après avoir obtenu une référence d’objet à l’élément où le gestionnaire doit être attaché.  
  
## <a name="see-also"></a>Voir aussi

- [Marquage des événements routés comme gérés et gestion de classe](marking-routed-events-as-handled-and-class-handling.md)
- [Vue d’ensemble des événements routés](routed-events-overview.md)
