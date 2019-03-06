---
title: 'Procédure : Mettre un élément en rotation'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: 2eaca5ba75eb8ac2eeb375a177c08659a65af2db
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371500"
---
# <a name="how-to-make-an-element-spin-in-place"></a>Procédure : Mettre un élément en rotation
Cet exemple montre comment mettre un élément en rotation à l’aide un <xref:System.Windows.Media.RotateTransform> et un <xref:System.Windows.Media.Animation.DoubleAnimation>.  
  
 L’exemple suivant applique le <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété de l’élément. L’exemple utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la <xref:System.Windows.Media.RotateTransform.Angle%2A> de la <xref:System.Windows.Media.RotateTransform>. Pour mettre l’élément en rotation, l’exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété de l’élément vers le point (0,5, 0,5).  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformanimations_snip#11](~/samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 Pour l’exemple complet, qui inclut plusieurs exemples de transformation, consultez [Transformations 2D, exemple](https://go.microsoft.com/fwlink/?LinkID=158252).  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d’ensemble des transformations](transforms-overview.md)
