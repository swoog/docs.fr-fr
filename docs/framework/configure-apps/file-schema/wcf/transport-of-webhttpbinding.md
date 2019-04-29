---
title: <transport> de <webHttpBinding>
ms.date: 03/30/2017
ms.assetid: f150fb19-7de1-44af-81f4-86cad881cd05
ms.openlocfilehash: 8dcd51cd248dbba3ccf60295cb1712167684328e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788269"
---
# <a name="transport-of-webhttpbinding"></a>\<transport > de \<webHttpBinding >
Définit les paramètres de sécurité au niveau du transport pour un point de terminaison de service configuré pour recevoir des demandes HTTP.  
  
 \<system.ServiceModel>  
\<bindings>  
\<webHttpBinding>  
\<binding>  
\<security>  
\<transport>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<webHttpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"
                 proxyCredentialType="None|Basic|Digest|Ntlm|Windows"
                 realm="string">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</webHttpBinding>
```  
  
## <a name="type"></a>Type  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`clientCredentialType`|Spécifie les informations d'identification utilisées pour authentifier le client auprès du service. Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.|  
|`proxyCredentialType`|Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine. Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.|  
|`realm`|Chaîne indiquant le domaine de l’authentification de base ou Digest. La valeur par défaut est une chaîne vide.<br /><br /> Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification. Il peut également spécifier une collection d’utilisateurs disposant d’un accès. Un utilisateur peut interroger le domaine d'authentification pour vérifier quels noms d'utilisateurs et mots de passe peuvent être utilisés.|  
|`policyEnforcement`|Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.<br /><br /> 1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).<br />2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.<br />3.  Always : la stratégie est toujours appliquée. Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.|  
  
## <a name="clientcredentialtype-attribute"></a>Attribut clientCredentialType  
  
|Value|Description|  
|-----------|-----------------|  
|`None`|La sécurité est désactivée.|  
|`Basic`|Utilise l'authentification de base.|  
|`Certificate`|Utilise des certificats X.509 pour authentifier le client.|  
|`Digest`|Utilise l’authentification Digest.|  
|`Ntlm`|Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.|  
|`Windows`|Utilise l'authentification intégrée Windows.|  
  
## <a name="proxycredentialtype-attribute"></a>Attribut proxyCredentialType  
  
|Value|Description|  
|-----------|-----------------|  
|`None`|La sécurité est désactivée.|  
|`Basic`|Utilise l'authentification de base.|  
|`Digest`|Utilise l’authentification Digest.|  
|`Ntlm`|Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.|  
|`Windows`|Utilise l'authentification intégrée Windows.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-webhttpbinding.md)|Représente les fonctionnalités de sécurité de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) élément.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.Configuration.WebHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.WebHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
- [Modèle de programmation HTTP web WCF](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
