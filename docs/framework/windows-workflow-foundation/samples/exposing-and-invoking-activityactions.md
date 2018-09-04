---
title: Exposition et appel d'ActivityActions
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: f36d88fc54e5150927113ed8825fbccad84129d4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520121"
---
# <a name="exposing-and-invoking-activityactions"></a><span data-ttu-id="c5bad-102">Exposition et appel d'ActivityActions</span><span class="sxs-lookup"><span data-stu-id="c5bad-102">Exposing and Invoking ActivityActions</span></span>
<span data-ttu-id="c5bad-103">Cet exemple montre comment développer une activité personnalisée qui a un <xref:System.Activities.ActivityAction>.</span><span class="sxs-lookup"><span data-stu-id="c5bad-103">This sample demonstrates how to develop a custom activity that has an <xref:System.Activities.ActivityAction>.</span></span> <span data-ttu-id="c5bad-104">Il montre également comment utiliser cette activité en fournissant une implémentation d'<xref:System.Activities.ActivityAction>.</span><span class="sxs-lookup"><span data-stu-id="c5bad-104">It also demonstrates how to use this activity by providing an implementation of the <xref:System.Activities.ActivityAction>.</span></span>  
  
 <span data-ttu-id="c5bad-105">Un <xref:System.Activities.ActivityAction> permet à un auteur d’activité exposer des « trous » avec des signatures spécifiques où l’utilisateur de l’activité peut incorporer un comportement personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c5bad-105">An <xref:System.Activities.ActivityAction> allows an activity author to expose "holes" with specific signatures where the activity user can plug in a custom behavior.</span></span> <span data-ttu-id="c5bad-106">Par exemple, le <!--zz <xref:System.Activities.Statements.ForEach>--> `System.Activities.Statements.ForEach` activité, (qui fonctionne sur une collection d’éléments), a un <xref:System.Activities.ActivityAction> qui permet à l’utilisateur de l’activité incorporer un comportement qui fonctionne sur l’élément d’itération actuel.</span><span class="sxs-lookup"><span data-stu-id="c5bad-106">For example, the <!--zz <xref:System.Activities.Statements.ForEach>--> `System.Activities.Statements.ForEach` activity, (which operates over a collection of items), has an <xref:System.Activities.ActivityAction> that allows the activity user to plug in behavior that operates on the current iteration item.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="c5bad-107">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="c5bad-107">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="c5bad-108">Ouvrez le **ActivityAction.sln** exemple de solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5bad-108">Open the **ActivityAction.sln** sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="c5bad-109">Générez et exécutez la solution.</span><span class="sxs-lookup"><span data-stu-id="c5bad-109">Build and run the solution.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="c5bad-110">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5bad-110">The samples may already be installed on your machine.</span></span> <span data-ttu-id="c5bad-111">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="c5bad-111">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="c5bad-112">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="c5bad-112">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="c5bad-113">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="c5bad-113">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ActivityAction`