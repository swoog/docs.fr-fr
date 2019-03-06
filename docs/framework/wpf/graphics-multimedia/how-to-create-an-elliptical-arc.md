---
title: 'Procédure : Créer un arc elliptique'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], elliptical arcs
- elliptical arcs [WPF], creating
- arcs [WPF], elliptical
ms.assetid: 3dcfe502-3485-45de-99fb-d53a1367c484
ms.openlocfilehash: bb4b4d99aab9daef70f446af176bb462b0661d54
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57354347"
---
# <a name="how-to-create-an-elliptical-arc"></a>Procédure : Créer un arc elliptique
Cet exemple montre comment dessiner un arc elliptique. Pour créer un arc elliptique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.ArcSegment> classes.  
  
## <a name="example"></a>Exemple  
 Dans les exemples suivants, un arc elliptique est dessiné de (10,100) à (200,100). L’arc a un <xref:System.Windows.Media.ArcSegment.Size%2A> de pixels indépendants du périphérique de 100 par 50, un <xref:System.Windows.Media.ArcSegment.RotationAngle%2A> de 45 degrés, un <xref:System.Windows.Media.ArcSegment.IsLargeArc%2A> définition de `true`et un <xref:System.Windows.Media.ArcSegment.SweepDirection%2A> de <xref:System.Windows.Media.SweepDirection.Counterclockwise>.  
  
 [xaml]  
  
 Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe d’attribut pour décrire un chemin d’accès.  
  
 [!code-xaml[GeometrySample#56](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#56)]  
  
 [xaml]  
  
 (Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>. (Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)  
  
 Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner un arc elliptique en utilisant explicitement des balises d’objet. Ce qui suit est équivalent à l’exemple précédent [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] balisage.  
  
 [!code-xaml[GeometrySample#36](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#36)]  
  
 Cet exemple fait partie d’un exemple plus complet. Pour obtenir un exemple complet, consultez la [géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).  
  
## <a name="see-also"></a>Voir aussi
- [Créer une courbe de Bézier quadratique](how-to-create-a-quadratic-bezier-curve.md)
- [Créer une courbe de Bézier cubique](how-to-create-a-cubic-bezier-curve.md)
