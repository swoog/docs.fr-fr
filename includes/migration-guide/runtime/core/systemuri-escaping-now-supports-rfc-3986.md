---
ms.openlocfilehash: 1654d58651bf14b0e7c21de2afa827634b7db858
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59235329"
---
### <a name="systemuri-escaping-now-supports-rfc-3986"></a>L’échappement de System.Uri prend maintenant en charge la norme RFC 3986

|   |   |
|---|---|
|Détails|L’échappement d’URI a été modifié dans NET Framework 4.5 de manière à prendre en charge la norme [RFC 3986](https://tools.ietf.org/html/rfc3986). Ces modifications sont les suivantes :<ul><li><xref:System.Uri.EscapeDataString(System.String)?displayProperty=name> représente une séquence d'échappement pour les caractères réservés basés sur la norme RFC 3986.</li><li><xref:System.Uri.EscapeUriString(System.String)?displayProperty=name> ne représente pas une séquence d'échappement pour les caractères réservés.</li><li><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> ne lève pas d'exception s'il rencontre une séquence d'échappement non valide.</li><li>Les caractères d'échappement non réservés sont sans séquence d'échappement.</li></ul>|
|Suggestion|<ul><li>Mettez à jour les applications pour qu’elles ne comptent pas sur <xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> pour lever une exception en cas de séquence d’échappement non valide. Ces séquences sont à présent directement détectées.</li><li>Il est également possible que les URI avec et sans séquence d’échappement, ainsi que les chaînes de données, varient entre les versions 4.0 et 4.5 du .NET Framework. De plus, ils ne doivent pas être comparés directement entre différentes versions de .NET. Ils doivent être analysés et normalisés dans une seule version du .NET avant de faire l’objet d’une comparaison.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Uri.EscapeDataString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.EscapeUriString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=nameWithType></li></ul>|
