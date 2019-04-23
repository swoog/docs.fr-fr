---
ms.openlocfilehash: a93fbbd787aa50f080337a6170cf8f56d0d24e31
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236695"
---
### <a name="concurrentqueuettrypeek-can-return-an-erroneous-null-via-its-out-parameter"></a>ConcurrentQueue\<T>.TryPeek risque de retourner une valeur Null erronée dans son paramètre de sortie

|   |   |
|---|---|
|Détails|Dans certains scénarios multithreads, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> peut retourner la valeur true, mais renseigner le paramètre de sortie avec la valeur Null (au lieu de la valeur correcte).|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.5.1. Pour résoudre votre problème, effectuez une mise niveau vers le .NET Framework 4.5.1.|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=nameWithType></li></ul>|
