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
# <a name="how-to-encode-a-visual-to-an-image-file"></a>Procédure : Encoder un Visual dans un fichier image
Cet exemple montre comment encoder un <xref:System.Windows.Media.Visual> objet dans un fichier image en utilisant un <xref:System.Windows.Media.Imaging.RenderTargetBitmap> et un <xref:System.Windows.Media.Imaging.PngBitmapEncoder>.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Media.DrawingVisual> est créé en utilisant un <xref:System.Windows.Media.Imaging.BitmapImage> et <xref:System.Windows.Media.FormattedText> qui est restitué dans un <xref:System.Windows.Media.Imaging.RenderTargetBitmap>. L’image bitmap affichée est ensuite utilisé pour créer un <xref:System.Windows.Media.Imaging.BitmapFrame> qui est ajouté à la <xref:System.Windows.Media.Imaging.PngBitmapEncoder> pour créer un nouveau [!INCLUDE[TLA#tla_png](../../../../includes/tlasharptla-png-md.md)] fichier.  
  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample_Encode.cs#rtbencodeinline1)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#RTBEncodeInline1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample_Encode.vb#rtbencodeinline1)]  
  
 Un <xref:System.Windows.Media.Imaging.PngBitmapEncoder> a été utilisé dans cet exemple, mais des dérivé <xref:System.Windows.Media.Imaging.BitmapEncoder> objets pourrait avoir été utilisés pour créer le fichier image.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.DrawingContext>
- [Vue d’ensemble de la création d’images](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)
- [Vue d’ensemble des objets de dessin](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [Utilisation d’objets DrawingVisual](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
