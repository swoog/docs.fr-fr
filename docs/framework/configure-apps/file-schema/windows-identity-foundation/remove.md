---
title: <remove>
ms.date: 03/30/2017
ms.assetid: 4058e2f1-7db4-4d1a-84dd-1b52836f2ae6
author: BrucePerlerMS
ms.openlocfilehash: a54957458311e2d5941d1aa1c2486a2f66994d9b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288130"
---
# <a name="remove"></a>\<remove>
Supprime le Gestionnaire de jetons de sécurité spécifié de la collection de gestionnaires de jetons.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<securityTokenHandlers>  
\<remove>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <remove type=xs:string >  
      </remove>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Le nom de type CLR de gestionnaire de jetons à supprimer. Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](https://msdn.microsoft.com/library/7286d2e3-c63d-49fd-abdc-ce2705f22c24). Obligatoire.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<securityTokenHandlers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.|  
  
## <a name="example"></a>Exemple  
 Le code XML suivant illustre l’utilisation de la `<add>` et `<remove>` éléments pour remplacer le Gestionnaire de jetons de session par défaut par un gestionnaire de jetons de session personnalisée. Le code XML provient de la `ClaimsAwareWebFarm` exemple.  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
