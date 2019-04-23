---
title: 'Procédure : Choisir entre StackPanel et DockPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], StackPanel control compared to
- StackPanel control [WPF], DockPanel control compared to
- controls [WPF], StackPanel
ms.assetid: f9239086-451f-42e6-81f7-ef89ef349742
ms.openlocfilehash: 8338421dfb1bea856c15edf9d324cec955584f9f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59206965"
---
# <a name="how-to-choose-between-stackpanel-and-dockpanel"></a><span data-ttu-id="943da-102">Procédure : Choisir entre StackPanel et DockPanel</span><span class="sxs-lookup"><span data-stu-id="943da-102">How to: Choose Between StackPanel and DockPanel</span></span>
<span data-ttu-id="943da-103">Cet exemple montre comment choisir entre l’utilisation d’un <xref:System.Windows.Controls.StackPanel> ou un <xref:System.Windows.Controls.DockPanel> pour empiler du contenu dans un <xref:System.Windows.Controls.Panel>.</span><span class="sxs-lookup"><span data-stu-id="943da-103">This example shows how to choose between using a <xref:System.Windows.Controls.StackPanel> or a <xref:System.Windows.Controls.DockPanel> when you stack content in a <xref:System.Windows.Controls.Panel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="943da-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="943da-104">Example</span></span>  
 <span data-ttu-id="943da-105">Bien que vous pouvez utiliser <xref:System.Windows.Controls.DockPanel> ou <xref:System.Windows.Controls.StackPanel> pour empiler des éléments enfants, les deux contrôles ne produisent pas toujours les mêmes résultats.</span><span class="sxs-lookup"><span data-stu-id="943da-105">Although you can use either <xref:System.Windows.Controls.DockPanel> or <xref:System.Windows.Controls.StackPanel> to stack child elements, the two controls do not always produce the same results.</span></span> <span data-ttu-id="943da-106">Par exemple, l’ordre que vous placez des éléments enfants peut affecter la taille des éléments enfants dans un <xref:System.Windows.Controls.DockPanel> , mais pas dans un <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="943da-106">For example, the order that you place child elements can affect the size of child elements in a <xref:System.Windows.Controls.DockPanel> but not in a <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="943da-107">Cette différence de comportement se produit parce que <xref:System.Windows.Controls.StackPanel> mesures dans le sens de l’empilement en <xref:System.Double>.<xref:System.Double.PositiveInfinity>; Toutefois, <xref:System.Windows.Controls.DockPanel> mesure uniquement la taille disponible.</span><span class="sxs-lookup"><span data-stu-id="943da-107">This different behavior occurs because <xref:System.Windows.Controls.StackPanel> measures in the direction of stacking at <xref:System.Double>.<xref:System.Double.PositiveInfinity>; however, <xref:System.Windows.Controls.DockPanel> measures only the available size.</span></span>  
  
 <span data-ttu-id="943da-108">L’exemple suivant illustre cette différence clé entre <xref:System.Windows.Controls.DockPanel> et <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="943da-108">The following example demonstrates this key difference between <xref:System.Windows.Controls.DockPanel> and <xref:System.Windows.Controls.StackPanel>.</span></span>  
  
 [!code-cpp[StackPanelOvw4#1](~/samples/snippets/cpp/VS_Snippets_Wpf/StackPanelOvw4/CPP/StackPanel_Ovw_Sample4.cpp#1)]
 [!code-csharp[StackPanelOvw4#1](~/samples/snippets/csharp/VS_Snippets_Wpf/StackPanelOvw4/CSharp/StackPanel_Ovw_Sample4.cs#1)]
 [!code-vb[StackPanelOvw4#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StackPanelOvw4/VisualBasic/StackPanelSamp.vb#1)]
 [!code-xaml[StackPanelOvw4#1](~/samples/snippets/xaml/VS_Snippets_Wpf/StackPanelOvw4/XAML/default.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="943da-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="943da-109">See also</span></span>

- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.DockPanel>
- [<span data-ttu-id="943da-110">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="943da-110">Panels Overview</span></span>](panels-overview.md)
