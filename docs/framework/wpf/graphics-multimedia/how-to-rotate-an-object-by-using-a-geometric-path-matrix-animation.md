---
title: 'Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique (animation de matrice)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
- matrix animation [WPF]
ms.assetid: 877dc9aa-6bdc-4beb-8772-3efaec32c0f0
ms.openlocfilehash: 8f1b0ac42ea7509f8bc22b0bd2f50e2f96b5bee5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59087883"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation"></a><span data-ttu-id="834c2-102">Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique (animation de matrice)</span><span class="sxs-lookup"><span data-stu-id="834c2-102">How to: Rotate an Object by Using a Geometric Path (Matrix Animation)</span></span>
<span data-ttu-id="834c2-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> et un <xref:System.Windows.Media.MatrixTransform> à faire tourner (pivoter) un objet le long d’un tracé géométrique défini par un <xref:System.Windows.Media.PathGeometry> objet.</span><span class="sxs-lookup"><span data-stu-id="834c2-103">This example shows how to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> and a <xref:System.Windows.Media.MatrixTransform> to rotate (pivot) an object along a geometric path defined by a <xref:System.Windows.Media.PathGeometry> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="834c2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="834c2-104">Example</span></span>  
 <span data-ttu-id="834c2-105">L’exemple suivant utilise le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet à animer le <xref:System.Windows.Media.MatrixTransform.Matrix%2A> propriété d’un <xref:System.Windows.Media.MatrixTransform>.</span><span class="sxs-lookup"><span data-stu-id="834c2-105">The following example uses the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object to animate the <xref:System.Windows.Media.MatrixTransform.Matrix%2A> property of a <xref:System.Windows.Media.MatrixTransform>.</span></span> <span data-ttu-id="834c2-106">Le <xref:System.Windows.Media.MatrixTransform> est appliqué à un bouton et oblige ce dernier à déplacer sur un tracé courbé.</span><span class="sxs-lookup"><span data-stu-id="834c2-106">The <xref:System.Windows.Media.MatrixTransform> is applied to a button and causes it to move along a curved path.</span></span> <span data-ttu-id="834c2-107">Étant donné que le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété est définie sur `true`, le rectangle pivote le long de la tangente du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="834c2-107">Because the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> property is set to `true`, the rectangle rotates along the tangent of the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathdoesrotatewithtangentexample.xaml#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathDoesRotateWithTangentExample.cs#matrixanimationusingpathdoesrotatewithtangentwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathDoesRotateWithTangentExample.vb#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 <span data-ttu-id="834c2-108">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="834c2-108">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
 <span data-ttu-id="834c2-109">La version du code de l’exemple précédent utilisé un <xref:System.Windows.Media.Animation.Storyboard> pour animer la <xref:System.Windows.Media.EllipseGeometry>, bien qu’une seule animation ait été appliquée.</span><span class="sxs-lookup"><span data-stu-id="834c2-109">The code version of the preceding sample used a <xref:System.Windows.Media.Animation.Storyboard> to animate the <xref:System.Windows.Media.EllipseGeometry>, even though only one animation was applied.</span></span> <span data-ttu-id="834c2-110">Appliquer une seule animation à une propriété dans le code d’un moyen plus simple consiste à utiliser le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="834c2-110">An easier way to apply a single animation to a property in code is to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method.</span></span> <span data-ttu-id="834c2-111">Si vous voulez voir un exemple, consultez l’article [Comment : animer une propriété sans utiliser de storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="834c2-111">For an example, see [Animate a Property Without Using a Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="834c2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="834c2-112">See also</span></span>

- [<span data-ttu-id="834c2-113">Vue d'ensemble de l'animation</span><span class="sxs-lookup"><span data-stu-id="834c2-113">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="834c2-114">Rubriques "Comment" relatives aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="834c2-114">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
- [<span data-ttu-id="834c2-115">Animation de tracés, exemple</span><span class="sxs-lookup"><span data-stu-id="834c2-115">Path Animation Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160028)
