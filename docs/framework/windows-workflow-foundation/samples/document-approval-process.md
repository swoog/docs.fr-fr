---
title: Processus d'approbation des documents
ms.date: 03/30/2017
ms.assetid: 9b240937-76a7-45cd-8823-7f82c34d03bd
ms.openlocfilehash: dfc2e0a12d053733823427ac50066b1e4a0f97aa
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59318466"
---
# <a name="document-approval-process"></a><span data-ttu-id="9f60b-102">Processus d'approbation des documents</span><span class="sxs-lookup"><span data-stu-id="9f60b-102">Document Approval Process</span></span>
<span data-ttu-id="9f60b-103">Cet exemple montre l’utilisation de nombreuses fonctionnalités de Windows Workflow Foundation (WF) et Windows Communication Foundation (WCF) ensemble.</span><span class="sxs-lookup"><span data-stu-id="9f60b-103">This sample demonstrates the use of many Windows Workflow Foundation (WF) and Windows Communication Foundation (WCF) features together.</span></span> <span data-ttu-id="9f60b-104">Ensemble, elles implémentent un scénario de processus d'approbation des documents.</span><span class="sxs-lookup"><span data-stu-id="9f60b-104">Together they implement a document approval process scenario.</span></span> <span data-ttu-id="9f60b-105">Une application cliente peut soumettre des documents pour approbation et approuver des documents.</span><span class="sxs-lookup"><span data-stu-id="9f60b-105">A client application can submit documents for approval and approve documents.</span></span> <span data-ttu-id="9f60b-106">Une application du responsable des approbations existe pour faciliter les communications entre les clients et mettre en vigueur les règles du processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-106">An approval manager application exists to facilitate communications between clients and to enforce the rules of the approval process.</span></span> <span data-ttu-id="9f60b-107">Le processus d'approbation est un workflow qui peut exécuter plusieurs types d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-107">The approval process is a workflow that can execute several types of approval.</span></span> <span data-ttu-id="9f60b-108">Il existe des activités pour obtenir une approbation unique, une approbation de quorum (pourcentage de l'ensemble d'approbateurs) et un processus d'approbation complexe qui se compose d'une approbation unique et de quorum dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="9f60b-108">Activities exist to get a single approval, a quorum approval (a percentage of set of approvers), and a complex approval process that consists of a quorum and single approval in a sequence.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="9f60b-109">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-109">The samples may already be installed on your machine.</span></span> <span data-ttu-id="9f60b-110">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="9f60b-110">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="9f60b-111">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="9f60b-111">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9f60b-112">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="9f60b-112">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Application\DocumentApprovalProcess`  
  
## <a name="sample-details"></a><span data-ttu-id="9f60b-113">Détails de l'exemple</span><span class="sxs-lookup"><span data-stu-id="9f60b-113">Sample Details</span></span>  
 <span data-ttu-id="9f60b-114">Le graphique suivant illustre le flux de travail du processus d’approbation document :</span><span class="sxs-lookup"><span data-stu-id="9f60b-114">The following graphic demonstrates the document approval process workflow:</span></span>  
  
 ![Flux de travail du processus d'approbation d'un document](./media/document-approval-process/document-approval-process.jpg)  
  
 <span data-ttu-id="9f60b-116">Du point de vue du client, le processus d'approbation fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="9f60b-116">From the client's perspective, the approval process functions as follows:</span></span>  
  
1. <span data-ttu-id="9f60b-117">Un client s'abonne pour être un utilisateur dans le système du processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-117">A client subscribes to be a user in the approval process system.</span></span>  
  
2. <span data-ttu-id="9f60b-118">Un client WCF envoie à un service WCF hébergé par l’application de gestionnaire d’approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-118">A WCF client sends to a WCF service hosted by the approval manager application.</span></span>  
  
3. <span data-ttu-id="9f60b-119">Un ID d'utilisateur unique est retourné au client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-119">A unique user ID is returned to the client.</span></span> <span data-ttu-id="9f60b-120">Le client peut maintenant participer aux processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-120">The client can now participate in approval processes.</span></span>  
  
4. <span data-ttu-id="9f60b-121">Une fois joint, un client peut envoyer un document pour approbation à l'aide de processus d'approbation unique, de quorum ou complexe.</span><span class="sxs-lookup"><span data-stu-id="9f60b-121">Once joined, a client can send a document for approval using single, quorum or complex approval processes.</span></span>  
  
