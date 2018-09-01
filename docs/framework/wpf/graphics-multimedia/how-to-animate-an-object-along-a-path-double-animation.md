---
title: 'Comment : animer un objet sur un tracé (animation double)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (double animation)
- double animation [WPF]
ms.assetid: 5a3c4a99-f303-42ad-a52a-e4794bb1798e
ms.openlocfilehash: 3dcdf6cfe8631ae0b7b1472e22d027cf9288a1db
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43386220"
---
# <a name="how-to-animate-an-object-along-a-path-double-animation"></a><span data-ttu-id="2e6bc-102">Comment : animer un objet sur un tracé (animation double)</span><span class="sxs-lookup"><span data-stu-id="2e6bc-102">How to: Animate an Object Along a Path (Double Animation)</span></span>
<span data-ttu-id="2e6bc-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> classe pour déplacer un objet sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-103">This example shows how to use the <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> class to move an object along a path defined by a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e6bc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e6bc-104">Example</span></span>  
 <span data-ttu-id="2e6bc-105">L’exemple suivant utilise deux <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objets pour déplacer un rectangle sur un tracé géométrique :</span><span class="sxs-lookup"><span data-stu-id="2e6bc-105">The following example uses two <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objects to move a rectangle along a geometric path:</span></span>  
  
-   <span data-ttu-id="2e6bc-106">La première <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime le <xref:System.Windows.Media.TranslateTransform.X%2A> de la <xref:System.Windows.Media.TranslateTransform> appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-106">The first <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates the <xref:System.Windows.Media.TranslateTransform.X%2A> of the <xref:System.Windows.Media.TranslateTransform> applied to the rectangle.</span></span> <span data-ttu-id="2e6bc-107">Le rectangle se déplace alors horizontalement sur le tracé.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-107">It makes the rectangle move horizontally along the path.</span></span>  
  
-   <span data-ttu-id="2e6bc-108">La seconde <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime le <xref:System.Windows.Media.TranslateTransform.Y%2A> de la <xref:System.Windows.Media.TranslateTransform> appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-108">The second <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates the <xref:System.Windows.Media.TranslateTransform.Y%2A> of the <xref:System.Windows.Media.TranslateTransform> applied to the rectangle.</span></span> <span data-ttu-id="2e6bc-109">Le rectangle se déplace alors verticalement sur le tracé.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-109">It makes the rectangle move vertically along the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/doubleanimationusingpathexample.xaml#doubleanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/DoubleAnimationUsingPathExample.cs#doubleanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/DoubleAnimationUsingPathExample.vb#doubleanimationusingpathwholepage)]  
  
 <span data-ttu-id="2e6bc-110">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="2e6bc-110">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
 <span data-ttu-id="2e6bc-111">Une autre façon de déplacer un objet à l’aide d’un tracé géométrique consiste à utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet.</span><span class="sxs-lookup"><span data-stu-id="2e6bc-111">Another way to move an object using a geometric path is to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object.</span></span> <span data-ttu-id="2e6bc-112">Pour obtenir un exemple, consultez [animer un objet sur un tracé (Animation de matrice)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md).</span><span class="sxs-lookup"><span data-stu-id="2e6bc-112">For an example, see [Animate an Object Along a Path (Matrix Animation)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e6bc-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e6bc-113">See Also</span></span>  
 [<span data-ttu-id="2e6bc-114">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="2e6bc-114">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="2e6bc-115">Guides pratiques relatifs aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="2e6bc-115">Path Animation How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
