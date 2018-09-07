---
title: Advanced Policy
ms.date: 03/30/2017
ms.assetid: 75a22c88-5e54-4ae8-84cb-fbb22a612f0a
ms.openlocfilehash: becdc28affd877239474d6f0f007a480297bccb8
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44083788"
---
# <a name="advanced-policy"></a><span data-ttu-id="2eec0-102">Advanced Policy</span><span class="sxs-lookup"><span data-stu-id="2eec0-102">Advanced Policy</span></span>
<span data-ttu-id="2eec0-103">Cet exemple complète l'exemple de stratégie simple.</span><span class="sxs-lookup"><span data-stu-id="2eec0-103">This sample extends the Simple Policy sample.</span></span> <span data-ttu-id="2eec0-104">Outre les règles de remise résidentielle et de remise d'entreprise traitées dans l'exemple de stratégie simple, plusieurs nouvelles règles ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="2eec0-104">In addition to the residential discount and business discount rules from the Simple Policy example, several new rules have been added.</span></span>  
  
 <span data-ttu-id="2eec0-105">Une règle de valeur élevée est ajoutée afin de proposer une remise plus importante pour les commandes à valeur élevée.</span><span class="sxs-lookup"><span data-stu-id="2eec0-105">A high-value rule is added, which provides a bigger discount for high-value orders.</span></span> <span data-ttu-id="2eec0-106">Sa valeur de priorité est inférieure à celle des deux règles précédentes de sorte qu'elle remplace le champ de remise et reste prioritaire par rapport aux règles de remise résidentielle et d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="2eec0-106">It is given a priority value less than the previous two rules so that it will overwrite the discount field and take precedence over both the residential and business discount rules.</span></span>  
  
 <span data-ttu-id="2eec0-107">Une règle de calcul du total est également ajoutée afin de calculer le montant total en fonction du niveau de remise.</span><span class="sxs-lookup"><span data-stu-id="2eec0-107">A calculate total rule is also added, which computes the total based on the discount level.</span></span> <span data-ttu-id="2eec0-108">Elle indique comment faire référence à une méthode définie sur l'activité de workflow et comment utiliser des actions Else.</span><span class="sxs-lookup"><span data-stu-id="2eec0-108">It shows how to reference a method defined on the workflow activity, as well as how to use else actions.</span></span> <span data-ttu-id="2eec0-109">Cette règle illustre également le comportement de chaînage puisqu'elle sera évaluée à chaque modification du champ de remise.</span><span class="sxs-lookup"><span data-stu-id="2eec0-109">This rule also demonstrates chaining behavior since it will be evaluated anytime the discount field changes.</span></span> <span data-ttu-id="2eec0-110">En outre, l'attribution de méthode est illustrée avec la classe RuleWriteAttribute sur la méthode CalculateTotal.</span><span class="sxs-lookup"><span data-stu-id="2eec0-110">Furthermore, method attributing is shown with the RuleWriteAttribute on the CalculateTotal method.</span></span> <span data-ttu-id="2eec0-111">Les règles impliquées (ErrorTotalRule) doivent être réévaluées chaque fois que la méthode est exécutée.</span><span class="sxs-lookup"><span data-stu-id="2eec0-111">This causes impacted rules (ErrorTotalRule) to be re-evaluated whenever the method gets executed.</span></span>  
  
 <span data-ttu-id="2eec0-112">La dernière règle ajoutée détecte les erreurs (dans le cas présent, Total inférieur à 0).</span><span class="sxs-lookup"><span data-stu-id="2eec0-112">The last rule added is one that detects errors (in this case, Total less than 0).</span></span> <span data-ttu-id="2eec0-113">Si cela se produit, l'exécution de la stratégie est interrompue.</span><span class="sxs-lookup"><span data-stu-id="2eec0-113">If this occurs, the policy execution is halted.</span></span>  
  
 <span data-ttu-id="2eec0-114">Enfin, les appels `Console.Writeline` sont ajoutés en tant qu'actions à chaque règle afin d'apporter plus de visibilité à l'exécution de la règle, tout en montrant également qu'il est possible d'accéder aux méthodes statiques sur les types référencés.</span><span class="sxs-lookup"><span data-stu-id="2eec0-114">Finally, `Console.Writeline` calls are added as actions to each rule to provide more visibility into rule execution, while also showing that it is possible to access static methods on referenced types.</span></span> <span data-ttu-id="2eec0-115">Vous pouvez également utiliser le traçage pour obtenir une meilleure visibilité des règles exécutées.</span><span class="sxs-lookup"><span data-stu-id="2eec0-115">You could also use tracking to get visibility into the rules that are executed.</span></span>  
  
 <span data-ttu-id="2eec0-116">Les règles utilisées dans cet exemple sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2eec0-116">The rules used in this sample are:</span></span>  
  
 <span data-ttu-id="2eec0-117">**ResidentialDiscountRule :**</span><span class="sxs-lookup"><span data-stu-id="2eec0-117">**ResidentialDiscountRule:**</span></span>  
  
 <span data-ttu-id="2eec0-118">IF OrderValue > 500 AND CustomerType = Residential</span><span class="sxs-lookup"><span data-stu-id="2eec0-118">IF OrderValue > 500 AND CustomerType = Residential</span></span>  
  
 <span data-ttu-id="2eec0-119">THEN Discount = 5%</span><span class="sxs-lookup"><span data-stu-id="2eec0-119">THEN Discount = 5%</span></span>  
  
 <span data-ttu-id="2eec0-120">**BusinessDiscountRule :**</span><span class="sxs-lookup"><span data-stu-id="2eec0-120">**BusinessDiscountRule:**</span></span>  
  
 <span data-ttu-id="2eec0-121">IF OrderValue > 10000 AND CustomerType = Business</span><span class="sxs-lookup"><span data-stu-id="2eec0-121">IF OrderValue > 10000 AND CustomerType = Business</span></span>  
  
 <span data-ttu-id="2eec0-122">THEN Discount = 10%</span><span class="sxs-lookup"><span data-stu-id="2eec0-122">THEN Discount = 10%</span></span>  
  
 <span data-ttu-id="2eec0-123">**HighValueDiscountRule :**</span><span class="sxs-lookup"><span data-stu-id="2eec0-123">**HighValueDiscountRule:**</span></span>  
  
 <span data-ttu-id="2eec0-124">IF OrderValue > 20000</span><span class="sxs-lookup"><span data-stu-id="2eec0-124">IF OrderValue > 20000</span></span>  
  
 <span data-ttu-id="2eec0-125">THEN Discount = 15%</span><span class="sxs-lookup"><span data-stu-id="2eec0-125">THEN Discount = 15%</span></span>  
  
 <span data-ttu-id="2eec0-126">**TotalRule :**</span><span class="sxs-lookup"><span data-stu-id="2eec0-126">**TotalRule:**</span></span>  
  
 <span data-ttu-id="2eec0-127">IF Discount > 0</span><span class="sxs-lookup"><span data-stu-id="2eec0-127">IF Discount > 0</span></span>  
  
 <span data-ttu-id="2eec0-128">THEN CalculateTotal(OrderValue, Discount)</span><span class="sxs-lookup"><span data-stu-id="2eec0-128">THEN CalculateTotal(OrderValue, Discount)</span></span>  
  
 <span data-ttu-id="2eec0-129">ELSE Total = OrderValue</span><span class="sxs-lookup"><span data-stu-id="2eec0-129">ELSE Total = OrderValue</span></span>  
  
 <span data-ttu-id="2eec0-130">**Impliquées ErrorTotalRule :**</span><span class="sxs-lookup"><span data-stu-id="2eec0-130">**ErrorTotalRule:**</span></span>  
  
 <span data-ttu-id="2eec0-131">IF Total \< 0</span><span class="sxs-lookup"><span data-stu-id="2eec0-131">IF Total \< 0</span></span>  
  
 <span data-ttu-id="2eec0-132">THEN Error = "Fired ErrorTotalRule"; Halt</span><span class="sxs-lookup"><span data-stu-id="2eec0-132">THEN Error = "Fired ErrorTotalRule"; Halt</span></span>  
  
 <span data-ttu-id="2eec0-133">L'évaluation et l'exécution des règles peuvent également être consultées par traçage et suivi.</span><span class="sxs-lookup"><span data-stu-id="2eec0-133">Rule evaluation and execution can also be seen through tracing and tracking.</span></span>  
  
