---
ms.openlocfilehash: 6cc1c65a95238e758f99090794f5e50b830d9667
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803829"
---
### <a name="systemactivities-is-now-aptca"></a>System.Activities est maintenant APTCA

|   |   |
|---|---|
|Détails|L'assembly est marqué avec l'attribut <xref:System.Security.AllowPartiallyTrustedCallersAttribute?displayProperty=name>.|
|Suggestion|Les classes dérivées ne peuvent pas être marquées avec l'objet <xref:System.Security.SecurityCriticalAttribute?displayProperty=name>. Auparavant, les types dérivés devaient être marqués avec l'objet <xref:System.Security.SecurityCriticalAttribute?displayProperty=name>. Toutefois, cette modification ne doit pas avoir d'impact réel.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
