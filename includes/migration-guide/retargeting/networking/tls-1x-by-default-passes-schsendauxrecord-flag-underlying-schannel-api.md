---
ms.openlocfilehash: 0ea8c4843bb0dfb4e4208f2bfad4c416bfae7a1e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803868"
---
### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a>TLS 1.x passe par défaut l’indicateur SCH_SEND_AUX_RECORD à l’API SCHANNEL sous-jacente

|   |   |
|---|---|
|Détails|Quand vous utilisez TLS 1.x, le .NET Framework s’appuie sur l’API SCHANNEL Windows sous-jacente. À compter de .NET Framework 4.6, l’indicateur [SCH_SEND_AUX_RECORD](https://docs.microsoft.com/windows/desktop/api/schannel/ns-schannel-_schannel_cred) est passé par défaut à SCHANNEL. Cela amène SCHANNEL à fractionner les données à chiffrer en deux enregistrements distincts, le premier sous forme d’un octet unique et le second de <em>n</em>-1 octets. Dans de rares cas, la communication s’en trouve interrompue entre les clients et les serveurs existants qui supposent que les données résident dans un seul enregistrement.|
|Suggestion|Si ce changement interrompt la communication avec un serveur existant, vous pouvez désactiver l’envoi de l’indicateur [SCH_SEND_AUX_RECORD](https://docs.microsoft.com/windows/desktop/api/schannel/ns-schannel-_schannel_cred) et restaurer le comportement précédent, qui consiste à ne pas fractionner les données dans des enregistrements distincts, en ajoutant le commutateur suivant à l’élément [\<AppContextSwitchOverrides>](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) de la section [\<runtime>](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) du fichier de configuration de votre application :<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Ce paramètre est fourni dans le seul but d’assurer la compatibilité descendante. Son utilisation à d’autres fins n’est pas recommandée.</blockquote> |
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|
