---
title: "Procédure : Ajouter une valeur de sortie d'animation à une valeur de départ d'animation"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF]
ms.assetid: b89a82be-b03d-481e-a8d3-cc513d09ca00
ms.openlocfilehash: f27a214d4fa6fd33d993e7ae458ebb736b60bed7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351955"
---
# <a name="how-to-add-an-animation-output-value-to-an-animation-starting-value"></a>Procédure : Ajouter une valeur de sortie d'animation à une valeur de départ d'animation
Cet exemple montre comment ajouter une valeur de sortie d’animation à une valeur de départ d’animation.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> propriété spécifie si vous souhaitez que la valeur de sortie d’une animation ajoutée à la valeur de départ (valeur de base) d’une propriété animée. Vous pouvez utiliser le <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> propriété avec des animations plus simples et la plupart des animations d’image clé. Pour plus d’informations, consultez [vue d’ensemble de l’Animation](animation-overview.md) et [vue d’ensemble des Animations image clé](key-frame-animations-overview.md).  
  
 L’exemple suivant montre l’effet de l’utilisation de la <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A?displayProperty=nameWithType> propriété avec <xref:System.Windows.Media.Animation.DoubleAnimation> et à l’aide de la <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsAdditive%2A?displayProperty=nameWithType> propriété avec <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>.  
  
 [!code-xaml[timingbehaviors_snip#IsAdditiveWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsAdditiveExample.xaml#isadditivewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Accumuler des valeurs d'animation pendant des cycles de répétition](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [L’animation et minutage des rubriques de procédures](animation-and-timing-how-to-topics.md)
