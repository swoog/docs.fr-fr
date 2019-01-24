---
title: 'Procédure : Encoder un Visual dans un fichier image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image files [WPF], encoding from visuals
- encoding image formats [WPF]
- visuals [WPF], encoding to an image file
ms.assetid: 2036385b-ea47-4d54-8027-5797f52c8149
ms.openlocfilehash: e8988256d4b7181c5e1af12252ca26e0248d016f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645221"
---
# <a name="how-to-encode-a-visual-to-an-image-file"></a><span data-ttu-id="0ad7e-102">Procédure : Encoder un Visual dans un fichier image</span><span class="sxs-lookup"><span data-stu-id="0ad7e-102">How to: Encode a Visual to an Image File</span></span>
<span data-ttu-id="0ad7e-103">Cet exemple montre comment encoder un <xref:System.Windows.Media.Visual> objet dans un fichier image en utilisant un <xref:System.Windows.Media.Imaging.RenderTargetBitmap> et un <xref:System.Windows.Media.Imaging.PngBitmapEncoder>.</span><span class="sxs-lookup"><span data-stu-id="0ad7e-103">This example demonstrates how to encode a <xref:System.Windows.Media.Visual> object into an image file using a <xref:System.Windows.Media.Imaging.RenderTargetBitmap> and a <xref:System.Windows.Media.Imaging.PngBitmapEncoder>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ad7e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ad7e-104">Example</span></span>  
 <span data-ttu-id="0ad7e-105">Le <xref:System.Windows.Media.DrawingVisual> est créé en utilisant un <xref:System.Windows.Media.Imaging.BitmapImage> et <xref:System.Windows.Media.FormattedText> qui est restitué dans un <xref:System.Windows.Media.Imaging.RenderTargetBitmap>.</span><span class="sxs-lookup"><span data-stu-id="0ad7e-105">The <xref:System.Windows.Media.DrawingVisual> is created using a <xref:System.Windows.Media.Imaging.BitmapImage> and <xref:System.Windows.Media.FormattedText> which is rendered to a <xref:System.Windows.Media.Imaging.RenderTargetBitmap>.</span></span> <span data-ttu-id="0ad7e-106">L’image bitmap affichée est ensuite utilisé pour créer un <xref:System.Windows.Media.Imaging.BitmapFrame> qui est ajouté à la <xref:System.Windows.Media.Imaging.PngBitmapEncoder> pour créer un nouveau [!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)] fichier.</span><span class="sxs-lookup"><span data-stu-id="0ad7e-106">The rendered bitmap is then used to create a <xref:System.Windows.Media.Imaging.BitmapFrame> which is added to the <xref:System.Windows.Media.Imaging.PngBitmapEncoder> to create a new [!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)] file.</span></span>  
  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample_Encode.cs#rtbencodeinline1)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample_Encode.vb#rtbencodeinline1)]  
  
 <span data-ttu-id="0ad7e-107">Un <xref:System.Windows.Media.Imaging.PngBitmapEncoder> a été utilisé dans cet exemple, mais des dérivé <xref:System.Windows.Media.Imaging.BitmapEncoder> objets pourrait avoir été utilisés pour créer le fichier image.</span><span class="sxs-lookup"><span data-stu-id="0ad7e-107">A <xref:System.Windows.Media.Imaging.PngBitmapEncoder> was used in this example but any of the derived <xref:System.Windows.Media.Imaging.BitmapEncoder> objects could have been used to create the image file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ad7e-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ad7e-108">See also</span></span>
- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="0ad7e-109">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="0ad7e-109">Imaging Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
- [<span data-ttu-id="0ad7e-110">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="0ad7e-110">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [<span data-ttu-id="0ad7e-111">Utilisation d’objets DrawingVisual</span><span class="sxs-lookup"><span data-stu-id="0ad7e-111">Using DrawingVisual Objects</span></span>](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
