---
title: 'Procédure : Animer la position d’un objet à l’aide de PointAnimation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 1ef3f77e551affaa7e61d2aabf95f10c29275417
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651348"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a>Procédure : Animer la position d’un objet à l’aide de PointAnimation
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.PointAnimation> classe pour animer un objet sur un <xref:System.Windows.Shapes.Path>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déplace une ellipse le long d’un <xref:System.Windows.Shapes.Path> à partir d’un point sur l’écran à un autre. L’exemple anime la position d’un <xref:System.Windows.Media.EllipseGeometry> à l’aide de <xref:System.Windows.Media.Animation.PointAnimation> pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Graphiques et multimédia](index.md)
- [Rubriques de procédures de graphiques](graphics-how-to-topics.md)
- [L’animation et minutage des rubriques de procédures](animation-and-timing-how-to-topics.md)
