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
ms.openlocfilehash: 460524a88427ef5fa822461a7bb985426fefea53
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693186"
---
# <a name="how-to-insert-an-element-into-text-programmatically"></a>Procédure : Insérer un élément dans du texte par programmation
L’exemple suivant montre comment utiliser deux <xref:System.Windows.Documents.TextPointer> objets pour spécifier une plage de texte où appliquer une <xref:System.Windows.Documents.Span> élément.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/CSharp/InsertInlineIntoTextExample.cs#insertinlineintotextexamplewholepage)]
 [!code-vb[FlowMiscSnippets_procedural_snip#InsertInlineIntoTextExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowMiscSnippets_procedural_snip/VisualBasic/InsertInlineIntoTextExample.vb#insertinlineintotextexamplewholepage)]  
  
 Cet exemple de code est illustré ci-dessous.  
  
 ![Élément Span appliqué à une plage de texte](../../../../docs/framework/wpf/advanced/media/flow-insertelementintotextprogrammatically.png "Flow_InsertElementIntoTextProgrammatically")  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des documents dynamiques](../../../../docs/framework/wpf/advanced/flow-document-overview.md)
