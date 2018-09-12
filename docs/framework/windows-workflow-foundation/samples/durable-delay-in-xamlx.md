---
title: Délai durable en XAMLX
ms.date: 03/30/2017
ms.assetid: efc38df4-2d34-453c-8e59-2c21d1307354
ms.openlocfilehash: 1eef9211c67d190ecb5f329c481fa2e3d1763353
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44708679"
---
# <a name="durable-delay-in-xamlx"></a><span data-ttu-id="bcf44-102">Délai durable en XAMLX</span><span class="sxs-lookup"><span data-stu-id="bcf44-102">Durable Delay in XAMLX</span></span>
<span data-ttu-id="bcf44-103">Cet exemple montre comment utiliser un délai durable, qui est un délai rendant le workflow persistant sur un périphérique durable pendant le délai.</span><span class="sxs-lookup"><span data-stu-id="bcf44-103">This sample demonstrates how to use a durable delay, which is a delay that persists the workflow to a durable device during the delay.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="bcf44-104">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcf44-104">The samples may already be installed on your machine.</span></span> <span data-ttu-id="bcf44-105">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="bcf44-105">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="bcf44-106">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="bcf44-106">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="bcf44-107">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="bcf44-107">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlx`  
  
## <a name="discussion"></a><span data-ttu-id="bcf44-108">Discussion</span><span class="sxs-lookup"><span data-stu-id="bcf44-108">Discussion</span></span>  
 <span data-ttu-id="bcf44-109">L'exemple de workflow contient deux messages sur un fichier local qui sont séparés par un délai.</span><span class="sxs-lookup"><span data-stu-id="bcf44-109">The sample workflow contains two messages to a local file that are separated by a delay.</span></span> <span data-ttu-id="bcf44-110">Lorsque le délai est déclenché, le workflow est déchargé, et attend 5 secondes dans le magasin d'instances de workflow avant d'être rechargé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bcf44-110">When the delay is triggered, the workflow is unloaded and waits 5 seconds in the workflow instance store before being reloaded in memory.</span></span>  
  
 <span data-ttu-id="bcf44-111">Le fichier .xamlx est un service de workflow est hébergé dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bcf44-111">The .xamlx file is a workflow service that is hosted in Visual Studio.</span></span> <span data-ttu-id="bcf44-112">Visual Studio utilise Cassini qui utilise un service de workflow hôte pour héberger le flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bcf44-112">Visual Studio uses Cassini that uses a workflow service host to host the workflow.</span></span>  
  
 <span data-ttu-id="bcf44-113">En plus d'héberger le workflow, l'hôte de service de workflow gère les instances de workflow en les chargeant et en les déchargeant.</span><span class="sxs-lookup"><span data-stu-id="bcf44-113">In addition to hosting the workflow, the workflow service host manages the workflow instances by loading and unloading them.</span></span> <span data-ttu-id="bcf44-114">Pour démarrer une instance de la définition de Windows Workflow Foundation (WF) (sur l’hôte de service de flux de travail), définissez un client qui envoie un message à la <xref:System.ServiceModel.Activities.Receive> activité dans le flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bcf44-114">To start an instance of the Windows Workflow Foundation (WF) definition (on the workflow service host), set a client that sends a message to the <xref:System.ServiceModel.Activities.Receive> activity in the workflow.</span></span> <span data-ttu-id="bcf44-115">Ce <xref:System.ServiceModel.Activities.Receive> a sa propriété <xref:System.ServiceModel.Activities.Receive.CanCreateInstance%2A> qui a la valeur `true`, ce qui lui permet de créer une instance du workflow une fois qu'il reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="bcf44-115">This <xref:System.ServiceModel.Activities.Receive> has its <xref:System.ServiceModel.Activities.Receive.CanCreateInstance%2A> property set to `true`, enabling it to create a new instance of the workflow once it receives a message.</span></span>  
  
 <span data-ttu-id="bcf44-116">Pendant l'initialisation, un comportement de déchargement d'instance est ajouté au fichier de configuration qui spécifie l'hôte de service de workflow sous lequel il doit décharger une instance dans le magasin de persistance (base de données).</span><span class="sxs-lookup"><span data-stu-id="bcf44-116">During initialization, an unload instance behavior is added to the configuration file that specifies to the workflow service host under which it should unload an instance to the persistence store (database).</span></span> <span data-ttu-id="bcf44-117">Pour cet exemple, il décharge l'instance immédiatement après le passage du workflow à l'état inactif (lorsque le délai est déclenché).</span><span class="sxs-lookup"><span data-stu-id="bcf44-117">For this sample, it unloads the instance immediately after the workflow goes idle (when the delay is triggered).</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="bcf44-118">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="bcf44-118">To use this sample</span></span>  
  
1.  <span data-ttu-id="bcf44-119">Ouvrez une invite de commandes [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="bcf44-119">Open a [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] command prompt.</span></span>  
  
2.  <span data-ttu-id="bcf44-120">Naviguez jusqu'au dossier DurableDelayXamlx\CS.</span><span class="sxs-lookup"><span data-stu-id="bcf44-120">Navigate to the DurableDelayXamlx\CS folder.</span></span>  
  
3.  <span data-ttu-id="bcf44-121">Exécutez Setup.cmd.</span><span class="sxs-lookup"><span data-stu-id="bcf44-121">Run Setup.cmd.</span></span>  
  
4.  <span data-ttu-id="bcf44-122">Exécutez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] en tant qu'administrateur.</span><span class="sxs-lookup"><span data-stu-id="bcf44-122">Run [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] as an administrator.</span></span>  
  
5.  <span data-ttu-id="bcf44-123">Ouvrez le fichier solution DurableDelayXamlx.sln.</span><span class="sxs-lookup"><span data-stu-id="bcf44-123">Open the DurableDelayXamlx.sln solution file.</span></span>  
  
6.  <span data-ttu-id="bcf44-124">Dans **l’Explorateur de solutions**, avec le bouton droit de la solution et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bcf44-124">In **Solution Explorer**, right-click the solution and select **Properties**.</span></span>  
  
7.  <span data-ttu-id="bcf44-125">Sélectionnez **plusieurs projets de démarrage** et définissez les deux projets sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="bcf44-125">Select **Multiple startup projects** and set both projects to **Start**.</span></span>  
  
8.  <span data-ttu-id="bcf44-126">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="bcf44-126">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
9. <span data-ttu-id="bcf44-127">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="bcf44-127">To run the solution, press CTRL+F5.</span></span>  
  
#### <a name="to-uninstall-this-sample"></a><span data-ttu-id="bcf44-128">Pour désinstaller cet exemple</span><span class="sxs-lookup"><span data-stu-id="bcf44-128">To uninstall this sample</span></span>  
  
1.  <span data-ttu-id="bcf44-129">Ouvrez une invite de commandes [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="bcf44-129">Open a [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] command prompt.</span></span>  
  
2.  <span data-ttu-id="bcf44-130">Naviguez jusqu'au dossier DurableDelayXamlx\CS.</span><span class="sxs-lookup"><span data-stu-id="bcf44-130">Navigate to the DurableDelayXamlx\CS folder.</span></span>  
  
3.  <span data-ttu-id="bcf44-131">Exécutez Cleanup.cmd.</span><span class="sxs-lookup"><span data-stu-id="bcf44-131">Run Cleanup.cmd.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="bcf44-132">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcf44-132">The samples may already be installed on your machine.</span></span> <span data-ttu-id="bcf44-133">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="bcf44-133">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="bcf44-134">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="bcf44-134">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="bcf44-135">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="bcf44-135">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\DurableDelayXamlX`
