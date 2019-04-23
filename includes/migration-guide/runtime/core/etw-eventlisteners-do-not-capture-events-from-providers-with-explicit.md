---
ms.openlocfilehash: 1ef31202d7c072ca27c21fc22db102aafa6b8de7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803846"
---
### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>Les EventListeners ETW ne capturent pas les événements provenant de fournisseurs avec des mots clés explicites (comme le fournisseur TPL)

|   |   |
|---|---|
|Détails|Les EventListeners ETW avec un masque de mot clé vide ne capturent pas correctement les événements provenant de fournisseurs ayant des mots clés explicites. Dans le .NET Framework 4.5, le fournisseur TPL fournissait des mots clés explicites et provoquait ce problème. Dans le .NET Framework 4.6, les EventListeners ont été mis à jour pour ne plus causer ce problème.|
|Suggestion|Pour contourner ce problème, remplacez les appels à <xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)> par des appels à la surcharge EnableEvents qui spécifie explicitement le masque &quot;tous les mots clés&quot; à utiliser : <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>. Étant donné que ce problème a été résolu dans .NET Framework 4.6, vous pouvez également effectuer la mise à niveau vers cette version du .NET Framework.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|
