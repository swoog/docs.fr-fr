---
title: 'Procédure : Animer les propriétés de matériel dans une scène 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- Material properties [WPF], animating in 3-D scenes
- animation [WPF], Material properties in 3-D scenes
- 3-D scenes [WPF], animating Material properties
ms.assetid: 229fd6eb-7401-4992-b0c9-8b28de230c0f
ms.openlocfilehash: 58e880a2828d21ee76f7fac6bdcf313e8454e65b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789322"
---
# <a name="how-to-animate-material-properties-in-a-3-d-scene"></a>Procédure : Animer les propriétés de matériel dans une scène 3D
Cet exemple montre comment animer la <xref:System.Windows.Media.Brush.Opacity%2A> propriété de la <xref:System.Windows.Media.Media3D.Material> appliqué à un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modèle.  
  
 L’exemple de code suivant définit la <xref:System.Windows.Media.LinearGradientBrush> utilisé en tant que le <xref:System.Windows.Media.Media3D.Material> appliqué à l’objet 3D.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline1)]  
  
 Le <xref:System.Windows.Media.Brush.Opacity%2A> propriété de ce <xref:System.Windows.Media.LinearGradientBrush> est animé à l’aide de l’exemple de code ci-dessous.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline2)]  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple complet.  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Créer une scène 3D](how-to-create-a-3-d-scene.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
