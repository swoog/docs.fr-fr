---
title: Événements de la durée de vie d'un objet
ms.date: 03/30/2017
helpviewer_keywords:
- events [WPF], ContentRendered
- events [WPF], Deactivated
- events [WPF], Unloaded
- Activated events [WPF]
- events [WPF], Loaded
- Application objects [WPF], lifetime events
- events [WPF], Activated
- ContentRendered events [WPF]
- Deactivated events [WPF]
- events [WPF], Initialized
- events [WPF], Closing
- Unloaded events [WPF]
- exit events [WPF]
- objects' lifetime events [WPF]
- Loaded events [WPF]
- Closing events [WPF]
- events [WPF], Closed
- Initialized events [WPF]
- Closed events [WPF]
- startup events [WPF]
- lifetime events of objects [WPF]
ms.assetid: face6fc7-465b-4502-bfe5-e88d2e729a78
ms.openlocfilehash: 8b42104522be854fe4e49d08e110497469d64980
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555360"
---
# <a name="object-lifetime-events"></a>Événements de la durée de vie d'un objet
Cette rubrique décrit les événements [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] spécifiques qui correspondent aux étapes de la durée de vie de création, d’utilisation et de destruction d’un objet.  
  

  
<a name="prerequisites"></a>   
## <a name="prerequisites"></a>Prérequis  
 Cette rubrique part du principe que vous maîtrisez les propriétés de dépendance du point de vue d’un consommateur de propriétés de dépendance existantes dans les classes [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)], et que vous avez lu la rubrique [Vue d’ensemble des propriétés de dépendance](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md). Pour pouvoir suivre les exemples de cette rubrique, vous devez aussi maîtriser le langage [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] (consultez [Vue d’ensemble du langage XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)) et savoir comment écrire des applications [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
<a name="intro"></a>   
## <a name="object-lifetime-events"></a>Événements de la durée de vie d'un objet  
 Tous les objets dans le code managé Microsoft .NET Framework passent par un ensemble similaire d’étapes de la vie, la création, l’utilisation et la destruction. De nombreux objets passent aussi par une étape de fin de vie qui se produit pendant la phase de destruction. Les objets [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], plus précisément les objets visuels que [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] identifie comme des éléments, ont aussi un ensemble d’étapes communes de vie d’objet. Les modèles de programmation et d’application [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] exposent ces étapes comme une série d’événements. Il existe quatre types d’objet principaux dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] en ce qui concerne les événements de durée de vie : éléments en général, éléments de fenêtre, hôtes de navigation et objets d’application. Les fenêtres et les hôtes de navigation appartiennent aussi au groupe d’objets visuels (éléments) le plus grand. Cette rubrique décrit les événements de durée de vie communs à tous les éléments et présente les événements plus spécifiques qui s’appliquent aux définitions d’application, fenêtres ou hôtes de navigation.  
  
<a name="common_events"></a>   
## <a name="common-lifetime-events-for-elements"></a>Événements de durée de vie communs des éléments  
 N’importe quel élément de niveau infrastructure WPF (objets dérivés de soit <xref:System.Windows.FrameworkElement> ou <xref:System.Windows.FrameworkContentElement>) a trois événements de durée de vie communs : <xref:System.Windows.FrameworkElement.Initialized>, <xref:System.Windows.FrameworkElement.Loaded>, et <xref:System.Windows.FrameworkElement.Unloaded>.  
  
### <a name="initialized"></a>Initialized  
 <xref:System.Windows.FrameworkElement.Initialized> est déclenché en premier et correspond approximativement à l’initialisation de l’objet par l’appel à son constructeur. Comme l’événement se produit en réponse à l’initialisation, vous êtes assuré que toutes les propriétés de l’objet sont définies. (Il existe une exception pour les utilisations d’expressions, telles que les ressources dynamiques ou la liaison ; ces expressions ne sont pas évaluées.) Par conséquent l’exigence indiquant que toutes les propriétés sont définies, la séquence de <xref:System.Windows.FrameworkElement.Initialized> déclenchés par des éléments imbriqués définis dans le balisage semble se produire dans l’ordre des éléments plus profondément imbriqués dans l’arborescence d’éléments tout d’abord, puis les éléments parents vers la racine. Cet ordre s’explique par le fait que les relations parent-enfant et contenant-contenu sont des propriétés. Par conséquent, le parent ne peut pas signaler l’initialisation tant que les éléments enfants qui remplissent la propriété ne sont pas eux aussi complètement initialisés.  
  
 Lorsque vous écrivez des gestionnaires en réponse à la <xref:System.Windows.FrameworkElement.Initialized> événement, vous devez prendre en compte qu’il n’existe aucune garantie que tous les autres éléments dans l’arborescence d’éléments (arborescence logique ou arborescence d’éléments visuels) autour d’où le gestionnaire est attaché ont été créés, en particulier éléments parents. Les variables membres peuvent avoir la valeur null ou les sources de données peuvent ne pas être encore remplies par la liaison sous-jacente (même au niveau de l’expression).  
  
