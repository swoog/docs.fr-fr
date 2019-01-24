---
title: '&lt;trustedIssuers&gt;'
ms.date: 03/30/2017
ms.assetid: d818c917-07b4-40db-9801-8676561859fd
author: BrucePerlerMS
ms.openlocfilehash: 1459027ae22344d5b1abc917c490b8e98fa0f2c3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54633997"
---
# <a name="lttrustedissuersgt"></a>&lt;trustedIssuers&gt;
Configure la liste des certificats d’émetteurs approuvés utilisés par le Registre des noms d’émetteurs basé sur la configuration (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration>  
\<issuerNameRegistry>  
\<trustedIssuers>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry>  
          <trustedIssuers>  
            <add thumbprint=xs:string name=xs:string>  
            <clear>  
            <remove thumbprint=xs:string>  
          </trustedIssuers>  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|`<add thumbprint=xs:string name=xs:string>`|Ajoute un certificat à la collection des émetteurs approuvés. Le certificat est spécifié avec la `thumbprint` attribut. Cet attribut est obligatoire et doit contenir le formulaire ASN.1 codé de l’empreinte du certificat. Le `name` attribut est facultatif et peut être utilisé pour spécifier un nom convivial pour le certificat.|  
|`<clear>`|Efface tous les certificats à partir de la collection des émetteurs approuvés.|  
|`<remove thumbprint=xs:string>`|Supprime un certificat à partir de la collection des émetteurs approuvés. Le certificat est spécifié avec la `thumbprint` attribut. Cet attribut est obligatoire.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<issuerNameRegistry>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|Configure le Registre des noms d’émetteur. **Important :**  Le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe pour le `<trustedIssuers>` élément soit valide.|  
  
## <a name="remarks"></a>Notes  
 Windows Identity Foundation (WIF) fournit une implémentation unique de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe dès le départ, le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe. Le Registre des noms configuration émetteur gère une liste d’émetteurs approuvés qui est chargée à partir de la configuration. La liste associe chaque nom de l’émetteur du certificat X.509 qui est nécessaire pour vérifier la signature des jetons produits par l’émetteur. La liste des certificats d’émetteurs approuvés est spécifiée sous la `<trustedIssuers>` élément. Chaque élément dans la liste associe un nom de l’émetteur mnémonique avec le certificat X.509 qui est nécessaire pour vérifier la signature des jetons produits par cet émetteur. Certificats de confiance sont spécifiés à l’aide de l’ASN.1 forme codée de l’empreinte de certificat et sont ajoutés de la collection à l’aide de `<add>` élément. Vous pouvez effacer ou supprimer des émetteurs (certificats) dans la liste à l’aide de la `<clear>` et `<remove>` éléments.  
  
 Le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe pour le `<trustedIssuers>` élément soit valide.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre comment spécifier l’émetteur de la configuration en fonction du Registre des noms.  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB2F32 … B1DC01EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
- <xref:System.IdentityModel.Tokens.IssuerNameRegistry>
