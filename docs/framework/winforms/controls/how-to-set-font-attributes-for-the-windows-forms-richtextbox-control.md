---
title: 'Procédure : définir des attributs de police pour le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- .rtf files [Windows Forms], formatting in RichTextBox control
- fonts [Windows Forms], changing attributes in RichTextBox control
- RTF files [Windows Forms], formatting in RichTextBox control
- RichTextBox control [Windows Forms], setting font attributes
- text [Windows Forms]
- text boxes [Windows Forms], formatting text
- formatting [Windows Forms]
ms.assetid: 2bc23ddb-0529-4489-a1a2-ad253cb43f9a
ms.openlocfilehash: a6fe5b30c457fae2d53c946092b214f492fe5e9b
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331206"
---
# <a name="how-to-set-font-attributes-for-the-windows-forms-richtextbox-control"></a>Procédure : définir des attributs de police pour le contrôle RichTextBox Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle a de nombreuses options pour mettre en forme le texte affiché. Vous pouvez afficher les caractères sélectionnés en gras, italique ou en souligné, à l’aide de la <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> propriété. Vous pouvez également utiliser cette propriété pour changer la taille et la police des caractères sélectionnés. Le <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> propriété permet de modifier la couleur des caractères sélectionnés.  
  
### <a name="to-change-the-appearance-of-characters"></a>Pour changer l’apparence de caractères  
  
1. Définir le <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> propriété à une police appropriée.  
  
     Pour permettre aux utilisateurs de définir la famille de polices, la taille et le type de caractères dans une application, vous utiliserez généralement le <xref:System.Windows.Forms.FontDialog> composant. Pour une vue d’ensemble, consultez [Vue d’ensemble du composant FontDialog](fontdialog-component-overview-windows-forms.md).  
  
2. Définir le <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> propriété sur une couleur appropriée.  
  
     Pour permettre aux utilisateurs de définir la couleur dans une application, vous utiliserez généralement le <xref:System.Windows.Forms.ColorDialog> composant. Pour une vue d’ensemble, consultez [Vue d’ensemble du composant ColorDialog](colordialog-component-overview-windows-forms.md).  
  
    ```vb  
    RichTextBox1.SelectionFont = New Font("Tahoma", 12, FontStyle.Bold)  
    RichTextBox1.SelectionColor = System.Drawing.Color.Red  
    ```  
  
    ```csharp  
    richTextBox1.SelectionFont = new Font("Tahoma", 12, FontStyle.Bold);  
    richTextBox1.SelectionColor = System.Drawing.Color.Red;  
    ```  
  
    ```cpp  
    richTextBox1->SelectionFont =  
       gcnew System::Drawing::Font("Tahoma", 12, FontStyle::Bold);  
    richTextBox1->SelectionColor = System::Drawing::Color::Red;  
    ```  
  
    > [!NOTE]
    >  Ces propriétés affectent uniquement le texte sélectionné ou, si aucun texte n’est sélectionné, le texte tapé à l’emplacement actif du point d’insertion. Pour plus d’informations sur la sélection de texte par programmation, consultez <xref:System.Windows.Forms.TextBoxBase.Select%2A>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
