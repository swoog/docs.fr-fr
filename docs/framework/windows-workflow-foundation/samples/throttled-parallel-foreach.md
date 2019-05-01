---
title: ParallelForEach limité
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: fd30a1ac587359a054a273b3deca2e9bb8bc2798
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62004859"
---
# <a name="throttled-parallel-foreach"></a><span data-ttu-id="8db04-102">ParallelForEach limité</span><span class="sxs-lookup"><span data-stu-id="8db04-102">Throttled Parallel ForEach</span></span>

<span data-ttu-id="8db04-103">L'activité `ThrottleParallelForEach` est semblable à l'activité <xref:System.Activities.Statements.ParallelForEach%601> hormis le seul fait qu'elle permet la définition d'un facteur de concurrence pour restreindre le nombre de branches simultanées à exécuter.</span><span class="sxs-lookup"><span data-stu-id="8db04-103">The `ThrottleParallelForEach` activity is similar to the <xref:System.Activities.Statements.ParallelForEach%601> activity with the one exception that it allows setting a concurrency factor to restrict the number of simultaneous branches to execute.</span></span> <span data-ttu-id="8db04-104">L'activité `ThrottleParallelForEach` dérive de <xref:System.Activities.NativeActivity>, parce qu'elle doit planifier d'autres activités (activités enfants) et est uniquement accessible via la classe <xref:System.Activities.NativeActivityContext>.</span><span class="sxs-lookup"><span data-stu-id="8db04-104">The `ThrottleParallelForEach` activity derives from <xref:System.Activities.NativeActivity>, because it needs to schedule other activities (the child activities) and this is only accessible through the <xref:System.Activities.NativeActivityContext> class.</span></span>

## <a name="projects"></a><span data-ttu-id="8db04-105">Projets</span><span class="sxs-lookup"><span data-stu-id="8db04-105">Projects</span></span>

|<span data-ttu-id="8db04-106">**ProjectName**</span><span class="sxs-lookup"><span data-stu-id="8db04-106">**ProjectName**</span></span>|<span data-ttu-id="8db04-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="8db04-107">**Description**</span></span>|<span data-ttu-id="8db04-108">**Fichiers principaux**</span><span class="sxs-lookup"><span data-stu-id="8db04-108">**Main Files**</span></span>|
|-|-|-|
|<span data-ttu-id="8db04-109">ThrottledParallelForEach</span><span class="sxs-lookup"><span data-stu-id="8db04-109">ThrottledParallelForEach</span></span>|<span data-ttu-id="8db04-110">Contient l'activité `ThrottledParallelForEach` et son concepteur.</span><span class="sxs-lookup"><span data-stu-id="8db04-110">Contains `ThrottledParallelForEach` activity and its designer.</span></span>|<span data-ttu-id="8db04-111">ThrottledParallelForEach.cs</span><span class="sxs-lookup"><span data-stu-id="8db04-111">ThrottledParallelForEach.cs</span></span><br /><br /> <span data-ttu-id="8db04-112">Définition de l'activité `ThrottledParallelForEach`.</span><span class="sxs-lookup"><span data-stu-id="8db04-112">The `ThrottledParallelForEach` activity definition.</span></span>|
|<span data-ttu-id="8db04-113">CodeTestClient</span><span class="sxs-lookup"><span data-stu-id="8db04-113">CodeTestClient</span></span>|<span data-ttu-id="8db04-114">Exemple d'application cliente qui configure et exécute un workflow avec un `ThrottledParallelForEach` à l'aide de code impératif.</span><span class="sxs-lookup"><span data-stu-id="8db04-114">Sample client application that configures and runs a workflow with a `ThrottledParallelForEach` using imperative code.</span></span>|<span data-ttu-id="8db04-115">Program.cs</span><span class="sxs-lookup"><span data-stu-id="8db04-115">Program.cs</span></span><br /><br /> <span data-ttu-id="8db04-116">Définit et exécute une instance de l'exemple de workflow.</span><span class="sxs-lookup"><span data-stu-id="8db04-116">Defines and runs an instance of the sample workflow.</span></span>|

## <a name="to-use-this-sample"></a><span data-ttu-id="8db04-117">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="8db04-117">To use this sample</span></span>

1. <span data-ttu-id="8db04-118">À l’aide de Visual Studio 2010, ouvrez le fichier ThrottledParallelForEach.sln.</span><span class="sxs-lookup"><span data-stu-id="8db04-118">Using Visual Studio 2010, open the ThrottledParallelForEach.sln file.</span></span>

2. <span data-ttu-id="8db04-119">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="8db04-119">To build the solution, press CTRL+SHIFT+B.</span></span>

3. <span data-ttu-id="8db04-120">Pour exécuter la solution, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="8db04-120">To run the solution, press F5.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8db04-121">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8db04-121">The samples may already be installed on your machine.</span></span> <span data-ttu-id="8db04-122">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="8db04-122">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="8db04-123">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="8db04-123">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="8db04-124">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="8db04-124">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`