---
title: 'Procédure : Animer l’opacité d’un élément ou d’un pinceau'
ms.date: 03/30/2017
helpviewer_keywords:
- opacity [WPF], animating
- animation [WPF], Opacity property
ms.assetid: 572af23b-39dd-48d1-9db5-4bca56a4b3d3
ms.openlocfilehash: f07138a0b68fff050133d477074571c60cd8651e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62020190"
---
# <a name="how-to-animate-the-opacity-of-an-element-or-brush"></a>Procédure : Animer l’opacité d’un élément ou d’un pinceau
Pour rendre un élément d’infrastructure apparaître et disparaître, vous pouvez animer sa <xref:System.Windows.UIElement.Opacity%2A> propriété, ou vous pouvez animer la <xref:System.Windows.Media.Brush.Opacity%2A> propriété de la <xref:System.Windows.Media.Brush> (ou pinceaux) utilisé pour peindre. Animer l’opacité de l’élément rend et ses enfants apparaître et disparaître, mais animer le pinceau utilisé pour peindre l’élément vous permet d’être plus sélectifs sur quelle partie de l’élément disparaît. Par exemple, vous pouvez animer l’opacité d’un pinceau utilisé pour peindre l’arrière-plan d’un bouton. Cela entraînerait l’arrière-plan du bouton à disparaître en fondu de la vue, tout en laissant son texte complètement opaque.  
  
> [!NOTE]
>  Animer la <xref:System.Windows.Media.Brush.Opacity%2A> d’un <xref:System.Windows.Media.Brush> offre les avantages de performances sur Animer le <xref:System.Windows.UIElement.Opacity%2A> propriété d’un élément.  
  
 Dans l’exemple suivant, deux boutons sont animés de sorte qu’ils apparaître et disparaître. L’opacité du premier <xref:System.Windows.Controls.Button> est animé de `1.0` à `0.0` sur un <xref:System.Windows.Media.Animation.Timeline.Duration%2A> de cinq secondes. Le deuxième bouton est également animé, mais l’opacité de SolidColorBrush utilisé pour peindre son <xref:System.Windows.Controls.Control.Background%2A> est animée au lieu de l’opacité du bouton entier. Lorsque l’exemple est exécuté, le premier bouton est complètement fondu dans et hors de vue, alors qu’uniquement l’arrière-plan du deuxième bouton Fondu dans et hors de vue. Son texte et sa bordure restent entièrement opaques.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[timingbehaviors_snip#10](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/OpacityAnimationExample.xaml#10)]  
  
 Code a été omis de cet exemple. L’exemple complet montre également comment animer l’opacité d’un <xref:System.Windows.Media.Color> au sein d’un <xref:System.Windows.Media.LinearGradientBrush>.  Pour l’exemple complet, consultez la [animer l’opacité d’un exemple d’élément](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/OpacityAnimation).
