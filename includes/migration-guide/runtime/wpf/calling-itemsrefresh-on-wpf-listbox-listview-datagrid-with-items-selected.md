---
ms.openlocfilehash: de73145273ad5aa5c19de55525417cfc3305b86d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803855"
---
### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>L’appel d’Items.Refresh dans un contrôle WPF ListBox, ListView ou DataGrid contenant des éléments sélectionnés peut provoquer l’apparition d’éléments en double.

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, si vous appelez ListBox.Items.Refresh à partir du code alors que des éléments sont sélectionnés dans une <xref:System.Windows.Controls.ListBox?displayProperty=name>, les éléments en question peuvent apparaître deux fois dans la liste. Un problème similaire se produit avec <xref:System.Windows.Controls.ListView?displayProperty=name> et <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Ce problème a été résolu dans le .NET Framework 4.6.|
|Suggestion|Pour contourner ce problème, vous pouvez désélectionner programmatiquement les éléments avant d’appeler <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name>, puis les resélectionner une fois l’appel effectué. Étant donné que ce problème a été résolu dans le .NET Framework 4.6, vous pouvez également mettre à niveau votre version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|
