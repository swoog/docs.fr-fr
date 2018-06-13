---
title: Utilisation de variables avec un Ruleset .NET Framework 3.5
ms.date: 03/30/2017
ms.assetid: 27b56249-22fe-4252-840f-74c0d6c7a6b3
ms.openlocfilehash: 9fa6eaf58aaddc4673f08ec9a9001647a494877d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516854"
---
# <a name="using-variables-with-a-net-framework-35-ruleset"></a><span data-ttu-id="b359e-102">Utilisation de variables avec un Ruleset .NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="b359e-102">Using Variables with a .NET Framework 3.5 Ruleset</span></span>
<span data-ttu-id="b359e-103">Cet exemple montre comment créer un workflow qui utilise l'activité <xref:System.Activities.Statements.Interop> pour une intégrer une activité personnalisée écrite dans [!INCLUDE[netfx35_short](../../../../includes/netfx35-short-md.md)] et qui utilise une stratégie et des règles.</span><span class="sxs-lookup"><span data-stu-id="b359e-103">This sample demonstrates how to create a workflow that uses the <xref:System.Activities.Statements.Interop> activity to integrate a custom activity written in [!INCLUDE[netfx35_short](../../../../includes/netfx35-short-md.md)] that uses policy and rules.</span></span> <span data-ttu-id="b359e-104">Le workflow passe des données à l'activité personnalisée en liant des variables aux propriétés de dépendance exposées par l'activité personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b359e-104">The workflow passes data to the custom activity by binding variables to the dependency properties exposed by the custom activity.</span></span>  
  
## <a name="sample-walkthrough"></a><span data-ttu-id="b359e-105">Exemple de procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="b359e-105">Sample walkthrough</span></span>  
  
#### <a name="to-examine-travelrulelibrary"></a><span data-ttu-id="b359e-106">Pour examiner TravelRuleLibrary</span><span class="sxs-lookup"><span data-stu-id="b359e-106">To examine TravelRuleLibrary</span></span>  
  
1.  <span data-ttu-id="b359e-107">À l’aide de Visual Studio, ouvrez le fichier solution InteropWith35RuleSet.sln.</span><span class="sxs-lookup"><span data-stu-id="b359e-107">Using Visual Studio, open the InteropWith35RuleSet.sln solution file.</span></span>  
  
2.  <span data-ttu-id="b359e-108">Ouvrez TravelRuleSet.cs dans le concepteur de workflow.</span><span class="sxs-lookup"><span data-stu-id="b359e-108">Open the TravelRuleSet.cs in the workflow designer.</span></span>  
  
     <span data-ttu-id="b359e-109">Une activité séquentielle personnalisée qui contient un <xref:System.Workflow.Activities.PolicyActivity> s'affiche.</span><span class="sxs-lookup"><span data-stu-id="b359e-109">A custom sequential activity that contains a <xref:System.Workflow.Activities.PolicyActivity> is displayed.</span></span>  
  
3.  <span data-ttu-id="b359e-110">Double-cliquez sur l'activité de stratégie DiscountPolicy pour examiner les règles.</span><span class="sxs-lookup"><span data-stu-id="b359e-110">Double-click the DiscountPolicy policy activity to examine the rules.</span></span>  
  
     <span data-ttu-id="b359e-111">L'éditeur de règles s'affiche pour présenter les règles.</span><span class="sxs-lookup"><span data-stu-id="b359e-111">The Rules editor pops up to show the rules.</span></span>  
  
4.  <span data-ttu-id="b359e-112">Bouton droit sur le `DiscountPolicy` et sélectionnez le **afficher le Code** option pour examiner le code en regard de code c# pour l’activité.</span><span class="sxs-lookup"><span data-stu-id="b359e-112">Right click the `DiscountPolicy` and select the **View Code** option to examine the code beside C# code for the activity.</span></span>  
  
     <span data-ttu-id="b359e-113">Observez le paramètre de propriété de dépendance pour `DiscountLevel`.</span><span class="sxs-lookup"><span data-stu-id="b359e-113">Observe the dependency property setting for `DiscountLevel`.</span></span> <span data-ttu-id="b359e-114">Cela est équivalent à des arguments dans le [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b359e-114">This is equivalent to arguments in [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)].</span></span> <span data-ttu-id="b359e-115">Pour plus d’informations sur les arguments, consultez [Variables et Arguments](../../../../docs/framework/windows-workflow-foundation/variables-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="b359e-115">For more information about arguments, see [Variables and Arguments](../../../../docs/framework/windows-workflow-foundation/variables-and-arguments.md).</span></span>  
  
## <a name="interopwith35ruleset"></a><span data-ttu-id="b359e-116">InteropWith35RuleSet</span><span class="sxs-lookup"><span data-stu-id="b359e-116">InteropWith35RuleSet</span></span>  
 <span data-ttu-id="b359e-117">C'est un projet de workflow séquentiel qui utilise l'activité <xref:System.Activities.Statements.Interop> pour une intégration à l'ensemble de règles personnalisé créé dans le projet `TravelRuleLibrary`.</span><span class="sxs-lookup"><span data-stu-id="b359e-117">This is a sequential workflow project that uses the <xref:System.Activities.Statements.Interop> activity to integrate with the custom Rule set created in the `TravelRuleLibrary` project.</span></span> <span data-ttu-id="b359e-118">Les variables sont créées sur l'activité <xref:System.Activities.Statements.Sequence> de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b359e-118">Variables are created on the top level <xref:System.Activities.Statements.Sequence> activity.</span></span> <span data-ttu-id="b359e-119">L'activité <xref:System.Activities.Statements.Interop> est utilisée pour une intégration à l'activité `TravelRuleSet`.</span><span class="sxs-lookup"><span data-stu-id="b359e-119">The <xref:System.Activities.Statements.Interop> activity is used to integrate with the `TravelRuleSet` activity.</span></span> <span data-ttu-id="b359e-120">Les variables déclarées sur <xref:System.Activities.Statements.Sequence> sont utilisées pour créer une liaison aux propriétés de dépendance.</span><span class="sxs-lookup"><span data-stu-id="b359e-120">The variables that are declared on the <xref:System.Activities.Statements.Sequence> are used to bind to the dependency properties.</span></span>  
  
## <a name="to-use-this-sample"></a><span data-ttu-id="b359e-121">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="b359e-121">To use this sample</span></span>  
  
1.  <span data-ttu-id="b359e-122">À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution InteropWith35RuleSet.sln.</span><span class="sxs-lookup"><span data-stu-id="b359e-122">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the InteropWith35RuleSet.sln solution file.</span></span>  
  
2.  <span data-ttu-id="b359e-123">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="b359e-123">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="b359e-124">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="b359e-124">To run the solution, press CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b359e-125">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b359e-125">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b359e-126">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b359e-126">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b359e-127">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="b359e-127">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b359e-128">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="b359e-128">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\InteropWith35RuleSet`