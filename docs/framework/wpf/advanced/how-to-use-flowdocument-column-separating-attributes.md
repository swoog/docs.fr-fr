---
title: 'Procédure : Utiliser les attributs de séparation de colonnes de FlowDocument'
ms.date: 03/30/2017
helpviewer_keywords:
- FlowDocument column-separating attributes
- column-separating attributes
- documents [WPF], FlowDocument column-separating attributes
ms.assetid: c7a822f8-aeca-45bd-a258-2852ff28005c
ms.openlocfilehash: 8693c8973442a5c6e65e64c5c66194c11bbff119
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57363781"
---
# <a name="how-to-use-flowdocument-column-separating-attributes"></a>Procédure : Utiliser les attributs de séparation de colonnes de FlowDocument
Cet exemple montre comment utiliser les fonctionnalités de séparation de colonnes d’un <xref:System.Windows.Documents.FlowDocument>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un <xref:System.Windows.Documents.FlowDocument>et définit le <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs.  Le <xref:System.Windows.Documents.FlowDocument> contient un paragraphe unique d’exemple de contenu.  
  
 [!code-xaml[FlowDocumentSnippets#_FlowDocumentColumnStuffXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml#_flowdocumentcolumnstuffxaml)]  
  
 La figure suivante montre les effets de la <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, et <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> attributs dans un rendu <xref:System.Windows.Documents.FlowDocument>.  
  
 ![Capture d’écran : FlowDocument Intra Column](./media/flowdocumentintracolumn.png "FlowDocumentIntraColumn")
