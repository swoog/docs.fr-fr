---
title: "Comment : ajuster l'espacement entre les paragraphes"
ms.date: 03/30/2017
helpviewer_keywords:
- spacing between paragraphs [WPF]
- paragraphs [WPF], spacing between
- documents [WPF], adjusting spacing between paragraphs
ms.assetid: 7cd2f2ac-0e19-4587-bfb6-7f5b18c9536e
ms.openlocfilehash: b232903054cf45b70ba99a9223352391498cf79b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-adjust-spacing-between-paragraphs"></a>Comment : ajuster l'espacement entre les paragraphes
Cet exemple montre comment ajuster ou éliminer l’espacement entre les paragraphes dans le contenu de flux.  
  
 Dans le contenu de flux, un espace supplémentaire qui apparaît entre les paragraphes est le résultat des marges définies pour ces paragraphes ; Par conséquent, l’espacement entre les paragraphes peut être contrôlé en ajustant les marges sur ces paragraphes.  Pour éliminer l’espacement supplémentaire entre deux paragraphes complètement, définissez les marges pour les paragraphes à **0**.  Pour obtenir un espacement uniforme entre les paragraphes dans l’ensemble de l’intégralité d’un <xref:System.Windows.Documents.FlowDocument>, utilisez les styles pour définir une valeur de marge uniforme pour tous les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.  
  
 Il est important de noter que les marges de deux paragraphes adjacents « réduira » au plus grand des deux marges, plutôt que se doubler. Par conséquent, si deux paragraphes adjacents ont des marges de 20 et 40 pixels respectivement, l’espace obtenu entre les paragraphes est 40 pixels, le plus grand de deux valeurs de marges.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise les styles pour définir la marge pour tous les <xref:System.Windows.Documents.Paragraph> éléments dans un <xref:System.Windows.Documents.FlowDocument> à **0**, ce qui élimine l’espacement supplémentaire entre les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.  
  
 [!code-xaml[BlockSnippets#_ParagraphSpacingXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BlockSnippets/CSharp/Window1.xaml#_paragraphspacingxaml)]
