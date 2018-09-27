---
title: '&lt;claimsAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 6d30a450-6d13-4671-81a8-77e0204500c5
author: BrucePerlerMS
ms.openlocfilehash: 0ec7e44363f87e54eae97b70352f520fe87540be
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47235268"
---
# <a name="ltclaimsauthenticationmanagergt"></a>&lt;claimsAuthenticationManager&gt;
Inscrit un gestionnaire d’authentification des revendications pour les revendications entrantes.  
  
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
 S’il existe aucune `type` attribut, ou si le `type` les références d’attribut le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants ; Toutefois, les classes dérivées de <xref:System.Security.Claims.ClaimsAuthenticationManager> peut définir les éléments de configuration enfants.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres de l’identité de niveau de service.|  
  
## <a name="remarks"></a>Notes  
 Le comportement par défaut fourni par le biais du <xref:System.Security.Claims.ClaimsAuthenticationManager> classe renvoie les revendications entrantes. Si aucun `type` attribut est spécifié ou si le `type` attribut spécifie le <xref:System.Security.Claims.ClaimsAuthenticationManager> (classe), le `<claimsAuthenticationManager>` élément ne prend pas d’éléments enfants. Vous pouvez spécifier le `type` attribut d’inscrire un type dérivé la <xref:System.Security.Claims.ClaimsAuthenticationManager> classe pour implémenter un comportement personnalisé. Les classes dérivées peuvent prendre en charge la configuration via les éléments enfants de la `<claimsAuthenticationManager>` élément en substituant le <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> méthode pour traiter ces éléments. Le schéma défini pour les éléments enfants revient le Concepteur de la classe.  
  
 Le `<claimsAuthenticationManager>` élément définit les <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> propriété.  
  
## <a name="example"></a>Exemple  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="MyIdentity">  
      <claimsAuthenticationManager type="MyNamespace.CustomClaimsAuthenticationManager, MyAssembly"/>          
    </identityConfiguration>  
</microsoft.identityModel>  
```
