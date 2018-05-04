---
title: '&lt;ajouter&gt; , élément pour &lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- add element for <namedCaches>
- <add> element for <namedCaches>
ms.assetid: ce2a63a8-c829-4742-a6ea-72ee5d89f169
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: d65dfd9a1560f2657f48b327277b64ab77014b47
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-element-for-ltnamedcachesgt"></a>&lt;ajouter&gt; , élément pour &lt;namedCaches&gt;
Ajoute un `namedCache` entrée à la `namedCaches` collection pour un cache mémoire.  
  
 \<system.runtime.caching>  
\<memoryCache>  
\<namedCaches >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<namedCaches>  
    <add name="default" />  
      <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a>Type  
 `None`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|-|-|  
|`CacheMemoryLimitMegabytes`|Valeur entière qui spécifie la taille maximale autorisée (en mégaoctets) qui une instance d’un <xref:System.Runtime.Caching.MemoryCache> peut atteindre. La valeur par défaut est 0, ce qui signifie que le <xref:System.Runtime.Caching.MemoryCache> heuristiques de redimensionnement automatique de la classe sont utilisées par défaut.|  
|`Name`|Nom du cache.|  
|`PhysicalMemoryLimitPercentage`|Valeur entière comprise entre 0 et 100 qui spécifie le pourcentage maximal de mémoire d’ordinateur physiquement installée qui peut être utilisé par le cache. La valeur par défaut est 0, ce qui signifie que le <xref:System.Runtime.Caching.MemoryCache> heuristiques de redimensionnement automatique de la classe sont utilisées par défaut.|  
|`PollingInterval`|Valeur qui indique l’intervalle de temps après lequel l’implémentation de cache compare la charge de mémoire actuelle aux limites de mémoire absolue et en pourcentage définies pour l’instance de cache. Cette valeur est entrée dans le format de « Hh : mm : ».|  
  
### <a name="child-elements"></a>Éléments enfants  
 `None`  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<namedCaches>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|Contient une collection de paramètres de configuration pour le nommé <xref:System.Runtime.Caching.MemoryCache> instances.|  
  
## <a name="remarks"></a>Notes  
 Le `add` élément ajoute une entrée à la `namedCaches` collection pour un cache mémoire. Vous pouvez utiliser la [effacer](../../../../../docs/framework/configure-apps/file-schema/runtime/clear-element-for-namedcaches.md) élément avant d’utiliser le `add` pour garantir qu’il n’existe aucun autre cache nommé dans la collection. Cet élément peut être utilisé dans le fichier machine.config et dans le fichier Web.config.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment définir les paramètres de la valeur par défaut `namedCache` entrée à la `namedCaches` collection pour un cache mémoire.  
  
```xml  
<configuration>  
  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="default"   
               cacheMemoryLimitMegabytes="0"   
               physicalMemoryPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [\<namedCaches >, élément (paramètres de Cache)](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
