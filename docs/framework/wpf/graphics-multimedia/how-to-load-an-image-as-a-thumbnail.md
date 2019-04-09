---
title: 'Procédure : Charger une image en tant que miniature'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- loading images as thumbnails [WPF]
- images [WPF], loading as thumbnails
- thumbnails [WPF], loading images as
ms.assetid: 02e055a0-54df-499a-b8b6-ab6ff7535cff
ms.openlocfilehash: f984293a395e925368b20cef6aa0cd902bd6fc15
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134041"
---
# <a name="how-to-load-an-image-as-a-thumbnail"></a>Procédure : Charger une image en tant que miniature
Les exemples suivants montrent comment charger un <xref:System.Windows.Controls.Image> en tant que miniature pour économiser la mémoire de l’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> propriété d’un <xref:System.Windows.Media.Imaging.BitmapImage> dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] afin de réduire la mémoire requise pour charger l’image.  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> propriété d’un <xref:System.Windows.Media.Imaging.BitmapImage> dans le code afin de réduire la mémoire requise pour charger l’image.  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de la création d'images](imaging-overview.md)
