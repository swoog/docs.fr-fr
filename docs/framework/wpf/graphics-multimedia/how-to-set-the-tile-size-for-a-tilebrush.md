---
title: 'Procédure : Définir la taille de la mosaïque pour un TileBrush'
ms.date: 03/30/2017
helpviewer_keywords:
- TileBrush [WPF], size of tile properties
- Viewport property of TileBrush [WPF]
ms.assetid: 04f41090-1b46-4e36-832f-d27d28708b8c
ms.openlocfilehash: 80b5dfc668464df829db593668bea8a9a4ec09e4
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58839674"
---
# <a name="how-to-set-the-tile-size-for-a-tilebrush"></a><span data-ttu-id="9bdb4-102">Procédure : Définir la taille de la mosaïque pour un TileBrush</span><span class="sxs-lookup"><span data-stu-id="9bdb4-102">How to: Set the Tile Size for a TileBrush</span></span>

<span data-ttu-id="9bdb4-103">Cet exemple montre comment définir la taille de la mosaïque pour un <xref:System.Windows.Media.TileBrush>.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-103">This example shows how to set the tile size for a <xref:System.Windows.Media.TileBrush>.</span></span> <span data-ttu-id="9bdb4-104">Par défaut, un <xref:System.Windows.Media.TileBrush> produit une seule mosaïque qui remplit complètement la zone que vous peignez.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-104">By default, a <xref:System.Windows.Media.TileBrush> produces a single tile that completely fills the area that you are painting.</span></span> <span data-ttu-id="9bdb4-105">Vous pouvez substituer ce comportement en définissant le <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-105">You can override this behavior by setting the <xref:System.Windows.Media.TileBrush.Viewport%2A> and <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> properties.</span></span>

<span data-ttu-id="9bdb4-106">Le <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété spécifie la taille de la mosaïque pour un <xref:System.Windows.Media.TileBrush>.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-106">The <xref:System.Windows.Media.TileBrush.Viewport%2A> property specifies the tile size for a <xref:System.Windows.Media.TileBrush>.</span></span> <span data-ttu-id="9bdb4-107">Par défaut, la valeur de la <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété est relative à la taille de la zone peinte.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-107">By default, the value of the <xref:System.Windows.Media.TileBrush.Viewport%2A> property is relative to the size of the area being painted.</span></span> <span data-ttu-id="9bdb4-108">Pour rendre le <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété spécifier une taille de mosaïque absolue, définissez le <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriété <xref:System.Windows.Media.BrushMappingMode.Absolute>.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-108">To make the <xref:System.Windows.Media.TileBrush.Viewport%2A> property specify an absolute tile size, set the <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> property to <xref:System.Windows.Media.BrushMappingMode.Absolute>.</span></span>

## <a name="example"></a><span data-ttu-id="9bdb4-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="9bdb4-109">Example</span></span>

<span data-ttu-id="9bdb4-110">L’exemple suivant utilise un <xref:System.Windows.Media.ImageBrush>, un type de <xref:System.Windows.Media.TileBrush>, pour peindre un rectangle avec des vignettes.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-110">The following example uses an <xref:System.Windows.Media.ImageBrush>, a type of <xref:System.Windows.Media.TileBrush>, to paint a rectangle with tiles.</span></span> <span data-ttu-id="9bdb4-111">L’exemple définit chaque mosaïque à 50 % de 50 % de la zone de sortie (le rectangle).</span><span class="sxs-lookup"><span data-stu-id="9bdb4-111">The example sets each tile to 50 percent by 50 percent of the output area (the rectangle).</span></span> <span data-ttu-id="9bdb4-112">Le rectangle est donc peint avec quatre projections de l’image.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-112">As a result, the rectangle is painted with four projections of the image.</span></span>

<span data-ttu-id="9bdb4-113">L’illustration suivante montre la sortie produite par l’exemple :</span><span class="sxs-lookup"><span data-stu-id="9bdb4-113">The following illustration shows the output that the example produces:</span></span>

![Un rectangle avec quatre cerises démonstration de mosaïque avec un pinceau d’image.](./media/how-to-set-the-tile-size-for-a-tilebrush/rectangle-tile-image-brush.png)

