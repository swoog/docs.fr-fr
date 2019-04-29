---
title: 'Procédure : Animer la couleur ou l’opacité d’un SolidColorBrush'
ms.date: 03/30/2017
helpviewer_keywords:
- SolidColorBrush [WPF], animating color of
- colors [WPF], animating
- opacity [WPF], animating
- animation [WPF], color of SolidColorBrush
- animation [WPF], opacity of SolidColorBrush
- SolidColorBrush [WPF], animating opacity of
ms.assetid: d9154354-843f-4713-bad1-35bb0ba6eaeb
ms.openlocfilehash: e440cf49b8b16051361650f9659dc6006c2e7b56
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789244"
---
# <a name="how-to-animate-the-color-or-opacity-of-a-solidcolorbrush"></a>Procédure : Animer la couleur ou l’opacité d’un SolidColorBrush
Cet exemple montre comment animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> et <xref:System.Windows.Media.Brush.Opacity%2A> d’un <xref:System.Windows.Media.SolidColorBrush>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise trois animations pour animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> et <xref:System.Windows.Media.Brush.Opacity%2A> d’un <xref:System.Windows.Media.SolidColorBrush>.  
  
- La première animation, un <xref:System.Windows.Media.Animation.ColorAnimation>, modifie la couleur du pinceau à <xref:System.Windows.Media.Colors.Gray%2A> lorsque la souris entre dans le rectangle.  
  
- L’animation suivante, une autre <xref:System.Windows.Media.Animation.ColorAnimation>, modifie la couleur du pinceau à <xref:System.Windows.Media.Colors.Orange%2A> lorsque la souris quitte le rectangle.  
  
- La dernière animation, un <xref:System.Windows.Media.Animation.DoubleAnimation>, modifie l’opacité du pinceau à 0.0 lorsque le bouton gauche de la souris est enfoncé.  
  
 [!code-csharp[brushanimations_snip#SolidColorBrushAnimationExample](~/samples/snippets/csharp/VS_Snippets_Wpf/brushanimations_snip/CSharp/SolidColorBrushExample.cs#solidcolorbrushanimationexample)]  
  
 Pour un exemple plus complet qui montre comment animer les différents types de pinceaux, consultez le [pinceaux, exemple](https://go.microsoft.com/fwlink/?LinkID=159973). Pour plus d’informations sur les animations, consultez le [vue d’ensemble de l’Animation](animation-overview.md).  
  
 Par souci de cohérence avec d’autres exemples d’animation, les versions de code de cet exemple utilisent un <xref:System.Windows.Media.Animation.Storyboard> objet pour appliquer leurs animations. Toutefois, lorsque vous appliquez une seule animation dans le code, il est plus simple d’utiliser le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> méthode au lieu d’utiliser un <xref:System.Windows.Media.Animation.Storyboard>. Si vous voulez voir un exemple, consultez l’article [Comment : animer une propriété sans utiliser de storyboard](how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des plans conceptuels](storyboards-overview.md)
- [Pinceaux, exemple](https://go.microsoft.com/fwlink/?LinkID=159973)
