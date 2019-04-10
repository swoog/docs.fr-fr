---
title: 'Procédure : Positionner une info-bulle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolTip control [WPF], positioning
- positioning ToolTip controls [WPF]
ms.assetid: cddf3757-9e5f-4ce3-a6eb-44489cf3804a
ms.openlocfilehash: 811818fe6e7c0d8ce9e2aa058b42bf592ada4b92
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212347"
---
# <a name="how-to-position-a-tooltip"></a><span data-ttu-id="599ba-102">Procédure : Positionner une info-bulle</span><span class="sxs-lookup"><span data-stu-id="599ba-102">How to: Position a ToolTip</span></span>
<span data-ttu-id="599ba-103">Cet exemple montre comment spécifier la position d’une info-bulle sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="599ba-103">This example shows how to specify the position of a tooltip on the screen.</span></span>  
  
## <a name="example"></a><span data-ttu-id="599ba-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="599ba-104">Example</span></span>  
 <span data-ttu-id="599ba-105">Vous pouvez positionner une info-bulle à l’aide d’un ensemble de cinq propriétés sont définies dans les deux le <xref:System.Windows.Controls.ToolTip> et <xref:System.Windows.Controls.ToolTipService> classes.</span><span class="sxs-lookup"><span data-stu-id="599ba-105">You can position a tooltip by using a set of five properties that are defined in both the <xref:System.Windows.Controls.ToolTip> and <xref:System.Windows.Controls.ToolTipService> classes.</span></span> <span data-ttu-id="599ba-106">Le tableau suivant illustre ces deux ensembles de cinq propriétés et fournit des liens vers leur documentation de référence en fonction de la classe.</span><span class="sxs-lookup"><span data-stu-id="599ba-106">The following table shows these two sets of five properties and provides links to their reference documentation according to class.</span></span>  
  
### <a name="corresponding-tooltip-properties-according-to-class"></a><span data-ttu-id="599ba-107">Propriétés d’info-bulle correspondant en fonction de classe</span><span class="sxs-lookup"><span data-stu-id="599ba-107">Corresponding tooltip properties according to class</span></span>  
  
