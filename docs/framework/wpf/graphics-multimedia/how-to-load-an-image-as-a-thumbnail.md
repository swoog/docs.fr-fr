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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62003182"
---
# <a name="how-to-load-an-image-as-a-thumbnail"></a><span data-ttu-id="db6cc-102">Procédure : Charger une image en tant que miniature</span><span class="sxs-lookup"><span data-stu-id="db6cc-102">How to: Load an Image as a Thumbnail</span></span>
<span data-ttu-id="db6cc-103">Les exemples suivants montrent comment charger un <xref:System.Windows.Controls.Image> en tant que miniature pour économiser la mémoire de l’application.</span><span class="sxs-lookup"><span data-stu-id="db6cc-103">The following examples show how to load an <xref:System.Windows.Controls.Image> as a thumbnail to conserve application memory.</span></span>  
  
## <a name="example"></a><span data-ttu-id="db6cc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="db6cc-104">Example</span></span>  
 <span data-ttu-id="db6cc-105">L’exemple suivant définit la <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> propriété d’un <xref:System.Windows.Media.Imaging.BitmapImage> dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] afin de réduire la mémoire requise pour charger l’image.</span><span class="sxs-lookup"><span data-stu-id="db6cc-105">The following example sets the <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> property of a <xref:System.Windows.Media.Imaging.BitmapImage> in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to reduce the memory required to load the image.</span></span>  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a><span data-ttu-id="db6cc-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="db6cc-106">Example</span></span>  
 <span data-ttu-id="db6cc-107">L’exemple suivant définit la <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> propriété d’un <xref:System.Windows.Media.Imaging.BitmapImage> dans le code afin de réduire la mémoire requise pour charger l’image.</span><span class="sxs-lookup"><span data-stu-id="db6cc-107">The following example sets the <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> property of a <xref:System.Windows.Media.Imaging.BitmapImage> in code to reduce the memory required to load the image.</span></span>  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a><span data-ttu-id="db6cc-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db6cc-108">See also</span></span>

- [<span data-ttu-id="db6cc-109">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="db6cc-109">Imaging Overview</span></span>](imaging-overview.md)
