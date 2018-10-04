---
title: WCF Services et suivi d'événements Windows
ms.date: 03/30/2017
ms.assetid: eda4355d-0bd0-4dc9-80a2-d2c832152272
ms.openlocfilehash: 26ce5fcb07b06a52f69ad8655adea563c177b055
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48266869"
---
# <a name="wcf-services-and-event-tracing-for-windows"></a><span data-ttu-id="9e272-102">WCF Services et suivi d'événements Windows</span><span class="sxs-lookup"><span data-stu-id="9e272-102">WCF Services and Event Tracing for Windows</span></span>
<span data-ttu-id="9e272-103">Cet exemple montre comment utiliser le traçage analytique dans Windows Communication Foundation (WCF) pour émettre des événements Event Tracing for Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="9e272-103">This sample demonstrates how to use the analytic tracing in Windows Communication Foundation (WCF) to emit events in Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="9e272-104">Les traces analytiques sont des événements émis à des points clés dans la pile de WCF qui permettent la résolution des problèmes des services WCF dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="9e272-104">The analytic traces are events emitted at key points in the WCF stack that allow troubleshooting of WCF services in production environment.</span></span>

 <span data-ttu-id="9e272-105">Trace analytique dans les services WCF qui est le suivi peut être activé dans un environnement de production avec un impact minimal sur les performances.</span><span class="sxs-lookup"><span data-stu-id="9e272-105">Analytic trace in WCF services is tracing that can be turned on in a production environment with minimal impact on performance.</span></span> <span data-ttu-id="9e272-106">Ces traces sont émises en tant qu'événements dans une session de suivi ETW.</span><span class="sxs-lookup"><span data-stu-id="9e272-106">These traces are emitted as events to an ETW session.</span></span>

 <span data-ttu-id="9e272-107">Cet exemple inclut un service WCF de base dans lequel les événements sont émis à partir du service dans le journal des événements, qui peut être affiché à l’aide de l’Observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-107">This sample includes a basic WCF service in which events are emitted from the service to the event log, which can be viewed using Event Viewer.</span></span> <span data-ttu-id="9e272-108">Il est également possible de démarrer une session ETW dédiée qui écoute les événements à partir du service WCF.</span><span class="sxs-lookup"><span data-stu-id="9e272-108">It is also possible to start a dedicated ETW session that listens for events from the WCF service.</span></span> <span data-ttu-id="9e272-109">L'exemple comprend un script permettant de créer une session de suivi ETW dédiée qui stocke des événements dans un fichier binaire pouvant être lu à l'aide de l'Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-109">The sample includes a script to create a dedicated ETW session that stores events in a binary file that can be read using Event Viewer.</span></span>

#### <a name="to-use-this-sample"></a><span data-ttu-id="9e272-110">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="9e272-110">To use this sample</span></span>

1.  <span data-ttu-id="9e272-111">À l’aide de Visual Studio 2012, ouvrez le fichier solution EtwAnalyticTraceSample.sln.</span><span class="sxs-lookup"><span data-stu-id="9e272-111">Using Visual Studio 2012, open the EtwAnalyticTraceSample.sln solution file.</span></span>

2.  <span data-ttu-id="9e272-112">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="9e272-112">To build the solution, press CTRL+SHIFT+B.</span></span>

