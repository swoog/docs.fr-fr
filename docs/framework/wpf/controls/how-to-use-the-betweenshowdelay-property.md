---
title: 'Comment : utiliser la propriété BetweenShowDelay'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolTip control [WPF], BetweenShowDelay time property
- BetweenShowDelay time property [WPF]
ms.assetid: 984ea76d-f2a2-4326-a02e-f97ec3d036d6
ms.openlocfilehash: 7d48fb859ec6d37abd2490bc718d58cbdaa67f13
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552712"
---
# <a name="how-to-use-the-betweenshowdelay-property"></a><span data-ttu-id="58d2f-102">Comment : utiliser la propriété BetweenShowDelay</span><span class="sxs-lookup"><span data-stu-id="58d2f-102">How to: Use the BetweenShowDelay Property</span></span>
<span data-ttu-id="58d2f-103">Cet exemple montre comment utiliser le <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> propriété temporelle afin que les info-bulles apparaissent rapidement, avec peu ou pas de délai, lorsqu’un utilisateur déplace le pointeur de la souris à partir d’une info-bulle directement à un autre.</span><span class="sxs-lookup"><span data-stu-id="58d2f-103">This example shows how to use the <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> time property so that tooltips appear quickly—with little or no delay—when a user moves the mouse pointer from one tooltip directly to another.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58d2f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="58d2f-104">Example</span></span>  
 <span data-ttu-id="58d2f-105">Dans l’exemple suivant, la <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> est définie sur une seconde (1000 millisecondes) et le <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> est défini à deux secondes (2 000 millisecondes) pour les info-bulles des deux <xref:System.Windows.Shapes.Ellipse> contrôles.</span><span class="sxs-lookup"><span data-stu-id="58d2f-105">In the following example, the <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> property is set to one second (1000 milliseconds) and the <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> is set to two seconds (2000 milliseconds) for the tooltips of both <xref:System.Windows.Shapes.Ellipse> controls.</span></span> <span data-ttu-id="58d2f-106">Si vous l’info-bulle pour l’une des ellipses et puis déplacez le pointeur de la souris à un autre ellipse dans les deux secondes et pause sur celle-ci, l’info-bulle de la deuxième ellipse s’affiche immédiatement.</span><span class="sxs-lookup"><span data-stu-id="58d2f-106">If you display the tooltip for one of the ellipses and then move the mouse pointer to another ellipse within two seconds and pause on it, the tooltip of the second ellipse displays immediately.</span></span>  
  
 <span data-ttu-id="58d2f-107">Dans un des scénarios suivants, le <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> s’applique, ce qui entraîne l’info-bulle de la deuxième ellipse à attendre une seconde avant d’apparaître :</span><span class="sxs-lookup"><span data-stu-id="58d2f-107">In either of the following scenarios, the <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> applies, which causes the tooltip for the second ellipse to wait one second before it appears:</span></span>  
  
-   <span data-ttu-id="58d2f-108">Si le temps nécessaire pour atteindre le deuxième bouton est plus de deux secondes.</span><span class="sxs-lookup"><span data-stu-id="58d2f-108">If the time it takes to move to the second button is more than two seconds.</span></span>  
  
-   <span data-ttu-id="58d2f-109">Si l’info-bulle n’est pas visible au début de l’intervalle de temps pour la première ellipse.</span><span class="sxs-lookup"><span data-stu-id="58d2f-109">If the tooltip is not visible at the beginning of the time interval for the first ellipse.</span></span>  
  
 [!code-xaml[ToolTipService#ToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
[!code-xaml[ToolTipService#NoToolTip](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
## <a name="see-also"></a><span data-ttu-id="58d2f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58d2f-110">See Also</span></span>  
 <xref:System.Windows.Controls.ToolTip>  
 <xref:System.Windows.Controls.ToolTipService>  
 [<span data-ttu-id="58d2f-111">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="58d2f-111">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/tooltip-how-to-topics.md)  
 [<span data-ttu-id="58d2f-112">Vue d’ensemble de l’info-bulle</span><span class="sxs-lookup"><span data-stu-id="58d2f-112">ToolTip Overview</span></span>](../../../../docs/framework/wpf/controls/tooltip-overview.md)
