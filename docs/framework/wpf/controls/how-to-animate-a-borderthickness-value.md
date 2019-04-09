---
title: 'Procédure : Animer une valeur BorderThickness'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF], animating changes to
- animation [WPF], changes to border thickness
ms.assetid: fd021978-f74b-4e7b-a7f7-3987dcad9e0f
ms.openlocfilehash: 10e177d1f6d6add4638ce14af900e75d7e363890
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150733"
---
# <a name="how-to-animate-a-borderthickness-value"></a>Procédure : Animer une valeur BorderThickness
Cet exemple montre comment animer les modifications apportées à l’épaisseur d’une bordure à l’aide de la <xref:System.Windows.Media.Animation.ThicknessAnimation> classe.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant anime l’épaisseur d’une bordure à l’aide de <xref:System.Windows.Media.Animation.ThicknessAnimation>. L’exemple utilise le <xref:System.Windows.Controls.Border.BorderThickness%2A> propriété du <xref:System.Windows.Controls.Border>.  
  
 [!code-csharp[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/ThicknessAnimationExample.cs#thicknessanimationwholepage)]
 [!code-vb[BasicAnimations_snip#ThicknessAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/ThicknessAnimationExample.vb#thicknessanimationwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Galerie d’exemples d’Animation](https://go.microsoft.com/fwlink/?LinkID=159969).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.ThicknessAnimation>
- <xref:System.Windows.Controls.Border.BorderThickness%2A>
- <xref:System.Windows.Controls.Border>
- [Vue d'ensemble de l'animation](../graphics-multimedia/animation-overview.md)
- [Rubriques "Comment" relatives à l'animation et au minutage](../graphics-multimedia/animation-and-timing-how-to-topics.md)
- [Animer l’épaisseur d’une bordure à l’aide d’images clés](../graphics-multimedia/how-to-animate-the-thickness-of-a-border-by-using-key-frames.md)
