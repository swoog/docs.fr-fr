---
ms.openlocfilehash: 2ec5224b1ab16c05f6f942f6084f1ab105b71b0f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774021"
---
### <a name="ensure-systemuri-uses-a-consistent-reserved-character-set"></a>Vérifier que System.Uri utilise un jeu de caractères réservés cohérent

|   |   |
|---|---|
|Détails|Dans <xref:System.Uri?displayProperty=fullName>, certains caractères encodés en pourcentage qui étaient parfois décodés demeurent désormais systématiquement encodés. Cela se produit sur les propriétés et méthodes qui accèdent aux composants de chemin, de requête, de fragment ou d’informations utilisateur de l’URI. Le comportement change uniquement quand les deux conditions suivantes sont vraies :<ul><li>L’URI contient la forme encodée d’un des caractères réservés suivants : <code>:</code>, <code>'</code>, <code>(</code>, <code>)</code>, <code>!</code> ou <code>*</code>.</li><li>L’URI contient un caractère non réservé encodé ou Unicode. Si les deux conditions ci-dessus sont remplies, les caractères réservés encodés demeurent encodés. Dans les versions précédentes du .NET Framework, ils sont décodés.</li></ul>|
|Suggestion|Pour les applications qui ciblent les versions du .NET Framework à partir de la version 4.7.2, le nouveau comportement de décodage est activé par défaut. Si ce changement n’est pas souhaitable, vous pouvez le désactiver en ajoutant le commutateur [AppContextSwitchOverrides](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier de configuration d’application :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Pour les applications qui ciblent des versions antérieures du .NET Framework, mais qui s’exécutent sur .NET Framework versions 4.7.2 et ultérieures, le nouveau comportement de décodage est désactivé par défaut. Vous pouvez l’activer en ajoutant le commutateur [AppContextSwitchOverrides](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier de configuration d’application :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Uri.DontEnableStrictRFC3986ReservedCharacterSets=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Uri?displayProperty=nameWithType></li></ul>|
