---
title: 'Procédure : Animer la position ou la couleur d’un point de dégradé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- position [WPF], animating
- animation [WPF], position of GradientStop objects
- GradientStop objects [WPF], animating color of
- colors [WPF], animating
- animation [WPF], color of GradientStop objects
- GradientStop objects [WPF], animating position of
ms.assetid: 6f5b8b47-6c32-4b8e-98ee-fdf6515ec843
ms.openlocfilehash: eeaea4732855155bf711912644f2f5b3f5a4f8d0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134808"
---
# <a name="how-to-animate-the-position-or-color-of-a-gradient-stop"></a>Procédure : Animer la position ou la couleur d’un point de dégradé
Cet exemple montre comment animer la <xref:System.Windows.Media.GradientStop.Color%2A> et <xref:System.Windows.Media.GradientStop.Offset%2A> de <xref:System.Windows.Media.GradientStop> objets.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant anime trois points de dégradé à l’intérieur d’un <xref:System.Windows.Media.LinearGradientBrush>. L’exemple utilise trois animations, chacun d’eux s’anime un dégradé différent :  
  
-   La première animation, un <xref:System.Windows.Media.Animation.DoubleAnimation>, anime le premier point de dégradé <xref:System.Windows.Media.GradientStop.Offset%2A> entre 0,0 et 1,0, puis revient à 0.0. Par conséquent, la première couleur du dégradé se décale de la gauche vers le côté droit du rectangle et puis de nouveau vers le côté gauche.  
  
-   La deuxième animation, un <xref:System.Windows.Media.Animation.ColorAnimation>, anime le deuxième point de dégradé <xref:System.Windows.Media.GradientStop.Color%2A> de <xref:System.Windows.Media.Colors.Purple%2A> à <xref:System.Windows.Media.Colors.Yellow%2A> , puis revient à <xref:System.Windows.Media.Colors.Purple%2A>. Par conséquent, la couleur intermédiaire du dégradé de la passe de violet jaune et en violet.  
  
-   La troisième animation, un autre <xref:System.Windows.Media.Animation.ColorAnimation>, anime l’opacité de la troisième point de dégradé <xref:System.Windows.Media.GradientStop.Color%2A> par -1, puis de nouveau. Par conséquent, la troisième couleur dans le dégradé disparaît et devient alors opaque à nouveau.  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/GradientStopAnimationExample.cs#graphicsmmgradientanimationexampleswholepage)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/gradientstopanimationexample.vb#graphicsmmgradientanimationexampleswholepage)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/GradientStopAnimationExample.xaml#graphicsmmgradientanimationexampleswholepage)]  
  
 Bien que cet exemple utilise un <xref:System.Windows.Media.LinearGradientBrush>, le processus est le même pour animer <xref:System.Windows.Media.GradientStop> d’objets contenus dans un <xref:System.Windows.Media.RadialGradientBrush>.  
  
 Pour obtenir des exemples supplémentaires, consultez le [pinceaux, exemple](https://go.microsoft.com/fwlink/?LinkID=159973).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.GradientStop>
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des plans conceptuels](storyboards-overview.md)
