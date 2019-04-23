---
ms.openlocfilehash: 3e9a1009167d8a765bc401d64a574bd123736ccd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774056"
---
### <a name="allow-unicode-bidirectional-control-characters-in-uris"></a>Autoriser les caractères de contrôle bidirectionnels Unicode dans les URI

|   |   |
|---|---|
|Détails|Unicode spécifie plusieurs caractères de contrôle spéciaux utilisés pour définir l’orientation du texte. Dans les versions précédentes du .NET Framework, ces caractères n’étaient pas correctement supprimés de tous les URI, même s’ils étaient encodés en pourcentage. Pour mieux suivre la spécification [RFC 3987](https://tools.ietf.org/html/rfc3987), nous autorisons désormais ces caractères dans les URI. Si une URI en contient qui ne sont pas encodés, ils sont encodés en pourcentage. Si elle en contient qui sont encodés en pourcentage, ils sont laissés tels quels.|
|Suggestion|Pour les applications qui ciblent des versions du .NET Framework à partir de la version 4.7.2, la prise en charge des caractères bidirectionnels Unicode est activée par défaut. Si ce changement n’est pas souhaitable, vous pouvez le désactiver en ajoutant le commutateur [AppContextSwitchOverrides](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier de configuration d’application :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Uri.DontKeepUnicodeBidiFormattingCharacters=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Pour les applications qui ciblent des versions antérieures du .NET Framework, mais qui s’exécutent sur .NET Framework versions 4.7.2 et ultérieures, la prise en charge des caractères bidirectionnels Unicode est désactivée par défaut. Vous pouvez l’activer en ajoutant le commutateur [AppContextSwitchOverrides](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier de configuration d’application :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Uri.DontKeepUnicodeBidiFormattingCharacters=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Uri?displayProperty=nameWithType></li></ul>|
