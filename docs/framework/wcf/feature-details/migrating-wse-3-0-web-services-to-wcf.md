---
title: Migration des services Web WSE 3.0 vers WCF
ms.date: 03/30/2017
ms.assetid: 7bc5fff7-a2b2-4dbc-86cc-ecf73653dcdc
ms.openlocfilehash: 21e36be178bb0dd0c52213d8c4c1387a564a0e5a
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45649417"
---
# <a name="migrating-wse-30-web-services-to-wcf"></a>Migration des services Web WSE 3.0 vers WCF
Les avantages de la migration des services Web WSE 3.0 pour Windows Communication Foundation (WCF) incluent l’amélioration des performances et la prise en charge de transports supplémentaires, renforcer la sécurité des scénarios et WS-* spécifications. Un service Web qui est migré à partir de WSE 3.0 vers WCF peut être confrontés à une amélioration des performances de 200 % et 400 %. Pour plus d’informations sur les transports pris en charge par WCF, consultez [choix d’un Transport](../../../../docs/framework/wcf/feature-details/choosing-a-transport.md). Pour obtenir la liste des scénarios pris en charge par WCF, consultez [scénarios de sécurité courants](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md). Pour obtenir la liste des spécifications qui sont pris en charge par WCF, consultez [Guide de l’interopérabilité de protocoles de Services Web](../../../../docs/framework/wcf/feature-details/web-services-protocols-interoperability-guide.md).  
  
 Les sections suivantes fournissent des conseils sur la façon de migrer une fonctionnalité spécifique d’un service Web WSE 3.0 vers WCF.  
  
## <a name="general"></a>Général  
 Les applications WSE 3.0 et WCF incluent l’interopérabilité au niveau du câble et un ensemble commun de terminologie. Les applications WSE 3.0 et WCF sont au niveau du câble interopérable basé sur l’ensemble de WS-* spécifications deux prennent en charge. Quand une application WSE 3.0 ou WCF est développée il est un ensemble commun de terminologie, tels que les noms des assertions de sécurité clé en main dans WSE et les modes d’authentification.  
  
 Bien qu’il existe de nombreux aspects semblables entre WCF et ASP.NET ou WSE 3.0, modèles de programmation, ils sont différents. Pour plus d’informations sur le modèle de programmation WCF, consultez [cycle de vie de programmation base](../../../../docs/framework/wcf/basic-programming-lifecycle.md).  
  
> [!NOTE]
>  Pour migrer un service Web WSE vers WCF le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil peut être utilisé pour générer un client. Ce client contient des interfaces et des classes qui peuvent être utilisées également comme point de départ pour un service WCF. Les interfaces générées ont l'attribut <xref:System.ServiceModel.OperationContractAttribute> appliqué aux membres du contrat avec la propriété <xref:System.ServiceModel.OperationContractAttribute.ReplyAction%2A> définie à `*`. Lorsqu’un client WSE appelle un service Web avec ce paramètre, l’exception suivante est levée : **Web.Services3.ResponseProcessingException : WSE910 : une erreur s’est produite lors du traitement d’un message de réponse, et vous pouvez trouver l’erreur dans l’exception interne exception**. À des fins d'atténuation, affectez à la propriété <xref:System.ServiceModel.OperationContractAttribute.ReplyAction%2A> de l'attribut <xref:System.ServiceModel.OperationContractAttribute> une valeur non `null`, telle que `http://Microsoft.WCF.Documentation/ResponseToOCAMethod`.  
  
## <a name="security"></a>Sécurité  
  
