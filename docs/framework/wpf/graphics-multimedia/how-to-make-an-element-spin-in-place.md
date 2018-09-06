---
title: 'Comment : mettre un élément en rotation'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: 56385d7c31465e25f19486ea5cdaa8876cdb30ff
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43784443"
---
# <a name="how-to-make-an-element-spin-in-place"></a>Comment : mettre un élément en rotation
Cet exemple montre comment mettre un élément en rotation à l’aide un <xref:System.Windows.Media.RotateTransform> et un <xref:System.Windows.Media.Animation.DoubleAnimation>.  
  
 L’exemple suivant applique le <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété de l’élément. L’exemple utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la <xref:System.Windows.Media.RotateTransform.Angle%2A> de la <xref:System.Windows.Media.RotateTransform>. Pour mettre l’élément en rotation, l’exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété de l’élément vers le point (0,5, 0,5).  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformanimations_snip#11](../../../../samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 Pour l’exemple complet, qui inclut plusieurs exemples de transformation, consultez [Transformations 2D, exemple](https://go.microsoft.com/fwlink/?LinkID=158252).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Vue d’ensemble des transformations](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
