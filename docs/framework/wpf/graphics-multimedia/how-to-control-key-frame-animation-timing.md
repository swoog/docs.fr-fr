---
title: "Procédure : Contrôler le minutage de l'animation d'image clé"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], timing
- timing key-frame animation
ms.assetid: b059216f-7d4b-4ca8-a019-bc287ee7bf16
ms.openlocfilehash: d0ea56b24f8fffeb688d297a675681bce3fdc4e0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489876"
---
# <a name="how-to-control-key-frame-animation-timing"></a>Procédure : Contrôler le minutage de l'animation d'image clé

Cet exemple montre comment contrôler le minutage des images clés d’une animation d’image clé. Comme les autres animations, les animations d’image clé ont une <xref:System.Windows.Media.Animation.Timeline.Duration%2A> propriété. En plus de spécifier la durée d’une animation, vous devez spécifier quelle partie de cette durée est alloué à chacun de ses images clés. Pour allouer du temps, vous spécifiez un <xref:System.Windows.Media.Animation.KeyTime> pour chaque image clé de l’animation.

Le <xref:System.Windows.Media.Animation.KeyTime> pour chaque image clé spécifie la fin d’une image clé (il ne spécifie pas la durée de lecture d’une image clé). Vous pouvez spécifier un <xref:System.Windows.Media.Animation.KeyTime> comme un <xref:System.TimeSpan> valeur sous forme de pourcentage ou en tant que le <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> ou <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> valeur spéciale.

## <a name="example"></a>Exemple

L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> pour animer un rectangle sur l’écran. Temps clés des images clés sont définies avec <xref:System.TimeSpan> valeurs.

[!code-csharp[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimestimespanexample)]
[!code-vb[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimestimespanexample)]
[!code-xaml[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimestimespanexample)]

L’illustration suivante montre les lorsque la valeur de chaque image clé est atteinte.

![Valeurs de clés atteintes à 3, 4 et 10 secondes](./media/graphicsmm-keyframe-keytime1-timespan.png "graphicsmm_keyframe_keytime1_timespan")

L’exemple suivant illustre une animation qui est identique, sauf que les temps clés des images clés sont définies avec les valeurs de pourcentage.

[!code-csharp[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespercentageexample)]
[!code-vb[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespercentageexample)]
[!code-xaml[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespercentageexample)]

L’illustration suivante montre les lorsque la valeur de chaque image clé est atteinte.

![Valeurs de clés atteintes à 3, 4 et 10 secondes](./media/graphicsmm-keyframe-keytime2-percentage.png "graphicsmm_keyframe_keytime2_percentage")

L’exemple suivant utilise <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> valeurs de temps clé.

[!code-csharp[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimesuniformexample)]
[!code-vb[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimesuniformexample)]
[!code-xaml[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimesuniformexample)]

L’illustration suivante montre les lorsque la valeur de chaque image clé est atteinte.

![Valeurs de clés atteintes à 3,3, 6,6 et 9,9 secondes](./media/graphicsmm-keyframe-keytime3-uniform.png "graphicsmm_keyframe_keytime3_uniform")

Le dernier exemple utilise <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> valeurs de temps clé.

[!code-csharp[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespacedexample)]
[!code-vb[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespacedexample)]
[!code-xaml[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespacedexample)]

L’illustration suivante montre les lorsque la valeur de chaque image clé est atteinte.

![Valeurs de clés atteintes à 0, 5 et 10 secondes](./media/graphicsmm-keyframe-keytime4-paced.png "graphicsmm_keyframe_keytime4_paced")

Par souci de simplicité, les versions de code de cet exemple utilisent des animations locales, pas storyboards, car une seule animation est appliquée à une propriété unique, mais les exemples peuvent être modifiés pour utiliser des tables de montage séquentiel à la place. Pour obtenir un exemple montrant comment déclarer un storyboard dans le code, consultez [animer une propriété à l’aide d’un Storyboard](how-to-animate-a-property-by-using-a-storyboard.md).

Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012). Pour plus d’informations sur les animations d’image clé, consultez le [vue d’ensemble des Animations image clé](key-frame-animations-overview.md).

## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Rubriques de guide pratique](animation-and-timing-how-to-topics.md)
