---
title: "Procédure : Animer la position et la direction d'une caméra à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera direction with key frames
- key frames [WPF], animating camera direction
- animation [WPF], camera position with key frames
- camera position [WPF], animating with key frames
- key frames [WPF], animating camera position
- camera direction [WPF], animating with key frames
ms.assetid: 5753024e-0057-454d-947f-43ea686879c7
ms.openlocfilehash: 5df3a201eaae4ddcf2e5d5aac3de6e0d5013947c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57353398"
---
# <a name="how-to-animate-camera-position-and-direction-using-key-frames"></a>Procédure : Animer la position et la direction d'une caméra à l'aide d'images clés
Dans l’exemple suivant, <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> est utilisé pour animer la position d’un <xref:System.Windows.Media.Media3D.PerspectiveCamera> dans une scène 3D. En outre, <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> est utilisé pour animer la direction pointe la caméra dans la scène 3D. Ces deux animations utilisent plusieurs images clés qui créent une série d’effets d’animation :  
  
1.  <xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> et <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> sont utilisées pour créer une interpolation linéaire fluide entre les valeurs.  
  
2.  <xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> et <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> sont utilisées pour créer des « sauts » soudains entre les valeurs (aucune interpolation).  
  
3.  <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> et <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> sont utilisées pour créer une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> propriété. Dans l’exemple ci-dessous, l’animation commence lentement vers la fin du segment temporel, accélère de façon exponentielle.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationUsingKeyFramesExample.xaml#pointvector3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Animer la position et la direction de la caméra d’une scène 3D](how-to-animate-camera-position-and-direction-in-a-3d-scene.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
