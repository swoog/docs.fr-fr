---
title: <caches>
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: b1d04280ef993297102d446ba5a7db54e8404dd8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285660"
---
# <a name="caches"></a>\<caches>
Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<caches>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<sessionSecurityTokenCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.|  
|[\<tokenReplayCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|Inscrit un cache de relecture de jetons avec un service ou une collection de gestionnaires de jetons de sécurité.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres de l’identité de niveau de service.|  
|[\<securityTokenHandlerConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|Fournit une configuration pour une collection de sécurité gestionnaires de jetons.|  
  
## <a name="remarks"></a>Notes  
 Un `<caches>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément. Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.  
  
 Le `<caches>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> classe. Caches configurés sont représentées par la <xref:System.IdentityModel.Configuration.IdentityModelCaches> classe.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>). La configuration est extraite la `ClaimsAwareWebFarm` exemple.  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