|<xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> <span data-ttu-id="599ba-108">propriétés de la classe</span><span class="sxs-lookup"><span data-stu-id="599ba-108">class properties</span></span>|<xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> <span data-ttu-id="599ba-109">propriétés de la classe</span><span class="sxs-lookup"><span data-stu-id="599ba-109">class properties</span></span>|  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Windows.Controls.ToolTip.Placement%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.Placement%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementTarget%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementTarget%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementRectangle%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementRectangle%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.HorizontalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.HorizontalOffset%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.VerticalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.VerticalOffset%2A?displayProperty=nameWithType>|  
  
 <span data-ttu-id="599ba-110">Si vous définissez le contenu d’une info-bulle à l’aide un <xref:System.Windows.Controls.ToolTip> de l’objet, vous pouvez utiliser les propriétés de classe ; Toutefois, le <xref:System.Windows.Controls.ToolTipService> propriétés sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="599ba-110">If you define the contents of a tooltip by using a <xref:System.Windows.Controls.ToolTip> object, you can use the properties of either class; however, the <xref:System.Windows.Controls.ToolTipService> properties take precedence.</span></span> <span data-ttu-id="599ba-111">Utilisez le <xref:System.Windows.Controls.ToolTipService> propriétés pour les info-bulles qui ne sont pas définies comme <xref:System.Windows.Controls.ToolTip> objets.</span><span class="sxs-lookup"><span data-stu-id="599ba-111">Use the <xref:System.Windows.Controls.ToolTipService> properties for tooltips that are not defined as <xref:System.Windows.Controls.ToolTip> objects.</span></span>  
  
 <span data-ttu-id="599ba-112">Les illustrations suivantes montrent comment positionner une info-bulle à l’aide de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="599ba-112">The following illustrations show how to position a tooltip by using these properties.</span></span> <span data-ttu-id="599ba-113">Bien que, le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples dans ces illustrations montrent comment définir les propriétés qui sont définies par le <xref:System.Windows.Controls.ToolTip> classe, les propriétés correspondantes de la <xref:System.Windows.Controls.ToolTipService> classe suivent les mêmes règles de mise en page.</span><span class="sxs-lookup"><span data-stu-id="599ba-113">Although, the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] examples in these illustrations show how to set the properties that are defined by the <xref:System.Windows.Controls.ToolTip> class, the corresponding properties of the <xref:System.Windows.Controls.ToolTipService> class follow the same layout rules.</span></span> <span data-ttu-id="599ba-114">Pour plus d’informations sur les valeurs possibles pour la propriété de positionnement, consultez [comportement de positionnement de Popup](popup-placement-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="599ba-114">For more information about the possible values for the Placement property, see [Popup Placement Behavior](popup-placement-behavior.md).</span></span>  
 
 <span data-ttu-id="599ba-115">L’illustration suivante montre le placement de l’info-bulle à l’aide de la propriété de positionnement :</span><span class="sxs-lookup"><span data-stu-id="599ba-115">The following image shows tooltip placement by using the Placement property:</span></span>  
  
 ![Diagramme montrant le placement de l’info-bulle à l’aide de la propriété de positionnement.](./media/how-to-position-a-tooltip/tooltip-placement-property.png)
 
 <span data-ttu-id="599ba-117">L’illustration suivante montre le placement de l’info-bulle à l’aide des propriétés Placement et PlacementRectangle :</span><span class="sxs-lookup"><span data-stu-id="599ba-117">The following image shows tooltip placement by using the Placement and PlacementRectangle properties:</span></span>   

 ![Diagramme montrant le placement de l’info-bulle à l’aide d’une propriété PlacementRectangle.](./media/how-to-position-a-tooltip/tooltip-placement-rectangle-property.png)  
 
 <span data-ttu-id="599ba-119">L’illustration suivante montre le placement de l’info-bulle à l’aide des propriétés Placement, PlacementRectangle et Offset :</span><span class="sxs-lookup"><span data-stu-id="599ba-119">The following image shows tooltip placement by using the Placement, PlacementRectangle, and Offset properties:</span></span>   
  
 ![Diagramme montrant le placement de l’info-bulle à l’aide de la propriété de décalage.](./media/how-to-position-a-tooltip/tooltip-placement-offset-property.png)

 <span data-ttu-id="599ba-121">L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.ToolTip> propriétés pour spécifier la position d’une info-bulle dont le contenu est un <xref:System.Windows.Controls.ToolTip> objet.</span><span class="sxs-lookup"><span data-stu-id="599ba-121">The following example shows how to use the <xref:System.Windows.Controls.ToolTip> properties to specify the position of a tooltip whose content is a <xref:System.Windows.Controls.ToolTip> object.</span></span>  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
  
 [!code-csharp[ToolTipService#ToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#tooltipcode)]
 [!code-vb[ToolTipService#ToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#tooltipcode)]  
  
 <span data-ttu-id="599ba-122">L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.ToolTipService> propriétés pour spécifier la position d’une info-bulle dont le contenu n’est pas un <xref:System.Windows.Controls.ToolTip> objet.</span><span class="sxs-lookup"><span data-stu-id="599ba-122">The following example shows how to use the <xref:System.Windows.Controls.ToolTipService> properties to specify the position of a tooltip whose content is not a <xref:System.Windows.Controls.ToolTip> object.</span></span>  
  
 [!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
 [!code-csharp[ToolTipService#NoToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#notooltipcode)]
 [!code-vb[ToolTipService#NoToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#notooltipcode)]  
  
## <a name="see-also"></a><span data-ttu-id="599ba-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="599ba-123">See also</span></span>

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [<span data-ttu-id="599ba-124">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="599ba-124">How-to Topics</span></span>](tooltip-how-to-topics.md)
- [<span data-ttu-id="599ba-125">Vue d'ensemble de l'info-bulle</span><span class="sxs-lookup"><span data-stu-id="599ba-125">ToolTip Overview</span></span>](tooltip-overview.md)
