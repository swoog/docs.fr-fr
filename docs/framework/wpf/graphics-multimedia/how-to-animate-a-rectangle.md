---
title: 'Procédure : Animer un rectangle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], rectangles
- rectangles [WPF], animating
ms.assetid: 572ffb95-790d-4ace-adbf-b2ea8a90e75b
ms.openlocfilehash: dbff015bdc5f9ce56d2c366e0d348429efb7f4b5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305153"
---
# <a name="how-to-animate-a-rectangle"></a>Procédure : Animer un rectangle
Cet exemple montre comment animer les modifications apportées à la taille et à la position d’un rectangle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise une instance de la <xref:System.Windows.Media.Animation.RectAnimation> classe pour animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry>, qui anime les modifications apportées à la taille et la position du rectangle.  
  
 [!code-csharp[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/RectAnimationExample.cs#rectanimationwholepage)]
 [!code-vb[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/RectAnimationExample.vb#rectanimationwholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.Animation.RectAnimation>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.RectangleGeometry>
- [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Graphiques et multimédia](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [Rubriques de procédures de graphiques](graphics-how-to-topics.md)
- [L’animation et minutage des rubriques de procédures](animation-and-timing-how-to-topics.md)
