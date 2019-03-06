---
title: 'Procédure : Rendre un UIElement transparent ou semi-transparent'
ms.date: 03/30/2017
helpviewer_keywords:
- UIElements [WPF], transparency
- opacity [WPF], of UIElements
- transparency of UIElements [WPF]
- UIElements [WPF], opacity
ms.assetid: a49fc8d6-7b32-4f28-9122-39b632a19b4b
ms.openlocfilehash: 1de9a7e11fee241ecb71242e9808e77b7e5e63b0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370525"
---
# <a name="how-to-make-a-uielement-transparent-or-semi-transparent"></a>Procédure : Rendre un UIElement transparent ou semi-transparent
Cet exemple montre comment rendre un <xref:System.Windows.UIElement> transparent ou semi-transparent. Pour rendre un élément transparent ou semi-transparent, vous définissez son <xref:System.Windows.UIElement.Opacity%2A> propriété. La valeur `0.0` rend l’élément complètement transparent, alors que la valeur `1.0` rend complètement opaque. La valeur `0.5` rend l’élément 50 % opaque et ainsi de suite. D’un élément <xref:System.Windows.UIElement.Opacity%2A> a la valeur `1.0` par défaut.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la <xref:System.Windows.UIElement.Opacity%2A> d’un bouton pour `0.25`, sorte que celui-ci et son contenu (dans ce cas, le texte du bouton) sont opaques à 25 %.  
  
 [!code-xaml[brushsamples_snip#2](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#2)]  
  
 [!code-csharp[brushsamples_procedural_snip#2](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#2)]  
  
 Si le contenu d’un élément ont leurs propres <xref:System.Windows.UIElement.Opacity%2A> paramètres, ces valeurs sont multipliés par rapport à des éléments CONTENANTS <xref:System.Windows.UIElement.Opacity%2A>.  
  
 L’exemple suivant définit un bouton de <xref:System.Windows.UIElement.Opacity%2A> à `0.25`et le <xref:System.Windows.UIElement.Opacity%2A> d’un <xref:System.Windows.Controls.Image> contrôle contenu dans le bouton pour `0.5`. Par conséquent, l’image apparaît 12,5 % opaque : 0.25 * 0.5 = 0.125.  
  
 [!code-xaml[brushsamples_snip#3](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#3)]  
  
 [!code-csharp[brushsamples_procedural_snip#3](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#3)]  
  
 Une autre façon de contrôler l’opacité d’un élément consiste à définir l’opacité de la <xref:System.Windows.Media.Brush> qui peint l’élément. Cette approche vous permet de modifier de manière sélective l’opacité de certaines parties d’un élément et offre des avantages de performances à l’aide de l’élément <xref:System.Windows.UIElement.Opacity%2A> propriété. L’exemple suivant définit la <xref:System.Windows.Media.Brush.Opacity%2A> d’un <xref:System.Windows.Media.SolidColorBrush> utilisé pour peindre le bouton <xref:System.Windows.Controls.Control.Background%2A> est défini sur `0.25`. Par conséquent, l’arrière-plan du pinceau est opaque à 25 %, mais son contenu (le texte du bouton) reste opaque à 100 %.  
  
 [!code-xaml[brushsamples_snip#4](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/OpacityExample.xaml#4)]  
  
 [!code-csharp[brushsamples_procedural_snip#4](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/OpacityExample.cs#4)]  
  
 Vous pouvez également contrôler l’opacité des couleurs individuelles au sein d’un pinceau. Pour plus d’informations sur les couleurs et les pinceaux, consultez [peinture avec des couleurs unies et vue d’ensemble des dégradés](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md). Pour obtenir un exemple montrant comment animer l’opacité d’un élément, consultez [animer l’opacité d’un élément ou d’un pinceau](../graphics-multimedia/how-to-animate-the-opacity-of-an-element-or-brush.md).
