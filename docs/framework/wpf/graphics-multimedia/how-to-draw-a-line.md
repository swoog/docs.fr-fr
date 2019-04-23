---
title: 'Procédure : Dessiner une ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], lines
- graphics [WPF], lines
- lines [WPF], drawing
ms.assetid: 0513ee01-6b27-4bb3-85f3-3a3e6710d80e
ms.openlocfilehash: c11dfb9523834ec2e622cb2e62bd6982a1a78fd4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143518"
---
# <a name="how-to-draw-a-line"></a><span data-ttu-id="efecc-102">Procédure : Dessiner une ligne</span><span class="sxs-lookup"><span data-stu-id="efecc-102">How to: Draw a Line</span></span>
<span data-ttu-id="efecc-103">Cet exemple vous montre comment dessiner des lignes à l’aide de la <xref:System.Windows.Shapes.Line> élément.</span><span class="sxs-lookup"><span data-stu-id="efecc-103">This example shows you how to draw lines by using the <xref:System.Windows.Shapes.Line> element.</span></span>  
  
 <span data-ttu-id="efecc-104">Pour dessiner une ligne, créez un <xref:System.Windows.Shapes.Line> élément.</span><span class="sxs-lookup"><span data-stu-id="efecc-104">To draw a line, create a <xref:System.Windows.Shapes.Line> element.</span></span> <span data-ttu-id="efecc-105">Utiliser son <xref:System.Windows.Shapes.Line.X1%2A> et <xref:System.Windows.Shapes.Line.Y1%2A> propriétés pour définir son point de départ ; et sa <xref:System.Windows.Shapes.Line.X2%2A> et <xref:System.Windows.Shapes.Line.Y2%2A> propriétés à définir son point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="efecc-105">Use its <xref:System.Windows.Shapes.Line.X1%2A> and <xref:System.Windows.Shapes.Line.Y1%2A> properties to set its start point; and use its <xref:System.Windows.Shapes.Line.X2%2A> and <xref:System.Windows.Shapes.Line.Y2%2A> properties to set its end point.</span></span> <span data-ttu-id="efecc-106">Enfin, définissez son <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> , car une ligne sans trait est invisible.</span><span class="sxs-lookup"><span data-stu-id="efecc-106">Finally, set its <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> because a line without a stroke is invisible.</span></span>  
  
 <span data-ttu-id="efecc-107">Définition de la <xref:System.Windows.Shapes.Shape.Fill%2A> élément pour une ligne n’a aucun effet, car une ligne n’a aucun intérieur.</span><span class="sxs-lookup"><span data-stu-id="efecc-107">Setting the <xref:System.Windows.Shapes.Shape.Fill%2A> element for a line has no effect, because a line has no interior.</span></span>  
  
 <span data-ttu-id="efecc-108">L’exemple suivant dessine trois lignes dans un <xref:System.Windows.Controls.Canvas> élément.</span><span class="sxs-lookup"><span data-stu-id="efecc-108">The following example draws three lines inside a <xref:System.Windows.Controls.Canvas> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="efecc-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="efecc-109">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#LineExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 <span data-ttu-id="efecc-110">Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).</span><span class="sxs-lookup"><span data-stu-id="efecc-110">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efecc-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efecc-111">See also</span></span>

- <xref:System.Windows.Shapes.Line>
- [<span data-ttu-id="efecc-112">Exemples d’éléments de forme</span><span class="sxs-lookup"><span data-stu-id="efecc-112">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
