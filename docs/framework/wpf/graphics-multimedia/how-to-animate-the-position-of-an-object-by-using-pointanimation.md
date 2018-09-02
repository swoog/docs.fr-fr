---
title: "Comment : animer la position d'un objet à l'aide de PointAnimation"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 91447685988d91dfe86707c2cf265deabeb717b9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43465693"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a>Comment : animer la position d'un objet à l'aide de PointAnimation
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.PointAnimation> classe pour animer un objet sur un <xref:System.Windows.Shapes.Path>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déplace une ellipse le long d’un <xref:System.Windows.Shapes.Path> à partir d’un point sur l’écran à un autre. L’exemple anime la position d’un <xref:System.Windows.Media.EllipseGeometry> à l’aide de <xref:System.Windows.Media.Animation.PointAnimation> pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Animation.PointAnimation>  
 <xref:System.Windows.Shapes.Path>  
 <xref:System.Windows.Media.EllipseGeometry>  
 <xref:System.Windows.Media.EllipseGeometry.Center%2A>  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Graphiques et multimédia](../../../../docs/framework/wpf/graphics-multimedia/index.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/graphics-multimedia/graphics-how-to-topics.md)  
 [Animation et minutage](https://msdn.microsoft.com/library/7d83765b-d5ae-41b1-b423-80206e1124aa)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/graphics-multimedia/animation-and-timing-how-to-topics.md)
