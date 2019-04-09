---
title: 'Procédure : Créer une ligne à l’aide d’un LineGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], lines
ms.assetid: 41231b22-1f74-4c26-a8e7-a55b29f8f6bd
ms.openlocfilehash: f8c334a54f78aec7af91064a447fd18f23dcfbdc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59123056"
---
# <a name="how-to-create-a-line-using-a-linegeometry"></a><span data-ttu-id="a0bca-102">Procédure : Créer une ligne à l’aide d’un LineGeometry</span><span class="sxs-lookup"><span data-stu-id="a0bca-102">How to: Create a Line Using a LineGeometry</span></span>
<span data-ttu-id="a0bca-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.LineGeometry> classe pour décrire une ligne.</span><span class="sxs-lookup"><span data-stu-id="a0bca-103">This example shows how to use the <xref:System.Windows.Media.LineGeometry> class to describe a line.</span></span> <span data-ttu-id="a0bca-104">Un <xref:System.Windows.Media.LineGeometry> est défini par son début et de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a0bca-104">A <xref:System.Windows.Media.LineGeometry> is defined by its start and end points.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a0bca-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0bca-105">Example</span></span>  
 <span data-ttu-id="a0bca-106">L’exemple suivant montre comment créer et afficher un <xref:System.Windows.Media.LineGeometry>.</span><span class="sxs-lookup"><span data-stu-id="a0bca-106">The following example shows how to create and render a <xref:System.Windows.Media.LineGeometry>.</span></span>  <span data-ttu-id="a0bca-107">Un <xref:System.Windows.Shapes.Path> élément est utilisé pour restituer la ligne.</span><span class="sxs-lookup"><span data-stu-id="a0bca-107">A <xref:System.Windows.Shapes.Path> element is used to render the line.</span></span>  <span data-ttu-id="a0bca-108">Dans la mesure où une ligne n’a pas de zone, le <xref:System.Windows.Shapes.Path> l’objet <xref:System.Windows.Shapes.Shape.Fill%2A> n’est pas spécifié ; au lieu de cela la <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> propriétés sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="a0bca-108">Since a line has no area, the <xref:System.Windows.Shapes.Path> object's <xref:System.Windows.Shapes.Shape.Fill%2A> is not specified; instead the <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> properties are used.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmlinegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmlinegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMLineGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmlinegeometryexample)]  
  
 <span data-ttu-id="a0bca-109">![A LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")</span><span class="sxs-lookup"><span data-stu-id="a0bca-109">![A LineGeometry](./media/graphicsmm-line.gif "graphicsmm_line")</span></span>  
<span data-ttu-id="a0bca-110">Une LineGeometry tracée de (10,20) à (100,130)</span><span class="sxs-lookup"><span data-stu-id="a0bca-110">A LineGeometry drawn from (10,20) to (100,130)</span></span>  
  
 <span data-ttu-id="a0bca-111">Autres classes de géométrie simple incluent <xref:System.Windows.Media.LineGeometry> et <xref:System.Windows.Media.EllipseGeometry>.</span><span class="sxs-lookup"><span data-stu-id="a0bca-111">Other simple geometry classes include <xref:System.Windows.Media.LineGeometry> and <xref:System.Windows.Media.EllipseGeometry>.</span></span> <span data-ttu-id="a0bca-112">Ces géométries, ainsi que celles qui sont plus complexes, peut également être créés à l’aide un <xref:System.Windows.Media.PathGeometry> ou <xref:System.Windows.Media.StreamGeometry>.</span><span class="sxs-lookup"><span data-stu-id="a0bca-112">These geometries, as well as more complex ones, can also be created using a <xref:System.Windows.Media.PathGeometry> or <xref:System.Windows.Media.StreamGeometry>.</span></span> <span data-ttu-id="a0bca-113">Pour plus d’informations, consultez le [vue d’ensemble de Geometry](geometry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a0bca-113">For more information, see the [Geometry Overview](geometry-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0bca-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0bca-114">See also</span></span>

- [<span data-ttu-id="a0bca-115">Vue d'ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="a0bca-115">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="a0bca-116">Créer une forme composite</span><span class="sxs-lookup"><span data-stu-id="a0bca-116">Create a Composite Shape</span></span>](how-to-create-a-composite-shape.md)
- [<span data-ttu-id="a0bca-117">Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="a0bca-117">Create a Shape by Using a PathGeometry</span></span>](how-to-create-a-shape-by-using-a-pathgeometry.md)
