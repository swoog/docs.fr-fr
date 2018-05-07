---
title: "Comment : animer la taille d'un FrameworkElement"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], FrameworkElement size
- FrameworkElement [WPF], animating size of
ms.assetid: d4cd5a13-c20d-4a6f-a2ba-14f2c9ce4cef
ms.openlocfilehash: 148e3d592e129984bd2f7ac062340c5169e48d30
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-animate-the-size-of-a-frameworkelement"></a>Comment : animer la taille d'un FrameworkElement
Pour animer la taille d’un <xref:System.Windows.FrameworkElement>, vous pouvez animer ses <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés ou utilisez un animé <xref:System.Windows.Media.ScaleTransform>.  
  
 Dans l’exemple suivant réalise une animation de la taille des deux boutons à l’aide de ces deux approches. Un bouton est redimensionné en animation son <xref:System.Windows.FrameworkElement.Width%2A> propriété et l’autre est redimensionnée par l’animation un <xref:System.Windows.Media.ScaleTransform> appliquée à ses <xref:System.Windows.UIElement.RenderTransform%2A> propriété. Chaque bouton contient du texte. Initialement, le texte est le même dans les deux boutons, mais que les boutons sont redimensionnés, le texte dans le deuxième bouton est déformé.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformanimations_snip#1](../../../../samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/AnimatingSizeExample.xaml#1)]  
  
 Lorsque vous transformez un élément, l’élément tout entier et son contenu est transformés. Lorsque vous modifiez directement la taille d’un élément, comme dans le cas du premier bouton, contenu de l’élément n’est pas redimensionné à moins que leur taille et la position dépendent de la taille de leur élément parent.  
  
 Animation de la taille d’un élément en appliquant une transformation animée à sa <xref:System.Windows.UIElement.RenderTransform%2A> propriété fournit de meilleures performances que sa <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> directement, car le <xref:System.Windows.UIElement.RenderTransform%2A> propriété ne déclenche pas une passe de disposition.  
  
 Pour plus d’informations sur les propriétés d’animation, consultez le [vue d’ensemble de l’Animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md). Pour plus d’informations sur les transformations, consultez la [transforme une vue d’ensemble](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md).
