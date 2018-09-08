---
title: Validation des relations des activités
ms.date: 03/30/2017
ms.assetid: 6f11a34e-ed67-4bce-88ce-7e96bbb4d052
ms.openlocfilehash: 50f08118fb5ad4d9b8fe809e7ab3cc5d57f28149
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44193664"
---
# <a name="activity-relationships-validation"></a><span data-ttu-id="184a2-102">Validation des relations des activités</span><span class="sxs-lookup"><span data-stu-id="184a2-102">Activity Relationships Validation</span></span>
<span data-ttu-id="184a2-103">Cet exemple se compose de trois activités, `CreateCity`, `CreateState` et `CreateCountry`.</span><span class="sxs-lookup"><span data-stu-id="184a2-103">This sample consists of three activities, `CreateCity`, `CreateState`, and `CreateCountry`.</span></span> <span data-ttu-id="184a2-104">`CreateCity` doit être à l'intérieur d'une activité `CreateState`, et `CreateState` à l'intérieur d'une activité `CreateCountry`.</span><span class="sxs-lookup"><span data-stu-id="184a2-104">`CreateCity` must be inside a `CreateState` activity, and `CreateState` must be inside a `CreateCountry` activity.</span></span> <span data-ttu-id="184a2-105">Pour les besoins de cet exemple, la logique de validation est dans le code pour l'activité `CreateState`, et dans XAML pour l'activité `CreateCity`.</span><span class="sxs-lookup"><span data-stu-id="184a2-105">For the purpose of this sample, the validation logic is in code for the `CreateState` activity, and in XAML for the `CreateCity` activity.</span></span> <span data-ttu-id="184a2-106">Les deux contraintes ont le même comportement.</span><span class="sxs-lookup"><span data-stu-id="184a2-106">Both constraints have the same behavior.</span></span>  
  
 <span data-ttu-id="184a2-107">[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] fournit les trois activités d'assistance suivantes qui permettent au développeur de valider les relations entre les activités :</span><span class="sxs-lookup"><span data-stu-id="184a2-107">The [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] provides the following three helper activities that allow the developer to validate relationships between activities:</span></span>  
  
 <xref:System.Activities.Validation.GetParentChain>  
 <span data-ttu-id="184a2-108">Fournit la collection de toutes les activités qui appartiennent au parent du nœud actuel</span><span class="sxs-lookup"><span data-stu-id="184a2-108">Provides the collection of all activities that belong to the parent of the current node</span></span>  
  
 <xref:System.Activities.Validation.GetChildSubtree>  
 <span data-ttu-id="184a2-109">Fournit la collection de toutes les activités qui appartiennent à la sous-arborescence du nœud actuel, à l'exclusion du nœud actuel</span><span class="sxs-lookup"><span data-stu-id="184a2-109">Provides the collection of all activities that belong to the sub-tree of the current node, excluding the current node</span></span>  
  
 <xref:System.Activities.Validation.GetWorkflowTree>  
 <span data-ttu-id="184a2-110">Fournit la collection de toutes les activités de la même arborescence que le nœud actuel</span><span class="sxs-lookup"><span data-stu-id="184a2-110">Provides the collection of all activities in the same tree as the current node</span></span>  
  
 <span data-ttu-id="184a2-111">Dans l'exemple, une activité <xref:System.Activities.Statements.ForEach%601> est utilisée pour parcourir la collection retournée par <xref:System.Activities.Validation.GetParentChain></span><span class="sxs-lookup"><span data-stu-id="184a2-111">In the sample, a <xref:System.Activities.Statements.ForEach%601> activity is used to walk through the collection returned by <xref:System.Activities.Validation.GetParentChain>.</span></span> <span data-ttu-id="184a2-112">Pour chaque élément de la collection, son type est comparé à `CreateCountry` (ou à `CreateState` si `CreateCity` est validé). Une fois que qu'une correspondance est trouvée, l'indicateur de résultat a la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="184a2-112">For every element in the collection, its type is compared to `CreateCountry` (or `CreateState` if `CreateCity` is being validated), and when a match is found the result flag is set to `true`.</span></span> <span data-ttu-id="184a2-113">Enfin, un <xref:System.Activities.Validation.AssertValidation> est utilisé pour générer une erreur de validation si l'indicateur de résultat a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="184a2-113">Finally, an <xref:System.Activities.Validation.AssertValidation> is used to generate a validation error if the result flag is set to `false`.</span></span>  
  
### <a name="to-use-this-sample"></a><span data-ttu-id="184a2-114">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="184a2-114">To use this sample</span></span>  
  
1.  <span data-ttu-id="184a2-115">Ouvrez l'exemple de solution ContainmentValidation.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="184a2-115">Open the ContainmentValidation.sln sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="184a2-116">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="184a2-116">Build the solution.</span></span>  
  
3.  <span data-ttu-id="184a2-117">Appuyez sur Ctrl+F5 pour lancer le programme.</span><span class="sxs-lookup"><span data-stu-id="184a2-117">Press CTRL + F5 to launch the program.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="184a2-118">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="184a2-118">The samples may already be installed on your computer.</span></span> <span data-ttu-id="184a2-119">Recherchez le répertoire (par défaut) suivant avant de continuer :</span><span class="sxs-lookup"><span data-stu-id="184a2-119">Check for the following (default) directory before continuing:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="184a2-120">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="184a2-120">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="184a2-121">Cet exemple se trouve dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="184a2-121">This sample is located in the following directory:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Validation\ActivityRelationships`
