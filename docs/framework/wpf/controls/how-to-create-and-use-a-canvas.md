---
title: 'Procédure : Créer et utiliser un canevas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Canvas
- Canvas control [WPF], creating
- Canvas control [WPF], using
ms.assetid: 420b9487-9a15-477c-9489-a22a4dec7779
ms.openlocfilehash: 33b98024699a88f56d27b7e5ab8d5216c906e7ec
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59190767"
---
# <a name="how-to-create-and-use-a-canvas"></a>Procédure : Créer et utiliser un canevas
Cet exemple montre comment créer et utiliser une instance de <xref:System.Windows.Controls.Canvas>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant positionne explicitement deux <xref:System.Windows.Controls.TextBlock> éléments à l’aide de la <xref:System.Windows.Controls.Canvas.SetTop%2A> et <xref:System.Windows.Controls.Canvas.SetLeft%2A> méthodes de <xref:System.Windows.Controls.Canvas>. L’exemple affecte également un <xref:System.Windows.Controls.Control.Background%2A> couleur de `LightSteelBlue` à la <xref:System.Windows.Controls.Canvas>.  
  
> [!NOTE]
>  Lorsque vous utilisez [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] à la position <xref:System.Windows.Controls.TextBlock> éléments, utilisez le <xref:System.Windows.Controls.Canvas.Top%2A> et <xref:System.Windows.Controls.Canvas.Left%2A> propriétés.  
  
 [!code-csharp[CanvasCode#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.TextBlock>
- <xref:System.Windows.Controls.Canvas.SetTop%2A>
- <xref:System.Windows.Controls.Canvas.SetLeft%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- [Vue d'ensemble de Panel](panels-overview.md)
- [Rubriques Comment](canvas-how-to-topics.md)
