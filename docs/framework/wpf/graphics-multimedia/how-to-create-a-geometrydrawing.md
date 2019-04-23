---
title: 'Procédure : Créer un GeometryDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
ms.openlocfilehash: f5cdcfdb68ad8030bcbd6c689f45a8baddd000e1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59179788"
---
# <a name="how-to-create-a-geometrydrawing"></a><span data-ttu-id="37ef5-102">Procédure : Créer un GeometryDrawing</span><span class="sxs-lookup"><span data-stu-id="37ef5-102">How to: Create a GeometryDrawing</span></span>
<span data-ttu-id="37ef5-103">Cet exemple montre comment créer et afficher un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="37ef5-103">This example shows how to create and display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="37ef5-104">Un <xref:System.Windows.Media.GeometryDrawing> vous permet de créer la forme avec un remplissage et un contour en associant un <xref:System.Windows.Media.Pen> et un <xref:System.Windows.Media.Brush> avec un <xref:System.Windows.Media.Geometry>.</span><span class="sxs-lookup"><span data-stu-id="37ef5-104">A <xref:System.Windows.Media.GeometryDrawing> enables you to create shape with a fill and an outline by associating a <xref:System.Windows.Media.Pen> and a <xref:System.Windows.Media.Brush> with a <xref:System.Windows.Media.Geometry>.</span></span> <span data-ttu-id="37ef5-105">Le <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> décrit la structure de la forme, le <xref:System.Windows.Media.GeometryDrawing.Brush%2A> décrit le remplissage de la forme et le <xref:System.Windows.Media.GeometryDrawing.Pen%2A> décrit le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="37ef5-105">The <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> describes the shape's structure, the <xref:System.Windows.Media.GeometryDrawing.Brush%2A> describes the shape's fill, and the <xref:System.Windows.Media.GeometryDrawing.Pen%2A> describes the shape's outline.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37ef5-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="37ef5-106">Example</span></span>  
 <span data-ttu-id="37ef5-107">L’exemple suivant utilise un <xref:System.Windows.Media.GeometryDrawing> pour rendre une forme.</span><span class="sxs-lookup"><span data-stu-id="37ef5-107">The following example uses a <xref:System.Windows.Media.GeometryDrawing> to render a shape.</span></span> <span data-ttu-id="37ef5-108">La forme est décrite par un <xref:System.Windows.Media.GeometryGroup> et deux <xref:System.Windows.Media.EllipseGeometry> objets.</span><span class="sxs-lookup"><span data-stu-id="37ef5-108">The shape is described by a <xref:System.Windows.Media.GeometryGroup> and two <xref:System.Windows.Media.EllipseGeometry> objects.</span></span> <span data-ttu-id="37ef5-109">Intérieur de la forme est peint avec un <xref:System.Windows.Media.LinearGradientBrush> et son contour est dessiné avec un <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>.</span><span class="sxs-lookup"><span data-stu-id="37ef5-109">The shape's interior is painted with a <xref:System.Windows.Media.LinearGradientBrush> and its outline is drawn with a <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>.</span></span> <span data-ttu-id="37ef5-110">Le <xref:System.Windows.Media.GeometryDrawing> est affichée en utilisant un <xref:System.Windows.Media.ImageDrawing> et un <xref:System.Windows.Controls.Image> élément.</span><span class="sxs-lookup"><span data-stu-id="37ef5-110">The <xref:System.Windows.Media.GeometryDrawing> is displayed using an <xref:System.Windows.Media.ImageDrawing> and an <xref:System.Windows.Controls.Image> element.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 <span data-ttu-id="37ef5-111">L’illustration suivante montre le résultat <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="37ef5-111">The following illustration shows the resulting <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 <span data-ttu-id="37ef5-112">![GeometryDrawing de deux ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="37ef5-112">![A GeometryDrawing of two ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
  
 <span data-ttu-id="37ef5-113">Pour créer des dessins plus complexes, vous pouvez combiner plusieurs objets de dessin dans un dessin à l’aide de composite unique un <xref:System.Windows.Media.DrawingGroup>.</span><span class="sxs-lookup"><span data-stu-id="37ef5-113">To create more complex drawings, you can combine multiple drawing objects into a single composite drawing using a <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37ef5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37ef5-114">See also</span></span>

- <xref:System.Windows.Media.DrawingGroup>
- [<span data-ttu-id="37ef5-115">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="37ef5-115">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="37ef5-116">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="37ef5-116">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="37ef5-117">Créer un dessin composite</span><span class="sxs-lookup"><span data-stu-id="37ef5-117">Create a Composite Drawing</span></span>](how-to-create-a-composite-drawing.md)
