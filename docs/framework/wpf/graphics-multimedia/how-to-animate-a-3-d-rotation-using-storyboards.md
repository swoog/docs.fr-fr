---
title: "Procédure : Animer une rotation 3D à l'aide de storyboards"
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF]
- 3-D translations [WPF], animating [WPF], with Storyboards
- animation [WPF], 3-D translations [WPF], with Storyboards
ms.assetid: 1020e44e-e21e-49a8-be53-53cbc1910e83
ms.openlocfilehash: 20f5bf565ded624e4ea7e1e615f09b4c698526bd
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357220"
---
# <a name="how-to-animate-a-3-d-rotation-using-storyboards"></a>Procédure : Animer une rotation 3D à l'aide de storyboards
L’exemple suivant montre comment faire pivoter un objet 3D pendant qu’il « tremblement » en animant la <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> et <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> propriétés d’un <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> objet. Cela <xref:System.Windows.Media.Media3D.AxisAngleRotation3D> objet spécifie la transformation de rotation de l’objet 3D et en animant ainsi ses propriétés, crée l’effet de rotation souhaité. Dans la table de montage séquentiel, <xref:System.Windows.Media.Animation.DoubleAnimation> est utilisé pour animer la <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Angle%2A> propriété lors de la <xref:System.Windows.Media.Animation.Vector3DAnimation> est utilisé pour animer la <xref:System.Windows.Media.Media3D.AxisAngleRotation3D.Axis%2A> propriété.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Animation3DGallery_snip#Rotate3DUsingAxisAngleRotation3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotat3DUsingAxisAngleRotation3DExample.xaml#rotate3dusingaxisanglerotation3dexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Animer une rotation 3D à l’aide de Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [Animer une rotation 3D à l’aide d’images clés (Rotation3DAnimationUsingKeyFrames)](how-to-animate-a-3-d-rotation-using-key-frames.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
- [Vue d'ensemble des plans conceptuels](storyboards-overview.md)
