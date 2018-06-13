---
title: 'Comment : créer une courbe de Bézier cubique'
ms.date: 03/30/2017
helpviewer_keywords:
- curves [WPF], cubic Bezier
- Bezier curves [WPF], cubic
- graphics [WPF], cubic Bezier curves
- cubic Bezier curves [WPF]
ms.assetid: 450a3a77-7c57-48b0-a008-0f6051add980
ms.openlocfilehash: 6332129179e1934e5a37c7a1a40ef5f46ab669a9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33560102"
---
# <a name="how-to-create-a-cubic-bezier-curve"></a><span data-ttu-id="1f981-102">Comment : créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="1f981-102">How to: Create a Cubic Bezier Curve</span></span>
<span data-ttu-id="1f981-103">Cet exemple montre comment créer une courbe de Bézier cubique.</span><span class="sxs-lookup"><span data-stu-id="1f981-103">This example shows how to create a cubic Bezier curve.</span></span> <span data-ttu-id="1f981-104">Pour créer une courbe de Bézier cubique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.BezierSegment> classes.</span><span class="sxs-lookup"><span data-stu-id="1f981-104">To create a cubic Bezier curve, use the <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, and <xref:System.Windows.Media.BezierSegment> classes.</span></span>  <span data-ttu-id="1f981-105">Pour afficher la géométrie résultante, utilisez un <xref:System.Windows.Shapes.Path> élément, ou l’utiliser avec un <xref:System.Windows.Media.GeometryDrawing> ou <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="1f981-105">To display the resulting geometry, use a <xref:System.Windows.Shapes.Path> element, or use it with a <xref:System.Windows.Media.GeometryDrawing> or a <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="1f981-106">Dans les exemples suivants, une courbe de Bézier cubique est tracée de (10, 100) à (300, 100).</span><span class="sxs-lookup"><span data-stu-id="1f981-106">In the following examples, a cubic Bezier curve is drawn from (10, 100) to (300, 100).</span></span> <span data-ttu-id="1f981-107">La courbe a des points de contrôle de (100, 0) et (200, 200).</span><span class="sxs-lookup"><span data-stu-id="1f981-107">The curve has control points of (100, 0) and (200, 200).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1f981-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="1f981-108">Example</span></span>  
 <span data-ttu-id="1f981-109">[xaml]</span><span class="sxs-lookup"><span data-stu-id="1f981-109">[xaml]</span></span>  
  
 <span data-ttu-id="1f981-110">Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe de balise abrégée pour décrire un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="1f981-110">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], you may use abbreviated markup syntax to describe a path.</span></span>  
  
 [!code-xaml[GeometrySample#53](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#53)]  
  
 <span data-ttu-id="1f981-111">[xaml]</span><span class="sxs-lookup"><span data-stu-id="1f981-111">[xaml]</span></span>  
  
 <span data-ttu-id="1f981-112">Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner une courbe de Bézier cubique à l’aide de balises d’objet.</span><span class="sxs-lookup"><span data-stu-id="1f981-112">In [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you can also draw a cubic Bezier curve using object tags.</span></span> <span data-ttu-id="1f981-113">L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.</span><span class="sxs-lookup"><span data-stu-id="1f981-113">The following is equivalent to the previous [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] example.</span></span>  
  
 [!code-xaml[GeometrySample#33](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#33)]  
  
 <span data-ttu-id="1f981-114">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](http://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="1f981-114">This example is part of larger sample; for the complete sample, see the [Geometries Sample](http://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f981-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f981-115">See Also</span></span>  
 [<span data-ttu-id="1f981-116">Créer un arc elliptique</span><span class="sxs-lookup"><span data-stu-id="1f981-116">Create an Elliptical Arc</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-an-elliptical-arc.md)  
 [<span data-ttu-id="1f981-117">Créer un LineSegment dans une PathGeometry</span><span class="sxs-lookup"><span data-stu-id="1f981-117">Create a LineSegment in a PathGeometry</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-linesegment-in-a-pathgeometry.md)  
 [<span data-ttu-id="1f981-118">Créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="1f981-118">Create a Cubic Bezier Curve</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-cubic-bezier-curve.md)  
 [<span data-ttu-id="1f981-119">Créer une courbe de Bézier quadratique</span><span class="sxs-lookup"><span data-stu-id="1f981-119">Create a Quadratic Bezier Curve</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-quadratic-bezier-curve.md)
