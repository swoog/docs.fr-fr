---
title: 'Procédure : Ajouter un filigrane à un TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a background image inside a text box to aid user input [WPF]
- aid usability of a TextBox using a background image [WPF]
ms.assetid: df89bdd8-a0fb-45e0-b312-dd53332d01a8
ms.openlocfilehash: 5a2b48c6f580def98a47913c4909d0c57aca0974
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57359417"
---
# <a name="how-to-add-a-watermark-to-a-textbox"></a>Procédure : Ajouter un filigrane à un TextBox
L’exemple suivant montre comment faciliter l’utilisation d’un <xref:System.Windows.Controls.TextBox> en affichant une image d’arrière-plan explicative à l’intérieur de la <xref:System.Windows.Controls.TextBox> jusqu'à ce que l’utilisateur entre le texte, moment où l’image est supprimée. En outre, l’image d’arrière-plan est restaurée si l’utilisateur supprime son entrée. Voir l’illustration ci-dessous.  
  
 ![Une zone de texte avec une image d’arrière-plan](./media/editing-textbox-using-background-image.png "Editing_TextBox_using_background_image")  
  
> [!NOTE]
>  La raison pour laquelle une image d’arrière-plan est utilisée dans cet exemple au lieu de simplement manipuler la <xref:System.Windows.Controls.TextBox.Text%2A> propriété du <xref:System.Windows.Controls.TextBox>, est qu’une image d’arrière-plan n’interfère pas avec la liaison de données.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TextBoxMiscSnippets_snip#TextBoxBackgroundExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml#textboxbackgroundexamplewholepage)]  
  
 [!code-csharp[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml.cs#textboxbackgroundcodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/textbox_with_background_image.xaml.vb#textboxbackgroundcodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
