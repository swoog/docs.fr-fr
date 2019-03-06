---
title: Comment créer une grille complexe
description: Un exemple sur l’utilisation d’un contrôle de grille pour créer une disposition qui ressemble à un calendrier mensuel.
ms.date: 03/30/2017
helpviewer_keywords:
- calendar [WPF], creating
- monthly calendar [WPF], creating
- Grid control [WPF], creating [WPF], complex grid
ms.assetid: 4ce3040a-a156-4364-9596-98ca1eca5550
ms.openlocfilehash: dd17dfeea85e2b404f7a284f93faceec63145b1f
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355012"
---
# <a name="how-to-create-a-complex-grid"></a>Comment créer une grille complexe

Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Grid> contrôle pour créer une disposition qui ressemble à un calendrier mensuel.

## <a name="example"></a>Exemple

L’exemple suivant définit huit lignes et huit colonnes à l’aide de la <xref:System.Windows.Controls.RowDefinition> et <xref:System.Windows.Controls.ColumnDefinition> classes. Il utilise le <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> et <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> avec des propriétés, jointes <xref:System.Windows.Shapes.Rectangle> éléments qui remplissent les arrière-plans des différentes colonnes et lignes. Cette conception est possible car plusieurs éléments peuvent exister dans chaque cellule dans un <xref:System.Windows.Controls.Grid>, une différence de principe entre <xref:System.Windows.Controls.Grid> et <xref:System.Windows.Documents.Table>.

L’exemple utilise des dégradés verticaux pour <xref:System.Windows.Shapes.Shape.Fill%2A> les colonnes et les lignes afin d’améliorer la présentation visuelle et la lisibilité du calendrier. Un style <xref:System.Windows.Controls.TextBlock> les éléments représentent les dates et les jours de la semaine. <xref:System.Windows.Controls.TextBlock> éléments sont positionnés dans leurs cellules à l’aide de la <xref:System.Windows.FrameworkElement.Margin%2A> propriété et les propriétés d’alignement qui sont définies dans le style de l’application.

[!code-xaml[GridComplex#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridComplex/CS/default.xaml#1)]

L’illustration suivante montre le contrôle résultant, un calendrier personnalisable :

![Capture d’écran du contrôle résultant](././media/how-to-create-a-complex-grid/wpf-manual-calendar.png)

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Grid?displayProperty=nameWithType>
- <xref:System.Windows.Documents.TableCell?displayProperty=nameWithType>
- [Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
- [Vue d’ensemble de Panel](panels-overview.md)
- [Vue d’ensemble de Table](../advanced/table-overview.md)