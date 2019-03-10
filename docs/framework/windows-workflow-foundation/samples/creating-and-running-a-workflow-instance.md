---
title: Création et exécution d'une instance de workflow
ms.date: 03/30/2017
ms.assetid: 19d27f47-0491-4569-8f53-51bc1d940e80
ms.openlocfilehash: d0c59946b6419e7088e3426d7ddd08537cfab5a4
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57722007"
---
# <a name="creating-and-running-a-workflow-instance"></a><span data-ttu-id="ada21-102">Création et exécution d'une instance de workflow</span><span class="sxs-lookup"><span data-stu-id="ada21-102">Creating and Running a Workflow Instance</span></span>
<span data-ttu-id="ada21-103">Cet exemple montre comment exécuter une instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="ada21-103">This sample shows how to run a workflow instance.</span></span> <span data-ttu-id="ada21-104">Il indique comment l’exécuter de façon synchrone et de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ada21-104">It shows how to execute it synchronously and asynchronously.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="ada21-105">Démonstrations</span><span class="sxs-lookup"><span data-stu-id="ada21-105">Demonstrates</span></span>  
 <span data-ttu-id="ada21-106"><xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.</span><span class="sxs-lookup"><span data-stu-id="ada21-106"><xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.</span></span>  
  
## <a name="discussion"></a><span data-ttu-id="ada21-107">Discussion</span><span class="sxs-lookup"><span data-stu-id="ada21-107">Discussion</span></span>  
 <span data-ttu-id="ada21-108">La première partie de l'exemple utilise <xref:System.Activities.WorkflowInvoker.Invoke%2A>.</span><span class="sxs-lookup"><span data-stu-id="ada21-108">The first part of the sample uses <xref:System.Activities.WorkflowInvoker.Invoke%2A>.</span></span> <span data-ttu-id="ada21-109">Il s'agit de la façon la plus simple d'exécuter un workflow.</span><span class="sxs-lookup"><span data-stu-id="ada21-109">This is the most basic way to execute a workflow.</span></span> <span data-ttu-id="ada21-110">Les workflows exécutés avec <xref:System.Activities.WorkflowInvoker.Invoke%2A> s'exécutent de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="ada21-110">Workflows executed with <xref:System.Activities.WorkflowInvoker.Invoke%2A> are executed synchronously.</span></span>  
  
 <span data-ttu-id="ada21-111">La deuxième partie de l'exemple utilise la classe <xref:System.Activities.WorkflowApplication>.</span><span class="sxs-lookup"><span data-stu-id="ada21-111">The second part of the sample uses the <xref:System.Activities.WorkflowApplication> class.</span></span> <span data-ttu-id="ada21-112"><xref:System.Activities.WorkflowApplication> vous permet d'avoir plus de contrôle sur chaque instance, notamment la possibilité d'interagir avec le workflow en cours d'exécution et d'exécuter le workflow de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ada21-112"><xref:System.Activities.WorkflowApplication> enables you to have more control over each instance, including the ability to interact with the running workflow and to run the workflow asynchronously.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ada21-113">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ada21-113">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ada21-114">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="ada21-114">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="ada21-115">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="ada21-115">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ada21-116">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="ada21-116">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\CreatingWorkflowInstances`  
  
## <a name="see-also"></a><span data-ttu-id="ada21-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ada21-117">See also</span></span>
- [<span data-ttu-id="ada21-118">Utilisation de WorkflowInvoker et WorkflowApplication</span><span class="sxs-lookup"><span data-stu-id="ada21-118">Using WorkflowInvoker and WorkflowApplication</span></span>](../using-workflowinvoker-and-workflowapplication.md)
