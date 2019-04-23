---
ms.openlocfilehash: 0a3dc43ebdc58d54675f2264a8ee56d9f4358cd8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803887"
---
### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>La sécurité des messages WCF peut désormais utiliser TLS 1.1 et TLS 1.2

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7, les clients peuvent configurer TLS 1.1 ou TLS 1.2 dans la sécurité des messages WCF en plus de SSL 3.0 et TLS 1.0 à l’aide des paramètres de configuration d’application.|
|Suggestion|Dans .NET Framework 4.7, la prise en charge de TLS 1.1 et de TLS 1.2 dans la sécurité des messages WCF est désactivée par défaut. Vous pouvez l’activer en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config ou du fichier web.config :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Reciblage|
