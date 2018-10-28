---
title: '&lt;socket&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/socket
- http://schemas.microsoft.com/.NetConfiguration/v2.0#socket
helpviewer_keywords:
- <socket> element
- socket element
ms.assetid: 366c634c-7d16-478f-aedf-053eda94a1a0
ms.openlocfilehash: ff06fd6518e67020b4d67d4e081307b8e54bae85
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194694"
---
# <a name="ltsocketgt-element-network-settings"></a>&lt;socket&gt; , élément (paramètres réseau)
Spécifie si les opérations de socket utilisent des ports de terminaison.  
  
 \<configuration>  
\<system.net>  
\<Paramètres >  
\<Socket >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<socket  
  alwaysUseCompletionPortsForConnect="true|false"  
  alwaysUseCompletionPortsForAccept="true|false"  
  ipProtectionLevel="EdgeRestricted|Restricted|Unrestricted|Unspecified"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|**Attribut**|**Description**|  
|-------------------|---------------------|  
|`alwaysUseCompletionPortsForAccept`|Indique si le socket doit toujours utiliser des ports de terminaison pour accepter les appels de méthode. La valeur par défaut est `false`.|  
|`alwaysUseCompletionPortsForConnect`|Indique si le socket doit toujours utiliser des ports de terminaison pour les appels de méthode Connect. La valeur par défaut est `false`.|  
|`ipProtectionLevel`|Spécifie la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> à utiliser pour un socket. La valeur par défaut dépend de la version de Windows.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[Paramètres](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|Configure les options réseau de base pour l’espace de noms <xref:System.Net>.|  
  
## <a name="remarks"></a>Notes  
 Le `alwaysUseCompletionPortsForAccept` et `alwaysUseCompletionPortsForConnect` attributs sont utilisés pour spécifier le comportement par défaut concernant l’utilisation de ports de terminaison par les classes dans le <xref:System.Net.Sockets?displayProperty=nameWithType>.namespace. Ports de terminaison sont recommandés pour les applications de serveur hautes performances.  
  
 La valeur par défaut pour le `alwaysUseCompletionPortsForAccept` et `alwaysUseCompletionPortsForConnect` attributs est **false**.  
  
 Le <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForAccept%2A> peut être utilisée pour obtenir la valeur actuelle de la `alwaysUseCompletionPortsForAccept` attribut à partir des fichiers de configuration applicables. Le <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForConnect%2A> peut être utilisée pour obtenir la valeur actuelle de la `alwaysUseCompletionPortsForConnect` attribut à partir des fichiers de configuration applicables.  
  
 Le `ipProtectionLevel` attribut spécifie la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> à utiliser pour un socket. Le <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> propriété permet la configuration d’une restriction pour un socket IPv6 à une portée spécifiée, telle que les adresses avec le même lien locales ou préfixe local de site. Cette option permet aux applications de placer des restrictions d’accès sur les sockets IPv6. Ces restrictions permettent à une application qui s'exécute sur un réseau local privé de se renforcer facilement et efficacement contre les attaques externes. Cette option élargit ou limite la portée d’un socket d’écoute, permettant l’accès illimité des utilisateurs publics et privés le cas échéant, ou restreindre l’accès uniquement au même site, en fonction des besoins.  
  
 Cela `ipProtectionLevel` paramètre d’attribut affecte uniquement le trafic entrant initial :  
  
-   Un serveur TCP à l’écoute les connexions entrantes sur un socket.  
  
-   Application UDP qui reçoit un paquet sur un socket.  
  
 Ce paramètre de configuration n’affecte pas les connexions TCP déjà établies (le trafic est illimité dans les deux directions) et n’affecte pas une application qui envoie des paquets UDP.  
  
 Les valeurs possibles pour le `ipProtectionLevel` paramètre d’attribut correspondent aux niveaux de protection définis spécifiés dans le <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> énumération comme suit :  
  
|**Valeur d’attribut**|**Description**|  
|-|-|  
|EdgeRestricted|Le niveau de protection IP est limité à un périmètre. Cette valeur peut être utilisée par les applications conçues pour fonctionner sur Internet. Ce paramètre n’autorise pas de parcours de traduction d’adresses réseau (NAT) à l’aide de l’implémentation de Windows Teredo. Ces applications peuvent contourner les pare-feux IPv4, applications ; doivent donc être renforcées contre les attaques Internet dirigées vers le port ouvert. Sur Windows Server 2003 et Windows XP, la valeur par défaut pour le niveau de Protection IP sur un socket est périmètre limité.|  
|restreint|Le niveau de protection IP est limité. Cette valeur peut être utilisée par les applications intranet qui n’implémentent pas de scénarios Internet. Ces applications sont généralement pas testées ou renforcées contre les attaques Internet. Ce paramètre limite le trafic reçu aux liens locaux uniquement.|  
|Non restreint|Le niveau de protection IP est illimité. Cette valeur peut être utilisée par les applications conçues pour fonctionner sur Internet, notamment les applications qui tirent parti des fonctions de traversée NAT IPv6 intégrées à Windows (Teredo, par exemple). Ces applications peuvent contourner les pare-feux IPv4, applications ; doivent donc être renforcées contre les attaques Internet dirigées vers le port ouvert. Sur Windows Server 2008 R2 et Windows Vista, la valeur par défaut pour le niveau de Protection IP sur un socket est illimitée.|  
|Non spécifié|Le niveau de protection IP n’est pas spécifié. Sur Windows 7 et Windows Server 2008 R2, la valeur par défaut pour le niveau de Protection IP sur un socket n’est pas spécifiée.|  
  
 La valeur par défaut pour le `ipProtectionLevel` attribut est **Unspecified**.  
  
 Le <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> propriété peut être utilisée pour obtenir la valeur actuelle de la `ipProtectionLevel` attribut à partir des fichiers de configuration applicables.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier que les ports de terminaison doivent être utilisés et que la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> doit être illimité.  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <socket  
        alwaysUseCompletionPortsForAccept="true"  
        alwaysUseCompletionPortsForConnect="true"  
        ipProtectionLevel="Unrestricted"  
       />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
- <xref:System.Net?displayProperty=nameWithType>  
- <xref:System.Net.Configuration.SocketElement?displayProperty=nameWithType>  
- <xref:System.Net.Sockets?displayProperty=nameWithType>  
- <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType>  
- <xref:System.Net.Sockets.SocketOptionName.IPProtectionLevel?displayProperty=nameWithType>  
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
