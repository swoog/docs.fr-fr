---
title: 'Procédure : Créer un StackPanel'
ms.date: 03/30/2017
helpviewer_keywords:
- StackPanel control [WPF], creating
ms.assetid: e7ce65cb-720a-4bb6-95b6-286b74488a58
ms.openlocfilehash: 20e2b21b10129c096398606501768a7ace0617fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674230"
---
# <a name="how-to-create-a-stackpanel"></a>Procédure : Créer un StackPanel
Cet exemple montre comment créer un <xref:System.Windows.Controls.StackPanel>.  
  
## <a name="example"></a>Exemple  
 Un <xref:System.Windows.Controls.StackPanel> vous permet d’empiler des éléments dans une direction spécifiée. À l’aide des propriétés qui sont définies sur <xref:System.Windows.Controls.StackPanel>, contenu peut circuler verticalement, qui est le paramètre par défaut, ou horizontalement.  
  
 L’exemple suivant empile verticalement cinq <xref:System.Windows.Controls.TextBlock> des contrôles, chacun avec un autre <xref:System.Windows.Controls.Border> et <xref:System.Windows.Controls.Border.Background%2A>, à l’aide de <xref:System.Windows.Controls.StackPanel>. Les éléments enfants qui n’ont pas spécifié <xref:System.Windows.FrameworkElement.Width%2A> s’étire pour remplir la fenêtre parente ; Toutefois, les éléments enfants qui ont une certaine <xref:System.Windows.FrameworkElement.Width%2A>, sont centrés dans la fenêtre.  
  
 La direction de la pile par défaut dans un <xref:System.Windows.Controls.StackPanel> est vertical. Pour contrôler le flux contenu dans un <xref:System.Windows.Controls.StackPanel>, utilisez le <xref:System.Windows.Controls.StackPanel.Orientation%2A> propriété. Vous pouvez contrôler l’alignement horizontal en utilisant la <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> propriété.  
  
```xaml  
<Page xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" WindowTitle="StackPanel Sample">  
  <StackPanel>  
    <Border Background="SkyBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="12">Stacked Item #1</TextBlock>  
    </Border>  
    <Border Width="400" Background="CadetBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="14">Stacked Item #2</TextBlock>  
    </Border>  
    <Border Background="LightGoldenRodYellow" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="16">Stacked Item #3</TextBlock>  
    </Border>  
    <Border Width="200" Background="PaleGreen" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="18">Stacked Item #4</TextBlock>  
    </Border>  
    <Border Background="White" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="20">Stacked Item #5</TextBlock>  
    </Border>  
  </StackPanel>  
</Page>  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.StackPanel>
- [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
- [Rubriques de guide pratique](../../../../docs/framework/wpf/controls/stackpanel-how-to-topics.md)
