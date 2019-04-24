---
ms.openlocfilehash: 4e81087431091dfa4d5432d5ea5e2b665be2b130
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774322"
---
### <a name="listtforeach-can-throw-exception-when-modifying-list-item"></a>List\<T>.ForEach risque de lever une exception en cas de modification d’un élément de liste

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, un énumérateur <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> lève une exception <xref:System.InvalidOperationException?displayProperty=name> si un élément de la collection appelante est modifié. Avant, il ne levait pas d’exception, mais pouvait entraîner des conditions de concurrence.|
|Suggestion|Dans l’idéal, le code doit être corrigé de manière à ne pas modifier les listes pendant l’énumération de leurs éléments, car cela n’est jamais une opération sûre. Cependant, pour restaurer le comportement précédent, une application peut cibler .NET Framework 4.0.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|
