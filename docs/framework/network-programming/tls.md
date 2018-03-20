---
title: Transport Layer Security (TLS) meilleures pratiques avec le .NET Framework
description: "Décrit les meilleures pratiques à l’aide de la sécurité TLS (Transport Layer) avec le .NET Framework"
ms.date: 03/15/2018
ms.prod: .net-framework
ms.topic: article
helpviewer_keywords:
- sending data, Internet security
- protocols, Internet security
- Network security
- network resources, Internet security
- receiving data, Internet security
- authentication [.NET Framework], Internet security
- Internet, security
- security [.NET Framework], Internet
- permissions [.NET Framework], Internet
author: blowdart
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 64829eee5b21a44acb18cbec9b901d77d49cab90
ms.sourcegitcommit: 32172ca05d5dcce7ef3d327b9c8639c736e0fe2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2018
---
# <a name="transport-layer-security-tls-best-practices-with-the-net-framework"></a>Transport Layer Security (TLS) meilleures pratiques avec le .NET Framework

Le protocole de sécurité TLS (Transport Layer) est une norme conçue pour vous aider à protéger la confidentialité des informations communiquées via Internet. [TLS 1.2](https://tools.ietf.org/html/rfc5246) est lancé standard les plus récents et fournit des améliorations de sécurité par rapport aux versions précédentes. TLS 1.2 sera finalement remplacée par [TLS 1.3](https://tools.ietf.org/html/draft-ietf-tls-tls13-22). Cet article présente les recommandations pour sécuriser les applications .NET Framework qui utilisent le protocole TLS.

Pour garantir que les applications .NET Framework restent sécurisées, la version TLS doit **pas** être codé en dur. Les applications .NET framework doivent utiliser la version TLS que prend en charge par le système d’exploitation (OS).

Ce document est destinée aux développeurs qui sont :

- Directement à l’aide de la <xref:System.Net> API (par exemple, <xref:System.Net.Http.HttpClient?displayProperty=nameWithType> et <xref:System.Net.Security.SslStream?displayProperty=nameWithType>).
- Directement à l’aide des clients WCF et les services à l’aide de la <xref:System.ServiceModel?displayProperty=nameWithType> espace de noms.
- À l’aide de [Azure Cloud Services](https://azure.microsoft.com/services/cloud-services/) rôles Web et de travail pour héberger et exécuter votre application. Consultez le [Azure Cloud Services](#azure-cloud-services) section.

Nous recommandons que vous :

- Cibler .NET Framework 4.7 ou versions ultérieures sur vos applications. Cibler .NET Framework 4.7.1 ou versions ultérieures sur vos applications WCF.
- Ne spécifiez pas la version TLS. Configurez votre code afin de laisser le système d’exploitation à décider de la version TLS.
- Effectuer un audit complet de code pour vérifier que vous n’indiquez pas une version SSL ou TLS.

Lorsque votre application vous permet du système d’exploitation choisir la version TLS :

- Il bénéficie automatiquement de nouveaux protocoles ajouté à l’avenir, tels que TLS 1.3.
- Le système d’exploitation bloque les protocoles qui sont découverts ne pas à être sécurisée.

La section [votre code de vérification et d’apporter des modifications de code](#audit-your-code-and-make-code-changes) couvre l’audit et de mise à jour de votre code.

Cet article explique comment activer la sécurité maximale disponible pour la version du .NET Framework que votre application cible et s’exécute sur. Lorsqu’une application définit explicitement une version et le protocole de sécurité, il exclut toute autre solution et exclut le .NET Framework et le système d’exploitation par défaut. Si vous souhaitez que votre application soit en mesure de négocier une connexion TLS 1.2, si vous affectez explicitement à une version antérieure de TLS empêche une connexion TLS 1.2.

Si vous ne pouvez pas éviter de coder en dur une version de protocole, nous vous recommandons vivement de spécifier TLS 1.2. Pour obtenir des conseils sur l’identification et la suppression des dépendances de TLS 1.0, téléchargez le [suffira TLS 1.0](https://www.microsoft.com/download/details.aspx?id=55266) livre blanc.

WCF prend en charge TLS 1.0, 1.1 et 1.2 par défaut dans .NET Framework 4.7. À compter de .NET Framework 4.7.1, WCF par défaut, le système d’exploitation configuré la version. Si une application est explicitement configurée avec `SslProtocols.None`, WCF utilise le paramètre par défaut de système d’exploitation lors de l’utilisation du transport NetTcp.

Vous pouvez poser des questions concernant ce document dans le problème GitHub [sécurité TLS (Transport Layer) meilleures pratiques avec le .NET Framework](https://github.com/dotnet/docs/issues/4675).

## <a name="audit-your-code-and-make-code-changes"></a>Votre code de vérification et d’apporter des modifications de code

Pour les applications ASP.NET, inspecter la `<system.web><httpRuntime targetFramework>` élément de _web.config_ pour vérifier à l’aide de la version du .NET Framework.

Pour les Windows Forms et d’autres applications, consultez [Comment : cibler une Version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).

Utilisez les sections suivantes pour vérifier que vous n’utilisez pas une version spécifique de SSL ou TLS.

## <a name="if-your-app-targets-net-framework-47-or-later-versions"></a>Si votre application cible .NET Framework 4.7 ou versions ultérieures

Les sections suivantes montrent comment vérifier si vous n’utilisez pas une version spécifique de SSL ou TLS.

### <a name="for-http-networking"></a>Mise en réseau HTTP

<xref:System.Net.ServicePointManager>, à l’aide de .NET Framework 4.7 et versions ultérieures, la valeur par défaut est le système d’exploitation en choisissant le meilleur protocole de sécurité et la version. Pour obtenir la meilleure du système d’exploitation par défaut, si possible, ne définissez pas une valeur pour le <xref:System.Net.ServicePointManager.SecurityProtocol> propriété. Sinon, attribuez-lui la valeur <xref:System.Net.SecurityProtocolType.SystemDefault>.

Le reste de cet article s’applique pas lorsque vous ciblez .NET Framework 4.7 ou versions ultérieures de mise en réseau HTTP.

### <a name="for-tcp-sockets-networking"></a>Pour les sockets TCP mise en réseau

<xref:System.Net.Security.SslStream>, à l’aide de .NET Framework 4.7 et versions ultérieures, la valeur par défaut est le système d’exploitation en choisissant le meilleur protocole de sécurité et la version. Pour obtenir la meilleure du système d’exploitation par défaut, si possible, n’utilisez pas les surcharges de méthode de <xref:System.Net.Security.SslStream> qui accepte une explicite <xref:System.Security.Authentication.SslProtocols> paramètre. Sinon, passez <xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType>. Nous vous recommandons de ne pas utiliser <xref:System.Security.Authentication.SslProtocols.Default>; paramètre `SslProtocols.Default` force l’utilisation de SSL 3.0 /TLS 1.0 et empêcher TLS 1.2.

Ne définissez pas une valeur pour le <xref:System.Net.ServicePointManager.SecurityProtocol> propriété (pour la gestion de réseau HTTP).

N’utilisez pas les surcharges de méthode de <xref:System.Net.Security.SslStream> qui accepte une explicite <xref:System.Security.Authentication.SslProtocols> paramètre (pour les sockets TCP mise en réseau). Lorsque vous reciblez votre application .NET Framework 4.7 ou version ultérieure, vous allez après la recommandation des meilleures pratiques.

Le reste de cette rubrique ne s’applique pas lors de la mise en réseau des sockets ciblant .NET Framework 4.7 ou versions ultérieures pour le protocole TCP.

<a name="wcf-tcp-cert"></a>

### <a name="for-wcf-tcp-transport-using-transport-security-with-certificate-credentials"></a>Pour le TCP de WCF de transport à l’aide de la sécurité de transport avec informations d’identification de certificat

WCF utilise la même pile de mise en réseau que le reste du .NET Framework.

Si vous ciblez 4.7.1, WCF est configuré pour autoriser le système d’exploitation choisir le meilleur protocole de sécurité par défaut, sauf si configuré de manière explicite :

- Dans le fichier de configuration de votre application.
- **Ou**, dans votre application dans le code source.

Par défaut, .NET Framework 4.7 et versions ultérieures est configuré pour utiliser TLS 1.2 et autorise les connexions à l’aide de TLS 1.1 ou TLS 1.0. Configurer WCF pour autoriser le système d’exploitation choisir le meilleur protocole de sécurité en configurant votre liaison à utiliser <xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType>. Cela peut être défini sur <xref:System.ServiceModel.TcpTransportSecurity.SslProtocols>. `SslProtocols.None` est accessible à partir de <xref:System.ServiceModel.NetTcpSecurity.Transport>. `NetTcpSecurity.Transport` est accessible à partir de <xref:System.ServiceModel.NetTcpBinding.Security>.

Si vous utilisez une liaison personnalisée :

- Configurer WCF pour autoriser le système d’exploitation choisir le meilleur protocole de sécurité en définissant <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement.SslProtocols> à utiliser <xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType>.
- **Ou** configurer le protocole utilisé avec le chemin d’accès de configuration `system.serviceModel/bindings/customBinding/binding/sslStreamSecurity:sslProtocols`.

Si vous êtes **pas** à l’aide d’une liaison personnalisée **et** vous définissez votre liaison WCF à l’aide de la configuration, de définir le protocole utilisé avec le chemin d’accès de configuration `system.serviceModel/bindings/netTcpBinding/binding/security/transport:sslProtocols`.

### <a name="for-wcf-message-security-with-certificate-credentials"></a>Pour la sécurité de Message WCF avec les informations d’identification de certificat

.NET framework 4.7 et versions ultérieures, par défaut utilise le protocole spécifié dans le <xref:System.Net.ServicePointManager.SecurityProtocol> propriété. Lorsque le [AppContextSwitch](../configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) `Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols` a la valeur `true`, WCF choisit le meilleur protocole, jusqu'à TLS 1.0.

## <a name="if-your-app-targets-a-net-framework-version-earlier-than-47"></a>Si votre application cible une version du .NET Framework antérieures à 4.7

Auditer votre code pour vérifier que vous ne configurez pas une version spécifique de SSL ou TLS à l’aide des sections suivantes :

### <a name="for-net-framework-46---462-and-not-wfc"></a>Pour .NET Framework 4.6 - 4.6.2 et pas WFC

Définir le `DontEnableSystemDefaultTlsVersions` `AppContext` basculer vers `false`. Consultez [configuration de la sécurité via des commutateurs AppContext](#configuring-security-via-appcontext-switches).

### <a name="for-wcf-using-net-framework-46---462-using-tcp-transport-security-with-certificate-credentials"></a>Pour WCF à l’aide de .NET Framework 4.6 - 4.6.2 à l’aide de la sécurité du transport TCP avec informations d’identification de certificat

Vous devez installer les derniers correctifs de système d’exploitation. Consultez [mises à jour de sécurité](#security-updates).

L’infrastructure WCF choisit automatiquement le protocole le plus élevé disponible jusque TLS 1.2, sauf si vous configurez explicitement une version de protocole. Pour plus d’informations, consultez la section précédente [transport pour le TCP de WCF à l’aide de la sécurité de transport avec informations d’identification de certificat](#wcf-tcp-cert).

### <a name="for-net-framework-35---451-and-not-wcf"></a>Pour .NET Framework 3.5 - 4.5.1 et pas de WCF

Nous vous recommandons de que mettre à niveau de votre application .NET Framework 4.7 ou version ultérieure. Si vous ne pouvez pas mettre à niveau, procédez comme suit. À un moment donné dans le futur, votre application peut échouer jusqu'à ce que vous mettez à niveau vers .NET Framework 4.7 ou versions ultérieures.

Définir le [SchUseStrongCrypto](#schusestrongcrypto) et [SystemDefaultTlsVersions](#systemdefaulttlsversions) les clés de Registre à 1. Consultez [configuration de la sécurité via le Registre Windows](#configuring-security-via-the-windows-registry). La version 3.5 du .NET Framework prend en charge la `SchUseStrongCrypto` indicateur uniquement lorsqu’une valeur explicite de TLS est passée.

Si vous exécutez sur .NET Framework 3.5, vous devez installer un correctif à chaud pour que TLS 1.2 peut être spécifié par votre programme :

| [KB3154518](https://support.microsoft.com/kb/3154518) | Fiabilité cumul HR-1605 - prise en charge des Versions par défaut du système TLS inclus dans le .NET Framework 3.5.1 sur Windows 7 SP1 et Server 2008 R2 SP1 |
| --- | --- |
| [KB3154519](https://support.microsoft.com/kb/3154519) | Cumul de la fiabilité HR-1605 - prise en charge des Versions TLS système par défaut inclus dans le .NET Framework 3.5 sur Windows Server 2012 |
| [KB3154520](https://support.microsoft.com/kb/3154520) | Cumul de la fiabilité 1605 HR - prise en charge des Versions par défaut du système TLS inclus dans le .NET Framework 3.5 sur Windows 8.1 et Windows Server 2012 R2 |
| [KB3156421](https://support.microsoft.com/kb/3156421) | 1605 correctif cumulatif 3154521 pour le .NET Framework 4.5.2 et 4.5.1 sur Windows |

### <a name="for-wcf-using-net-framework-35---452-using-tcp-transport-security-with-certificate-credentials"></a>Pour WCF à l’aide de .NET Framework 3.5 - 4.5.2 à l’aide de la sécurité du transport TCP avec informations d’identification de certificat

Ces versions de l’infrastructure WCF sont codées en dur pour utiliser les valeurs SSL 3.0 et TLS 1.0. Ces valeurs ne peuvent pas être modifiées. Vous devez mettre à jour et recibler NET Framework 4.6 ou version ultérieure pour utiliser TLS 1.1 et 1.2.

## <a name="if-your-app-targets-net-framework-35"></a>Si votre application cible .NET Framework 3.5

Si vous devez définir explicitement un protocole de sécurité au lieu de laisser le .NET framework ou le choix du système d’exploitation le protocole de sécurité, ajoutez `SecurityProtocolTypeExtensions` et `SslProtocolsExtension` énumérations à votre code. `SecurityProtocolTypeExtensions` et `SslProtocolsExtension` inclure des valeurs pour `Tls12`, `Tls11`et le `SystemDefault` valeur. Consultez [prise en charge des Versions TLS système par défaut inclus dans .NET Framework 3.5 sur Windows 8.1 et Windows Server 2012 R2](https://support.microsoft.com/help/3154520/support-for-tls-system-default-versions-included-in-the--net-framework).

<a name="configuring-security-via-appcontext-switches"></a>

## <a name="configuring-security-via-appcontext-switches-for-net-framework-46-or-later-versions"></a>Configuration de la sécurité via AppContext bascule (pour .NET Framework 4.6 ou versions ultérieures)

Le [AppContext](../configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) options décrites dans cette section concernent si votre application cible, ou s’exécute sur le .NET Framework 4.6 ou version ultérieure. Si, par défaut, ou en les définissant explicitement, les commutateurs doivent être `false` si possible. Si vous souhaitez configurer la sécurité via un ou deux commutateurs, ne spécifiez pas une valeur de protocole de sécurité dans votre code ; Par conséquent, cette opération remplace l’ou les commutateurs.

Les commutateurs ont le même effet si vous effectuez la mise en réseau HTTP (<xref:System.Net.ServicePointManager>) ou de la mise en réseau des sockets TCP (<xref:System.Net.Security.SslStream>).

### <a name="switchsystemnetdontenableschusestrongcrypto"></a>Switch.System.Net.DontEnableSchUseStrongCrypto

La valeur `false` pour `Switch.System.Net.DontEnableSchUseStrongCrypto` provoque votre application d’utiliser un chiffrement fort. La valeur `false` pour `DontEnableSchUseStrongCrypto` utilise les protocoles de réseau plus sécurisés (TLS 1.2, TLS 1.1 et TLS 1.0) et bloque les protocoles qui ne sont pas sécurisées. Pour plus d’informations, consultez [indicateur de la SCH_USE_STRONG_CRYPTO](#the-schusestrongcrypto-flag). La valeur `true` désactive le chiffrement fort pour votre application.

Si votre application cible .NET Framework 4.6 ou version ultérieure, ce commutateur par défaut est `false`. Qui est sécurisé par défaut, nous vous recommandons de. Si votre application s’exécute sur .NET Framework 4.6, mais il cible une version antérieure, le commutateur par défaut est `true`. Dans ce cas, vous devez définir explicitement `false`.

`DontEnableSchUseStrongCrypto` doit uniquement avoir la valeur `true` si vous avez besoin pour se connecter à des services hérités qui ne prennent pas en charge le chiffrement fort et ne peut pas être mis à niveau.

### <a name="switchsystemnetdontenablesystemdefaulttlsversions"></a>Switch.System.Net.DontEnableSystemDefaultTlsVersions

La valeur `false` pour `Switch.System.Net.DontEnableSystemDefaultTlsVersions` provoque votre application permettre au système d’exploitation choisir le protocole. Une valeur de `true` provoque votre application d’utiliser des protocoles choisis par le .NET Framework.

Si votre application cible .NET Framework 4.7 ou versions ultérieures, ce commutateur par défaut est `false`. Qui est sécurisé par défaut que nous recommandons. Si votre application s’exécute sur le .NET Framework 4.7 ou versions ultérieures, mais il cible une version antérieure, le commutateur par défaut est `true`. Dans ce cas, vous devez définir explicitement `false`.

### <a name="switchsystemservicemodeldisableusingservicepointmanagersecurityprotocols"></a>Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols

La valeur `false` pour `Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols` votre application d’utiliser la valeur définie dans `ServicePointManager.SecurityProtocols` pour la sécurité de message à l’aide des informations d’identification du certificat. La valeur `true` utilise le protocole le plus élevé disponible, jusque TLS 1.0

Pour les applications ciblant le .NET Framework 4.7 et versions ultérieures, cette valeur par défaut est `false`. Pour les applications qui ciblent .NET Framework 4.6.2 et versions antérieures, cette valeur par défaut est `true`.

### <a name="switchsystemservicemodeldontenablesystemdefaulttlsversions"></a>Switch.System.ServiceModel.DontEnableSystemDefaultTlsVersions

La valeur `false` pour `Switch.System.ServiceModel.DontEnableSystemDefaultTlsVersions` définit la configuration par défaut pour permettre au système d’exploitation choisir le protocole. La valeur `true` définit la valeur par défaut pour le protocole le plus élevé disponible, jusque TLS 1.2.

Pour les applications ciblant le .NET Framework 4.7.1 et versions ultérieures, cette valeur par défaut est `false`. Pour les applications qui ciblent .NET Framework 4.7 et versions antérieur, cette valeur par défaut est `true`.

Pour plus d’informations sur les protocoles TLS, consultez [atténuation : protocoles TLS](../migration-guide/mitigation-tls-protocols.md). Pour plus d’informations sur `AppContext` commutateurs, consultez [ `<AppContextSwitchOverrides> Element` ](../configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md).

## <a name="configuring-security-via-the-windows-registry"></a>Configuration de la sécurité via le Registre Windows

Si une ou les deux `AppContext` commutateurs ne sont pas une option, vous pouvez contrôler les protocoles de sécurité utilisé par votre application avec les clés de Registre de Windows décrits dans cette section. Vous n’êtes peut-être pas en mesure d’utiliser une ou les deux le `AppContext` bascule si votre application cible une version du .NET Framework antérieures à la version 4.6, ou vous ne pouvez pas modifier le fichier de configuration. Si vous souhaitez configurer la sécurité du Registre, ne spécifiez pas une valeur de protocole de sécurité dans votre code ; Par conséquent, cette opération remplace le Registre.

Les noms des clés de Registre sont similaires aux noms correspondantes `AppContext` bascule, mais sans un `DontEnable` précède le nom. Par exemple, le `AppContext` commutateur `DontEnableSchUseStrongCrypto` est la clé de Registre appelée [SchUseStrongCrypto](#schusestrongcrypto).

Ces clés sont disponibles dans toutes les versions du .NET Framework pour lequel il existe un correctif de sécurité récents. Consultez [mises à jour de sécurité](#security-updates).

Toutes les clés de Registre décrites ci-dessous ont le même effet si vous effectuez la mise en réseau HTTP (<xref:System.Net.ServicePointManager>) ou de la mise en réseau des sockets TCP (<xref:System.Net.Security.SslStream>).

### <a name="schusestrongcrypto"></a>SchUseStrongCrypto

Le `HKEY_LOCAL_MACHINE\SOFTWARE\[Wow6432Node\]Microsoft\.NETFramework\<VERSION>: SchUseStrongCrypto` clé de Registre a une valeur de type DWORD. La valeur 1 entraîne votre application d’utiliser un chiffrement fort. Le chiffrement fort utilise les protocoles de réseau plus sécurisés (TLS 1.2, TLS 1.1 et TLS 1.0) et bloque les protocoles qui ne sont pas sécurisées. La valeur 0 désactive le chiffrement fort. Pour plus d’informations, consultez [indicateur de la SCH_USE_STRONG_CRYPTO](#the-schusestrongcrypto-flag).

Si votre application cible .NET Framework 4.6 ou version ultérieure, cette clé par défaut est une valeur de 1. Qui est sécurisé par défaut que nous recommandons. Si votre application s’exécute sur .NET Framework 4.6, mais il cible une version antérieure, la clé par défaut est 0. Dans ce cas, vous devez explicitement définir sa valeur à 1.

Cette clé doit uniquement avoir une valeur 0 si vous devez vous connecter aux services hérités qui ne prennent pas en charge le chiffrement fort et ne peut pas être mis à niveau.

### <a name="systemdefaulttlsversions"></a>SystemDefaultTlsVersions

Le `HKEY_LOCAL_MACHINE\SOFTWARE\[Wow6432Node\]Microsoft\.NETFramework\<VERSION>: SystemDefaultTlsVersions` clé de Registre a une valeur de type DWORD. La valeur 1 entraîne votre application permettre au système d’exploitation choisir le protocole. La valeur 0 entraîne votre application d’utiliser des protocoles choisis par le .NET Framework.

`<VERSION>` doit être v4.0.30319 (pour .NET Framework 4 et versions ultérieures) ou v2.0.50727 (pour .NET Framework 3.5).

Si votre application cible .NET Framework 4.7 ou versions ultérieures, cette clé par défaut est une valeur de 1. Qui est sécurisé par défaut que nous recommandons. Si votre application s’exécute sur le .NET Framework 4.7 ou versions ultérieures, mais il cible une version antérieure, la clé par défaut est 0. Dans ce cas, vous devez explicitement définir sa valeur à 1.

Pour plus d’informations, consultez [Cumulative mise à jour pour Windows 10 Version 1511 et Windows Server 2016 Technical Preview 4 : 10 mai 2016](https://support.microsoft.com/help/3156421/cumulative-update-for-windows-10-version-1511-and-windows-server-2016).

Pour plus d’informations avec .NET framework 3.5.1, consultez [prise en charge des Versions TLS système par défaut inclus dans .NET Framework 3.5.1 sur Windows 7 SP1 et Server 2008 R2 SP1](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the--net-framework).

Les éléments suivants _. REG_ fichier définit les clés de Registre et leurs variantes de leurs valeurs plus sûres :

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\.NETFramework\v2.0.50727]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\.NETFramework\v4.0.30319]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\v2.0.50727]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\v4.0.30319]
"SystemDefaultTlsVersions"=dword:00000001
"SchUseStrongCrypto"=dword:00000001
```

## <a name="configuring-schannel-protocols-in-the-windows-registry"></a>Configuration des protocoles Schannel dans le Registre Windows

Vous pouvez utiliser le Registre pour un contrôle affiné sur les protocoles qui négocie de votre application client ou serveur. Mise en réseau de votre application passe par Schannel (qui est un autre nom pour [Secure Channel](https://msdn.microsoft.com/library/windows/desktop/aa380123). En configurant `Schannel`, vous pouvez configurer le comportement de votre application.

Démarrer avec la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols` clé de Registre. Sous cette clé, vous pouvez créer toutes les sous-clés dans le jeu de `SSL 2.0`, `SSL 3.0`, `TLS 1.0`, `TLS 1.1`, et `TLS 1.2`. Chacune de ces sous-clés, vous pouvez créer des sous-clés `Client` et/ou `Server`. Sous `Client` et `Server`, vous pouvez créer des valeurs DWORD `DisabledByDefault` (0 ou 1) et `Enabled` (0 ou 0xFFFFFFFF).

## <a name="the-schusestrongcrypto-flag"></a>L’indicateur SCH_USE_STRONG_CRYPTO

Lorsqu’elle est activée (par défaut, par un `AppContext` basculer, ou par le Registre Windows), le .NET Framework utilise le `SCH_USE_STRONG_CRYPTO` indicateur lorsque votre application demande un protocole de sécurité TLS. Le `SCH_USE_STRONG_CRYPTO` indicateur peut être activé par défaut, avec le `AppContext` basculer, ou avec le Registre. Le système d’exploitation passe de l’indicateur à `Schannel`pour lui demander de désactiver les algorithmes de chiffrement faibles connus, le chiffrement suites de tests et les versions du protocole TLS/SSL peuvent être activées dans le cas contraire pour une meilleure interopérabilité. Pour plus d'informations, voir :

- [Canal sécurisé](https://msdn.microsoft.com/library/windows/desktop/aa380123)
- [Structure SCHANNEL_CRED](https://msdn.microsoft.com/library/windows/desktop/aa379810)

Le `SCH_USE_STRONG_CRYPTO` indicateur est également passé à `Schannel` lorsque vous utilisez explicitement le `Tls` (TLS 1.0), `Tls11`, ou `Tls12` énumérée des valeurs de <xref:System.Net.SecurityProtocolType> ou <xref:System.Security.Authentication.SslProtocols>.

## <a name="security-updates"></a>Mises à jour de sécurité

Les meilleures pratiques dans cet article varient selon les récentes mises à jour de sécurité en cours d’installation. Ces mises à jour incluent la possibilité d’utiliser 4.7 de Framework .NET avancées et des fonctionnalités plus loin. Les récentes mises à jour de sécurité sont importantes si votre application s’exécute sur .NET Framework 4.7 et versions ultérieures (même si elle cible une version antérieure).

Pour mettre à jour de .NET Framework pour permettre au système d’exploitation choisir la meilleure version de TLS afin d’utiliser, vous devez installer au moins :

- Le [.NET Framework août 2017 Preview de cumul de la qualité](https://blogs.msdn.microsoft.com/dotnet/2017/08/16/net-framework-august-2017-preview-of-quality-rollup).
- **Ou** le [.NET Framework septembre 2017 et qualité](https://blogs.msdn.microsoft.com/dotnet/2017/09/12/net-framework-september-2017-security-and-quality-rollup).

Voir aussi :

- [Dépendances et les Versions du .NET framework](../migration-guide/versions-and-dependencies.md)
- [Comment : déterminer les Versions du .NET Framework sont installées](../migration-guide/how-to-determine-which-versions-are-installed.md).

## <a name="support-for-tls-12"></a>Prise en charge de TLS 1.2

Pour votre application négocier TLS 1.2, le système d’exploitation et la version du .NET Framework, les deux prendre en charge TLS 1.2.

**Configuration requise du système d’exploitation pour prendre en charge TLS 1.2**

Pour activer ou de réactiver TLS 1.2 et/ou TLS 1.1 sur les systèmes qui les prend en charge, consultez [les paramètres de Registre de sécurité TLS (Transport Layer)](/windows-server/security/tls/tls-registry-settings).

| **OS** | **Prise en charge de TLS 1.2** |
| --- | --- |
| Windows 10</br>Windows Server 2016 | Prise en charge et activé par défaut. |
| Windows 8.1</br>Windows Server 2012 R2 | Prise en charge et activé par défaut. |
| Windows 8.0</br>Windows Server 2012 | Prise en charge et activé par défaut. |
| Windows 7 SP1</br>Windows Server 2008 R2 SP1 | Prise en charge, mais non activé par défaut. Consultez le [les paramètres de Registre de sécurité TLS (Transport Layer)](/windows-server/security/tls/tls-registry-settings) page web pour plus d’informations sur l’activation de TLS 1.2. |
| Windows Server 2008 | Prise en charge de TLS 1.2 et TLS 1.1 requiert une mise à jour. Consultez [mise à jour pour ajouter la prise en charge de TLS 1.1 et TLS 1.2 dans Windows Server 2008 SP2](https://support.microsoft.com/help/4019276/update-to-add-support-for-tls-1-1-and-tls-1-2-in-windows-server-2008-s). |
| Windows Vista | Non pris en charge. |

Pour plus d’informations sur le protocole TLS/SSL protocoles sont activés par défaut sur chaque version de Windows, consultez [protocoles TLS/SSL (SSP Schannel)](https://msdn.microsoft.com/library/windows/desktop/mt808159).

**Configuration requise pour prendre en charge TLS 1.2 avec .NET Framework 3.5**

Ce tableau montre la mise à jour du système d’exploitation que vous devez prendre en charge TLS 1.2 avec .NET Framework 3.5. Nous vous recommandons de qu'appliquer de toutes les mises à jour du système d’exploitation.

| **OS** | **Mise à jour minimale nécessaire pour prendre en charge TLS 1.2 avec .NET Framework 3.5** |
| --- | --- |
| Windows 10</br>Windows Server 2016 | [Afficher un aperçu de la mise à jour cumulative pour Windows 10 Version 1511 et Windows Server 2016 Technical 4 : 10 mai 2016](https://support.microsoft.com/help/3156421/cumulative-update-for-windows-10-version-1511-and-windows-server-2016) |
| Windows 8.1</br>Windows Server 2012 R2 | [Prise en charge des Versions TLS système par défaut inclus dans le .NET Framework 3.5 sur Windows 8.1 et Windows Server 2012 R2](https://support.microsoft.com/help/3154520/support-for-tls-system-default-versions-included-in-the--net-framework) |
| Windows 8.0</br>Windows Server 2012 | [Prise en charge des Versions TLS système par défaut inclus dans le .NET Framework 3.5 sur Windows Server 2012](https://support.microsoft.com/help/3154519/support-for-tls-system-default-versions-included-in-the--net-framework) |
| Windows 7 SP1</br>Windows Server 2008 R2 SP1 | [Prise en charge des Versions TLS système par défaut inclus dans le .NET Framework 3.5.1 sur Windows 7 SP1 et Server 2008 R2 SP1](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the--net-framework) |
| Windows Server 2008 | [Prise en charge des Versions TLS système par défaut inclus dans le .NET Framework 2.0 SP2 sur Windows Vista SP2 et Server 2008 SP2](https://support.microsoft.com/help/3154517/support-for-tls-system-default-versions-included-in-the--net-framework) |
| Windows Vista | Non pris en charge |

## <a name="azure-cloud-services"></a>Services de cloud computing Azure

Si vous utilisez [Azure Cloud Services](https://azure.microsoft.com/services/cloud-services/) rôles Web et de travail pour héberger et exécuter votre application, il existe des considérations dont vous avez besoin pour prendre en compte pour la prise en charge TLS 1.2.

### <a name="net-framework-47-is-not-installed-on-azure-guest-os-by-default"></a>.NET framework 4.7 n’est pas installé par défaut sur le système d’exploitation invité de Azure

La dernière version installée de la dernière version 5 de famille du système d’exploitation Azure invité (Windows Server 2016) est 4.6.2. Pour connaître les versions du .NET Framework sont installées sur chaque système d’exploitation invité de Azure, consultez le [versions de système d’exploitation invité de Azure et matrice de compatibilité SDK](https://docs.microsoft.com/azure/cloud-services/cloud-services-guestos-update-matrix).

Si votre application cible une version du .NET Framework qui n’est pas disponible sur la version du système d’exploitation invité de Azure, vous devez installer vous-même. Consultez [installer .NET sur les rôles de Service Cloud Azure](https://docs.microsoft.com/azure/cloud-services/cloud-services-dotnet-install-dotnet). Si l’installation du framework nécessite un redémarrage, les rôles de service peuvent également redémarrer avant de passer à l’état prêt.

### <a name="azure-guest-os-registry-settings"></a>Paramètres de Registre du système d’exploitation invité Azure

L’image du système d’exploitation invité de Azure pour [Azure Cloud Services](https://azure.microsoft.com/services/cloud-services/) possède déjà le `SchUseStrongCrypto` clé de Registre est définie sur une valeur de 1. Pour plus d’informations, consultez [SchUseStrongCrypto](#schusestrongcrypto).

Définir le [SystemDefaultTlsVersions](#systemdefaulttlsversions) clé de Registre à 1. Consultez [configuration de la sécurité via le Registre Windows](#configuring-security-via-the-windows-registry).
