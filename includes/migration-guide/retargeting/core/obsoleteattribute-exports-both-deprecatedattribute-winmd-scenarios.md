---
ms.openlocfilehash: e8c48c4b1031813ce62f576e5bf1f94c082dfe4b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774347"
---
### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute est exporté à la fois comme ObsoleteAttribute et comme DeprecatedAttribute dans les scénarios WinMD

|   |   |
|---|---|
|Détails|Quand vous créez une bibliothèque de métadonnées Windows (fichier .winmd), l’attribut <xref:System.ObsoleteAttribute?displayProperty=name> est exporté à la fois comme <xref:System.ObsoleteAttribute?displayProperty=name> et comme [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Suggestion|La recompilation de code source existant qui utilise l’attribut <xref:System.ObsoleteAttribute?displayProperty=name> peut générer des avertissements quand ce code est consommé à partir de C++/CX ou de JavaScript. Nous déconseillons d’appliquer à la fois <xref:System.ObsoleteAttribute?displayProperty=name> et [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) au code d’assemblys managés, car cela peut produire des avertissements de génération.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Reciblage|
