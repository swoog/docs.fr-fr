---
title: "Comment : utiliser un dessin comme source d'image"
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], drawings [WPF], as image sources
- image sources [WPF], drawings
- drawings [WPF], as image sources
ms.assetid: dcf71c7b-9e86-4b8e-8e39-0d0ce0389ef4
ms.openlocfilehash: 7da8a2a594b0562667aaf417d736159d98818a63
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33562284"
---
# <a name="how-to-use-a-drawing-as-an-image-source"></a><span data-ttu-id="78250-102">Comment : utiliser un dessin comme source d'image</span><span class="sxs-lookup"><span data-stu-id="78250-102">How to: Use a Drawing as an Image Source</span></span>
<span data-ttu-id="78250-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Drawing> comme le <xref:System.Windows.Controls.Image.Source%2A> pour un <xref:System.Windows.Controls.Image> contrôle.</span><span class="sxs-lookup"><span data-stu-id="78250-103">This example shows how to use a <xref:System.Windows.Media.Drawing> as the <xref:System.Windows.Controls.Image.Source%2A> for an <xref:System.Windows.Controls.Image> control.</span></span> <span data-ttu-id="78250-104">Pour afficher un <xref:System.Windows.Media.Drawing> avec un <xref:System.Windows.Controls.Image> contrôler, utilisez un <xref:System.Windows.Media.DrawingImage> comme le <xref:System.Windows.Controls.Image> du contrôle <xref:System.Windows.Controls.Image.Source%2A> et définir le <xref:System.Windows.Media.DrawingImage> l’objet <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> propriété au dessin que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="78250-104">To display a <xref:System.Windows.Media.Drawing> with an <xref:System.Windows.Controls.Image> control, use a <xref:System.Windows.Media.DrawingImage> as the <xref:System.Windows.Controls.Image> control's <xref:System.Windows.Controls.Image.Source%2A> and set the <xref:System.Windows.Media.DrawingImage> object's <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> property to the drawing you want to display.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78250-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="78250-105">Example</span></span>  
 <span data-ttu-id="78250-106">L’exemple suivant utilise un <xref:System.Windows.Media.DrawingImage> et un <xref:System.Windows.Controls.Image> contrôle pour afficher un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="78250-106">The following example uses a <xref:System.Windows.Media.DrawingImage> and an <xref:System.Windows.Controls.Image> control to display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="78250-107">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="78250-107">This example produces the following output:</span></span>  
  
 <span data-ttu-id="78250-108">![GeometryDrawing de deux ellipses](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="78250-108">![A GeometryDrawing of two ellipses](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
<span data-ttu-id="78250-109">DrawingImage</span><span class="sxs-lookup"><span data-stu-id="78250-109">A DrawingImage</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="78250-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78250-110">See Also</span></span>  
 <xref:System.Windows.Freezable.Freeze%2A>  
 [<span data-ttu-id="78250-111">Dessiner une image à l’aide d’ImageDrawing</span><span class="sxs-lookup"><span data-stu-id="78250-111">Draw an Image Using ImageDrawing</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-draw-an-image-using-imagedrawing.md)  
 [<span data-ttu-id="78250-112">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="78250-112">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [<span data-ttu-id="78250-113">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="78250-113">Freezable Objects Overview</span></span>](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)  
 [<span data-ttu-id="78250-114">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="78250-114">PresentationOptions:Freeze Attribute</span></span>](../../../../docs/framework/wpf/advanced/presentationoptions-freeze-attribute.md)
