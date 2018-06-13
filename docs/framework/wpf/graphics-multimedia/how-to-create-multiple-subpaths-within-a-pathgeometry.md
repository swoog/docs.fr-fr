---
title: 'Comment : créer plusieurs sous-chemins dans un PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- multiple subpaths [WPF]
- graphics [WPF], subpaths
- subpaths [WPF]
ms.assetid: 104a862c-dde2-4e62-ac87-80660dd1681c
ms.openlocfilehash: 5b129b1bacb5dc2cba87376e8df70e115a5ebd72
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559321"
---
# <a name="how-to-create-multiple-subpaths-within-a-pathgeometry"></a><span data-ttu-id="98d85-102">Comment : créer plusieurs sous-chemins dans un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="98d85-102">How to: Create Multiple Subpaths Within a PathGeometry</span></span>
<span data-ttu-id="98d85-103">Cet exemple montre comment créer plusieurs sous-chemins dans un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="98d85-103">This example shows how to create multiple subpaths in a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="98d85-104">Pour créer plusieurs sous-chemins, vous créez un <xref:System.Windows.Media.PathFigure> de chaque sous-tracé.</span><span class="sxs-lookup"><span data-stu-id="98d85-104">To create multiple subpaths, you create a <xref:System.Windows.Media.PathFigure> for each subpath.</span></span>  
  
## <a name="example"></a><span data-ttu-id="98d85-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="98d85-105">Example</span></span>  
 <span data-ttu-id="98d85-106">L’exemple suivant crée deux sous-chemins, chacun un triangle.</span><span class="sxs-lookup"><span data-stu-id="98d85-106">The following example creates two subpaths, each one a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#38](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#38)]  
  
 <span data-ttu-id="98d85-107">L’exemple suivant montre comment créer plusieurs sous-chemins à l’aide un <xref:System.Windows.Shapes.Path> et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] la syntaxe d’attribut.</span><span class="sxs-lookup"><span data-stu-id="98d85-107">The following example shows how to create multiple subpaths by using a <xref:System.Windows.Shapes.Path> and [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] attribute syntax.</span></span> <span data-ttu-id="98d85-108">Chaque `M` crée un sous-chemin de sorte que l’exemple crée deux sous-chemins qui dessinent chacun un triangle.</span><span class="sxs-lookup"><span data-stu-id="98d85-108">Each `M` creates a new subpath so that the example creates two subpaths that each draw a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#58](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#58)]  
  
 <span data-ttu-id="98d85-109">(Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="98d85-109">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="98d85-110">(Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md).)</span><span class="sxs-lookup"><span data-stu-id="98d85-110">For more information, see the [Path Markup Syntax](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) page.)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98d85-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98d85-111">See Also</span></span>  
 [<span data-ttu-id="98d85-112">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="98d85-112">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)
