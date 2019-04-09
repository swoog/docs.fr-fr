---
title: <wsFederation>
ms.date: 03/30/2017
ms.assetid: c537f770-68bd-4f82-96ad-6424ad91369f
author: BrucePerlerMS
ms.openlocfilehash: 276f552767897729bf58c6a803669f39c96f09e3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135133"
---
# <a name="wsfederation"></a>\<wsFederation>
Fournit une configuration pour le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM).  
  
\<system.identityModel.services>  
\<federationConfiguration>  
\<wsFederation>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml
<system.identityModel.services>  
  <federationConfiguration>  
    <wsFederation authenticationType=xs:string (URI)  
                  freshness=xs:decimal  
                  homerealm=xs:string (URI)  
                  issuer=xs:string (URI)  
                  persistentCookiesOnPassiveRedirects=xs:boolean  
                  passiveRedirectEnabled=xs:boolean  
                  policy=xs:string (URI)  
                  realm=xs:string (URI)  
                  reply=xs:string (URI)  
                  request=xs:string (URI)  
                  requestPtr=xs:string (URI)  
                  requireHttps=xs:boolean  
                  resource=xs:string (URI)  
                  signInQueryString=xs:string  
                  signOutQueryString=xs:string  
                  signOutReply=xs:string (URL)  
    </wsFederation>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|authenticationType|URI qui spécifie le type d’authentification. Définit le paramètre wauth de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wauth n’est pas inclus dans la demande.|  
