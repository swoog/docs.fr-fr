---
title: 'Procédure : Créer plusieurs sous-chemins dans un PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- multiple subpaths [WPF]
- graphics [WPF], subpaths
- subpaths [WPF]
ms.assetid: 104a862c-dde2-4e62-ac87-80660dd1681c
ms.openlocfilehash: 286075448cd6a343f8a7b15b2b5005f840f68e1d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59111746"
---
# <a name="how-to-create-multiple-subpaths-within-a-pathgeometry"></a><span data-ttu-id="01d7c-102">Procédure : Créer plusieurs sous-chemins dans un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="01d7c-102">How to: Create Multiple Subpaths Within a PathGeometry</span></span>
<span data-ttu-id="01d7c-103">Cet exemple montre comment créer plusieurs sous-chemins dans un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="01d7c-103">This example shows how to create multiple subpaths in a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="01d7c-104">Pour créer plusieurs sous-chemins, vous créez un <xref:System.Windows.Media.PathFigure> de chaque sous-tracé.</span><span class="sxs-lookup"><span data-stu-id="01d7c-104">To create multiple subpaths, you create a <xref:System.Windows.Media.PathFigure> for each subpath.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01d7c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="01d7c-105">Example</span></span>  
 <span data-ttu-id="01d7c-106">L’exemple suivant crée deux sous-chemins, chacun d’eux un triangle.</span><span class="sxs-lookup"><span data-stu-id="01d7c-106">The following example creates two subpaths, each one a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#38](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#38)]  
  
 <span data-ttu-id="01d7c-107">L’exemple suivant montre comment créer plusieurs sous-chemins à l’aide un <xref:System.Windows.Shapes.Path> et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] syntaxe d’attribut.</span><span class="sxs-lookup"><span data-stu-id="01d7c-107">The following example shows how to create multiple subpaths by using a <xref:System.Windows.Shapes.Path> and [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] attribute syntax.</span></span> <span data-ttu-id="01d7c-108">Chaque `M` crée un sous-chemin de sorte que l’exemple crée deux sous-chemins qui dessinent chacun un triangle.</span><span class="sxs-lookup"><span data-stu-id="01d7c-108">Each `M` creates a new subpath so that the example creates two subpaths that each draw a triangle.</span></span>  
  
 [!code-xaml[GeometrySample#58](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#58)]  
  
 <span data-ttu-id="01d7c-109">(Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="01d7c-109">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="01d7c-110">(Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)</span><span class="sxs-lookup"><span data-stu-id="01d7c-110">For more information, see the [Path Markup Syntax](path-markup-syntax.md) page.)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01d7c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d7c-111">See also</span></span>

- [<span data-ttu-id="01d7c-112">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="01d7c-112">Geometry Overview</span></span>](geometry-overview.md)
