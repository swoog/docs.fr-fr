---
title: "Comment : créer une forme à l'aide d'un PathGeometry"
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], creating with PathGeometry class
- graphics [WPF], shapes
ms.assetid: 49a4a8b7-e738-45be-8dac-b54a6d8f5b21
ms.openlocfilehash: 6c77844b054dd89a0c3f3cbecd0725968df9ae71
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33560180"
---
# <a name="how-to-create-a-shape-by-using-a-pathgeometry"></a><span data-ttu-id="0bcb9-102">Comment : créer une forme à l'aide d'un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="0bcb9-102">How to: Create a Shape by Using a PathGeometry</span></span>
<span data-ttu-id="0bcb9-103">Cet exemple montre comment créer une forme à l’aide de la <xref:System.Windows.Media.PathGeometry> classe.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-103">This example shows how to create a shape using the <xref:System.Windows.Media.PathGeometry> class.</span></span> <span data-ttu-id="0bcb9-104"><xref:System.Windows.Media.PathGeometry> les objets sont composés d’un ou plusieurs <xref:System.Windows.Media.PathFigure> objets ; chaque <xref:System.Windows.Media.PathFigure> représente une forme ou un autre « figure ».</span><span class="sxs-lookup"><span data-stu-id="0bcb9-104"><xref:System.Windows.Media.PathGeometry> objects are composed of one or more <xref:System.Windows.Media.PathFigure> objects; each <xref:System.Windows.Media.PathFigure> represents a different "figure" or shape.</span></span> <span data-ttu-id="0bcb9-105">Chaque <xref:System.Windows.Media.PathFigure> est lui-même composé d’un ou plusieurs <xref:System.Windows.Media.PathSegment> d’objets, chacun représentant une partie connectée de l’illustration ou forme.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-105">Each <xref:System.Windows.Media.PathFigure> is itself composed of one or more <xref:System.Windows.Media.PathSegment> objects, each representing a connected portion of the figure or shape.</span></span> <span data-ttu-id="0bcb9-106">Types de segment sont <xref:System.Windows.Media.LineSegment>, <xref:System.Windows.Media.ArcSegment>, et <xref:System.Windows.Media.BezierSegment>.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-106">Segment types include <xref:System.Windows.Media.LineSegment>, <xref:System.Windows.Media.ArcSegment>, and <xref:System.Windows.Media.BezierSegment>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0bcb9-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="0bcb9-107">Example</span></span>  
 <span data-ttu-id="0bcb9-108">L’exemple suivant utilise un <xref:System.Windows.Media.PathGeometry> pour créer un triangle.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-108">The following example uses a <xref:System.Windows.Media.PathGeometry> to create a triangle.</span></span> <span data-ttu-id="0bcb9-109">Le <xref:System.Windows.Media.PathGeometry> est affichée en utilisant un <xref:System.Windows.Shapes.Path> élément.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-109">The  <xref:System.Windows.Media.PathGeometry> is displayed using a <xref:System.Windows.Shapes.Path> element.</span></span>  
  
 [!code-xaml[GeometrySample#49](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#49)]  
  
 <span data-ttu-id="0bcb9-110">L’illustration suivante montre la forme créée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-110">The following illustration shows the shape created in the previous example.</span></span>  
  
 <span data-ttu-id="0bcb9-111">![PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")</span><span class="sxs-lookup"><span data-stu-id="0bcb9-111">![A PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")</span></span>  
<span data-ttu-id="0bcb9-112">Un triangle créé avec un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="0bcb9-112">A triangle created with a PathGeometry</span></span>  
  
 <span data-ttu-id="0bcb9-113">L’exemple précédent a montré comment créer une forme relativement simple, un triangle.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-113">The previous example showed how to create a relatively simple shape, a triangle.</span></span> <span data-ttu-id="0bcb9-114">Un <xref:System.Windows.Media.PathGeometry> peut également être utilisé pour créer des formes plus complexes, y compris des arcs et des courbes.</span><span class="sxs-lookup"><span data-stu-id="0bcb9-114">A <xref:System.Windows.Media.PathGeometry> can also be used to create more complex shapes, including arcs and curves.</span></span> <span data-ttu-id="0bcb9-115">Pour obtenir des exemples, consultez [créer un Arc elliptique](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-an-elliptical-arc.md), [créer une courbe de Bézier cubique](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-cubic-bezier-curve.md), et [créer une courbe de Bézier quadratique](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-quadratic-bezier-curve.md).</span><span class="sxs-lookup"><span data-stu-id="0bcb9-115">For examples, see [Create an Elliptical Arc](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-an-elliptical-arc.md), [Create a Cubic Bezier Curve](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-cubic-bezier-curve.md), and [Create a Quadratic Bezier Curve](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-quadratic-bezier-curve.md).</span></span>  
  
 <span data-ttu-id="0bcb9-116">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](http://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="0bcb9-116">This example is part of larger sample; for the complete sample, see the [Geometries Sample](http://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bcb9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bcb9-117">See Also</span></span>  
 <xref:System.Windows.Shapes.Path>  
 <xref:System.Windows.Media.GeometryDrawing>  
 [<span data-ttu-id="0bcb9-118">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="0bcb9-118">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)  
 [<span data-ttu-id="0bcb9-119">Géométries, exemple</span><span class="sxs-lookup"><span data-stu-id="0bcb9-119">Geometries Sample</span></span>](http://go.microsoft.com/fwlink/?LinkID=159989)
