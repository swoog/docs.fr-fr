---
title: '&lt;issuerNameRegistry&gt;'
ms.date: 03/30/2017
ms.assetid: 58b39d12-c953-40c4-88af-d7eb3343ca28
author: BrucePerlerMS
ms.openlocfilehash: de3ceb5d84d17307c69e9155834a0a584e6920a1
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48245216"
---
# <a name="ltissuernameregistrygt"></a>&lt;issuerNameRegistry&gt;
Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration >  
\<issuerNameRegistry >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry type=xs:string>  
          <optionalCustomConfigurationElements />  
        </issuerNameRegistry>  
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
|type|Un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe. Pour plus d’informations sur la façon de spécifier une personnalisée `type`, consultez [références de Type personnalisé].|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)|Lorsque le `type` attribut spécifie le Registre des noms d’émetteurs basé sur la configuration (le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe), la [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément doit être spécifié. Le [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément peut prendre `<add>`, `<clear>`, ou `<remove>` éléments comme des éléments enfants.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|Fournit une configuration pour une collection de sécurité gestionnaires de jetons.|  
  
## <a name="remarks"></a>Notes  
 Tous les jetons d’émetteur sont validés à l’aide d’un registre des noms d’émetteur. Il s’agit d’un objet qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe. Le Registre des noms d’émetteur est utilisé pour associer un nom mnémonique avec le matériel de chiffrement qui est nécessaire pour vérifier les signatures des jetons produits par l’émetteur correspondant. Le Registre des noms d’émetteur gère une liste d’émetteurs approuvés par l’application de confiance (RP). Le type du Registre de nom de l’émetteur est spécifié à l’aide de la `type` attribut. Le `<issuerNameRegistry>` élément peut avoir un ou plusieurs éléments enfants qui fournissent la configuration pour le type spécifié. Vous fournissez la logique qui traite ces éléments enfants en substituant le <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> (méthode).  
  
 WIF fournit un émetteur unique type de Registre de nom dès le départ, le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe. Cette classe utilise un ensemble de certificats d’émetteurs approuvés qui sont spécifiés dans la configuration. Il requiert un élément de configuration enfant, `<trustedIssuers>`, sous lequel la collection de certificats d’émetteurs approuvés est configurée. Approuvé de certificats sont spécifiés à l’aide de l’ASN.1 forme codée de l’empreinte de certificat et est ajouté ou supprimé de la collection à l’aide de `<add>`, `<clear>`, ou `<remove>` éléments.  
  
 Le `<issuerNameRegistry>` élément est représenté par la <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> classe.  
  
> [!NOTE]
>  En spécifiant le `<issuerNameRegistry>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante. Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre comment spécifier l’émetteur de la configuration en fonction du Registre des noms.  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB … 1EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.IdentityModel.Tokens.IssuerNameRegistry>  
 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