5. <span data-ttu-id="9f60b-122">Un clic sur un bouton dans l'interface du client permet de démarrer une instance de workflow dans un hôte du service de workflow client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-122">A button in the client’s interface is clicked, starting a workflow instance in a client Workflow Service Host.</span></span>  
  
6. <span data-ttu-id="9f60b-123">Le workflow envoie une demande d'approbation à l'application du responsable des approbations.</span><span class="sxs-lookup"><span data-stu-id="9f60b-123">The workflow sends an approval request to the approval manager application.</span></span>  
  
7. <span data-ttu-id="9f60b-124">Le gestionnaire de workflow démarre un workflow de son propre côté pour représenter un processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-124">The workflow manager starts a workflow on its own side to represent an approval process.</span></span>  
  
8. <span data-ttu-id="9f60b-125">Une fois le workflow d'approbation du responsable exécuté, les résultats sont renvoyés au client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-125">Once the manager approval workflow executes, the results are sent back to the client.</span></span>  
  
9. <span data-ttu-id="9f60b-126">Le client affiche les résultats.</span><span class="sxs-lookup"><span data-stu-id="9f60b-126">The client displays the results.</span></span>  
  
10. <span data-ttu-id="9f60b-127">Un client peut recevoir une demande d'approbation et y répondre à tout moment.</span><span class="sxs-lookup"><span data-stu-id="9f60b-127">A client may receive an approval request and respond to the request at any point in time.</span></span>  
  
11. <span data-ttu-id="9f60b-128">Un service WCF hébergé sur le client peut recevoir une demande d’approbation à partir du Gestionnaire d’approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-128">A WCF service hosted on the client can receive an approval request from the approval manager application.</span></span>  
  
12. <span data-ttu-id="9f60b-129">Les informations concernant les documents sont présentées sur le client à des fins de revue.</span><span class="sxs-lookup"><span data-stu-id="9f60b-129">The document information is presented on the client for review.</span></span>  
  
13. <span data-ttu-id="9f60b-130">L'utilisateur peut approuver ou rejeter le document.</span><span class="sxs-lookup"><span data-stu-id="9f60b-130">The user can approve or reject the document.</span></span>  
  
14. <span data-ttu-id="9f60b-131">Un client WCF est utilisé pour envoyer une réponse d’approbation à l’application de gestionnaire d’approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-131">A WCF client is used to send an approval response back to the approval manager application.</span></span>  
  
 <span data-ttu-id="9f60b-132">Du point de vue de l'application du responsable des approbations, le processus d'approbation fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="9f60b-132">From the approval manager application’s point of view, the approval process functions as follows:</span></span>  
  
1. <span data-ttu-id="9f60b-133">Un client demande à participer au système du processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-133">A client requests to participate to the approval process system.</span></span>  
  
2. <span data-ttu-id="9f60b-134">Un service WCF sur le responsable des approbations reçoit une demande de faire partie du système de processus d’approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-134">A WCF service on the approval manager receives a request to be part of the approval process system.</span></span>  
  
3. <span data-ttu-id="9f60b-135">Un ID unique est généré pour le client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-135">A unique ID is generated for the client.</span></span> <span data-ttu-id="9f60b-136">Les informations utilisateur sont stockées dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="9f60b-136">The user information is stored in a database.</span></span>  
  
4. <span data-ttu-id="9f60b-137">L'ID unique est renvoyé à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-137">The unique ID is sent back to the user.</span></span>  
  
5. <span data-ttu-id="9f60b-138">Une demande d'approbation est reçue.</span><span class="sxs-lookup"><span data-stu-id="9f60b-138">An approval request is receive.</span></span> <span data-ttu-id="9f60b-139">Le responsable des approbations exécute un processus d'approbation.</span><span class="sxs-lookup"><span data-stu-id="9f60b-139">The approval manager executes an approval process.</span></span>  
  
6. <span data-ttu-id="9f60b-140">Une demande d'approbation est reçue par le responsable des approbations, ce qui démarre un nouveau workflow.</span><span class="sxs-lookup"><span data-stu-id="9f60b-140">An approval request is received by the approval manager, starting a new workflow.</span></span>  
  
7. <span data-ttu-id="9f60b-141">Selon le type de demande (simple, quorum ou complexe), une activité différente est exécutée.</span><span class="sxs-lookup"><span data-stu-id="9f60b-141">Depending on the type of request (simple, quorum, or complex) a different activity is executed.</span></span>  
  
