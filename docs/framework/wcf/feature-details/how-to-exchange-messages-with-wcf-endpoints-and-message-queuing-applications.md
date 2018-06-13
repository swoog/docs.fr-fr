---
title: 'Comment : échanger des messages avec des points de terminaison WCF et des applications Message Queuing'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 62210fd8-a372-4d55-ab9b-c99827d1885e
ms.openlocfilehash: 807a34ac50ea317ace42ec12eddcd9ec7cf3736b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491077"
---
# <a name="how-to-exchange-messages-with-wcf-endpoints-and-message-queuing-applications"></a><span data-ttu-id="06d57-102">Comment : échanger des messages avec des points de terminaison WCF et des applications Message Queuing</span><span class="sxs-lookup"><span data-stu-id="06d57-102">How to: Exchange Messages with WCF Endpoints and Message Queuing Applications</span></span>
<span data-ttu-id="06d57-103">Vous pouvez intégrer des applications Message Queuing (MSMQ) existantes avec les applications Windows Communication Foundation (WCF) pour convertir des messages MSMQ en messages WCF à l’aide de la liaison d’intégration MSMQ.</span><span class="sxs-lookup"><span data-stu-id="06d57-103">You can integrate existing Message Queuing (MSMQ) applications with Windows Communication Foundation (WCF) applications by using the MSMQ integration binding to convert MSMQ messages to and from WCF messages.</span></span> <span data-ttu-id="06d57-104">Cela vous permet de vous appeler dans les applications réceptrices MSMQ depuis des clients WCF ainsi que d’appeler dans les services WCF à partir d’applications expéditrices MSMQ.</span><span class="sxs-lookup"><span data-stu-id="06d57-104">This allows you to call into MSMQ receiver applications from WCF clients as well as call into WCF services from MSMQ sender applications.</span></span>  
  
 <span data-ttu-id="06d57-105">Dans cette section, nous expliquons comment utiliser <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> pour la communication en file d’attente entre (1) un client WCF et un service d’application MSMQ écrit à l’aide de System.Messaging et (2) un client d’application MSMQ et un service WCF.</span><span class="sxs-lookup"><span data-stu-id="06d57-105">In this section, we explain how to use <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> for queued communication between (1) a WCF client and an MSMQ application service written using System.Messaging and (2) an MSMQ application client and a WCF service.</span></span>  
  
 <span data-ttu-id="06d57-106">Pour obtenir un exemple complet qui montre comment appeler une application réceptrice MSMQ à partir d’un client WCF, consultez le [Windows Communication Foundation à Message Queuing](../../../../docs/framework/wcf/samples/wcf-to-message-queuing.md) exemple.</span><span class="sxs-lookup"><span data-stu-id="06d57-106">For a complete sample that demonstrates how to call a MSMQ receiver application from a WCF client, see the [Windows Communication Foundation to Message Queuing](../../../../docs/framework/wcf/samples/wcf-to-message-queuing.md) sample.</span></span>  
  
 <span data-ttu-id="06d57-107">Pour obtenir un exemple complet qui montre comment appeler un service WCF à partir d’un client MSMQ, consultez le [Message Queuing pour Windows Communication Foundation](../../../../docs/framework/wcf/samples/message-queuing-to-wcf.md) exemple.</span><span class="sxs-lookup"><span data-stu-id="06d57-107">For a complete sample that demonstrates how to call a WCF service from a MSMQ client, see the [Message Queuing to Windows Communication Foundation](../../../../docs/framework/wcf/samples/message-queuing-to-wcf.md) sample.</span></span>  
  
### <a name="to-create-a-wcf-service-that-receives-messages-from-a-msmq-client"></a><span data-ttu-id="06d57-108">Pour créer un service WCF qui reçoit des messages depuis un client MSMQ</span><span class="sxs-lookup"><span data-stu-id="06d57-108">To create a WCF service that receives messages from a MSMQ client</span></span>  
  
