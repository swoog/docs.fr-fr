---
title: 'Procédure : Modifier l’extrémité de fin d’une ligne ou d’un segment'
ms.date: 03/30/2017
helpviewer_keywords:
- Shape elements [WPF], ends
- Shape elements [WPF], caps
- graphics [WPF], Shape caps
ms.assetid: f4bf3416-b3d8-4568-b98e-3eda8f6dbf7a
ms.openlocfilehash: 462e32520393a1c23809cce8eb3c130c13bc882f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59977669"
---
# <a name="how-to-modify-the-cap-at-the-end-of-a-line-or-segment"></a>Procédure : Modifier l’extrémité de fin d’une ligne ou d’un segment
Cet exemple montre comment modifier la forme au début ou à la fin d’une ouverture <xref:System.Windows.Shapes.Shape> élément. Pour modifier l’embout au début d’une ouverture <xref:System.Windows.Shapes.Shape>, utilisez son <xref:System.Windows.Shapes.Shape.StrokeStartLineCap%2A> propriété. Pour modifier l’embout à la fin d’une ouverture <xref:System.Windows.Shapes.Shape>, utilisez son <xref:System.Windows.Shapes.Shape.StrokeEndLineCap%2A> propriété. Pour afficher les embouts de ligne disponibles, consultez le <xref:System.Windows.Media.PenLineCap> énumération.  
  
> [!NOTE]
>  Cette propriété affecte uniquement une forme ouverte, comme un <xref:System.Windows.Shapes.Line>, un <xref:System.Windows.Shapes.Polyline>, ou une ouverture <xref:System.Windows.Shapes.Path> élément.  
  
 L’exemple suivant dessine quatre <xref:System.Windows.Shapes.Polyline> éléments et utilise un autre ensemble de formes à la fin de chacun d’eux.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[drawingwithshapeelements#ShapeLineCaps1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/linecapsandjoinsexample.xaml#shapelinecaps1)]  
  
 Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Shapes.Polyline>
- <xref:System.Windows.Media.PenLineCap>
