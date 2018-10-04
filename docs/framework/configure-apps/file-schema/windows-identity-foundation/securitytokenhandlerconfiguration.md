---
title: '&lt;securityTokenHandlerConfiguration&gt;'
ms.date: 03/30/2017
ms.assetid: 28724cc6-020c-4a06-9a1f-d7594f315019
author: BrucePerlerMS
ms.openlocfilehash: d66771ec7ed52ace52df6bb3bfafdcf9cce989b5
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48793277"
---
# <a name="ltsecuritytokenhandlerconfigurationgt"></a>&lt;securityTokenHandlerConfiguration&gt;
Fournit la configuration de la collection de gestionnaires de jetons.  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration saveBootstrapContext=xs:boolean  
          maximumClockSkew=TimeSpan>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|saveBootstrapContext|Spécifie si les jetons de démarrage doivent être inclus dans le jeton de session. La valeur peut également être définie sur une collection de gestionnaires de jetons en définissant le `saveBootstrapContext` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément. Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.|  
|maximumClockSkew|Un <xref:System.TimeSpan> qui spécifie le décalage d’horloge maximale autorisée. Contrôle le décalage d’horloge maximale autorisée lorsque vous effectuez des opérations de contrainte de temps, telles que la validation de l’heure d’expiration d’une session de connexion. La valeur par défaut est 5 minutes, « 00 : 05:00 ». Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md). Le décalage d’horloge maximale peut également être défini au niveau du service en définissant le `maximumClockSkew` d’attribut sur le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément. Une valeur définie sur la collection de gestionnaires de jetons substitue à la valeur définie sur le service.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<audienceUris >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/audienceuris.md)|Spécifie le jeu d’URI qui sont des identificateurs acceptables de cette partie de confiance. Facultatif.|  
|[\<met en cache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Facultatif.|  
|[\<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md)|Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur. Facultatif.|  
|[\<issuerNameRegistry >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons. Facultatif.|  
|[\<issuerTokenResolver >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuertokenresolver.md)|Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons. Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant. Facultatif.|  
|[\<serviceTokenResolver >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/servicetokenresolver.md)|Inscrit le résolveur de jeton de service qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons. Le programme de résolution de jeton de service est utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant. Facultatif.|  
|[\<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)|Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons. Peut être spécifié au niveau du service ou sur une collection de gestionnaires de jetons de sécurité. Facultatif.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.|  
  
## <a name="remarks"></a>Notes  
 Cette section fournit des valeurs de propriété pour un <xref:System.IdentityModel.Tokens.SecurityTokenHandlerConfiguration> objet. Paramètres configurés dans cette section remplacent ceux configurés sur le service. Certains de ces paramètres peuvent, à son tour, être substituée par les paramètres qui sont spécifiés lors de l’ajout d’un gestionnaire à la collection de gestionnaires de jetons de sécurité.  
  
## <a name="example"></a>Exemple  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>   
      <securityTokenHandlerConfiguration>  
  
        <audienceUris>  
          <clear/>  
          <add value="http://www.example.com/myapp/" />  
        </audienceUris>  
  
        <issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel">  
          <trustedIssuers>  
            <add thumbprint="97249e1a … 4c9158de" name="contoso.com" />  
          </trustedIssuers>  
        </issuerNameRegistry>  
  
        <issuerTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
        <serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```
