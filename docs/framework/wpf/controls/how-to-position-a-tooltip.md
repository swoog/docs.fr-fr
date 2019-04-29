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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770901"
---
# <a name="how-to-position-a-tooltip"></a>Procédure : Positionner une info-bulle
Cet exemple montre comment spécifier la position d’une info-bulle sur l’écran.  
  
## <a name="example"></a>Exemple  
 Vous pouvez positionner une info-bulle à l’aide d’un ensemble de cinq propriétés sont définies dans les deux le <xref:System.Windows.Controls.ToolTip> et <xref:System.Windows.Controls.ToolTipService> classes. Le tableau suivant illustre ces deux ensembles de cinq propriétés et fournit des liens vers leur documentation de référence en fonction de la classe.  
  
### <a name="corresponding-tooltip-properties-according-to-class"></a>Propriétés d’info-bulle correspondant en fonction de classe  
  
|<xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> propriétés de la classe|<xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> propriétés de la classe|  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Windows.Controls.ToolTip.Placement%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.Placement%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementTarget%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementTarget%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementRectangle%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementRectangle%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.HorizontalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.HorizontalOffset%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.VerticalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.VerticalOffset%2A?displayProperty=nameWithType>|  
  
 Si vous définissez le contenu d’une info-bulle à l’aide un <xref:System.Windows.Controls.ToolTip> de l’objet, vous pouvez utiliser les propriétés de classe ; Toutefois, le <xref:System.Windows.Controls.ToolTipService> propriétés sont prioritaires. Utilisez le <xref:System.Windows.Controls.ToolTipService> propriétés pour les info-bulles qui ne sont pas définies comme <xref:System.Windows.Controls.ToolTip> objets.  
  
 Les illustrations suivantes montrent comment positionner une info-bulle à l’aide de ces propriétés. Bien que, le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples dans ces illustrations montrent comment définir les propriétés qui sont définies par le <xref:System.Windows.Controls.ToolTip> classe, les propriétés correspondantes de la <xref:System.Windows.Controls.ToolTipService> classe suivent les mêmes règles de mise en page. Pour plus d’informations sur les valeurs possibles pour la propriété de positionnement, consultez [comportement de positionnement de Popup](popup-placement-behavior.md).  
 
 L’illustration suivante montre le placement de l’info-bulle à l’aide de la propriété de positionnement :  
  
 ![Diagramme montrant le placement de l’info-bulle à l’aide de la propriété de positionnement.](./media/how-to-position-a-tooltip/tooltip-placement-property.png)
 
 L’illustration suivante montre le placement de l’info-bulle à l’aide des propriétés Placement et PlacementRectangle :   

 ![Diagramme montrant le placement de l’info-bulle à l’aide d’une propriété PlacementRectangle.](./media/how-to-position-a-tooltip/tooltip-placement-rectangle-property.png)  
 
 L’illustration suivante montre le placement de l’info-bulle à l’aide des propriétés Placement, PlacementRectangle et Offset :   
  
 ![Diagramme montrant le placement de l’info-bulle à l’aide de la propriété de décalage.](./media/how-to-position-a-tooltip/tooltip-placement-offset-property.png)

 L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.ToolTip> propriétés pour spécifier la position d’une info-bulle dont le contenu est un <xref:System.Windows.Controls.ToolTip> objet.  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
  
 [!code-csharp[ToolTipService#ToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#tooltipcode)]
 [!code-vb[ToolTipService#ToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#tooltipcode)]  
  
 L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.ToolTipService> propriétés pour spécifier la position d’une info-bulle dont le contenu n’est pas un <xref:System.Windows.Controls.ToolTip> objet.  
  
 [!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
 [!code-csharp[ToolTipService#NoToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#notooltipcode)]
 [!code-vb[ToolTipService#NoToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#notooltipcode)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [Rubriques de guide pratique](tooltip-how-to-topics.md)
- [Vue d’ensemble de l’info-bulle](tooltip-overview.md)
