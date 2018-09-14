---
title: 'Comment : accéder à un service WSE 3.0 avec un client WCF'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1f9bcd9b-8f8f-47fa-8f1e-0d47236eb800
ms.openlocfilehash: 2e01d3de6ee7b415c7b3f18a20e840b8ec4ab9b6
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45597662"
---
# <a name="how-to-access-a-wse-30-service-with-a-wcf-client"></a>Comment : accéder à un service WSE 3.0 avec un client WCF
Les clients Windows Communication Foundation (WCF) sont compatible au niveau câble avec Web Services Enhancements (WSE) 3.0 pour les services Microsoft .NET lorsque les clients WCF sont configurés pour utiliser la version d’août 2004 de la spécification WS-Addressing. Toutefois, les services WSE 3.0 ne pas prennent en charge le protocole d’échange (MEX) de métadonnées, par conséquent, lorsque vous utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour créer une classe de client WCF, les paramètres de sécurité ne sont pas appliquées pour le texte généré Client WCF. Par conséquent, vous devez spécifier les paramètres de sécurité que le service WSE 3.0 requiert une fois le client WCF est généré.  
  
 Vous pouvez appliquer ces paramètres de sécurité à l’aide d’une liaison personnalisée pour prendre en compte les exigences du service WSE 3.0 et les exigences interopérables entre un service WSE 3.0 et un client WCF. Ces spécifications d'interopérabilité incluent l'utilisation précédemment mentionnée de la version d'août 2004 de la spécification WS-Addressing et la protection des messages par défaut WSE 3.0 de <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>. La protection de message par défaut pour WCF est <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature>. Cette rubrique explique comment créer une liaison WCF qui interagit avec un service WSE 3.0. WCF fournit également un exemple qui incorpore cette liaison. Pour plus d’informations sur cet exemple, consultez [interopérabilité avec les Services Web ASMX](../../../../docs/framework/wcf/samples/interoperating-with-asmx-web-services.md).  
  
### <a name="to-access-a-wse-30-web-service-with-a-wcf-client"></a>Pour accéder à un service Web WSE 3.0 avec un client WCF  
  
1.  Exécutez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour créer un client WCF pour le service Web WSE 3.0.  
  
     Pour un service Web WSE 3.0, un client WCF est créé. WSE 3.0 ne prenant pas en charge le protocole MEX, vous ne pouvez pas utiliser l’outil pour récupérer les exigences de sécurité pour le service Web. Le développeur d'applications doit ajouter les paramètres de sécurité pour le client.  
  
     Pour plus d’informations sur la création d’un client WCF, consultez le [Comment : créer un Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).  
  
2.  Créez une classe qui représente une liaison pouvant communiquer avec les services Web WSE 3.0.  
  
     La classe suivante fait partie de la [interopérabilité avec WSE](https://msdn.microsoft.com/library/f6816861-96a0-45f9-8736-8e4e82cd3a41) exemple :  
  
    1.  Créez une classe qui dérive de la classe <xref:System.ServiceModel.Channels.Binding>.  
  
         L'exemple de code suivant crée une classe nommée `WseHttpBinding` qui dérive de la classe <xref:System.ServiceModel.Channels.Binding>.  
  
         [!code-csharp[c_WCFClientToWSEService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#1)]
         [!code-vb[c_WCFClientToWSEService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#1)]  
  
    2.  Ajoutez à la classe des propriétés spécifiant l'assertion clé en main WSE utilisée par le service WSE, si des clés dérivées sont requises, si des sessions sécurisées sont utilisées, si des confirmations de signature sont requises, ainsi que les paramètres de protection des messages. Dans WSE 3.0, une assertion clé en main spécifie les exigences de sécurité pour un client ou un service Web, similaire au mode d’authentification d’une liaison dans WCF.  
  
         L'exemple de code suivant définit les propriétés `SecurityAssertion`, `RequireDerivedKeys`, `EstablishSecurityContext` et `MessageProtectionOrder` qui spécifient l'assertion clé en main WSE, si des clés dérivées sont requises, si des sessions sécurisées sont utilisées, si des confirmations de signature sont requises, ainsi que les paramètres de protection des messages, respectivement.  
  
         [!code-csharp[c_WCFClientToWSEService#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#3)]
         [!code-vb[c_WCFClientToWSEService#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#3)]  
  
    3.  Substituez la méthode <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> pour définir les propriétés de la liaison.  
  
         L'exemple de code suivant spécifie le transport, l'encodage de message et les paramètres de protection des messages en obtenant les valeurs des propriétés `SecurityAssertion` et `MessageProtectionOrder`.  
  
         [!code-csharp[c_WCFClientToWSEService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#2)]
         [!code-vb[c_WCFClientToWSEService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#2)]  
  
3.  Dans le code d’application cliente, ajoutez le code pour définir les propriétés de la liaison.  
  
     L’exemple de code suivant spécifie que le client WCF doit utiliser l’authentification et protection des messages tel que défini par le WSE 3.0 `AnonymousForCertificate` assertion de sécurité clé en main. En outre, des sessions sécurisées et des clés dérivées sont requises.  
  
     [!code-csharp[c_WCFClientToWSEService#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#4)]
     [!code-vb[c_WCFClientToWSEService#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#4)]  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant définit une liaison personnalisée qui expose des propriétés correspondant à celles d’une assertion de sécurité clé en main WSE 3.0. Cette liaison personnalisée, qui est nommée `WseHttpBinding`, est ensuite utilisé pour spécifier les propriétés de liaison pour un client WCF qui communique avec l’exemple de démarrage rapide de WSSecurityAnonymous WSE 3.0.  
  
  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.Binding>  
 [Interopérabilité avec WSE](https://msdn.microsoft.com/library/f6816861-96a0-45f9-8736-8e4e82cd3a41)
