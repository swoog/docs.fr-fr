---
title: "Comment : créer une image bitmap à partir d'un Visual"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: 4735474d00712598cb5e41fad289e8f568d83a48
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559764"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a>Comment : créer une image bitmap à partir d'un Visual
Cet exemple montre comment vous pouvez créer une bitmap à partir d’un <xref:System.Windows.Media.Visual>. A <xref:System.Windows.Media.DrawingVisual> est rendue avec <xref:System.Windows.Media.FormattedText>. Le <xref:System.Windows.Media.Visual> est ensuite rendu dans le <xref:System.Windows.Media.Imaging.RenderTargetBitmap> création d’une bitmap d’un texte donné.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.DrawingContext>  
 [Vue d’ensemble de la création d’images](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)  
 [Vue d’ensemble des objets de dessin](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [Utilisation d’objets DrawingVisual](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
