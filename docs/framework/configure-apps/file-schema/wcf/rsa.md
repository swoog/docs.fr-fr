---
title: '&lt;RSA&gt;'
ms.date: 03/30/2017
ms.assetid: ae1f2267-e40d-42ff-8abf-06ab7067bdb9
ms.openlocfilehash: 8005fd67b92cb14d82b525e7c990f9d58aef7b58
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145339"
---
# <a name="ltrsagt"></a>&lt;RSA&gt;
Un client WCF sécurisé qui se connecte à un point de terminaison avec cette identité vérifie que les revendications présentées par le serveur contiennent une revendication intégrant la clé publique RSA utilisée pour construire cette identité.  
  
 \<identité >  
\<RSA >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<rsa value="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|par défaut|Chaîne facultative. Valeur de clé publique RSA à comparer sur le client.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identité >](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|Spécifie l'identité du service à authentifier par le client.|  
  
## <a name="remarks"></a>Notes  
 Un contrôle RSA vous permet de limiter l'authentification à un seul certificat basé sur sa clé RSA ou de générer votre propre valeur de clé RSA. Cette opération active une authentification plus stricte d'une clé RSA spécifique aux dépens du service, qui n'utilise plus les clients existants lorsque la valeur de clé RSA est modifiée.  
  
 Pour plus d’informations sur l’utilisation d’identité pour valider un service à un client, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
## <a name="example"></a>Exemple  
 Le code de configuration suivant spécifie la valeur de clé publique d'un certificat X.509 utilisé pour authentifier un serveur.  
  
```xml  
<identity>
  <rsa value="0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000" />
</identity>
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.RsaEndpointIdentity>  
 [Identité du service et authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [\<identité >](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
