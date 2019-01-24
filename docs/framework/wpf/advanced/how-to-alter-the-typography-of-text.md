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
ms.openlocfilehash: f04c873e542ad02c1d2a20b770ded4464af7a6d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645403"
---
# <a name="how-to-alter-the-typography-of-text"></a><span data-ttu-id="9cfae-102">Comment : Modifier la typographie d'un texte</span><span class="sxs-lookup"><span data-stu-id="9cfae-102">How-to: Alter the Typography of Text</span></span>
<span data-ttu-id="9cfae-103">L’exemple suivant montre comment définir le <xref:System.Windows.Documents.TextElement.Typography%2A> d’attribut, à l’aide de <xref:System.Windows.Documents.Paragraph> en tant que l’élément de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9cfae-103">The following example shows how to set the <xref:System.Windows.Documents.TextElement.Typography%2A> attribute, using <xref:System.Windows.Documents.Paragraph> as the example element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9cfae-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9cfae-104">Example</span></span>  
 [!code-xaml[TextElementSnippets#_TextElement_TypogXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml#_textelement_typogxaml)]  
  
 <span data-ttu-id="9cfae-105">La figure suivante montre le rendu de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="9cfae-105">The following figure shows how this example renders.</span></span>  
  
 <span data-ttu-id="9cfae-106">![Capture d’écran : Texte avec typographie altérée](../../../../docs/framework/wpf/advanced/media/textelement-typog.png "TextElement_Typog")</span><span class="sxs-lookup"><span data-stu-id="9cfae-106">![Screenshot: Text with altered typography](../../../../docs/framework/wpf/advanced/media/textelement-typog.png "TextElement_Typog")</span></span>  
  
 <span data-ttu-id="9cfae-107">Par contraste, l’illustration suivante montre comment s’affiche un exemple similaire avec des propriétés typographiques par défaut.</span><span class="sxs-lookup"><span data-stu-id="9cfae-107">In contrast, the following figure shows how a similar example with default typographic properties renders.</span></span>  
  
 <span data-ttu-id="9cfae-108">![Capture d’écran : Texte avec typographie altérée](../../../../docs/framework/wpf/advanced/media/textelement-typog-default.png "TextElement_Typog_Default")</span><span class="sxs-lookup"><span data-stu-id="9cfae-108">![Screenshot: Text with altered typography](../../../../docs/framework/wpf/advanced/media/textelement-typog-default.png "TextElement_Typog_Default")</span></span>  
  
## <a name="example"></a><span data-ttu-id="9cfae-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="9cfae-109">Example</span></span>  
 <span data-ttu-id="9cfae-110">L’exemple suivant montre comment définir le <xref:System.Windows.Controls.TextBox.Typography%2A> propriété par programmation.</span><span class="sxs-lookup"><span data-stu-id="9cfae-110">The following example shows how to set the <xref:System.Windows.Controls.TextBox.Typography%2A> property programmatically.</span></span>  
  
 [!code-csharp[TextElementSnippets#_TextElement_Typog](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextElementSnippets/CSharp/Window1.xaml.cs#_textelement_typog)]
 [!code-vb[TextElementSnippets#_TextElement_Typog](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextElementSnippets/visualbasic/window1.xaml.vb#_textelement_typog)]  
  
## <a name="see-also"></a><span data-ttu-id="9cfae-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cfae-111">See also</span></span>
- [<span data-ttu-id="9cfae-112">Vue d’ensemble des documents dynamiques</span><span class="sxs-lookup"><span data-stu-id="9cfae-112">Flow Document Overview</span></span>](../../../../docs/framework/wpf/advanced/flow-document-overview.md)
