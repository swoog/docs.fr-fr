---
title: 'Procédure : Animer un Popup'
ms.date: 03/30/2017
helpviewer_keywords:
- Popup control [WPF], animating
- animation [WPF], Popup controls
ms.assetid: acaa2a0a-6137-4efd-9cd1-75ece222e390
ms.openlocfilehash: b70d9c4cb1bca26a6c77d3a7c50add517ca8ef92
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150109"
---
# <a name="how-to-animate-a-popup"></a>Procédure : Animer un Popup
Cet exemple montre deux façons d’animer un <xref:System.Windows.Controls.Primitives.Popup> contrôle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la <xref:System.Windows.Controls.Primitives.PopupAnimation> à une valeur de propriété <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide>, ce qui conduit le <xref:System.Windows.Controls.Primitives.Popup> sur « diapositive-in » lorsqu’il apparaît.  
  
 Pour faire pivoter le <xref:System.Windows.Controls.Primitives.Popup>, cet exemple affecte un <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété sur le <xref:System.Windows.Controls.Canvas>, qui est l’élément enfant de la <xref:System.Windows.Controls.Primitives.Popup>.  
  
 Pour la transformation fonctionne correctement, l’exemple doit définir le <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> propriété `true`. En outre, le <xref:System.Windows.FrameworkElement.Margin%2A> sur le <xref:System.Windows.Controls.Canvas> contenu doit spécifier suffisamment d’espace pour le <xref:System.Windows.Controls.Primitives.Popup> pour faire pivoter.  
  
 [!code-xaml[AnimatedPopup#RotateTransform2](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform2)]  
  
 L’exemple suivant montre comment un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement qui se produit lorsqu’un <xref:System.Windows.Controls.Button> est activé, les déclencheurs le <xref:System.Windows.Media.Animation.Storyboard> qui démarre l’animation.  
  
 [!code-xaml[AnimatedPopup#RotateTransform1](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Controls.Primitives.BulletDecorator>
- <xref:System.Windows.Media.RotateTransform>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Controls.Primitives.Popup>
- [Rubriques Comment](popup-how-to-topics.md)
- [Vue d'ensemble de Popup](popup-overview.md)
