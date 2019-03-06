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
ms.openlocfilehash: c93a1c7542a4ddb33b3880de423c256adcc3f1c3
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378559"
---
# <a name="how-to-insert-an-element-into-text-programmatically"></a><span data-ttu-id="76358-102">Procédure : Insérer un élément dans du texte par programmation</span><span class="sxs-lookup"><span data-stu-id="76358-102">How to: Insert an Element Into Text Programmatically</span></span>
<span data-ttu-id="76358-103">L’exemple suivant montre comment utiliser deux <xref:System.Windows.Documents.TextPointer> objets pour spécifier une plage de texte où appliquer une <xref:System.Windows.Documents.Span> élément.</span><span class="sxs-lookup"><span data-stu-id="76358-103">The following example shows how to use two <xref:System.Windows.Documents.TextPointer> objects to specify a range within text to apply a <xref:System.Windows.Documents.Span> element to.</span></span>  
  
## <a name="example"></a><span data-ttu-id="76358-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="76358-104">Example</span></span>  
 [!code-csharp[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/CSharp/InsertInlineIntoTextExample.cs#insertinlineintotextexamplewholepage)]
 [!code-vb[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/VisualBasic/InsertInlineIntoTextExample.vb#insertinlineintotextexamplewholepage)]  
  
 <span data-ttu-id="76358-105">Cet exemple de code est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="76358-105">The illustration below shows what this example looks like.</span></span>  
  
 <span data-ttu-id="76358-106">![Élément Span appliqué à une plage de texte](./media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span><span class="sxs-lookup"><span data-stu-id="76358-106">![A Span element applied to a range of text](./media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76358-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76358-107">See also</span></span>
- [<span data-ttu-id="76358-108">Vue d’ensemble des documents dynamiques</span><span class="sxs-lookup"><span data-stu-id="76358-108">Flow Document Overview</span></span>](flow-document-overview.md)
