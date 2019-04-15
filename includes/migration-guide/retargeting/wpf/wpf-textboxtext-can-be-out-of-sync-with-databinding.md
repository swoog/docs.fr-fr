---
ms.openlocfilehash: 8b0617d8f021a9534289fd7ae8539cd054684862
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234685"
---
### <a name="wpf-textboxtext-can-be-out-of-sync-with-databinding"></a>Dans WPF, TextBox.Text et la liaison de données peuvent être désynchronisés

|   |   |
|---|---|
|Détails|Dans certains cas, la propriété <xref:System.Windows.Controls.TextBox.Text> reflète une valeur précédente de la propriété liée aux données si cette propriété est modifiée au cours d'une opération d'écriture de liaison de données.|
|Suggestion|Cela ne doit pas avoir d'impact négatif. Vous pouvez, cependant, restaurer le comportement précédent en affectant à la propriété <xref:System.Windows.FrameworkCompatibilityPreferences.KeepTextBoxDisplaySynchronizedWithTextProperty> la valeur <code>false</code>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox.Text?displayProperty=nameWithType></li></ul>|
