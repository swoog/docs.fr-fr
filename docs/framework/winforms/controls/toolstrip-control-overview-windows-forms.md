---
title: Vue d'ensemble du contrôle ToolStrip (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Toolstrip
helpviewer_keywords:
- ToolStrip control [Windows Forms], about ToolStrip control
- toolbars [Windows Forms], what's new in Windows Forms
- toolbars [Windows Forms]
- what's new [Windows Forms], toolbars
ms.assetid: 81d067ed-297c-4dad-90de-1bcac15336ec
ms.openlocfilehash: c701ed6ff155ca507f827874a955b2361a3b2359
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57719376"
---
# <a name="toolstrip-control-overview-windows-forms"></a>Vue d'ensemble du contrôle ToolStrip (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.ToolStrip> contrôle et ses classes associées fournissent une infrastructure commune pour combiner les éléments d’interface utilisateur en barres d’outils, des barres d’état et des menus. <xref:System.Windows.Forms.ToolStrip> contrôles offrent une riche expérience au moment du design qui inclut l’activation sur place et la modification, la disposition personnalisée et la rafting, qui est la capacité des barres d’outils à partager l’espace horizontal ou vertical.  
  
 Bien que <xref:System.Windows.Forms.ToolStrip> remplace et ajoute des fonctionnalités au contrôle dans les versions précédentes, <xref:System.Windows.Forms.ToolBar> est conservé pour la compatibilité descendante et l’utilisation future si vous le souhaitez.  
  
## <a name="features-of-the-toolstrip-controls"></a>Fonctionnalités des contrôles ToolStrip  
 Utilisez le <xref:System.Windows.Forms.ToolStrip> le contrôle à :  
  
-   Présenter une interface utilisateur commune entre les conteneurs.  
  
-   Créez facilement personnalisées, employées couramment barres d’outils qui prennent en charge utilisateur interface et la disposition des fonctionnalités avancées, telles que des boutons d’ancrage, le rafting, avec le texte et des images, des boutons de liste déroulante et des contrôles, dépassement de capacité des boutons et réorganisation au moment de l’exécution de <xref:System.Windows.Forms.ToolStrip> éléments.  
  
-   Prend en charge le dépassement de capacité et la réorganisation des éléments au moment de l’exécution. La fonctionnalité de dépassement de capacité déplace les éléments à un menu déroulant lorsqu’il n’est pas assez de place pour les afficher dans un <xref:System.Windows.Forms.ToolStrip>.  
  
-   Prend en charge l’apparence classique et le comportement du système d’exploitation via un modèle de rendu commun.  
  
-   Gérer les événements cohérente pour tous les conteneurs et les éléments de contenu, de la même façon que vous gérez des événements pour d’autres contrôles.  
  
-   Faites glisser des éléments à partir d’un <xref:System.Windows.Forms.ToolStrip> vers un autre ou dans un <xref:System.Windows.Forms.ToolStrip>.  
  
-   Créer des éditeurs de type d’interface utilisateur et les contrôles de liste déroulante avec des présentations avancées dans un <xref:System.Windows.Forms.ToolStripDropDown>.  
  
 Utiliser le <xref:System.Windows.Forms.ToolStripControlHost> classe à utiliser d’autres contrôles sur un <xref:System.Windows.Forms.ToolStrip> et d’en prendre <xref:System.Windows.Forms.ToolStrip> fonctionnalité pour eux.  
  
 Vous pouvez étendre les fonctionnalités et modifier l’apparence et le comportement à l’aide de la <xref:System.Windows.Forms.ToolStripRenderer>, <xref:System.Windows.Forms.ToolStripProfessionalRenderer>, et <xref:System.Windows.Forms.ToolStripManager> avec la <xref:System.Windows.Forms.ToolStripRenderMode> et <xref:System.Windows.Forms.ToolStripManagerRenderMode> énumérations.  
  
 Le <xref:System.Windows.Forms.ToolStrip> contrôle est hautement configurable et extensible, et il fournit de nombreuses propriétés, méthodes et événements pour personnaliser l’apparence et le comportement. Voici certains membres les plus importants :  
  
### <a name="important-toolstrip-members"></a>Membres ToolStrip importants  
  
