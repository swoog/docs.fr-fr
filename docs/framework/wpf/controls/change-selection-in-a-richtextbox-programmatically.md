---
title: Modification par programmation de la sélection dans un RichTextBox
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- changing selections in a text box [WPF]
- changing selections in a RichTextBox [WPF]
ms.assetid: f1213205-1ad7-4cd2-b115-460173cc5aa3
ms.openlocfilehash: a85dc4baa8a59d25f577996c541a422bbe2af24e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367074"
---
# <a name="change-selection-in-a-richtextbox-programmatically"></a>Modification par programmation de la sélection dans un RichTextBox
Cet exemple montre comment modifier par programme la sélection actuelle dans un <xref:System.Windows.Controls.RichTextBox>. Cette sélection est le même que si l’utilisateur a sélectionné le contenu à l’aide de l’interface utilisateur.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code décrit une nommée <xref:System.Windows.Controls.RichTextBox> contrôle avec du contenu simple.  
  
 [!code-xaml[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml#changeselectionprogrammaticalyexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Le code suivant sélectionne par programme du texte arbitraire lorsque l’utilisateur clique à l’intérieur de la <xref:System.Windows.Controls.RichTextBox>.  
  
 [!code-csharp[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml.cs#changeselectionprogrammaticalycodeexamplewholepage)]
 [!code-vb[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/VisualBasic/ChangeSelectionProgrammaticaly.xaml.vb#changeselectionprogrammaticalycodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
- [Vue d’ensemble de TextBox](textbox-overview.md)