### <a name="wse-30-web-services-that-are-secured-using-a-policy-file"></a>Services Web WSE 3.0 sécurisés à l'aide d'un fichier de stratégie  
 Les services WCF peuvent utiliser un fichier de configuration pour sécuriser un service et ce mécanisme s’apparente à un fichier de stratégie WSE 3.0. Dans WSE 3.0, lorsque vous sécurisez un service Web à l'aide d'un fichier de stratégie, vous utilisez une assertion de sécurité clé en main ou une assertion de stratégie personnalisée. Les assertions de sécurité clé en main correspondent étroitement au mode d’authentification d’un élément de liaison de sécurité WCF. Non seulement les modes d’authentification WCF et les assertions de sécurité clé en main de WSE 3.0 portent le même ou de la même façon, qu’elles sécurisent les messages en utilisant les mêmes types d’informations d’identification. Par exemple, le `usernameForCertificate` assertion de sécurité clé en main dans WSE 3.0 mappe à la `UsernameForCertificate` mode d’authentification dans WCF. Les exemples de code suivants montrent comment une stratégie minimale qui utilise le `usernameForCertificate` assertion de sécurité clé en main dans WSE 3.0 mappe à un `UsernameForCertificate` mode d’authentification dans WCF dans une liaison personnalisée.  
  
 **WSE 3.0**  
  
```xml  
<policies>  
  <policy name="MyPolicy">  
    <usernameForCertificate messageProtectionOrder="SignBeforeEncrypt"  
                            requireDeriveKeys="true"/>  
  </policy>  
</policies>  
```  
  
 **WCF**  
  
```xml  
<customBinding>  
  <binding name="MyBinding">  
    <security authenticationMode="UserNameForCertificate"   
              messageProtectionOrder="SignBeforeEncrypt"  
              requireDerivedKeys="true"/>  
  </binding>  
</customBinding>  
```  
  
 Pour migrer les paramètres de sécurité d’un service Web WSE 3.0 qui sont spécifiés dans un fichier de stratégie à WCF, une liaison personnalisée doit être créée dans un fichier de configuration et l’assertion de sécurité clé en main doit être définie sur son mode d’authentification équivalent. En outre, la liaison personnalisée doit être configurée de façon à utiliser la spécification WS-Addressing d’août 2004 lorsque des clients WSE 3.0 communiquent avec le service. Lorsque le service WCF migré ne nécessite pas de communication avec les clients WSE 3.0 et doit uniquement maintenir la parité de sécurité, envisagez d’utiliser les liaisons définies par le système WCF avec les paramètres de sécurité appropriés au lieu de créer une liaison personnalisée.  
  
 Le tableau suivant répertorie le mappage entre un fichier de stratégie WSE 3.0 et la liaison personnalisée équivalente dans WCF.  
  
