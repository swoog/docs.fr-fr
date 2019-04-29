---
title: <secureConversationAuthentication> de <serviceCredential>
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: f35392b91d047c46e65ce433ef544b86cf6c88c6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670610"
---
# <a name="secureconversationauthentication-of-servicecredential"></a>\<secureConversationAuthentication > de \<serviceCredential >
Spécifie les paramètres pour un service de conversation sécurisé.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<secureConversationAuthentication>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`securityStateEncoderType`|Chaîne qui spécifie le type de <xref:System.ServiceModel.Security.SecurityStateEncoder> à utiliser.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.|  
  
## <a name="remarks"></a>Notes  
 Utilisez cet élément de configuration pour spécifier la liste des types de revendication connus pour la sérialisation des cookies SCT (Security Context Token), ainsi qu'un encodeur pour encoder et sécuriser les informations de cookies. Pour plus d'informations sur SCT, consultez <xref:System.ServiceModel.Security.SecureConversationServiceCredential>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>
- <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
