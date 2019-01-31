---
title: <webRequestModules>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#webRequestModules
helpviewer_keywords:
- webRequestModules element
- <webRequestModules> element
ms.assetid: 1263de11-3e0a-4f94-97c9-710b2ae53817
ms.openlocfilehash: fd7c5765665345906597963f8a4b2dbf7fcc7227
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288845"
---
# <a name="webrequestmodules-element-network-settings"></a>\<webRequestModules >, élément (paramètres réseau)
Spécifie les modules à utiliser pour demander des informations à partir d’hôtes de réseau.  
  
 \<configuration>  
\<system.net>  
\<webRequestModules>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<webRequestModules>   
</webRequestModules>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[add](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-webrequestmodules-network-settings.md)|Ajoute un module de demande Web personnalisé à l’application.|  
|[clear](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-webrequestmodules-network-settings.md)|Supprime tous les modules de demande Web inscrits de l’application.|  
|[remove](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-webrequestmodules-network-settings.md)|Supprime un module de demande Web personnalisé de l’application.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[system.net](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.|  
  
## <a name="remarks"></a>Notes  
 Le `webRequestModules` élément inscrit les descendants de le <xref:System.Net.WebRequest> classe pour gérer les demandes d’informations sur les hôtes de réseau. Modules de demande Web doivent implémenter le <xref:System.Net.IWebRequestCreate> interface.  
  
 Le .NET Framework inclut des modules de demande Web pour les URI qui commencent par `http://`, `https://`, et `file://`. Vous pouvez remplacer les modules par défaut qu’en inscrivant un module personnalisé dans le fichier de configuration.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant inscrit le module HTTP par défaut. Vous devez remplacer les valeurs de Version et PublicKeyToken par les valeurs correctes pour le module spécifié.  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Net.WebRequest>
- <xref:System.Net.IWebRequestCreate>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