### <a name="loaded"></a>Chargé  
 <xref:System.Windows.FrameworkElement.Loaded> est ensuite déclenché. Le <xref:System.Windows.FrameworkElement.Loaded> événement est déclenché avant le rendu final, mais après que le système de disposition a calculé toutes les valeurs nécessaires pour le rendu. <xref:System.Windows.FrameworkElement.Loaded> implique que l’arborescence logique contenue dans un élément est terminée et se connecte à une source de présentation qui fournit le HWND et la surface de rendu. Liaison de données standard (liaison à des sources locales, telles que les autres propriétés ou les sources de données directement définies) se produit avant <xref:System.Windows.FrameworkElement.Loaded>. La liaison de données asynchrone (sources externes ou dynamiques) peut s’être produite, mais du fait même de sa nature asynchrone, elle peut ne pas avoir eu lieu.  
  
 Le mécanisme par lequel le <xref:System.Windows.FrameworkElement.Loaded> événement est déclenché est différente de celle <xref:System.Windows.FrameworkElement.Initialized>. Le <xref:System.Windows.FrameworkElement.Initialized> événement est déclenché élément par élément, sans coordination directe par une arborescence d’éléments complétée. En revanche, le <xref:System.Windows.FrameworkElement.Loaded> événement est déclenché de manière coordonnée dans toute l’arborescence de la totalité de l’élément (plus précisément, l’arborescence logique). Lorsque tous les éléments dans l’arborescence se trouvent dans un état où elles sont considérées comme chargé, le <xref:System.Windows.FrameworkElement.Loaded> événement est déclenché tout d’abord sur l’élément racine. Le <xref:System.Windows.FrameworkElement.Loaded> événement est déclenché successivement sur chaque élément enfant.  
  
> [!NOTE]
>  Ce comportement peut rappeler en apparence le tunneling dans le cas d’un événement routé. Cependant, aucune information n’est transmise d’un événement à l’autre. Chaque élément a toujours la possibilité de gérer son <xref:System.Windows.FrameworkElement.Loaded> événement et marquer les données d’événement comme géré n’a aucun effet au-delà de l’élément.  
  
### <a name="unloaded"></a>Non chargé  
 <xref:System.Windows.FrameworkElement.Unloaded> est déclenché en dernier et est initialisé par la source de présentation ou le parent visuel en cours de suppression. Lorsque <xref:System.Windows.FrameworkElement.Unloaded> est déclenché et géré, l’élément qui est le parent de source d’événement (comme déterminé par <xref:System.Windows.FrameworkElement.Parent%2A> propriété) ou tout élément vers le haut dans l’arborescence logique ou visuelle peut-être avoir déjà été pas définie, ce qui signifie que cette liaison de données, les références de ressources , et les styles ne peuvent pas être définies à leur valeur d’exécution normale ou dernière connue.  
  
<a name="application_model_elements"></a>   
## <a name="lifetime-events-application-model-elements"></a>Éléments de modèle d’application d’événements de durée de vie  
 Reposent sur les événements de durée de vie communs des éléments de modèle d’application suivants : <xref:System.Windows.Application>, <xref:System.Windows.Window>, <xref:System.Windows.Controls.Page>, <xref:System.Windows.Navigation.NavigationWindow>, et <xref:System.Windows.Controls.Frame>. Ces éléments étendent les événements de durée de vie communs avec des événements supplémentaires en rapport avec leur fonction. Ils sont décrits en détail aux emplacements suivants :  
  
-   <xref:System.Windows.Application>: [Vue d’ensemble de la gestion des applications](../../../../docs/framework/wpf/app-development/application-management-overview.md).  
  
-   <xref:System.Windows.Window>: [Vue d’ensemble WPF Windows](../../../../docs/framework/wpf/app-development/wpf-windows-overview.md).  
  
-   <xref:System.Windows.Controls.Page>, <xref:System.Windows.Navigation.NavigationWindow>, et <xref:System.Windows.Controls.Frame>: [Vue d’ensemble de la navigation](../../../../docs/framework/wpf/app-development/navigation-overview.md).  
  
## <a name="see-also"></a>Voir aussi
- [Priorité de la valeur de propriété de dépendance](../../../../docs/framework/wpf/advanced/dependency-property-value-precedence.md)
- [Vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
