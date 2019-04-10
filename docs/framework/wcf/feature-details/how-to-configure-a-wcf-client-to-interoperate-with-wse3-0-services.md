---
title: 'Procédure : configurer un client WCF pour interagir avec des services WSE 3.0'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 3dadd7f1-d207-4ea5-a73b-3e8aa44407f8
ms.openlocfilehash: 62642651516274a27c44abfc19e94dc529690ea9
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59304543"
---
# <a name="how-to-configure-a-wcf-client-to-interoperate-with-wse30-services"></a><span data-ttu-id="f4ae5-102">Procédure : configurer un client WCF pour interagir avec des services WSE 3.0</span><span class="sxs-lookup"><span data-stu-id="f4ae5-102">How to: Configure a WCF Client to interoperate with WSE3.0 Services</span></span>
<span data-ttu-id="f4ae5-103">Les clients Windows Communication Foundation (WCF) sont compatible au niveau câble avec Web Services Enhancements 3.0 pour les services Microsoft .NET (WSE) lorsque les clients WCF sont configurés pour utiliser la version d’août 2004 de la spécification WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-103">Windows Communication Foundation (WCF) clients are wire-level compatible with Web Services Enhancements 3.0 for Microsoft .NET (WSE) services when WCF clients are configured to use the August 2004 version of the WS-Addressing specification.</span></span>  
  
### <a name="to-configure-a-wcf-client-to-interoperate-with-a-wse-30-web-service"></a><span data-ttu-id="f4ae5-104">Configurer un client WCF pour interagir avec un service Web WSE 3.0</span><span class="sxs-lookup"><span data-stu-id="f4ae5-104">To configure a WCF client to interoperate with a WSE 3.0 Web service</span></span>  
  
