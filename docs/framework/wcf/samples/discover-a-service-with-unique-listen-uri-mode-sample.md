---
title: Découvrir un service avec Unique Listen Uri Mode Sample
ms.date: 03/30/2017
ms.assetid: 9a6d35b2-0469-43c8-a0c9-63623e3d2733
ms.openlocfilehash: e6129594df6170f94a06caa08a9f16e4770bbfd4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33501453"
---
# <a name="discover-a-service-with-unique-listen-uri-mode-sample"></a><span data-ttu-id="3eade-102">Découvrir un service avec Unique Listen Uri Mode Sample</span><span class="sxs-lookup"><span data-stu-id="3eade-102">Discover a Service with Unique Listen Uri Mode Sample</span></span>
<span data-ttu-id="3eade-103">Cet exemple montre comment découvrir un service dont la propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique>.</span><span class="sxs-lookup"><span data-stu-id="3eade-103">This sample demonstrates how to discover a service that has the <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> property set to <xref:System.ServiceModel.Description.ListenUriMode.Unique>.</span></span> <span data-ttu-id="3eade-104">Lorsque la propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique>, le caractère unique de ListenUri peut être garanti soit en définissant le port de sorte qu'il soit unique, soit en ajoutant un GUID pour que le chemin d'accès soit unique.</span><span class="sxs-lookup"><span data-stu-id="3eade-104">When the <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> property is set to <xref:System.ServiceModel.Description.ListenUriMode.Unique>, the ListenUri is ensured to be unique by either setting the port to be unique or for the path to be unique by appending a GUID.</span></span>  
  
### <a name="features-on-the-service"></a><span data-ttu-id="3eade-105">Fonctionnalités sur le service</span><span class="sxs-lookup"><span data-stu-id="3eade-105">Features on the Service</span></span>  
 <span data-ttu-id="3eade-106">La propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique> pour le point de terminaison TCP.</span><span class="sxs-lookup"><span data-stu-id="3eade-106">The <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> property is set to <xref:System.ServiceModel.Description.ListenUriMode.Unique> for the TCP endpoint.</span></span> <span data-ttu-id="3eade-107">Le service est alors rendu détectable sur un point de terminaison <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>.</span><span class="sxs-lookup"><span data-stu-id="3eade-107">The service is then made discoverable over a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> endpoint.</span></span>  
  
### <a name="features-on-the-client"></a><span data-ttu-id="3eade-108">Caractéristiques sur le client</span><span class="sxs-lookup"><span data-stu-id="3eade-108">Features on the Client</span></span>  
 <span data-ttu-id="3eade-109">Ce client se connecte au service à l'aide du `Via.Uri` en utilisant la méthode <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A>.</span><span class="sxs-lookup"><span data-stu-id="3eade-109">This client connects to the service using the correct `Via.Uri` by using the <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A> method.</span></span> <span data-ttu-id="3eade-110">Le <xref:System.ServiceModel.Discovery.FindResponse> retourné par la méthode est alors interrogé pour déterminer s'il contient un <xref:System.ServiceModel.Endpoint.ListenUri%2A> valide et s'il est différent d'`Address.Uri`.</span><span class="sxs-lookup"><span data-stu-id="3eade-110">The <xref:System.ServiceModel.Discovery.FindResponse> that is returned from the method is then queried for whether it contains a valid <xref:System.ServiceModel.Endpoint.ListenUri%2A> and whether it is different than `Address.Uri`.</span></span> <span data-ttu-id="3eade-111">Les informations appropriées sont ensuite passées à la méthode `InvokeCalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="3eade-111">The appropriate information is then passed to the `InvokeCalculatorService` method.</span></span> <span data-ttu-id="3eade-112">Dans la méthode `InvokeCalculatorService`, l'appelant passe <xref:System.ServiceModel.Endpoint.ListenUri%2A>, suite à quoi un `ClientViaBehavior` avec le `Via.Uri` correct est ajouté au point de terminaison du client.</span><span class="sxs-lookup"><span data-stu-id="3eade-112">In the `InvokeCalculatorService` method, the <xref:System.ServiceModel.Endpoint.ListenUri%2A> was passed in by the caller, then a `ClientViaBehavior` with the correct `Via.Uri` is added to the client’s endpoint.</span></span>  
  
##### <a name="to-use-this-sample"></a><span data-ttu-id="3eade-113">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="3eade-113">To use this sample</span></span>  
  
1.  <span data-ttu-id="3eade-114">À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez UniqueListenUriMode.sln.</span><span class="sxs-lookup"><span data-stu-id="3eade-114">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open UniqueListenUriMode.sln.</span></span>  
  
2.  <span data-ttu-id="3eade-115">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="3eade-115">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="3eade-116">Exécutez l'application du service, générée dans le dossier [répertoire de base de la solution]\service\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="3eade-116">Run the service application, which is generated in the [solution base directory]\service\bin\debug folder.</span></span>  
  
4.  <span data-ttu-id="3eade-117">Exécutez l’application du client, générée dans le dossier [répertoire de base de la solution]\Client\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="3eade-117">Run the client application, which is generated in the [solution base directory]\Client\bin\debug folder.</span></span>  
  
     <span data-ttu-id="3eade-118">Le client trouve le service en cours d'exécution et écrit dans la console les métadonnées publiées par le point de terminaison du service.</span><span class="sxs-lookup"><span data-stu-id="3eade-118">The client locates the running service and writes to the console the metadata published by the service’s endpoint.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3eade-119">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3eade-119">The samples may already be installed on your machine.</span></span> <span data-ttu-id="3eade-120">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="3eade-120">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="3eade-121">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="3eade-121">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="3eade-122">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="3eade-122">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\UniqueListenUriMode`  
  
## <a name="see-also"></a><span data-ttu-id="3eade-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eade-123">See Also</span></span>
