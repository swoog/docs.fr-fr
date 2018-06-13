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
# <a name="how-to-use-a-drawing-as-an-image-source"></a>Comment : utiliser un dessin comme source d'image
Cet exemple montre comment utiliser un <xref:System.Windows.Media.Drawing> comme le <xref:System.Windows.Controls.Image.Source%2A> pour un <xref:System.Windows.Controls.Image> contrôle. Pour afficher un <xref:System.Windows.Media.Drawing> avec un <xref:System.Windows.Controls.Image> contrôler, utilisez un <xref:System.Windows.Media.DrawingImage> comme le <xref:System.Windows.Controls.Image> du contrôle <xref:System.Windows.Controls.Image.Source%2A> et définir le <xref:System.Windows.Media.DrawingImage> l’objet <xref:System.Windows.Media.DrawingImage.Drawing%2A?displayProperty=nameWithType> propriété au dessin que vous souhaitez afficher.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.DrawingImage> et un <xref:System.Windows.Controls.Image> contrôle pour afficher un <xref:System.Windows.Media.GeometryDrawing>. Cet exemple génère la sortie suivante :  
  
 ![GeometryDrawing de deux ellipses](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")  
DrawingImage  
  
 [!code-csharp[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingImageExample.cs#drawingimageexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#DrawingImageExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingImageExample.xaml#drawingimageexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Freezable.Freeze%2A>  
 [Dessiner une image à l’aide d’ImageDrawing](../../../../docs/framework/wpf/graphics-multimedia/how-to-draw-an-image-using-imagedrawing.md)  
 [Vue d’ensemble des objets de dessin](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [Vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)  
 [PresentationOptions:Freeze, attribut](../../../../docs/framework/wpf/advanced/presentationoptions-freeze-attribute.md)
