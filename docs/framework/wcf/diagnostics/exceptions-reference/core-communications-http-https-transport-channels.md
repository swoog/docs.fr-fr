---
title: 'Communications principales : Canaux de Transport HTTP-HTTPS'
ms.date: 03/30/2017
ms.assetid: 6c0a23c9-a663-461c-bdab-58b4d3e23642
ms.openlocfilehash: 4c4a2537ae615943ffac299a8c8cd00c67094360
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844187"
---
# <a name="core-communications-httphttps-transport-channels"></a>Communications principales : canaux de transport HTTP/HTTPS
Cette rubrique répertorie toutes les exceptions générées par les canaux de Windows Communication Foundation (WCF) Transport HTTP/HTTPS.  
  
## <a name="exception-list"></a>Liste des exceptions  
  
|Code de la ressource|Chaîne de la ressource|  
|-------------------|---------------------|  
|DigestExplicitCredsImpersonationLevel|Le niveau d'emprunt d'identité spécifié a été spécifié. L'authentification Digest HTTP prend en charge le niveau d'emprunt d'identité uniquement lorsque celui-ci est utilisé avec des informations d'identification explicites.|  
|FramingContentTypeMismatch|Le type de contenu spécifié n'est pas pris en charge par le service spécifié. Il se peut que les liaisons client et service ne se correspondent pas.|  
|Hosting_SslSettingsMisconfigured|Les paramètre SSL du service spécifié ne correspondent pas à ceux des services IIS.|  
|HttpAuthSchemeAndClientCert|La configuration de la fabrication d'écouteur HTTPS nécessite le recours à un certificat client ainsi qu'au schéma d'authentification spécifié. Cependant, un seul mode d'authentification client peut être utilisé à la fois.|  
|HttpReceiveFailure|Une erreur s'est produite lors de la réception de la réponse HTTP sur le spécifié. La liaison de point de terminaison de service n'utilise peut-être pas le protocole HTTP. Le serveur a peut-être également arrêté le contexte de requête HTTP à cause de la fermeture du service. Pour plus d'informations, consultez les journaux du serveur.|  
|HttpRegistrationAccessDenied|HTTP ne parvient pas à enregistrer l'adresse URL spécifiée. Le processus n’a pas de droits d’accès à cet espace de noms (consultez [Namespace réservations, les enregistrements et routage](/windows/desktop/http/namespace-reservations-registrations-and-routing) pour plus d’informations).|  
|HttpRegistrationAlreadyExists|HTTP ne parvient pas à enregistrer l'adresse URL spécifiée. Une autre application a déjà enregistré cette adresse URL avec HTTP.SYS.|  
|HttpRegistrationPortInUse|HTTP ne parvient pas à enregistrer l'adresse URL spécifiée car le port TCP indiqué est utilisé par une autre application. .|  
|HttpSendFailure|Une erreur s'est produite lors de la requête HTTP au spécifié. Assurez-vous qu'un éventuel problème de disparité au niveau des liaisons de sécurité n'est pas à l'origine de cette erreur. Assurez-vous également que la configuration du service ne requiert pas l'utilisation du protocole SSL.|  
|MessageXmlProtocolError|Un problème s'est produit au niveau du document XML reçu depuis le réseau. Pour plus d'informations, consultez l'exception interne.|  
|MissingContentType|Le destinataire a retourné une erreur indiquant que le type de contenu ne figurait pas sur la demande au spécifié. Pour plus d'informations, consultez l'exception interne.|  
|ProxyAuthenticationLevelMismatch|Les informations d'identification dans le cadre de l'authentification proxy HTTP exigent un niveau d'authentification (authentification mutuelle) plus rigoureux que le niveau d'authentification requis par l'authentification du serveur cible.|  
|ProxyImpersonationLevelMismatch|Les informations d'identification dans le cadre de l'authentification proxy HTTP définissent une restriction en matière de niveau d'emprunt d'identité plus rigoureuse que la restriction définie par l'authentification du serveur cible.|  
|SecureChannelFailure|Il n'est pas possible de générer un canal sécurisé pour SSL / TLS avec l'autorité spécifiée.|  
|TrustFailure|Impossible d'établir une relation d'approbation pour le canal sécurisé SSL / TLS avec l'autorité spécifiée.|  
|UseDefaultWebProxyCantBeUsedWithExplicitProxyAddress|Vous ne pouvez pas spécifier une adresse de proxy explicite et affecter la valeur true à la propriété UseDefaultWebProxy de votre élément HttpTransportBinding.|
