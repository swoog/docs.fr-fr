---
title: 'Procédure : créer des clés d’accès pour les contrôles Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [Windows Forms], access keys
- Button control [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- mnemonics [Windows Forms], adding to dialog box controls
- mnemonics
- ampersand character in shortcut key
- Windows Forms controls, access keys
- examples [Windows Forms], controls
- Text property [Windows Forms], specifying access keys for controls
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
- ALT key
ms.assetid: 4faa0991-28ec-4eca-91db-51dc2cd6a7ac
ms.openlocfilehash: e6c829553163359301bad2cd896fc43562ee8069
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746812"
---
# <a name="how-to-create-access-keys-for-windows-forms-controls"></a>Procédure : créer des clés d’accès pour les contrôles Windows Forms
Un *clé d’accès* est un caractère souligné dans le texte d’un menu, un élément de menu ou l’étiquette d’un contrôle tel qu’un bouton. Avec une clé d’accès, l’utilisateur peut « cliquer » un bouton en appuyant sur la touche ALT conjointement avec la clé d’accès prédéfinies. Par exemple, si un bouton exécute une procédure pour imprimer un formulaire et par conséquent son `Text` propriété est définie à « Impression », en ajoutant une esperluette avant la lettre « P » provoque la lettre « P » être souligné dans le texte du bouton en cours d’exécution. L’utilisateur peut exécuter la commande associée au bouton en appuyant sur ALT + P. Vous ne pouvez avoir une clé d’accès pour un contrôle qui ne peut pas recevoir le focus.  
  
### <a name="to-create-an-access-key-for-a-control"></a>Pour créer une clé d’accès pour un contrôle  
  
1. Définir le `Text` propriété à une chaîne qui inclut une esperluette (&) avant la lettre qui sera le raccourci.  
  
    ```vb  
    ' Set the letter "P" as an access key.  
    Button1.Text = "&Print"  
    ```  
  
    ```csharp  
    // Set the letter "P" as an access key.  
    button1.Text = "&Print";  
    ```  
  
    ```cpp  
    // Set the letter "P" as an access key.  
    button1->Text = "&Print";  
    ```  
  
    > [!NOTE]
    >  Pour inclure une esperluette dans une légende sans créer une clé d’accès, insérez deux et commerciaux (& &). Une esperluette unique s’affiche dans la légende et aucun caractère n’est soulignées.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Button>
- [Guide pratique pour Répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Guide pratique pour Définir le texte affiché par un Windows Forms de contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [Création d'étiquettes et de raccourcis pour les contrôles Windows Forms](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
