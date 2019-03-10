---
title: 'Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], for controls
- examples [Windows Forms], tooltips
ms.assetid: c4b60637-4c0a-44c2-a103-f66dff887936
ms.openlocfilehash: 541e50a8ee9c5338acc7c5e347549fd03a0f6323
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710717"
---
# <a name="how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time"></a>Procédure : Définir des info-bulles pour les contrôles sur un formulaire Windows au moment du Design
Vous pouvez définir un <xref:System.Windows.Forms.ToolTip> chaîne dans le code ou dans le Concepteur de formulaires Windows. Pour plus d’informations sur la <xref:System.Windows.Forms.ToolTip> composant, consultez [vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-a-tooltip-programmatically"></a>Pour définir une info-bulle par programmation  
  
1.  Ajoutez le contrôle qui affiche l’info-bulle.  
  
2.  Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.  
  
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
  
### <a name="to-set-a-tooltip-in-the-designer"></a>Pour définir une info-bulle dans le Concepteur  
  
1.  Ajoutez un composant <xref:System.Windows.Forms.ToolTip> au formulaire.  
  
2.  Sélectionnez le contrôle qui affiche l’info-bulle, ou ajoutez-le au formulaire.  
  
3.  Dans le **propriétés** fenêtre, définissez la **info-bulle sur ToolTip1** valeur à une chaîne de texte appropriée.  

### <a name="to-remove-a-tooltip-programmatically"></a>Pour supprimer une info-bulle par programme  
  
1.  Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.  
  
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
  
### <a name="to-remove-a-tooltip-in-the-designer"></a>Pour supprimer une info-bulle dans le Concepteur  
  
1.  Sélectionnez le contrôle qui affiche l’info-bulle.  
  
2.  Dans le **propriétés** fenêtre, supprimez le texte dans le **info-bulle sur ToolTip1**.  

## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md)
- [Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
- [ToolTip, composant](tooltip-component-windows-forms.md)
