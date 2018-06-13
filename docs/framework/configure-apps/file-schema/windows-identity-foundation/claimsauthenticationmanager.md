---
title: '&lt;claimsAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 6d30a450-6d13-4671-81a8-77e0204500c5
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 4d4a91e0ed1f437089e26e5902515f73a15d94a8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32755238"
---
# <a name="ltclaimsauthenticationmanagergt"></a>&lt;claimsAuthenticationManager&gt;
Inscrit un gestionnaire de l’authentification par revendications pour les revendications entrantes.  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<claimsAuthenticationManager >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthenticationManager type=xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthenticationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Spécifie un type personnalisé qui dérive de la <xref:System.Security.Claims.ClaimsAuthenticationManager> classe. Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé].|  
  
### <a name="child-elements"></a>Éléments enfants  
 S’il existe aucune `type` attribut, ou si le `type` les références d’attribut le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants ; Toutefois, les classes dérivées de <xref:System.Security.Claims.ClaimsAuthenticationManager> peut définir des éléments de configuration enfants.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres d’identité au niveau du service.|  
  
## <a name="remarks"></a>Notes  
 Le comportement par défaut fourni par le biais du <xref:System.Security.Claims.ClaimsAuthenticationManager> classe renvoie les revendications entrantes. Si aucun `type` attribut est spécifié ou si le `type` attribut spécifie la <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants. Vous pouvez spécifier le `type` attribut pour enregistrer un type dérivé de la <xref:System.Security.Claims.ClaimsAuthenticationManager> classe pour implémenter un comportement personnalisé. Les classes dérivées peuvent prendre en charge la configuration par le biais des éléments enfants de la `<claimsAuthenticationManager>` élément en remplaçant le <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> méthode pour gérer ces éléments. Le schéma défini pour les éléments enfants est sur le Concepteur de la classe.  
  
 Le `<claimsAuthenticationManager>` élément définit les <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> propriété.  
  
## <a name="example"></a>Exemple  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="MyIdentity">  
      <claimsAuthenticationManager type="MyNamespace.CustomClaimsAuthenticationManager, MyAssembly"/>          
    </identityConfiguration>  
</microsoft.identityModel>  
```
