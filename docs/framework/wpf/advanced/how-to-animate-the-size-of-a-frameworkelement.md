---
title: "Procédure : Animer la taille d'un FrameworkElement"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], FrameworkElement size
- FrameworkElement [WPF], animating size of
ms.assetid: d4cd5a13-c20d-4a6f-a2ba-14f2c9ce4cef
ms.openlocfilehash: d1995deec5ab2c9bf405911af43b4d242d599119
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57360990"
---
# <a name="how-to-animate-the-size-of-a-frameworkelement"></a>Procédure : Animer la taille d'un FrameworkElement
Pour animer la taille d’un <xref:System.Windows.FrameworkElement>, vous pouvez animer sa <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés ou utilisez un texte animé <xref:System.Windows.Media.ScaleTransform>.  
  
 Dans l’exemple suivant anime la taille des deux boutons à l’aide de ces deux approches. Un bouton est redimensionné en animant ses <xref:System.Windows.FrameworkElement.Width%2A> propriété et l’autre est redimensionné en animant un <xref:System.Windows.Media.ScaleTransform> appliquée à ses <xref:System.Windows.UIElement.RenderTransform%2A> propriété. Chaque bouton contient du texte. Initialement, le texte est le même dans les deux boutons, mais comme les boutons sont redimensionnés, le texte dans le deuxième bouton est déformé.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformanimations_snip#1](~/samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/AnimatingSizeExample.xaml#1)]  
  
 Lorsque vous transformez un élément, l’élément tout entier et son contenu est transformés. Lorsque vous modifiez directement la taille d’un élément, comme dans le cas du premier bouton, contenu de l’élément n’est pas redimensionné à moins que leur taille et la position dépendent de la taille de leur élément parent.  
  
 Animer la taille d’un élément en appliquant une transformation animée à sa <xref:System.Windows.UIElement.RenderTransform%2A> propriété fournit de meilleures performances que sa <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> directement, car le <xref:System.Windows.UIElement.RenderTransform%2A> propriété ne déclenche pas une passe de disposition.  
  
 Pour plus d’informations sur l’animation de propriétés, consultez le [vue d’ensemble de l’Animation](../graphics-multimedia/animation-overview.md). Pour plus d’informations sur les transformations, consultez la [transforme la vue d’ensemble](../graphics-multimedia/transforms-overview.md).
