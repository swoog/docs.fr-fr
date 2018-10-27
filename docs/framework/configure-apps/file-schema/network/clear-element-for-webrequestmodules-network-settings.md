---
title: '&lt;Désactivez&gt; , élément de webRequestModules (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- <clear> element, webRequestModules
- <webRequestModules>, clear element
- webRequestModules, clear element
- clear element, webRequestModules
ms.assetid: 48f38bcb-f30c-4b74-a8f0-1a3caf1aa96f
ms.openlocfilehash: 39d4a184972036677aaa9fdb33e672521033d35f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190526"
---
# <a name="ltcleargt-element-for-webrequestmodules-network-settings"></a>&lt;Désactivez&gt; , élément de webRequestModules (paramètres réseau)
Supprime tous les modules de demande Web inscrits de l’application.  
  
 \<configuration>  
\<system.net>  
\<webRequestModules>  
\<Désactivez >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[webRequestModules](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|Spécifie les modules à utiliser pour demander des informations à partir d’hôtes de réseau.|  
  
## <a name="remarks"></a>Notes  
 Le `clear` élément supprime inscrits tous les modules de demande Web qui ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant efface tous les modules de demande Web et inscrit un module de demande Web pour HTTP.  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <clear/>  
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
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
