---
title: "Procédure : Améliorer les performances d'un contrôle TreeView"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], improving the performance
ms.assetid: b792c740-cf2b-4da8-8ba8-3d2e5a821874
ms.openlocfilehash: 3c7bd151e1c8a5f318660cc45702b5b9c98534a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54500692"
---
# <a name="how-to-improve-the-performance-of-a-treeview"></a>Procédure : Améliorer les performances d'un contrôle TreeView
Si un <xref:System.Windows.Controls.TreeView> contient de nombreux éléments, la quantité de temps de chargement peut provoquer un retard considérable dans l’interface utilisateur. Vous pouvez améliorer le temps de chargement en définissant le `VirtualizingStackPanel.IsVirtualizing` propriété jointe `true`.  L’interface utilisateur peut également être lente à réagir lorsqu’un utilisateur fait défiler le <xref:System.Windows.Controls.TreeView> à l’aide de la roulette de souris ou en faisant glisser le curseur d’une barre de défilement. Vous pouvez améliorer les performances de la <xref:System.Windows.Controls.TreeView> lorsque l’utilisateur fait défiler en définissant le `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.  
  
## <a name="example"></a>Exemple  
  
## <a name="description"></a>Description  
L’exemple suivant crée un <xref:System.Windows.Controls.TreeView> qui définit le `VirtualizingStackPanel.IsVirtualizing` propriété jointe sur true et la `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> pour optimiser ses performances.  
  
## <a name="code"></a>Code  
 [!code-xaml[RecycleItemContainerShippets#VirtualizingTreeView](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizingtreeview)]  
  
 L’exemple suivant montre les données que l’exemple précédent utilise.  
  
 [!code-csharp[RecycleItemContainerShippets#TreeViewData](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#treeviewdata)]
 [!code-vb[RecycleItemContainerShippets#TreeViewData](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#treeviewdata)]  
  
## <a name="see-also"></a>Voir aussi
- [Contrôles](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)
