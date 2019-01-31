---
title: <system.identityModel.services>
ms.date: 03/30/2017
ms.assetid: fa1624dd-2d74-4ae3-942e-498cee261ac5
author: BrucePerlerMS
ms.openlocfilehash: 9728f3caee4dba367e4fc4a3e68213b1055cc3d1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273973"
---
# <a name="systemidentitymodelservices"></a>\<system.identityModel.services>
Section de configuration pour l’authentification à l’aide du protocole WS-Federation.  
  
 \<system.identityModel.services>  
  
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
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<federationConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|Contient les paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> modules (SAM) HTTP.|  
  
### <a name="parent-elements"></a>Éléments parents  
 Aucun.  
  
## <a name="remarks"></a>Notes  
 Ajouter un `<system.identityModel.services>` section au fichier de configuration de votre application pour fournir des paramètres pour le SAM et le WSFAM.  
  
> [!IMPORTANT]
>  Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou le <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, le Gestionnaire d’autorisation des revendications (<xref:System.Security.Claims.ClaimsAuthorizationManager>) et de la stratégie qui est utilisée pour prendre des décisions d’autorisation sont configurés via un `<identityConfiguration>` élément qui est implicitement ou explicitement référencé à partir d’un `<federationConfiguration>` élément dans cette section. Pour plus d’informations, consultez le **remarques** sous le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.  
  
 Le `<system.identityModel.services>` section est représentée par la <xref:System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection> classe. La collection d’enfants `<federationConfiguration>` configurés dans la section des éléments est représenté par la <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElementCollection> classe.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre comment ajouter un `<system.identityModel.services>` section dans un fichier de configuration. Vous devez d’abord ajouter les déclarations de section à la fois pour le `<system.identityModel.services>` section et le `<system.identityModel>` sections. (Lorsque vous ajoutez un `<system.identityModel.services>` section, vous devez également ajouter une déclaration pour le `<system.identityModel>` section pour vous assurer que la valeur par défaut `<identityConfiguration>` section peut être créée par le runtime si nécessaire.) Après ont ajouté les déclarations de section, vous pouvez configurer les paramètres de l’authentification fédérée sous le `<system.identityModel.services>` élément.  
  
```xml  
<configuration>  
  <configSections>  
    <section name="system.identityModel" type="System.IdentityModel.Configuration.SystemIdentityModelSection, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
    <section name="system.identityModel.services" type="System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
  </configSections>  
  
  <!-- Additional elements (not shown) -->  
  
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
  
</configuration>  
```
