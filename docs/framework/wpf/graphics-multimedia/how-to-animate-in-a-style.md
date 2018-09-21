---
title: Comment animer dans un style (WPF)
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], properties [WPF], within styles
- styles [WPF], animating properties within
ms.assetid: 6a791f3d-6b1f-4972-a2f9-35880bcfd954
ms.openlocfilehash: a455bbfb9defbcf83f7e490f60031917a3b41779
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46516728"
---
# <a name="how-to-animate-in-a-style"></a>Comment animer dans un style

Cet exemple montre comment animer des propriétés dans un style. Lors de l’animation dans un style, seul l’élément de framework pour lequel le style est défini peut être ciblé directement. Pour cibler un objet freezable, vous devez « point vers le bas » à partir d’une propriété de l’élément de style.

Dans l’exemple suivant, plusieurs animations sont définies dans un style et appliquées à un <xref:System.Windows.Controls.Button>. Lorsque l’utilisateur déplace la souris sur le bouton, il passe d’opaque à partiellement transparent et vice à nouveau, à plusieurs reprises. Lorsque l’utilisateur déplace la souris hors du bouton, il devient complètement opaque. Lorsque le bouton est activé, sa couleur d’arrière-plan passe d’orange à blanc et inversement. Étant donné que le <xref:System.Windows.Media.SolidColorBrush> utilisé pour peindre le bouton ne peut pas être ciblé directement, il est accessible par pointillage au bas à partir du bouton <xref:System.Windows.Controls.Control.Background%2A> propriété.

## <a name="example"></a>Exemple

[!code-xaml[timingbehaviors_snip#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StyleStoryboardsExample.xaml#21)]

Notez que lors de l’animation dans un style, il est possible de cibler des objets qui n’existent pas. Par exemple, supposons que votre style utilise un <xref:System.Windows.Media.SolidColorBrush> pour définir la propriété d’arrière-plan d’un bouton, mais à un moment donné le style est substituée et que l’arrière-plan du bouton est défini avec un <xref:System.Windows.Media.LinearGradientBrush>.  Essayez d’animer la <xref:System.Windows.Media.SolidColorBrush> ne lève pas d’exception ; l’animation échouent silencieusement.

Pour plus d’informations sur la syntaxe de ciblage de plan conceptuel, consultez le [vue d’ensemble des Storyboards](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md). Pour plus d’informations sur les animations, consultez le [vue d’ensemble de l’Animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md). Pour plus d’informations sur les styles, consultez le [Styling and Templating](../../../../docs/framework/wpf/controls/styling-and-templating.md).