8. <span data-ttu-id="9f60b-142">Les activités Send et Receive avec corrélation sont utilisées pour envoyer la demande d’approbation au client à des fins de revue et pour recevoir la réponse.</span><span class="sxs-lookup"><span data-stu-id="9f60b-142">Send and Receive activities with correlation are used to send the approval request to the client for review and receive the response.</span></span>  
  
9. <span data-ttu-id="9f60b-143">Le résultat du workflow de processus d'approbation est envoyé au client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-143">The result of the approval process workflow is sent to the client.</span></span>  
  
## <a name="using-the-sample"></a><span data-ttu-id="9f60b-144">Utilisation de l'exemple</span><span class="sxs-lookup"><span data-stu-id="9f60b-144">Using the Sample</span></span>  
  
##### <a name="to-set-up-the-database"></a><span data-ttu-id="9f60b-145">Pour configurer la base de données</span><span class="sxs-lookup"><span data-stu-id="9f60b-145">To set up the database</span></span>  
  
1. <span data-ttu-id="9f60b-146">À partir d’une invite de commandes de Visual Studio 2010 avec des privilèges d’administrateur, accédez au dossier DocumentApprovalProcess et exécutez Setup.cmd.</span><span class="sxs-lookup"><span data-stu-id="9f60b-146">From a Visual Studio 2010 command prompt opened with Administrator privileges, navigate to this DocumentApprovalProcess folder and run Setup.cmd.</span></span>  
  
##### <a name="to-set-up-the-application"></a><span data-ttu-id="9f60b-147">Pour configurer l'application</span><span class="sxs-lookup"><span data-stu-id="9f60b-147">To set up the application</span></span>  
  
1. <span data-ttu-id="9f60b-148">À l’aide de Visual Studio 2010, ouvrez le fichier solution DocumentApprovalProcess.sln.</span><span class="sxs-lookup"><span data-stu-id="9f60b-148">Using Visual Studio 2010, open the DocumentApprovalProcess.sln solution file.</span></span>  
  
2. <span data-ttu-id="9f60b-149">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="9f60b-149">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3. <span data-ttu-id="9f60b-150">Pour exécuter la solution, lancez l’Application responsable des approbations en double-cliquant sur le projet ApprovalManager dans le **l’Explorateur de solutions** et en cliquant sur **déboguer**->**Démarrer**  nouvelle instance dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="9f60b-150">To run the solution, launch the Approval Manager Application by right-clicking the ApprovalManager project in the **Solution Explorer** and clicking **Debug**->**Start** new instance from the right-click menu.</span></span>  
  
     <span data-ttu-id="9f60b-151">Attendez que la sortie du responsable vous indique qu'il est prêt.</span><span class="sxs-lookup"><span data-stu-id="9f60b-151">Wait for the manager’s output to let you know that it is ready.</span></span>  
  
##### <a name="to-run-the-single-approval-scenario"></a><span data-ttu-id="9f60b-152">Pour exécuter le scénario avec approbation unique</span><span class="sxs-lookup"><span data-stu-id="9f60b-152">To run the single approval scenario</span></span>  
  
1. <span data-ttu-id="9f60b-153">Ouvrez une invite de commandes avec l'autorisation d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-153">Open a command prompt with administrator permission.</span></span>  
  
2. <span data-ttu-id="9f60b-154">Naviguez jusqu'au répertoire qui contient la solution.</span><span class="sxs-lookup"><span data-stu-id="9f60b-154">Navigate to the directory that contains the solution.</span></span>  
  
3. <span data-ttu-id="9f60b-155">Naviguez jusqu’au dossier ApprovalClient\Bin\Debug et exécutez deux instances d’ApprovalClient.exe.</span><span class="sxs-lookup"><span data-stu-id="9f60b-155">Navigate to the ApprovalClient\Bin\Debug folder and execute two instances of ApprovalClient.exe.</span></span>  
  
4. <span data-ttu-id="9f60b-156">Cliquez sur **découvrir**, attendez que le **s’abonner** bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="9f60b-156">Click **discover**, wait until the **subscribe** button is enabled.</span></span>  
  
5. <span data-ttu-id="9f60b-157">Tapez le nom d’utilisateur et cliquez sur **s’abonner**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-157">Type any user name and click **subscribe**.</span></span> <span data-ttu-id="9f60b-158">Pour un client, utilisez `UserType1` et pour l'autre, tapez `UserType2`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-158">For one client, use `UserType1` and the other type `UserType2`.</span></span>  
  
