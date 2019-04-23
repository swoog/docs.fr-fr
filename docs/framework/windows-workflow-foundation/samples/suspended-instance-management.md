---
title: Gestion de l'instance interrompue
ms.date: 03/30/2017
ms.assetid: f5ca3faa-ba1f-4857-b92c-d927e4b29598
ms.openlocfilehash: ace4d2baef8f6b030790deaa5b1c20bb4b0cd30d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59319558"
---
# <a name="suspended-instance-management"></a><span data-ttu-id="7cfa8-102">Gestion de l'instance interrompue</span><span class="sxs-lookup"><span data-stu-id="7cfa8-102">Suspended Instance Management</span></span>
<span data-ttu-id="7cfa8-103">Cet exemple montre comment gérer des instances de workflow qui ont été interrompues.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-103">This sample demonstrates how to manage workflow instances that have been suspended.</span></span>  <span data-ttu-id="7cfa8-104">L'action par défaut pour <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> est `AbandonAndSuspend`.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-104">The default action for <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> is `AbandonAndSuspend`.</span></span> <span data-ttu-id="7cfa8-105">Cela signifie que, par défaut, les exceptions non gérées levées à partir d'une instance de workflow hébergée dans le <xref:System.ServiceModel.WorkflowServiceHost> provoqueront la suppression de l'instance de la mémoire (abandon), et la version durable/persistante de l'instance sera marquée comme interrompue.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-105">This means that by default, unhandled exceptions thrown from a workflow instance hosted in the <xref:System.ServiceModel.WorkflowServiceHost> will cause the instance to be disposed from memory (abandoned) and the durable/persisted version of the instance to be marked as suspended.</span></span> <span data-ttu-id="7cfa8-106">Une instance de workflow interrompue ne sera pas en mesure de fonctionner tant que l'interruption n'a pas été annulée.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-106">A suspended workflow instance will not be able to run until it has been unsuspended.</span></span>

 <span data-ttu-id="7cfa8-107">L'exemple montre comment un utilitaire en ligne de commande peut être implémenté pour rechercher des instances interrompues et comment permettre à l'utilisateur de reprendre ou de terminer l'instance.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-107">The sample shows how a command-line utility can be implemented to query for suspended instances, and how to give the user the option to resume or terminate the instance.</span></span> <span data-ttu-id="7cfa8-108">Dans cet exemple, un service de workflow lève une exception intentionnellement, ce qui provoque son interruption.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-108">In this sample, a workflow service intentionally throws an exception, causing it to become suspended.</span></span> <span data-ttu-id="7cfa8-109">L'utilitaire en ligne de command peut ensuite être utilisé pour rechercher l'instance et, par la suite, la reprendre ou la terminer.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-109">The command-line utility can then be used to query for the instance and subsequently resume or terminate the instance.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="7cfa8-110">Démonstrations</span><span class="sxs-lookup"><span data-stu-id="7cfa8-110">Demonstrates</span></span>
 <span data-ttu-id="7cfa8-111"><xref:System.ServiceModel.WorkflowServiceHost> avec <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> et <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> dans Windows Workflow Foundation (WF).</span><span class="sxs-lookup"><span data-stu-id="7cfa8-111"><xref:System.ServiceModel.WorkflowServiceHost> with <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> and <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> in Windows Workflow Foundation (WF).</span></span>

