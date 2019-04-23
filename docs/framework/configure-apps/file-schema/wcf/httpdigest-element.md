---
title: Élément <httpDigest>
ms.date: 03/30/2017
ms.assetid: 3da4f276-dfd9-4247-8c07-01d83618727c
ms.openlocfilehash: 914711e4d6c3dbb1ccc741af1b3abd6b8de716a8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165319"
---
# <a name="httpdigest-element"></a>\<httpDigest > élément
Spécifie une information d'identification de type condensé utilisée lors de l'authentification du client à un service.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<clientCredentials>  
\<httpDigest>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<digest impersonationLevel="Identification/Impersonation/Delegation/Anonymous/None" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`impersonationLevel`|Définit la préférence d'emprunt d'identité que le client communique au serveur. Le mode d'emprunt d'identité que le client sélectionne n'est pas appliqué sur le serveur. Les valeurs valides sont les suivantes :<br /><br /> -   Identification: Le serveur peut obtenir l’identité et les privilèges du client, mais ne peut pas représenter le client.<br />-L’emprunt d’identité : Le serveur peut emprunter l’identité de contexte de sécurité du client sur le système local.<br />-Délégation : Le serveur peut emprunter l’identité de contexte de sécurité du client sur des systèmes distants.<br />-Anonyme : Le serveur ne peut pas emprunter l’identité ou identifier le client.<br />-None : Un niveau d’emprunt d’identité n’est pas affecté.<br /><br /> La valeur par défaut est Identification. Cet attribut est de type <xref:System.Security.Principal.TokenImpersonationLevel>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|Spécifie les informations d'identification utilisées pour authentifier un client auprès d'un service.|  
  
## <a name="remarks"></a>Notes  
 Un condensat est un hachage déterminé à l’aide d’un algorithme et d’un jeu d’entrées. L'authentificateur et l'authentifié acceptent un algorithme et échangent les données utilisées comme entrées. Le client peut calculer le hachage et l'envoyer au service. Le service calcule également le hachage et compare les valeurs. Une correspondance valide le client.  
  
 Cette fonction doit être activée avec Active Directory sur Windows et les services IIS (Internet Information Services). Pour plus d’informations, consultez [l’authentification Digest dans IIS 6.0](https://go.microsoft.com/fwlink/?LinkId=88443).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.HttpDigest%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.HttpDigest%2A>
- <xref:System.ServiceModel.Configuration.HttpDigestClientElement>
- <xref:System.ServiceModel.Security.HttpDigestClientCredential>
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Sécurisation des clients](../../../../../docs/framework/wcf/securing-clients.md)
- [Utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
