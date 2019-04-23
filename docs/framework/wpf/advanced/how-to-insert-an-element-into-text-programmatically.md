---
title: 'Procédure : Insérer un élément dans du texte par programmation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Text Animation sample [WPF]
- elements [WPF], inserting into text
- inserting elements into text [WPF]
- TextPointer objects [WPF]
- text [WPF], inserting elements
ms.assetid: 97bd950a-25ac-4e42-a311-94b6420d4136
ms.openlocfilehash: ea9850c8490ec37032d4565c6b3375e3116d4313
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169583"
---
# <a name="how-to-insert-an-element-into-text-programmatically"></a><span data-ttu-id="a2b92-102">Procédure : Insérer un élément dans du texte par programmation</span><span class="sxs-lookup"><span data-stu-id="a2b92-102">How to: Insert an Element Into Text Programmatically</span></span>
<span data-ttu-id="a2b92-103">L’exemple suivant montre comment utiliser deux <xref:System.Windows.Documents.TextPointer> objets pour spécifier une plage de texte où appliquer une <xref:System.Windows.Documents.Span> élément.</span><span class="sxs-lookup"><span data-stu-id="a2b92-103">The following example shows how to use two <xref:System.Windows.Documents.TextPointer> objects to specify a range within text to apply a <xref:System.Windows.Documents.Span> element to.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a2b92-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2b92-104">Example</span></span>  
 [!code-csharp[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/CSharp/InsertInlineIntoTextExample.cs#insertinlineintotextexamplewholepage)]
 [!code-vb[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/VisualBasic/InsertInlineIntoTextExample.vb#insertinlineintotextexamplewholepage)]  
  
 <span data-ttu-id="a2b92-105">Cet exemple de code est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a2b92-105">The illustration below shows what this example looks like.</span></span>  
  
 <span data-ttu-id="a2b92-106">![Élément Span appliqué à une plage de texte](./media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span><span class="sxs-lookup"><span data-stu-id="a2b92-106">![A Span element applied to a range of text](./media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2b92-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2b92-107">See also</span></span>

- [<span data-ttu-id="a2b92-108">Vue d’ensemble des documents dynamiques</span><span class="sxs-lookup"><span data-stu-id="a2b92-108">Flow Document Overview</span></span>](flow-document-overview.md)
