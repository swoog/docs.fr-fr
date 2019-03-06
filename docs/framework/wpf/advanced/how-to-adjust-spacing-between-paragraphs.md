---
title: "Procédure : Ajuster l'espacement entre les paragraphes"
ms.date: 03/30/2017
helpviewer_keywords:
- spacing between paragraphs [WPF]
- paragraphs [WPF], spacing between
- documents [WPF], adjusting spacing between paragraphs
ms.assetid: 7cd2f2ac-0e19-4587-bfb6-7f5b18c9536e
ms.openlocfilehash: e2a6ba34e3ab15eb316671fef7c11bea03d53c73
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367477"
---
# <a name="how-to-adjust-spacing-between-paragraphs"></a><span data-ttu-id="b8718-102">Procédure : Ajuster l'espacement entre les paragraphes</span><span class="sxs-lookup"><span data-stu-id="b8718-102">How to: Adjust Spacing Between Paragraphs</span></span>
<span data-ttu-id="b8718-103">Cet exemple montre comment ajuster ou éliminer l’espacement entre les paragraphes dans le contenu dynamique.</span><span class="sxs-lookup"><span data-stu-id="b8718-103">This example shows how to adjust or eliminate spacing between paragraphs in flow content.</span></span>  
  
 <span data-ttu-id="b8718-104">Dans le contenu dynamique, un espace supplémentaire qui apparaît entre les paragraphes est le résultat des marges définies pour ces paragraphes ; Par conséquent, l’espacement entre les paragraphes peut être contrôlé en ajustant les marges sur ces paragraphes.</span><span class="sxs-lookup"><span data-stu-id="b8718-104">In flow content, extra space that appears between paragraphs is the result of margins set on these paragraphs; thus, the spacing between paragraphs can be controlled by adjusting the margins on those paragraphs.</span></span>  <span data-ttu-id="b8718-105">Pour éliminer complètement l’espacement supplémentaire entre deux paragraphes, définissez les marges pour les paragraphes à **0**.</span><span class="sxs-lookup"><span data-stu-id="b8718-105">To eliminate extra spacing between two paragraphs altogether, set the margins for the paragraphs to **0**.</span></span>  <span data-ttu-id="b8718-106">Pour obtenir un espacement uniforme entre les paragraphes tout au long de l’intégralité d’un <xref:System.Windows.Documents.FlowDocument>, utilisez les styles pour définir une valeur de marge uniforme pour tous les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="b8718-106">To achieve uniform spacing between paragraphs throughout an entire <xref:System.Windows.Documents.FlowDocument>, use styling to set a uniform margin value for all paragraphs in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 <span data-ttu-id="b8718-107">Il est important de noter que les marges de deux paragraphes adjacents sont « réduits » à la plus grande des deux marges, plutôt que se doubler.</span><span class="sxs-lookup"><span data-stu-id="b8718-107">It is important to note that the margins for two adjacent paragraphs will "collapse" to the larger of the two margins, rather than doubling up.</span></span> <span data-ttu-id="b8718-108">Par conséquent, si deux paragraphes adjacents ont des marges de 20 et 40 pixels respectivement, l’espace entre les paragraphes résultant est 40 pixels, la plus grande des deux valeurs de marges.</span><span class="sxs-lookup"><span data-stu-id="b8718-108">So, if two adjacent paragraphs have margins of 20 pixels and 40 pixels respectively, the resulting space between the paragraphs is 40 pixels, the larger of the two margin values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b8718-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8718-109">Example</span></span>  
 <span data-ttu-id="b8718-110">L’exemple suivant utilise des styles pour définir la marge pour tous les <xref:System.Windows.Documents.Paragraph> éléments dans un <xref:System.Windows.Documents.FlowDocument> à **0**, ce qui élimine l’espacement supplémentaire entre les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="b8718-110">The following example uses styling to set the margin for all <xref:System.Windows.Documents.Paragraph> elements in a <xref:System.Windows.Documents.FlowDocument> to **0**, which effectively eliminates extra spacing between paragraphs in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-xaml[BlockSnippets#_ParagraphSpacingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/BlockSnippets/CSharp/Window1.xaml#_paragraphspacingxaml)]
