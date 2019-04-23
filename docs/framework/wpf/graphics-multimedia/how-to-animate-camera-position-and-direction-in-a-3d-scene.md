---
title: 'Procédure : Animer la position et la direction de la caméra d’une scène 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera position in 3-D scenes
- camera direction [WPF], animating in 3-D scenes
- 3-D scenes [WPF], animating camera position
- 3-D scenes [WPF], animating camera direction
- camera position [WPF], animating in 3-D scenes
- animation [WPF], camera direction in 3-D scenes
ms.assetid: 480224b7-a5e5-4165-ba7f-ef760ddff94a
ms.openlocfilehash: b64263a495ffe845a76317aad8f5b4a14e11b31e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59146001"
---
# <a name="how-to-animate-camera-position-and-direction-in-a-3d-scene"></a>Procédure : Animer la position et la direction de la caméra d’une scène 3D
L’exemple suivant montre comment animer la position d’une caméra et animer la direction qu’il pointe dans une scène 3D. Pour cela, à l’aide de <xref:System.Windows.Media.Animation.Point3DAnimation> et <xref:System.Windows.Media.Animation.Vector3DAnimation> pour animer la <xref:System.Windows.Media.Media3D.ProjectionCamera.Position%2A> et <xref:System.Windows.Media.Media3D.ProjectionCamera.LookDirection%2A> propriétés respectivement de la <xref:System.Windows.Media.Media3D.PerspectiveCamera>. Vous pouvez utiliser une animation comme suit pour modifier l’affichage du spectateur d’une scène en réponse à un événement.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationExample.xaml#pointvector3danimationexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.Vector3DAnimation>
- <xref:System.Windows.Media.Animation.Point3DAnimation>
- [Animer la position et la direction de la caméra à l’aide d’images clés](how-to-animate-camera-position-and-direction-using-key-frames.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
