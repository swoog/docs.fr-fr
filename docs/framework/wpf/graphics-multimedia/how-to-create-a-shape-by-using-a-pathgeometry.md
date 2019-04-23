---
title: 'Procédure : Créer une forme à l’aide d’un PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], creating with PathGeometry class
- graphics [WPF], shapes
ms.assetid: 49a4a8b7-e738-45be-8dac-b54a6d8f5b21
ms.openlocfilehash: b0ab703596612524881ab892a1095b0f49cd1551
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59159313"
---
# <a name="how-to-create-a-shape-by-using-a-pathgeometry"></a><span data-ttu-id="49ff9-102">Procédure : Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="49ff9-102">How to: Create a Shape by Using a PathGeometry</span></span>
<span data-ttu-id="49ff9-103">Cet exemple montre comment créer une forme à l’aide de la <xref:System.Windows.Media.PathGeometry> classe.</span><span class="sxs-lookup"><span data-stu-id="49ff9-103">This example shows how to create a shape using the <xref:System.Windows.Media.PathGeometry> class.</span></span> <span data-ttu-id="49ff9-104"><xref:System.Windows.Media.PathGeometry> les objets sont composés d’un ou plusieurs <xref:System.Windows.Media.PathFigure> objets ; chaque <xref:System.Windows.Media.PathFigure> représente un autre « figure » ou une forme.</span><span class="sxs-lookup"><span data-stu-id="49ff9-104"><xref:System.Windows.Media.PathGeometry> objects are composed of one or more <xref:System.Windows.Media.PathFigure> objects; each <xref:System.Windows.Media.PathFigure> represents a different "figure" or shape.</span></span> <span data-ttu-id="49ff9-105">Chaque <xref:System.Windows.Media.PathFigure> est elle-même composée d’un ou plusieurs <xref:System.Windows.Media.PathSegment> d’objets, chacun représentant une partie connectée de l’illustration ou d’une forme.</span><span class="sxs-lookup"><span data-stu-id="49ff9-105">Each <xref:System.Windows.Media.PathFigure> is itself composed of one or more <xref:System.Windows.Media.PathSegment> objects, each representing a connected portion of the figure or shape.</span></span> <span data-ttu-id="49ff9-106">Types de segment sont <xref:System.Windows.Media.LineSegment>, <xref:System.Windows.Media.ArcSegment>, et <xref:System.Windows.Media.BezierSegment>.</span><span class="sxs-lookup"><span data-stu-id="49ff9-106">Segment types include <xref:System.Windows.Media.LineSegment>, <xref:System.Windows.Media.ArcSegment>, and <xref:System.Windows.Media.BezierSegment>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="49ff9-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="49ff9-107">Example</span></span>  
 <span data-ttu-id="49ff9-108">L’exemple suivant utilise un <xref:System.Windows.Media.PathGeometry> pour créer un triangle.</span><span class="sxs-lookup"><span data-stu-id="49ff9-108">The following example uses a <xref:System.Windows.Media.PathGeometry> to create a triangle.</span></span> <span data-ttu-id="49ff9-109">Le <xref:System.Windows.Media.PathGeometry> est affichée en utilisant un <xref:System.Windows.Shapes.Path> élément.</span><span class="sxs-lookup"><span data-stu-id="49ff9-109">The  <xref:System.Windows.Media.PathGeometry> is displayed using a <xref:System.Windows.Shapes.Path> element.</span></span>  
  
 [!code-xaml[GeometrySample#49](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#49)]  
  
 <span data-ttu-id="49ff9-110">L’illustration suivante montre la forme créée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="49ff9-110">The following illustration shows the shape created in the previous example.</span></span>  
  
 <span data-ttu-id="49ff9-111">![Une PathGeometry](./media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")</span><span class="sxs-lookup"><span data-stu-id="49ff9-111">![A PathGeometry](./media/wcpsdk-graphicsmm-pathgeometry-triangle.gif "wcpsdk_graphicsmm_pathgeometry_triangle")</span></span>  
<span data-ttu-id="49ff9-112">Un triangle créé avec un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="49ff9-112">A triangle created with a PathGeometry</span></span>  
  
 <span data-ttu-id="49ff9-113">L’exemple précédent a montré comment créer une forme relativement simple, un triangle.</span><span class="sxs-lookup"><span data-stu-id="49ff9-113">The previous example showed how to create a relatively simple shape, a triangle.</span></span> <span data-ttu-id="49ff9-114">Un <xref:System.Windows.Media.PathGeometry> peut également être utilisé pour créer des formes plus complexes, y compris les arcs et courbes.</span><span class="sxs-lookup"><span data-stu-id="49ff9-114">A <xref:System.Windows.Media.PathGeometry> can also be used to create more complex shapes, including arcs and curves.</span></span> <span data-ttu-id="49ff9-115">Pour obtenir des exemples, consultez [créer un Arc elliptique](how-to-create-an-elliptical-arc.md), [créer une courbe de Bézier cubique](how-to-create-a-cubic-bezier-curve.md), et [créer une courbe de Bézier quadratique](how-to-create-a-quadratic-bezier-curve.md).</span><span class="sxs-lookup"><span data-stu-id="49ff9-115">For examples, see [Create an Elliptical Arc](how-to-create-an-elliptical-arc.md), [Create a Cubic Bezier Curve](how-to-create-a-cubic-bezier-curve.md), and [Create a Quadratic Bezier Curve](how-to-create-a-quadratic-bezier-curve.md).</span></span>  
  
 <span data-ttu-id="49ff9-116">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="49ff9-116">This example is part of larger sample; for the complete sample, see the [Geometries Sample](https://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49ff9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49ff9-117">See also</span></span>

- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.GeometryDrawing>
- [<span data-ttu-id="49ff9-118">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="49ff9-118">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="49ff9-119">Géométries, exemple</span><span class="sxs-lookup"><span data-stu-id="49ff9-119">Geometries Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159989)
