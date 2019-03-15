---
title: 'Procédure : Créer un LineSegment dans un PathGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- line segments [WPF], creating
- graphics [WPF], line segments
ms.assetid: 0155ed47-a20d-49a7-a306-186d8e07fbc4
ms.openlocfilehash: a50c98ccc3f6d517e0917cb774af4d49d2bfa7a3
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57845630"
---
# <a name="how-to-create-a-linesegment-in-a-pathgeometry"></a><span data-ttu-id="25e74-102">Procédure : Créer un LineSegment dans un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="25e74-102">How to: Create a LineSegment in a PathGeometry</span></span>

<span data-ttu-id="25e74-103">Cet exemple indique comment créer un segment de ligne.</span><span class="sxs-lookup"><span data-stu-id="25e74-103">This example shows how to create a line segment.</span></span> <span data-ttu-id="25e74-104">Pour créer un segment de ligne, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.LineSegment> classes.</span><span class="sxs-lookup"><span data-stu-id="25e74-104">To create a line segment, use the <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, and <xref:System.Windows.Media.LineSegment> classes.</span></span>

## <a name="example"></a><span data-ttu-id="25e74-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="25e74-105">Example</span></span>

<span data-ttu-id="25e74-106">Les exemples suivants tracent un <xref:System.Windows.Media.LineSegment> à partir de (10, 50) à (200, 70).</span><span class="sxs-lookup"><span data-stu-id="25e74-106">The following examples draw a <xref:System.Windows.Media.LineSegment> from (10, 50) to (200, 70).</span></span> <span data-ttu-id="25e74-107">L’illustration suivante montre le résultat <xref:System.Windows.Media.LineSegment>; un arrière-plan de la grille a été ajouté pour afficher le système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="25e74-107">The following illustration shows the resulting <xref:System.Windows.Media.LineSegment>; a grid background was added to show the coordinate system.</span></span>

<span data-ttu-id="25e74-108">![LineSegment dans un PathFigure](./media/graphicsmm-pathgeometrylinesegment.png "graphicsmm_pathgeometrylinesegment") LineSegment un tracé de (10,50) à (200,70)</span><span class="sxs-lookup"><span data-stu-id="25e74-108">![A LineSegment in a PathFigure](./media/graphicsmm-pathgeometrylinesegment.png "graphicsmm_pathgeometrylinesegment") A LineSegment drawn from (10,50) to (200,70)</span></span>

<span data-ttu-id="25e74-109">[xaml]</span><span class="sxs-lookup"><span data-stu-id="25e74-109">[xaml]</span></span>

<span data-ttu-id="25e74-110">En [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe d’attribut pour décrire un tracé.</span><span class="sxs-lookup"><span data-stu-id="25e74-110">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], you may use attribute syntax to describe a path.</span></span>

```xaml
<Path Stroke="Black" StrokeThickness="1"
  Data="M 10,50 L 200,70" />
```

<span data-ttu-id="25e74-111">[xaml]</span><span class="sxs-lookup"><span data-stu-id="25e74-111">[xaml]</span></span>

<span data-ttu-id="25e74-112">(Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="25e74-112">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="25e74-113">(Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)</span><span class="sxs-lookup"><span data-stu-id="25e74-113">For more information, see the [Path Markup Syntax](path-markup-syntax.md) page.)</span></span>

<span data-ttu-id="25e74-114">En [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner un segment de ligne en utilisant la syntaxe d’élément objet.</span><span class="sxs-lookup"><span data-stu-id="25e74-114">In [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you may also draw a line segment by using object element syntax.</span></span> <span data-ttu-id="25e74-115">L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.</span><span class="sxs-lookup"><span data-stu-id="25e74-115">The following is equivalent to the previous [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] example.</span></span>

```xaml
<Path Stroke="Black" StrokeThickness="1">
  <Path.Data>
    <PathGeometry>
      <PathFigure StartPoint="10,50">
        <LineSegment Point="200,70" />
      </PathFigure>
    </PathGeometry>
  </Path.Data>
</Path>
```

```csharp
PathFigure myPathFigure = new PathFigure();
myPathFigure.StartPoint = new Point(10, 50);

LineSegment myLineSegment = new LineSegment();
myLineSegment.Point = new Point(200, 70);

PathSegmentCollection myPathSegmentCollection = new PathSegmentCollection();
myPathSegmentCollection.Add(myLineSegment);

myPathFigure.Segments = myPathSegmentCollection;

PathFigureCollection myPathFigureCollection = new PathFigureCollection();
myPathFigureCollection.Add(myPathFigure);

PathGeometry myPathGeometry = new PathGeometry();
myPathGeometry.Figures = myPathFigureCollection;

Path myPath = new Path();
myPath.Stroke = Brushes.Black;
myPath.StrokeThickness = 1;
myPath.Data = myPathGeometry;
```

```vb
Dim myPathFigure As New PathFigure()
myPathFigure.StartPoint = New Point(10, 50)

Dim myLineSegment As New LineSegment()
myLineSegment.Point = New Point(200, 70)

Dim myPathSegmentCollection As New PathSegmentCollection()
myPathSegmentCollection.Add(myLineSegment)

myPathFigure.Segments = myPathSegmentCollection

Dim myPathFigureCollection As New PathFigureCollection()
myPathFigureCollection.Add(myPathFigure)

Dim myPathGeometry As New PathGeometry()
myPathGeometry.Figures = myPathFigureCollection

Dim myPath As New Path()
myPath.Stroke = Brushes.Black
myPath.StrokeThickness = 1
myPath.Data = myPathGeometry
```

<span data-ttu-id="25e74-116">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="25e74-116">This example is part of larger sample; for the complete sample, see the [Geometries Sample](https://go.microsoft.com/fwlink/?LinkID=159989).</span></span>

## <a name="see-also"></a><span data-ttu-id="25e74-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25e74-117">See also</span></span>

- <xref:System.Windows.Media.PathFigure>
- <xref:System.Windows.Media.PathGeometry>
- <xref:System.Windows.Media.GeometryDrawing>
- <xref:System.Windows.Shapes.Path>
- [<span data-ttu-id="25e74-118">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="25e74-118">Geometry Overview</span></span>](geometry-overview.md)
