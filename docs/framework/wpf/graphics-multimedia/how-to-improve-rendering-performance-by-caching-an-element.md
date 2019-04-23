---
title: 'Procédure : Améliorer les performances de rendu en mettant en cache un élément'
ms.date: 03/30/2017
helpviewer_keywords:
- rendering performance [WPF], caching an element
- BitmapCache [WPF], improving rendering performance
- CacheMode [WPF], improving rendering performance
- performance [WPF], caching an element
- UIElement [WPF], caching
ms.assetid: 4739c1fc-60ba-4c46-aba6-f6c1a2688f19
ms.openlocfilehash: 118e8b0cca52c44788c9d5b291d710f765e7af2a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153372"
---
# <a name="how-to-improve-rendering-performance-by-caching-an-element"></a>Procédure : Améliorer les performances de rendu en mettant en cache un élément
Utilisez le <xref:System.Windows.Media.BitmapCache> classe afin d’améliorer les performances de rendu d’un type complexe <xref:System.Windows.UIElement>. Pour mettre en cache un élément, créez une nouvelle instance de la <xref:System.Windows.Media.BitmapCache> classe et l’affecter à l’élément <xref:System.Windows.UIElement.CacheMode%2A> propriété. Vous pouvez réutiliser un <xref:System.Windows.Media.BitmapCache> efficacement dans un <xref:System.Windows.Media.BitmapCacheBrush>.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment créer un élément complexe et le met en cache sous forme de bitmap, ce qui améliore les performances lors de l’élément est animée. L’élément est une zone qui contient les géométries de forme avec le nombre de vertex. Un <xref:System.Windows.Media.BitmapCache> avec la valeur par défaut valeurs est affectée à la <xref:System.Windows.UIElement.CacheMode%2A> du canevas, et une animation montre la mise à l’échelle sans heurts de l’image bitmap mise en cache.  
  
 [!code-xaml[System.Windows.Media.BitmapCache#_BitmapCacheXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcache/cs/window1.xaml#_bitmapcachexaml)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [Guide pratique pour Utiliser un élément mis en cache comme pinceau](how-to-use-a-cached-element-as-a-brush.md)
