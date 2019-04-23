---
ms.openlocfilehash: 88e00454894c8404fd48e92404e35ae27fa056f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235224"
---
### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>Les éléments TreeViewItem WPF doivent être utilisés dans un contrôle TreeView

|   |   |
|---|---|
|Détails|Une modification a été introduite dans 4.5, qui limite l’utilisation des éléments <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> en dehors d’un <xref:System.Windows.Controls.TreeView?displayProperty=name>. Cette restriction est applicable dans les cas suivants :<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>Le visuel parent n’est pas un panneau. (Un <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> généré pour un <xref:System.Windows.Controls.TreeView?displayProperty=name> aura un panneau comme parent)</li><li>Le <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> est un descendant d’un <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> agissant comme « hôte des éléments » pour un contrôle de liste (ListBox, DataGrid, ListView, etc.). Il n’est pas nécessaire d’activer la virtualisation.</li><li>Le <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> peut faire défiler les éléments (<code>ScrollUnit=&quot;Item&quot;</code>).</li><li><code>VirtualizingStackPanel.MakeVisible(v)</code> est appelé pour faire défiler un élément <code>v</code> dans l’affichage. Vous pouvez faire ceci de manière explicite ou implicite de différentes façons. Le moyen le plus courant est de cliquer sur <code>v</code> pour lui donner le focus clavier.</li><li>La chaîne du parent visuel de <code>v</code> à <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> passe par <xref:System.Windows.Controls.TreeViewItem?displayProperty=name>.</li></ul>En d’autres termes, cela se produit quand un <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> est utilisé en dehors d’un <xref:System.Windows.Controls.TreeView?displayProperty=name>, et que l’utilisateur clique sur un descendant du <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> pour l’afficher. Si le <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> n’a pas de descendant pouvant recevoir le focus, vous ne rencontrez jamais ce problème. Cela peut se produire quand un <xref:System.Windows.Controls.TreeViewItem?displayProperty=name> est la racine d’un DataTemplate. Une exception InvalidCastException est alors levée dans le cadre de WPF.|
|Suggestion|Un correctif sera mis à disposition pour résoudre ce problème.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