### <a name="to-build-the-sample"></a><span data-ttu-id="2eec0-134">Pour générer l'exemple</span><span class="sxs-lookup"><span data-stu-id="2eec0-134">To build the sample</span></span>  
  
1.  <span data-ttu-id="2eec0-135">Ouvrez la solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="2eec0-135">Open the solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="2eec0-136">Générez la solution en appuyant sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="2eec0-136">Build the solution by pressing CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="2eec0-137">Exécutez la solution sans débogage en appuyant sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="2eec0-137">Run the solution without debugging by pressing CTRL+F5.</span></span>  
  
### <a name="to-run-the-sample"></a><span data-ttu-id="2eec0-138">Pour exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="2eec0-138">To run the sample</span></span>  
  
-   <span data-ttu-id="2eec0-139">Dans la fenêtre d'invite de commandes du Kit de développement logiciel (SDK), exécutez le fichier .exe dans le dossier AdvancedPolicy\bin\debug (ou le dossier AdvancedPolicy\bin pour la version Visual Basic de l'exemple), situé sous le dossier principal de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="2eec0-139">In the SDK Command Prompt window, run the .exe file in the AdvancedPolicy\bin\debug folder (or the AdvancedPolicy \bin folder for the Visual Basic version of the sample), which is located below the main folder for the sample.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="2eec0-140">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2eec0-140">The samples may already be installed on your computer.</span></span> <span data-ttu-id="2eec0-141">Recherchez le répertoire (par défaut) suivant avant de continuer :</span><span class="sxs-lookup"><span data-stu-id="2eec0-141">Check for the following (default) directory before continuing:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="2eec0-142">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="2eec0-142">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="2eec0-143">Cet exemple se trouve dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="2eec0-143">This sample is located in the following directory:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Rules\Policy\AdvancedPolicy`  
  
## <a name="see-also"></a><span data-ttu-id="2eec0-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eec0-144">See Also</span></span>  
 <xref:System.Workflow.Activities.Rules.RuleSet>  
 <xref:System.Workflow.Activities.PolicyActivity>  
 [<span data-ttu-id="2eec0-145">Stratégie simple</span><span class="sxs-lookup"><span data-stu-id="2eec0-145">Simple Policy</span></span>](../../../../docs/framework/windows-workflow-foundation/samples/simple-policy.md)