1.  <span data-ttu-id="06d57-109">Définissez une interface qui définit le contrat de service pour le service WCF qui reçoit les messages en file d’attente à partir d’une application expéditrice MSMQ, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="06d57-109">Define an interface that defines the service contract for the WCF service that receives queued messages from a MSMQ sender application, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_MsmqToWcf#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#1)]
     [!code-vb[S_MsmqToWcf#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#1)]  
  
2.  <span data-ttu-id="06d57-110">Implémentez l'interface et appliquez l'attribut <xref:System.ServiceModel.ServiceBehaviorAttribute> à la classe, comme le montre l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="06d57-110">Implement the interface and apply the <xref:System.ServiceModel.ServiceBehaviorAttribute> attribute to the class, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_MsmqToWcf#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#2)]
     [!code-vb[S_MsmqToWcf#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#2)]  
  
3.  <span data-ttu-id="06d57-111">Créez un fichier de configuration qui spécifie la liaison <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>.</span><span class="sxs-lookup"><span data-stu-id="06d57-111">Create a configuration file that specifies the <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>.</span></span>  
  
  
  
4.  <span data-ttu-id="06d57-112">Instanciez un objet <xref:System.ServiceModel.ServiceHost> qui utilise la liaison configurée.</span><span class="sxs-lookup"><span data-stu-id="06d57-112">Instantiate a <xref:System.ServiceModel.ServiceHost> object that uses the configured binding.</span></span>  
  
  
  
### <a name="to-create-a-wcf-client-that-sends-messages-to-a-msmq-receiver-application"></a><span data-ttu-id="06d57-113">Pour créer un client WCF qui envoie des messages à une application réceptrice MSMQ</span><span class="sxs-lookup"><span data-stu-id="06d57-113">To create a WCF client that sends messages to a MSMQ receiver application</span></span>  
  
1.  <span data-ttu-id="06d57-114">Définissez une interface qui définit le contrat de service pour le client WCF qui envoie en attente des messages du récepteur MSMQ, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="06d57-114">Define an interface that defines the service contract for the WCF client that sends queued messages to the MSMQ receiver, as shown in the following example code.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/proxy.cs#6)]
     [!code-vb[S_WcfToMsmq#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/proxy.vb#6)]  
  
2.  <span data-ttu-id="06d57-115">Définissez une classe de client que le client WCF utilise pour appeler le récepteur MSMQ.</span><span class="sxs-lookup"><span data-stu-id="06d57-115">Define a client class that the WCF client uses to call the MSMQ receiver.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#2)]
     [!code-vb[S_WcfToMsmq#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#2)]  
  
3.  <span data-ttu-id="06d57-116">Créez une configuration qui spécifie l’utilisation de la liaison MsmqIntegrationBinding.</span><span class="sxs-lookup"><span data-stu-id="06d57-116">Create a configuration that specifies use of the MsmqIntegrationBinding binding.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#3)]
     [!code-vb[S_WcfToMsmq#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#3)]  
  
4.  <span data-ttu-id="06d57-117">Créez une instance de la classe de client et appelez la méthode définie par le service qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="06d57-117">Create an instance of the client class and call the method defined by the message receiving service.</span></span>  
  
     [!code-csharp[S_WcfToMsmq#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/client.cs#4)]  
  
## <a name="see-also"></a><span data-ttu-id="06d57-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06d57-118">See Also</span></span>  
 [<span data-ttu-id="06d57-119">Vue d’ensemble des files d’attente</span><span class="sxs-lookup"><span data-stu-id="06d57-119">Queues Overview</span></span>](../../../../docs/framework/wcf/feature-details/queues-overview.md)  
 [<span data-ttu-id="06d57-120">Guide pratique pour échanger des messages en file d’attente avec des points de terminaison WCF</span><span class="sxs-lookup"><span data-stu-id="06d57-120">How to: Exchange Queued Messages with WCF Endpoints</span></span>](../../../../docs/framework/wcf/feature-details/how-to-exchange-queued-messages-with-wcf-endpoints.md)  
 [<span data-ttu-id="06d57-121">Windows Communication Foundation vers Message Queuing</span><span class="sxs-lookup"><span data-stu-id="06d57-121">Windows Communication Foundation to Message Queuing</span></span>](../../../../docs/framework/wcf/samples/wcf-to-message-queuing.md)  
 [<span data-ttu-id="06d57-122">Installation de Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="06d57-122">Installing Message Queuing (MSMQ)</span></span>](../../../../docs/framework/wcf/samples/installing-message-queuing-msmq.md)  
 [<span data-ttu-id="06d57-123">Message Queuing vers Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="06d57-123">Message Queuing to Windows Communication Foundation</span></span>](../../../../docs/framework/wcf/samples/message-queuing-to-wcf.md)  
 [<span data-ttu-id="06d57-124">Sécurité du message sur Message Queuing</span><span class="sxs-lookup"><span data-stu-id="06d57-124">Message Security over Message Queuing</span></span>](../../../../docs/framework/wcf/samples/message-security-over-message-queuing.md)
