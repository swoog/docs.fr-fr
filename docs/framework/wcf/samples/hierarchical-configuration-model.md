---
title: Modèle de configuration hiérarchique
ms.date: 03/30/2017
ms.assetid: 28dcc698-226c-4b77-9e51-8bf45a36216c
ms.openlocfilehash: 8ca9b01eb022e2e2ab940866a6230e8227ceb2dc
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43736391"
---
# <a name="hierarchical-configuration-model"></a><span data-ttu-id="d5dd9-102">Modèle de configuration hiérarchique</span><span class="sxs-lookup"><span data-stu-id="d5dd9-102">Hierarchical Configuration Model</span></span>
<span data-ttu-id="d5dd9-103">Cet exemple montre comment implémenter une hiérarchie de fichiers de configuration pour les services.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-103">This sample demonstrates how to implement a hierarchy of configuration files for services.</span></span> <span data-ttu-id="d5dd9-104">Il montre également comment les liaisons, comportements de service et comportements de point de terminaison sont hérités des niveaux supérieurs de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-104">It also shows how bindings, service behaviors, and endpoint behaviors are inherited from higher levels in the hierarchy.</span></span>  
  
## <a name="sample-details"></a><span data-ttu-id="d5dd9-105">Détails de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d5dd9-105">Sample details</span></span>  
 <span data-ttu-id="d5dd9-106">L’une des fonctionnalités développées pour WCF dans [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)] est l’amélioration du produit dans le modèle de configuration hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-106">One of the features developed for WCF in [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)] is the improvement in the hierarchical configuration model.</span></span> <span data-ttu-id="d5dd9-107">Un exemple de modèle de configuration hiérarchique pourrait être celui que définit Machine.config -> Rootweb.config -> Web.config. Dans [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], les liaisons et comportements définis dans les niveaux supérieurs de la hiérarchie de configuration sont ajoutés à vos services sans configuration explicite.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-107">An example of a hierarchical configuration model would be the one defined by Machine.config -> Rootweb.config -> Web.config. In [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], those bindings and behaviors that are defined in upper levels in the configuration hierarchy are added to your services with no explicit configuration.</span></span> <span data-ttu-id="d5dd9-108">Cet exemple montre comment il est possible de simplifier votre configuration de services en vous appuyant sur les éléments de configuration définis au niveau de l'ordinateur ou de l'application.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-108">This sample shows how it is possible to simplify your service configuration by relying on configuration elements defined at the computer or the application level.</span></span>  
  
 <span data-ttu-id="d5dd9-109">Cet exemple se compose de neuf services, définis dans trois niveaux de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-109">This sample consists of nine services, defined in three levels of hierarchy.</span></span> <span data-ttu-id="d5dd9-110">`Service1` se trouve à la racine.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-110">`Service1` is at the root.</span></span> <span data-ttu-id="d5dd9-111">`Service2` et `Service3` héritent des éléments par défaut de `Service1`.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-111">`Service2` and `Service3` inherit the default elements from `Service1`.</span></span> <span data-ttu-id="d5dd9-112">`Service4`, `Service5`, `Service6` et `Service7` sont définis à un troisième niveau de la hiérarchie et héritent des éléments par défaut de `Service3`.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-112">`Service4`, `Service5`, `Service6` and `Service7` are defined at a third level of the hierarchy, inheriting the default elements from `Service3`.</span></span> <span data-ttu-id="d5dd9-113">Enfin, `Service10` et `Service11` se situent à un quatrième niveau de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-113">Finally `Service10` and `Service11` are at a fourth level of the hierarchy.</span></span>  
  
 <span data-ttu-id="d5dd9-114">Tous les services implémentent le contrat `IDesc`.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-114">All the services implement the `IDesc` contract.</span></span> <span data-ttu-id="d5dd9-115">La définition de l'interface `IDesc` qui montre les méthodes exposées dans cette interface est présentée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-115">The following is the definition of the `IDesc` interface that shows the methods exposed in this interface.</span></span> <span data-ttu-id="d5dd9-116">L'interface `IDesc` est définie dans Service1.cs.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-116">The `IDesc` interface is defined in Service1.cs.</span></span>  
  
