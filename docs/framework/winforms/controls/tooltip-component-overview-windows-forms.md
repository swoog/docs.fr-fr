---
title: Vue d'ensemble du composant ToolTip (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ToolTip
helpviewer_keywords:
- tooltips [Windows Forms], about tooltips
- ToolTip component [Windows Forms], about ToolTip component
ms.assetid: 3fbc6f08-c882-4acd-a960-a08efe3c7e6e
ms.openlocfilehash: e31bb1169eeedd85a92e3bf96318623696020f9b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33535536"
---
# <a name="tooltip-component-overview-windows-forms"></a>Vue d'ensemble du composant ToolTip (Windows Forms)
Le composant Windows Forms <xref:System.Windows.Forms.ToolTip> affiche du texte quand l'utilisateur pointe sur des contrôles. Une info-bulle peut être associée à n'importe quel contrôle. Un exemple d’utilisation de ce composant : pour économiser de l’espace sur un formulaire, vous pouvez afficher une petite icône sur un bouton et utiliser une info-bulle pour expliquer la fonction du bouton.  
  
## <a name="working-with-the-tooltip-component"></a>Utilisation du composant ToolTip  
 A <xref:System.Windows.Forms.ToolTip> composant fournit un `ToolTip` propriété à plusieurs contrôles sur un Windows Form ou autre conteneur. Par exemple, si vous placez un <xref:System.Windows.Forms.ToolTip> composant d’un formulaire, vous pouvez afficher la « Type de votre nom ici » pour un <xref:System.Windows.Forms.TextBox> contrôler et « Cliquez ici pour enregistrer les modifications » pour un <xref:System.Windows.Forms.Button> contrôle.  
  
 Les méthodes clés de la <xref:System.Windows.Forms.ToolTip> composant sont <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> et <xref:System.Windows.Forms.ToolTip.GetToolTip%2A>. Vous pouvez utiliser la <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> pour définir les info-bulles affichées pour des contrôles. Pour plus d’informations, consultez [Comment : définir des info-bulles pour les contrôles sur un Windows Form au moment du Design](../../../../docs/framework/winforms/controls/how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md). Les propriétés de clé sont <xref:System.Windows.Forms.ToolTip.Active%2A>, qui doit être défini sur `true` pour l’info-bulle s’affiche, et <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A>, qui définit la durée pendant laquelle la chaîne d’info-bulle est affichée, la durée pendant laquelle l’utilisateur doit pointer sur le contrôle de l’info-bulle s’affiche et la durée de l’opération prend pour les info-bulles suivantes pour s’affichent. Pour plus d’informations, consultez [Comment : modifier la durée avant affichage du composant ToolTip Windows Forms](../../../../docs/framework/winforms/controls/how-to-change-the-delay-of-the-windows-forms-tooltip-component.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.ToolTip>  
 [Guide pratique pour définir des info-bulles pour les contrôles d'un Windows Form au moment du design](../../../../docs/framework/winforms/controls/how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)  
 [Guide pratique pour modifier la durée avant affichage du composant ToolTip Windows Forms](../../../../docs/framework/winforms/controls/how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