6. <span data-ttu-id="9f60b-159">Dans le client `UserType1`, sélectionnez le type d’approbation unique dans le menu déroulant et tapez un nom de document ainsi qu’un contenu.</span><span class="sxs-lookup"><span data-stu-id="9f60b-159">In the `UserType1` client, select the single approval type from the drop down menu and type a document name and content.</span></span> <span data-ttu-id="9f60b-160">Cliquez sur **demander l’approbation**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-160">Click **Request Approval**.</span></span>  
  
7. <span data-ttu-id="9f60b-161">Dans le client `UserType2`, un document en attente d'approbation apparaît.</span><span class="sxs-lookup"><span data-stu-id="9f60b-161">In the `UserType2` client, a document awaiting approval appears.</span></span> <span data-ttu-id="9f60b-162">Sélectionnez-la, puis appuyez sur **approuver** ou **rejeter**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-162">Select it and press **approve** or **reject**.</span></span> <span data-ttu-id="9f60b-163">Les résultats doivent s'afficher dans le client `UserType1`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-163">The results should show in the `UserType1` client.</span></span>  
  
##### <a name="to-run-the-quorum-approval-scenario"></a><span data-ttu-id="9f60b-164">Pour exécuter le scénario avec approbation de quorum</span><span class="sxs-lookup"><span data-stu-id="9f60b-164">To run the quorum approval scenario</span></span>  
  
1. <span data-ttu-id="9f60b-165">Ouvrez une invite de commandes avec l'autorisation d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-165">Open a command prompt with administrator permission.</span></span>  
  
2. <span data-ttu-id="9f60b-166">Naviguez jusqu'au répertoire qui contient la solution.</span><span class="sxs-lookup"><span data-stu-id="9f60b-166">Navigate to the directory that contains the solution.</span></span>  
  
3. <span data-ttu-id="9f60b-167">Naviguez jusqu’au dossier ApprovalClient\Bin\Debug et exécutez trois instances d’ApprovalClient.exe.</span><span class="sxs-lookup"><span data-stu-id="9f60b-167">Navigate to the ApprovalClient\Bin\Debug folder and execute three instances of ApprovalClient.exe.</span></span>  
  
4. <span data-ttu-id="9f60b-168">Cliquez sur **découvrir**, attendez que le **s’abonner** bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="9f60b-168">Click **discover**, wait until the **subscribe** button is enabled.</span></span>  
  
5. <span data-ttu-id="9f60b-169">Tapez le nom d’utilisateur et cliquez sur **s’abonner**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-169">Type any user name and click **subscribe**.</span></span> <span data-ttu-id="9f60b-170">Pour un client, utilisez `UserType1` et pour les deux autres, tapez `UserType2`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-170">For one client use `UserType1` and the other two type `UserType2`.</span></span>  
  
6. <span data-ttu-id="9f60b-171">Dans le client `UserType1`, sélectionnez le type d’approbation de quorum dans le menu déroulant et tapez un nom de document ainsi qu’un contenu.</span><span class="sxs-lookup"><span data-stu-id="9f60b-171">In the `UserType1` client, select the quorum approval type from the drop down menu and type a document name and content.</span></span> <span data-ttu-id="9f60b-172">Cliquez sur **demander l’approbation**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-172">Click **Request Approval**.</span></span> <span data-ttu-id="9f60b-173">Ceci nécessite que les deux clients `UserType2` approuvent ou rejettent le document.</span><span class="sxs-lookup"><span data-stu-id="9f60b-173">This requests that the two `UserType2` clients approve or reject the document.</span></span> <span data-ttu-id="9f60b-174">Alors que les deux clients `UserType2` doivent répondre, un seul client doit approuver le document pour qu'il le soit.</span><span class="sxs-lookup"><span data-stu-id="9f60b-174">While both `UserType2` clients must respond, only one client must approve the document for it to be approved.</span></span>  
  
7. <span data-ttu-id="9f60b-175">Dans les clients `UserType2`, un document en attente d'approbation apparaît.</span><span class="sxs-lookup"><span data-stu-id="9f60b-175">In the `UserType2` clients, a document awaiting approval appears.</span></span> <span data-ttu-id="9f60b-176">Sélectionnez-la, puis appuyez sur **approuver** ou **rejeter**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-176">Select it and press **approve** or **reject**.</span></span> <span data-ttu-id="9f60b-177">Les résultats doivent s'afficher dans le client `UserType1`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-177">The results should show in the `UserType1` client.</span></span>  
  
