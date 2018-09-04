---
title: Canaux WCF prenant en charge ReceiveContext
ms.date: 03/30/2017
ms.assetid: d990d119-7321-4b8c-852b-10256f59f9b0
ms.openlocfilehash: d7f80d0874606129876fbf7dfa30c0327680b922
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515928"
---
# <a name="receivecontext-enabled-wcf-channels"></a><span data-ttu-id="c25fd-102">Canaux WCF prenant en charge ReceiveContext</span><span class="sxs-lookup"><span data-stu-id="c25fd-102">ReceiveContext-Enabled WCF Channels</span></span>
<span data-ttu-id="c25fd-103">Cet exemple montre l'utilité de canaux WCF prenant en charge <xref:System.ServiceModel.Channels.ReceiveContext>.</span><span class="sxs-lookup"><span data-stu-id="c25fd-103">This sample demonstrates the usefulness of <xref:System.ServiceModel.Channels.ReceiveContext>-enabled WCF channels.</span></span> <span data-ttu-id="c25fd-104">L'exemple implémente un service pour rechercher le produit de deux nombres à l'aide d'un canal NetMSMQ.</span><span class="sxs-lookup"><span data-stu-id="c25fd-104">The sample implements a service to find the product of two numbers using a NetMSMQ channel.</span></span>  
  
 <span data-ttu-id="c25fd-105">La classe <xref:System.ServiceModel.Channels.ReceiveContext> permet à une application de décider s'il faut accéder au message ou le laisser dans la file d'attente pour un traitement supplémentaire, même une fois le contenu du message inspecté.</span><span class="sxs-lookup"><span data-stu-id="c25fd-105">The <xref:System.ServiceModel.Channels.ReceiveContext> class enables an application to decide whether to access the message or leave it in the queue for further processing, even after the contents of the message have been inspected.</span></span> <span data-ttu-id="c25fd-106">Dans cet exemple, un client envoie des entiers aléatoires à une file d'attente transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="c25fd-106">In this sample, a client sends random integers to a transactional queue.</span></span> <span data-ttu-id="c25fd-107">Le service `ProductCalculator` reçoit les messages et en inspecte le contenu, en l'occurrence, des entiers, afin de déterminer si le produit peut être calculé.</span><span class="sxs-lookup"><span data-stu-id="c25fd-107">The `ProductCalculator` service receives the messages and inspects the message contents, which are integers, to determine whether the product can be computed.</span></span> <span data-ttu-id="c25fd-108">Si l'opération réalisée par le service ne calcule pas le produit, le message est remis en file d'attente et peut à nouveau être reçu par le service qui écoute la file d'attente.</span><span class="sxs-lookup"><span data-stu-id="c25fd-108">If the service operation does not compute the product, the message is put back into the queue and can be received again by the service listening on the queue.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="c25fd-109">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c25fd-109">The samples may already be installed on your computer.</span></span> <span data-ttu-id="c25fd-110">Recherchez le répertoire (par défaut) suivant avant de continuer :</span><span class="sxs-lookup"><span data-stu-id="c25fd-110">Check for the following (default) directory before continuing:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="c25fd-111">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="c25fd-111">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="c25fd-112">Cet exemple se trouve dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="c25fd-112">This sample is located in the following directory:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Net\MSMQ\ReceiveContextProductGenerator`  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="c25fd-113">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="c25fd-113">To use this sample</span></span>  
  