3.  <span data-ttu-id="9e272-113">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="9e272-113">To run the solution, press CTRL+F5.</span></span>

     <span data-ttu-id="9e272-114">Dans le navigateur Web, cliquez sur **Calculator.svc**.</span><span class="sxs-lookup"><span data-stu-id="9e272-114">In the Web browser, click **Calculator.svc**.</span></span> <span data-ttu-id="9e272-115">L'URI du document WSDL du service doit s'afficher dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="9e272-115">The URI of the WSDL document for the service should appear in the browser.</span></span> <span data-ttu-id="9e272-116">Copiez cet URI.</span><span class="sxs-lookup"><span data-stu-id="9e272-116">Copy that URI.</span></span>

     <span data-ttu-id="9e272-117">Par défaut, le service commence à écouter les demandes sur le port 1378 (http://localhost:1378/Calculator.svc).</span><span class="sxs-lookup"><span data-stu-id="9e272-117">By default, the service starts listening for requests on port 1378 (http://localhost:1378/Calculator.svc).</span></span>

4.  <span data-ttu-id="9e272-118">Exécutez le client de test WCF (WcfTestClient.exe).</span><span class="sxs-lookup"><span data-stu-id="9e272-118">Run the WCF test client (WcfTestClient.exe).</span></span>

     <span data-ttu-id="9e272-119">Le client de test WCF (WcfTestClient.exe) se trouve dans le \<Visual Studio 2012 Répertoire_installation > \Common7\IDE\ WcfTestClient.exe (le répertoire d’installation Visual Studio 2012 par défaut est C:\Program Files\Microsoft Visual Studio 10.0).</span><span class="sxs-lookup"><span data-stu-id="9e272-119">The WCF test client (WcfTestClient.exe) is located in the \<Visual Studio 2012 Install Dir>\Common7\IDE\ WcfTestClient.exe (default Visual Studio 2012 install dir is C:\Program Files\Microsoft Visual Studio 10.0).</span></span>

5.  <span data-ttu-id="9e272-120">Dans le client test WCF, ajoutez le service en sélectionnant **fichier**, puis **ajouter un Service**.</span><span class="sxs-lookup"><span data-stu-id="9e272-120">Within the WCF test client, add the service by selecting **File**, and then **Add Service**.</span></span>

     <span data-ttu-id="9e272-121">Ajoutez l'adresse du point de terminaison dans la zone d'entrée.</span><span class="sxs-lookup"><span data-stu-id="9e272-121">Add the endpoint address in the input box.</span></span> <span data-ttu-id="9e272-122">La valeur par défaut est http://localhost:1378/Calculator.svc.</span><span class="sxs-lookup"><span data-stu-id="9e272-122">The default is http://localhost:1378/Calculator.svc.</span></span>

6.  <span data-ttu-id="9e272-123">Ouvrez l'application Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-123">Open the Event Viewer application.</span></span>

     <span data-ttu-id="9e272-124">Avant d’appeler le service, démarrez l’Observateur d’événements et vérifiez que le journal des événements écoute les événements de suivi émis à partir du service WCF.</span><span class="sxs-lookup"><span data-stu-id="9e272-124">Before invoking the service, start Event Viewer and ensure that the event log is listening for tracking events emitted from the WCF service.</span></span>

7.  <span data-ttu-id="9e272-125">À partir de la **Démarrer** menu, sélectionnez **outils d’administration**, puis **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="9e272-125">From the **Start** menu, select **Administrative Tools**, and then **Event Viewer**.</span></span>  <span data-ttu-id="9e272-126">Activer la **analyse** et **déboguer** journaux.</span><span class="sxs-lookup"><span data-stu-id="9e272-126">Enable the **Analytic** and **Debug** logs.</span></span>

8.  <span data-ttu-id="9e272-127">Dans l’arborescence de commandes dans l’Observateur d’événements, accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="9e272-127">In the tree view in Event Viewer, navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="9e272-128">Avec le bouton droit **serveur d’applications-Applications**, sélectionnez **vue**, puis **afficher les journaux d’analyse et de débogage**.</span><span class="sxs-lookup"><span data-stu-id="9e272-128">Right-click **Application Server-Applications**, select **View**, and then **Show Analytic and Debug Logs**.</span></span>

     <span data-ttu-id="9e272-129">Vérifiez que le **afficher les journaux d’analyse et de débogage** option est activée.</span><span class="sxs-lookup"><span data-stu-id="9e272-129">Ensure that the **Show Analytic and Debug Logs** option is checked.</span></span>

9. <span data-ttu-id="9e272-130">Activer la **analyse** journal.</span><span class="sxs-lookup"><span data-stu-id="9e272-130">Enable the **Analytic** log.</span></span>

     <span data-ttu-id="9e272-131">Dans l’arborescence de commandes dans l’Observateur d’événements, accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="9e272-131">In the tree view in Event Viewer, navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="9e272-132">Avec le bouton droit **analyse** et sélectionnez **activer le journal**.</span><span class="sxs-lookup"><span data-stu-id="9e272-132">Right-click **Analytic** and select **Enable Log**.</span></span>

#### <a name="to-test-the-service"></a><span data-ttu-id="9e272-133">Pour tester le service</span><span class="sxs-lookup"><span data-stu-id="9e272-133">To test the service</span></span>

1.  <span data-ttu-id="9e272-134">Basculez vers le client test WCF et double-cliquez sur `Divide` et conservez les valeurs par défaut, qui spécifient le dénominateur 0.</span><span class="sxs-lookup"><span data-stu-id="9e272-134">Switch back to WCF test client and double-click `Divide` and keep the default values, which specify a denominator of 0.</span></span>

     <span data-ttu-id="9e272-135">Si le dénominateur est 0, le service génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="9e272-135">If the denominator is 0, then the service throws a fault.</span></span>

2.  <span data-ttu-id="9e272-136">Observez les événements émis par le service.</span><span class="sxs-lookup"><span data-stu-id="9e272-136">Observe the events emitted from the service.</span></span>

     <span data-ttu-id="9e272-137">Revenez à l’Observateur d’événements et accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="9e272-137">Switch back to Event Viewer and navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application Server-Applications**.</span></span> <span data-ttu-id="9e272-138">Avec le bouton droit **analyse** et sélectionnez **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="9e272-138">Right-click **Analytic** and select **Refresh**.</span></span>

     <span data-ttu-id="9e272-139">Les événements du traçage analytique de WCF s'affichent dans l'Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-139">The WCF analytic trace events are displayed in the event viewer.</span></span> <span data-ttu-id="9e272-140">Notez qu'en raison de l'erreur générée par le service, un événement de trace d'erreur est visible dans l'Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-140">Notice that because a fault was thrown by the service an error trace event is displayed in the event viewer.</span></span>

3.  <span data-ttu-id="9e272-141">Répétez les étapes 1 et 2, mais avec des entrées valides.</span><span class="sxs-lookup"><span data-stu-id="9e272-141">Repeat steps 1 and 2, but with valid inputs.</span></span> <span data-ttu-id="9e272-142">La valeur du paramètre `N2` peut être n'importe quel nombre différent de 0.</span><span class="sxs-lookup"><span data-stu-id="9e272-142">The value of the `N2` parameter can be any number other than 0.</span></span>

     <span data-ttu-id="9e272-143">Actualisez le canal analytique pour constater que les événements WCF n'incluent aucun événement d'erreur.</span><span class="sxs-lookup"><span data-stu-id="9e272-143">Refresh the analytic channel to view the WCF events do not include any error events.</span></span>

 <span data-ttu-id="9e272-144">L'exemple montre les événements de trace analytique émis par un service WCF.</span><span class="sxs-lookup"><span data-stu-id="9e272-144">The sample demonstrates the analytic trace events emitted from a WCF service.</span></span>

#### <a name="to-cleanup-optional"></a><span data-ttu-id="9e272-145">Pour effectuer un nettoyage (facultatif)</span><span class="sxs-lookup"><span data-stu-id="9e272-145">To cleanup (Optional)</span></span>

1.  <span data-ttu-id="9e272-146">Ouvrez l'observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-146">Open Event Viewer.</span></span>

2.  <span data-ttu-id="9e272-147">Accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis  **Serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="9e272-147">Navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application-Server-Applications**.</span></span> <span data-ttu-id="9e272-148">Avec le bouton droit **analyse** et sélectionnez **désactiver le journal**.</span><span class="sxs-lookup"><span data-stu-id="9e272-148">Right-click **Analytic** and select **Disable Log**.</span></span>

3.  <span data-ttu-id="9e272-149">Accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis  **Serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="9e272-149">Navigate to **Event Viewer**, **Applications and Services Logs**, **Microsoft**, **Windows**, and then **Application-Server-Applications**.</span></span> <span data-ttu-id="9e272-150">Avec le bouton droit **analyse** et sélectionnez **effacer le journal**.</span><span class="sxs-lookup"><span data-stu-id="9e272-150">Right-click **Analytic** and select **Clear Log**.</span></span>

4.  <span data-ttu-id="9e272-151">Choisissez le **effacer** option pour effacer les événements.</span><span class="sxs-lookup"><span data-stu-id="9e272-151">Choose the **Clear** option to clear the events.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="9e272-152">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9e272-152">The samples may already be installed on your computer.</span></span> <span data-ttu-id="9e272-153">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="9e272-153">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="9e272-154">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="9e272-154">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9e272-155">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="9e272-155">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\ETWTracing`  
  
## <a name="see-also"></a><span data-ttu-id="9e272-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e272-156">See Also</span></span>  
 [<span data-ttu-id="9e272-157">Exemples d’analyse AppFabric</span><span class="sxs-lookup"><span data-stu-id="9e272-157">AppFabric Monitoring Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=193959)
