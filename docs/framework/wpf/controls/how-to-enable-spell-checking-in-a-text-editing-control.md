---
title: "Procédure : Activer la vérification de l'orthographe dans un contrôle d'édition de texte"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- spellchecking [WPF]
- real-time spellchecking
- TextBox control [WPF], real-time spellchecking
- spelling checker [WPF]
- checking spelling [WPF]
ms.assetid: 6f953d2b-67e8-4012-84ce-53c0e958da47
ms.openlocfilehash: 633ffe38503df743df355a8b476e7b254fcafffa
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370673"
---
# <a name="how-to-enable-spell-checking-in-a-text-editing-control"></a>Procédure : Activer la vérification de l'orthographe dans un contrôle d'édition de texte
L’exemple suivant montre comment activer la correction orthographique en temps réel un <xref:System.Windows.Controls.TextBox> à l’aide de la <xref:System.Windows.Controls.SpellCheck.IsEnabled%2A> propriété de la <xref:System.Windows.Controls.SpellCheck> classe.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TextBoxMiscSnippets_snip#SpellCheckExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/spellcheckexample.xaml#spellcheckexamplewholepage)]  
  
 [!code-csharp[TextBoxMiscSnippets_procedural_snip#SpellCheckCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_procedural_snip/CSharp/SpellCheckExample.cs#spellcheckcodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_procedural_snip#SpellCheckCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_procedural_snip/visualbasic/spellcheckexample.vb#spellcheckcodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Utiliser la vérification de l'orthographe avec un menu contextuel](how-to-use-spell-checking-with-a-context-menu.md)
- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
