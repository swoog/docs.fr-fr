---
title: '&lt;ajouter&gt; , élément de webRequestModules (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
helpviewer_keywords:
- <webRequestModules>, add element
- webRequestModules, add element
- add element, webRequestModules
- <add> element, webRequestModules
ms.assetid: 47ec4adc-f39f-4bcd-8680-1ec21fd26890
ms.openlocfilehash: d78405546d00797677134e038bbaa69bf088f88e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575708"
---
# <a name="ltaddgt-element-for-webrequestmodules-network-settings"></a>&lt;ajouter&gt; , élément de webRequestModules (paramètres réseau)
Ajoute un module de demande Web personnalisé à l’application.  
  
 \<configuration>  
\<system.net>  
\<webRequestModules>  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add   
  prefix="URI prefix"   
  type="type_fullname, assembly_fullname"   
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|**Attribut**|**Description**|  
|-------------------|---------------------|  
|`prefix`|Le préfixe URI pour les demandes traitées par ce module de demande Web.|  
|`type`|Le nom de type qualifié complet (indiqué par le <xref:System.Type.FullName%2A> propriété) et le nom d’assembly (indiqué par le <xref:System.Reflection.Assembly.FullName%2A> propriété), séparés par une virgule, qui implémente ce module de demande Web.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[webRequestModules](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|Spécifie les modules à utiliser pour demander des informations à partir d’hôtes de réseau.|  
  
## <a name="remarks"></a>Notes  
 Le `prefix` attribut définit le préfixe URI qui utilise le module de demande Web spécifié. Modules de demande Web sont généralement inscrits pour gérer un protocole spécifique, tel que HTTP ou FTP, mais peuvent être inscrits pour gérer une demande à un serveur spécifique ou un chemin d’accès sur un serveur.  
  
 Le module de demande Web est créé lorsqu’un préfixe URI correspondant est passé à la <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> (méthode).  
  
 La valeur de la `prefix` attribut doit-elle être les premiers caractères d’un URI valide. Par exemple, `http` ou `http://www.contoso.com`.
  
 La valeur de la `type` attribut doit être un nom de type valide et le nom de l’assembly correspondant, séparés par une virgule.
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant inscrit un module de demande Web personnalisé pour HTTP. Vous devez remplacer les valeurs de Version et PublicKeyToken par les valeurs correctes pour le module spécifié.  
  
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
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
