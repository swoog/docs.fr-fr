---
ms.openlocfilehash: a51738fa75ba2dd4574549fce2570df8231c4cae
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59234922"
---
### <a name="path-colon-checks-are-stricter"></a>Les vérifications des signes deux-points dans les chemins sont plus strictes

|   |   |
|---|---|
|Détails|Dans.NET Framework 4.6.2, plusieurs changements ont été apportés pour prendre en charge les chemins qui n’étaient précédemment pas pris en charge (à la fois du fait de la longueur et du format). Les vérifications de syntaxe correcte de séparateur de lecteur (signe deux-points) ont été rendues plus exactes, ce qui a eu pour effet secondaire de bloquer certains chemins d’URI dans quelques API de chemin spécifiques qui étaient habituellement tolérées.|
|Suggestion|Si vous passez un URI à des API affectées, modifiez d’abord la chaîne pour en faire un chemin valide.<ul><li>Supprimez manuellement le schéma des URL (par exemple, supprimez <code>file://</code> des URL)</li><li>Passez l’URI de la classe <xref:System.Uri> et utilisez <xref:System.Uri.LocalPath></li></ul>Vous pouvez également refuser la nouvelle normalisation de chemin en définissant le commutateur AppContext <code>Switch.System.IO.UseLegacyPathHandling</code> sur true.|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|
