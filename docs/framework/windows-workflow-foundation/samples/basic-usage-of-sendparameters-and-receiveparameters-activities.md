---
title: Utilisation de base des activités SendParameters et ReceiveParameters
ms.date: 03/30/2017
ms.assetid: 1b6b1681-3d41-403f-bfe2-3f600f24aa8c
ms.openlocfilehash: 8732b10f3f96ccf9ed352f9b54c60a4ee0d1664c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33515396"
---
# <a name="basic-usage-of-sendparameters-and-receiveparameters-activities"></a><span data-ttu-id="0cef6-102">Utilisation de base des activités SendParameters et ReceiveParameters</span><span class="sxs-lookup"><span data-stu-id="0cef6-102">Basic Usage of SendParameters and ReceiveParameters Activities</span></span>
<span data-ttu-id="0cef6-103">Cet exemple illustre l'utilisation des activités <xref:System.ServiceModel.Activities.SendParametersContent> et <xref:System.ServiceModel.Activities.ReceiveParametersContent>.</span><span class="sxs-lookup"><span data-stu-id="0cef6-103">This sample shows the use of <xref:System.ServiceModel.Activities.SendParametersContent> and <xref:System.ServiceModel.Activities.ReceiveParametersContent> activities.</span></span> <span data-ttu-id="0cef6-104">Le service expose une opération qui accepte un argument de type chaîne et retourne l'entrée au client.</span><span class="sxs-lookup"><span data-stu-id="0cef6-104">The service exposes one operation that takes a string argument and echoes the input back to the client.</span></span> <span data-ttu-id="0cef6-105">L'exemple montre comment configurer les paramètres pour ces activités de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0cef6-105">The sample shows how to set up the parameters for these messaging activities.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="0cef6-106">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0cef6-106">The samples may already be installed on your machine.</span></span> <span data-ttu-id="0cef6-107">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0cef6-107">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="0cef6-108">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="0cef6-108">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="0cef6-109">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="0cef6-109">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\SendReceiveParameters`  
  
#### <a name="using-this-sample"></a><span data-ttu-id="0cef6-110">Utilisation de cet exemple</span><span class="sxs-lookup"><span data-stu-id="0cef6-110">Using this sample</span></span>  
  
1.  <span data-ttu-id="0cef6-111">Chargez la solution du projet dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] et générez le projet.</span><span class="sxs-lookup"><span data-stu-id="0cef6-111">Load the project solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] and build the project.</span></span>  
  
2.  <span data-ttu-id="0cef6-112">En premier lieu, exécutez l'application EchoWorkflowService, générée dans [répertoire de base de la solution]\EchoWorkflowService\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="0cef6-112">First run the EchoWorkflowService application generated in [solution base directory]\EchoWorkflowService\bin\debug.</span></span>  
  
3.  <span data-ttu-id="0cef6-113">En second lieu, exécutez l'application EchoWorkflowClient, générée dans [répertoire de base de la solution]\EchoWorkflowClient\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="0cef6-113">Second, run the EchoWorkflowClient application generated in [solution base directory]\EchoWorkflowClient\bin\debug.</span></span>  
  
4.  <span data-ttu-id="0cef6-114">Le client appelle l'opération Echo sur le service et imprime les résultats.</span><span class="sxs-lookup"><span data-stu-id="0cef6-114">The client calls Echo operation on the service and prints the results.</span></span> <span data-ttu-id="0cef6-115">Une fois cette opération terminée, appuyez sur ENTRÉE pour quitter le client, puis le service.</span><span class="sxs-lookup"><span data-stu-id="0cef6-115">When complete, press ENTER to exit the client and then the service.</span></span>