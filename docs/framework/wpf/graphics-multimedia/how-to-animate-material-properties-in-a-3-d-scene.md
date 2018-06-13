---
title: 'Comment : animer des propriétés de matériel dans une scène 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- Material properties [WPF], animating in 3-D scenes
- animation [WPF], Material properties in 3-D scenes
- 3-D scenes [WPF], animating Material properties
ms.assetid: 229fd6eb-7401-4992-b0c9-8b28de230c0f
ms.openlocfilehash: ed4bbb3b22b09c24ed40b72a483db38b35038759
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559050"
---
# <a name="how-to-animate-material-properties-in-a-3-d-scene"></a>Comment : animer des propriétés de matériel dans une scène 3D
Cet exemple montre comment animer la <xref:System.Windows.Media.Brush.Opacity%2A> propriété de la <xref:System.Windows.Media.Media3D.Material> appliqué à un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modèle.  
  
 L’exemple de code suivant définit la <xref:System.Windows.Media.LinearGradientBrush> utilisé comme le <xref:System.Windows.Media.Media3D.Material> appliqué à l’objet 3D.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline1)]  
  
 Le <xref:System.Windows.Media.Brush.Opacity%2A> propriété de ce <xref:System.Windows.Media.LinearGradientBrush> s’anime à l’aide de l’exemple de code ci-dessous.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline2)]  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple complet.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi  
 [Créer une scène 3D](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [Vue d’ensemble des graphiques 3D](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
