---
title: ParallelForEach limité
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: 195c627d62665f832384989d4ef03105c4af3757
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516260"
---
# <a name="throttled-parallel-foreach"></a><span data-ttu-id="d662f-102">ParallelForEach limité</span><span class="sxs-lookup"><span data-stu-id="d662f-102">Throttled Parallel ForEach</span></span>
<span data-ttu-id="d662f-103">Le `ThrottleParallelForEach` activité est similaire à la <!--zz <xref:System.Activities.Statements.ParallelForEach>--> `System.Activities.Statements.ParallelForEach` activité hormis le seul fait qu’elle permet de définir un facteur de concurrence pour restreindre le nombre de branches simultanées à exécuter.</span><span class="sxs-lookup"><span data-stu-id="d662f-103">The `ThrottleParallelForEach` activity is similar to the <!--zz <xref:System.Activities.Statements.ParallelForEach>--> `System.Activities.Statements.ParallelForEach` activity with the one exception that it allows setting a concurrency factor to restrict the number of simultaneous branches to execute.</span></span> <span data-ttu-id="d662f-104">L'activité `ThrottleParallelForEach` dérive de <xref:System.Activities.NativeActivity>, parce qu'elle doit planifier d'autres activités (activités enfants) et est uniquement accessible via la classe <xref:System.Activities.NativeActivityContext>.</span><span class="sxs-lookup"><span data-stu-id="d662f-104">The `ThrottleParallelForEach` activity derives from <xref:System.Activities.NativeActivity>, because it needs to schedule other activities (the child activities) and this is only accessible through the <xref:System.Activities.NativeActivityContext> class.</span></span>  
  
## <a name="projects"></a><span data-ttu-id="d662f-105">Projets</span><span class="sxs-lookup"><span data-stu-id="d662f-105">Projects</span></span>  
  
|<span data-ttu-id="d662f-106">**ProjectName**</span><span class="sxs-lookup"><span data-stu-id="d662f-106">**ProjectName**</span></span>|<span data-ttu-id="d662f-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="d662f-107">**Description**</span></span>|<span data-ttu-id="d662f-108">**Fichiers principaux**</span><span class="sxs-lookup"><span data-stu-id="d662f-108">**Main Files**</span></span>|  
|-|-|-|  
|<span data-ttu-id="d662f-109">ThrottledParallelForEach</span><span class="sxs-lookup"><span data-stu-id="d662f-109">ThrottledParallelForEach</span></span>|<span data-ttu-id="d662f-110">Contient l'activité `ThrottledParallelForEach` et son concepteur.</span><span class="sxs-lookup"><span data-stu-id="d662f-110">Contains `ThrottledParallelForEach` activity and its designer.</span></span>|<span data-ttu-id="d662f-111">ThrottledParallelForEach.cs</span><span class="sxs-lookup"><span data-stu-id="d662f-111">ThrottledParallelForEach.cs</span></span><br /><br /> <span data-ttu-id="d662f-112">Définition de l'activité `ThrottledParallelForEach`.</span><span class="sxs-lookup"><span data-stu-id="d662f-112">The `ThrottledParallelForEach` activity definition.</span></span>|  
|<span data-ttu-id="d662f-113">CodeTestClient</span><span class="sxs-lookup"><span data-stu-id="d662f-113">CodeTestClient</span></span>|<span data-ttu-id="d662f-114">Exemple d'application cliente qui configure et exécute un workflow avec un `ThrottledParallelForEach` à l'aide de code impératif.</span><span class="sxs-lookup"><span data-stu-id="d662f-114">Sample client application that configures and runs a workflow with a `ThrottledParallelForEach` using imperative code.</span></span>|<span data-ttu-id="d662f-115">Program.cs</span><span class="sxs-lookup"><span data-stu-id="d662f-115">Program.cs</span></span><br /><br /> <span data-ttu-id="d662f-116">Définit et exécute une instance de l'exemple de workflow.</span><span class="sxs-lookup"><span data-stu-id="d662f-116">Defines and runs an instance of the sample workflow.</span></span>|  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="d662f-117">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="d662f-117">To use this sample</span></span>  
  
1.  <span data-ttu-id="d662f-118">À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier ThrottledParallelForEach.sln.</span><span class="sxs-lookup"><span data-stu-id="d662f-118">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the ThrottledParallelForEach.sln file.</span></span>  
  
2.  <span data-ttu-id="d662f-119">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="d662f-119">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="d662f-120">Pour exécuter la solution, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="d662f-120">To run the solution, press F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d662f-121">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d662f-121">The samples may already be installed on your machine.</span></span> <span data-ttu-id="d662f-122">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="d662f-122">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="d662f-123">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="d662f-123">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="d662f-124">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="d662f-124">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`