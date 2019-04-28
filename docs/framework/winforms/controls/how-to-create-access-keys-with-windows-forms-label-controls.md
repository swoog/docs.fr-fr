---
title: 'Procédure : créer des clés d’accès avec les contrôles Label Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- Label control [Windows Forms], creating access keys
- mnemonics [Windows Forms], adding to dialog box controls
- mnemonics
- Windows Forms controls, access keys
- UseMnemonic property [Windows Forms], Label control
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
ms.assetid: 5ee8f823-80be-4a4f-96a4-412671e2e306
ms.openlocfilehash: ffe4bf6fb29e82b04938e2ba9a2d9d21e5eabcde
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61747106"
---
# <a name="how-to-create-access-keys-with-windows-forms-label-controls"></a>Procédure : créer des clés d’accès avec les contrôles Label Windows Forms
Windows Forms <xref:System.Windows.Forms.Label> contrôles peuvent être utilisés pour définir des clés d’accès pour d’autres contrôles. Lorsque vous définissez une clé d’accès dans un contrôle label, l’utilisateur peut appuyer sur la touche ALT et le caractère que vous désignez pour déplacer le focus au contrôle qui suit dans l’ordre de tabulation. Étant donné que les étiquettes ne peuvent pas recevoir le focus, le focus se déplace automatiquement vers le contrôle suivant dans l’ordre de tabulation. Utilisez cette technique pour affecter des clés d’accès aux zones de texte, zones de liste modifiable, zones de liste et des grilles de données.  
  
### <a name="to-assign-an-access-key-to-a-control-with-a-label"></a>Pour affecter une touche d’accès à un contrôle avec une étiquette  
  
1. Dessiner d’abord l’étiquette et dessinez l’autre contrôle.  
  
     - ou -  
  
     Dessiner les contrôles dans n’importe quel ordre et définir le <xref:System.Windows.Forms.Control.TabIndex%2A> propriété de l’étiquette et l’autre contrôle moins 1.  
  
2. Définir l’étiquette <xref:System.Windows.Forms.Label.UseMnemonic%2A> propriété `true`.  
  
3. Utilisez une esperluette (&) dans l’étiquette <xref:System.Windows.Forms.Label.Text%2A> propriété à attribuer la clé d’accès pour l’étiquette. Pour plus d’informations, consultez [création de clés d’accès rapide pour les contrôles Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md).  
  
    > [!NOTE]
    >  Voulez-vous afficher ce symbole dans un contrôle label, plutôt que de les utiliser pour créer des clés d’accès. Cela peut se produire si vous liez un contrôle étiquette à un champ dans un jeu d’enregistrements dans lequel les données incluent les et commerciaux. Pour afficher ce symbole dans un contrôle label, définissez le <xref:System.Windows.Forms.Label.UseMnemonic%2A> propriété `false`. Si vous souhaitez afficher le symbole & et ont également une clé d’accès, définissez le <xref:System.Windows.Forms.Label.UseMnemonic%2A> propriété `true` et indiquer la clé d’accès avec une esperluette (&) et l’esperluette par deux signes &.  
  
    ```vb  
    Label1.UseMnemonic = True  
    Label1.Text = "&Print"  
    Label2.UseMnemonic = True  
    Label2.Text = "&Copy && Paste"  
    ```  
  
    ```csharp  
    label1.UseMnemonic = true;  
    label1.Text = "&Print";  
    label2.UseMnemonic = true;  
    label2.Text = "&Copy && Paste";  
    ```  
  
    ```cpp  
    label1->UseMnemonic = true;  
    label1->Text = "&Print";  
    label2->UseMnemonic = true;  
    label2->Text = "&Copy && Paste";  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Taille d’un contrôle d’étiquette Windows Forms pour s’ajuster à son contenu](how-to-size-a-windows-forms-label-control-to-fit-its-contents.md)
- [Vue d'ensemble du contrôle Label](label-control-overview-windows-forms.md)
- [Label, contrôle](label-control-windows-forms.md)
