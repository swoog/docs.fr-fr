---
ms.openlocfilehash: 948c83f49b703194ccfe932e53751e0bb2dde37c
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760805"
---
### <a name="contextmenustripsourcecontrol-property-contains-a-valid-control-in-the-case-of-nested-toolstripmenuitems"></a>La propriété ContextMenuStrip.SourceControl contient un contrôle valide dans le cas des ToolStripMenuItems imbriqués

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7.1 et versions antérieures, la propriété <xref:System.Windows.Forms.ContextMenuStrip.SourceControl?displayProperty=nameWithType> retourne la valeur null quand l’utilisateur ouvre le menu à partir de contrôles <xref:System.Windows.Forms.ToolStripMenuItem> imbriqués. Dans .NET Framework 4.7.2 et versions ultérieures, la propriété <xref:System.Windows.Forms.ContextMenuStrip.SourceControl> est toujours définie sur le contrôle de code source réel.|
|Suggestion|<strong>Comment accepter ou refuser ces changements</strong>Une application doit s’exécuter sur .NET Framework 4.7.2 ou ultérieur pour tirer parti de ces changements. Pour que l’application bénéficie de ces changements, procédez de l’une des manières suivantes :<ul><li>Faites-lui cibler .NET Framework 4.7.2. Ce changement est activé par défaut sur les applications Windows Forms qui ciblent .NET Framework 4.7.2 ou ultérieur.</li><li>Faites-lui cibler .NET Framework version 4.7.1 ou antérieure et refusez les comportements d’accessibilité hérités en ajoutant le [commutateur AppContext](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) suivant à la section <code>&lt;runtime&gt;</code> du fichier app.config et en lui affectant la valeur <code>false</code>, comme dans l’exemple suivant.</li></ul><pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Forms.UseLegacyContextMenuStripSourceControlValue=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Si votre application cible .NET Framework 4.7.2 ou une version ultérieure et que vous souhaitez conserver le comportement hérité, choisissez d’utiliser la valeur de contrôle de code source héritée en affectant explicitement à ce commutateur AppContext la valeur <code>true</code>.|
|Portée|Microsoft Edge|
|Version|4.7.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Forms.ContextMenuStrip.SourceControl?displayProperty=nameWithType></li></ul>|

