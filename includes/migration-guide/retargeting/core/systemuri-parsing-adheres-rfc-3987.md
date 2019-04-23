---
ms.openlocfilehash: 6c2c6422ca4d426fcc2ff5827a2387abb5578e3d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234741"
---
### <a name="systemuri-parsing-adheres-to-rfc-3987"></a>L’analyse des objets System.Uri respecte la norme RFC 3987

|   |   |
|---|---|
|Détails|L’analyse URI a changé à différents niveaux dans .NET Framework 4.5. Notez, cependant, que ces changements affectent uniquement le code qui cible .NET Framework 4.5. Si un fichier binaire cible .NET Framework 4.0, l’ancien comportement est appliqué. Les changements appliqués à l’analyse URI dans .NET Framework 4.5 sont les suivants :<ul><li>L’analyse des URI effectue la normalisation et la vérification des caractères selon les dernières règles IRI de la norme RFC 3987.</li><li>Le formulaire C de normalisation Unicode n’est appliqué que sur la partie hôte de l’URI.</li><li>Les URI mailto: non valides génèrent désormais une exception.</li><li>Les espaces à la fin d’un segment de chemin sont désormais conservés.</li><li><code>file://</code> Les URI n’échappent pas le caractère <code>?</code>.</li><li>Les caractères de contrôle Unicode allant de <code>U+0080</code> à <code>U+009F</code> ne sont pas pris en charge.</li><li>Les virgules <code>,</code> ou <code>%2c</code> ne sont pas automatiquement sans séquence d’échappement.</li></ul>|
|Suggestion|Si l’ancienne sémantique d’analyse URI de .NET Framework 4.0 est nécessaire (et c’est souvent le cas), elle peut être utilisée en ciblant .NET Framework 4.0. Pour cela, utilisez un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> sur l’assembly ou modifiez les propriétés du projet dans l’interface utilisateur du système de projet de Visual Studio.|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Uri.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.UriKind)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.Uri,System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li></ul>|
