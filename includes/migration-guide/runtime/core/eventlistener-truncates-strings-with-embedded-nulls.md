---
ms.openlocfilehash: 9084c135769f595491d645e49d24cf507f5f6070
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235311"
---
### <a name="eventlistener-truncates-strings-with-embedded-nulls"></a>EventListener tronque les chaînes comportant des valeurs Null incorporées

|   |   |
|---|---|
|Détails|<xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> tronque les chaînes comportant des valeurs Null incorporées. Les caractères Null ne sont pas pris en charge par la classe <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name>. La modification affecte uniquement les applications qui utilisent <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> pour lire des données <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> dans le processus et qui utilisent des caractères Null comme délimiteurs.|
|Suggestion|<xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> Les données doivent si possible être mises à jour de façon à ne pas utiliser de caractères Null incorporés.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Diagnostics.Tracing.EventListener.%23ctor?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords,System.Collections.Generic.IDictionary{System.String,System.String})?displayProperty=nameWithType></li></ul>|