1.  <span data-ttu-id="c25fd-114">Vérifiez que Microsoft Message Queuing (MSMQ) est installé.</span><span class="sxs-lookup"><span data-stu-id="c25fd-114">Ensure that Microsoft Message Queuing (MSMQ) is installed.</span></span>  
  
    1.  <span data-ttu-id="c25fd-115">Pour installer MSMQ sur [!INCLUDE[lserver](../../../../includes/lserver-md.md)] :</span><span class="sxs-lookup"><span data-stu-id="c25fd-115">To install MSMQ on [!INCLUDE[lserver](../../../../includes/lserver-md.md)]:</span></span>  
  
        1.  <span data-ttu-id="c25fd-116">Dans **le Gestionnaire de serveur**, cliquez sur **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-116">In **Server Manager**, click **Features**.</span></span>  
  
        2.  <span data-ttu-id="c25fd-117">Dans le volet droit sous **résumé des fonctionnalités**, cliquez sur **ajouter des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-117">In the right pane under **Features Summary**, click **Add Features**.</span></span>  
  
        3.  <span data-ttu-id="c25fd-118">Dans la fenêtre résultante, développez **Message Queuing**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-118">In the resulting window, expand **Message Queuing**.</span></span>  
  
        4.  <span data-ttu-id="c25fd-119">Développez **Services de file d’attente de messages**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-119">Expand **Message Queuing Services**.</span></span>  
  
        5.  <span data-ttu-id="c25fd-120">Cliquez sur **intégration de Services d’annuaire** (pour les ordinateurs joints à un domaine), puis cliquez sur **prise en charge HTTP**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-120">Click **Directory Services Integration** (for computers joined to a domain), and then click **HTTP Support**.</span></span>  
  
        6.  <span data-ttu-id="c25fd-121">Cliquez sur **suivant**, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-121">Click **Next**, and then click **Install**.</span></span>  
  
    2.  <span data-ttu-id="c25fd-122">Pour installer MSMQ sur [!INCLUDE[wv](../../../../includes/wv-md.md)] :</span><span class="sxs-lookup"><span data-stu-id="c25fd-122">To install MSMQ on [!INCLUDE[wv](../../../../includes/wv-md.md)]:</span></span>  
  
        1.  <span data-ttu-id="c25fd-123">Ouvrez le **Panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-123">Open **Control Panel**.</span></span>  
  
        2.  <span data-ttu-id="c25fd-124">Cliquez sur **programmes** puis, sous **programmes et fonctionnalités**, cliquez sur **activer et désactiver des fonctionnalités Windows**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-124">Click **Programs** and then, under **Programs and Features**, click **Turn Windows Features on and off**.</span></span>  
  
        3.  <span data-ttu-id="c25fd-125">Développez **Microsoft Message Queue Server (MSMQ)**, développez **Microsoft Message Queue (MSMQ) Server Core**, puis sélectionnez les cases à cocher pour les fonctionnalités suivantes de Message Queuing à installer :</span><span class="sxs-lookup"><span data-stu-id="c25fd-125">Expand **Microsoft Message Queue (MSMQ) Server**, expand **Microsoft Message Queue (MSMQ) Server Core**, and then select the check boxes for the following Message Queuing features to install:</span></span>  
  
            -   <span data-ttu-id="c25fd-126">Serveur Message Queuing</span><span class="sxs-lookup"><span data-stu-id="c25fd-126">Message Queuing Server</span></span>  
  
            -   <span data-ttu-id="c25fd-127">Intégration des services de domaine Active Directory MSMQ (pour les ordinateurs liés à un domaine).</span><span class="sxs-lookup"><span data-stu-id="c25fd-127">MSMQ Active Directory Domain Services Integration (for computers joined to a domain)</span></span>  
  
            -   <span data-ttu-id="c25fd-128">Prise en charge HTTP MSMQ</span><span class="sxs-lookup"><span data-stu-id="c25fd-128">MSMQ HTTP Support</span></span>  
  
        4.  <span data-ttu-id="c25fd-129">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c25fd-129">Click **OK**.</span></span>  
  
        5.  <span data-ttu-id="c25fd-130">Si vous êtes invité à redémarrer l’ordinateur, cliquez sur **OK** pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="c25fd-130">If you are prompted to restart the computer, click **OK** to complete the installation.</span></span>  
  
2.  <span data-ttu-id="c25fd-131">Assurez-vous que [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] est installé sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c25fd-131">Ensure that [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] is installed on the computer.</span></span>  
  
3.  <span data-ttu-id="c25fd-132">À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier solution ReceiveContextProductGenerator.sln.</span><span class="sxs-lookup"><span data-stu-id="c25fd-132">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the ReceiveContextProductGenerator.sln solution file.</span></span>  
  
4.  <span data-ttu-id="c25fd-133">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="c25fd-133">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
5.  <span data-ttu-id="c25fd-134">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="c25fd-134">To run the solution, press CTRL+F5.</span></span>
