---
title: 'Procédure : Animer une Rotation 3D à l’aide d’images clés'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3-D translations [WPF], with key frames (Rotation3DAnimation)
- key frames [WPF], Rotation3DAnimation
- 3-D translations [WPF], animating [WPF], with key frames (Rotation3DAnimation)
ms.assetid: 6f671b95-7f30-4836-9a4f-aeb7dc30121f
ms.openlocfilehash: 90e982838cb5d5b4488185c041e946c15d1e61e8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57369134"
---
# <a name="how-to-animate-a-3-d-rotation-using-key-frames"></a>Procédure : Animer une Rotation 3D à l’aide d’images clés
Dans l’exemple suivant, <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> est utilisé pour faire pivoter un objet 3D pendant son axe de rotation s’anime en créant une « déviation ». Cette animation utilise les images clés suivantes :  
  
1.  <xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> permet de créer une interpolation linéaire fluide entre les valeurs.  
  
2.  <xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> permet de créer des « sauts » soudains entre les valeurs (aucune interpolation).  
  
3.  <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> permet de créer une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> propriété. Dans l’exemple ci-dessous, cette partie de l’animation commence lentement vers la fin du segment temporel, accélère de façon exponentielle.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Animation3DGallery_snip#Rotation3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotation3DAnimationUsingKeyFramesExample.xaml#rotation3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Animer une rotation 3D à l’aide de storyboards](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Animer une rotation 3D à l’aide de Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [Animer une rotation 3D à l'aide de quaternions](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [Animer une rotation 3D à l’aide d’images clés (QuaternionAnimationUsingKeyFrames)](animate-a-3-d-rotation-quaternionanimationusingkeyframes.md)
