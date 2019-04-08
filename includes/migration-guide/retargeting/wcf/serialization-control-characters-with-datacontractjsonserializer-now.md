---
ms.openlocfilehash: 2f5511b7694f91893b731805119b85d1a5669a33
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760216"
---
### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>La sérialisation des caractères de contrôle avec DataContractJsonSerializer est maintenant compatible avec ECMAScript V6 et V8

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6.2 et antérieur, <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> ne sérialisait pas certains caractères de contrôle spéciaux, comme \b, \f et \t, d’une manière compatible avec les normes ECMAScript V6 et V8. À compter de .NET Framework 4.7, la sérialisation de ces caractères de contrôle est compatible avec ECMAScript V6 et V8.|
|Suggestion|Pour les applications qui ciblent .NET. Framework 4.7, cette fonctionnalité est activée par défaut. Si ce comportement n’est pas souhaitable, vous pouvez désactiver cette fonctionnalité en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config ou au fichier web.config :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

