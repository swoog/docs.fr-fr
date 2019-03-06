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
# <a name="how-to-animate-camera-position-and-direction-using-key-frames"></a><span data-ttu-id="0fb70-102">Procédure : Animer la position et la direction d'une caméra à l'aide d'images clés</span><span class="sxs-lookup"><span data-stu-id="0fb70-102">How to: Animate Camera Position and Direction Using Key Frames</span></span>
<span data-ttu-id="0fb70-103">Dans l’exemple suivant, <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> est utilisé pour animer la position d’un <xref:System.Windows.Media.Media3D.PerspectiveCamera> dans une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="0fb70-103">In the following example, <xref:System.Windows.Media.Animation.Point3DAnimationUsingKeyFrames> is used to animate the position of a <xref:System.Windows.Media.Media3D.PerspectiveCamera> in a 3D scene.</span></span> <span data-ttu-id="0fb70-104">En outre, <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> est utilisé pour animer la direction pointe la caméra dans la scène 3D.</span><span class="sxs-lookup"><span data-stu-id="0fb70-104">In addition, <xref:System.Windows.Media.Animation.Vector3DAnimationUsingKeyFrames> is used to animate the direction the camera is pointing in the 3D scene.</span></span> <span data-ttu-id="0fb70-105">Ces deux animations utilisent plusieurs images clés qui créent une série d’effets d’animation :</span><span class="sxs-lookup"><span data-stu-id="0fb70-105">Both of these animations use several key frames which create a series of animation effects:</span></span>  
  
1.  <span data-ttu-id="0fb70-106"><xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> et <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> sont utilisées pour créer une interpolation linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0fb70-106"><xref:System.Windows.Media.Animation.LinearPoint3DKeyFrame> and <xref:System.Windows.Media.Animation.LinearVector3DKeyFrame> are used to create a smooth, linear interpolation between values.</span></span>  
  
2.  <span data-ttu-id="0fb70-107"><xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> et <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> sont utilisées pour créer des « sauts » soudains entre les valeurs (aucune interpolation).</span><span class="sxs-lookup"><span data-stu-id="0fb70-107"><xref:System.Windows.Media.Animation.DiscretePoint3DKeyFrame> and <xref:System.Windows.Media.Animation.DiscreteVector3DKeyFrame> are used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3.  <span data-ttu-id="0fb70-108"><xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> et <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> sont utilisées pour créer une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="0fb70-108"><xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame> and <xref:System.Windows.Media.Animation.SplineVector3DKeyFrame> are used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplinePoint3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="0fb70-109">Dans l’exemple ci-dessous, l’animation commence lentement vers la fin du segment temporel, accélère de façon exponentielle.</span><span class="sxs-lookup"><span data-stu-id="0fb70-109">In the example below, the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0fb70-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="0fb70-110">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationUsingKeyFramesExample.xaml#pointvector3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="0fb70-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fb70-111">See also</span></span>
- [<span data-ttu-id="0fb70-112">Animer la position et la direction de la caméra d’une scène 3D</span><span class="sxs-lookup"><span data-stu-id="0fb70-112">Animate Camera Position and Direction in a 3D Scene</span></span>](how-to-animate-camera-position-and-direction-in-a-3d-scene.md)
- [<span data-ttu-id="0fb70-113">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="0fb70-113">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
