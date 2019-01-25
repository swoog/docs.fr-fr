---
title: 'Procédure : Superposer des objets dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, layering
- controls [Windows Forms], layering
- z order
- controls [Windows Forms], positioning
- z-order
ms.assetid: 1acc4281-2976-4715-86f4-bda68134baaf
ms.openlocfilehash: 2911542f93bf6afaf1560d0f627af3de1b2871ba
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509183"
---
# <a name="how-to-layer-objects-on-windows-forms"></a>Procédure : Superposer des objets dans les Windows Forms
Lorsque vous créez une interface utilisateur complexe, ou travaillez avec un formulaire d’interface (multidocument MDI) document, vous souhaiterez souvent des contrôles et formulaires enfants pour créer des interfaces utilisateur plus complexes (IU) de couche. Pour déplacer et effectuer le suivi des contrôles et fenêtres dans le contexte d’un groupe, vous manipulez leur ordre de plan. *Ordre de plan* est la superposition visuelle des contrôles sur un formulaire sur l’axe z (profondeur). La fenêtre en haut de l’ordre de plan superpose à toutes les autres fenêtres. Toutes les autres fenêtres chevauchent à la fenêtre en bas de l’ordre de plan.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-layer-controls-at-design-time"></a>Pour les contrôles de la couche au moment du design  
  
1.  Sélectionnez un contrôle à la couche.  
  
2.  Sur le **Format** menu, pointez sur **ordre**, puis cliquez sur **mettre au premier plan** ou **arrière-plan**.  
  
### <a name="to-layer-controls-programmatically"></a>Pour superposer les contrôles par programmation  
  
-   Utilisez le <xref:System.Windows.Forms.Control.BringToFront%2A> et <xref:System.Windows.Forms.Control.SendToBack%2A> méthodes permettant de manipuler l’ordre de plan des contrôles.  
  
     Par exemple, si un <xref:System.Windows.Forms.TextBox> contrôle, `txtFirstName`, est en dessous un autre contrôle et que vous souhaitez elle est sur le haut, utilisez le code suivant :  
  
    ```vb  
    txtFirstName.BringToFront()  
    ```  
  
    ```csharp  
    txtFirstName.BringToFront();  
    ```  
  
    ```cpp  
    txtFirstName->BringToFront();  
    ```  
  
> [!NOTE]
>  Windows Forms prend en charge *contrôler la relation contenant-contenu*. Fonction consiste à placer un certain nombre de contrôles dans un contrôle conteneur, comme un nombre de <xref:System.Windows.Forms.RadioButton> contrôle au sein d’un <xref:System.Windows.Forms.GroupBox> contrôle. Vous pouvez ensuite superposer les contrôles dans le contrôle conteneur. La zone de groupe est déplacée, les contrôles, car elle contient.  
  
## <a name="see-also"></a>Voir aussi
- [Contrôles Windows Forms](../../../../docs/framework/winforms/controls/index.md)
- [Disposition des contrôles dans les Windows Forms](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Contrôles à utiliser dans les Windows Forms](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
- [Classement par fonction des contrôles Windows Forms](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
