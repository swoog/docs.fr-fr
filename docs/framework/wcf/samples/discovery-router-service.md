---
title: Discovery Router Service
ms.date: 03/30/2017
ms.assetid: 3d30af47-b24f-40e5-833a-24d77125c9e6
ms.openlocfilehash: 9c0c409eb6cf3146a198b9f4bcd6d76660f5da36
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43509079"
---
# <a name="discovery-router-service"></a><span data-ttu-id="3cf4e-102">Discovery Router Service</span><span class="sxs-lookup"><span data-stu-id="3cf4e-102">Discovery Router Service</span></span>
<span data-ttu-id="3cf4e-103">Cet exemple montre comment transférer des messages de découverte à un autre point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-103">This sample demonstrates how to forward discovery messages to another endpoint.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="3cf4e-104">Démonstrations</span><span class="sxs-lookup"><span data-stu-id="3cf4e-104">Demonstrates</span></span>  
 <span data-ttu-id="3cf4e-105">Routage de découverte</span><span class="sxs-lookup"><span data-stu-id="3cf4e-105">Discovery Routing</span></span>  
  
## <a name="discussion"></a><span data-ttu-id="3cf4e-106">Discussion</span><span class="sxs-lookup"><span data-stu-id="3cf4e-106">Discussion</span></span>  
 <span data-ttu-id="3cf4e-107">Le routage de découverte est utile dans un scénario où un client recherche un service à l'aide d'un proxy et que le proxy ne connaît pas ce service, mais connaît l'existence d'un autre proxy.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-107">Discovery routing is useful in a scenario in which a client is looking for a service using a proxy and the proxy is unaware of such a service, but knows of another proxy.</span></span> <span data-ttu-id="3cf4e-108">Ce proxy peut transférer le paquet de découverte de ce client au deuxième proxy.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-108">This proxy can forward the discovery packet from this client to the second proxy.</span></span> <span data-ttu-id="3cf4e-109">Le deuxième proxy peut rechercher le service et retourner les réponses au client d'origine.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-109">The second proxy can look for the service and return the responses to the original client.</span></span>  
  
 <span data-ttu-id="3cf4e-110">Dans cet exemple, un client envoie un message à un composant de routage de découverte.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-110">In this sample, a client sends a message to a discovery routing component.</span></span> <span data-ttu-id="3cf4e-111">Ce message est envoyé à un point de terminaison spécifique situé sur le routeur de découverte.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-111">This message is sent to a specific endpoint on the discovery router.</span></span> <span data-ttu-id="3cf4e-112">Le routeur transfère alors le message à un point de terminaison de multidiffusion UDP.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-112">The router then forwards the message to a UDP multicast endpoint.</span></span> <span data-ttu-id="3cf4e-113">Le message Probe rejoint le point de terminaison de multidiffusion et un service à l'écoute d'une adresse de multidiffusion UDP répond à ce routeur de découverte.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-113">The probe message goes out to the multicast endpoint and a service listening on a UDP multicast address responds to that discovery router.</span></span> <span data-ttu-id="3cf4e-114">Le routeur de découverte collecte les réponses et les renvoie au client.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-114">The discovery router collects the responses and sends them back to the client.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="3cf4e-115">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="3cf4e-115">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="3cf4e-116">Créez un exemple.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-116">Build the sample.</span></span>  
  
2.  <span data-ttu-id="3cf4e-117">Exécutez le fichier exécutable DiscoveryRouter.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-117">Run the DiscoveryRouter executable.</span></span>  
  
3.  <span data-ttu-id="3cf4e-118">Exécutez le fichier exécutable du service à partir du répertoire de build.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-118">Run the service executable from the build directory.</span></span>  
  
4.  <span data-ttu-id="3cf4e-119">Exécutez le fichier exécutable du client.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-119">Run the client executable.</span></span> <span data-ttu-id="3cf4e-120">Notez que le client trouve le service.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-120">Note that the client locates the service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3cf4e-121">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-121">The samples may already be installed on your machine.</span></span> <span data-ttu-id="3cf4e-122">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-122">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="3cf4e-123">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-123">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="3cf4e-124">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="3cf4e-124">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\DiscoveryRouter`
