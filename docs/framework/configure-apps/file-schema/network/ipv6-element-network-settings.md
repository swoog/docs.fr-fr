---
title: <ipv6>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/ipv6
- http://schemas.microsoft.com/.NetConfiguration/v2.0#ipv6
helpviewer_keywords:
- <ipv6> element
- ipv6 element
ms.assetid: 10b79aef-327b-4718-a892-e11f55e4d169
ms.openlocfilehash: 708604c782690efa631e4eab0aa62c1c0b1f657b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279693"
---
# <a name="ipv6-element-network-settings"></a>\<IPv6 >, élément (paramètres réseau)
Permet d’Internet Protocol version 6 (IPv6) des réponses à partir des membres obsolètes de la <xref:System.Net.Dns> classe.  
  
 \<configuration>  
\<system.net>  
\<settings>  
\<ipv6>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<ipv6  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|**Attribut**|**Description**|  
|-------------------|---------------------|  
|`enabled`|Spécifie si les membres de la <xref:System.Net.Dns> classe retourner Internet Protocol version 6 (IPv6) adresses. La valeur par défaut est `false`.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[settings](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|Configure les options réseau de base pour l’espace de noms <xref:System.Net>.|  
  
## <a name="remarks"></a>Notes  
 Ce paramètre permet la prise en charge IPv6 pour les membres obsolètes de la <xref:System.Net.Dns> classe : <xref:System.Net.Dns.BeginGetHostByName%2A>, <xref:System.Net.Dns.BeginResolve%2A>, <xref:System.Net.Dns.EndGetHostByName%2A>, <xref:System.Net.Dns.EndResolve%2A>, <xref:System.Net.Dns.GetHostByAddress%2A>, <xref:System.Net.Dns.GetHostByName%2A>, et <xref:System.Net.Dns.Resolve%2A>. Pour d’autres membres de la <xref:System.Net?displayProperty=nameWithType> espace de noms, les adresses IPv6 peuvent être retournées si IPv6 est activé dans le système d’exploitation.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment activer la prise en charge IPv6 pour la <xref:System.Net.Dns> classe.  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <ipv6 enabled="true"/>  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Net?displayProperty=nameWithType>
- <xref:System.Net.Dns?displayProperty=nameWithType>
- <xref:System.Net.Sockets.Socket.OSSupportsIPv6%2A?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
