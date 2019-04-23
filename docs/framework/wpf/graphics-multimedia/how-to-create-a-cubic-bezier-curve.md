---
title: 'Procédure : Créer une courbe de Bézier cubique'
ms.date: 03/30/2017
helpviewer_keywords:
- curves [WPF], cubic Bezier
- Bezier curves [WPF], cubic
- graphics [WPF], cubic Bezier curves
- cubic Bezier curves [WPF]
ms.assetid: 450a3a77-7c57-48b0-a008-0f6051add980
ms.openlocfilehash: 36544abc774b7fe82c2ff47483cfedd6fb13e344
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115568"
---
# <a name="how-to-create-a-cubic-bezier-curve"></a><span data-ttu-id="d04a9-102">Procédure : Créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="d04a9-102">How to: Create a Cubic Bezier Curve</span></span>
<span data-ttu-id="d04a9-103">Cet exemple montre comment créer une courbe de Bézier cubique.</span><span class="sxs-lookup"><span data-stu-id="d04a9-103">This example shows how to create a cubic Bezier curve.</span></span> <span data-ttu-id="d04a9-104">Pour créer une courbe de Bézier cubique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.BezierSegment> classes.</span><span class="sxs-lookup"><span data-stu-id="d04a9-104">To create a cubic Bezier curve, use the <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, and <xref:System.Windows.Media.BezierSegment> classes.</span></span>  <span data-ttu-id="d04a9-105">Pour afficher la géométrie résultante, utilisez un <xref:System.Windows.Shapes.Path> élément, ou l’utiliser avec un <xref:System.Windows.Media.GeometryDrawing> ou un <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="d04a9-105">To display the resulting geometry, use a <xref:System.Windows.Shapes.Path> element, or use it with a <xref:System.Windows.Media.GeometryDrawing> or a <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="d04a9-106">Dans les exemples suivants, une courbe de Bézier cubique est tracée de (10, 100) à (300, 100).</span><span class="sxs-lookup"><span data-stu-id="d04a9-106">In the following examples, a cubic Bezier curve is drawn from (10, 100) to (300, 100).</span></span> <span data-ttu-id="d04a9-107">La courbe a des points de contrôle de (100, 0) et (200, 200).</span><span class="sxs-lookup"><span data-stu-id="d04a9-107">The curve has control points of (100, 0) and (200, 200).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d04a9-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="d04a9-108">Example</span></span>  
 <span data-ttu-id="d04a9-109">[xaml]</span><span class="sxs-lookup"><span data-stu-id="d04a9-109">[xaml]</span></span>  
  
 <span data-ttu-id="d04a9-110">Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe de balise abrégée pour décrire un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d04a9-110">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], you may use abbreviated markup syntax to describe a path.</span></span>  
  
 [!code-xaml[GeometrySample#53](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#53)]  
  
 <span data-ttu-id="d04a9-111">[xaml]</span><span class="sxs-lookup"><span data-stu-id="d04a9-111">[xaml]</span></span>  
  
 <span data-ttu-id="d04a9-112">Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner une courbe de Bézier cubique à l’aide de balises d’objet.</span><span class="sxs-lookup"><span data-stu-id="d04a9-112">In [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you can also draw a cubic Bezier curve using object tags.</span></span> <span data-ttu-id="d04a9-113">L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.</span><span class="sxs-lookup"><span data-stu-id="d04a9-113">The following is equivalent to the previous [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] example.</span></span>  
  
 [!code-xaml[GeometrySample#33](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#33)]  
  
 <span data-ttu-id="d04a9-114">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="d04a9-114">This example is part of larger sample; for the complete sample, see the [Geometries Sample](https://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d04a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d04a9-115">See also</span></span>

- [<span data-ttu-id="d04a9-116">Créer un arc elliptique</span><span class="sxs-lookup"><span data-stu-id="d04a9-116">Create an Elliptical Arc</span></span>](how-to-create-an-elliptical-arc.md)
- [<span data-ttu-id="d04a9-117">Créer un LineSegment dans une PathGeometry</span><span class="sxs-lookup"><span data-stu-id="d04a9-117">Create a LineSegment in a PathGeometry</span></span>](how-to-create-a-linesegment-in-a-pathgeometry.md)
- [<span data-ttu-id="d04a9-118">Créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="d04a9-118">Create a Cubic Bezier Curve</span></span>](how-to-create-a-cubic-bezier-curve.md)
- [<span data-ttu-id="d04a9-119">Créer une courbe de Bézier quadratique</span><span class="sxs-lookup"><span data-stu-id="d04a9-119">Create a Quadratic Bezier Curve</span></span>](how-to-create-a-quadratic-bezier-curve.md)
