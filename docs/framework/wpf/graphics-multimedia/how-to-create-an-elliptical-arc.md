---
title: 'Comment : créer un arc elliptique'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], elliptical arcs
- elliptical arcs [WPF], creating
- arcs [WPF], elliptical
ms.assetid: 3dcfe502-3485-45de-99fb-d53a1367c484
ms.openlocfilehash: 7ca7d06aa25f8dfae648d8c54c8b95cc277ffbf9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43393833"
---
# <a name="how-to-create-an-elliptical-arc"></a><span data-ttu-id="0836b-102">Comment : créer un arc elliptique</span><span class="sxs-lookup"><span data-stu-id="0836b-102">How to: Create an Elliptical Arc</span></span>
<span data-ttu-id="0836b-103">Cet exemple montre comment dessiner un arc elliptique. Pour créer un arc elliptique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.ArcSegment> classes.</span><span class="sxs-lookup"><span data-stu-id="0836b-103">This example shows how to draw an elliptical arc. To create an elliptical arc, use the <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, and <xref:System.Windows.Media.ArcSegment> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0836b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0836b-104">Example</span></span>  
 <span data-ttu-id="0836b-105">Dans les exemples suivants, un arc elliptique est dessiné de (10,100) à (200,100).</span><span class="sxs-lookup"><span data-stu-id="0836b-105">In the following examples, an elliptical arc is drawn from (10,100) to (200,100).</span></span> <span data-ttu-id="0836b-106">L’arc a un <xref:System.Windows.Media.ArcSegment.Size%2A> de pixels indépendants du périphérique de 100 par 50, un <xref:System.Windows.Media.ArcSegment.RotationAngle%2A> de 45 degrés, un <xref:System.Windows.Media.ArcSegment.IsLargeArc%2A> définition de `true`et un <xref:System.Windows.Media.ArcSegment.SweepDirection%2A> de <xref:System.Windows.Media.SweepDirection.Counterclockwise>.</span><span class="sxs-lookup"><span data-stu-id="0836b-106">The arc has a <xref:System.Windows.Media.ArcSegment.Size%2A> of 100 by 50 device-independent pixels, a <xref:System.Windows.Media.ArcSegment.RotationAngle%2A> of 45 degrees, an <xref:System.Windows.Media.ArcSegment.IsLargeArc%2A> setting of `true`, and a <xref:System.Windows.Media.ArcSegment.SweepDirection%2A> of <xref:System.Windows.Media.SweepDirection.Counterclockwise>.</span></span>  
  
 <span data-ttu-id="0836b-107">[xaml]</span><span class="sxs-lookup"><span data-stu-id="0836b-107">[xaml]</span></span>  
  
 <span data-ttu-id="0836b-108">Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe d’attribut pour décrire un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0836b-108">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], you can use attribute syntax to describe a path.</span></span>  
  
 [!code-xaml[GeometrySample#56](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#56)]  
  
 <span data-ttu-id="0836b-109">[xaml]</span><span class="sxs-lookup"><span data-stu-id="0836b-109">[xaml]</span></span>  
  
 <span data-ttu-id="0836b-110">(Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="0836b-110">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="0836b-111">(Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md).)</span><span class="sxs-lookup"><span data-stu-id="0836b-111">For more information, see the [Path Markup Syntax](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) page.)</span></span>  
  
 <span data-ttu-id="0836b-112">Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner un arc elliptique en utilisant explicitement des balises d’objet.</span><span class="sxs-lookup"><span data-stu-id="0836b-112">In [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you can also draw an elliptical arc by explicitly using object tags.</span></span> <span data-ttu-id="0836b-113">Ce qui suit est équivalent à l’exemple précédent [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] balisage.</span><span class="sxs-lookup"><span data-stu-id="0836b-113">The following is equivalent to the preceding [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] markup.</span></span>  
  
 [!code-xaml[GeometrySample#36](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#36)]  
  
 <span data-ttu-id="0836b-114">Cet exemple fait partie d’un exemple plus complet.</span><span class="sxs-lookup"><span data-stu-id="0836b-114">This example is part of a larger sample.</span></span> <span data-ttu-id="0836b-115">Pour obtenir un exemple complet, consultez la [géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="0836b-115">For the complete sample, see the [Geometries Sample](https://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0836b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0836b-116">See Also</span></span>  
 [<span data-ttu-id="0836b-117">Créer une courbe de Bézier quadratique</span><span class="sxs-lookup"><span data-stu-id="0836b-117">Create a Quadratic Bezier Curve</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-quadratic-bezier-curve.md)  
 [<span data-ttu-id="0836b-118">Créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="0836b-118">Create a Cubic Bezier Curve</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-cubic-bezier-curve.md)
