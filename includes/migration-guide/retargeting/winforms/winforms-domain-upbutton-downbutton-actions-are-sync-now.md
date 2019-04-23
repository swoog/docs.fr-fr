---
ms.openlocfilehash: e73fe48467ede501bae0ddd9362d9d55b3ca998b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774055"
---
### <a name="winforms-domain-upbutton-and-downbutton-actions-are-in-sync-now"></a>Les actions upbutton et downbutton Domain de WinForm sont désormais synchronisées

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7.1 et versions antérieures, l’action <xref:System.Windows.Forms.DomainUpDown.UpButton?displayProperty=nameWithType> du contrôle <xref:System.Windows.Forms.DomainUpDown> est ignorée quand le texte du contrôle est présent, obligeant le développeur à utiliser l’action <xref:System.Windows.Forms.DomainUpDown.DownButton?displayProperty=nameWithType> sur le contrôle avant d’utiliser l’action <xref:System.Windows.Forms.DomainUpDown.UpButton?displayProperty=nameWithType>. À compter de .NET Framework 4.7.2, les actions <xref:System.Windows.Forms.DomainUpDown.UpButton?displayProperty=nameWithType> et <xref:System.Windows.Forms.DomainUpDown.DownButton?displayProperty=nameWithType> fonctionnent indépendamment dans ce scénario et restent synchronisées.|
|Suggestion|Une application doit s’exécuter sur .NET Framework 4.7.2 ou ultérieur pour tirer parti de ces changements. Pour que l’application bénéficie de ces changements, procédez de l’une des manières suivantes :<ul><li>Recompilez-la pour qu’elle cible .NET Framework 4.7.2. Ce changement est activé par défaut sur les applications Windows Forms qui ciblent .NET Framework 4.7.2 ou ultérieur.</li><li>Refusez le comportement de défilement hérité en ajoutant le [commutateur AppContext](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier de configuration de l’application et en lui affectant la valeur <code>false</code>, comme dans l’exemple suivant.</li></ul><pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Forms.DomainUpDown.UseLegacyScrolling=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Forms.DomainUpDown.UpButton?displayProperty=nameWithType></li><li><xref:System.Windows.Forms.DomainUpDown.DownButton?displayProperty=nameWithType></li></ul>|
