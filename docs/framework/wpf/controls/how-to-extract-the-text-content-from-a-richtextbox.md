---
title: 'Procédure : Extraire le texte d’un RichTextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], extracting
- RichTextBox control [WPF], extracting text content
- content [WPF], extracting
- extracting text content [WPF]
ms.assetid: f13c093f-1a05-45b3-ac8f-c9ea5e4a11c5
ms.openlocfilehash: 220da59ec893528c99014e9ec95fb185c461b291
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086115"
---
# <a name="how-to-extract-the-text-content-from-a-richtextbox"></a>Procédure : Extraire le texte d’un RichTextBox
Cet exemple montre comment extraire le contenu d’un <xref:System.Windows.Controls.RichTextBox> en tant que texte brut.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code décrit une nommée <xref:System.Windows.Controls.RichTextBox> contrôle avec du contenu simple.  
  
 [!code-xaml[RichTextBoxSnippets#_RTB_XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml#_rtb_xaml)]  
  
## <a name="example"></a>Exemple  
 Le code suivant implémente une méthode qui prend un <xref:System.Windows.Controls.RichTextBox> en tant qu’argument et retourne une chaîne représentant le contenu de texte brut de la <xref:System.Windows.Controls.RichTextBox>.  
  
 La méthode crée un nouveau <xref:System.Windows.Documents.TextRange> à partir du contenu de la <xref:System.Windows.Controls.RichTextBox>, en utilisant le <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> et <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> pour indiquer la plage de contenu à extraire.  <xref:System.Windows.Documents.FlowDocument.ContentStart%2A> et <xref:System.Windows.Documents.FlowDocument.ContentEnd%2A> chacune des propriétés retournent un <xref:System.Windows.Documents.TextPointer>et sont accessibles dans le FlowDocument sous-jacent qui représente le contenu de la <xref:System.Windows.Controls.RichTextBox>.  <xref:System.Windows.Documents.TextRange> Fournit une propriété de texte, qui retourne les parties de texte brut de la <xref:System.Windows.Documents.TextRange> sous forme de chaîne.  
  
 [!code-csharp[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxSnippets/CSharp/Window1.xaml.cs#_rtb_stringfrom)]
 [!code-vb[RichTextBoxSnippets#_RTB_StringFrom](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxSnippets/visualbasic/window1.xaml.vb#_rtb_stringfrom)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
- [Vue d’ensemble de TextBox](textbox-overview.md)
