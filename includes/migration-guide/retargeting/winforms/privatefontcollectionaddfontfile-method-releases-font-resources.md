---
ms.openlocfilehash: f5d93d76ab3409d4d4c1870cfef94cac59f9475c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59233953"
---
### <a name="privatefontcollectionaddfontfile-method-releases-font-resources"></a>La méthode PrivateFontCollection.AddFontFile libère les ressources de police

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7.1 et versions antérieures, une fois le <xref:System.Drawing.Text.PrivateFontCollection> supprimé pour les objets <xref:System.Drawing.Font>, la classe <xref:System.Drawing.Text.PrivateFontCollection?displayProperty=nameWithType> ne libère pas les ressources de police GDI+ qui sont ajoutées à cette collection à l’aide de la méthode <xref:System.Drawing.Text.PrivateFontCollection.AddFontFile(System.String)>. Dans .NET Framework 4.7.2 et versions ultérieures, <xref:System.Drawing.Text.FontCollection.Dispose%2A> libère les polices GDI+ qui ont été ajoutées à la collection en tant que fichiers.|
|Suggestion|<strong>Comment accepter ou refuser ces changements</strong>Une application doit s’exécuter sur .NET Framework 4.7.2 ou ultérieur pour tirer parti de ces changements. Pour que l’application bénéficie de ces changements, procédez de l’une des manières suivantes :<ul><li>Recompilez-la pour qu’elle cible .NET Framework 4.7.2. Ce changement est activé par défaut sur les applications Windows Forms qui ciblent .NET Framework 4.7.2 ou ultérieur.</li><li>Faites-lui cibler .NET Framework version 4.7.1 ou antérieure et refusez les comportements d’accessibilité hérités en ajoutant le [commutateur AppContext](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier app.config et en lui affectant la valeur <code>false</code>, comme dans l’exemple suivant.</li></ul><pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Drawing.Text.DoNotRemoveGdiFontsResourcesFromFontCollection=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Si votre application cible .NET Framework 4.7.2 ou une version ultérieure et que vous souhaitez conserver le comportement hérité, choisissez de ne pas libérer les ressources de police en affectant explicitement à ce commutateur AppContext la valeur <code>true</code>.|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Drawing.Text.PrivateFontCollection.AddFontFile(System.String)?displayProperty=nameWithType></li><li><xref:System.Drawing.Text.FontCollection.Dispose?displayProperty=nameWithType></li></ul>|
