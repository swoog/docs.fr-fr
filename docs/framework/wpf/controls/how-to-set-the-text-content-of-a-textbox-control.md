---
title: 'Procédure : Définir le texte d’un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], setting
- TextBox control [WPF], setting text content
ms.assetid: bcd25fc7-a52f-4453-b802-2c8d2b335ab8
ms.openlocfilehash: da91e27b804d649f5b8010bc9d7c074425be26f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212191"
---
# <a name="how-to-set-the-text-content-of-a-textbox-control"></a>Procédure : Définir le texte d’un contrôle TextBox
Cet exemple montre comment utiliser le <xref:System.Windows.Controls.TextBox.Text%2A> propriété pour définir le texte initial d’un <xref:System.Windows.Controls.TextBox> contrôle.  
  
 **Remarque** bien que le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] version de l’exemple peut utiliser le `<TextBox.Text>` balises autour du texte de chaque bouton <xref:System.Windows.Controls.TextBox> contenu, il n’est pas nécessaire, car le <xref:System.Windows.Controls.TextBox> s’applique le <xref:System.Windows.Markup.ContentPropertyAttribute> attribut le <xref:System.Windows.Controls.TextBox.Text%2A> propriété. Pour plus d’informations, consultez [vue d’ensemble de XAML (WPF)](../advanced/xaml-overview-wpf.md).  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TextBox_MiscCode#_TextBoxSetTextXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxsettextxaml)]  
  
## <a name="example"></a>Exemple  
 [!code-csharp[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textboxsettext)]
 [!code-vb[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_textboxsettext)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
