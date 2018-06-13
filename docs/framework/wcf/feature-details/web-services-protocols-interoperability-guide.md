---
title: Guide de l'interopérabilité des protocoles de services Web
ms.date: 03/30/2017
ms.assetid: f2981678-ebdb-433d-899b-467f7df95fb2
ms.openlocfilehash: 1ee8b485d8a46d2599958db2c71f4a6e84875169
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33506605"
---
# <a name="web-services-protocols-interoperability-guide"></a>Guide de l'interopérabilité des protocoles de services Web
Windows Communication Foundation (WCF) implémente plusieurs protocoles de services Web. Un grand nombre de ces protocoles incluent plusieurs options et points d'extensibilité qui sont laissés à la discrétion de l'implémenteur. Cette rubrique fournit une liste de protocoles de services Web que WCF implémente. Des détails d'implémentation pour chaque protocole pris en charge sont fournis dans les autres rubriques de cette section.  
  
## <a name="web-services-protocols-implemented-by-wcf"></a>Protocoles des services Web implémentés par WCF  
 WCF prend en charge pour les protocoles d’infrastructure Web services (WS) via les canaux et les protocoles d’application via la fonctionnalité de contrats de services Web. L'interopérabilité pour les protocoles d'application s'effectue à l'aide des langages XSD (XML Schema Description) 1.0 et WSDL (Web Services Description Language ) 1.1.  
  
 L'interopérabilité des protocoles d'infrastructure est fournie par la famille des spécifications WS-*. Canaux WCF prennent en charge un nombre de WS -\* protocoles d’infrastructure. Canaux WCF sont configurés à l’aide des éléments de liaison. Les tableaux suivants contiennent la liste complète des WS -\* protocoles d’infrastructure implémentées par les différents éléments de liaison WCF.  
  
 <xref:System.ServiceModel.Channels.HttpTransportBindingElement> prend en charge les spécifications présentées dans le tableau suivant :  
  
