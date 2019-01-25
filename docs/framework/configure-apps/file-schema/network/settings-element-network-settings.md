---
title: '&lt;paramètres&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
ms.openlocfilehash: 7db55dd9d2ca79342cadb2320d08ca9235223def
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671849"
---
# <a name="ltsettingsgt-element-network-settings"></a>&lt;paramètres&gt; , élément (paramètres réseau)
Configure les options réseau de base pour l’espace de noms <xref:System.Net?displayProperty=nameWithType>.  
  
 \<configuration>  
\<system.net>  
\<settings>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<settings>  
  <httpListener>...</httpListener>  
  <httpWebRequest>...</httpWebRequest>  
  <ipv6>...</ipv6>  
  <performanceCounters>...</performanceCounters>  
  <servicePointManager>...</servicePointManager>  
  <socket>...</socket>  
  <webProxyScript>...</webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[httpListener](../../../../../docs/framework/configure-apps/file-schema/network/httplistener-element-network-settings.md)|Personnalise les paramètres utilisés par la <xref:System.Net.HttpListener> classe.|  
|[httpWebRequest](../../../../../docs/framework/configure-apps/file-schema/network/httpwebrequest-element-network-settings.md)|Personnalise les paramètres de la demande Web.|  
|[ipv6](../../../../../docs/framework/configure-apps/file-schema/network/ipv6-element-network-settings.md)|Permet d’Internet Protocol version 6 (IPv6) prennent en charge.|  
|[\<performanceCounter >, élément (paramètres réseau)](../../../../../docs/framework/configure-apps/file-schema/network/performancecounter-element-network-settings.md)|Active les compteurs de performances réseau.|  
|[servicePointManager](../../../../../docs/framework/configure-apps/file-schema/network/servicepointmanager-element-network-settings.md)|Configure les connexions aux ressources réseau.|  
|[socket](../../../../../docs/framework/configure-apps/file-schema/network/socket-element-network-settings.md)|Spécifie si les opérations de socket utilisent des ports de terminaison.|  
|[\<webProxyScript >, élément (paramètres réseau)](../../../../../docs/framework/configure-apps/file-schema/network/webproxyscript-element-network-settings.md)|Configure les caractéristiques du script utilisé pour découvrir les proxys Web.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[system.net](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Net?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
