---
title: 'Procédure : Améliorer les performances d’un contrôle TreeView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], improving the performance
ms.assetid: b792c740-cf2b-4da8-8ba8-3d2e5a821874
ms.openlocfilehash: de1b46da2a7c6c3db0c0c19cdbb654fcf2fbbd6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153437"
---
# <a name="how-to-improve-the-performance-of-a-treeview"></a><span data-ttu-id="0ffe9-102">Procédure : Améliorer les performances d’un contrôle TreeView</span><span class="sxs-lookup"><span data-stu-id="0ffe9-102">How to: Improve the Performance of a TreeView</span></span>
<span data-ttu-id="0ffe9-103">Si un <xref:System.Windows.Controls.TreeView> contient de nombreux éléments, la quantité de temps de chargement peut provoquer un retard considérable dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-103">If a <xref:System.Windows.Controls.TreeView> contains many items, the amount of time it takes to load may cause a significant delay in the user interface.</span></span> <span data-ttu-id="0ffe9-104">Vous pouvez améliorer le temps de chargement en définissant le `VirtualizingStackPanel.IsVirtualizing` propriété jointe `true`.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-104">You can improve the load time by setting the `VirtualizingStackPanel.IsVirtualizing` attached property to `true`.</span></span>  <span data-ttu-id="0ffe9-105">L’interface utilisateur peut également être lente à réagir lorsqu’un utilisateur fait défiler le <xref:System.Windows.Controls.TreeView> à l’aide de la roulette de souris ou en faisant glisser le curseur d’une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-105">The UI might also be slow to react when a user scrolls the <xref:System.Windows.Controls.TreeView> by using the mouse wheel or dragging the thumb of a scrollbar.</span></span> <span data-ttu-id="0ffe9-106">Vous pouvez améliorer les performances de la <xref:System.Windows.Controls.TreeView> lorsque l’utilisateur fait défiler en définissant le `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-106">You can improve the performance of the <xref:System.Windows.Controls.TreeView> when the user scrolls by setting the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ffe9-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ffe9-107">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="0ffe9-108">Description</span><span class="sxs-lookup"><span data-stu-id="0ffe9-108">Description</span></span>  
<span data-ttu-id="0ffe9-109">L’exemple suivant crée un <xref:System.Windows.Controls.TreeView> qui définit le `VirtualizingStackPanel.IsVirtualizing` propriété jointe sur true et la `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> pour optimiser ses performances.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-109">The following example creates a <xref:System.Windows.Controls.TreeView> that sets the `VirtualizingStackPanel.IsVirtualizing` attached property to true and the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> to optimize its performance.</span></span>  
  
## <a name="code"></a><span data-ttu-id="0ffe9-110">Code</span><span class="sxs-lookup"><span data-stu-id="0ffe9-110">Code</span></span>  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 <span data-ttu-id="0ffe9-111">L’exemple suivant montre les données que l’exemple précédent utilise.</span><span class="sxs-lookup"><span data-stu-id="0ffe9-111">The following example shows the data that the previous example uses.</span></span>  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a><span data-ttu-id="0ffe9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ffe9-112">See also</span></span>

- [<span data-ttu-id="0ffe9-113">Contrôles</span><span class="sxs-lookup"><span data-stu-id="0ffe9-113">Controls</span></span>](../advanced/optimizing-performance-controls.md)
