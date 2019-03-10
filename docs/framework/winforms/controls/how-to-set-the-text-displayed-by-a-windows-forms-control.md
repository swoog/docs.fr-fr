---
title: 'Procédure : Définir le texte affiché par un Windows Forms de contrôle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, captions
- Button control [Windows Forms], button text
- StdFont object and CommandButton caption
- captions [Windows Forms], Windows Forms controls
- Text property [Windows Forms], Windows Forms control
- Button control [Windows Forms], text display
- labels [Windows Forms], adding to CommandButton control
- buttons [Windows Forms], text
- captions [Windows Forms], setting
- text
- examples [Windows Forms], controls
- text [Windows Forms], Windows Forms controls
- controls [Windows Forms], captions
- forms [Windows Forms], captions
ms.assetid: 36b95bff-8780-479d-b86a-f1a0673653aa
ms.openlocfilehash: 8ebb39e4e9337ede0dc8c7f5569ea27d8cfafd26
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716905"
---
# <a name="how-to-set-the-text-displayed-by-a-windows-forms-control"></a>Procédure : Définir le texte affiché par un Windows Forms de contrôle
Généralement, les contrôles Windows Forms affichent du texte en rapport avec la fonction principale du contrôle. Par exemple, un contrôle <xref:System.Windows.Forms.Button> affiche habituellement une légende indiquant l'action à exécuter quand le bouton est activé. Pour tous les contrôles, vous pouvez définir ou retourner le texte à l'aide de la propriété <xref:System.Windows.Forms.Control.Text%2A>. Vous pouvez modifier la police en utilisant la propriété <xref:System.Windows.Forms.Control.Font%2A>. Vous pouvez également définir le texte à l'aide du concepteur.  Voir également [Guide pratique pour Créer des touches d’accès rapide pour Windows Forms à l’aide du Concepteur de contrôles](how-to-create-access-keys-for-windows-forms-controls-using-the-designer.md), [Comment : Définir le texte affiché par un Windows Forms à l’aide du Concepteur de contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer.md), [Comment : Définir l’Image affichée par un Windows Forms à l’aide du Concepteur de contrôle](how-to-set-the-image-displayed-by-a-windows-forms-control-using-the-designer.md).  
  
### <a name="to-set-the-text-displayed-by-a-control-programmatically"></a>Pour définir le texte affiché par un contrôle par programmation  
  
1.  Affectez une chaîne comme valeur de la propriété <xref:System.Windows.Forms.Control.Text%2A>.  
  
     Pour créer une touche d'accès soulignée, incluez une esperluette (&) avant la lettre qui sera la touche d'accès.  
  
2.  Affectez un objet de type <xref:System.Drawing.Font> comme valeur de la propriété <xref:System.Windows.Forms.Control.Font%2A>.  
  
    ```vb  
    Button1.Text = "Click here to save changes"  
    Button1.Font = New Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point)  
    ```  
  
    ```csharp  
    button1.Text = "Click here to save changes";  
    button1.Font = new Font("Arial", 10, FontStyle.Bold,  
       GraphicsUnit.Point);  
    ```  
  
    ```cpp  
    button1->Text = "Click here to save changes";  
    button1->Font = new System::Drawing::Font("Arial",  
       10, FontStyle::Bold, GraphicsUnit::Point);  
    ```  
  
    > [!NOTE]
    >  Vous pouvez utiliser un caractère d'échappement pour afficher un caractère spécial dans des éléments d'interface utilisateur qui l'interpréteraient normalement différemment, tels que des éléments de menu. Par exemple, la ligne de code suivante définit le texte de l'élément de menu pour qu'il indique « & Now For Something Completely Different » :  
  
    ```vb  
    MPMenuItem.Text = "&& Now For Something Completely Different"  
    ```  
  
    ```csharp  
    mpMenuItem.Text = "&& Now For Something Completely Different";  
    ```  
  
    ```cpp  
    mpMenuItem->Text = "&& Now For Something Completely Different";  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Control.Text%2A?displayProperty=nameWithType>
- [Guide pratique pour Créer des clés d’accès pour les contrôles Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md)
- [Guide pratique pour Répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
