---
title: <issuerTokenResolver>
ms.date: 03/30/2017
ms.assetid: f74392f6-3f5b-4880-bd8a-3a9130d31e65
author: BrucePerlerMS
ms.openlocfilehash: a37935fa9302493c0ecaab0f56e1414d44637af6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269222"
---
# <a name="issuertokenresolver"></a>\<issuerTokenResolver>
Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons. Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration>  
\<issuerTokenResolver>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerTokenResolver type=xs:string>  
        </issuerTokenResolver>  
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
|type|Spécifie le type du programme de résolution de jeton de l’émetteur. Doit être le <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe ou un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe. Obligatoire.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|Fournit une configuration pour une collection de sécurité gestionnaires de jetons.|  
  
## <a name="remarks"></a>Notes  
 Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant. Il est utilisé pour récupérer le matériel de chiffrement qui est utilisé pour la vérification de la signature. Vous devez spécifier le `type` attribut. Le type spécifié peut être soit <xref:System.IdentityModel.Tokens.IssuerTokenResolver> ou un type personnalisé qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe.  
  
 Certains gestionnaires de jetons permettent de spécifier les paramètres de résolution de jeton de l’émetteur dans la configuration. Les paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées sur la collection de gestionnaires de jetons de sécurité.  
  
> [!NOTE]
>  En spécifiant le `<issuerTokenResolver>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante. Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre la configuration pour un résolveur de jeton de l’émetteur est basé sur une classe personnalisée qui dérive de <xref:System.IdentityModel.Tokens.IssuerTokenResolver>. Le programme de résolution de jeton gère un dictionnaire de paires clé-public qui est initialisé à partir d’un élément de configuration personnalisé (`<AddAudienceKeyPair>`) définie pour la classe. La classe substitue la <xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A> méthode pour traiter cet élément. Le remplacement est illustré dans l’exemple suivant ; Toutefois, les méthodes qu’elle appelle ne sont pas affichés par souci de concision. Pour obtenir un exemple complet, consultez la `CustomToken` exemple.  
  
```xml  
<issuerTokenResolver type="SimpleWebToken.CustomIssuerTokenResolver, SimpleWebToken">  
  <AddAudienceKeyPair  symmetricKey="wAVkldQiFypTQ+kdNdGWCYCHRcee8XmXxOvgmak8vSY=" audience="http://localhost:19851/" />  
</issuerTokenResolver>  
```  
  
## <a name="example"></a>Exemple  
  
```  
public override void LoadCustomConfiguration(System.Xml.XmlNodeList nodelist)  
{  
    foreach (XmlNode node in nodelist)  
    {  
        XmlDictionaryReader rdr = XmlDictionaryReader.CreateDictionaryReader(new XmlTextReader(new StringReader(node.OuterXml)));  
        rdr.MoveToContent();  
  
        string symmetricKey = rdr.GetAttribute("symmetricKey");  
        string audience = rdr.GetAttribute("audience");  
  
        this.AddAudienceKeyPair(audience, symmetricKey);  
    }  
}  
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.IdentityModel.Tokens.IssuerTokenResolver>
