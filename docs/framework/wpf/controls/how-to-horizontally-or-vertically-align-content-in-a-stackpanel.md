---
title: 'Procédure : Aligner horizontalement ou verticalement le contenu dans un StackPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- StackPanel control [WPF], content alignment [WPF]
- content alignment [WPF]
- aligning [WPF], content
ms.assetid: c1e8f962-72c8-4e7a-8670-7a2d7e021791
ms.openlocfilehash: 03348aa0eb5b6c1791c27683c1c6c6a5d4a8a9d4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186041"
---
# <a name="how-to-horizontally-or-vertically-align-content-in-a-stackpanel"></a>Procédure : Aligner horizontalement ou verticalement le contenu dans un StackPanel
Cet exemple montre comment ajuster la <xref:System.Windows.Controls.StackPanel.Orientation%2A> du contenu dans un <xref:System.Windows.Controls.StackPanel> élément et également comment ajuster la <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> et <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> du contenu enfant.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée trois <xref:System.Windows.Controls.ListBox> éléments dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]. Chaque <xref:System.Windows.Controls.ListBox> représente les valeurs possibles de la <xref:System.Windows.Controls.StackPanel.Orientation%2A>, <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A>, et <xref:System.Windows.FrameworkElement.VerticalAlignment%2A> propriétés d’un <xref:System.Windows.Controls.StackPanel>. Lorsqu’un utilisateur sélectionne une valeur dans un de la <xref:System.Windows.Controls.ListBox> éléments, la propriété associée de la <xref:System.Windows.Controls.StackPanel> et son enfant <xref:System.Windows.Controls.Button> éléments changent.  
  
 [!code-xaml[StackPanelIntroSamp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/StackPanelIntroSamp/CSharp/Window1.xaml#1)]  
  
 Le fichier code-behind suivant définit les modifications apportées aux événements qui sont associés les <xref:System.Windows.Controls.ListBox> sélection change. <xref:System.Windows.Controls.StackPanel> est identifié par le <xref:System.Windows.FrameworkElement.Name%2A> `sp1`.  
  
 [!code-csharp[StackPanelIntroSamp#2](~/samples/snippets/csharp/VS_Snippets_Wpf/StackPanelIntroSamp/CSharp/Window1.xaml.cs#2)]
 [!code-vb[StackPanelIntroSamp#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StackPanelIntroSamp/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A>
- <xref:System.Windows.FrameworkElement.VerticalAlignment%2A>
- [Vue d'ensemble de Panel](panels-overview.md)
