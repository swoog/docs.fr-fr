---
title: 'Comment : peindre une zone avec une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], painting with
- painting [WPF], with images
- brushes [WPF], painting with images
ms.assetid: 3432c533-1fc7-492d-94ee-0b13d60125ae
ms.openlocfilehash: 5899531291c22ada76213905d0f2ca6944fcbba7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43857204"
---
# <a name="how-to-paint-an-area-with-an-image"></a><span data-ttu-id="85441-102">Comment : peindre une zone avec une image</span><span class="sxs-lookup"><span data-stu-id="85441-102">How to: Paint an Area with an Image</span></span>
<span data-ttu-id="85441-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.ImageBrush> classe pour peindre une zone avec une image.</span><span class="sxs-lookup"><span data-stu-id="85441-103">This example shows how to use the <xref:System.Windows.Media.ImageBrush> class to paint an area with an image.</span></span> <span data-ttu-id="85441-104">Un <xref:System.Windows.Media.ImageBrush> affiche une seule image, qui est spécifiée par son <xref:System.Windows.Media.ImageBrush.ImageSource%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="85441-104">An <xref:System.Windows.Media.ImageBrush> displays a single image, which is specified by its <xref:System.Windows.Media.ImageBrush.ImageSource%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="85441-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="85441-105">Example</span></span>  
 <span data-ttu-id="85441-106">L’exemple suivant peint le <xref:System.Windows.Controls.Control.Background%2A> d’un bouton à l’aide un <xref:System.Windows.Media.ImageBrush>.</span><span class="sxs-lookup"><span data-stu-id="85441-106">The following example paints the <xref:System.Windows.Controls.Control.Background%2A> of a button by using an <xref:System.Windows.Media.ImageBrush>.</span></span>  
  
 [!code-csharp[UsingImageBrush_snip#ImageBrushExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/PaintingWithImagesExample.cs#imagebrushexamplewholepage)]  
  
 <span data-ttu-id="85441-107">Par défaut, un <xref:System.Windows.Media.ImageBrush> étire son image pour remplir complètement la zone que vous peignez.</span><span class="sxs-lookup"><span data-stu-id="85441-107">By default, an <xref:System.Windows.Media.ImageBrush> stretches its image to completely fill the area that you are painting.</span></span> <span data-ttu-id="85441-108">Dans l’exemple précédent, l’image est étirée pour remplir le bouton, ce qui peut éventuellement déformer l’image.</span><span class="sxs-lookup"><span data-stu-id="85441-108">In the preceding example, the image is stretched to fill the button, possibly distorting the image.</span></span> <span data-ttu-id="85441-109">Vous pouvez contrôler ce comportement en définissant le <xref:System.Windows.Media.TileBrush.Stretch%2A> propriété du <xref:System.Windows.Media.TileBrush> à <xref:System.Windows.Media.Stretch.Uniform> ou <xref:System.Windows.Media.Stretch.UniformToFill>, ce qui entraîne le pinceau de conserver les proportions de l’image.</span><span class="sxs-lookup"><span data-stu-id="85441-109">You can control this behavior by setting the <xref:System.Windows.Media.TileBrush.Stretch%2A> property of <xref:System.Windows.Media.TileBrush> to <xref:System.Windows.Media.Stretch.Uniform> or <xref:System.Windows.Media.Stretch.UniformToFill>, which causes the brush to preserve the aspect ratio of the image.</span></span>  
  
 <span data-ttu-id="85441-110">Si vous définissez la <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.TileMode%2A> propriétés d’un <xref:System.Windows.Media.ImageBrush>, vous pouvez créer un modèle de répétition.</span><span class="sxs-lookup"><span data-stu-id="85441-110">If you set the <xref:System.Windows.Media.TileBrush.Viewport%2A> and <xref:System.Windows.Media.TileBrush.TileMode%2A> properties of an <xref:System.Windows.Media.ImageBrush>, you can create a repeating pattern.</span></span> <span data-ttu-id="85441-111">L’exemple suivant peint un bouton en utilisant un modèle créé à partir d’une image.</span><span class="sxs-lookup"><span data-stu-id="85441-111">The following example paints a button by using a pattern that is created from an image.</span></span>  
  
 [!code-csharp[UsingImageBrush_snip#TiledImageBrushExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TiledImageBrushExample.cs#tiledimagebrushexamplewholepage)]
 [!code-vb[UsingImageBrush_snip#TiledImageBrushExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UsingImageBrush_snip/VisualBasic/TiledImageBrushExample.vb#tiledimagebrushexamplewholepage)]  
  
 <span data-ttu-id="85441-112">Pour plus d’informations sur la <xref:System.Windows.Media.ImageBrush> de classe, consultez [peinture avec des Images, de dessin et visuels](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md).</span><span class="sxs-lookup"><span data-stu-id="85441-112">For more information about the <xref:System.Windows.Media.ImageBrush> class, see [Painting with Images, Drawings, and Visuals](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md).</span></span>  
  
 <span data-ttu-id="85441-113">Cet exemple de code fait partie d’un exemple plus complet fourni pour la <xref:System.Windows.Media.ImageBrush> classe.</span><span class="sxs-lookup"><span data-stu-id="85441-113">This code example is part of a larger example that is provided for the <xref:System.Windows.Media.ImageBrush> class.</span></span> <span data-ttu-id="85441-114">Pour obtenir un exemple complet, consultez [ImageBrush, exemple](https://go.microsoft.com/fwlink/?LinkID=160005).</span><span class="sxs-lookup"><span data-stu-id="85441-114">For the complete sample, see [ImageBrush Sample](https://go.microsoft.com/fwlink/?LinkID=160005).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85441-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85441-115">See Also</span></span>  
 [<span data-ttu-id="85441-116">Peinture avec des images, des dessins et des objets visuels</span><span class="sxs-lookup"><span data-stu-id="85441-116">Painting with Images, Drawings, and Visuals</span></span>](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)
