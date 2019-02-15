---
title: 'Procédure : Animer un rectangle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], rectangles
- rectangles [WPF], animating
ms.assetid: 572ffb95-790d-4ace-adbf-b2ea8a90e75b
ms.openlocfilehash: dbff015bdc5f9ce56d2c366e0d348429efb7f4b5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305153"
---
# <a name="how-to-animate-a-rectangle"></a><span data-ttu-id="a1ce6-102">Procédure : Animer un rectangle</span><span class="sxs-lookup"><span data-stu-id="a1ce6-102">How to: Animate a Rectangle</span></span>
<span data-ttu-id="a1ce6-103">Cet exemple montre comment animer les modifications apportées à la taille et à la position d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="a1ce6-103">This example shows how to animate changes to the size and position of a rectangle.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1ce6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a1ce6-104">Example</span></span>  
 <span data-ttu-id="a1ce6-105">L’exemple suivant utilise une instance de la <xref:System.Windows.Media.Animation.RectAnimation> classe pour animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry>, qui anime les modifications apportées à la taille et la position du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a1ce6-105">The following example uses an instance of the <xref:System.Windows.Media.Animation.RectAnimation> class to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry>, which animates changes to the size and position of the rectangle.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/RectAnimationExample.cs#rectanimationwholepage)]
 [!code-vb[BasicAnimations_snip#RectAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/RectAnimationExample.vb#rectanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="a1ce6-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1ce6-106">See also</span></span>
- <xref:System.Windows.Media.Animation.RectAnimation>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.RectangleGeometry>
- [<span data-ttu-id="a1ce6-107">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="a1ce6-107">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [<span data-ttu-id="a1ce6-108">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="a1ce6-108">Graphics and Multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [<span data-ttu-id="a1ce6-109">Rubriques de procédures de graphiques</span><span class="sxs-lookup"><span data-stu-id="a1ce6-109">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="a1ce6-110">L’animation et minutage des rubriques de procédures</span><span class="sxs-lookup"><span data-stu-id="a1ce6-110">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
