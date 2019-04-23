---
ms.openlocfilehash: b761cb699c4677f815835cdab9c6aa3039f5bb38
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235323"
---
### <a name="listboxitem-isselected-binding-issue-with-observablecollectiontmove"></a>Problème de liaison ListBoxItem IsSelected avec ObservableCollection\<T>.Move

|   |   |
|---|---|
|Détails|L’appel de <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> ou de <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> sur une collection liée à un <xref:System.Windows.Controls.ListBox?displayProperty=name> avec des éléments sélectionnés peut entraîner un comportement imprévisible avec une sélection ultérieure ou la désélection d’éléments de <xref:System.Windows.Controls.ListBox?displayProperty=name>.|
|Suggestion|L’appel de <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> et de <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> au lieu de <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> permet de contourner ce problème. Étant donné que ce problème a été résolu dans le .NET Framework 4.6, vous pouvez également mettre à niveau votre version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
