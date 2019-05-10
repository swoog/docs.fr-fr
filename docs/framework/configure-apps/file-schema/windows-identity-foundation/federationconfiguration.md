---
title: <federationConfiguration>
ms.date: 03/30/2017
ms.assetid: 8b14054c-6d07-46ab-ab58-03f14beac0f2
author: BrucePerlerMS
ms.openlocfilehash: 102aadaaa7d7780f1266e1abcea46f0fcf95671e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64622552"
---
# <a name="federationconfiguration"></a>\<federationConfiguration>
Configure le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) lorsque vous utilisez federated authentication via le protocole WS-Federation. Configure le <xref:System.Security.Claims.ClaimsAuthorizationManager> lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications.  
  
 \<system.identityModel.services>  
\<federationConfiguration>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration name=xs:string identityConfigurationName=xs:string>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Le nom de cet élément de configuration de fédération. Cet attribut fournit principalement un point d’extensibilité pour les protocoles à venir. Facultatif.|  
|identityConfigurationName|Le nom de la section de configuration d’identité tel que spécifié dans un [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément à utiliser. Si cet attribut n’est pas spécifié, la section de configuration d’identité par défaut est utilisée. Facultatif.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<cookieHandler>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|Configure le Gestionnaire de cookies utilisé par le module SAM. Facultatif.|  
|[\<serviceCertificate>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicecertificate.md)|Configure le certificat qui est utilisé pour chiffrer et déchiffrer les jetons. Facultatif.|  
|[\<wsFederation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/wsfederation.md)|Configure le Module d’authentification WS-Federation (WSFAM). Facultatif.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<system.identityModel.services>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel-services.md)|Section de configuration pour l’authentification à l’aide du protocole WS-Federation.|  
  
## <a name="remarks"></a>Notes  
 Le \<federationConfiguration > élément fournit différents paramètres dans deux scénarios différents :  
  
- Lorsque vous utilisez WS-Federation dans une application Web passive, l’élément contient des paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM). Il fait référence également à la configuration d’identité à utiliser pour configurer les gestionnaires de jetons de sécurité et des certificats et des composants tels que le Gestionnaire d’autorisation des revendications et le Gestionnaire d’authentification des revendications.  
  
- Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> de classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, l’élément fait référence à la configuration d’identité qui configure le Gestionnaire d’autorisation des revendications et une stratégie qui est utilisée pour rendre l’autorisation prendre des décisions. Cela est vrai, même dans les scénarios qui ne sont pas les scénarios Web passifs ; par exemple, les applications Windows Communication Foundation (WCF) ou une application qui n’est pas basée sur le Web. Si l’application n’est pas une application Web passive, le [ \<claimsAuthorizationManager >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimsauthorizationmanager.md) élément (et ses éléments de la stratégie enfant, le cas échéant) de la configuration de l’identité référencée par le `<federationConfiguration>` élément les seuls paramètres sont appliqués. Tous les autres sont ignorés.  
  
 Quel que soit le scénario, le runtime charge la configuration de fédération par défaut. Le comportement est défini comme suit :  
  
1. S’il existe aucune `<federationConfiguration>` élément présent, le runtime crée une configuration de fédération et le remplit avec les valeurs par défaut. Cette configuration de fédération par défaut se réfère à la configuration d’identité par défaut.  
  
2. Si un seul `<federationConfiguration>` élément est présent, il s’agit de la configuration de fédération par défaut qu’il est nommé ou sans nom. Si son `identityConfiguration` attribut est spécifié, la configuration d’identité nommée est référencée ; sinon, la configuration d’identité par défaut est référencée.  
  
3. Si un sans nom `<federationConfiguration>` élément est présent, il s’agit de la configuration de fédération par défaut. Si son `identityConfiguration` attribut est spécifié, la configuration d’identité nommée est référencée ; sinon, la configuration d’identité par défaut est référencée.  
  
4. Si plusieurs nommé `<federationConfiguration>` éléments sont présents et absence sans nom `<federationConfiguration>` élément est présent, une exception est levée.  
  
 En règle générale, un seul `<federationConfiguration>` section est définie. Cette section est la configuration de fédération par défaut. Vous pouvez spécifier plusieurs, nommés de manière unique `<federationConfiguration>` éléments ; Toutefois, dans ce cas, si vous souhaitez charger une configuration de fédération autre que celui sans nom, vous devez fournir un gestionnaire pour le. <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfigurationCreated> événements et définissez le <xref:System.IdentityModel.Services.Configuration.FederationConfigurationCreatedEventArgs.FederationConfiguration%2A?displayProperty=nameWithType> propriété dans le gestionnaire pour un <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> objet initialisée avec les valeurs appropriées `<federationConfiguration>` élément dans le fichier de configuration.  
  
 Le `<federationConfiguration>` élément est représenté par la <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElement> classe. L’objet de configuration lui-même est représenté par la <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> classe. Un seul <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> instance est définie sur le <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType> propriété et fournit une configuration fédérée de l’application.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre un `<federationConfiguration>` élément qui spécifie les paramètres pour le WSFAM et spécifie que le Gestionnaire de cookie par défaut (une instance de la <xref:System.IdentityModel.Services.ChunkedCookieHandler> classe) est utilisé par le module SAM.  
  
> [!WARNING]
>  Dans cet exemple, ni le Gestionnaire de cookies ni le WSFAM sont requis pour utiliser HTTPS. Il s’agit, car le `requireHttps` d’attribut sur le `<wsFederation>` élément et le `requireSsl` d’attribut sur le `<cookieHandlerElement>` sont `false`. Ces paramètres ne sont pas recommandés pour la plupart des environnements de production car ils pourraient présenter un risque de sécurité.  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <wsFederation passiveRedirectEnabled="true"   
      issuer="http://localhost:15839/wsFederationSTS/Issue"   
      realm="http://localhost:50969/" reply="http://localhost:50969/"   
      requireHttps="false"   
      signOutReply="http://localhost:50969/SignedOutPage.html"   
      signOutQueryString="Param1=value2&Param2=value2"   
      persistentCookiesOnPassiveRedirects="true" />  
    <cookieHandler requireSsl="false" />  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IdentityModel.Services.WSFederationAuthenticationModule>
- <xref:System.IdentityModel.Services.SessionAuthenticationModule>
- <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType>
- [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)
