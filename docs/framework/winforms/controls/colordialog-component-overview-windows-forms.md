---
title: Vue d'ensemble du composant ColorDialog (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ColorDialog
helpviewer_keywords:
- color dialog box [Windows Forms], about color dialog box
- ColorDialog component [Windows Forms], about ColorDialog
ms.assetid: 6dbdd8f0-f697-4728-bb09-7ea156f6d800
ms.openlocfilehash: 7dd48c8df0a36262962df596e8efadf4de1c2cd3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57713330"
---
# <a name="colordialog-component-overview-windows-forms"></a>Vue d'ensemble du composant ColorDialog (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.ColorDialog> composant est une boîte de dialogue préconfigurée qui permet à l’utilisateur de sélectionner une couleur dans une palette et d’ajouter des couleurs personnalisées à cette palette. Il s’agit de la même boîte de dialogue que celle que vous voyez dans d’autres applications Windows pour sélectionner des couleurs. Vous pouvez l'utiliser dans votre application Windows comme alternative à la configuration de votre propre boîte de dialogue.  
  
 La couleur sélectionnée dans la boîte de dialogue est retournée dans le <xref:System.Windows.Forms.ColorDialog.Color%2A> propriété. Si le <xref:System.Windows.Forms.ColorDialog.AllowFullOpen%2A> propriété est définie sur `false`, le bouton « Définir les couleurs personnalisées » est désactivé et que l’utilisateur est limité aux couleurs prédéfinies dans la palette. Si le <xref:System.Windows.Forms.ColorDialog.SolidColorOnly%2A> propriété est définie sur `true`, l’utilisateur ne peut pas sélectionner de couleurs tramées. Pour afficher la boîte de dialogue, vous devez appeler son <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ColorDialog>
- [ColorDialog, composant](colordialog-component-windows-forms.md)
- [Contrôles et composants de boîte de dialogue](dialog-box-controls-and-components-windows-forms.md)
- [Guide pratique pour Modifier l’apparence du composant ColorDialog Windows Forms](how-to-change-the-appearance-of-the-windows-forms-colordialog-component.md)
