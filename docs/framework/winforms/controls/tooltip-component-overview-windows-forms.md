---
title: Vue d'ensemble du composant ToolTip (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ToolTip
helpviewer_keywords:
- tooltips [Windows Forms], about tooltips
- ToolTip component [Windows Forms], about ToolTip component
ms.assetid: 3fbc6f08-c882-4acd-a960-a08efe3c7e6e
ms.openlocfilehash: 3fbe883501d1ce36ca25ea07631f98042f451e07
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197306"
---
# <a name="tooltip-component-overview-windows-forms"></a>Vue d'ensemble du composant ToolTip (Windows Forms)
Le composant Windows Forms <xref:System.Windows.Forms.ToolTip> affiche du texte quand l'utilisateur pointe sur des contrôles. Une info-bulle peut être associée à n'importe quel contrôle. Un exemple d’utilisation de ce composant : pour économiser de l’espace sur un formulaire, vous pouvez afficher une petite icône sur un bouton et utiliser une info-bulle pour expliquer la fonction du bouton.  
  
## <a name="working-with-the-tooltip-component"></a>Utilisation du composant info-bulle  
 Un <xref:System.Windows.Forms.ToolTip> composant fournit un `ToolTip` propriété à plusieurs contrôles sur un formulaire Windows ou un autre conteneur. Par exemple, si vous placez un <xref:System.Windows.Forms.ToolTip> composant sur un formulaire, vous pouvez afficher « Tapez ici votre nom » pour un <xref:System.Windows.Forms.TextBox> contrôler et « Cliquez ici pour enregistrer les modifications » pour un <xref:System.Windows.Forms.Button> contrôle.  
  
 Les principales méthodes de la <xref:System.Windows.Forms.ToolTip> composant sont <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> et <xref:System.Windows.Forms.ToolTip.GetToolTip%2A>. Vous pouvez utiliser la <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode pour définir les info-bulles affichées pour des contrôles. Pour plus d'informations, voir [Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md). Les propriétés de clé sont <xref:System.Windows.Forms.ToolTip.Active%2A>, qui doit être défini sur `true` pour l’info-bulle s’affiche, et <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A>, qui définit la durée pendant laquelle la chaîne d’info-bulle est affichée, la durée pendant laquelle l’utilisateur doit pointer sur le contrôle pour l’info-bulle s’affiche et la durée de l’opération nécessaire pour que les fenêtres info-bulle suivantes s’affichent. Pour plus d'informations, voir [Procédure : Modifier la durée avant affichage du composant ToolTip Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolTip>
- [Guide pratique pour Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)
- [Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
