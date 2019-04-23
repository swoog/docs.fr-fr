---
ms.openlocfilehash: 891c29b731214fb0028e960256b79cfc267d86b9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235248"
---
### <a name="deserialization-of-objects-across-appdomains-can-fail"></a>La désérialisation d’objets entre les domaines d’application peut échouer

|   |   |
|---|---|
|Détails|Dans certains cas, quand une application utilise deux domaines d'application ou plus avec des bases d'application différentes, une tentative de désérialisation des objets dans le contexte d'appel logique entre les domaines d'application lève une exception.|
|Suggestion|Voir [Prévention : désérialisation d’objets sur plusieurs domaines d’application](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md).|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Runtime|
