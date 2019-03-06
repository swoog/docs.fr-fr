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
# <a name="how-to-adjust-spacing-between-paragraphs"></a>Procédure : Ajuster l'espacement entre les paragraphes
Cet exemple montre comment ajuster ou éliminer l’espacement entre les paragraphes dans le contenu dynamique.  
  
 Dans le contenu dynamique, un espace supplémentaire qui apparaît entre les paragraphes est le résultat des marges définies pour ces paragraphes ; Par conséquent, l’espacement entre les paragraphes peut être contrôlé en ajustant les marges sur ces paragraphes.  Pour éliminer complètement l’espacement supplémentaire entre deux paragraphes, définissez les marges pour les paragraphes à **0**.  Pour obtenir un espacement uniforme entre les paragraphes tout au long de l’intégralité d’un <xref:System.Windows.Documents.FlowDocument>, utilisez les styles pour définir une valeur de marge uniforme pour tous les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.  
  
 Il est important de noter que les marges de deux paragraphes adjacents sont « réduits » à la plus grande des deux marges, plutôt que se doubler. Par conséquent, si deux paragraphes adjacents ont des marges de 20 et 40 pixels respectivement, l’espace entre les paragraphes résultant est 40 pixels, la plus grande des deux valeurs de marges.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise des styles pour définir la marge pour tous les <xref:System.Windows.Documents.Paragraph> éléments dans un <xref:System.Windows.Documents.FlowDocument> à **0**, ce qui élimine l’espacement supplémentaire entre les paragraphes dans le <xref:System.Windows.Documents.FlowDocument>.  
  
 [!code-xaml[BlockSnippets#_ParagraphSpacingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/BlockSnippets/CSharp/Window1.xaml#_paragraphspacingxaml)]
