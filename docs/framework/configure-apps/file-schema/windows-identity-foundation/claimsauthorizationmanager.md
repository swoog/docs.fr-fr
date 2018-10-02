---
title: '&lt;claimsAuthorizationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 9354eee3-f692-4ad6-8427-3169686b8bcc
author: BrucePerlerMS
ms.openlocfilehash: a745339cffdada56a9b7f27f3f879b9d437c2da2
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48032099"
---
# <a name="ltclaimsauthorizationmanagergt"></a>&lt;claimsAuthorizationManager&gt;
Inscrit un gestionnaire d’autorisation des revendications pour les revendications entrantes.  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<claimsAuthorizationManager >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthorizationManager type = xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthorizationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Un type personnalisé qui dérive de la <xref:System.Security.Claims.ClaimsAuthorizationManager> classe. Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 S’il existe aucune `type` attribut, ou si le `type` les références d’attribut le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthorizationManager>` élément ne prend pas d’éléments enfants ; Toutefois, les classes dérivées de <xref:System.Security.Claims.ClaimsAuthorizationManager> peut définir les éléments de configuration enfants.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres de l’identité de niveau de service.|  
  
## <a name="remarks"></a>Notes  
 Le comportement par défaut fourni par le biais du <xref:System.Security.Claims.ClaimsAuthorizationManager> classe autorise toujours les revendications entrantes. Si aucun `type` attribut est spécifié ou si le `type` attribut spécifie le <xref:System.Security.Claims.ClaimsAuthorizationManager> (classe), le `<claimsAuthorizationManager>` élément ne prend pas d’éléments enfants. Vous pouvez spécifier le `type` attribut d’inscrire un type dérivé la <xref:System.Security.Claims.ClaimsAuthorizationManager> classe pour implémenter un comportement personnalisé. Les classes dérivées peuvent prendre en charge la configuration via les éléments enfants de la `<claimsAuthorizationManager>` élément en substituant le <xref:System.Security.Claims.ClaimsAuthorizationManager.LoadCustomConfiguration%2A> méthode pour traiter ces éléments. Le schéma défini pour les éléments enfants revient le Concepteur de la classe.  
  
> [!IMPORTANT]
>  Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou le <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, la configuration d’identité qui est référencée par le `<federationConfiguration>` élément configure le Gestionnaire d’autorisation des revendications et la stratégie qui est utilisée pour rendre décisions d’autorisation. Cela est vrai, même dans les scénarios qui ne sont pas les scénarios Web passifs, par exemple les applications Windows Communication Foundation (WCF) ou une application qui n’est pas basée sur le Web. Si l’application n’est pas une application Web passive, le `<claimsAuthorizationManager>` élément (et ses éléments de la stratégie enfant, le cas échéant) de la configuration de l’identité référencée sont les seuls paramètres appliqués. Tous les autres paramètres sont ignorés. Pour plus d’informations, consultez le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.  
  
 Cet élément définit les <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthorizationManager%2A?displayProperty=nameWithType> propriété.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant illustre la configuration d’une autorisation de revendications gestionnaire qui implémente la stratégie composée de paires de ressource-action qui spécifient chacune des combinaisons booléennes des revendications comportant un demandeur doit effectuer l’action sur la ressource. Vous trouverez le code qui implémente le Gestionnaire d’autorisation des revendications capable d’utiliser cette stratégie dans le `ClaimsBasedAuthorization` exemple.  
  
```xml  
<system.identityModel>  
    <identityConfiguration>  
      <claimsAuthorizationManager type="ClaimsAuthorizationLibrary.MyClaimsAuthorizationManager, ClaimsAuthorizationLibrary">  
        <policy resource="http://localhost:28491/Developers.aspx" action="GET">  
          <or>  
            <claim claimType="http://schemas.microsoft.com/ws/2008/06/identity/claims/role" claimValue="developer" />  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
          </or>  
        </policy>  
        <policy resource="http://localhost:28491/Administrators.aspx" action="GET">  
          <and>  
            <claim claimType="http://schemas.xmlsoap.org/claims/Group" claimValue="Administrator" />  
            <claim claimType="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country" claimValue="USA" />  
          </and>  
        </policy>  
        <policy resource="http://localhost:28491/Default.aspx" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/" action="GET">  
        </policy>  
        <policy resource="http://localhost:28491/Claims.aspx" action="GET">  
        </policy>  
      </claimsAuthorizationManager>  
    <identityConfiguration>  
<system.identityModel>  
```