|actualisation|L’âge maximal souhaité des demandes d’authentification, en quelques minutes. Définit le paramètre wfresh de demande de connexion WS-Federation. Facultatif. La valeur par défaut est zéro. Optionnel. **Avertissement :**  Dans la prochaine version de .NET Framework 4.5, le `freshness` attribut sera de type `xs:string` et sa valeur par défaut sera `null`.|  
|homeRealm|Le domaine d’accueil du fournisseur d’identité (IdP) à utiliser pour l’authentification. Définit le paramètre whr de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre whr n’est pas inclus dans la demande.|  
|issuer|L’URI de l’émetteur de jeton attendu. Définit les demandes de connexion URL WS-Federation base et les demandes de déconnexion requis.|  
|persistentCookiesOnPassiveRedirects|Spécifie si les cookies persistants sont émis sur l’authentification. Optionnel. La valeur par défaut est « false », les cookies ne sont pas émis.|  
|passiveRedirectEnabled|Spécifie si le WSFAM est activé pour rediriger automatiquement les demandes non autorisées vers un STS. Optionnel. La valeur par défaut est « true », les demandes non autorisées sont automatiquement redirigés.|  
|d’exception non gérée|Une URL qui spécifie l’emplacement de la stratégie appropriée à utiliser sur les demandes de connexion. La valeur par défaut est une chaîne vide. Définit le paramètre wp de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wp n’est pas inclus dans la demande.|  
|realm|L’URI du domaine demandeur. (Un URI qui identifie la partie de confiance (RP) pour le service de jeton de sécurité (STS).) Définit le paramètre de demande de wtrealm WS-Federation sign-in de requête. Obligatoire.|  
|Réponse|Une URL qui identifie l’adresse à laquelle l’application de confiance (RP) aimerait recevoir des réponses à partir du Service STS (Security Token). Définit le paramètre wreply de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wreply n’est pas inclus dans la demande.|  
|demande|La demande d’émission de jeton. Définit le paramètre wreq de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wreq n’est pas inclus dans la demande. Ne pas inclure le wreq ou le paramètre wreqptr dans la demande implique que le service STS sache quel type de jeton à émettre.|  
|requestPtr|Une URL qui spécifie l’emplacement de la demande d’émission de jeton. Définit le paramètre wreqptr de demande. Facultatif. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wreqptr n’est pas inclus dans la demande. Ne pas inclure le wreq ou le paramètre wreqptr dans la demande implique que le service STS sache quel type de jeton à émettre.|  
|requireHttps|Spécifie si la communication avec le service de jeton de sécurité (STS) doit utiliser le protocole HTTPS. Optionnel. La valeur par défaut est « true », vous devez utiliser HTTPS.|  
|ressource|Un URI qui identifie la ressource sollicitée, la partie de confiance (RP), à la pour le service de jeton de sécurité (STS). Facultatif. Définit le paramètre wres de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, qui spécifie que le paramètre wres n’est pas inclus dans la demande. **Remarque :** wres est un paramètre hérité. Spécifiez le `realm` attribut à utiliser le paramètre wtrealm à la place.|  
|signInQueryString|Fournit un point d’extensibilité pour spécifier les paramètres de requête définis par l’application dans l’URL de demande de connexion WS-Federation. Optionnel. La valeur par défaut est une chaîne vide, ce qui indique que des paramètres supplémentaires doivent être inclus dans la demande. Les paramètres sont spécifiés comme un fragment de chaîne de requête à l’aide de la forme suivante : `"param1=value1&param2=value2&param3=value3"` et ainsi de suite. **Remarque :**  Dans un fichier de configuration le » & « caractère de la chaîne de requête doit être spécifié à l’aide de sa référence d’entité, `&`.|  
|signOutQueryString|Fournit un point d’extensibilité pour spécifier les paramètres de requête définis par l’application dans l’URL de demande de connexion WS-Federation. Facultatif. La valeur par défaut est une chaîne vide, ce qui indique que des paramètres supplémentaires doivent être inclus dans la demande. Les paramètres sont spécifiés comme un fragment de chaîne de requête à l’aide de la forme suivante : `"param1=value1&param2=value2&param3=value3"` et ainsi de suite. **Remarque :**  Dans un fichier de configuration le » & « caractère de la chaîne de requête doit être spécifié à l’aide de sa référence d’entité, `&`.|  
|signOutReply|Spécifie l’URL à laquelle le client doit être redirigé par le service de jeton de sécurité (STS) pendant la déconnexion passive via le protocole WS-Federation. Définit le paramètre wreply sur une demande de déconnexion WS-Federation. Facultatif. La valeur par défaut est une chaîne vide, ce qui indique que des paramètres supplémentaires doivent être inclus dans la demande.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<federationConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|Contient les paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).|  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser le `<wsFederation>` élément pour configurer les paramètres par défaut WS-Federation et le comportement par défaut pour le WSFAM. Valeurs des paramètres WS-Federation définis sous la `<wsFederation>` élément défini les propriétés équivalentes exposées par le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> classe. Ces propriétés restent les mêmes pour chaque demande émise par le WSFAM. Vous pouvez modifier les paramètres WS-Federation dynamiquement pendant la demande de traitement en ajoutant des gestionnaires d’événements pour les événements exposés par le WSFAM ; par exemple, le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule.RedirectingToIdentityProvider> événement. Pour plus d’informations, consultez la documentation pour le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> classe.  
  
 Le `<wsFederation>` élément est représenté par la <xref:System.IdentityModel.Services.Configuration.WSFederationElement> classe. L’objet de configuration lui-même est représenté par la <xref:System.IdentityModel.Services.Configuration.WsFederationConfiguration> classe. Un seul <xref:System.IdentityModel.Services.Configuration.WsFederationConfiguration> instance est définie sur le <xref:System.IdentityModel.Services.Configuration.FederationConfiguration> objet qui est accessible via la <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType> propriété et fournit une configuration pour le WSFAM.  
  
## <a name="example"></a>Exemple  
 Le code XML suivant montre un `<wsFederation>` élément qui spécifie les paramètres pour le WSFAM.  
  
> [!WARNING]
>  Dans cet exemple, le WSFAM n’est pas nécessaire d’utiliser HTTPS. Il s’agit, car le `requireHttps` d’attribut sur le `<wsFederation>` élément a la valeur `false`. Ce paramètre n’est pas recommandé pour la plupart des environnements de production comme il peut présenter un risque de sécurité.  
  
```xml
<wsFederation passiveRedirectEnabled="true"   
              issuer="http://localhost:15839/wsFederationSTS/Issue"   
              realm="http://localhost:50969/"   
              reply="http://localhost:50969/"   
              requireHttps="false"   
              signOutReply="http://localhost:50969/SignedOutPage.html"   
              signOutQueryString="Param1=value2&Param2=value2"   
              persistentCookiesOnPassiveRedirects="true" />
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IdentityModel.Services.WSFederationAuthenticationModule>
- <xref:System.IdentityModel.Services.FederatedAuthentication.FederationConfiguration%2A?displayProperty=nameWithType>