## <a name="discussion"></a><span data-ttu-id="7cfa8-112">Discussion</span><span class="sxs-lookup"><span data-stu-id="7cfa8-112">Discussion</span></span>
 <span data-ttu-id="7cfa8-113">L'utilitaire en ligne de commande implémenté dans cet exemple est spécifique à l'implémentation du magasin d'instances SQL fournie dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="7cfa8-113">The command-line utility implemented in this sample is specific to the SQL instance store implementation that ships in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span></span> <span data-ttu-id="7cfa8-114">Si vous avez une implémentation personnalisée du magasin d'instances, vous pouvez adapter cet utilitaire en remplaçant les implémentations `WorkflowInstanceCommand` dans l'exemple par des implémentations qui sont spécifiques à votre magasin d'instances.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-114">If you have a custom implementation of the instance store, then you can adapt this utility by replacing the `WorkflowInstanceCommand` implementations in the sample with implementations that are specific to your instance store.</span></span>

 <span data-ttu-id="7cfa8-115">L'implémentation fournie exécute directement des commandes SQL dans le magasin d'instances SQL pour répertorier les instances interrompues et s'appuie sur un <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> ajouté au <xref:System.ServiceModel.WorkflowServiceHost> pour reprendre ou terminer les instances.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-115">The provided implementation runs SQL commands against the SQL instance store directly to list suspended instances, and it relies on a <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> added to the <xref:System.ServiceModel.WorkflowServiceHost> in order to resume or terminate the instances.</span></span>

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="7cfa8-116">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="7cfa8-116">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="7cfa8-117">Cet exemple requiert que les composants Windows suivants soient activés :</span><span class="sxs-lookup"><span data-stu-id="7cfa8-117">This sample requires that the following Windows components are enabled:</span></span>

    1.  <span data-ttu-id="7cfa8-118">Serveur de file d'attente Microsoft Message Queue (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="7cfa8-118">Microsoft Message Queues (MSMQ) Server</span></span>

    2.  <span data-ttu-id="7cfa8-119">SQL Server Express</span><span class="sxs-lookup"><span data-stu-id="7cfa8-119">SQL Server Express</span></span>

2. <span data-ttu-id="7cfa8-120">Configurez la base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-120">Set up the SQL Server database.</span></span>

    1.  <span data-ttu-id="7cfa8-121">À partir d’une invite de commandes Visual Studio 2010, exécutez « setup.cmd » à partir de l’exemple suspendedinstancemanagement, qui effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7cfa8-121">From a Visual Studio 2010 command prompt, run "setup.cmd" from the SuspendedInstanceManagement sample directory, which does the following:</span></span>

        1.  <span data-ttu-id="7cfa8-122">Crée une base de données de persistance à l'aide de SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-122">Creates a persistence database using SQL Server Express.</span></span> <span data-ttu-id="7cfa8-123">Si la base de données de persistance existe déjà, elle est supprimée et recréée.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-123">If the persistence database already exists, then it is dropped and re-created</span></span>

        2.  <span data-ttu-id="7cfa8-124">Configure la base de données pour la persistance.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-124">Sets up the database for persistence.</span></span>

        3.  <span data-ttu-id="7cfa8-125">Ajoute IIS APPPOOL\DefaultAppPool et NT AUTHORITY\Network Service au rôle InstanceStoreUsers qui a été défini lors de la configuration de la base de données pour la persistance.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-125">Adds IIS APPPOOL\DefaultAppPool and NT AUTHORITY\Network Service to the InstanceStoreUsers role that was defined when setting up the database for persistence.</span></span>

3. <span data-ttu-id="7cfa8-126">Configurez la file d'attente de service.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-126">Set up the service queue.</span></span>

    1.  <span data-ttu-id="7cfa8-127">Dans Visual Studio 2010, cliquez sur le **SampleWorkflowApp** projet puis cliquez sur **définir comme projet de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-127">In Visual Studio 2010, right-click the **SampleWorkflowApp** project and click **Set as Startup Project**.</span></span>

    2.  <span data-ttu-id="7cfa8-128">Compilez et exécutez SampleWorkflowApp en appuyant sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-128">Compile and run the SampleWorkflowApp by pressing **F5**.</span></span> <span data-ttu-id="7cfa8-129">La file d'attente requise sera ainsi créée.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-129">This will create the required queue.</span></span>

    3.  <span data-ttu-id="7cfa8-130">Appuyez sur **entrée** pour arrêter SampleWorkflowApp.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-130">Press **Enter** to stop the SampleWorkflowApp.</span></span>

    4.  <span data-ttu-id="7cfa8-131">Ouvrez la console Gestion de l'ordinateur en exécutant Compmgmt.msc à partir d'une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-131">Open the Computer Management console by running Compmgmt.msc from a command prompt.</span></span>

    5.  <span data-ttu-id="7cfa8-132">Développez **Service et les Applications**, **Message Queuing**, **files d’attente privées**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-132">Expand **Service and Applications**, **Message Queuing**, **Private Queues**.</span></span>

    6.  <span data-ttu-id="7cfa8-133">Bouton droit sur le **ReceiveTx** de file d’attente et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-133">Right click the **ReceiveTx** queue and select **Properties**.</span></span>

    7.  <span data-ttu-id="7cfa8-134">Sélectionnez le **sécurité** onglet et autoriser **tout le monde** disposer d’autorisations à **recevoir un Message**, **lire le Message**, et  **Envoyer le Message**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-134">Select the **Security** tab and allow **Everyone** to have permissions to **Receive Message**, **Peek Message**, and **Send Message**.</span></span>

