---
title: "Procédure : Animer la position d'un objet à l'aide de PointAnimation"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 04dbcfdb64525e6231ecf33c8ac5ecf2a2d2cb7e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357927"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a><span data-ttu-id="78da8-102">Procédure : Animer la position d'un objet à l'aide de PointAnimation</span><span class="sxs-lookup"><span data-stu-id="78da8-102">How to: Animate the Position of an Object by Using PointAnimation</span></span>
<span data-ttu-id="78da8-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.PointAnimation> classe pour animer un objet sur un <xref:System.Windows.Shapes.Path>.</span><span class="sxs-lookup"><span data-stu-id="78da8-103">This example shows how to use the <xref:System.Windows.Media.Animation.PointAnimation> class to animate an object along a <xref:System.Windows.Shapes.Path>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78da8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="78da8-104">Example</span></span>  
 <span data-ttu-id="78da8-105">L’exemple suivant déplace une ellipse le long d’un <xref:System.Windows.Shapes.Path> à partir d’un point sur l’écran à un autre.</span><span class="sxs-lookup"><span data-stu-id="78da8-105">The following example moves an ellipse along a <xref:System.Windows.Shapes.Path> from one point on the screen to another.</span></span> <span data-ttu-id="78da8-106">L’exemple anime la position d’un <xref:System.Windows.Media.EllipseGeometry> à l’aide de <xref:System.Windows.Media.Animation.PointAnimation> pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="78da8-106">The example animates the position of an <xref:System.Windows.Media.EllipseGeometry> by using <xref:System.Windows.Media.Animation.PointAnimation> to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> property.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="78da8-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78da8-107">See also</span></span>
- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [<span data-ttu-id="78da8-108">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="78da8-108">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="78da8-109">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="78da8-109">Graphics and Multimedia</span></span>](index.md)
- [<span data-ttu-id="78da8-110">Rubriques de procédures de graphiques</span><span class="sxs-lookup"><span data-stu-id="78da8-110">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="78da8-111">L’animation et minutage des rubriques de procédures</span><span class="sxs-lookup"><span data-stu-id="78da8-111">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
