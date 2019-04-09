---
title: 'Procédure : Animer la position d’un objet à l’aide de PointAnimation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 1ef3f77e551affaa7e61d2aabf95f10c29275417
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59111304"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a><span data-ttu-id="30b86-102">Procédure : Animer la position d’un objet à l’aide de PointAnimation</span><span class="sxs-lookup"><span data-stu-id="30b86-102">How to: Animate the Position of an Object by Using PointAnimation</span></span>
<span data-ttu-id="30b86-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.PointAnimation> classe pour animer un objet sur un <xref:System.Windows.Shapes.Path>.</span><span class="sxs-lookup"><span data-stu-id="30b86-103">This example shows how to use the <xref:System.Windows.Media.Animation.PointAnimation> class to animate an object along a <xref:System.Windows.Shapes.Path>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="30b86-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="30b86-104">Example</span></span>  
 <span data-ttu-id="30b86-105">L’exemple suivant déplace une ellipse le long d’un <xref:System.Windows.Shapes.Path> à partir d’un point sur l’écran à un autre.</span><span class="sxs-lookup"><span data-stu-id="30b86-105">The following example moves an ellipse along a <xref:System.Windows.Shapes.Path> from one point on the screen to another.</span></span> <span data-ttu-id="30b86-106">L’exemple anime la position d’un <xref:System.Windows.Media.EllipseGeometry> à l’aide de <xref:System.Windows.Media.Animation.PointAnimation> pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="30b86-106">The example animates the position of an <xref:System.Windows.Media.EllipseGeometry> by using <xref:System.Windows.Media.Animation.PointAnimation> to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> property.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="30b86-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30b86-107">See also</span></span>

- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [<span data-ttu-id="30b86-108">Vue d'ensemble de l'animation</span><span class="sxs-lookup"><span data-stu-id="30b86-108">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="30b86-109">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="30b86-109">Graphics and Multimedia</span></span>](index.md)
- [<span data-ttu-id="30b86-110">Rubriques "Comment" relatives aux graphiques</span><span class="sxs-lookup"><span data-stu-id="30b86-110">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="30b86-111">Rubriques "Comment" relatives à l'animation et au minutage</span><span class="sxs-lookup"><span data-stu-id="30b86-111">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