4. <span data-ttu-id="7cfa8-135">Exécutez maintenant l'exemple.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-135">Now, run the sample.</span></span>

    1.  <span data-ttu-id="7cfa8-136">Dans Visual Studio 2010, réexécutez le projet SampleWorkflowApp sans déboguer en appuyant sur **Ctrl + F5**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-136">In Visual Studio 2010, run the SampleWorkflowApp project again without debugging by pressing **Ctrl+F5**.</span></span> <span data-ttu-id="7cfa8-137">Deux adresses de point de terminaison seront imprimées dans la fenêtre de console : une pour le point de terminaison d'application et l'autre pour le <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-137">Two endpoint addresses will be printed in the console window: one for the application endpoint and then other from the <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>.</span></span> <span data-ttu-id="7cfa8-138">Une instance de workflow est ensuite créée et les enregistrements de suivi pour cette instance s'afficheront dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-138">A workflow instance is then created, and tracking records for that instance will appear in the console window.</span></span> <span data-ttu-id="7cfa8-139">L'instance de workflow lèvera une exception qui provoquera l'interruption et l'abandon de l'instance.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-139">The workflow instance will throw an exception causing the instance to be suspended and aborted.</span></span>

    2.  <span data-ttu-id="7cfa8-140">L'utilitaire en ligne de commande peut ensuite être utilisé pour entreprendre des actions supplémentaires sur chacune de ces instances.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-140">The command-line utility can then be used to take further action on any of these instances.</span></span> <span data-ttu-id="7cfa8-141">La syntaxe pour les arguments de ligne de commande est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7cfa8-141">The syntax for command line arguments is as follows::</span></span>

         `SuspendedInstanceManagement -Command:[CommandName] -Server:[ServerName] -Database:[DatabaseName] -InstanceId:[InstanceId]`

         <span data-ttu-id="7cfa8-142">Les commandes prises en charge sont `Query`, `Resume` et `Terminate`.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-142">The supported commands are: `Query`, `Resume`, and `Terminate`.</span></span>  <span data-ttu-id="7cfa8-143">Le commutateur InstanceId est uniquement obligatoire pour les opérations `Resume` et `Terminate`.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-143">The InstanceId switch is only required for `Resume` and `Terminate` operations.</span></span>

#### <a name="to-cleanup-optional"></a><span data-ttu-id="7cfa8-144">Pour effectuer un nettoyage (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7cfa8-144">To cleanup (Optional)</span></span>

1. <span data-ttu-id="7cfa8-145">Ouvrez la console Gestion de l'ordinateur en exécutant Compmgmt.msc à partir d'une invite de commandes `vs2010`.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-145">Open the Computer Management console by running Compmgmt.msc from a `vs2010` command prompt.</span></span>

2. <span data-ttu-id="7cfa8-146">Développez **Service et les Applications**, **Message Queuing**, **files d’attente privées**.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-146">Expand **Service and Applications**, **Message Queuing**, **Private Queues**.</span></span>

3. <span data-ttu-id="7cfa8-147">Supprimer le **ReceiveTx** file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-147">Delete the **ReceiveTx** queue.</span></span>

4. <span data-ttu-id="7cfa8-148">Pour supprimer la base de données de persistance, exécutez cleanup.cmd.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-148">To remove the persistence database, run cleanup.cmd.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="7cfa8-149">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-149">The samples may already be installed on your machine.</span></span> <span data-ttu-id="7cfa8-150">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-150">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="7cfa8-151">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-151">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="7cfa8-152">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="7cfa8-152">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Application\SuspendedInstanceManagement`
