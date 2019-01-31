---
title: <clear>, élément de <namedCaches>
ms.date: 03/30/2017
helpviewer_keywords:
- <clear> element for <namedCaches>
- clear element for <namedCaches>
ms.assetid: ea01a858-65da-4348-800f-5e3df59d4d79
ms.openlocfilehash: aaf5c2360b53a1cd6e5775a195c89c96ed6440a3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288663"
---
# <a name="clear-element-for-namedcaches"></a>\<Désactivez >, élément pour \<namedCaches >
Efface tous les `namedCache` entrées dans le `namedCaches` collection pour un cache mémoire.  
  
 \<system.runtime.caching>  
\<memoryCache>  
\<namedCaches>  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<namedCaches>  
    <clear name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 `None`  
  
### <a name="child-elements"></a>Éléments enfants  
 `None`  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<namedCaches>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|Contient une collection de paramètres de configuration pour l’élément nommé <xref:System.Runtime.Caching.MemoryCache> instances.|  
  
## <a name="remarks"></a>Notes  
 Le `clear` élément efface tous les `namedCache` entrées dans la collection de cache nommé pour un cache mémoire. Vous pouvez utiliser la `clear` élément avant d’utiliser le `add` élément à ajouter une nouvelle entrée de cache nommé afin d’être certain qu’il n’existe aucun autre cache nommé dans la collection.  
  
## <a name="see-also"></a>Voir aussi
- [\<namedCaches >, élément (paramètres de Cache)](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
