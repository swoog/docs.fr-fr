---
title: 'Procédure : Créer une image bitmap à partir d’un visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: a622d99f7c477f8654526ed399f1eb37288682fe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189875"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a>Procédure : Créer une image bitmap à partir d’un visuel
Cet exemple montre comment vous pouvez créer une image bitmap à partir d’un <xref:System.Windows.Media.Visual>. Un <xref:System.Windows.Media.DrawingVisual> est rendue avec <xref:System.Windows.Media.FormattedText>. Le <xref:System.Windows.Media.Visual> est ensuite rendu dans le <xref:System.Windows.Media.Imaging.RenderTargetBitmap> création d’une bitmap d’un texte donné.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.DrawingContext>
- [Vue d’ensemble de la création d’images](imaging-overview.md)
- [Vue d’ensemble des objets de dessin](drawing-objects-overview.md)
- [Utilisation d’objets DrawingVisual](using-drawingvisual-objects.md)
