---
title: "Comment : faire pivoter un objet à l'aide d'un tracé géométrique"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
ms.assetid: cb31ca4d-f05a-4c6b-9a18-4b6faaf38d45
ms.openlocfilehash: 6d6d21f3f7b609cb2933093a6990425deb39d4a6
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43398146"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path"></a><span data-ttu-id="5e83a-102">Comment : faire pivoter un objet à l'aide d'un tracé géométrique</span><span class="sxs-lookup"><span data-stu-id="5e83a-102">How to: Rotate an Object by Using a Geometric Path</span></span>
<span data-ttu-id="5e83a-103">Cet exemple montre comment faire tourner (pivoter) un objet sur un tracé géométrique défini par un <xref:System.Windows.Media.PathGeometry> objet.</span><span class="sxs-lookup"><span data-stu-id="5e83a-103">This example shows how to rotate (pivot) an object along a geometric path that is defined by a <xref:System.Windows.Media.PathGeometry> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5e83a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5e83a-104">Example</span></span>  
 <span data-ttu-id="5e83a-105">L’exemple suivant utilise trois <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objets pour déplacer un rectangle sur un tracé géométrique.</span><span class="sxs-lookup"><span data-stu-id="5e83a-105">The following example uses three <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objects to move a rectangle along a geometric path.</span></span>  
  
-   <span data-ttu-id="5e83a-106">La première <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime un <xref:System.Windows.Media.RotateTransform> qui est appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="5e83a-106">The first <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates a <xref:System.Windows.Media.RotateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="5e83a-107">L’animation génère des valeurs d’angle.</span><span class="sxs-lookup"><span data-stu-id="5e83a-107">The animation generates angle values.</span></span> <span data-ttu-id="5e83a-108">Le rectangle tourne (pivote) ainsi sur les contours du tracé.</span><span class="sxs-lookup"><span data-stu-id="5e83a-108">It makes the rectangle rotate (pivot) along the contours of the path.</span></span>  
  
-   <span data-ttu-id="5e83a-109">Les deux autres objets animent les <xref:System.Windows.Media.TranslateTransform.X%2A> et <xref:System.Windows.Media.TranslateTransform.Y%2A> valeurs d’un <xref:System.Windows.Media.TranslateTransform> qui est appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="5e83a-109">The other two objects animate the <xref:System.Windows.Media.TranslateTransform.X%2A> and <xref:System.Windows.Media.TranslateTransform.Y%2A> values of a <xref:System.Windows.Media.TranslateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="5e83a-110">Le rectangle se déplace alors horizontalement et verticalement sur le tracé.</span><span class="sxs-lookup"><span data-stu-id="5e83a-110">They make the rectangle move horizontally and vertically along the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#RotateAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/rotateanimationusingpathexample.xaml#rotateanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/RotateAnimationUsingPathExample.cs#rotateanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/RotateAnimationUsingPathExample.vb#rotateanimationusingpathwholepage)]  
  
 <span data-ttu-id="5e83a-111">Une autre façon de faire pivoter un objet à l’aide d’un tracé géométrique consiste à utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> de l’objet et définissez son <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="5e83a-111">Another way to rotate an object by using a geometric path is to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object and set its <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> property to `true`.</span></span> <span data-ttu-id="5e83a-112">Pour plus d’informations et un exemple, consultez [faire pivoter un objet à l’aide d’un tracé géométrique (Animation de matrice)](../../../../docs/framework/wpf/graphics-multimedia/how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span><span class="sxs-lookup"><span data-stu-id="5e83a-112">For more information and an example, see [Rotate an Object by Using a Geometric Path (Matrix Animation)](../../../../docs/framework/wpf/graphics-multimedia/how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span></span>  
  
 <span data-ttu-id="5e83a-113">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="5e83a-113">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e83a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e83a-114">See Also</span></span>  
 [<span data-ttu-id="5e83a-115">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="5e83a-115">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="5e83a-116">Animation de tracés, exemple</span><span class="sxs-lookup"><span data-stu-id="5e83a-116">Path Animation Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160028)  
 [<span data-ttu-id="5e83a-117">Guides pratiques relatifs aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="5e83a-117">Path Animation How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
