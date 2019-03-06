---
title: "Procédure : Utiliser un dessin comme source d'image"
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], drawings [WPF], as image sources
- image sources [WPF], drawings
- drawings [WPF], as image sources
ms.assetid: dcf71c7b-9e86-4b8e-8e39-0d0ce0389ef4
ms.openlocfilehash: 07659463a3fec9b962f7b4bb255ed065d544d954
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351734"
---
# <a name="how-to-use-a-drawing-as-an-image-source"></a><span data-ttu-id="de385-102">Procédure : Utiliser un dessin comme source d'image</span><span class="sxs-lookup"><span data-stu-id="de385-102">How to: Use a Drawing as an Image Source</span></span>
<span data-ttu-id="de385-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Drawing> en tant que le <xref:System.Windows.Controls.Image.Source%2A> pour un <xref:System.Windows.Controls.Image> contrôle.</span><span class="sxs-lookup"><span data-stu-id="de385-103">This example shows how to use a <xref:System.Windows.Media.Drawing> as the <xref:System.Windows.Controls.Image.Source%2A> for an <xref:System.Windows.Controls.Image> control.</span></span> <span data-ttu-id="de385-104">Pour afficher un <xref:System.Windows.Media.Drawing> avec un <xref:System.Windows.Controls.Image> contrôler, utilisez un <xref:System.Windows.Media.DrawingImage> en tant que le <xref:System.Windows.Controls.Image> du contrôle <xref:System.Windows.Controls.Image.Source%2A> et définir le <xref:System.Windows.Media.DrawingImage> l’objet <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> propriété sur le dessin que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="de385-104">To display a <xref:System.Windows.Media.Drawing> with an <xref:System.Windows.Controls.Image> control, use a <xref:System.Windows.Media.DrawingImage> as the <xref:System.Windows.Controls.Image> control's <xref:System.Windows.Controls.Image.Source%2A> and set the <xref:System.Windows.Media.DrawingImage> object's <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> property to the drawing you want to display.</span></span>  
  
## <a name="example"></a><span data-ttu-id="de385-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="de385-105">Example</span></span>  
 <span data-ttu-id="de385-106">L’exemple suivant utilise un <xref:System.Windows.Media.DrawingImage> et un <xref:System.Windows.Controls.Image> contrôle pour afficher un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="de385-106">The following example uses a <xref:System.Windows.Media.DrawingImage> and an <xref:System.Windows.Controls.Image> control to display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="de385-107">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="de385-107">This example produces the following output:</span></span>  
  
 <span data-ttu-id="de385-108">![GeometryDrawing de deux ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="de385-108">![A GeometryDrawing of two ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
<span data-ttu-id="de385-109">DrawingImage</span><span class="sxs-lookup"><span data-stu-id="de385-109">A DrawingImage</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="de385-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de385-110">See also</span></span>
- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="de385-111">Dessiner une image à l’aide d’ImageDrawing</span><span class="sxs-lookup"><span data-stu-id="de385-111">Draw an Image Using ImageDrawing</span></span>](how-to-draw-an-image-using-imagedrawing.md)
- [<span data-ttu-id="de385-112">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="de385-112">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="de385-113">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="de385-113">Freezable Objects Overview</span></span>](../advanced/freezable-objects-overview.md)
- [<span data-ttu-id="de385-114">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="de385-114">PresentationOptions:Freeze Attribute</span></span>](../advanced/presentationoptions-freeze-attribute.md)
