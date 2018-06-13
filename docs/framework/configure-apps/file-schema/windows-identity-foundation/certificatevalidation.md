---
title: '&lt;certificateValidation&gt;'
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: af4dc459da49b46d70276d3f4bcd5f94d2a91ffe
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756057"
---
# <a name="ltcertificatevalidationgt"></a>&lt;certificateValidation&gt;
Contrôle les paramètres qui utilisent des gestionnaires de jetons pour valider les certificats. Ces paramètres sont remplacés si un gestionnaire spécifique est configuré avec son propre validateur.  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<certificateValidation >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation  
      certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
      revocationMode="NoCheck||Offline||Online"  
      trustedStoreLocation="CurrentLocation||LocalMachine" >  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|certificateValidationMode|Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valeur qui spécifie le mode de validation à utiliser pour le certificat X.509. La valeur par défaut est « PeerOrChainTrust ». Pour spécifier un validateur personnalisé, définissez cet attribut à « Custom » et le programme de validation à l’aide de la [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) élément. Facultatif.|  
|revocationMode|Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valeur qui spécifie le mode de révocation à utiliser pour le certificat X.509. La valeur par défaut est « Online ». Facultatif.|  
|trustedStoreLocation|A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valeur qui spécifie le magasin de certificats X.509. La valeur par défaut est « Ordinateur_local ». Facultatif.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|Spécifie un type personnalisé pour la validation de certificat. Ce type est utilisé uniquement si la `certificateValidationMode` attribut de la [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) a la valeur « Custom ».|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres d’identité au niveau du service.|  
|[\<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|Fournit des gestionnaires de jetons de configuration pour une collection de sécurité.|  
  
## <a name="remarks"></a>Notes  
 A `<certificateValidation>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de regroupement de gestionnaire de jetons de sécurité sous le `<securityTokenHandlerConfiguration>` élément. Paramètres sur une collection de gestionnaire de jetons remplacent celles spécifiées sur le service. Certains gestionnaires de jetons permettent de spécifier les paramètres de validation de certificat dans la configuration. Paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées à la fois au niveau du service et sur la collection de gestionnaire de jetons de sécurité.  
  
## <a name="example"></a>Exemple  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
