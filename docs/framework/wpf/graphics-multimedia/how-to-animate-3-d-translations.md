---
title: 'Procédure : Animer des translations 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3-D translations
- 3-D translations [WPF], animating
ms.assetid: d4eece1f-0cd2-4a2c-8370-293354c380e4
ms.openlocfilehash: 3e27c2d5f0cd44235a1d897b1b8f057808ae6bd8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168270"
---
# <a name="how-to-animate-3-d-translations"></a><span data-ttu-id="e0ee8-102">Procédure : Animer des translations 3D</span><span class="sxs-lookup"><span data-stu-id="e0ee8-102">How to: Animate 3-D Translations</span></span>
<span data-ttu-id="e0ee8-103">Cette rubrique montre comment animer une transformation de translation définie sur un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modèle.</span><span class="sxs-lookup"><span data-stu-id="e0ee8-103">This topic demonstrates how to animate a translation transformation set on a [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] model.</span></span>  
  
 <span data-ttu-id="e0ee8-104">Le code ci-dessous montre l’application d’un <xref:System.Windows.Media.Media3D.TranslateTransform3D> de l’objet à la <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> propriété d’un <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span><span class="sxs-lookup"><span data-stu-id="e0ee8-104">The code below shows the application of a <xref:System.Windows.Media.Media3D.TranslateTransform3D> object to the <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline1)]  
  
 <span data-ttu-id="e0ee8-105">Le <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> propriété de ce <xref:System.Windows.Media.Media3D.TranslateTransform3D> objet est animé en utilisant le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e0ee8-105">The <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> property of this <xref:System.Windows.Media.Media3D.TranslateTransform3D> object is animated using the code below.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline2)]  
  
## <a name="example"></a><span data-ttu-id="e0ee8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0ee8-106">Example</span></span>  
 <span data-ttu-id="e0ee8-107">Le code suivant montre l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="e0ee8-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e0ee8-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0ee8-108">See also</span></span>

- [<span data-ttu-id="e0ee8-109">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="e0ee8-109">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="e0ee8-110">Créer une scène 3D</span><span class="sxs-lookup"><span data-stu-id="e0ee8-110">Create a 3-D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="e0ee8-111">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="e0ee8-111">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="e0ee8-112">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="e0ee8-112">Transforms Overview</span></span>](transforms-overview.md)
