---
title: Propriétés d'exécution
ms.date: 03/30/2017
ms.assetid: 31c009db-397c-4653-87e2-32dc77fa4b13
ms.openlocfilehash: 4906c2ad11c8b5822764435d2b39a5b51f2673ba
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43748192"
---
# <a name="execution-properties"></a><span data-ttu-id="9e3ff-102">Propriétés d'exécution</span><span class="sxs-lookup"><span data-stu-id="9e3ff-102">Execution Properties</span></span>
<span data-ttu-id="9e3ff-103">Cet exemple montre comment définir et utiliser une propriété d'exécution dans une activité personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-103">This sample shows how to define and use an execution property in a custom activity.</span></span> <span data-ttu-id="9e3ff-104">Dans cet exemple, la propriété d'exécution détermine la couleur de premier plan de la console.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-104">In this example, the execution property determines the console's foreground color.</span></span> <span data-ttu-id="9e3ff-105">Un exemple de workflow montre comment différents chemins logiques d'exécution (branches d'une activité <xref:System.Activities.Statements.Parallel>) peuvent maintenir des couleurs de console différentes malgré l'exécution entrelacée d'activités (à travers les branches de l'activité <xref:System.Activities.Statements.Parallel>).</span><span class="sxs-lookup"><span data-stu-id="9e3ff-105">An example workflow shows how different logical paths of execution (branches of a <xref:System.Activities.Statements.Parallel> activity) can maintain different console colors despite interleaved execution of activities (across the branches of the <xref:System.Activities.Statements.Parallel> activity).</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="9e3ff-106">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="9e3ff-106">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="9e3ff-107">Ouvrez l'exemple de solution ExecutionProperties.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9e3ff-107">Open the ExecutionProperties.sln sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="9e3ff-108">La consultation de ThreeColors.xaml avant la génération de la solution affiche une erreur, car les activités personnalisées utilisées doivent être générées en même temps que la solution.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-108">Viewing ThreeColors.xaml before building the solution displays an error, because the custom activities used must be built at the same time as the solution.</span></span>  
  
2.  <span data-ttu-id="9e3ff-109">Générez et exécutez la solution.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-109">Build and run the solution.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="9e3ff-110">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-110">The samples may already be installed on your machine.</span></span> <span data-ttu-id="9e3ff-111">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-111">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="9e3ff-112">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-112">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9e3ff-113">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="9e3ff-113">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ExecutionProperties`