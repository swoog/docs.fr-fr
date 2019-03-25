---
title: 'Procédure : Utiliser les attributs de séparation de colonnes de FlowDocument'
ms.date: 03/30/2017
helpviewer_keywords:
- FlowDocument column-separating attributes
- column-separating attributes
- documents [WPF], FlowDocument column-separating attributes
ms.assetid: c7a822f8-aeca-45bd-a258-2852ff28005c
ms.openlocfilehash: 27491b21da587fa198061ba52d8daed5d3f28de3
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58410899"
---
# <a name="how-to-use-flowdocument-column-separating-attributes"></a><span data-ttu-id="6b1a4-102">Procédure : Utiliser les attributs de séparation de colonnes de FlowDocument</span><span class="sxs-lookup"><span data-stu-id="6b1a4-102">How to: Use FlowDocument Column-Separating Attributes</span></span>
<span data-ttu-id="6b1a4-103">Cet exemple montre comment utiliser les fonctionnalités de séparation de colonnes d’un <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="6b1a4-103">This example shows how to use the column-separating features of a <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b1a4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6b1a4-104">Example</span></span>  
 <span data-ttu-id="6b1a4-105">L’exemple suivant définit un <xref:System.Windows.Documents.FlowDocument>et définit le <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs.</span><span class="sxs-lookup"><span data-stu-id="6b1a4-105">The following example defines a <xref:System.Windows.Documents.FlowDocument>, and sets the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes.</span></span>  <span data-ttu-id="6b1a4-106">Le <xref:System.Windows.Documents.FlowDocument> contient un paragraphe unique d’exemple de contenu.</span><span class="sxs-lookup"><span data-stu-id="6b1a4-106">The <xref:System.Windows.Documents.FlowDocument> contains a single paragraph of sample content.</span></span>  
  
 [!code-xaml[FlowDocumentSnippets#_FlowDocumentColumnStuffXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml#_flowdocumentcolumnstuffxaml)]  
  
 <span data-ttu-id="6b1a4-107">La figure suivante montre les effets de la <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs dans un rendu <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="6b1a4-107">The following figure shows the effects of the <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, and <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributes in a rendered <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 ![Capture d’écran montrant l’attribut FlowDocument intra-colonnes.](./media/how-to-use-flowdocument-column-separating-attributes/flowdocument-intra-column.png)
