---
title: 'Procédure : Créer un dessin composite'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], composite
- composite drawings [WPF]
- graphics [WPF], composite drawings
ms.assetid: 066eb0ab-5f0e-439d-85c6-dca60af269fc
ms.openlocfilehash: 0af7fbca593627ebe8cd102a02617a27eac50aa5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61909982"
---
# <a name="how-to-create-a-composite-drawing"></a>Procédure : Créer un dessin composite
Cet exemple montre comment utiliser un <xref:System.Windows.Media.DrawingGroup> pour créer des dessins complexes en combinant plusieurs <xref:System.Windows.Media.Drawing> objets en un seul dessin composite.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.DrawingGroup> pour créer un dessin composite à partir du <xref:System.Windows.Media.GeometryDrawing> et <xref:System.Windows.Media.ImageDrawing> objets. L’illustration suivante montre la sortie que l’exemple génère.  
  
 ![DrawingGroup avec plusieurs dessins](./media/graphicsmm-simple.jpg "graphicsmm_simple")  
Un dessin composite qui est créé à l’aide de DrawingGroup  
  
 Notez la bordure grise, qui affiche les limites du dessin.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmsimpledrawinggroupexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMSimpleDrawingGroupExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmsimpledrawinggroupexample)]  
  
 Vous pouvez utiliser un <xref:System.Windows.Media.DrawingGroup> pour appliquer un <xref:System.Windows.Media.DrawingGroup.Transform%2A>, <xref:System.Windows.Media.DrawingGroup.Opacity%2A> définition, <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A>, <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A>, <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>, ou <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> aux dessins qu’il contient. Étant donné qu’un <xref:System.Windows.Media.DrawingGroup> est également un <xref:System.Windows.Media.Drawing>, il peut contenir d’autres <xref:System.Windows.Media.DrawingGroup> objets.  
  
 L’exemple suivant est similaire à l’exemple précédent, sauf qu’elle utilise supplémentaires <xref:System.Windows.Media.DrawingGroup> objets à appliquer des effets bitmap et un masque d’opacité à certains dessins. L’illustration suivante montre la sortie que l’exemple génère.  
  
 ![DrawingGroup avec plusieurs dessins](./media/graphicsmm-multiple.jpg "graphicsmm_multiple")  
Dessin composite qui contient plusieurs objets DrawingGroup  
  
 Notez la bordure grise, qui affiche les limites du dessin.  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupExample.cs#graphicsmmmultipledrawinggroupsexample)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMMultipleDrawingGroupsExample](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupExample.xaml#graphicsmmmultipledrawinggroupsexample)]  
  
 Pour plus d’informations sur <xref:System.Windows.Media.Drawing> , consultez [vue d’ensemble des objets Drawing](drawing-objects-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.DrawingGroup.BitmapEffect%2A>
- <xref:System.Windows.Media.DrawingGroup.Transform%2A>
- <xref:System.Windows.Media.DrawingGroup.OpacityMask%2A>
- <xref:System.Windows.Media.DrawingGroup.Opacity%2A>
- <xref:System.Windows.Media.DrawingGroup.ClipGeometry%2A>
- <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A>
- [Vue d’ensemble des objets de dessin](drawing-objects-overview.md)
