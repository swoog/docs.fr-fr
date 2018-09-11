---
title: "Comment : mettre à l'échelle un élément"
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], elements
- graphics [WPF], scaling elements
ms.assetid: 18158d94-bbe7-4f6a-814e-84d27fa748bf
ms.openlocfilehash: 44c638b58d828e5beb0b9de5c7bb0b67c8e82d87
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44366018"
---
# <a name="how-to-scale-an-element"></a>Comment : mettre à l'échelle un élément
Cet exemple montre comment utiliser un <xref:System.Windows.Media.ScaleTransform> à l’échelle un élément.  
  
 Utilisez le <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> et <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> propriétés pour redimensionner l’élément selon le facteur que vous spécifiez. Par exemple, un <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> valeur de 1,5 étire l’élément à 150 % de sa largeur d’origine. A <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> la valeur 0,5 diminue la hauteur d’un élément de 50 %.  
  
 Utilisez le <xref:System.Windows.Media.ScaleTransform.CenterX%2A> et <xref:System.Windows.Media.ScaleTransform.CenterY%2A> propriétés pour spécifier le point qui correspond au centre de l’opération de mise à l’échelle. Par défaut, un <xref:System.Windows.Media.ScaleTransform> est centré au point (0,0), qui correspond à l’angle supérieur gauche du rectangle. Cela a pour effet de déplacer l’élément et également de le faire paraître plus grand, car lorsque vous appliquez un <xref:System.Windows.Media.Transform>, vous modifiez l’espace de coordonnées dans lequel réside l’objet.  
  
 L’exemple suivant utilise un <xref:System.Windows.Media.ScaleTransform> de doubler la taille de 50 par 50 <xref:System.Windows.Shapes.Rectangle>. Le <xref:System.Windows.Media.ScaleTransform> a la valeur 0 (valeur par défaut) pour les deux <xref:System.Windows.Media.ScaleTransform.CenterX%2A> et <xref:System.Windows.Media.ScaleTransform.CenterY%2A>.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[transformsSample#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#21)]  
  
 En règle générale, vous définissez <xref:System.Windows.Media.ScaleTransform.CenterX%2A> et <xref:System.Windows.Media.ScaleTransform.CenterY%2A> au centre de l’objet à l’échelle : (<xref:System.Windows.FrameworkElement.Width%2A>/2,  <xref:System.Windows.FrameworkElement.Height%2A> /2).  
  
 L’exemple suivant montre un autre <xref:System.Windows.Shapes.Rectangle> qui est doublé de taille ; Toutefois, cela <xref:System.Windows.Media.ScaleTransform> a une valeur de 25 pour <xref:System.Windows.Media.ScaleTransform.CenterX%2A> et <xref:System.Windows.Media.ScaleTransform.CenterY%2A>, qui correspond au centre du rectangle.  
  
 [!code-xaml[transformsSample#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/ScaleTransformExample.xaml#22)]  
  
 L’illustration suivante montre la différence entre les deux <xref:System.Windows.Media.ScaleTransform> operations. La ligne en pointillés affiche la taille et la position du rectangle avant la mise à l’échelle.  
  
 ![échelles de 2 x avec différents points centraux](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-scalecenter.gif "wcpsdk_graphicsmm_scalecenter")  
Deux opérations ScaleTransform avec des valeurs ScaleX et ScaleY identiques, mais des centres différents  
  
 Pour voir l’exemple complet, consultez la page [2-D Transforms Sample](https://go.microsoft.com/fwlink/?LinkID=158252) (Exemple de transformations 2D).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Transform>  
 <xref:System.Windows.Media.ScaleTransform>  
 [Vue d’ensemble des transformations](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