|Spécification/document|Link|  
|-----------------------------|----------|  
|HTTP 1.1|[RFC 2616](http://go.microsoft.com/fwlink/?LinkId=90372)|  
|Liaison HTTP SOAP 1.1|[Simple Object Access Protocol (SOAP) 1.1](http://go.microsoft.com/fwlink/?LinkId=90520), Section 7|  
|Liaison HTTP SOAP 1,2|[La Version de SOAP 1.2, partie 2 : Compléments ((deuxième édition)](http://go.microsoft.com/fwlink/?LinkId=95329), Section 7|  
  
 <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement> et <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> prennent en charge les spécifications présentées dans le tableau suivant :  
  
|Spécification/Document|Link|  
|-----------------------------|----------|  
|XML|[Extensible Markup Language (XML) 1.0 ((quatrième édition)](http://go.microsoft.com/fwlink/?LinkId=15139)|  
|SOAP 1,1|[Simple Object Access Protocol (SOAP) 1.1](http://go.microsoft.com/fwlink/?LinkId=96687)|  
|SOAP 1.2 Core|[SOAP Version 1.2, partie 1 : Infrastructure de messagerie ((deuxième édition)](http://go.microsoft.com/fwlink/?LinkId=94664)|  
|WS-Addressing 2004/08|[Adressage (WS-Addressing) de Services Web](http://go.microsoft.com/fwlink/?LinkId=81239)|  
|W3C Web Services Addressing 1.0 – Éléments principaux|[Web Services Addressing 1.0 - éléments principaux](http://go.microsoft.com/fwlink/?LinkId=96688)|  
|W3C Web Services Addressing 1.0 – Liaison SOAP|[Web Services Addressing 1.0 - liaison SOAP](http://go.microsoft.com/fwlink/?LinkId=96689)|  
|W3C Web Services Addressing 1.0 – Liaison WSDL*|[Web Services Addressing 1.0 - liaison WSDL](http://go.microsoft.com/fwlink/?LinkId=96690)|  
|W3C Web Services Addressing 1.0 - Métadonnées|[Web Services Addressing 1.0 - métadonnées](http://www.w3.org/TR/ws-addr-metadata/)|  
|Liaison WSDL SOAP 1.1|[Web Services Description Language (WSDL) 1.1](http://go.microsoft.com/fwlink/?LinkId=96160)|  
|Liaison WSDL SOAP 1.2|[WSDL Extension de liaison 1.1 pour SOAP 1.2](http://go.microsoft.com/fwlink/?LinkId=96691)|  
  
 <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement> prend en charge les spécifications présentées dans le tableau suivant :  
  
|Spécification/document|Link|  
|-----------------------------|----------|  
|XOP|[XML binaire optimisé empaquetage](http://go.microsoft.com/fwlink/?LinkId=96714)|  
|Liaison MTOM + SOAP1.2|[SOAP Message Transmission Optimization Mechanism](http://go.microsoft.com/fwlink/?LinkId=96713)|  
|Liaison MTOM SOAP 1.1|[Liaison SOAP 1.1 pour MTOM 1.0](http://go.microsoft.com/fwlink/?LinkId=96712)|  
|MTOM WS-PolicyAssertions|Résultats à publier.|  
  
 <xref:System.ServiceModel.Channels.SecurityBindingElement> prend en charge les spécifications présentées dans le tableau suivant :  
  
|Spécification/document|Link|  
|-----------------------------|----------|  
|WSS : SOAP Message Security 1,0|[Web Services Security : SOAP Message Security 1.0](http://go.microsoft.com/fwlink/?LinkId=94684)|  
|WSS : Username Token Profile 1.0|[Web Services Security UsernameToken Profile 1.0](http://go.microsoft.com/fwlink/?LinkId=95334)<br /><br /> nécessitent Password/@Type= PasswordText (par défaut)|  
|WSS : X.509 Token Profile 1.0|[Web Services Security X.509 Certificate Token Profile](http://go.microsoft.com/fwlink/?LinkId=95335)|  
|WSS: SAML 1.1 Token Profile 1,0|[Web Services Security : Profil du jeton SAML](http://go.microsoft.com/fwlink/?LinkId=96693)|  
|WSS : SOAP Message Security 1.1|[Web Services Security : SOAP Message Security 1.1](http://go.microsoft.com/fwlink/?LinkId=91240)|  
|WSS Username Token Profile 1.1|[Web Services Security UsernameToken Profile 1.1](http://go.microsoft.com/fwlink/?LinkId=95331)<br /><br /> n'implémentez pas la dérivation de clés basée sur mot de passe ;<br /><br /> nécessitent Password/@Type= PasswordText (par défaut)|  
|WSS : X509 Token Profile 1.1|[Web Services Security X.509 Certificate Token Profile 1.1](http://go.microsoft.com/fwlink/?LinkId=95332)|  
|WSS: Kerberos Token Profile 1.1|[Web Services Security Kerberos Token Profile 1.1](http://go.microsoft.com/fwlink/?LinkId=95333)|  
|WSS: SAML 1.1 Token Profile 1.1|[Web Services Security SAML Token Profile 1.1](http://go.microsoft.com/fwlink/?LinkId=96694)|  
|WS-Secure Conversation|[Langue de Conversation sécurisée de Services Web](http://go.microsoft.com/fwlink/?LinkId=95317)|  
|WS-Trust 1.4 (page pouvant être en anglais)|[Services Web confiance Language](http://go.microsoft.com/fwlink/?LinkId=169514)|  
|WS-SecurityPolicy 2005/07|[Langue de Conversation sécurisée de Services Web](http://go.microsoft.com/fwlink/?LinkId=95317)<br /><br /> Selon les corrections des errata soumis au comité technique OASIS WS-SX.<br /><br /> [message de ws-sx.](http://go.microsoft.com/fwlink/?LinkId=96700)|  
|WS-ReliableMessaging 1.1|[Protocole de messagerie fiable version 1.1](../../../../docs/framework/wcf/feature-details/reliable-messaging-protocol-version-1-1.md)|  
  
 <xref:System.ServiceModel.Channels.TransactionFlowBindingElement> prend en charge les spécifications présentées dans le tableau suivant :  
  
|Spécification/Document|Link|  
|-----------------------------|----------|  
|WS-Coordination|[Coordination de Services Web](http://go.microsoft.com/fwlink/?LinkId=95324)|  
|WS-AtomicTransaction|[Transaction atomique des Services Web](http://go.microsoft.com/fwlink/?LinkId=95323)|  
  
 Le <xref:System.ServiceModel.Description.MetadataExporter>, <xref:System.ServiceModel.Description.MetadataImporter>, <!--zz <xref:System.ServiceModel.Description.WSDLExporter>, <xref:System.ServiceModel.Description.WSDLImporter>, --> `System.ServiceModel.Description.MetadataImporter`, `System.ServiceModel.Description.WSDLImporter`, et <xref:System.ServiceModel.Description.MetadataResolver> classes prennent en charge les spécifications de métadonnées suivantes :  
  
-   [XML Schema Part 1 : Structures Second Edition](http://go.microsoft.com/fwlink/?LinkId=3536)  
  
-   [XML Schema Part 2 : Types de données deuxième édition](http://go.microsoft.com/fwlink/?LinkId=40138)  
  
-   [WSDL 1.1](http://go.microsoft.com/fwlink/?LinkId=96160)  
  
-   [WS-Policy 1.2](http://go.microsoft.com/fwlink/?LinkId=96705)  
  
-   [WS-Policy 1.5](http://go.microsoft.com/fwlink/?LinkId=96706)  
  
-   [WS-PolicyAttachment 1.2](http://go.microsoft.com/fwlink/?LinkId=96707)  
  
-   [WS-MetadataExchange 1.1](http://go.microsoft.com/fwlink/?LinkId=94868)  
  
-   [WS-Transfer Get pour la récupération de métadonnées](http://go.microsoft.com/fwlink/?LinkId=96708)  
  
 En outre, les profils d’interopérabilité suivants sont implémentés dans WCF :  
  
-   [Basic Profile 1.1](http://go.microsoft.com/fwlink/?LinkId=69313)  
  
-   [Simple SOAP Binding 1.0](http://go.microsoft.com/fwlink/?LinkId=96710)  
  
-   [Basic Security Profile 1.0 travail brouillon](http://go.microsoft.com/fwlink/?LinkId=96711)  
  
## <a name="see-also"></a>Voir aussi  
 [Protocoles de services web pris en charge par des liaisons d’interopérabilité fournies par le système](../../../../docs/framework/wcf/feature-details/web-services-protocols-supported-by-system-provided-interoperability-bindings.md)  
 [Protocoles de messagerie](../../../../docs/framework/wcf/feature-details/messaging-protocols.md)  
 [Informations de référence sur les schémas de contrats de données](../../../../docs/framework/wcf/feature-details/data-contract-schema-reference.md)  
 [WSDL et stratégie](../../../../docs/framework/wcf/feature-details/wsdl-and-policy.md)  
 [Protocoles de sécurité](../../../../docs/framework/wcf/feature-details/security-protocols.md)  
 [Protocole de messagerie fiable version 1.0](../../../../docs/framework/wcf/feature-details/reliable-messaging-protocol-version-1-0.md)  
 [Protocole de messagerie fiable version 1.1](../../../../docs/framework/wcf/feature-details/reliable-messaging-protocol-version-1-1.md)  
 [Protocoles de transaction](../../../../docs/framework/wcf/feature-details/transaction-protocols.md)  
 [Protocole d’échange de contexte](../../../../docs/framework/wcf/feature-details/context-exchange-protocol.md)