##### <a name="to-run-the-complex-approval-scenario"></a><span data-ttu-id="9f60b-178">Pour exécuter le scénario avec approbation complexe</span><span class="sxs-lookup"><span data-stu-id="9f60b-178">To run the complex approval scenario</span></span>  
  
1. <span data-ttu-id="9f60b-179">Ouvrez une invite de commandes avec l'autorisation d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="9f60b-179">Open a command prompt with administrator permission.</span></span>  
  
2. <span data-ttu-id="9f60b-180">Naviguez jusqu'au répertoire qui contient la solution.</span><span class="sxs-lookup"><span data-stu-id="9f60b-180">Navigate to the directory that contains the solution.</span></span>  
  
3. <span data-ttu-id="9f60b-181">Naviguez jusqu'au dossier ApprovalClient\Bin\Debug et exécutez quatre instances d'ApprovalClient.exe.</span><span class="sxs-lookup"><span data-stu-id="9f60b-181">Navigate to the ApprovalClient\Bin\Debug folder and execute four instances of ApprovalClient.exe.</span></span>  
  
4. <span data-ttu-id="9f60b-182">Cliquez sur **découvrir**, attendez que le **s’abonner** bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="9f60b-182">Click **discover**, wait until the **subscribe** button is enabled.</span></span>  
  
5. <span data-ttu-id="9f60b-183">Tapez le nom d’utilisateur et cliquez sur **s’abonner**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-183">Type any user name and click **subscribe**.</span></span> <span data-ttu-id="9f60b-184">Pour un client, utilisez `UserType1`, pour deux utilisations, tapez `UserType2` et, pour le dernier, utilisez `UserType3`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-184">For one client use `UserType1`, in two uses type `UserType2`, and in the last use `UserType3`.</span></span>  
  
6. <span data-ttu-id="9f60b-185">Dans le client `UserType1`, sélectionnez le type d’approbation unique dans le menu déroulant et tapez un nom de document ainsi qu’un contenu.</span><span class="sxs-lookup"><span data-stu-id="9f60b-185">In the `UserType1` client, select the single approval type from the drop down menu and type a document name and content.</span></span> <span data-ttu-id="9f60b-186">Cliquez sur **demander l’approbation**.</span><span class="sxs-lookup"><span data-stu-id="9f60b-186">Click **Request Approval**.</span></span>  
  
7. <span data-ttu-id="9f60b-187">Dans les clients `UserType2`, un document en attente d'approbation apparaît.</span><span class="sxs-lookup"><span data-stu-id="9f60b-187">In the `UserType2` clients, a document awaiting approval appears.</span></span> <span data-ttu-id="9f60b-188">Sélectionnez-la, puis appuyez sur **approuver**, le document est transmis à la `UserType3` client.</span><span class="sxs-lookup"><span data-stu-id="9f60b-188">Select it and press **approve**, the document is passed to the `UserType3` client.</span></span>  
  
     <span data-ttu-id="9f60b-189">Si le document est approuvé par le premier quorum `UserType2`, le document est passé au client `UserType3`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-189">If the document is approved by the first `UserType2` quorum, the document is passed to the `UserType3` client.</span></span>  
  
8. <span data-ttu-id="9f60b-190">Approuvez ou rejetez le document du client `UserType3`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-190">Approve or reject the document from the `UserType3` client.</span></span> <span data-ttu-id="9f60b-191">Les résultats doivent s'afficher dans le client `UserType1`.</span><span class="sxs-lookup"><span data-stu-id="9f60b-191">The results should show in the `UserType1` client.</span></span>  
  
##### <a name="to-clean-up"></a><span data-ttu-id="9f60b-192">Pour nettoyer</span><span class="sxs-lookup"><span data-stu-id="9f60b-192">To clean up</span></span>  
  
1. <span data-ttu-id="9f60b-193">À partir d’une invite de commandes Visual Studio 2010, accédez au dossier DocumentApprovalProcess et exécutez Cleanup.cmd.</span><span class="sxs-lookup"><span data-stu-id="9f60b-193">From a Visual Studio 2010 command prompt, navigate to the DocumentApprovalProcess folder and run Cleanup.cmd.</span></span>
