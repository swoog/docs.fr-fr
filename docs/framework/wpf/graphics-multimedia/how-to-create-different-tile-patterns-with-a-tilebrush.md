---
title: 'Procédure : Créer différents modèles de mosaïque avec un TileBrush'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], creating tile patterns
- tile patterns [WPF], creating
- creating [WPF], tile patterns with TileBrush
ms.assetid: 5aa46632-3527-4668-9d8d-0375c8af28aa
ms.openlocfilehash: c1051b234961eee9ae740af2abac3d64c523656c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227403"
---
# <a name="how-to-create-different-tile-patterns-with-a-tilebrush"></a><span data-ttu-id="14456-102">Procédure : Créer différents modèles de mosaïque avec un TileBrush</span><span class="sxs-lookup"><span data-stu-id="14456-102">How to: Create Different Tile Patterns with a TileBrush</span></span>
<span data-ttu-id="14456-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété d’un <xref:System.Windows.Media.TileBrush> pour créer un modèle.</span><span class="sxs-lookup"><span data-stu-id="14456-103">This example shows how to use the <xref:System.Windows.Media.TileBrush.TileMode%2A> property of a <xref:System.Windows.Media.TileBrush> to create a pattern.</span></span>  
  
 <span data-ttu-id="14456-104">Le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété vous permet de spécifier comment le contenu d’un <xref:System.Windows.Media.TileBrush> est répété, autrement dit, en mosaïque pour remplir une zone de sortie.</span><span class="sxs-lookup"><span data-stu-id="14456-104">The <xref:System.Windows.Media.TileBrush.TileMode%2A> property enables you to specify how the content of a <xref:System.Windows.Media.TileBrush> is repeated, that is, tiled to fill an output area.</span></span> <span data-ttu-id="14456-105">Pour créer un modèle, vous définissez le <xref:System.Windows.Media.TileBrush.TileMode%2A> à <xref:System.Windows.Media.TileMode.Tile>, <xref:System.Windows.Media.TileMode.FlipX>, <xref:System.Windows.Media.TileMode.FlipY>, ou <xref:System.Windows.Media.TileMode.FlipXY>.</span><span class="sxs-lookup"><span data-stu-id="14456-105">To create a pattern, you set the <xref:System.Windows.Media.TileBrush.TileMode%2A> to <xref:System.Windows.Media.TileMode.Tile>, <xref:System.Windows.Media.TileMode.FlipX>, <xref:System.Windows.Media.TileMode.FlipY>, or <xref:System.Windows.Media.TileMode.FlipXY>.</span></span> <span data-ttu-id="14456-106">Vous devez également définir le <xref:System.Windows.Media.TileBrush.Viewport%2A> de la <xref:System.Windows.Media.TileBrush> afin qu’elle soit inférieure à la zone que vous peignez ; sinon, qu’une seule vignette est produite, quel que soit ce qui <xref:System.Windows.Media.TileBrush.TileMode%2A> paramètre que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="14456-106">You must also set the <xref:System.Windows.Media.TileBrush.Viewport%2A> of the <xref:System.Windows.Media.TileBrush> so that it is smaller than the area that you are painting; otherwise, only a single tile is produced, regardless which <xref:System.Windows.Media.TileBrush.TileMode%2A> setting you use.</span></span>  
  
## <a name="example"></a><span data-ttu-id="14456-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="14456-107">Example</span></span>  
 <span data-ttu-id="14456-108">L’exemple suivant crée cinq <xref:System.Windows.Media.DrawingBrush> des objets, leur donne chaque une autre <xref:System.Windows.Media.TileBrush.TileMode%2A> définition et les utilise pour peindre cinq rectangles.</span><span class="sxs-lookup"><span data-stu-id="14456-108">The following example creates five <xref:System.Windows.Media.DrawingBrush> objects, gives them each a different <xref:System.Windows.Media.TileBrush.TileMode%2A> setting, and uses them to paint five rectangles.</span></span> <span data-ttu-id="14456-109">Bien que cet exemple utilise le <xref:System.Windows.Media.DrawingBrush> classe afin d’illustrer <xref:System.Windows.Media.TileBrush.TileMode%2A> comportement, le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété fonctionne de manière identique pour tous les le <xref:System.Windows.Media.TileBrush> d’objets, autrement dit, pour <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.VisualBrush>, et <xref:System.Windows.Media.DrawingBrush>.</span><span class="sxs-lookup"><span data-stu-id="14456-109">Although this example uses the <xref:System.Windows.Media.DrawingBrush> class to demonstrate <xref:System.Windows.Media.TileBrush.TileMode%2A> behavior, the <xref:System.Windows.Media.TileBrush.TileMode%2A> property works identically for all the <xref:System.Windows.Media.TileBrush> objects, that is, for <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.VisualBrush>, and <xref:System.Windows.Media.DrawingBrush>.</span></span>  
  
 <span data-ttu-id="14456-110">L’illustration suivante montre la sortie que l’exemple génère.</span><span class="sxs-lookup"><span data-stu-id="14456-110">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="14456-111">![Exemple de sortie de la mosaïque de TileBrush](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")</span><span class="sxs-lookup"><span data-stu-id="14456-111">![TileBrush tiling example output](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")</span></span>  
<span data-ttu-id="14456-112">Les modèles créés avec la propriété TileMode de mosaïque</span><span class="sxs-lookup"><span data-stu-id="14456-112">Tile patterns created with the TileMode property</span></span>  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/TileModeExample.cs#graphicsmmdrawingbrushtilemodeexample)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/tilemodeexample.vb#graphicsmmdrawingbrushtilemodeexample)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/TileModeExample.xaml#graphicsmmdrawingbrushtilemodeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="14456-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14456-113">See also</span></span>

- [<span data-ttu-id="14456-114">Définir la taille de la mosaïque pour un TileBrush</span><span class="sxs-lookup"><span data-stu-id="14456-114">Set the Tile Size for a TileBrush</span></span>](how-to-set-the-tile-size-for-a-tilebrush.md)
- [<span data-ttu-id="14456-115">Peinture avec des objets d'image, de dessin et visuels</span><span class="sxs-lookup"><span data-stu-id="14456-115">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
