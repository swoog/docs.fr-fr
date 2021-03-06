---
title: Configuration des applications Internet
ms.date: 03/30/2017
helpviewer_keywords:
- downloading Internet resources, default proxy
- sending data, default proxy
- receiving data, default proxy
- downloading Internet resources, configuring Internet applications
- protocol-specific modules
- custom authentication modules
- receiving data, configuring Internet applications
- configuration settings [.NET Framework], Internet applications
- requesting data from Internet, configuring Internet applications
- requesting data from Internet, default proxy
- response to Internet request, default proxy
- Internet, configuring Internet applications
- response to Internet request, configuring Internet applications
- default proxy
- network resources, default proxy
- sending data, configuring Internet applications
- network resources, configuring Internet applications
- Internet, default proxy
ms.assetid: bb707c72-eed2-4a82-8800-c9e68df2fd4f
ms.openlocfilehash: ddc4717c873e65311a8502e66f3edaf39dd89ff9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133800"
---
# <a name="configuring-internet-applications"></a>Configuration des applications Internet
L’[élément de configuration \<system.Net> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md) contient des informations de configuration réseau pour les applications. Avec l’[élément \<system.Net> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md), vous pouvez définir des serveurs proxy, définir des paramètres de gestion de connexion, et inclure des modules de requête et d’authentification personnalisés dans votre application.  
  
 L’[élément \<defaultProxy> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md) définit le serveur proxy retourné par la classe `GlobalProxySelection`. Tout <xref:System.Net.HttpWebRequest> dont la propre propriété <xref:System.Net.HttpWebRequest.Proxy%2A> n’a pas une valeur spécifique utilise le proxy par défaut. En plus de définir l’adresse du proxy, vous pouvez créer une liste d’adresses de serveurs qui n’utiliseront pas le serveur proxy, et vous pouvez indiquer que le proxy ne doit pas être utilisé pour les adresses locales.  
  
 Il est important de noter que les paramètres de Microsoft Internet Explorer sont combinés avec les paramètres de configuration, ces derniers étant prioritaires.  
  
 L’exemple suivant définit `http://proxyserver` comme adresse du serveur proxy par défaut, indique que le proxy ne doit pas être utilisé pour les adresses locales, et spécifie que toutes les requêtes aux serveurs situés dans le domaine contoso.com doivent ignorer le proxy.  
  
```xml  
<configuration>  
    <system.net>  
        <defaultProxy>  
            <proxy  
                usesystemdefault = "false"  
                proxyaddress = "http://proxyserver:80"  
                bypassonlocal = "true"  
            />  
            <bypasslist>  
                <add address="http://[a-z]+\.contoso\.com/" />  
            </bypasslist>  
        </defaultProxy>  
    </system.net>  
</configuration>  
```  
  
 Utilisez l’élément [\<connectionManagement> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md) pour configurer le nombre de connexions persistantes pouvant être établies avec un serveur spécifique ou avec tous les autres serveurs. L’exemple suivant configure l’application pour qu’elle utilise deux connexions persistantes au serveur `www.contoso.com`, quatre connexions persistantes au serveur avec l’adresse IP 192.168.1.2, et une connexion persistante à tous les autres serveurs.  
  
```xml  
<configuration>  
    <system.net>  
        <connectionManagement>  
            <add address="http://www.contoso.com" maxconnection="2" />  
            <add address="192.168.1.2" maxconnection="4" />  
            <add address="*" maxconnection="1" />  
        </connectionManagement>  
    </system.net>  
</configuration>  
```  
  
 Les modules d’authentification personnalisés sont configurés avec l’élément [\<authenticationModules> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md). Ils doivent implémenter l’interface <xref:System.Net.IAuthenticationModule>.  
  
 L’exemple suivant configure un module d’authentification personnalisé.  
  
```xml  
<configuration>  
    <system.net>  
        <authenticationModules>  
            <add type="MyAuthModule, MyAuthModule.dll" />  
        </authenticationModules>  
    </system.net>  
</configuration>  
```  
  
 Vous pouvez utiliser l’élément [\<webRequestModules> (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md) pour configurer votre application afin qu’elle utilise des modules propres au protocole personnalisés pour demander des informations à partir des ressources Internet. Les modules spécifiés doivent implémenter l’interface <xref:System.Net.IWebRequestCreate>. Vous pouvez substituer les modules HTTP, HTTPS et de requête de fichier par défaut en spécifiant votre module personnalisé dans le fichier de configuration, comme dans l’exemple suivant.  
  
```xml  
<configuration>  
    <system.net>  
        <webRequestModules>  
            <add  
                prefix="HTTP"  
                type = "MyHttpRequest.dll, MyHttpRequestCreator"  
            />  
        </webRequestModules>  
    </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Programmation réseau dans le .NET Framework](../../../docs/framework/network-programming/index.md)
- [Schéma des paramètres réseau](../../../docs/framework/configure-apps/file-schema/network/index.md)
- [\<system.Net>, élément (Paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)
