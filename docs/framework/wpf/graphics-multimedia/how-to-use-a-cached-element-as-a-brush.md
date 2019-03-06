---
title: 'Procédure : Utiliser un élément mis en cache comme pinceau'
ms.date: 03/30/2017
helpviewer_keywords:
- BitmapCache [WPF], using
- cached element [WPF], use as a brush
- BitmapCacheBrush [WPF], using
- CacheMode [WPF], using
ms.assetid: d36e944a-866e-4baf-98c4-fd6a75f6fdd0
ms.openlocfilehash: 008bec87390a807ae2b4797af8b86aaf59c92ef5
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372488"
---
# <a name="how-to-use-a-cached-element-as-a-brush"></a>Procédure : Utiliser un élément mis en cache comme pinceau
Utilisez la <xref:System.Windows.Media.BitmapCacheBrush> classe pour réutiliser efficacement un élément mis en cache. Pour mettre en cache un élément, créez une nouvelle instance de la <xref:System.Windows.Media.BitmapCache> classe et l’affecter à l’élément <xref:System.Windows.UIElement.CacheMode%2A> propriété.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment réutiliser un élément mis en cache. L’élément mis en cache est un <xref:System.Windows.Controls.Image> contrôle qui affiche une grande image. Le <xref:System.Windows.Controls.Image> contrôle est mis en cache sous forme de bitmap à l’aide de la <xref:System.Windows.Media.BitmapCache> classe et le cache est réutilisé en lui assignant un <xref:System.Windows.Media.BitmapCacheBrush>. Le pinceau est affecté à l’arrière-plan des boutons de 25 pour une réutilisation efficace.  
  
 [!code-xaml[System.Windows.Media.BitmapCacheBrush#_BitmapCacheBrushXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcachebrush/cs/window1.xaml#_bitmapcachebrushxaml)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.BitmapCache>
- <xref:System.Windows.Media.BitmapCacheBrush>
- <xref:System.Windows.UIElement.CacheMode%2A>
- [Guide pratique pour Améliorer les performances de rendu en mettant en cache un élément](how-to-improve-rendering-performance-by-caching-an-element.md)
