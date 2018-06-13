---
title: 'Comment : utiliser les attributs de séparation de colonnes de FlowDocument'
ms.date: 03/30/2017
helpviewer_keywords:
- FlowDocument column-separating attributes
- column-separating attributes
- documents [WPF], FlowDocument column-separating attributes
ms.assetid: c7a822f8-aeca-45bd-a258-2852ff28005c
ms.openlocfilehash: 678e01a35c286ea03f0385291d64f2f900f068c5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543769"
---
# <a name="how-to-use-flowdocument-column-separating-attributes"></a><span data-ttu-id="0cc71-102">Comment : utiliser les attributs de séparation de colonnes de FlowDocument</span><span class="sxs-lookup"><span data-stu-id="0cc71-102">How to: Use FlowDocument Column-Separating Attributes</span></span>
<span data-ttu-id="0cc71-103">Cet exemple montre comment utiliser les fonctionnalités de séparation de colonnes d’un <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="0cc71-103">This example shows how to use the column-separating features of a <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0cc71-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0cc71-104">Example</span></span>  
 <span data-ttu-id="0cc71-105">L’exemple suivant définit un <xref:System.Windows.Documents.FlowDocument>et définit les <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs.</span><span class="sxs-lookup"><span data-stu-id="0cc71-105">The following example defines a <xref:System.Windows.Documents.FlowDocument>, and sets the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes.</span></span>  <span data-ttu-id="0cc71-106">Le <xref:System.Windows.Documents.FlowDocument> contient un paragraphe unique d’exemple de contenu.</span><span class="sxs-lookup"><span data-stu-id="0cc71-106">The <xref:System.Windows.Documents.FlowDocument> contains a single paragraph of sample content.</span></span>  
  
 [!code-xaml[FlowDocumentSnippets#_FlowDocumentColumnStuffXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml#_flowdocumentcolumnstuffxaml)]  
  
 <span data-ttu-id="0cc71-107">L’illustration suivante montre les effets de la <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs dans un rendu <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="0cc71-107">The following figure shows the effects of the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes in a rendered <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 <span data-ttu-id="0cc71-108">![Capture d’écran : FlowDocument intra-colonnes](../../../../docs/framework/wpf/advanced/media/flowdocumentintracolumn.png "FlowDocumentIntraColumn")</span><span class="sxs-lookup"><span data-stu-id="0cc71-108">![Screenshot: FlowDocument Intra Column](../../../../docs/framework/wpf/advanced/media/flowdocumentintracolumn.png "FlowDocumentIntraColumn")</span></span>
