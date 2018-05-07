---
title: 'Comment : mettre un élément en rotation'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: a37952af621c79d231b45a247c92d3576a533580
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-make-an-element-spin-in-place"></a>Comment : mettre un élément en rotation
Cet exemple montre comment mettre un élément en rotation à l’aide un <xref:System.Windows.Media.RotateTransform> et un <xref:System.Windows.Media.Animation.DoubleAnimation>.  
  
 L’exemple suivant applique la <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété de l’élément. L’exemple utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la <xref:System.Windows.Media.RotateTransform.Angle%2A> de la <xref:System.Windows.Media.RotateTransform>. Pour rendre l’élément à mettre en place, l’exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété de l’élément sur le point (0,5, 0,5).  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformanimations_snip#11](../../../../samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 Pour l’exemple complet, qui inclut plusieurs exemples de transformation, consultez [Transformations 2D, exemple](http://go.microsoft.com/fwlink/?LinkID=158252).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Vue d’ensemble des transformations](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
