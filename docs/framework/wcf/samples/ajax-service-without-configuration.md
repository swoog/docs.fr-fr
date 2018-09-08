---
title: AJAX Service Without Configuration
ms.date: 03/30/2017
ms.assetid: e6db7acd-5679-45d4-b98a-8449c6873838
ms.openlocfilehash: f12b0fad97c9f43397f3b202800943e6d061aa53
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44180892"
---
# <a name="ajax-service-without-configuration"></a><span data-ttu-id="b1772-102">AJAX Service Without Configuration</span><span class="sxs-lookup"><span data-stu-id="b1772-102">AJAX Service Without Configuration</span></span>
<span data-ttu-id="b1772-103">Cet exemple montre comment utiliser Windows Communication Foundation (WCF) pour créer un service ASP.NET Asynchronous JavaScript and XML (AJAX) base (un service auquel vous pouvez accéder à l’aide de code JavaScript à partir d’un client de navigateur Web) sans utiliser de configuration Paramètres.</span><span class="sxs-lookup"><span data-stu-id="b1772-103">This sample demonstrates how to use Windows Communication Foundation (WCF) to create a basic ASP.NET Asynchronous JavaScript and XML (AJAX) service (a service that you can access by using JavaScript code from a Web browser client) without using any configuration settings.</span></span> <span data-ttu-id="b1772-104">Le service utilise une syntaxe spéciale dans le fichier .svc pour activer automatiquement un point de terminaison AJAX.</span><span class="sxs-lookup"><span data-stu-id="b1772-104">The service uses special syntax in the .svc file to automatically enable an AJAX endpoint.</span></span>  
  
 <span data-ttu-id="b1772-105">Prise en charge d’AJAX dans WCF est optimisé pour une utilisation avec ASP.NET AJAX via le `ScriptManager` contrôle.</span><span class="sxs-lookup"><span data-stu-id="b1772-105">AJAX support in WCF is optimized for use with ASP.NET AJAX through the `ScriptManager` control.</span></span> <span data-ttu-id="b1772-106">Pour obtenir un exemple d’utilisation de WCF avec ASP.NET AJAX, consultez le [exemples Ajax](https://msdn.microsoft.com/library/f3fa45b3-44d5-4926-8cc4-a13c30a3bf3e).</span><span class="sxs-lookup"><span data-stu-id="b1772-106">For an example of using WCF with ASP.NET AJAX, see the [Ajax Samples](https://msdn.microsoft.com/library/f3fa45b3-44d5-4926-8cc4-a13c30a3bf3e).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b1772-107">La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b1772-107">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="b1772-108">Cet exemple est basé sur le service AJAX Service utilisant HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="b1772-108">This sample builds upon the AJAX Service Using HTTP POST.</span></span> <span data-ttu-id="b1772-109">Comme décrit dans la [base AJAX Service](../../../../docs/framework/wcf/samples/basic-ajax-service.md) exemple, <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> est utilisé pour héberger le service.</span><span class="sxs-lookup"><span data-stu-id="b1772-109">As described in the [Basic AJAX Service](../../../../docs/framework/wcf/samples/basic-ajax-service.md) sample, <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> is used to host the service.</span></span>  

```svc
<%ServiceHost  
    language=c#  
    Debug="true"  
    Service="Microsoft.Ajax.Samples.CalculatorService  
    Factory="System.ServiceModel.Activation.WebScriptServiceHostFactory"  
%>  
```

 <span data-ttu-id="b1772-110"><xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> ajoute automatiquement un <xref:System.ServiceModel.Description.WebScriptEndpoint> au service.</span><span class="sxs-lookup"><span data-stu-id="b1772-110"><xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> automatically adds a <xref:System.ServiceModel.Description.WebScriptEndpoint> to the service.</span></span> <span data-ttu-id="b1772-111">Si aucune modification de configuration ne doit être apportée au point de terminaison, la section `<system.ServiceModel>` peut être supprimée complètement du fichier Web.config pour le service.</span><span class="sxs-lookup"><span data-stu-id="b1772-111">If no configuration changes need to be made to the endpoint, the `<system.ServiceModel>` section can be completely removed from the Web.config file for the service.</span></span> <span data-ttu-id="b1772-112">Le fichier Web.config contient des paramètres ASP.NET, qui sont utilisés par ConfigFreeClientPage.aspx.</span><span class="sxs-lookup"><span data-stu-id="b1772-112">The Web.config file contains some ASP.NET settings, which are used by ConfigFreeClientPage.aspx.</span></span> <span data-ttu-id="b1772-113">Si ce n'était pas le cas, l'intégralité du fichier Web.config pourrait être supprimée.</span><span class="sxs-lookup"><span data-stu-id="b1772-113">If that were not the case, the entire Web.config file could be removed.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b1772-114">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b1772-114">The samples may already be installed on your computer.</span></span> <span data-ttu-id="b1772-115">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b1772-115">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b1772-116">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="b1772-116">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b1772-117">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="b1772-117">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\ConfigFreeAjaxService`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="b1772-118">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="b1772-118">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="b1772-119">Assurez-vous d’avoir suivi les instructions d’installation dans [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b1772-119">Ensure that you perform the setup instructions in [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="b1772-120">Générez la solution configfreeajaxservice.sln tel que décrit dans [génération des exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b1772-120">Build the solution ConfigFreeAjaxService.sln as described in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="b1772-121">Accédez à http://localhost/ServiceModelSamples/ConfigFreeClientPage.aspx (n’ouvrez pas ConfigFreeClientPage.aspx dans le navigateur à partir du répertoire de projet).</span><span class="sxs-lookup"><span data-stu-id="b1772-121">Navigate to http://localhost/ServiceModelSamples/ConfigFreeClientPage.aspx (do not open ConfigFreeClientPage.aspx in the browser from within the project directory).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b1772-122">Avant d’exécuter cet exemple, assurez-vous que l’authentification anonyme et que l’authentification Windows ne sont pas toutes deux activées dans le dossier ServiceModelSamples des services IIS.</span><span class="sxs-lookup"><span data-stu-id="b1772-122">When running this sample, please ensure that Anonymous Authentication and Windows Authentication are not enabled simultaneously for the ServiceModelSamples folder in IIS.</span></span> <span data-ttu-id="b1772-123">Si tel est le cas, désactivez l'authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="b1772-123">If that is the case, please disable Windows Authentication.</span></span> <span data-ttu-id="b1772-124">Une fois que vous avez exécuté l'exemple, activez l'authentification Windows et réexécutez « iisreset ».</span><span class="sxs-lookup"><span data-stu-id="b1772-124">Once you have run the sample, enable Windows Authentication and run "iisreset".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1772-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1772-125">See Also</span></span>  
 [<span data-ttu-id="b1772-126">Service AJAX de base</span><span class="sxs-lookup"><span data-stu-id="b1772-126">Basic AJAX Service</span></span>](../../../../docs/framework/wcf/samples/basic-ajax-service.md)
