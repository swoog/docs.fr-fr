---
title: 'Comment : créer une grille complexe'
ms.date: 03/30/2017
helpviewer_keywords:
- calendar [WPF], creating
- monthly calendar [WPF], creating
- Grid control [WPF], creating [WPF], complex grid
ms.assetid: 4ce3040a-a156-4364-9596-98ca1eca5550
ms.openlocfilehash: 49bf9781d56b93fd4529f3c9b62deb171e69155f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-create-a-complex-grid"></a>Comment : créer une grille complexe
Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Grid> pour créer une disposition qui ressemble à un calendrier mensuel.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit huit lignes et huit colonnes à l’aide de la <xref:System.Windows.Controls.RowDefinition> et <xref:System.Windows.Controls.ColumnDefinition> classes. Elle utilise le <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> et <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> propriétés jointes avec <xref:System.Windows.Shapes.Rectangle> éléments, qui remplissent les arrière-plans des différentes colonnes et lignes. Cette conception est possible car plusieurs éléments peuvent exister dans chaque cellule dans un <xref:System.Windows.Controls.Grid>, une différence de principe entre <xref:System.Windows.Controls.Grid> et <xref:System.Windows.Documents.Table>.  
  
 L’exemple utilise des dégradés verticaux pour <xref:System.Windows.Shapes.Shape.Fill%2A> les colonnes et les lignes afin d’améliorer la présentation visuelle et la lisibilité du calendrier. Style <xref:System.Windows.Controls.TextBlock> éléments représentent les dates et les jours de la semaine. <xref:System.Windows.Controls.TextBlock> éléments sont absolues dans leurs cellules à l’aide de la <xref:System.Windows.FrameworkElement.Margin%2A> propriété et les propriétés d’alignement sont définies dans le style de l’application.  
  
 [!code-xaml[GridComplex#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridComplex/CS/default.xaml#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.Grid>  
 <xref:System.Windows.Documents.TableCell>  
 [Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)  
 [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Vue d’ensemble de Table](../../../../docs/framework/wpf/advanced/table-overview.md)
