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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052181"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a><span data-ttu-id="55684-102">Procédure : Partitionner l’espace à l’aide de l’élément DockPanel</span><span class="sxs-lookup"><span data-stu-id="55684-102">How to: Partition Space by Using the DockPanel Element</span></span>
<span data-ttu-id="55684-103">L’exemple suivant crée un simple [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] framework à l’aide un <xref:System.Windows.Controls.DockPanel> élément.</span><span class="sxs-lookup"><span data-stu-id="55684-103">The following example creates a simple [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] framework using a <xref:System.Windows.Controls.DockPanel> element.</span></span> <span data-ttu-id="55684-104">Le <xref:System.Windows.Controls.DockPanel> partitionne l’espace disponible pour ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="55684-104">The <xref:System.Windows.Controls.DockPanel> partitions available space to its child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55684-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="55684-105">Example</span></span>  
 <span data-ttu-id="55684-106">Cet exemple utilise le <xref:System.Windows.Controls.DockPanel.Dock%2A> propriété, qui est une propriété jointe, pour ancrer deux identiques <xref:System.Windows.Controls.Border> éléments à la <xref:System.Windows.Controls.Dock.Top> de l’espace partitionné.</span><span class="sxs-lookup"><span data-stu-id="55684-106">This example uses the <xref:System.Windows.Controls.DockPanel.Dock%2A> property, which is an attached property, to dock two identical <xref:System.Windows.Controls.Border> elements at the <xref:System.Windows.Controls.Dock.Top> of the partitioned space.</span></span> <span data-ttu-id="55684-107">Une troisième <xref:System.Windows.Controls.Border> élément est ancré à le <xref:System.Windows.Controls.Dock.Left>, sa largeur est définie sur 200 pixels.</span><span class="sxs-lookup"><span data-stu-id="55684-107">A third <xref:System.Windows.Controls.Border> element is docked to the <xref:System.Windows.Controls.Dock.Left>, with its width set to 200 pixels.</span></span> <span data-ttu-id="55684-108">Une quatrième <xref:System.Windows.Controls.Border> est ancré à le <xref:System.Windows.Controls.Dock.Bottom> de l’écran.</span><span class="sxs-lookup"><span data-stu-id="55684-108">A fourth <xref:System.Windows.Controls.Border> is docked to the <xref:System.Windows.Controls.Dock.Bottom> of the screen.</span></span> <span data-ttu-id="55684-109">La dernière <xref:System.Windows.Controls.Border> élément remplit automatiquement l’espace restant.</span><span class="sxs-lookup"><span data-stu-id="55684-109">The last <xref:System.Windows.Controls.Border> element automatically fills the remaining space.</span></span>  
  
 [!code-cpp[DockPanelOvwSample#1](~/samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](~/samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
>  <span data-ttu-id="55684-110">Par défaut, le dernier enfant d’un <xref:System.Windows.Controls.DockPanel> élément remplit l’espace non alloué restant.</span><span class="sxs-lookup"><span data-stu-id="55684-110">By default, the last child of a <xref:System.Windows.Controls.DockPanel> element fills the remaining unallocated space.</span></span> <span data-ttu-id="55684-111">Si ce comportement ne vous convient pas, définissez `LastChildFill="False"`.</span><span class="sxs-lookup"><span data-stu-id="55684-111">If you do not want this behavior, set `LastChildFill="False"`.</span></span>  
  
 <span data-ttu-id="55684-112">L’application compilée produit une nouvelle IU qui ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="55684-112">The compiled application yields a new UI that looks like this.</span></span>  
  
 <span data-ttu-id="55684-113">![Scénario classique d’utilisation de l’élément DockPanel.](./media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")</span><span class="sxs-lookup"><span data-stu-id="55684-113">![A typical DockPanel scenario.](./media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55684-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55684-114">See also</span></span>

- <xref:System.Windows.Controls.DockPanel>
- [<span data-ttu-id="55684-115">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="55684-115">Panels Overview</span></span>](panels-overview.md)
