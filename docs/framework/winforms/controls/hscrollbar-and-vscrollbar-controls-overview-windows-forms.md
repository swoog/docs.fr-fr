---
title: Vue d'ensemble des contrôles HScrollBar et VScrollBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- HScrollBar
- VScrollBar
helpviewer_keywords:
- ScrollBar control [Windows Forms]
- HScrollBar control [Windows Forms], about HScrollBar
- VScrollBar control [Windows Forms], about VScrollBar control
- ScrollBar control [Windows Forms], about ScrollBar control
- scroll bars [Windows Forms], about scroll bars
ms.assetid: 8b307679-1cae-41d8-99aa-3d1efd207cd6
ms.openlocfilehash: 2c6436e77753322733580acba5a20d6bb220f29c
ms.sourcegitcommit: 67de6cb5dd66a19f2180ba7e4d7aecc697f8a963
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44342366"
---
# <a name="hscrollbar-and-vscrollbar-controls-overview-windows-forms"></a>Vue d'ensemble des contrôles HScrollBar et VScrollBar (Windows Forms)
Windows Forms <xref:System.Windows.Forms.ScrollBar> contrôles sont utilisés pour fournir une navigation facile dans une longue liste d’éléments ou d’une grande quantité d’informations en faisant défiler horizontalement ou verticalement dans une application ou un contrôle. Barres de défilement sont un élément courant de l’interface Windows, afin que la <xref:System.Windows.Forms.ScrollBar> contrôle est souvent utilisé avec les contrôles qui ne dérivent pas de la <xref:System.Windows.Forms.ScrollableControl> classe. De même, de nombreux développeurs choisissent d’incorporer le <xref:System.Windows.Forms.ScrollBar> contrôler lors de la création de leurs propres contrôles utilisateur.  
  
 Le <xref:System.Windows.Forms.HScrollBar> (horizontal) et <xref:System.Windows.Forms.VScrollBar> (verticales) contrôles fonctionnent indépendamment des autres contrôles et ont leur propre jeu d’événements, propriétés et méthodes. <xref:System.Windows.Forms.ScrollBar> contrôles ne sont pas les mêmes que les barres de défilement intégrées qui sont attachés à des zones de texte, zones de liste, zones de liste déroulante ou des formulaires MDI (le <xref:System.Windows.Forms.TextBox> contrôle a un <xref:System.Windows.Forms.TextBox.ScrollBars%2A> propriété pour afficher ou masquer les barres de défilement qui sont attachés au contrôle).  
  
 Le <xref:System.Windows.Forms.ScrollBar> contrôles utilisent la <xref:System.Windows.Forms.ScrollBar.Scroll> événement pour surveiller le mouvement de la case de défilement (parfois appelé curseur de défilement) le long de la barre de défilement. À l’aide de la <xref:System.Windows.Forms.ScrollBar.Scroll> événement fournit l’accès à la valeur de barre de défilement pendant qu’il est glissé.  
  
## <a name="value-property"></a>Propriété Value  
 Le <xref:System.Windows.Forms.ScrollBar.Value%2A> propriété (c'est-à-dire, par défaut, 0) est un `integer` valeur correspondant à la position de la case de défilement dans la barre de défilement. Lorsque la position de la zone de défilement est à la valeur minimale, il déplace vers la position la plus à gauche (pour les barres de défilement horizontale) ou la position supérieure (pour les barres de défilement verticale). Lorsque la case de défilement est à la valeur maximale, le défilement se place à la plus à droite ou la position inférieure. De même, une valeur à mi-chemin entre le bas et haut de gamme place la pointe de la case de défilement au milieu de la barre de défilement.  
  
 Outre l’utilisation des clics de souris pour modifier la valeur de barre de défilement, un utilisateur peut également faire glisser la case de défilement à n’importe quel point le long de la barre. La valeur obtenue dépend de la position de la case de défilement, mais elle se trouve toujours dans la plage de la <xref:System.Windows.Forms.ScrollBar.Minimum%2A> à <xref:System.Windows.Forms.ScrollBar.Maximum%2A> propriétés définies par l’utilisateur.  
  
## <a name="largechange-and-smallchange-properties"></a>Propriétés LargeChange et SmallChange  
 Lorsque l’utilisateur appuie sur la touche Pg préc ou Pg suiv ou clique dans le rail de barre de défilement de chaque côté de la case de défilement, le <xref:System.Windows.Forms.ScrollBar.Value%2A> des modifications de propriété en fonction de la valeur définie dans le <xref:System.Windows.Forms.ScrollBar.LargeChange%2A> propriété.  
  
 Lorsque l’utilisateur appuie sur l’une de la flèche de touches ou clique sur un des boutons de la barre de défilement, le <xref:System.Windows.Forms.ScrollBar.Value%2A> des modifications de propriété en fonction de la valeur définie dans le <xref:System.Windows.Forms.ScrollBar.SmallChange%2A> propriété.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.HScrollBar>  
 <xref:System.Windows.Forms.VScrollBar>  
 [Ajouts dans les Windows Forms pour .NET Framework 2.0](https://msdn.microsoft.com/library/c61a923d-3d6a-4c8c-820c-e94c83f3f9a8)  
 [Contrôles à utiliser dans les Windows Forms](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