|Assertion de sécurité clé en main WSE 3.0|Configuration de liaison personnalisée WCF|  
|----------------------------------------|--------------------------------------|  
|\<usernameOverTransportSecurity / >|`<customBinding>   <binding name="MyBinding">     <security authenticationMode="UserNameOverTransport" />     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
|\<mutualCertificate10Security / >|`<customBinding>   <binding name="MyBinding">     <security messageSecurityVersion="WSSecurity10WSTrustFebruary2005WSSecureConversationFebruary2005WSSecurityPolicy11BasicSecurityProfile10" authenticationMode="MutualCertificate" />     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
|\<usernameForCertificateSecurity />|`<customBinding>   <binding name="MyBinding">     <security authenticationMode="UsernameForCertificate"/>     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
|\<anonymousForCertificateSecurity />|`<customBinding>   <binding name="MyBinding">     <security authenticationMode="AnonymousForCertificate"/>     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
|\<kerberosSecurity / >|`<customBinding>   <binding name="MyBinding">     <security authenticationMode="Kerberos"/>     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
|\<mutualCertificate11Security / >|`<customBinding>   <binding name="MyBinding">     <security authenticationMode="MutualCertificate"/>     <textMessageEncoding messageVersion="Soap12WSAddressingAugust2004" />   </binding> </customBinding>`|  
  
 Pour plus d’informations sur la création de liaisons personnalisées dans WCF, consultez [liaisons personnalisées](../../../../docs/framework/wcf/extending/custom-bindings.md).  
  
### <a name="wse-30-web-services-that-are-secured-using-application-code"></a>Services Web WSE 3.0 sécurisés à l'aide du code d'application  
 Si WSE 3.0 ou WCF est utilisé, les exigences de sécurité peuvent être spécifiés dans le code d’application au lieu de dans la configuration. Dans WSE 3.0, cette tâche est accomplie en créant une classe qui dérive de la classe `Policy`, puis en ajoutant les spécifications en appelant la méthode `Add`. Pour plus d’informations sur la spécification des exigences de sécurité dans le code, consultez [Comment : sécuriser un Service Web sans utiliser un fichier de stratégie](https://go.microsoft.com/fwlink/?LinkId=73747). Dans WCF, pour spécifier les exigences de sécurité dans le code, créez une instance de la <xref:System.ServiceModel.Channels.BindingElementCollection> classe et ajoutez une instance d’un <xref:System.ServiceModel.Channels.SecurityBindingElement> à la <xref:System.ServiceModel.Channels.BindingElementCollection>. Les spécifications de l'assertion de sécurité sont définies à l'aide des méthodes d'assistance de mode d'authentification statiques de la classe <xref:System.ServiceModel.Channels.SecurityBindingElement>. Pour plus d’informations sur la spécification des exigences de sécurité dans le code à l’aide de WCF, consultez [Comment : créer un personnalisé de liaison à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md) et [Comment : créer un SecurityBindingElement pour un spécifié Mode d’authentification](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md).  
  
### <a name="wse-30-custom-policy-assertion"></a>Assertion de stratégie personnalisée WSE 3.0  
 Dans WSE 3.0, il existe deux types d'assertions de stratégie personnalisées : celles qui sécurisent un message SOAP et celles qui ne le font pas. Assertions de stratégie qui sécurisent les messages SOAP dérivent de WSE 3.0 `SecurityPolicyAssertion` classe et l’équivalent conceptuel dans WCF est le <xref:System.ServiceModel.Channels.SecurityBindingElement> classe.  
  
 Un point important à retenir est que les assertions de sécurité clé en main de WSE 3.0 sont un sous-ensemble des modes d’authentification WCF. Si vous avez créé une assertion de stratégie personnalisé dans WSE 3.0, il peut y avoir un mode d’authentification WCF équivalent. Par exemple, WSE 3.0 ne fournit pas d'assertion de sécurité CertificateOverTransport qui équivaut à l'assertion de sécurité clé en main `UsernameOverTransport`, mais il utilise un certificat X.509 à des fins d'authentification du client. Si vous avez défini votre propre assertion de stratégie personnalisée pour ce scénario, WCF facilite grandement la migration. WCF définit un mode d’authentification pour ce scénario, donc vous pouvez tirer parti de l’authentification statique de méthodes d’assistance de mode pour configurer un service WCF<xref:System.ServiceModel.Channels.SecurityBindingElement>.  
  
 Lorsqu’il n’est pas un mode d’authentification WCF qui équivaut à une assertion de stratégie personnalisée qui sécurise les messages SOAP, dérivez une classe à partir de <xref:System.ServiceModel.Channels.TransportSecurityBindingElement>, <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> ou <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>classes de WCF et spécifier l’élément de liaison équivalent. Pour plus d’informations, consultez [Comment : créer un personnalisé de liaison à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md).  
  
 Pour convertir une assertion de stratégie personnalisée qui ne sécurise pas un message SOAP, consultez [filtrage](../../../../docs/framework/wcf/feature-details/filtering.md) et l’exemple [intercepteur de Message personnalisé](../../../../docs/framework/wcf/samples/custom-message-interceptor.md).  
  
### <a name="wse-30-custom-security-token"></a>Jeton de sécurité personnalisé WSE 3.0  
 Le modèle de programmation WCF pour la création d’un jeton personnalisé diffère de WSE 3.0. Pour plus d’informations sur la création d’un jeton personnalisé dans WSE, consultez [création de jetons de sécurité personnalisés](https://go.microsoft.com/fwlink/?LinkID=73750). Pour plus d’informations sur la création d’un jeton personnalisé dans WCF, consultez [Comment : créer un jeton personnalisé](../../../../docs/framework/wcf/extending/how-to-create-a-custom-token.md).  
  
### <a name="wse-30-custom-token-manager"></a>Gestionnaire de jetons personnalisés WSE 3.0  
 Le modèle de programmation pour la création d’un gestionnaire de jetons personnalisés diffère dans WCF WSE 3.0. Pour plus d’informations sur la création d’un gestionnaire de jetons personnalisés et les autres composants sont requis pour un jeton de sécurité personnalisé, consultez [Comment : créer un jeton personnalisé](../../../../docs/framework/wcf/extending/how-to-create-a-custom-token.md).  
  
> [!NOTE]
>  Si vous avez créé un personnalisé `UsernameToken` Gestionnaire de jetons de sécurité, WCF fournit un mécanisme plus simple pour spécifier la logique d’authentification que la création d’un sécurité personnalisée Gestionnaire de jetons. Pour plus d’informations, consultez [Comment : utiliser un validateur de mot de passe et le nom d’utilisateur personnalisé](../../../../docs/framework/wcf/feature-details/how-to-use-a-custom-user-name-and-password-validator.md).  
  
### <a name="wse-30-web-services-that-use-mtom-encoded-soap-messages"></a>Services Web WSE 3.0 qui utilisent des messages SOAP encodés MTOM  
 Comme une application WSE 3, une application WCF peut spécifier l’encodage dans la configuration de message MTOM. Pour migrer ce paramètre, ajoutez le [ \<mtomMessageEncoding >](../../../../docs/framework/configure-apps/file-schema/wcf/mtommessageencoding.md) à la liaison pour le service. L’exemple de code suivant illustre l’encodage MTOM comment est spécifié dans WSE 3.0 pour un service qui est équivalent dans WCF.  
  
 **WSE 3.0**  
  
```xml  
<messaging>  
    <mtom clientMode="On"/>  
