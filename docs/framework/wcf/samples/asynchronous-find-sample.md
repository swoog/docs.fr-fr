---
title: Exemple Asynchronous Find
ms.date: 03/30/2017
ms.assetid: 7a713a25-c1f4-42e1-8c4a-93d64ca45a3b
ms.openlocfilehash: 37edcb4d1f04eb56d3f24ca3acc3543d7f9696f5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43424389"
---
# <a name="asynchronous-find-sample"></a><span data-ttu-id="b9791-102">Exemple Asynchronous Find</span><span class="sxs-lookup"><span data-stu-id="b9791-102">Asynchronous Find Sample</span></span>
<span data-ttu-id="b9791-103">Cet exemple montre comment utiliser l'opération de recherche asynchrone à partir d'une application cliente.</span><span class="sxs-lookup"><span data-stu-id="b9791-103">This sample shows how to use the asynchronous find operation from a client application.</span></span>  
  
## <a name="sample-details"></a><span data-ttu-id="b9791-104">Détails de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b9791-104">Sample Details</span></span>  
 <span data-ttu-id="b9791-105">L'avantage à suivre ce modèle de conception réside dans le fait que le client reçoit une notification asynchrone lorsque la demande de recherche a situé des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b9791-105">The benefit of following this design pattern is that the client is notified asynchronously of the endpoints located as a result of the find request.</span></span> <span data-ttu-id="b9791-106">Pour en comprendre le fonctionnement, ouvrez le fichier Client.cs.</span><span class="sxs-lookup"><span data-stu-id="b9791-106">To see how this works, open the Client.cs file.</span></span> <span data-ttu-id="b9791-107">Notez que l'objet <xref:System.ServiceModel.Discovery.DiscoveryClient> a deux délégués attachés à ses gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="b9791-107">Note the <xref:System.ServiceModel.Discovery.DiscoveryClient> object has two delegates attached to its event handlers.</span></span> <span data-ttu-id="b9791-108">Un délégué est appelé lorsqu'un événement <xref:System.ServiceModel.Discovery.DiscoveryClient.FindCompleted> est déclenché et un autre est appelé chaque fois qu'un événement <xref:System.ServiceModel.Discovery.DiscoveryClient.FindProgressChanged> est déclenché.</span><span class="sxs-lookup"><span data-stu-id="b9791-108">One delegate is called when a <xref:System.ServiceModel.Discovery.DiscoveryClient.FindCompleted> event is raised and another is called each time a <xref:System.ServiceModel.Discovery.DiscoveryClient.FindProgressChanged> event is raised.</span></span> <span data-ttu-id="b9791-109">L’exemple montre comment vous pouvez utiliser ce modèle dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b9791-109">The sample shows how you can utilize this pattern in your application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b9791-110">Cet exemple utilise des points de terminaison HTTP et pour l'exécuter, des listes de contrôle d'accès (ACL) d'URL appropriées doivent être ajoutées.</span><span class="sxs-lookup"><span data-stu-id="b9791-110">This sample uses HTTP endpoints and to run, proper URL ACLs must be added.</span></span> <span data-ttu-id="b9791-111">Pour plus d’informations, consultez [configuration de HTTP et HTTPS](../../../../docs/framework/wcf/feature-details/configuring-http-and-https.md).</span><span class="sxs-lookup"><span data-stu-id="b9791-111">For more information, see [Configuring HTTP and HTTPS](../../../../docs/framework/wcf/feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="b9791-112">L'exécution de la commande suivante avec un privilège élevé doit ajouter les ACL appropriées.</span><span class="sxs-lookup"><span data-stu-id="b9791-112">Executing the following command at an elevated privilege should add the appropriate ACLs.</span></span> <span data-ttu-id="b9791-113">Vous pouvez substituer vos domaine et nom d’utilisateur aux arguments suivants si la commande ne fonctionne pas telle quelle.</span><span class="sxs-lookup"><span data-stu-id="b9791-113">You may want to substitute your domain and username for the following arguments if the command does not work as is.</span></span> `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="b9791-114">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="b9791-114">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="b9791-115">À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier AsyncFind.sln.</span><span class="sxs-lookup"><span data-stu-id="b9791-115">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the AsyncFind.sln.</span></span>  
  
2.  <span data-ttu-id="b9791-116">Appuyez sur Ctrl+Maj+B pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="b9791-116">Press CTRL+SHIFT+B to build the solution.</span></span>  
  
3.  <span data-ttu-id="b9791-117">Ouvrez une invite de commandes [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], accédez au répertoire \WCF\Basic\Discovery\AsyncFind\CS\service\bin\Debug ou \WCF\Basic\Discovery\AsyncFind\VB\service\bin\Debug et exécutez Service.exe.</span><span class="sxs-lookup"><span data-stu-id="b9791-117">Open a [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] command prompt and navigate to the \WCF\Basic\Discovery\AsyncFind\CS\service\bin\Debug or \WCF\Basic\Discovery\AsyncFind\VB\service\bin\Debug directory and run Service.exe.</span></span>  
  
4.  <span data-ttu-id="b9791-118">Une fois le service démarré, accédez au répertoire \WCF\Basic\Discovery\AsyncFind\CS\client\bin\Debug ou WCF\Basic\Discovery\AsyncFind\VB\client\bin\Debug et exécutez Client.exe.</span><span class="sxs-lookup"><span data-stu-id="b9791-118">After the service has started, navigate to the \WCF\Basic\Discovery\AsyncFind\CS\client\bin\Debug or WCF\Basic\Discovery\AsyncFind\VB\client\bin\Debug directory and run Client.exe.</span></span>  
  
5.  <span data-ttu-id="b9791-119">Notez que le client est en mesure de trouver et d'appeler le service.</span><span class="sxs-lookup"><span data-stu-id="b9791-119">Observe the client is able to locate and call the service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b9791-120">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b9791-120">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b9791-121">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b9791-121">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b9791-122">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="b9791-122">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b9791-123">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="b9791-123">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\AsyncFind`  
  
## <a name="see-also"></a><span data-ttu-id="b9791-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9791-124">See Also</span></span>
