---
title: 'Procédure : Définir les propriétés Height d’un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- height properties [WPF]
- Panel control [WPF], height properties of elements
ms.assetid: 5ab9e781-dbb8-469a-a3c8-cf38ce312647
ms.openlocfilehash: fb655630336c3b69afdc726a2e3c5a2cb8838667
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59221585"
---
# <a name="how-to-set-the-height-properties-of-an-element"></a>Procédure : Définir les propriétés Height d’un élément
## <a name="example"></a>Exemple  
 Cet exemple montre visuellement les différences de rendu de comportement entre les quatre propriétés associées à la hauteur dans [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].  
  
 Le <xref:System.Windows.FrameworkElement> classe expose quatre propriétés qui décrivent les caractéristiques de hauteur d’un élément. Ces quatre propriétés peuvent entrer en conflit, et quand ils le font, la valeur prioritaire est déterminée comme suit : le <xref:System.Windows.FrameworkElement.MinHeight%2A> valeur est prioritaire sur la <xref:System.Windows.FrameworkElement.MaxHeight%2A> valeur, qui à son tour est prioritaire sur la <xref:System.Windows.FrameworkElement.Height%2A> valeur. Une quatrième propriété <xref:System.Windows.FrameworkElement.ActualHeight%2A>, est en lecture seule et signale la hauteur réelle, telle que déterminée par les interactions avec le processus de disposition.  
  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples dessinent un <xref:System.Windows.Shapes.Rectangle> élément (`rect1`) en tant qu’enfant de <xref:System.Windows.Controls.Canvas>. Vous pouvez modifier les propriétés height d’un <xref:System.Windows.Shapes.Rectangle> à l’aide d’une série de <xref:System.Windows.Controls.ListBox> éléments qui représentent les valeurs de propriété <xref:System.Windows.FrameworkElement.MinHeight%2A>, <xref:System.Windows.FrameworkElement.MaxHeight%2A>, et <xref:System.Windows.FrameworkElement.Height%2A>. De cette manière, la priorité de chaque propriété est affichée visuellement.  
  
 [!code-xaml[HeightMinHeightMaxHeight#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#1)]  
[!code-xaml[HeightMinHeightMaxHeight#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#2)]  
  
 Les exemples de code-behind suivant gèrent les événements qui le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> déclenche des événements. Chaque gestionnaire extrait l’entrée de la <xref:System.Windows.Controls.ListBox>, analyse la valeur comme un <xref:System.Double>et applique la valeur à la propriété associées à la hauteur spécifiée. Les valeurs de hauteur sont également converties en une chaîne et écrites dans différents <xref:System.Windows.Controls.TextBlock> éléments (la définition de ces éléments n’est pas affichée dans le XAML sélectionné).  
  
 [!code-csharp[HeightMinHeightMaxHeight#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml.cs#3)]
 [!code-vb[HeightMinHeightMaxHeight#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HeightMinHeightMaxHeight/VisualBasic/Window1.xaml.vb#3)]  
  
 Pour obtenir un exemple complet, consultez [propriétés Height, exemple](https://go.microsoft.com/fwlink/?LinkID=159993).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.FrameworkElement>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement.ActualHeight%2A>
- <xref:System.Windows.FrameworkElement.MaxHeight%2A>
- <xref:System.Windows.FrameworkElement.MinHeight%2A>
- <xref:System.Windows.FrameworkElement.Height%2A>
- [Définir les propriétés Width d’un élément](how-to-set-the-width-properties-of-an-element.md)
- [Vue d'ensemble de Panel](panels-overview.md)
- [Exemple de propriétés de hauteur](https://go.microsoft.com/fwlink/?LinkID=159993)