</messaging>  
```  
  
 **WCF**  
  
```xml  
<customBinding>  
  <binding name="MyBinding">  
    <mtomMessageEncoding/>  
  </binding>  
</customBinding>  
```  
  
## <a name="messaging"></a>Messagerie  
  
### <a name="wse-30-applications-that-use-the-wse-messaging-api"></a>Applications WSE 3.0 qui utilisent l'API de messagerie WSE  
 Lorsque l'API de messagerie WSE est utilisée pour obtenir un accès direct au XML communiqué entre le client et le service Web, l'application peut être convertie de façon à utiliser le « Plain Old XML » (POX). Pour plus d’informations sur POX, consultez [l’interopérabilité avec les Applications POX](../../../../docs/framework/wcf/feature-details/interoperability-with-pox-applications.md). Pour plus d’informations sur l’API de messagerie WSE, consultez [envoi et réception de Messages à l’aide de WSE messagerie API SOAP](https://go.microsoft.com/fwlink/?LinkID=73755).  
  
## <a name="transports"></a>Transports  
  
### <a name="tcp"></a>TCP  
 Par défaut, les clients WSE 3.0 et les services Web qui envoient des messages SOAP à l’aide du transport TCP n’interagissent pas avec les clients WCF et les services Web. Cette incompatibilité est due aux différences de tramage utilisé dans le protocole TCP et aux performances. Toutefois, un exemple WCF décrit en détail comment implémenter une session TCP personnalisée qui interagit avec WSE 3.0. Pour plus d’informations sur cet exemple, consultez [Transport : WSE 3.0 TCP Interoperability](../../../../docs/framework/wcf/samples/transport-wse-3-0-tcp-interoperability.md).  
  
 Pour spécifier qu’une application WCF utilise le transport TCP, utilisez le [ \<netTcpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md).  
  
### <a name="custom-transport"></a>Transport personnalisé  
 L’équivalent d’un transport personnalisé WSE 3.0 dans WCF est une extension de canal. Pour plus d’informations sur la création d’une extension de canal, consultez [extension de la couche de canal](../../../../docs/framework/wcf/extending/extending-the-channel-layer.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Cycle de vie de la programmation de base](../../../../docs/framework/wcf/basic-programming-lifecycle.md)  
 [Liaisons personnalisées](../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [Guide pratique pour créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [Guide pratique pour créer un SecurityBindingElement pour un mode d’authentification spécifié](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)
