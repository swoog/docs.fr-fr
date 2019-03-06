---
title: "Procédure : Simplifier des animations à l'aide de chronologies enfants"
ms.date: 03/30/2017
helpviewer_keywords:
- simplifying animations by child timelines [WPF]
- animation [WPF], simplifying by child timelines
- child timelines [WPF]
ms.assetid: 8335d770-d13d-42bd-8dfa-63f92c0327e2
ms.openlocfilehash: 933ba2dff86b99bddd8d8f75bafcd94833b2e066
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370356"
---
# <a name="how-to-simplify-animations-by-using-child-timelines"></a>Procédure : Simplifier des animations à l'aide de chronologies enfants
Cet exemple montre comment simplifier des animations à l’aide des enfants <xref:System.Windows.Media.Animation.ParallelTimeline> objets. Un <xref:System.Windows.Media.Animation.Storyboard> est un type de <xref:System.Windows.Media.Animation.Timeline> qui fournit des informations de ciblage pour les chronologies qu’il contient. Utilisez un <xref:System.Windows.Media.Animation.Storyboard> pour fournir plus d’informations, y compris les informations d’objet et la propriété le ciblage de chronologie.  
  
 Pour commencer une animation, utilisez une ou plusieurs <xref:System.Windows.Media.Animation.ParallelTimeline> objets en tant qu’éléments enfants imbriqués d’un <xref:System.Windows.Media.Animation.Storyboard>. Ces <xref:System.Windows.Media.Animation.ParallelTimeline> objets peuvent contenir d’autres animations et par conséquent, mieux encapsuler les séquences temporelles dans des animations complexes. Par exemple, si vous animez une <xref:System.Windows.Controls.TextBlock> et plusieurs formes dans le même <xref:System.Windows.Media.Animation.Storyboard>, vous pouvez séparer les animations pour le <xref:System.Windows.Controls.TextBlock> et les formes, en les mettant chacune dans un distinct <xref:System.Windows.Media.Animation.ParallelTimeline>. Étant donné que chaque <xref:System.Windows.Media.Animation.ParallelTimeline> possède son propre <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A> et tous les éléments enfants de la <xref:System.Windows.Media.Animation.ParallelTimeline> commencent par rapport à ce <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A>, temporelle est mieux encapsulée.  
  
 L’exemple suivant anime deux parties de texte (<xref:System.Windows.Controls.TextBlock> objets) à partir d’au sein du même <xref:System.Windows.Media.Animation.Storyboard>. Un <xref:System.Windows.Media.Animation.ParallelTimeline> encapsule les animations de l’un de le <xref:System.Windows.Controls.TextBlock> objets.  
  
 **Remarque relative aux performances :** Bien que vous pouvez imbriquer <xref:System.Windows.Media.Animation.Storyboard> chronologies dans les autres, <xref:System.Windows.Media.Animation.ParallelTimeline>s sont plus adaptés pour l’imbrication, car elles nécessitent moins de surcharge. (Le <xref:System.Windows.Media.Animation.Storyboard> classe hérite de la <xref:System.Windows.Media.Animation.ParallelTimeline> classe.)  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Timelines_snip#ParallelTimelineWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Timelines_snip/CS/ParallelTimelineExample.xaml#paralleltimelinewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Spécifier HandoffBehavior entre des animations de storyboard](how-to-specify-handoffbehavior-between-storyboard-animations.md)
