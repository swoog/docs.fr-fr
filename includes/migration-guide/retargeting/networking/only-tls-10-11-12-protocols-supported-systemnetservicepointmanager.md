---
ms.openlocfilehash: 29c5055a84e2dcc94bc4cdeab95722e4358aad89
ms.sourcegitcommit: 0aca6c5d166d7961a1e354c248495645b97a1dc5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58760987"
---
### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>Seuls les protocoles TLS 1.0, 1.1 et 1.2 sont pris en charge dans System.Net.ServicePointManager et System.Net.Security.SslStream

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6, les classes <xref:System.Net.ServicePointManager> et <xref:System.Net.Security.SslStream> ne peuvent utiliser que l’un des trois protocoles suivants : Tls1.0, Tls1.1 ou Tls1.2. Le protocole SSL 3.0 et le chiffrement RC4 ne sont pas pris en charge.|
|Suggestion|L’atténuation recommandée consiste à mettre à niveau l’application côté serveur vers TLS 1.0, TLS 1.1 ou TLS 1.2. Si ce n'est pas possible, ou si les applications clientes sont interrompues, la classe <xref:System.AppContext?displayProperty=name> peut être utilisée pour désactiver cette fonctionnalité de deux manières :<ol><li>En définissant des commutateurs de compatibilité par programmation sur <xref:System.AppContext?displayProperty=name>, comme expliqué [ici](https://devblogs.microsoft.com/dotnet/net-announcements-at-build-2015/#dotnet46)</li><li>En ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> du fichier app.config : <code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code></li></ol>|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

