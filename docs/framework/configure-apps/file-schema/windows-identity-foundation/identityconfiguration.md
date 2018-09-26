---
title: '&lt;identityConfiguration&gt;'
ms.date: 03/30/2017
ms.assetid: 1db76253-07da-447b-9e7a-3705c7228cf4
author: BrucePerlerMS
ms.openlocfilehash: 11ba7df79ead1693fc6828aeabde413237680737
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47193773"
---
# <a name="ltidentityconfigurationgt"></a>&lt;identityConfiguration&gt;
Spécifie les paramètres de l’identité de niveau de service.  
  
 \<system.identityModel>  
\<identityConfiguration >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration  
      name=xs:string  
      saveBootstrapContext=xs:boolean>  
      maximumClockSkew=TimeSpan >  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Le nom de la section de configuration d’identité. Vous pouvez utiliser ce nom pour faire référence à une section de configuration spécifique. Si aucun `name` attribut est spécifié, la section définit la configuration par défaut. La configuration par défaut est toujours utilisée pour les scénarios de fédération passive. Pour plus d’informations, consultez le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.|  
|saveBootstrapContext|Spécifie si les jetons de démarrage doivent être inclus dans le jeton de session. La valeur peut également être définie sur une collection de gestionnaires de jetons en définissant le `saveBootstrapContext` d’attribut sur le [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) élément. Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.|  
|maximumClockSkew|Un <xref:System.TimeSpan> qui spécifie le décalage d’horloge maximale autorisée. Contrôle le décalage d’horloge maximale autorisée lorsque vous effectuez des opérations de contrainte de temps, telles que la validation de l’heure d’expiration d’une session de connexion. La valeur par défaut est 5 minutes, « 00 : 05:00 ». Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md). Le décalage d’horloge maximale peut également être défini sur une collection de gestionnaires de jetons en définissant le `maximumClockSkew` d’attribut sur le [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) élément. Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<met en cache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Facultatif.|  
|[\<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Facultatif.|  
|[\<claimsAuthenticationManager >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimsauthenticationmanager.md)|Inscrit un gestionnaire d’authentification des revendications pour les revendications entrantes. Facultatif.|  
|[\<claimsAuthorizationManager >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimsauthorizationmanager.md)|Inscrit un gestionnaire d’autorisation des revendications pour les revendications entrantes. Facultatif.|  
|[\<claimTypeRequired >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimtyperequired.md)|Spécifie le jeu de revendications requises pour les jetons de sécurité entrants. Facultatif.|  
|[\<securityTokenHandlers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|Spécifie une collection de gestionnaires de jetons de sécurité. Zéro ou plusieurs collections de gestionnaires de jetons de sécurité peuvent être spécifiées. Facultatif.|  
|[\<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)|Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Facultatif.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<system.identityModel >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel.md)|Fournit la configuration permettant d’activer les options de Windows Identity Foundation (WIF) dans les applications.|  
  
## <a name="remarks"></a>Notes  
 Plusieurs identités configurations peuvent être définies, chacun avec un nom unique. Le comportement est comme suit :  
  
1.  Si aucun `<identityConfiguration>` élément est spécifié. Une configuration d’identité par défaut est créée lors de l’exécution et remplie avec les valeurs par défaut.  
  
2.  Si un seul `<identityConfiguration>` élément est spécifié. Il s’agit de la configuration d’identité par défaut. S’il est nommé ou sans nom n’a pas d’importance.  
  
3.  Si plusieurs `<identityConfiguration>` éléments sont spécifiés. L’élément sans nom spécifie la configuration d’identité par défaut. Il est recommandé que lorsque vous spécifiez plusieurs `<identityConfiguration>` éléments, un d’eux doit avoir un nom.  
  
> [!WARNING]
>  Si vous spécifiez plusieurs `<identityConfiguration>` éléments, un d’eux doit avoir un nom. L’élément sans nom sera la configuration d’identité par défaut.  
  
 Certains des paramètres spécifiés dans le `<identityConfiguration>` élément peut être substitué par les paramètres sur une collection de gestionnaires de jetons de sécurité ou par les paramètres de gestionnaires de jetons de sécurité individuels.  
  
> [!IMPORTANT]
>  Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou le <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, la configuration d’identité qui est référencée par le `<federationConfiguration>` élément configure le Gestionnaire d’autorisation des revendications et la stratégie qui est utilisée pour rendre décisions d’autorisation. Cela est vrai, même dans les scénarios qui ne sont pas les scénarios Web passifs, par exemple les applications Windows Communication Foundation (WCF) ou une application qui n’est pas basée sur le Web. Si l’application n’est pas une application Web passive, le [ \<claimsAuthorizationManager >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/claimsauthorizationmanager.md) élément (et ses éléments de la stratégie enfant, le cas échéant) de la configuration de l’identité référencée sont les seuls paramètres appliqués. Tous les autres paramètres sont ignorés. Pour plus d’informations, consultez le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.  
  
 Le `<identityConfiguration>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityConfigurationElement> classe. Une section de configuration d’identité est représentée par la <xref:System.IdentityModel.Configuration.IdentityConfiguration> classe.  
  
> [!IMPORTANT]
>  En spécifiant les éléments suivants en tant qu’éléments enfants de le `<identityConfiguration>` élément a été déconseillé, même si le comportement est toujours pris en charge pour la compatibilité descendante. Ces éléments doivent, au lieu de cela, être spécifiés sous la [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) élément.  
>   
>  -   [\<audienceUris >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/audienceuris.md)  
> -   [\<issuerNameRegistry >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)  
> -   [\<issuerTokenResolver >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuertokenresolver.md)  
> -   [\<serviceTokenResolver >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicetokenresolver.md)  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une configuration d’identité nommée « alternateConfiguration ». La configuration d’identité spécifie les paramètres par défaut.  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="alternateConfiguration"/>  
</system.identityModel>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IdentityModel.Configuration.IdentityConfiguration>  
 <xref:System.IdentityModel.Configuration.IdentityConfigurationElement>
