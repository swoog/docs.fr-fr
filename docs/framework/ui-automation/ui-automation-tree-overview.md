---
title: Vue d'ensemble de l'arborescence UI Automation
ms.date: 03/30/2017
helpviewer_keywords:
- automation tree
- UI Automation, tree
ms.assetid: 03b98058-bdb3-47a0-8ff7-45e6cdf67166
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 042f3f82a88e987131145f38c1d8f5ecfa8dc487
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46484609"
---
# <a name="ui-automation-tree-overview"></a>Vue d’ensemble de l’arborescence UI Automation
> [!NOTE]
>  Cette documentation s'adresse aux développeurs .NET Framework qui souhaitent utiliser les classes [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] managées définies dans l'espace de noms <xref:System.Windows.Automation>. Pour plus d’informations sur [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consultez [Windows Automation API : UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Scripts de test et les produits de technologie d’assistance dans le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence pour recueillir des informations sur la [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] et ses éléments.  
  
 Dans le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence il est un élément racine (<xref:System.Windows.Automation.AutomationElement.RootElement%2A>) qui représente le bureau actuel et dont les éléments enfants représentent des fenêtres d’application. Chacun de ces éléments enfants peut contenir des éléments représentant des composants de [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] tels que des menus, des boutons, des barres d’outils et des zones de liste. Ces éléments peuvent à leur tour contenir des éléments tels que des éléments de liste.  
  
 Le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence n’est pas une structure fixe et est rarement visible dans son intégralité, car il peut contenir des milliers d’éléments. Certains de ses composants sont créés à mesure des besoins et elle peut subir des modifications à mesure que des éléments sont ajoutés, déplacés ou supprimés.  
  
 Les fournisseurs UI Automation prennent en charge la [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence en implémentant une navigation entre les éléments d’un fragment, qui se compose d’une racine (généralement hébergée dans une fenêtre) et d’une sous-arborescence. Cependant, les fournisseurs ne sont pas concernés par la navigation d’un contrôle à un autre. Elle est gérée par le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] core, à l’aide des informations à partir des fournisseurs de fenêtre par défaut.  
  
<a name="uiautomation_tree_view"></a>   
## <a name="views-of-the-automation-tree"></a>Affichages de l’arborescence Automation  
 Le [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence peut être filtrée pour créer des vues qui contiennent uniquement les <xref:System.Windows.Automation.AutomationElement> objets pertinents pour un client particulier. Cette approche permet aux clients de personnaliser la structure présentée via [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] à leurs besoins particuliers.  
  
 Le client peut personnaliser l’affichage de deux façons : par la portée et par le filtrage. La portée consiste à définir l’étendue de l’affichage à partir d’un élément de base. Par exemple, l’application peut rechercher uniquement les enfants directs du bureau ou tous les descendants d’une fenêtre de l’application. Le filtrage consiste à définir les types d’éléments qui doivent être inclus dans l’affichage.  
  
 Fournisseurs UI Automation prennent en charge le filtrage en définissant des propriétés sur les éléments, y compris le <xref:System.Windows.Automation.AutomationElementIdentifiers.IsControlElementProperty> et <xref:System.Windows.Automation.AutomationElementIdentifiers.IsContentElementProperty> propriétés.  
  
 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] fournit trois affichages par défaut. Ces affichages sont définis en fonction du type de filtrage effectué ; l’étendue d’un affichage est définie par l’application. Par ailleurs, l’application peut appliquer d’autres filtres sur les propriétés, par exemple, pour inclure uniquement des contrôles activés dans un affichage de contrôle.  
  
<a name="uiautomation_raw_view"></a>   
### <a name="raw-view"></a>Affichage brut  
 L’affichage brut de la [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence est l’arborescence complète de <xref:System.Windows.Automation.AutomationElement> objets pour lesquels le bureau est la racine. L’affichage brut suit étroitement la structure de programmation native d’une application et est de ce fait l’affichage le plus détaillé. C’est aussi la base sur laquelle reposent les autres affichages de l’arborescence. Étant donné que cette vue dépend sous-jacent [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] framework, l’affichage brut d’un [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] bouton aura un affichage brut différent à un [!INCLUDE[TLA2#tla_win32](../../../includes/tla2sharptla-win32-md.md)] bouton.  
  
 L’affichage brut s’obtient en recherchant des éléments sans spécifier de propriétés ou à l’aide de la <xref:System.Windows.Automation.TreeWalker.RawViewWalker> pour parcourir l’arborescence.  
  
<a name="uiautomation_control_view"></a>   
### <a name="control-view"></a>Affichage de contrôle  
 L’affichage de contrôle de la [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence simplifie la tâche du produit de technologie d’assistance de décrire la [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] à l’utilisateur final et aide utilisateur final interagir avec l’application, car il correspond étroitement à la [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] structure perçue par un utilisateur final.  
  
 L’affichage de contrôle est un sous-ensemble de l’affichage brut. Elle inclut toutes [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] éléments à partir de l’affichage brut qu’un utilisateur final considérerait comme interactif ou contribuant à la structure logique du contrôle dans le [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)]. Exemples de [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] les éléments qui contribuent à la structure logique de la [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)], mais ne sont pas interactives eux-mêmes, sont des conteneurs d’éléments tels que les en-têtes de vue liste, barres d’outils, menus et la barre d’état. Les éléments non interactifs utilisés simplement à des fins de disposition ou de décoration n’apparaissent pas dans l’affichage de contrôle. Tel est le cas, par exemple, d’un volet servant uniquement à disposer les contrôles dans une boîte de dialogue mais qui ne contient lui-même aucune information. Les éléments non interactifs qui apparaissent dans l’affichage de contrôle sont des éléments graphiques associées aux informations et au texte statique d’une boîte de dialogue. Les éléments non interactifs qui sont inclus dans l’affichage de contrôle ne peuvent pas recevoir le focus clavier.  
  
 L’affichage de contrôle s’obtient en recherchant des éléments dont le <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.IsControlElement%2A> propriété définie sur `true`, ou en utilisant le <xref:System.Windows.Automation.TreeWalker.ControlViewWalker> pour parcourir l’arborescence.  
  
<a name="uiautomation_content_view"></a>   
### <a name="content-view"></a>Affichage de contenu  
 L’affichage du contenu de la [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] arborescence est un sous-ensemble de l’affichage de contrôle. Il contient [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] éléments qui communiquent les véritables informations dans une interface utilisateur, y compris [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] les éléments qui peuvent recevoir le focus clavier et du texte qui n’est pas une étiquette sur un [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] élément. Par exemple, les valeurs contenues dans une zone de liste déroulante s’affichent dans l’affichage de contenu, car elles représentent les informations utilisées par un utilisateur final. Dans l’affichage du contenu, une zone de liste modifiable et zone de liste sont représentés en tant que collection de [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] éléments où un, ou éventuellement plusieurs, éléments peuvent être sélectionnés. Le fait qu’il y en a un toujours d’ouvert et un qui peut être développé et réduit est sans importance dans l’affichage de contenu, car il est conçu pour afficher les données (ou le contenu) présentées à l’utilisateur.  
  
 L’affichage du contenu s’obtient en recherchant des éléments dont le <xref:System.Windows.Automation.AutomationElement.AutomationElementInformation.IsContentElement%2A> propriété définie sur `true`, ou en utilisant le <xref:System.Windows.Automation.TreeWalker.ContentViewWalker> pour parcourir l’arborescence.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Automation.AutomationElement>  
 [Vue d’ensemble d’UI Automation](../../../docs/framework/ui-automation/ui-automation-overview.md)
