---
title: 'Procédure : Utiliser un dessin comme source d’image'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], drawings [WPF], as image sources
- image sources [WPF], drawings
- drawings [WPF], as image sources
ms.assetid: dcf71c7b-9e86-4b8e-8e39-0d0ce0389ef4
ms.openlocfilehash: d4b91a6495e1c54400d5fbfe43b6311d908565a7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769357"
---
# <a name="how-to-use-a-drawing-as-an-image-source"></a><span data-ttu-id="cfb4f-102">Procédure : Utiliser un dessin comme source d’image</span><span class="sxs-lookup"><span data-stu-id="cfb4f-102">How to: Use a Drawing as an Image Source</span></span>
<span data-ttu-id="cfb4f-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Drawing> en tant que le <xref:System.Windows.Controls.Image.Source%2A> pour un <xref:System.Windows.Controls.Image> contrôle.</span><span class="sxs-lookup"><span data-stu-id="cfb4f-103">This example shows how to use a <xref:System.Windows.Media.Drawing> as the <xref:System.Windows.Controls.Image.Source%2A> for an <xref:System.Windows.Controls.Image> control.</span></span> <span data-ttu-id="cfb4f-104">Pour afficher un <xref:System.Windows.Media.Drawing> avec un <xref:System.Windows.Controls.Image> contrôler, utilisez un <xref:System.Windows.Media.DrawingImage> en tant que le <xref:System.Windows.Controls.Image> du contrôle <xref:System.Windows.Controls.Image.Source%2A> et définir le <xref:System.Windows.Media.DrawingImage> l’objet <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> propriété sur le dessin que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="cfb4f-104">To display a <xref:System.Windows.Media.Drawing> with an <xref:System.Windows.Controls.Image> control, use a <xref:System.Windows.Media.DrawingImage> as the <xref:System.Windows.Controls.Image> control's <xref:System.Windows.Controls.Image.Source%2A> and set the <xref:System.Windows.Media.DrawingImage> object's <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> property to the drawing you want to display.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfb4f-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="cfb4f-105">Example</span></span>  
 <span data-ttu-id="cfb4f-106">L’exemple suivant utilise un <xref:System.Windows.Media.DrawingImage> et un <xref:System.Windows.Controls.Image> contrôle pour afficher un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="cfb4f-106">The following example uses a <xref:System.Windows.Media.DrawingImage> and an <xref:System.Windows.Controls.Image> control to display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="cfb4f-107">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="cfb4f-107">This example produces the following output:</span></span>  
  
 <span data-ttu-id="cfb4f-108">![GeometryDrawing de deux ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="cfb4f-108">![A GeometryDrawing of two ellipses](./media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
<span data-ttu-id="cfb4f-109">DrawingImage</span><span class="sxs-lookup"><span data-stu-id="cfb4f-109">A DrawingImage</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="cfb4f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb4f-110">See also</span></span>

- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="cfb4f-111">Dessiner une image à l’aide d’ImageDrawing</span><span class="sxs-lookup"><span data-stu-id="cfb4f-111">Draw an Image Using ImageDrawing</span></span>](how-to-draw-an-image-using-imagedrawing.md)
- [<span data-ttu-id="cfb4f-112">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="cfb4f-112">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="cfb4f-113">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="cfb4f-113">Freezable Objects Overview</span></span>](../advanced/freezable-objects-overview.md)
- [<span data-ttu-id="cfb4f-114">PresentationOptions:Freeze, attribut</span><span class="sxs-lookup"><span data-stu-id="cfb4f-114">PresentationOptions:Freeze Attribute</span></span>](../advanced/presentationoptions-freeze-attribute.md)
