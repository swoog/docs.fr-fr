---
ms.openlocfilehash: 734041f5921571cd11225a359e794526cbd8d0e1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234631"
---
### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>La méthode System.Uri.IsWellFormedUriString retourne la valeur false pour les URI relatifs comprenant un caractère deux-points dans le premier segment

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> traite les URI relatifs comprenant un <code>:</code> dans leur premier segment comme n’étant pas bien formés. Il s’agit là d’un changement par rapport au comportement de <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> dans .NET Framework 4.0 qui a été apporté pour qu’il soit conforme à la norme RFC 3986.|
|Suggestion|Ce changement (comme de nombreux autres changements relatifs aux URI) affecte uniquement les applications qui ciblent .NET Framework 4.5 (ou les versions ultérieures). Pour continuer à utiliser l’ancien comportement, ciblez l’application sur .NET Framework 4.0. Si l’ancien comportement est souhaitable, vous pouvez également analyser les URI avant d’appeler <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> pour rechercher les caractères <code>:</code> que vous voulez supprimer à des fins de validation.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|
