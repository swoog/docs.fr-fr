---
title: 'Comment : dessiner une ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], lines
- graphics [WPF], lines
- lines [WPF], drawing
ms.assetid: 0513ee01-6b27-4bb3-85f3-3a3e6710d80e
ms.openlocfilehash: bee343676175098493df347823a3bdbdf17b205f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398443"
---
# <a name="how-to-draw-a-line"></a><span data-ttu-id="ffe71-102">Comment : dessiner une ligne</span><span class="sxs-lookup"><span data-stu-id="ffe71-102">How to: Draw a Line</span></span>
<span data-ttu-id="ffe71-103">Cet exemple vous montre comment dessiner des lignes à l’aide de la <xref:System.Windows.Shapes.Line> élément.</span><span class="sxs-lookup"><span data-stu-id="ffe71-103">This example shows you how to draw lines by using the <xref:System.Windows.Shapes.Line> element.</span></span>  
  
 <span data-ttu-id="ffe71-104">Pour dessiner une ligne, créez un <xref:System.Windows.Shapes.Line> élément.</span><span class="sxs-lookup"><span data-stu-id="ffe71-104">To draw a line, create a <xref:System.Windows.Shapes.Line> element.</span></span> <span data-ttu-id="ffe71-105">Utiliser son <xref:System.Windows.Shapes.Line.X1%2A> et <xref:System.Windows.Shapes.Line.Y1%2A> propriétés pour définir son point de départ ; et sa <xref:System.Windows.Shapes.Line.X2%2A> et <xref:System.Windows.Shapes.Line.Y2%2A> propriétés à définir son point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ffe71-105">Use its <xref:System.Windows.Shapes.Line.X1%2A> and <xref:System.Windows.Shapes.Line.Y1%2A> properties to set its start point; and use its <xref:System.Windows.Shapes.Line.X2%2A> and <xref:System.Windows.Shapes.Line.Y2%2A> properties to set its end point.</span></span> <span data-ttu-id="ffe71-106">Enfin, définissez son <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> , car une ligne sans trait est invisible.</span><span class="sxs-lookup"><span data-stu-id="ffe71-106">Finally, set its <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> because a line without a stroke is invisible.</span></span>  
  
 <span data-ttu-id="ffe71-107">Définition de la <xref:System.Windows.Shapes.Shape.Fill%2A> élément pour une ligne n’a aucun effet, car une ligne n’a aucun intérieur.</span><span class="sxs-lookup"><span data-stu-id="ffe71-107">Setting the <xref:System.Windows.Shapes.Shape.Fill%2A> element for a line has no effect, because a line has no interior.</span></span>  
  
 <span data-ttu-id="ffe71-108">L’exemple suivant dessine trois lignes dans un <xref:System.Windows.Controls.Canvas> élément.</span><span class="sxs-lookup"><span data-stu-id="ffe71-108">The following example draws three lines inside a <xref:System.Windows.Controls.Canvas> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ffe71-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ffe71-109">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#LineExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 <span data-ttu-id="ffe71-110">Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).</span><span class="sxs-lookup"><span data-stu-id="ffe71-110">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffe71-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffe71-111">See Also</span></span>  
 <xref:System.Windows.Shapes.Line>  
 [<span data-ttu-id="ffe71-112">Exemples d’éléments de forme</span><span class="sxs-lookup"><span data-stu-id="ffe71-112">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
