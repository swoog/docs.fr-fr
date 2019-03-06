---
title: 'Procédure : Retourner un UIElement horizontalement ou verticalement'
ms.date: 03/30/2017
helpviewer_keywords:
- flipping UIElements [WPF]
- UIElements [WPF], flipping
ms.assetid: 02c6730f-65c0-40d5-a553-4cb663721882
ms.openlocfilehash: 3dd9a8e2a94acf62973701094e8966c8ebff15c9
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57356349"
---
# <a name="how-to-flip-a-uielement-horizontally-or-vertically"></a>Procédure : Retourner un UIElement horizontalement ou verticalement
Cet exemple montre comment utiliser un <xref:System.Windows.Media.ScaleTransform> pour retourner un <xref:System.Windows.UIElement> horizontalement ou verticalement. Dans cet exemple, un <xref:System.Windows.Controls.Button> contrôle (un type de <xref:System.Windows.UIElement>) est retourné en appliquant un <xref:System.Windows.Media.ScaleTransform> à son <xref:System.Windows.UIElement.RenderTransform%2A> propriété.  
  
## <a name="example"></a>Exemple  
 L’illustration suivante montre le bouton à retourner.  
  
 ![Un bouton sans transformation](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")  
UIElement à retourner  
  
 Voici le code qui crée le bouton.  
  
 [!code-xaml[Transforms_snip#GraphicsMMButtonWithoutFlip](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmbuttonwithoutflip)]  
  
## <a name="example"></a>Exemple  
 Pour retourner le bouton horizontalement, créez un <xref:System.Windows.Media.ScaleTransform> et définissez son <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> propriété sur -1. Appliquer le <xref:System.Windows.Media.ScaleTransform> sur le bouton <xref:System.Windows.UIElement.RenderTransform%2A> propriété.  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample1)]  
  
 ![Bouton renvoyé horizontalement autour de &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")  
Bouton après l’application de ScaleTransform  
  
## <a name="example"></a>Exemple  
 Comme vous pouvez le voir à partir de l’illustration précédente, le bouton a été retourné, mais il a également été déplacé. C’est parce que le bouton a été retourné à partir de son coin supérieur gauche. Pour retourner le bouton, vous souhaitez appliquer le <xref:System.Windows.Media.ScaleTransform> à son centre, pas son supérieur. Un moyen facile d’appliquer le <xref:System.Windows.Media.ScaleTransform> aux boutons center consiste à définir le bouton <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété 0.5, 0.5.  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample2)]  
  
 ![Bouton renvoyé horizontalement autour de son centre](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")  
Le bouton avec un RenderTransformOrigin de 0.5, 0.5  
  
## <a name="example"></a>Exemple  
 Pour retourner le bouton verticalement, définissez la <xref:System.Windows.Media.ScaleTransform> l’objet <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> propriété au lieu de son <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> propriété.  
  
 [!code-xaml[Transforms_snip#GraphicsMMVerticalFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmverticalflipbuttonexample2)]  
  
 ![Bouton renvoyé verticalement autour de son centre](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")  
Bouton retourné verticalement  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des transformations](../graphics-multimedia/transforms-overview.md)
