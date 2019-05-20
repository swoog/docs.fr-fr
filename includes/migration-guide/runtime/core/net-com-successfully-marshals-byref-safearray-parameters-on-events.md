---
ms.openlocfilehash: 9c72bc686e014a0bffdf272e3813358d1b29cc66
ms.sourcegitcommit: ca2ca60e6f5ea327f164be7ce26d9599e0f85fe4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65199008"
---
### <a name="net-com-successfully-marshals-byref-safearray-parameters-on-events"></a>.NET COM marshale avec succès les paramètres ByRef SafeArray sur les événements

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7.2 et versions antérieures, le marshaling en code natif d’un paramètre ByRef [SafeArray](https://docs.microsoft.com/en-us/windows/desktop/api/oaidl/ns-oaidl-safearray) sur un événement COM était voué à l’échec.  Avec cette modification, le [SafeArray](https://docs.microsoft.com/en-us/windows/desktop/api/oaidl/ns-oaidl-safearray) est maintenant correctement marshalé.<ul><li>[ x ] Quirked</li></ul>|
|Suggestion|Si un marshaling correct des paramètres ByRef SafeArray sur des événements COM interrompt l’exécution, vous pouvez désactiver ce code en ajoutant le commutateur de configuration suivant à la configuration de votre application :<pre><code class="lang-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.Runtime.InteropServices.DoNotMarshalOutByrefSafeArrayOnInvoke&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.8|
|Type|Runtime|
