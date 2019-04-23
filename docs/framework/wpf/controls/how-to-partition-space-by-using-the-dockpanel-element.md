---
title: 'Procédure : Partitionner l’espace à l’aide de l’élément DockPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], partitioning space
- partitioning space [WPF]
ms.assetid: a219b9e5-b205-4438-89b5-0a137ac463ab
ms.openlocfilehash: ab51270644bf370944ebc933c765b40c528681c5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59158884"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a><span data-ttu-id="a2e26-102">Procédure : Partitionner l’espace à l’aide de l’élément DockPanel</span><span class="sxs-lookup"><span data-stu-id="a2e26-102">How to: Partition Space by Using the DockPanel Element</span></span>
<span data-ttu-id="a2e26-103">L’exemple suivant crée un simple [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] framework à l’aide un <xref:System.Windows.Controls.DockPanel> élément.</span><span class="sxs-lookup"><span data-stu-id="a2e26-103">The following example creates a simple [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] framework using a <xref:System.Windows.Controls.DockPanel> element.</span></span> <span data-ttu-id="a2e26-104">Le <xref:System.Windows.Controls.DockPanel> partitionne l’espace disponible pour ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="a2e26-104">The <xref:System.Windows.Controls.DockPanel> partitions available space to its child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a2e26-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2e26-105">Example</span></span>  
 <span data-ttu-id="a2e26-106">Cet exemple utilise le <xref:System.Windows.Controls.DockPanel.Dock%2A> propriété, qui est une propriété jointe, pour ancrer deux identiques <xref:System.Windows.Controls.Border> éléments à la <xref:System.Windows.Controls.Dock.Top> de l’espace partitionné.</span><span class="sxs-lookup"><span data-stu-id="a2e26-106">This example uses the <xref:System.Windows.Controls.DockPanel.Dock%2A> property, which is an attached property, to dock two identical <xref:System.Windows.Controls.Border> elements at the <xref:System.Windows.Controls.Dock.Top> of the partitioned space.</span></span> <span data-ttu-id="a2e26-107">Une troisième <xref:System.Windows.Controls.Border> élément est ancré à le <xref:System.Windows.Controls.Dock.Left>, sa largeur est définie sur 200 pixels.</span><span class="sxs-lookup"><span data-stu-id="a2e26-107">A third <xref:System.Windows.Controls.Border> element is docked to the <xref:System.Windows.Controls.Dock.Left>, with its width set to 200 pixels.</span></span> <span data-ttu-id="a2e26-108">Une quatrième <xref:System.Windows.Controls.Border> est ancré à le <xref:System.Windows.Controls.Dock.Bottom> de l’écran.</span><span class="sxs-lookup"><span data-stu-id="a2e26-108">A fourth <xref:System.Windows.Controls.Border> is docked to the <xref:System.Windows.Controls.Dock.Bottom> of the screen.</span></span> <span data-ttu-id="a2e26-109">La dernière <xref:System.Windows.Controls.Border> élément remplit automatiquement l’espace restant.</span><span class="sxs-lookup"><span data-stu-id="a2e26-109">The last <xref:System.Windows.Controls.Border> element automatically fills the remaining space.</span></span>  
  
 [!code-cpp[DockPanelOvwSample#1](~/samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](~/samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
>  <span data-ttu-id="a2e26-110">Par défaut, le dernier enfant d’un <xref:System.Windows.Controls.DockPanel> élément remplit l’espace non alloué restant.</span><span class="sxs-lookup"><span data-stu-id="a2e26-110">By default, the last child of a <xref:System.Windows.Controls.DockPanel> element fills the remaining unallocated space.</span></span> <span data-ttu-id="a2e26-111">Si ce comportement ne vous convient pas, définissez `LastChildFill="False"`.</span><span class="sxs-lookup"><span data-stu-id="a2e26-111">If you do not want this behavior, set `LastChildFill="False"`.</span></span>  
  
 <span data-ttu-id="a2e26-112">L’application compilée produit une nouvelle IU qui ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="a2e26-112">The compiled application yields a new UI that looks like this.</span></span>  
  
 <span data-ttu-id="a2e26-113">![Scénario classique d’utilisation de l’élément DockPanel.](./media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")</span><span class="sxs-lookup"><span data-stu-id="a2e26-113">![A typical DockPanel scenario.](./media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2e26-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2e26-114">See also</span></span>

- <xref:System.Windows.Controls.DockPanel>
- [<span data-ttu-id="a2e26-115">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="a2e26-115">Panels Overview</span></span>](panels-overview.md)
