---
title: 'Procédure : Utiliser les éléments de contenu de flux'
ms.date: 03/30/2017
helpviewer_keywords:
- flow content elements [WPF]
- documents [WPF], flow content elements
ms.assetid: 70fa11cd-5fa7-4872-a1cc-04d80f1132be
ms.openlocfilehash: df591304736adf1725b2b4235149bd426fe15216
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57368105"
---
# <a name="how-to-use-flow-content-elements"></a><span data-ttu-id="19b9d-102">Procédure : Utiliser les éléments de contenu de flux</span><span class="sxs-lookup"><span data-stu-id="19b9d-102">How to: Use Flow Content Elements</span></span>
<span data-ttu-id="19b9d-103">L’exemple suivant illustre l’utilisation déclarative de différents éléments de contenu de flux et les attributs associés.</span><span class="sxs-lookup"><span data-stu-id="19b9d-103">The following example demonstrates declarative usage for various flow content elements and associated attributes.</span></span>  <span data-ttu-id="19b9d-104">Parmi les éléments et attributs illustrés figurent :</span><span class="sxs-lookup"><span data-stu-id="19b9d-104">Elements and attributes demonstrated include:</span></span>  
  
-   <span data-ttu-id="19b9d-105"><xref:System.Windows.Documents.Bold> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-105"><xref:System.Windows.Documents.Bold> element</span></span>  
  
-   <span data-ttu-id="19b9d-106">Attribut <xref:System.Windows.Documents.Block.BreakPageBefore%2A></span><span class="sxs-lookup"><span data-stu-id="19b9d-106"><xref:System.Windows.Documents.Block.BreakPageBefore%2A> attribute</span></span>  
  
-   <span data-ttu-id="19b9d-107">Attribut <xref:System.Windows.Documents.TextElement.FontSize%2A></span><span class="sxs-lookup"><span data-stu-id="19b9d-107"><xref:System.Windows.Documents.TextElement.FontSize%2A> attribute</span></span>  
  
-   <span data-ttu-id="19b9d-108"><xref:System.Windows.Documents.Italic> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-108"><xref:System.Windows.Documents.Italic> element</span></span>  
  
-   <span data-ttu-id="19b9d-109"><xref:System.Windows.Documents.LineBreak> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-109"><xref:System.Windows.Documents.LineBreak> element</span></span>  
  
-   <span data-ttu-id="19b9d-110"><xref:System.Windows.Documents.List> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-110"><xref:System.Windows.Documents.List> element</span></span>  
  
-   <span data-ttu-id="19b9d-111"><xref:System.Windows.Documents.ListItem> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-111"><xref:System.Windows.Documents.ListItem> element</span></span>  
  
-   <span data-ttu-id="19b9d-112"><xref:System.Windows.Documents.Paragraph> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-112"><xref:System.Windows.Documents.Paragraph> element</span></span>  
  
-   <span data-ttu-id="19b9d-113"><xref:System.Windows.Documents.Run> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-113"><xref:System.Windows.Documents.Run> element</span></span>  
  
-   <span data-ttu-id="19b9d-114"><xref:System.Windows.Documents.Section> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-114"><xref:System.Windows.Documents.Section> element</span></span>  
  
-   <span data-ttu-id="19b9d-115"><xref:System.Windows.Documents.Span> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-115"><xref:System.Windows.Documents.Span> element</span></span>  
  
-   <span data-ttu-id="19b9d-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribut (exposant et indice)</span><span class="sxs-lookup"><span data-stu-id="19b9d-116"><xref:System.Windows.Documents.Typography.Variants%2A> attribute (superscript and subscript)</span></span>  
  
-   <span data-ttu-id="19b9d-117"><xref:System.Windows.Documents.Underline> (élément)</span><span class="sxs-lookup"><span data-stu-id="19b9d-117"><xref:System.Windows.Documents.Underline> element</span></span>  
  
## <a name="example"></a><span data-ttu-id="19b9d-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="19b9d-118">Example</span></span>  
 [!code-xaml[FlowDocInlineSnippets#_InlineElementsXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocInlineSnippets/CS/document.xaml#_inlineelementsxaml)]
