---
ms.openlocfilehash: d4859629fe3922b71cc90664e1e3304cdb312bae
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235296"
---
### <a name="listsort-algorithm-changed"></a>Algorithme List.Sort modifié

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, l’algorithme de tri de <xref:System.Collections.Generic.List%601?displayProperty=name> a changé (pour correspondre à un tri approfondi au lieu d’un tri rapide). <xref:System.Collections.Generic.List%601?displayProperty=name>Le tri n’a jamais été stable, mais cette modification peut aboutir à des tris instables dans différents scénarios. Cela signifie simplement que des éléments équivalents peuvent être triés dans des ordres différents lors des appels suivants de l’API.|
|Suggestion|Comme l’ancien algorithme de tri était également instable (de manière légèrement différente, toutefois), aucun code ne doit dépendre du tri dans un ordre particulier des éléments équivalents. Si des instances de code présentent cette dépendance et réussissent avec l’ancien comportement, ce code doit être mis à jour pour utiliser un comparateur qui va trier de façon déterministe les éléments dans l’ordre souhaité.|
|Portée|Transparent|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|
