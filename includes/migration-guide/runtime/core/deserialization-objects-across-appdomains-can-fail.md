---
ms.openlocfilehash: 891c29b731214fb0028e960256b79cfc267d86b9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803847"
---
### <a name="deserialization-of-objects-across-appdomains-can-fail"></a>La désérialisation d’objets entre les domaines d’application peut échouer

|   |   |
|---|---|
|Détails|Dans certains cas, quand une application utilise deux domaines d'application ou plus avec des bases d'application différentes, une tentative de désérialisation des objets dans le contexte d'appel logique entre les domaines d'application lève une exception.|
|Suggestion|Voir [Prévention : désérialisation d’objets sur plusieurs domaines d’application](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md).|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Runtime|