1. <span data-ttu-id="f4ae5-105">Exécutez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour créer un client WCF pour le service Web WSE 3.0.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-105">Run the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to create a WCF client for the WSE 3.0 Web service.</span></span>  
  
     <span data-ttu-id="f4ae5-106">Pour un service Web WSE, une classe de client WCF est créée.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-106">For a WSE Web service, a WCF client class is created.</span></span>  
  
     <span data-ttu-id="f4ae5-107">Pour plus d’informations sur la création d’un client WCF, consultez le [Comment : Créer un Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="f4ae5-107">For details about creating a WCF client, see the [How to: Create a Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span></span>  
  
2. <span data-ttu-id="f4ae5-108">Créez une classe qui représente une liaison pouvant communiquer avec les services Web WSE 3.0.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-108">Create a class that represents a binding that can communicate with WSE 3.0 Web services.</span></span>  
  
     <span data-ttu-id="f4ae5-109">La classe suivante fait partie de la [interopérabilité avec WSE](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms752257%28v=vs.90%29) exemple.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-109">The following class is part of the [Interoperating with WSE](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms752257%28v=vs.90%29) sample.</span></span>  
  
    1.  <span data-ttu-id="f4ae5-110">Créez une classe qui dérive de la classe <xref:System.ServiceModel.Channels.Binding>.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-110">Create a class that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         <span data-ttu-id="f4ae5-111">L'exemple de code suivant crée une classe nommée `WseHttpBinding` qui dérive de la classe <xref:System.ServiceModel.Channels.Binding>.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-111">The following code example creates a class named `WseHttpBinding` that derives from the <xref:System.ServiceModel.Channels.Binding> class.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#1)]
         [!code-vb[c_WCFClientToWSEService#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#1)]  
  
    2.  <span data-ttu-id="f4ae5-112">Ajoutez à la classe des propriétés spécifiant l'assertion clé en main WSE, si des clés dérivées sont requises, si des sessions sécurisées sont utilisées, si des confirmations de signature sont requises, et les paramètres de protection des messages.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-112">Add properties to the class that specify the WSE turnkey assertion, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings.</span></span>  
  
         <span data-ttu-id="f4ae5-113">L’exemple de code suivant définit la `SecurityAssertion`, `RequireDerivedKeys`, `EstablishSecurityContext`, et `MessageProtectionOrder` propriétés.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-113">The following code example defines the `SecurityAssertion`, `RequireDerivedKeys`, `EstablishSecurityContext`, and `MessageProtectionOrder` properties.</span></span> <span data-ttu-id="f4ae5-114">Ils spécifient l’assertion clé en main WSE, si des clés dérivées sont requises, si des sessions sécurisées sont utilisées, si des confirmations de signature sont requises et les paramètres de protection des messages, respectivement.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-114">They specify the WSE turnkey assertion, whether derived keys are required, whether secure sessions are used, whether signature confirmations are required, and the message protection settings, respectively.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#3)]
         [!code-vb[c_WCFClientToWSEService#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#3)]  
  
    3.  <span data-ttu-id="f4ae5-115">Substituez la méthode <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> pour définir les propriétés de la liaison.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-115">Override the <xref:System.ServiceModel.Channels.Binding.CreateBindingElements%2A> method to set the binding properties.</span></span>  
  
         <span data-ttu-id="f4ae5-116">L'exemple de code suivant spécifie le transport, l'encodage de message et les paramètres de protection des messages en obtenant les valeurs des propriétés `SecurityAssertion` et `MessageProtectionOrder`.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-116">The following code example specifies the transport, message encoding, and message protection settings by getting the values of the `SecurityAssertion` and `MessageProtectionOrder` properties.</span></span>  
  
         [!code-csharp[c_WCFClientToWSEService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/wsehttpbinding.cs#2)]
         [!code-vb[c_WCFClientToWSEService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/wsehttpbinding.vb#2)]  
  
3. <span data-ttu-id="f4ae5-117">Dans le code d’application cliente, ajoutez le code pour définir les propriétés de la liaison.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-117">In the client application code, add code to set the binding properties.</span></span>  
  
     <span data-ttu-id="f4ae5-118">L’exemple de code suivant spécifie que le client WCF doit utiliser l’authentification et protection des messages tel que défini par le WSE 3.0 `AnonymousForCertificate` assertion de sécurité clé en main.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-118">The following code example specifies that the WCF client must use message protection and authentication as defined by the WSE 3.0 `AnonymousForCertificate` turnkey security assertion.</span></span> <span data-ttu-id="f4ae5-119">En outre, des sessions sécurisées et des clés dérivées sont requises.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-119">Additionally, secure sessions and derived keys are required.</span></span>  
  
     [!code-csharp[c_WCFClientToWSEService#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#4)]
     [!code-vb[c_WCFClientToWSEService#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="f4ae5-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4ae5-120">Example</span></span>  
 <span data-ttu-id="f4ae5-121">L'exemple de code suivant définit une liaison personnalisée qui expose des propriétés correspondant à celles d'une assertion de sécurité clé en main WSE 3.0.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-121">The following code example defines a custom binding that exposes properties that correspond to the properties of a WSE 3.0 turnkey security assertion.</span></span> <span data-ttu-id="f4ae5-122">La liaison personnalisée, qui est nommée `WseHttpBinding`, est ensuite utilisé pour spécifier les propriétés de liaison pour un client WCF.</span><span class="sxs-lookup"><span data-stu-id="f4ae5-122">The custom binding, which is named `WseHttpBinding`, is then used to specify the binding properties for a WCF client.</span></span>  

[!code-csharp[c_WCFClientToWSEService#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_wcfclienttowseservice/cs/client.cs#0)]
[!code-vb[c_WCFClientToWSEService#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_wcfclienttowseservice/vb/client.vb#0)]  
  
## <a name="see-also"></a><span data-ttu-id="f4ae5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4ae5-123">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
- [<span data-ttu-id="f4ae5-124">Interoperating with WSE</span><span class="sxs-lookup"><span data-stu-id="f4ae5-124">Interoperating with WSE</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms752257%28v=vs.90%29)
