---
title: "Comment : définir les propriétés Width d'un élément"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- width properties [WPF]
- Panel control [WPF], width properties of elements
ms.assetid: 6ee04a9d-63f0-4f5b-a406-0a8cd4c35729
ms.openlocfilehash: 72617744a8b2565857d19a1c6ef41bf4211c89ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33554833"
---
# <a name="how-to-set-the-width-properties-of-an-element"></a>Comment : définir les propriétés Width d'un élément
## <a name="example"></a>Exemple  
 Cet exemple montre visuellement les différences de comportement entre les quatre propriétés associées à la largeur de rendu [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].  
  
 La <xref:System.Windows.FrameworkElement> classe expose quatre propriétés qui décrivent les caractéristiques de la largeur d’un élément. Ces quatre propriétés peuvent entrer en conflit, et dans ce cas, la valeur est prioritaire est déterminée comme suit : le <xref:System.Windows.FrameworkElement.MinWidth%2A> valeur est prioritaire sur la <xref:System.Windows.FrameworkElement.MaxWidth%2A> valeur, qui à son tour est prioritaire sur la <xref:System.Windows.FrameworkElement.Width%2A> valeur. Une quatrième propriété, <xref:System.Windows.FrameworkElement.ActualWidth%2A>, est en lecture seule et la largeur réelle déterminée par les interactions avec le processus de mise en page des rapports.  
  
 Les éléments suivants [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples dessinent un <xref:System.Windows.Shapes.Rectangle> élément (`rect1`) en tant qu’enfant de <xref:System.Windows.Controls.Canvas>. Vous pouvez modifier les propriétés de la largeur d’un <xref:System.Windows.Shapes.Rectangle> à l’aide d’une série de <xref:System.Windows.Controls.ListBox> éléments qui représentent les valeurs de propriété <xref:System.Windows.FrameworkElement.MinWidth%2A>, <xref:System.Windows.FrameworkElement.MaxWidth%2A>, et <xref:System.Windows.FrameworkElement.Width%2A>. De cette manière, la priorité de chaque propriété est affichée visuellement.  
  
 [!code-xaml[WidthMinWidthMaxWidth#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#1)]  
[!code-xaml[WidthMinWidthMaxWidth#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#2)]  
  
 Les exemples de code-behind suivants gèrent les événements qui le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> déclenche des événements. Chaque méthode personnalisée extrait l’entrée de la <xref:System.Windows.Controls.ListBox>, analyse la valeur en tant qu’un <xref:System.Double>et applique la valeur à la propriété associées à la largeur spécifiée. Les valeurs de largeur sont également converties en une chaîne et écrites dans différents <xref:System.Windows.Controls.TextBlock> éléments (définition de ces éléments n’est pas affichée dans le XAML sélectionné).  
  
 [!code-csharp[WidthMinWidthMaxWidth#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml.cs#3)]
 [!code-vb[WidthMinWidthMaxWidth#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WidthMinWidthMaxWidth/VisualBasic/Window1.xaml.vb#3)]  
  
 Pour obtenir un exemple complet, consultez [propriétés Width, exemple de comparaison](http://go.microsoft.com/fwlink/?LinkID=160050).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.ListBox>  
 <xref:System.Windows.FrameworkElement>  
 <xref:System.Windows.FrameworkElement.ActualWidth%2A>  
 <xref:System.Windows.FrameworkElement.MaxWidth%2A>  
 <xref:System.Windows.FrameworkElement.MinWidth%2A>  
 <xref:System.Windows.FrameworkElement.Width%2A>  
 [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Définir les propriétés Height d’un élément](../../../../docs/framework/wpf/controls/how-to-set-the-height-properties-of-an-element.md)  
 [Comparaison des propriétés Width, exemple](http://go.microsoft.com/fwlink/?LinkID=160050)
