---
title: 'Procédure : Utiliser les éléments de contenu de flux'
ms.date: 03/30/2017
helpviewer_keywords:
- flow content elements [WPF]
- documents [WPF], flow content elements
ms.assetid: 70fa11cd-5fa7-4872-a1cc-04d80f1132be
ms.openlocfilehash: f61116c0bf52ac726238d9e21c2422cedbb4716f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663324"
---
# <a name="how-to-use-flow-content-elements"></a><span data-ttu-id="15437-102">Procédure : Utiliser les éléments de contenu de flux</span><span class="sxs-lookup"><span data-stu-id="15437-102">How to: Use Flow Content Elements</span></span>
<span data-ttu-id="15437-103">L’exemple suivant illustre l’utilisation déclarative de différents éléments de contenu de flux et les attributs associés.</span><span class="sxs-lookup"><span data-stu-id="15437-103">The following example demonstrates declarative usage for various flow content elements and associated attributes.</span></span>  <span data-ttu-id="15437-104">Parmi les éléments et attributs illustrés figurent :</span><span class="sxs-lookup"><span data-stu-id="15437-104">Elements and attributes demonstrated include:</span></span>  
  
- <span data-ttu-id="15437-105"><xref:System.Windows.Documents.Bold>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-105"><xref:System.Windows.Documents.Bold> element</span></span>  
  
- <span data-ttu-id="15437-106"><xref:System.Windows.Documents.Block.BreakPageBefore%2A> Attribut</span><span class="sxs-lookup"><span data-stu-id="15437-106"><xref:System.Windows.Documents.Block.BreakPageBefore%2A> attribute</span></span>  
  
- <span data-ttu-id="15437-107"><xref:System.Windows.Documents.TextElement.FontSize%2A> Attribut</span><span class="sxs-lookup"><span data-stu-id="15437-107"><xref:System.Windows.Documents.TextElement.FontSize%2A> attribute</span></span>  
  
- <span data-ttu-id="15437-108"><xref:System.Windows.Documents.Italic>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-108"><xref:System.Windows.Documents.Italic> element</span></span>  
  
- <span data-ttu-id="15437-109"><xref:System.Windows.Documents.LineBreak>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-109"><xref:System.Windows.Documents.LineBreak> element</span></span>  
  
- <span data-ttu-id="15437-110"><xref:System.Windows.Documents.List>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-110"><xref:System.Windows.Documents.List> element</span></span>  
  
- <span data-ttu-id="15437-111"><xref:System.Windows.Documents.ListItem>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-111"><xref:System.Windows.Documents.ListItem> element</span></span>  
  
- <span data-ttu-id="15437-112"><xref:System.Windows.Documents.Paragraph>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-112"><xref:System.Windows.Documents.Paragraph> element</span></span>  
  
- <span data-ttu-id="15437-113"><xref:System.Windows.Documents.Run>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-113"><xref:System.Windows.Documents.Run> element</span></span>  
  
- <span data-ttu-id="15437-114"><xref:System.Windows.Documents.Section>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-114"><xref:System.Windows.Documents.Section> element</span></span>  
  
- <span data-ttu-id="15437-115"><xref:System.Windows.Documents.Span>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-115"><xref:System.Windows.Documents.Span> element</span></span>  
  
- <span data-ttu-id="15437-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribut (exposant et indice)</span><span class="sxs-lookup"><span data-stu-id="15437-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribute (superscript and subscript)</span></span>  
  
- <span data-ttu-id="15437-117"><xref:System.Windows.Documents.Underline>, élément</span><span class="sxs-lookup"><span data-stu-id="15437-117"><xref:System.Windows.Documents.Underline> element</span></span>  
  
## <a name="example"></a><span data-ttu-id="15437-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="15437-118">Example</span></span>  
 [!code-xaml[FlowDocInlineSnippets#_InlineElementsXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocInlineSnippets/CS/document.xaml#_inlineelementsxaml)]