|Name|Description|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStrip.Dock%2A>|Obtient ou définit le bord du conteneur parent un <xref:System.Windows.Forms.ToolStrip> est ancré.|  
|<xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>|Obtient ou définit une valeur qui indique si des opérations de glisser-déplacer et de réorganisation d'éléments sont traitées en privé par la classe <xref:System.Windows.Forms.ToolStrip>.|  
|<xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A>|Obtient ou définit une valeur indiquant comment la <xref:System.Windows.Forms.ToolStrip> expose ses éléments.|  
|<xref:System.Windows.Forms.ToolStripItem.Overflow%2A>|Obtient ou définit si un <xref:System.Windows.Forms.ToolStripItem> est attaché à la <xref:System.Windows.Forms.ToolStrip> ou <xref:System.Windows.Forms.ToolStripOverflowButton> ou peut flotter entre les deux.|  
|<xref:System.Windows.Forms.ToolStrip.IsDropDown%2A>|Obtient une valeur indiquant si un <xref:System.Windows.Forms.ToolStripItem> affiche d’autres éléments dans une liste déroulante liste lorsque le <xref:System.Windows.Forms.ToolStripItem> est cliqué.|  
|<xref:System.Windows.Forms.ToolStrip.OverflowButton%2A>|Obtient le <xref:System.Windows.Forms.ToolStripItem>, qui correspond au bouton de dépassement de capacité pour un <xref:System.Windows.Forms.ToolStrip> avec dépassement de capacité activé.|  
|<xref:System.Windows.Forms.ToolStrip.Renderer%2A>|Obtient ou définit un <xref:System.Windows.Forms.ToolStripRenderer> utilisé pour personnaliser l’apparence et le comportement (aspect) d’un <xref:System.Windows.Forms.ToolStrip>.|  
|<xref:System.Windows.Forms.ToolStrip.RenderMode%2A>|Obtient ou définit les styles de peinture à appliquer à <xref:System.Windows.Forms.ToolStrip>.|  
|<xref:System.Windows.Forms.ToolStrip.RendererChanged>|Déclenché lorsque le <xref:System.Windows.Forms.ToolStrip.Renderer%2A> les modifications de propriété.|  
  
 Le <xref:System.Windows.Forms.ToolStrip> souplesse du contrôle s’effectue via l’utilisation d’un nombre de classes auxiliaires. Voici quelques-unes des plus importantes :  
  
### <a name="important-toolstrip-companion-classes"></a>Classes auxiliaires ToolStrip importantes  
  
|Name|Description|  
|----------|-----------------|  
|<xref:System.Windows.Forms.MenuStrip>|Remplace et ajoute des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> classe.|  
|<xref:System.Windows.Forms.StatusStrip>|Remplace et ajoute des fonctionnalités à la <xref:System.Windows.Forms.StatusBar> classe.|  
|<xref:System.Windows.Forms.ContextMenuStrip>|Remplace et ajoute des fonctionnalités à la <xref:System.Windows.Forms.ContextMenu> classe.|  
|<xref:System.Windows.Forms.ToolStripItem>|Classe qui gère les événements et la disposition de tous les éléments de base abstraite qui un <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.ToolStripControlHost>, ou <xref:System.Windows.Forms.ToolStripDropDown> peut contenir.|  
|<xref:System.Windows.Forms.ToolStripContainer>|Fournit un conteneur avec un panneau sur chaque côté du formulaire dans lequel les contrôles peuvent être organisés de différentes manières.|  
|<xref:System.Windows.Forms.ToolStripRenderer>|Gère les fonctionnalités de peinture pour <xref:System.Windows.Forms.ToolStrip> objets.|  
|<xref:System.Windows.Forms.ToolStripProfessionalRenderer>|Fournit l’apparence de style Microsoft Office.|  
|<xref:System.Windows.Forms.ToolStripManager>|Contrôles <xref:System.Windows.Forms.ToolStrip> rendu et le rafting et la fusion de <xref:System.Windows.Forms.MenuStrip>, <xref:System.Windows.Forms.ToolStripDropDownMenu>, et <xref:System.Windows.Forms.ToolStripMenuItem> objets.|  
|<xref:System.Windows.Forms.ToolStripManagerRenderMode>|Spécifie le style de peinture (personnalisé, Windows XP ou Microsoft Office Professional) appliqué à plusieurs <xref:System.Windows.Forms.ToolStrip> objets contenus dans un formulaire.|  
|<xref:System.Windows.Forms.ToolStripRenderMode>|Spécifie le style de peinture (personnalisé, Windows XP ou Microsoft Office Professionnel) appliqué à un seul <xref:System.Windows.Forms.ToolStrip> objet contenu dans un formulaire.|  
|<xref:System.Windows.Forms.ToolStripControlHost>|Héberge d’autres contrôles qui ne sont pas spécifiquement <xref:System.Windows.Forms.ToolStrip> contrôles mais pour lequel vous voulez <xref:System.Windows.Forms.ToolStrip> fonctionnalité.|  
|<xref:System.Windows.Forms.ToolStripItemPlacement>|Spécifie si un <xref:System.Windows.Forms.ToolStripItem> doit être disposé sur les principaux <xref:System.Windows.Forms.ToolStrip>, sur le dépassement de capacité <xref:System.Windows.Forms.ToolStrip>, ou aucun.|  
  
 Pour plus d’informations, consultez [résumé de la technologie ToolStrip](toolstrip-technology-summary.md) et [Architecture du contrôle ToolStrip](toolstrip-control-architecture.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripDropDown>
