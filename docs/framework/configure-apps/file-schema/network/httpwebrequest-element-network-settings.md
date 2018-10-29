---
title: '&lt;httpWebRequest&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/httpWebRequest
- http://schemas.microsoft.com/.NetConfiguration/v2.0#httpWebRequest
helpviewer_keywords:
- <httpWebRequest> element
- httpWebRequest element
ms.assetid: 52acd9d2-5bdc-4dc4-9c2a-f0a476ccbb31
ms.openlocfilehash: 0d3feb168acbd623270a2038bf06a3c97126bd05
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50205150"
---
# <a name="lthttpwebrequestgt-element-network-settings"></a>&lt;httpWebRequest&gt; , élément (paramètres réseau)
Personnalise les paramètres de la demande Web.  
  
 \<configuration>  
\<system.net>  
\<Paramètres >  
\<httpWebRequest >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<httpWebRequest  
  maximumResponseHeadersLength="size"  
  maximumErrorResponseLength="size"  
  maximumUnauthorizedUploadLength="size"  
  useUnsafeHeaderParsing="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|**Attribut**|**Description**|  
|-------------------|---------------------|  
|`maximumResponseHeadersLength`|Spécifie la longueur maximale d’un en-tête de réponse, en kilo-octets. La valeur par défaut est 64. La valeur -1 indique qu’aucune limite de taille ne sera imposée sur les en-têtes de réponse.|  
|`maximumErrorResponseLength`|Spécifie la longueur maximale d’une réponse d’erreur, en kilo-octets. La valeur par défaut est 64. La valeur -1 indique qu’aucune limite de taille ne sera imposée sur la réponse d’erreur.|  
|`maximumUnauthorizedUploadLength`|Spécifie la longueur maximale d’un téléchargement en réponse à un code d’erreur non autorisé, en octets. La valeur par défaut est -1. La valeur -1 indique qu’aucune limite de taille ne sera imposée sur le téléchargement.|  
|`useUnsafeHeaderParsing`|Spécifie si l’analyse des en-têtes non sécurisé est activé. La valeur par défaut est `false`.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[Paramètres](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|Configure les options réseau de base pour l’espace de noms <xref:System.Net>.|  
  
## <a name="remarks"></a>Notes  
 Par défaut, le .NET Framework applique strictement la norme RFC 2616 pour l’analyse URI. Certaines réponses du serveur peuvent inclure des caractères de contrôle dans les champs interdits, ce qui provoquent le <xref:System.Net.HttpWebRequest.GetResponse?displayProperty=nameWithType> méthode lève un <xref:System.Net.WebException>. Si **useUnsafeHeaderParsing** a la valeur **true**, <xref:System.Net.HttpWebRequest.GetResponse?displayProperty=nameWithType> ne lèvera pas dans ce cas, toutefois, votre application sera vulnérable à plusieurs formes d’attaques d’analyse URI. La meilleure solution consiste à modifier le serveur afin que la réponse n’inclut pas les caractères de contrôle.  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier une valeur plus élevée à la longueur d’en-tête maximale normal.  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <httpWebRequest  
        maximumResponseHeadersLength="128"  
      />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
- <xref:System.Net.HttpWebRequest.MaximumResponseHeadersLength%2A>  
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
