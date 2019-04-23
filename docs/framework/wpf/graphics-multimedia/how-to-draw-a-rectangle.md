---
title: 'Procédure : Dessiner un rectangle'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], rectangles
- graphics [WPF], rectangles
- rectangles [WPF], drawing
ms.assetid: beeb57ef-fab5-4446-a38a-1588f97b4c2f
ms.openlocfilehash: 261026b994b432565928b38ff1657115ff7cbe4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217352"
---
# <a name="how-to-draw-a-rectangle"></a>Procédure : Dessiner un rectangle
Cet exemple montre comment dessiner un rectangle à l’aide de la <xref:System.Windows.Shapes.Rectangle> élément.  
  
 Pour dessiner un rectangle, créez un <xref:System.Windows.Shapes.Rectangle> élément et spécifiez son <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A>. Pour peindre l’intérieur du rectangle, définissez son <xref:System.Windows.Shapes.Shape.Fill%2A>. Pour donner le rectangle à un plan, utilisez son <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> propriétés.  
  
 Le rectangle de donner des angles arrondis, spécifiez le paramètre facultatif <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> et <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> propriétés. Le <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> et <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> propriétés définies les rayons des axes x et y de l’ellipse utilisée pour arrondir les angles du rectangle.  
  
 Dans l’exemple suivant, deux <xref:System.Windows.Shapes.Rectangle> éléments sont dessinés un <xref:System.Windows.Controls.Canvas>. Le premier rectangle est un <xref:System.Windows.Media.Brushes.Blue%2A> intérieurs. Le deuxième rectangle a une <xref:System.Windows.Media.Brushes.Blue%2A> intérieurs, une <xref:System.Windows.Media.Brushes.Black%2A> contour et angles arrondis est utilisée.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[drawingwithshapeelements#Rectangle1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/rectangleexample.xaml#rectangle1)]  
  
 Bien que cet exemple utilise un <xref:System.Windows.Controls.Canvas> pour contenir les rectangles, vous pouvez utiliser des éléments rectangle (et toutes les autres formes) avec n’importe quel <xref:System.Windows.Controls.Panel> ou <xref:System.Windows.Controls.Control> qui prend en charge le contenu non textuel. En fait, les rectangles sont particulièrement utiles pour fournir des arrière-plans pour certaines parties de <xref:System.Windows.Controls.Grid> panneaux. Pour obtenir un exemple, consultez le [vue d’ensemble de la Table](../advanced/table-overview.md).  
  
 Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Shapes.Rectangle>
- [Exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037)
- [Vue d’ensemble des formes et dessins de base dans WPF](shapes-and-basic-drawing-in-wpf-overview.md)
- [Vue d’ensemble de Table](../advanced/table-overview.md)
