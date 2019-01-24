---
title: 'Procédure : Dessiner une ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], lines
- graphics [WPF], lines
- lines [WPF], drawing
ms.assetid: 0513ee01-6b27-4bb3-85f3-3a3e6710d80e
ms.openlocfilehash: 54152b6b68dd453c565afa2ffb23edfe8132a441
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629018"
---
# <a name="how-to-draw-a-line"></a>Procédure : Dessiner une ligne
Cet exemple vous montre comment dessiner des lignes à l’aide de la <xref:System.Windows.Shapes.Line> élément.  
  
 Pour dessiner une ligne, créez un <xref:System.Windows.Shapes.Line> élément. Utiliser son <xref:System.Windows.Shapes.Line.X1%2A> et <xref:System.Windows.Shapes.Line.Y1%2A> propriétés pour définir son point de départ ; et sa <xref:System.Windows.Shapes.Line.X2%2A> et <xref:System.Windows.Shapes.Line.Y2%2A> propriétés à définir son point de terminaison. Enfin, définissez son <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> , car une ligne sans trait est invisible.  
  
 Définition de la <xref:System.Windows.Shapes.Shape.Fill%2A> élément pour une ligne n’a aucun effet, car une ligne n’a aucun intérieur.  
  
 L’exemple suivant dessine trois lignes dans un <xref:System.Windows.Controls.Canvas> élément.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[drawingwithshapeelements#LineExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/lineexample.xaml#lineexample1)]  
  
 Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Shapes.Line>
- [Exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037)