[!code-csharp[UsingImageBrush_snip#RelativeTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#relativetilesizeexample)]

<span data-ttu-id="9bdb4-115">L’exemple suivant crée un <xref:System.Windows.Media.ImageBrush>, définit son <xref:System.Windows.Media.TileBrush.Viewport%2A> à `0,0,25,25` et son <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> à <xref:System.Windows.Media.BrushMappingMode.Absolute>et l’utilise pour peindre un autre rectangle.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-115">The next example creates an <xref:System.Windows.Media.ImageBrush>, sets its <xref:System.Windows.Media.TileBrush.Viewport%2A> to `0,0,25,25` and its <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> to <xref:System.Windows.Media.BrushMappingMode.Absolute>, and uses it to paint another rectangle.</span></span> <span data-ttu-id="9bdb4-116">Le pinceau produit ainsi des mosaïques d’une largeur de 25 pixels et d’une hauteur de 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-116">As a result, the brush produces tiles that have a width of 25  pixels and a height of 25 pixels .</span></span>

<span data-ttu-id="9bdb4-117">L’illustration suivante montre la sortie produite par l’exemple :</span><span class="sxs-lookup"><span data-stu-id="9bdb4-117">The following illustration shows the output that the example produces:</span></span>

![Un rectangle avec cerises quarante-huit illustrant un TileBrush en mosaïque avec une fenêtre d’affichage.](./media/how-to-set-the-tile-size-for-a-tilebrush/25-x-25-viewport-tilebrush.png)

[!code-csharp[UsingImageBrush_snip#AbsoluteTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#absolutetilesizeexample)]

<span data-ttu-id="9bdb4-119">Les exemples précédents font partie d’un exemple plus complet.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-119">The preceding examples are part of a larger sample.</span></span> <span data-ttu-id="9bdb4-120">Pour obtenir un exemple complet, consultez [ImageBrush, exemple](https://go.microsoft.com/fwlink/?LinkID=160005).</span><span class="sxs-lookup"><span data-stu-id="9bdb4-120">For the complete sample, see [ImageBrush Sample](https://go.microsoft.com/fwlink/?LinkID=160005).</span></span>

<span data-ttu-id="9bdb4-121">Bien que cet exemple utilise le <xref:System.Windows.Media.ImageBrush> (classe), le <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriétés ont un comportement identique pour les autres <xref:System.Windows.Media.TileBrush> d’objets, autrement dit, pour <xref:System.Windows.Media.DrawingBrush> et <xref:System.Windows.Media.VisualBrush>.</span><span class="sxs-lookup"><span data-stu-id="9bdb4-121">Although this example uses the <xref:System.Windows.Media.ImageBrush> class, the <xref:System.Windows.Media.TileBrush.Viewport%2A> and <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> properties behave identically for the other <xref:System.Windows.Media.TileBrush> objects, that is, for <xref:System.Windows.Media.DrawingBrush> and <xref:System.Windows.Media.VisualBrush>.</span></span> <span data-ttu-id="9bdb4-122">Pour plus d’informations sur <xref:System.Windows.Media.ImageBrush> et l’autre <xref:System.Windows.Media.TileBrush> , consultez [peinture avec des Images, de dessin et visuels](painting-with-images-drawings-and-visuals.md).</span><span class="sxs-lookup"><span data-stu-id="9bdb4-122">For more information about <xref:System.Windows.Media.ImageBrush> and the other <xref:System.Windows.Media.TileBrush> objects, see [Painting with Images, Drawings, and Visuals](painting-with-images-drawings-and-visuals.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9bdb4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bdb4-123">See also</span></span>

- <xref:System.Windows.Media.TileBrush>
- [<span data-ttu-id="9bdb4-124">Peinture avec des images, des dessins et des objets visuels</span><span class="sxs-lookup"><span data-stu-id="9bdb4-124">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
- [<span data-ttu-id="9bdb4-125">Créer différents modèles de mosaïque avec un TileBrush</span><span class="sxs-lookup"><span data-stu-id="9bdb4-125">Create Different Tile Patterns with a TileBrush</span></span>](how-to-create-different-tile-patterns-with-a-tilebrush.md)
