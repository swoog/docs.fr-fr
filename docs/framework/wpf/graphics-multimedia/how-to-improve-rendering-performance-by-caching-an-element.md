---
title: 'Comment : améliorer les performances de rendu en mettant en cache un élément'
ms.date: 03/30/2017
helpviewer_keywords:
- rendering performance [WPF], caching an element
- BitmapCache [WPF], improving rendering performance
- CacheMode [WPF], improving rendering performance
- performance [WPF], caching an element
- UIElement [WPF], caching
ms.assetid: 4739c1fc-60ba-4c46-aba6-f6c1a2688f19
ms.openlocfilehash: a92909c623db0c10e3434677b4275fa82b787fa7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559296"
---
# <a name="how-to-improve-rendering-performance-by-caching-an-element"></a>Comment : améliorer les performances de rendu en mettant en cache un élément
Utilisez le <xref:System.Windows.Media.BitmapCache> classe pour améliorer les performances de rendu d’un type complexe <xref:System.Windows.UIElement>. Pour mettre en cache un élément, créer une nouvelle instance de la <xref:System.Windows.Media.BitmapCache> de classe et l’affecter à l’élément <xref:System.Windows.UIElement.CacheMode%2A> propriété. Vous pouvez réutiliser un <xref:System.Windows.Media.BitmapCache> efficacement dans un <xref:System.Windows.Media.BitmapCacheBrush>.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment créer un élément complexe et de mettre en cache sous forme de bitmap, ce qui améliore les performances lors de l’élément est animé. L’élément est une zone qui contient les géométries de forme avec un grand nombre de sommets. A <xref:System.Windows.Media.BitmapCache> avec la valeur par défaut des valeurs est attribué à la <xref:System.Windows.UIElement.CacheMode%2A> de la zone de dessin, et une animation montre l’évolution en douceur de l’image bitmap mise en cache.  
  
 [!code-xaml[System.Windows.Media.BitmapCache#_BitmapCacheXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcache/cs/window1.xaml#_bitmapcachexaml)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.BitmapCache>  
 <xref:System.Windows.Media.BitmapCacheBrush>  
 <xref:System.Windows.UIElement.CacheMode%2A>  
 [Guide pratique pour utiliser un élément mis en cache comme pinceau](../../../../docs/framework/wpf/graphics-multimedia/how-to-use-a-cached-element-as-a-brush.md)
