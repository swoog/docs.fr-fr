---
title: 'Procédure : Dessiner une image à l’aide d’ImageDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], images
- graphics [WPF], drawing images
- images [WPF], drawing
ms.assetid: df28ab41-25fb-4ab3-b51d-7f695b24f55e
ms.openlocfilehash: f9459185bf81160b45222e7d6821e0f945ada381
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59100156"
---
# <a name="how-to-draw-an-image-using-imagedrawing"></a>Procédure : Dessiner une image à l’aide d’ImageDrawing
Cet exemple montre comment utiliser un <xref:System.Windows.Media.ImageDrawing> pour dessiner une image. Un <xref:System.Windows.Media.ImageDrawing> vous permet d’afficher un <xref:System.Windows.Media.ImageSource> avec un <xref:System.Windows.Media.DrawingBrush>, <xref:System.Windows.Media.DrawingImage>, ou <xref:System.Windows.Media.Visual>. Pour dessiner une image, vous créez un <xref:System.Windows.Media.ImageDrawing> et définissez son <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> et <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> propriétés. Le <xref:System.Windows.Media.ImageDrawing.ImageSource%2A?displayProperty=nameWithType> propriété spécifie l’image à dessiner et le <xref:System.Windows.Media.ImageDrawing.Rect%2A?displayProperty=nameWithType> propriété spécifie la position et la taille de chaque image.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un dessin composite à l’aide de quatre <xref:System.Windows.Media.ImageDrawing> objets. Cet exemple génère l’image suivante :  
  
 ![Plusieurs objets DrawingImage](./media/graphicsmm-imagedrawingexample.jpg "graphicsmm_ImageDrawingExample")  
Quatre objets ImageDrawing  
  
 [!code-csharp[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/ImageDrawingExample.cs#imagedrawingexample)]
 [!code-xaml[DrawingMiscSnippets_snip#ImageDrawingExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/ImageDrawingExample.xaml#imagedrawingexample)]  
  
 Pour obtenir un exemple montrant un moyen simple pour afficher une image sans utiliser <xref:System.Windows.Media.ImageDrawing>, consultez [utiliser l’élément Image](../controls/how-to-use-the-image-element.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Freezable.Freeze%2A>
- <xref:System.Windows.Controls.Image>
- [Vue d'ensemble des objets Drawing](drawing-objects-overview.md)
- [Vue d'ensemble des objets Freezable](../advanced/freezable-objects-overview.md)
- [PresentationOptions:Freeze, attribut](../advanced/presentationoptions-freeze-attribute.md)
