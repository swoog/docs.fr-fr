---
title: 'Procédure : Créer différents modèles de mosaïque avec un TileBrush'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], creating tile patterns
- tile patterns [WPF], creating
- creating [WPF], tile patterns with TileBrush
ms.assetid: 5aa46632-3527-4668-9d8d-0375c8af28aa
ms.openlocfilehash: c1051b234961eee9ae740af2abac3d64c523656c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227403"
---
# <a name="how-to-create-different-tile-patterns-with-a-tilebrush"></a>Procédure : Créer différents modèles de mosaïque avec un TileBrush
Cet exemple montre comment utiliser le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété d’un <xref:System.Windows.Media.TileBrush> pour créer un modèle.  
  
 Le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété vous permet de spécifier comment le contenu d’un <xref:System.Windows.Media.TileBrush> est répété, autrement dit, en mosaïque pour remplir une zone de sortie. Pour créer un modèle, vous définissez le <xref:System.Windows.Media.TileBrush.TileMode%2A> à <xref:System.Windows.Media.TileMode.Tile>, <xref:System.Windows.Media.TileMode.FlipX>, <xref:System.Windows.Media.TileMode.FlipY>, ou <xref:System.Windows.Media.TileMode.FlipXY>. Vous devez également définir le <xref:System.Windows.Media.TileBrush.Viewport%2A> de la <xref:System.Windows.Media.TileBrush> afin qu’elle soit inférieure à la zone que vous peignez ; sinon, qu’une seule vignette est produite, quel que soit ce qui <xref:System.Windows.Media.TileBrush.TileMode%2A> paramètre que vous utilisez.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée cinq <xref:System.Windows.Media.DrawingBrush> des objets, leur donne chaque une autre <xref:System.Windows.Media.TileBrush.TileMode%2A> définition et les utilise pour peindre cinq rectangles. Bien que cet exemple utilise le <xref:System.Windows.Media.DrawingBrush> classe afin d’illustrer <xref:System.Windows.Media.TileBrush.TileMode%2A> comportement, le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété fonctionne de manière identique pour tous les le <xref:System.Windows.Media.TileBrush> d’objets, autrement dit, pour <xref:System.Windows.Media.ImageBrush>, <xref:System.Windows.Media.VisualBrush>, et <xref:System.Windows.Media.DrawingBrush>.  
  
 L’illustration suivante montre la sortie que l’exemple génère.  
  
 ![Exemple de sortie de la mosaïque de TileBrush](./media/graphicsmm-drawingbrushtilemodeexample.png "graphicsmm_DrawingBrushTileModeExample")  
Les modèles créés avec la propriété TileMode de mosaïque  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/TileModeExample.cs#graphicsmmdrawingbrushtilemodeexample)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/tilemodeexample.vb#graphicsmmdrawingbrushtilemodeexample)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMDrawingBrushTileModeExample](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/TileModeExample.xaml#graphicsmmdrawingbrushtilemodeexample)]  
  
## <a name="see-also"></a>Voir aussi

- [Définir la taille de la mosaïque pour un TileBrush](how-to-set-the-tile-size-for-a-tilebrush.md)
- [Peinture avec des objets d'image, de dessin et visuels](painting-with-images-drawings-and-visuals.md)
