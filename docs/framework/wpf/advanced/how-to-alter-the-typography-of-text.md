---
title: "Comment : Modifier la typographie d'un texte"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- setting Typography attributes [WPF]
- Typography attribute [WPF], setting
ms.assetid: 19a3b49b-60a2-4c11-a786-e26b4c965588
ms.openlocfilehash: eeed93f62802a942915511db060c0e6c029579e0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57365778"
---
# <a name="how-to-alter-the-typography-of-text"></a>Comment : Modifier la typographie d'un texte
L’exemple suivant montre comment définir le <xref:System.Windows.Documents.TextElement.Typography%2A> d’attribut, à l’aide de <xref:System.Windows.Documents.Paragraph> en tant que l’élément de l’exemple.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TextElementSnippets#_TextElement_TypogXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml#_textelement_typogxaml)]  
  
 La figure suivante montre le rendu de cet exemple.  
  
 ![Capture d’écran : Texte avec typographie altérée](./media/textelement-typog.png "TextElement_Typog")  
  
 Par contraste, l’illustration suivante montre comment s’affiche un exemple similaire avec des propriétés typographiques par défaut.  
  
 ![Capture d’écran : Texte avec typographie altérée](./media/textelement-typog-default.png "TextElement_Typog_Default")  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment définir le <xref:System.Windows.Controls.TextBox.Typography%2A> propriété par programmation.  
  
 [!code-csharp[TextElementSnippets#_TextElement_Typog](~/samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml.cs#_textelement_typog)]
 [!code-vb[TextElementSnippets#_TextElement_Typog](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextElementSnippets/visualbasic/window1.xaml.vb#_textelement_typog)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des documents dynamiques](flow-document-overview.md)
