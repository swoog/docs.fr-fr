---
title: 'Procédure : Peindre une zone avec une vidéo'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- painting with a video [WPF]
- video [WPF], painting with
- brushes [WPF], painting with a video
ms.assetid: 04dd6600-4a6e-4b43-a93e-21cce7dfbcb8
ms.openlocfilehash: 0756a9e87840648b55ecad4b3f1ce6e0e5452eb7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57363291"
---
# <a name="how-to-paint-an-area-with-a-video"></a><span data-ttu-id="1970c-102">Procédure : Peindre une zone avec une vidéo</span><span class="sxs-lookup"><span data-stu-id="1970c-102">How to: Paint an Area with a Video</span></span>
<span data-ttu-id="1970c-103">Cet exemple montre comment peindre une zone avec le média.</span><span class="sxs-lookup"><span data-stu-id="1970c-103">This example shows how to paint an area with media.</span></span> <span data-ttu-id="1970c-104">Pour peindre une zone avec un média consiste à utiliser un <xref:System.Windows.Controls.MediaElement> avec un <xref:System.Windows.Media.VisualBrush>.</span><span class="sxs-lookup"><span data-stu-id="1970c-104">One way to paint an area with media is to use a <xref:System.Windows.Controls.MediaElement> together with a <xref:System.Windows.Media.VisualBrush>.</span></span> <span data-ttu-id="1970c-105">Utiliser le <xref:System.Windows.Controls.MediaElement> pour charger et lire le média, puis utilisez-le pour définir le <xref:System.Windows.Media.VisualBrush.Visual%2A> propriété de la <xref:System.Windows.Media.VisualBrush>.</span><span class="sxs-lookup"><span data-stu-id="1970c-105">Use the <xref:System.Windows.Controls.MediaElement> to load and play the media, and then use it to set the <xref:System.Windows.Media.VisualBrush.Visual%2A> property of the <xref:System.Windows.Media.VisualBrush>.</span></span> <span data-ttu-id="1970c-106">Vous pouvez ensuite utiliser le <xref:System.Windows.Media.VisualBrush> pour peindre une zone avec le média chargé.</span><span class="sxs-lookup"><span data-stu-id="1970c-106">You can then use the <xref:System.Windows.Media.VisualBrush> to paint an area with the loaded media.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1970c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="1970c-107">Example</span></span>  
 <span data-ttu-id="1970c-108">L’exemple suivant utilise un <xref:System.Windows.Controls.MediaElement> et un <xref:System.Windows.Media.VisualBrush> pour peindre le <xref:System.Windows.Controls.TextBlock.Foreground%2A> d’un <xref:System.Windows.Controls.TextBlock> contrôle avec la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1970c-108">The following example uses a <xref:System.Windows.Controls.MediaElement> and a <xref:System.Windows.Media.VisualBrush> to paint the <xref:System.Windows.Controls.TextBlock.Foreground%2A> of a <xref:System.Windows.Controls.TextBlock> control with video.</span></span> <span data-ttu-id="1970c-109">Cet exemple définit le <xref:System.Windows.Controls.MediaElement.IsMuted%2A> propriété de la <xref:System.Windows.Controls.MediaElement> à `true` afin qu’il ne produise aucun son.</span><span class="sxs-lookup"><span data-stu-id="1970c-109">This example sets the <xref:System.Windows.Controls.MediaElement.IsMuted%2A> property of the <xref:System.Windows.Controls.MediaElement> to `true` so that it produces no sound.</span></span>  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundinline)]  
  
## <a name="example"></a><span data-ttu-id="1970c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1970c-110">Example</span></span>  
 <span data-ttu-id="1970c-111">Étant donné que <xref:System.Windows.Media.VisualBrush> hérite le <xref:System.Windows.Media.TileBrush> (classe), il fournit plusieurs modes de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1970c-111">Because <xref:System.Windows.Media.VisualBrush> inherits from the <xref:System.Windows.Media.TileBrush> class, it provides several tiling modes.</span></span> <span data-ttu-id="1970c-112">En définissant le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété d’un <xref:System.Windows.Media.VisualBrush> à <xref:System.Windows.Media.TileMode.Tile> et en définissant son <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété à une valeur inférieure à la zone que vous peignez, vous pouvez créer un modèle en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1970c-112">By setting the <xref:System.Windows.Media.TileBrush.TileMode%2A> property of a <xref:System.Windows.Media.VisualBrush> to <xref:System.Windows.Media.TileMode.Tile> and by setting its <xref:System.Windows.Media.TileBrush.Viewport%2A> property to a value smaller than the area that you are painting, you can create a tiled pattern.</span></span>  
  
 <span data-ttu-id="1970c-113">L’exemple suivant est identique à l’exemple précédent, à ceci près que le <xref:System.Windows.Media.VisualBrush> génère un modèle à partir de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="1970c-113">The following example is identical to the previous example, except that the <xref:System.Windows.Media.VisualBrush> generates a pattern from the video.</span></span>  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundtiledinline)]  
  
 <span data-ttu-id="1970c-114">Pour plus d’informations sur l’ajout d’un fichier de contenu, tel qu’un fichier multimédia, à votre application, consultez [ressource d’Application WPF, de contenu et de fichiers de données](../app-development/wpf-application-resource-content-and-data-files.md).</span><span class="sxs-lookup"><span data-stu-id="1970c-114">For information about how to add a content file, such as a media file, to your application, see [WPF Application Resource, Content, and Data Files](../app-development/wpf-application-resource-content-and-data-files.md).</span></span> <span data-ttu-id="1970c-115">Lorsque vous ajoutez un fichier multimédia, vous devez l’ajouter en tant qu’un fichier de contenu, et non comme un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="1970c-115">When you add a media file, you must add it as a content file, not as a resource file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1970c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1970c-116">See also</span></span>
- <xref:System.Windows.Media.VisualBrush>
- [<span data-ttu-id="1970c-117">Peinture avec des images, des dessins et des objets visuels</span><span class="sxs-lookup"><span data-stu-id="1970c-117">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
- [<span data-ttu-id="1970c-118">Vue d’ensemble de TileBrush</span><span class="sxs-lookup"><span data-stu-id="1970c-118">TileBrush Overview</span></span>](tilebrush-overview.md)
- [<span data-ttu-id="1970c-119">Vue d’ensemble multimédia</span><span class="sxs-lookup"><span data-stu-id="1970c-119">Multimedia Overview</span></span>](multimedia-overview.md)
