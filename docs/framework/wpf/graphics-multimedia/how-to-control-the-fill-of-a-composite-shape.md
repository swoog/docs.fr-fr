---
title: 'Procédure : Contrôler le remplissage d’une forme composite'
ms.date: 03/30/2017
helpviewer_keywords:
- shapes [WPF], composite [WPF], controlling fill
- composite shapes [WPF], controlling fill
- graphics [WPF], composite shapes
- fill [WPF], controlling
ms.assetid: c1c94575-9eca-48a5-a49a-2ec65259f229
ms.openlocfilehash: 0ba07d8979a2910ce4ec775493e38c714240f642
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61997111"
---
# <a name="how-to-control-the-fill-of-a-composite-shape"></a>Procédure : Contrôler le remplissage d’une forme composite
Le <xref:System.Windows.Media.GeometryGroup.FillRule%2A> propriété d’un <xref:System.Windows.Media.GeometryGroup> ou un <xref:System.Windows.Media.PathGeometry>, spécifie une « règle » que la forme composite utilise pour déterminer si un point donné fait partie de la géométrie. Il existe deux valeurs possibles pour <xref:System.Windows.Media.FillRule>: <xref:System.Windows.Media.FillRule.EvenOdd> et <xref:System.Windows.Media.FillRule.Nonzero>. Les sections suivantes décrivent comment utiliser ces deux règles.  
  
 **EvenOdd :** Cette règle détermine si un point est dans la région de remplissage en dessinant un rayon à partir de ce point vers l’infini dans n’importe quelle direction et en comptant le nombre de segments de chemin d’accès dans la forme donnée que le rayon traverse. Si ce nombre est impair, le point est à l’intérieur ; s’il est pair, le point est à l’extérieur.  
  
 Par exemple, le XAML ci-dessous crée une forme composite constituée d’une série d’anneaux concentriques (cible) avec un <xref:System.Windows.Media.GeometryGroup.FillRule%2A> défini sur <xref:System.Windows.Media.FillRule.EvenOdd>.  
  
 [!code-xaml[GeometriesMiscSnippets_snip#FillRuleEvenOddValue](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillruleevenoddvalue)]  
  
 L’illustration suivante montre la forme créée dans l’exemple précédent.  
  
 ![Un cercle est constitué d’un anneaux concentriques série avec des couleurs alternées.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-evenodd-property.png)  
  
 Dans l’illustration précédente, notez que le centre et le troisième anneau ne sont pas remplis. En effet, un rayon dessiné à partir de n’importe quel point dans un de ces deux anneaux traverse un nombre pair de segments. Consultez l’illustration suivante :  
  
 ![Diagramme montrant les rayons EvenOdd dessinés dans le cercle.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-evenodd-rays.png)  
  
 **Différent de zéro :** Cette règle détermine si un point est dans la région de remplissage du tracé en dessinant un rayon à partir de ce point vers l’infini dans n’importe quelle direction et en examinant ensuite les emplacements où un segment de la forme coupe le rayon. En commençant à zéro, comptez un point chaque fois qu’un segment coupe le rayon de gauche à droite, et soustrayez un point chaque fois qu’un segment de tracé traverse le rayon de droite à gauche. Comptez ensuite le nombre d’intersections : si le résultat est égal à zéro, le point est à l’extérieur du tracé. Sinon, il est à l’intérieur.  
  
 [!code-xaml[GeometriesMiscSnippets_snip#FillRuleNonZeroValueEllipseGeometry](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillrulenonzerovalueellipsegeometry)]  
  
 À l’aide de l’exemple précédent, la valeur <xref:System.Windows.Media.FillRule.Nonzero> pour <xref:System.Windows.Media.GeometryGroup.FillRule%2A> donne par conséquent de l’illustration suivante :  
  
 ![Un cercle est constitué d’une série anneaux concentriques tous les rempli avec la même couleur.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-value-nonzero.png)  
  
 Comme vous pouvez le voir, tous les anneaux sont remplis. En effet, tous les segments s’étendent dans la même direction, ce qui signifie qu’un rayon dessiné à partir de n’importe quel point traversera un ou plusieurs segments et que la somme des intersections ne sera pas égale à zéro. Par exemple, dans l’illustration suivante, les flèches rouges représentent la direction que les segments sont dessinés et les flèches blanches représentent un rayon arbitraire à partir d’un point dans l’anneau intérieur. En commençant par une valeur égale à zéro, pour chaque segment que le rayon traverse, une valeur de un est ajoutée car le segment traverse le rayon de gauche à droite.  
  
 ![Schéma montrant la valeur de propriété FillRule égale à Nonzero.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-value-equal-nonzero.png)  
  
 Pour mieux illustrer le comportement de <xref:System.Windows.Media.FillRule.Nonzero> règle une forme plus complexe avec des segments en cours d’exécution dans différentes directions est requise. Le code XAML ci-dessous crée une forme semblable que l’exemple précédent, à ceci près qu’elle est créée avec un <xref:System.Windows.Media.PathGeometry> puis plutôt un <xref:System.Windows.Media.EllipseGeometry> cercles concentriques plutôt puis qui crée quatre cercles concentriques complètement fermés.  
  
 [!code-xaml[GeometriesMiscSnippets_snip#FillRuleNonZeroValuePathGeometry](~/samples/snippets/xaml/VS_Snippets_Wpf/GeometriesMiscSnippets_snip/XAML/FillRuleExample.xaml#fillrulenonzerovaluepathgeometry)]  
  
 L’illustration suivante montre la forme créée dans l’exemple précédent.  
  
 ![Un cercle est constitué d’un anneaux concentriques série avec des couleurs alternées avec le troisième arc ne pas rempli.](./media/how-to-control-the-fill-of-a-composite-shape/pathgeometry-concentric-arcs.png)  
  
 Notez que le troisième arc partant du centre n’est pas rempli. L’illustration suivante montre pourquoi il s’agit. Dans l’illustration, les flèches rouges représentent la direction dans laquelle les segments sont dessinés. Les deux flèches blanches représentent deux rayons arbitraires qui partent d’un point dans la région « non remplie ». Comme le montre l’illustration, la somme des valeurs d’un rayon donné qui traverse les segments dans son tracé est égale à zéro. Comme indiqué ci-dessus, une somme égale à zéro signifie que le point ne fait pas partie de la géométrie (il ne fait pas partie du remplissage) tandis qu’une somme qui n’est *pas* égale à zéro, y compris une valeur négative, fait partie de la géométrie.  
  
 ![Diagramme montrant des segments de traversée de rayons arbitraires.](./media/how-to-control-the-fill-of-a-composite-shape/arbitrary-ray-cross-segment.png)  
  
 **Remarque :** Dans le cadre de <xref:System.Windows.Media.FillRule>, toutes les formes sont considérées comme fermées. S’il y a un écart dans un segment, dessinez une ligne imaginaire pour le fermer. Dans l’exemple ci-dessus, on observe existe de petits écarts au niveau des anneaux. On peut donc s’attendre à ce qu’un rayon qui traverse cet écart produise un résultat différent de celui d’un rayon qui s’étend dans une autre direction. Voici une illustration agrandie d’un de ces écarts et du « segment imaginaire » (segment dessiné afin d’appliquer le <xref:System.Windows.Media.FillRule>) qui le referme.  
  
 ![Diagramme montrant les segments FillRule qui sont toujours fermés.](./media/how-to-control-the-fill-of-a-composite-shape/fillrule-closed-segments.png)  
  
## <a name="example"></a>Exemple  
  
## <a name="see-also"></a>Voir aussi

- [Créer une forme composite](how-to-create-a-composite-shape.md)
- [Vue d’ensemble de Geometry](geometry-overview.md)
