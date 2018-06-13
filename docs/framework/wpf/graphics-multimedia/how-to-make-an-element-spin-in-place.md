---
title: 'Comment : mettre un élément en rotation'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], spinning elements
- spinning elements [WPF]
ms.assetid: 1f011976-8b07-4c31-9faf-019e0ddaa24c
ms.openlocfilehash: a37952af621c79d231b45a247c92d3576a533580
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33562509"
---
# <a name="how-to-make-an-element-spin-in-place"></a><span data-ttu-id="2635e-102">Comment : mettre un élément en rotation</span><span class="sxs-lookup"><span data-stu-id="2635e-102">How to: Make an Element Spin in Place</span></span>
<span data-ttu-id="2635e-103">Cet exemple montre comment mettre un élément en rotation à l’aide un <xref:System.Windows.Media.RotateTransform> et un <xref:System.Windows.Media.Animation.DoubleAnimation>.</span><span class="sxs-lookup"><span data-stu-id="2635e-103">This example shows how to make an element spin by using a <xref:System.Windows.Media.RotateTransform> and a <xref:System.Windows.Media.Animation.DoubleAnimation>.</span></span>  
  
 <span data-ttu-id="2635e-104">L’exemple suivant applique la <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2635e-104">The following example applies the <xref:System.Windows.Media.RotateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of the element.</span></span> <span data-ttu-id="2635e-105">L’exemple utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la <xref:System.Windows.Media.RotateTransform.Angle%2A> de la <xref:System.Windows.Media.RotateTransform>.</span><span class="sxs-lookup"><span data-stu-id="2635e-105">The example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the <xref:System.Windows.Media.RotateTransform.Angle%2A> of the <xref:System.Windows.Media.RotateTransform>.</span></span> <span data-ttu-id="2635e-106">Pour rendre l’élément à mettre en place, l’exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété de l’élément sur le point (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="2635e-106">To make the element spin in place, the example sets the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property of the element to the point (0.5, 0.5).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2635e-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="2635e-107">Example</span></span>  
 [!code-xaml[transformanimations_snip#11](../../../../samples/snippets/xaml/VS_Snippets_Wpf/transformanimations_snip/XAML/RotateAboutCenterExample.xaml#11)]  
  
 <span data-ttu-id="2635e-108">Pour l’exemple complet, qui inclut plusieurs exemples de transformation, consultez [Transformations 2D, exemple](http://go.microsoft.com/fwlink/?LinkID=158252).</span><span class="sxs-lookup"><span data-stu-id="2635e-108">For the complete sample, which includes more transformation examples, see [2-D Transforms Sample](http://go.microsoft.com/fwlink/?LinkID=158252).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2635e-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2635e-109">See Also</span></span>  
 [<span data-ttu-id="2635e-110">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="2635e-110">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="2635e-111">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="2635e-111">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
