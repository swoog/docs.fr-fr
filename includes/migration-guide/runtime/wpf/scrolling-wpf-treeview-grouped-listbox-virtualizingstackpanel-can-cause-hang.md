---
ms.openlocfilehash: 0887379fb23e9e66c6cc55a3774545162634c3f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803845"
---
### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Le défilement d’un TreeView ou d’une ListBox groupée WPF dans un VirtualizingStackPanel peut provoquer un blocage

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, le défilement d’un contrôle <xref:System.Windows.Controls.TreeView?displayProperty=name> WPF dans un panneau d’empilement virtualisé peut provoquer un blocage si la fenêtre d’affichage comporte des marges (par exemple entre les éléments du <xref:System.Windows.Controls.TreeView?displayProperty=name> ou sur un élément ItemsPresenter). En outre, dans certains cas, des éléments de taille différente dans une même vue peuvent causer une instabilité, même s’il n’y a pas de marges.|
|Suggestion|Vous pouvez éviter ce problème en effectuant une mise à niveau vers .NET Framework 4.5.1. Vous pouvez également supprimer les marges des collections de vue (comme les <xref:System.Windows.Controls.TreeView?displayProperty=name>s) dans les panneaux d’empilement virtualisés, si tous les éléments qu’ils contiennent sont de même taille.|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|
