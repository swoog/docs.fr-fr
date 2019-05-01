---
title: 'Procédure : Utiliser les éléments de contenu de flux'
ms.date: 03/30/2017
helpviewer_keywords:
- flow content elements [WPF]
- documents [WPF], flow content elements
ms.assetid: 70fa11cd-5fa7-4872-a1cc-04d80f1132be
ms.openlocfilehash: df591304736adf1725b2b4235149bd426fe15216
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052350"
---
# <a name="how-to-use-flow-content-elements"></a><span data-ttu-id="620bb-102">Procédure : Utiliser les éléments de contenu de flux</span><span class="sxs-lookup"><span data-stu-id="620bb-102">How to: Use Flow Content Elements</span></span>
<span data-ttu-id="620bb-103">L’exemple suivant illustre l’utilisation déclarative de différents éléments de contenu de flux et les attributs associés.</span><span class="sxs-lookup"><span data-stu-id="620bb-103">The following example demonstrates declarative usage for various flow content elements and associated attributes.</span></span>  <span data-ttu-id="620bb-104">Parmi les éléments et attributs illustrés figurent :</span><span class="sxs-lookup"><span data-stu-id="620bb-104">Elements and attributes demonstrated include:</span></span>  
  
- <span data-ttu-id="620bb-105"><xref:System.Windows.Documents.Bold>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-105"><xref:System.Windows.Documents.Bold> element</span></span>  
  
- <span data-ttu-id="620bb-106"><xref:System.Windows.Documents.Block.BreakPageBefore%2A> Attribut</span><span class="sxs-lookup"><span data-stu-id="620bb-106"><xref:System.Windows.Documents.Block.BreakPageBefore%2A> attribute</span></span>  
  
- <span data-ttu-id="620bb-107"><xref:System.Windows.Documents.TextElement.FontSize%2A> Attribut</span><span class="sxs-lookup"><span data-stu-id="620bb-107"><xref:System.Windows.Documents.TextElement.FontSize%2A> attribute</span></span>  
  
- <span data-ttu-id="620bb-108"><xref:System.Windows.Documents.Italic>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-108"><xref:System.Windows.Documents.Italic> element</span></span>  
  
- <span data-ttu-id="620bb-109"><xref:System.Windows.Documents.LineBreak>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-109"><xref:System.Windows.Documents.LineBreak> element</span></span>  
  
- <span data-ttu-id="620bb-110"><xref:System.Windows.Documents.List>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-110"><xref:System.Windows.Documents.List> element</span></span>  
  
- <span data-ttu-id="620bb-111"><xref:System.Windows.Documents.ListItem>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-111"><xref:System.Windows.Documents.ListItem> element</span></span>  
  
- <span data-ttu-id="620bb-112"><xref:System.Windows.Documents.Paragraph>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-112"><xref:System.Windows.Documents.Paragraph> element</span></span>  
  
- <span data-ttu-id="620bb-113"><xref:System.Windows.Documents.Run>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-113"><xref:System.Windows.Documents.Run> element</span></span>  
  
- <span data-ttu-id="620bb-114"><xref:System.Windows.Documents.Section>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-114"><xref:System.Windows.Documents.Section> element</span></span>  
  
- <span data-ttu-id="620bb-115"><xref:System.Windows.Documents.Span>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-115"><xref:System.Windows.Documents.Span> element</span></span>  
  
- <span data-ttu-id="620bb-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribut (exposant et indice)</span><span class="sxs-lookup"><span data-stu-id="620bb-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribute (superscript and subscript)</span></span>  
  
- <span data-ttu-id="620bb-117"><xref:System.Windows.Documents.Underline>, élément</span><span class="sxs-lookup"><span data-stu-id="620bb-117"><xref:System.Windows.Documents.Underline> element</span></span>  
  
## <a name="example"></a><span data-ttu-id="620bb-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="620bb-118">Example</span></span>  
 [!code-xaml[FlowDocInlineSnippets#_InlineElementsXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocInlineSnippets/CS/document.xaml#_inlineelementsxaml)]
