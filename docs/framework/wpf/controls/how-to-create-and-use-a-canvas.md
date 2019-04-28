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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000998"
---
# <a name="how-to-create-and-use-a-canvas"></a><span data-ttu-id="61120-102">Procédure : Créer et utiliser un canevas</span><span class="sxs-lookup"><span data-stu-id="61120-102">How to: Create and Use a Canvas</span></span>
<span data-ttu-id="61120-103">Cet exemple montre comment créer et utiliser une instance de <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="61120-103">This example shows how to create and use an instance of <xref:System.Windows.Controls.Canvas>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="61120-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="61120-104">Example</span></span>  
 <span data-ttu-id="61120-105">L’exemple suivant positionne explicitement deux <xref:System.Windows.Controls.TextBlock> éléments à l’aide de la <xref:System.Windows.Controls.Canvas.SetTop%2A> et <xref:System.Windows.Controls.Canvas.SetLeft%2A> méthodes de <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="61120-105">The following example explicitly positions two <xref:System.Windows.Controls.TextBlock> elements by using the <xref:System.Windows.Controls.Canvas.SetTop%2A> and <xref:System.Windows.Controls.Canvas.SetLeft%2A> methods of <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="61120-106">L’exemple affecte également un <xref:System.Windows.Controls.Control.Background%2A> couleur de `LightSteelBlue` à la <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="61120-106">The example also assigns a <xref:System.Windows.Controls.Control.Background%2A> color of `LightSteelBlue` to the <xref:System.Windows.Controls.Canvas>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="61120-107">Lorsque vous utilisez [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] à la position <xref:System.Windows.Controls.TextBlock> éléments, utilisez le <xref:System.Windows.Controls.Canvas.Top%2A> et <xref:System.Windows.Controls.Canvas.Left%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="61120-107">When you use [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to position <xref:System.Windows.Controls.TextBlock> elements, use the <xref:System.Windows.Controls.Canvas.Top%2A> and <xref:System.Windows.Controls.Canvas.Left%2A> properties.</span></span>  
  
 [!code-csharp[CanvasCode#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="61120-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61120-108">See also</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.TextBlock>
- <xref:System.Windows.Controls.Canvas.SetTop%2A>
- <xref:System.Windows.Controls.Canvas.SetLeft%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- [<span data-ttu-id="61120-109">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="61120-109">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="61120-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="61120-110">How-to Topics</span></span>](canvas-how-to-topics.md)
