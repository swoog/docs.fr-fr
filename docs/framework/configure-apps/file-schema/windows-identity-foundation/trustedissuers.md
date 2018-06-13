---
title: '&lt;trustedIssuers&gt;'
ms.date: 03/30/2017
ms.assetid: d818c917-07b4-40db-9801-8676561859fd
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: f9daea7d6b78e2f6790050b35dde62db6058c60b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32757468"
---
# <a name="lttrustedissuersgt"></a>&lt;trustedIssuers&gt;
Configure la liste des certificats d’émetteur de confiance utilisé par le Registre de nom de base de configuration de l’émetteur (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).  
  
 \<system.identityModel>  
\<identityConfiguration >  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration >  
\<issuerNameRegistry >  
\<trustedIssuers >  
  
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
 Aucun  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|`<add thumbprint=xs:string name=xs:string>`|Ajoute un certificat à la collection des émetteurs approuvés. Le certificat est spécifié avec la `thumbprint` attribut. Cet attribut est obligatoire et doit contenir le formulaire ASN.1 codé de l’empreinte numérique du certificat. Le `name` attribut est facultatif et peut être utilisé pour spécifier un nom convivial pour le certificat.|  
|`<clear>`|Efface tous les certificats de la collection des émetteurs approuvés.|  
|`<remove thumbprint=xs:string>`|Supprime un certificat à partir de la collection des émetteurs approuvés. Le certificat est spécifié avec la `thumbprint` attribut. Cet attribut est obligatoire.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<issuerNameRegistry >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|Configure le Registre de nom de l’émetteur. **Important :** le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> de classes pour la `<trustedIssuers>` élément soit valide.|  
  
## <a name="remarks"></a>Notes  
 Windows Identity Foundation (WIF) fournit une implémentation unique de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe prêtes à l’emploi, la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe. Le Registre de nom d’émetteur configuration gère une liste d’émetteurs approuvés qui est chargée à partir de la configuration. La liste associe chaque nom de l’émetteur du certificat X.509 qui est nécessaire pour vérifier la signature de jetons généré par l’émetteur. La liste de certificats de confiance de l’émetteur est spécifiée sous la `<trustedIssuers>` élément. Chaque élément dans la liste associe un nom mnémonique de l’émetteur du certificat X.509 qui est nécessaire pour vérifier la signature des jetons générés par cet émetteur. Certificats de confiance sont spécifiés à l’aide de la ASN.1 forme encodée de l’empreinte numérique du certificat et sont ajoutés de la collection à l’aide de `<add>` élément. Vous pouvez effacer ou supprimer des émetteurs (certificats) dans la liste à l’aide de la `<clear>` et `<remove>` éléments.  
  
 Le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> de classes pour la `<trustedIssuers>` élément soit valide.  
  
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
 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>  
 <xref:System.IdentityModel.Tokens.IssuerNameRegistry>
