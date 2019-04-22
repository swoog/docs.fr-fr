---
title: 'Procédure : Définir la taille de la mosaïque pour un TileBrush'
ms.date: 03/30/2017
helpviewer_keywords:
- TileBrush [WPF], size of tile properties
- Viewport property of TileBrush [WPF]
ms.assetid: 04f41090-1b46-4e36-832f-d27d28708b8c
ms.openlocfilehash: 80b5dfc668464df829db593668bea8a9a4ec09e4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58839674"
---
# <a name="how-to-set-the-tile-size-for-a-tilebrush"></a>Procédure : Définir la taille de la mosaïque pour un TileBrush

Cet exemple montre comment définir la taille de la mosaïque pour un <xref:System.Windows.Media.TileBrush>. Par défaut, un <xref:System.Windows.Media.TileBrush> produit une seule mosaïque qui remplit complètement la zone que vous peignez. Vous pouvez substituer ce comportement en définissant le <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriétés.

Le <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété spécifie la taille de la mosaïque pour un <xref:System.Windows.Media.TileBrush>. Par défaut, la valeur de la <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété est relative à la taille de la zone peinte. Pour rendre le <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété spécifier une taille de mosaïque absolue, définissez le <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriété <xref:System.Windows.Media.BrushMappingMode.Absolute>.

## <a name="example"></a>Exemple

L’exemple suivant utilise un <xref:System.Windows.Media.ImageBrush>, un type de <xref:System.Windows.Media.TileBrush>, pour peindre un rectangle avec des vignettes. L’exemple définit chaque mosaïque à 50 % de 50 % de la zone de sortie (le rectangle). Le rectangle est donc peint avec quatre projections de l’image.

L’illustration suivante montre la sortie produite par l’exemple :

![Un rectangle avec quatre cerises démonstration de mosaïque avec un pinceau d’image.](./media/how-to-set-the-tile-size-for-a-tilebrush/rectangle-tile-image-brush.png)

[!code-csharp[UsingImageBrush_snip#RelativeTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#relativetilesizeexample)]

L’exemple suivant crée un <xref:System.Windows.Media.ImageBrush>, définit son <xref:System.Windows.Media.TileBrush.Viewport%2A> à `0,0,25,25` et son <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> à <xref:System.Windows.Media.BrushMappingMode.Absolute>et l’utilise pour peindre un autre rectangle. Le pinceau produit ainsi des mosaïques d’une largeur de 25 pixels et d’une hauteur de 25 pixels.

L’illustration suivante montre la sortie produite par l’exemple :

![Un rectangle avec cerises quarante-huit illustrant un TileBrush en mosaïque avec une fenêtre d’affichage.](./media/how-to-set-the-tile-size-for-a-tilebrush/25-x-25-viewport-tilebrush.png)

[!code-csharp[UsingImageBrush_snip#AbsoluteTileSizeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/UsingImageBrush_snip/CSharp/TileSizeExample.cs#absolutetilesizeexample)]

Les exemples précédents font partie d’un exemple plus complet. Pour obtenir un exemple complet, consultez [ImageBrush, exemple](https://go.microsoft.com/fwlink/?LinkID=160005).

Bien que cet exemple utilise le <xref:System.Windows.Media.ImageBrush> (classe), le <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.ViewportUnits%2A> propriétés ont un comportement identique pour les autres <xref:System.Windows.Media.TileBrush> d’objets, autrement dit, pour <xref:System.Windows.Media.DrawingBrush> et <xref:System.Windows.Media.VisualBrush>. Pour plus d’informations sur <xref:System.Windows.Media.ImageBrush> et l’autre <xref:System.Windows.Media.TileBrush> , consultez [peinture avec des Images, de dessin et visuels](painting-with-images-drawings-and-visuals.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.TileBrush>
- [Peinture avec des images, des dessins et des objets visuels](painting-with-images-drawings-and-visuals.md)
- [Créer différents modèles de mosaïque avec un TileBrush](how-to-create-different-tile-patterns-with-a-tilebrush.md)
