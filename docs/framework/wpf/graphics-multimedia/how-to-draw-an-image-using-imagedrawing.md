---
title: "Procédure : Dessiner une image à l'aide d'ImageDrawing"
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], images
- graphics [WPF], drawing images
- images [WPF], drawing
ms.assetid: df28ab41-25fb-4ab3-b51d-7f695b24f55e
ms.openlocfilehash: 9a9a7ee32104e44997e6eaada09edaac2b1d610e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355592"
---
# <a name="how-to-draw-an-image-using-imagedrawing"></a><span data-ttu-id="0ea7f-102">Procédure : Dessiner une image à l'aide d'ImageDrawing</span><span class="sxs-lookup"><span data-stu-id="0ea7f-102">How to: Draw an Image Using ImageDrawing</span></span>
<span data-ttu-id="0ea7f-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.ImageDrawing> pour dessiner une image.</span><span class="sxs-lookup"><span data-stu-id="0ea7f-103">This example shows how to use an <xref:System.Windows.Media.ImageDrawing> to draw an image.</span></span> <span data-ttu-id="0ea7f-104">Un <xref:System.Windows.Media.ImageDrawing> vous permet d’afficher un <xref:System.Windows.Media.ImageSource> avec un <xref:System.Windows.Media.DrawingBrush>, <xref:System.Windows.Media.DrawingImage>, ou <xref:System.Windows.Media.Visual>.</span><span class="sxs-lookup"><span data-stu-id="0ea7f-104">An <xref:System.Windows.Media.ImageDrawing> enables you display an <xref:System.Windows.Media.ImageSource> with a <xref:System.Windows.Media.DrawingBrush>, <xref:System.Windows.Media.DrawingImage>, or <xref:System.Windows.Media.Visual>.</span></span> <span data-ttu-id="0ea7f-105">Pour dessiner une image, vous créez un <xref:System.Windows.Media.ImageDrawing> et définissez son <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> et <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ea7f-105">To draw an image, you create an <xref:System.Windows.Media.ImageDrawing> and set its <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> and <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> properties.</span></span> <span data-ttu-id="0ea7f-106">Le <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> propriété spécifie l’image à dessiner et le <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> propriété spécifie la position et la taille de chaque image.</span><span class="sxs-lookup"><span data-stu-id="0ea7f-106">The <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> property specifies the image to draw, and the <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> property specifies the position and size of each image.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ea7f-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ea7f-107">Example</span></span>  
 <span data-ttu-id="0ea7f-108">L’exemple suivant crée un dessin composite à l’aide de quatre <xref:System.Windows.Media.ImageDrawing> objets.</span><span class="sxs-lookup"><span data-stu-id="0ea7f-108">The following example creates a composite drawing using four <xref:System.Windows.Media.ImageDrawing> objects.</span></span> <span data-ttu-id="0ea7f-109">Cet exemple génère l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="0ea7f-109">This example produces the following image:</span></span>  
  
 <span data-ttu-id="0ea7f-110">![Plusieurs objets DrawingImage](./media/graphicsmm-imagedrawingexample.jpg "graphicsmm_ImageDrawingExample")</span><span class="sxs-lookup"><span data-stu-id="0ea7f-110">![Several DrawingImage objects](./media/graphicsmm-imagedrawingexample.jpg "graphicsmm_ImageDrawingExample")</span></span>  
<span data-ttu-id="0ea7f-111">Quatre objets ImageDrawing</span><span class="sxs-lookup"><span data-stu-id="0ea7f-111">Four ImageDrawing objects</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/ImageDrawingExample.cs#imagedrawingexample)]
 [!code-xaml[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/ImageDrawingExample.xaml#imagedrawingexample)]  
  
 <span data-ttu-id="0ea7f-112">Pour obtenir un exemple montrant un moyen simple pour afficher une image sans utiliser <xref:System.Windows.Media.ImageDrawing>, consultez [utiliser l’élément Image](../controls/how-to-use-the-image-element.md).</span><span class="sxs-lookup"><span data-stu-id="0ea7f-112">For an example showing a simple way to display an image without using <xref:System.Windows.Media.ImageDrawing>, see [Use the Image Element](../controls/how-to-use-the-image-element.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ea7f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea7f-113">See also</span></span>
- <xref:System.Windows.Freezable.Freeze%2A>
- <xref:System.Windows.Controls.Image>
- [<span data-ttu-id="0ea7f-114">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="0ea7f-114">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="0ea7f-115">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="0ea7f-115">Freezable Objects Overview</span></span>](../advanced/freezable-objects-overview.md)
- [<span data-ttu-id="0ea7f-116">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="0ea7f-116">PresentationOptions:Freeze Attribute</span></span>](../advanced/presentationoptions-freeze-attribute.md)
