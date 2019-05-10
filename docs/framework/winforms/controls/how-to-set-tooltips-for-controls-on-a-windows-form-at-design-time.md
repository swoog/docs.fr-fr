---
title: 'Procédure : définir des info-bulles pour des contrôles dans un formulaire Windows au moment du design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], for controls
- examples [Windows Forms], tooltips
ms.assetid: c4b60637-4c0a-44c2-a103-f66dff887936
ms.openlocfilehash: 0d6725fc1a00826870e6400bffce63a1788e802c
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211685"
---
# <a name="how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time"></a>Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du design

Vous pouvez définir un <xref:System.Windows.Forms.ToolTip> chaîne dans le code ou dans le Concepteur de formulaires Windows dans Visual Studio. Pour plus d’informations sur la <xref:System.Windows.Forms.ToolTip> composant, consultez [vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md).

## <a name="set-a-tooltip-programmatically"></a>Définir une info-bulle par programmation

1. Ajoutez le contrôle qui affiche l’info-bulle.

2. Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.

    ```vb
    ' In this example, Button1 is the control to display the ToolTip.
    ToolTip1.SetToolTip(Button1, "Save changes")
    ```

    ```csharp
    // In this example, button1 is the control to display the ToolTip.
    toolTip1.SetToolTip(button1, "Save changes");
    ```

    ```cpp
    // In this example, button1 is the control to display the ToolTip.
    toolTip1->SetToolTip(button1, "Save changes");
    ```

## <a name="set-a-tooltip-in-the-designer"></a>Définir une info-bulle dans le Concepteur

1. Dans Visual Studio, ajoutez un <xref:System.Windows.Forms.ToolTip> composant au formulaire.

2. Sélectionnez le contrôle qui affiche l’info-bulle, ou ajoutez-le au formulaire.

3. Dans le **propriétés** fenêtre, définissez la **info-bulle sur ToolTip1** valeur à une chaîne de texte appropriée.

### <a name="to-remove-a-tooltip-programmatically"></a>Pour supprimer une info-bulle par programme

1. Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.

    ```vb
    ' In this example, Button1 is the control displaying the ToolTip.
    ToolTip1.SetToolTip(Button1, Nothing)
    ```

    ```csharp
    // In this example, button1 is the control displaying the ToolTip.
    toolTip1.SetToolTip(button1, null);
    ```

    ```cpp
    // In this example, button1 is the control displaying the ToolTip.
    toolTip1->SetToolTip(button1, NULL);
    ```

## <a name="remove-a-tooltip-in-the-designer"></a>Supprimer une info-bulle dans le Concepteur

1. Dans Visual Studio, sélectionnez le contrôle qui affiche l’info-bulle.

2. Dans le **propriétés** fenêtre, supprimez le texte dans le **info-bulle sur ToolTip1**.

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md)
- [Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
- [ToolTip, composant](tooltip-component-windows-forms.md)