```csharp  
// Define a service contract  
[ServiceContract(Namespace="http://Microsoft.Samples.ConfigHierarchicalModel")]  
public interface IDesc  
{  
    [OperationContract]  
    List<string> ListEndpoints();  
    [OperationContract]  
    List<string> ListServiceBehaviors();  
    [OperationContract]  
    List<string> ListEndpointBehaviors();  
}  
```  
  
 <span data-ttu-id="d5dd9-117">L'implémentation de ces méthodes par les services est simple.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-117">The implementation of these methods by the services is straightforward.</span></span> <span data-ttu-id="d5dd9-118">`ListEndpoints` itère au sein de tous les points de terminaison de service et retourne une liste de tous les points de terminaison dont le service dispose.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-118">`ListEndpoints` iterates through all the service endpoints and returns a list of all the endpoints that the service has.</span></span> <span data-ttu-id="d5dd9-119">`ListServiceBehaviors` itère au sein de tous les comportements ajoutés au service et retourne la liste de tous les comportements de service associés au service.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-119">`ListServiceBehaviors` iterates through all the behaviors added to the service and returns the list of all the service behaviors associated with the service.</span></span> <span data-ttu-id="d5dd9-120">`ListEndpointBehaviors` se comporte de manière similaire à `ListServiceBehaviors`, mais il retourne la liste des comportements de point de terminaison à la place.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-120">`ListEndpointBehaviors` behaves in a similar way to `ListServiceBehaviors`, but it returns the list of endpoint behaviors instead.</span></span>  
  
 <span data-ttu-id="d5dd9-121">Cette implémentation permet au client de connaître le nombre de points de terminaison qu'expose le service et les comportements de service et comportements de point de terminaison qui ont été ajoutés au service.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-121">This implementation allows the client to know how many endpoints the service is exposing and which service behaviors and endpoint behaviors have been added to the service.</span></span> <span data-ttu-id="d5dd9-122">Le client implémenté dans le cadre de l'exemple ajoute une référence de service à tous les services de la solution et affiche ces éléments pour chacun des services.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-122">The client that has been implemented as part of the sample adds a service reference to all the services in the solution and shows these elements for each one of the services.</span></span>  
  
## <a name="to-use-this-sample"></a><span data-ttu-id="d5dd9-123">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="d5dd9-123">To use this sample</span></span>  
  
#### <a name="to-run-the-client"></a><span data-ttu-id="d5dd9-124">Pour exécuter le client</span><span class="sxs-lookup"><span data-stu-id="d5dd9-124">To run the client</span></span>  
  
1.  <span data-ttu-id="d5dd9-125">À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier ConfigHierarchicalModel.sln.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-125">Using [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], open the ConfigHierarchicalModel.sln file.</span></span>  
  
2.  <span data-ttu-id="d5dd9-126">Le projet client n'est pas encore configuré en tant que projet de démarrage. Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-126">The client project is not already set up as the start-up project, follow these steps.</span></span>  
  
    1.  <span data-ttu-id="d5dd9-127">Dans **l’Explorateur de solutions**, avec le bouton droit de la solution, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-127">In **Solution Explorer**, right-click the solution and then select **Properties**.</span></span>  
  
    2.  <span data-ttu-id="d5dd9-128">Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis cliquez sur **projet de démarrage unique**.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-128">In **Common Properties**, select **Startup Project**, and then click **Single startup project**.</span></span>  
  
    3.  <span data-ttu-id="d5dd9-129">À partir de la **projet de démarrage unique** liste déroulante, sélectionnez **Client**.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-129">From the **Single startup project** drop-down, select **Client**.</span></span>  
  
    4.  <span data-ttu-id="d5dd9-130">Cliquez sur **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-130">Click **OK** to close the dialog.</span></span>  
  
3.  <span data-ttu-id="d5dd9-131">Pour créer l'exemple, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-131">To build the sample, press CTRL+SHIFT+B.</span></span>  
  
4.  <span data-ttu-id="d5dd9-132">Pour exécuter le client, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-132">To run the client, press Ctrl+F5.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5dd9-133">Si ces étapes ne fonctionnent pas, assurez-vous que votre environnement a été correctement configuré, en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5dd9-133">If these steps do not work, make sure that your environment has been properly set up, using the following steps:</span></span>  
>   
> 1.  <span data-ttu-id="d5dd9-134">Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d5dd9-134">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
> 2.  <span data-ttu-id="d5dd9-135">Pour générer la solution, suivez les instructions de [génération des exemples Windows Communication Foundation](building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d5dd9-135">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
> 3.  <span data-ttu-id="d5dd9-136">Pour exécuter l’exemple dans un seul ou plusieurs configurations d’ordinateur, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d5dd9-136">To run the sample in a single or multiple computer configurations, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d5dd9-137">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-137">The samples may already be installed on your computer.</span></span> <span data-ttu-id="d5dd9-138">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-138">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="d5dd9-139">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-139">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="d5dd9-140">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="d5dd9-140">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\ConfigHierarchicalModel`  
  
## <a name="see-also"></a><span data-ttu-id="d5dd9-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5dd9-141">See Also</span></span>  
 [<span data-ttu-id="d5dd9-142">Exemples de gestion AppFabric</span><span class="sxs-lookup"><span data-stu-id="d5dd9-142">AppFabric Management Samples</span></span>](https://go.microsoft.com/fwlink/?LinkId=193960)
