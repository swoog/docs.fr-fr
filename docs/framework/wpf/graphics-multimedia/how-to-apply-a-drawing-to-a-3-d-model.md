---
title: 'Comment : appliquer un dessin à un modèle 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], applying to 3-D models
- 3-D models [WPF], applying drawings to
ms.assetid: 68357577-b7fc-446e-8be9-a8cc7df3a350
ms.openlocfilehash: 26a84d963cac3b5c23617bfaa23279021e29c07a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559062"
---
# <a name="how-to-apply-a-drawing-to-a-3-d-model"></a><span data-ttu-id="ed852-102">Comment : appliquer un dessin à un modèle 3D</span><span class="sxs-lookup"><span data-stu-id="ed852-102">How to: Apply a Drawing to a 3-D Model</span></span>
<span data-ttu-id="ed852-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.DrawingBrush> comme le <xref:System.Windows.Media.Media3D.Material> appliqué à un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modèle.</span><span class="sxs-lookup"><span data-stu-id="ed852-103">This example shows how to use a <xref:System.Windows.Media.DrawingBrush> as the <xref:System.Windows.Media.Media3D.Material> applied to a [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] model.</span></span>  
  
 <span data-ttu-id="ed852-104">Le code suivant définit un <xref:System.Windows.Media.DrawingGroup> comme contenu d’un <xref:System.Windows.Media.DrawingBrush>.</span><span class="sxs-lookup"><span data-stu-id="ed852-104">The following code defines a <xref:System.Windows.Media.DrawingGroup> as the content of a <xref:System.Windows.Media.DrawingBrush>.</span></span>  <span data-ttu-id="ed852-105">Le <xref:System.Windows.Media.DrawingBrush> est défini comme le <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> propriété de la <xref:System.Windows.Media.Media3D.DiffuseMaterial> appliqué à un [!INCLUDE[TLA2#tla_3d](../../../../includes/tla2sharptla-3d-md.md)] plan.</span><span class="sxs-lookup"><span data-stu-id="ed852-105">The <xref:System.Windows.Media.DrawingBrush> is set as the <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> property of the <xref:System.Windows.Media.Media3D.DiffuseMaterial> applied to a [!INCLUDE[TLA2#tla_3d](../../../../includes/tla2sharptla-3d-md.md)] plane.</span></span>  
  
 <span data-ttu-id="ed852-106">**Remarque :** il est souvent souhaitable de définir des valeurs telles que le dessin ci-dessous et les objets complexes en tant que ressources qui peuvent être réutilisées et de simplifieront votre code.</span><span class="sxs-lookup"><span data-stu-id="ed852-106">**Note:** It is often desirable to define complex objects and values like the drawing below as resources which can be reused and simplify your code.</span></span> <span data-ttu-id="ed852-107">Consultez [ressources XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ed852-107">See [XAML Resources](../../../../docs/framework/wpf/advanced/xaml-resources.md) for more information.</span></span>  
  
 [!code-xaml[3DGallery_snip#ApplyDrawingToMaterialInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialinline1)]  
  
## <a name="example"></a><span data-ttu-id="ed852-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ed852-108">Example</span></span>  
 <span data-ttu-id="ed852-109">Le code suivant montre l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="ed852-109">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[3DGallery_snip#ApplyDrawingToMaterialExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="ed852-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed852-110">See Also</span></span>  
 [<span data-ttu-id="ed852-111">Ressources XAML</span><span class="sxs-lookup"><span data-stu-id="ed852-111">XAML Resources</span></span>](../../../../docs/framework/wpf/advanced/xaml-resources.md)  
 [<span data-ttu-id="ed852-112">Créer une scène 3D</span><span class="sxs-lookup"><span data-stu-id="ed852-112">Create a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [<span data-ttu-id="ed852-113">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="ed852-113">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [<span data-ttu-id="ed852-114">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="ed852-114">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
