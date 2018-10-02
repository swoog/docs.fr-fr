---
title: '&lt;customCookieHandler&gt;'
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 51ca91de5c77727f5f5506118461d19354f12c14
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48029081"
---
# <a name="ltcustomcookiehandlergt"></a>&lt;customCookieHandler&gt;
Définit le type de gestionnaire de cookie personnalisé. Cet élément peut uniquement être présent si la `mode` attribut de la `<cookieHandler>` élément est « Custom ». Le type personnalisé doit être dérivé du <xref:System.IdentityModel.Services.CookieHandler> classe.  
  
 \<system.identityModel.services >  
\<federationConfiguration >  
\<cookieHandler >  
\<customCookieHandler >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Services.CookieHandler> classe. Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<cookieHandler >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|Configure le <xref:System.IdentityModel.Services.CookieHandler> qui le <xref:System.IdentityModel.Services.SessionAuthenticationModule> utilise pour lire et écrire des cookies.|  
  
## <a name="remarks"></a>Notes  
 Lorsque vous spécifiez un gestionnaire de cookie personnalisé en définissant le `mode` attribut de la `<cookieHandler>` élément « Personnalisé », vous devez spécifier le type du Gestionnaire de cookie personnalisé en incluant un `<customCookieHandler>` élément enfant qui fait référence au type de gestionnaire de cookie. Cet élément ne peut pas être spécifié lorsque le `mode` attribut a la valeur « Chunked » ou « Default ». Gestionnaires de cookie personnalisé doivent dériver de la <xref:System.IdentityModel.Services.CookieHandler> classe.  
  
 Le `<customCookieHandler>` élément est représenté par la <xref:System.IdentityModel.Configuration.CustomTypeElement> classe.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant configure le module SAM pour utiliser un gestionnaire de cookie personnalisé de type `MyNamespace.MyCustomCookieHandler`.  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IdentityModel.Services.CookieHandler>
