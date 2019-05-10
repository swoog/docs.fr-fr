---
title: 'Procédure : afficher l’aide contextuelle'
ms.date: 03/30/2017
helpviewer_keywords:
- pop-up Help
- Help [Windows Forms], pop-up Help
- Windows Forms, displaying Help
- forms [Windows Forms], displaying Help
- modal dialog boxes [Windows Forms], pop-up Help
- F1 Help [Windows Forms], in dialog boxes
- HelpProvider component [Windows Forms]
- Help [Windows Forms], adding to dialog boxes
ms.assetid: 218aa81e-e87e-4d67-af05-11627bbdce3b
ms.openlocfilehash: bf3bcbff0cd6f3bbf71e96e748cb170d5ce68dfc
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211399"
---
# <a name="how-to-display-pop-up-help"></a>Procédure : Afficher l’aide contextuelle

Pour afficher l’aide dans les Windows Forms offre un moyen du **aide** bouton situé sur le côté droit de la barre de titre, accessible via la <xref:System.Windows.Forms.Form.HelpButton%2A> propriété. Ce type d’affichage de l’aide convient parfaitement aux boîtes de dialogue. Les boîtes de dialogue modales (affichées avec la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A>) ont des difficultés à afficher les systèmes d'aide externes, car elles doivent être fermées pour que le focus puisse basculer vers une autre fenêtre. En outre, à l’aide de la **aide** bouton requiert l’existence aucun **réduire** bouton ou **agrandir** affiché dans la barre de titre. Il s’agit une convention de boîte de dialogue standard, tandis que les formulaires possèdent généralement **réduire** et **agrandir** boutons.

Vous pouvez également utiliser le <xref:System.Windows.Forms.HelpProvider> composant pour lier des contrôles aux fichiers dans un système d’aide, même si vous avez implémenté l’aide contextuelle. Pour plus d’informations, consultez [fourniture d’aide dans une Application Windows](how-to-provide-help-in-a-windows-application.md).

## <a name="display-pop-up-help"></a>Afficher l’aide contextuelle

1. Dans Visual Studio, faites glisser un [HelpProvider](../controls/helpprovider-component-windows-forms.md) composant à partir de la boîte à outils à votre formulaire.

   Il sera placé dans la barre d'état en bas du Concepteur Windows Forms.

2. Dans la fenêtre Propriétés, affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Form.HelpButton%2A>. Ceci affichera un bouton avec un point d'interrogation sur le côté droit de la barre de titre du formulaire.

3. Pour que le <xref:System.Windows.Forms.Form.HelpButton%2A> soit affiché, il faut que les propriétés <xref:System.Windows.Forms.Form.MinimizeBox%2A> et <xref:System.Windows.Forms.Form.MaximizeBox%2A>  du formulaire aient la valeur `false`, que la propriété <xref:System.Windows.Forms.Form.ControlBox%2A> ait la valeur `true` et que la propriété <xref:System.Windows.Forms.Form.FormBorderStyle%2A> ait l'une des valeurs suivantes : <xref:System.Windows.Forms.FormBorderStyle.FixedSingle>, <xref:System.Windows.Forms.FormBorderStyle.Fixed3D>, <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> ou <xref:System.Windows.Forms.FormBorderStyle.Sizable>.

4. Sélectionnez le contrôle pour lequel vous souhaitez afficher l'aide sur votre formulaire et définissez la chaîne d'aide dans la fenêtre Propriétés. C’est la chaîne de texte qui s’affichera dans une fenêtre similaire à un [info-bulle](../controls/tooltip-component-windows-forms.md).

5. Appuyez sur **F5**.

6. Appuyez sur la **aide** sur la barre de titre, puis cliquez sur le contrôle sur lequel vous avez défini la chaîne d’aide.

## <a name="see-also"></a>Voir aussi

- [Affichage sous forme d’info-bulles de l’aide relative aux contrôles](control-help-using-tooltips.md)
- [Intégration de l’aide d’utilisateur dans les Windows Forms](integrating-user-help-in-windows-forms.md)
- [Windows Forms](../index.md)
