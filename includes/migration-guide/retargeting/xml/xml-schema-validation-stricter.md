---
ms.openlocfilehash: ef0381dc2ce4373b2a62e8ebefa44152059ca332
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234695"
---
### <a name="xml-schema-validation-is-stricter"></a>La validation du schéma XML est plus stricte

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, la validation du schéma XML est plus stricte. Si vous utilisez xsd:anyURI pour valider un URI tel qu'un protocole mailto, la validation échoue si l'URI contient des espaces. Dans les versions antérieures du .NET Framework, la validation réussissait. Le changement affecte uniquement les applications qui ciblent .NET Framework 4.5.|
|Suggestion|Si une validation moins précise de .NET Framework 4.0 est nécessaire, l’application de validation peut cibler la version 4.0 du .NET Framework. Toutefois, si .NET Framework 4.5 est reciblé, effectuez une revue du code pour vérifier que les URI non valides (avec des espaces) ne sont pas attendus comme valeurs d’attribut avec le type de données anyURI.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
