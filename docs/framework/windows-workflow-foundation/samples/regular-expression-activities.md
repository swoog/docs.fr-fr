---
title: Activités d'expression régulière
ms.date: 03/30/2017
ms.assetid: b8f24694-49db-4339-92ec-014e3d4ae63b
ms.openlocfilehash: 50daa5b6d7baab37f372de4c30c2e0d12b4fa943
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45668949"
---
# <a name="regular-expression-activities"></a><span data-ttu-id="9d8b8-102">Activités d'expression régulière</span><span class="sxs-lookup"><span data-stu-id="9d8b8-102">Regular Expression Activities</span></span>
<span data-ttu-id="9d8b8-103">Cet exemple montre comment créer un ensemble d'activités qui exposent la fonctionnalité d'expression régulière de l'espace de noms <xref:System.Text.RegularExpressions>.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-103">This sample demonstrates how to create a set of activities that expose the regular expression functionality of the <xref:System.Text.RegularExpressions> namespace.</span></span> <span data-ttu-id="9d8b8-104">Ces activités personnalisées peuvent être utilisées dans une application de workflow.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-104">These custom activities can be used within a workflow application.</span></span> <span data-ttu-id="9d8b8-105">Pour plus d’informations sur les expressions régulières, consultez [System.Text.RegularExpressions](https://go.microsoft.com/fwlink/?LinkId=150434) Namespace.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-105">For more information about regular expressions, see [N:System.Text.RegularExpressions](https://go.microsoft.com/fwlink/?LinkId=150434) Namespace.</span></span>  
  
 <span data-ttu-id="9d8b8-106">Le tableau suivant détaille les activités personnalisées dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-106">The following table details the custom activities in this sample.</span></span>  
  
|<span data-ttu-id="9d8b8-107">Activité</span><span class="sxs-lookup"><span data-stu-id="9d8b8-107">Activity</span></span>|<span data-ttu-id="9d8b8-108">Description</span><span class="sxs-lookup"><span data-stu-id="9d8b8-108">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="9d8b8-109">IsMatch</span><span class="sxs-lookup"><span data-stu-id="9d8b8-109">IsMatch</span></span>|<span data-ttu-id="9d8b8-110">Spécifie si l'expression régulière a trouvé une correspondance dans la chaîne d'entrée.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-110">Specifies whether the regular expression found a match in the input string.</span></span>|  
|<span data-ttu-id="9d8b8-111">Correspondance</span><span class="sxs-lookup"><span data-stu-id="9d8b8-111">Matches</span></span>|<span data-ttu-id="9d8b8-112">Recherche une chaîne d'entrée pour toutes les occurrences d'une expression régulière et retourne toutes les correspondances réussies.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-112">Searches an input string for all occurrences of a regular expression and returns all the successful matches.</span></span>|  
|<span data-ttu-id="9d8b8-113">Remplacer</span><span class="sxs-lookup"><span data-stu-id="9d8b8-113">Replace</span></span>|<span data-ttu-id="9d8b8-114">Dans une chaîne d'entrée spécifiée, remplace les chaînes qui correspondent à un modèle d'expression régulière par une chaîne de remplacement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-114">Within a specified input string, replaces strings that match a regular expression pattern with a specified replacement string.</span></span>|  
  
## <a name="ismatch"></a><span data-ttu-id="9d8b8-115">IsMatch</span><span class="sxs-lookup"><span data-stu-id="9d8b8-115">IsMatch</span></span>  
 <span data-ttu-id="9d8b8-116">L'activité personnalisée `IsMatch` retourne la valeur `true` si la propriété de type chaîne `Input` trouve une correspondance dans l'expression régulière spécifiée dans la propriété `Pattern`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-116">The `IsMatch` custom activity returns `true` if the `Input` string property finds a match in the regular expression specified in the `Pattern` property.</span></span> <span data-ttu-id="9d8b8-117">L'activité dérive de <xref:System.Activities.CodeActivity%601> et, dans la méthode <xref:System.Activities.CodeActivity%601.Execute%2A>, appelle la méthode <xref:System.Text.RegularExpressions.Regex.IsMatch%2A>.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-117">The activity derives from <xref:System.Activities.CodeActivity%601> and within the <xref:System.Activities.CodeActivity%601.Execute%2A> method calls the <xref:System.Text.RegularExpressions.Regex.IsMatch%2A> method.</span></span>  
  
 <span data-ttu-id="9d8b8-118">Le tableau suivant décrit les propriétés et la valeur de retour pour l'activité personnalisée `IsMatch`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-118">The following table describes the properties and return value for the `IsMatch` custom activity.</span></span>  
  
|<span data-ttu-id="9d8b8-119">Propriété ou valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-119">Property or Return Value</span></span>|<span data-ttu-id="9d8b8-120">Description</span><span class="sxs-lookup"><span data-stu-id="9d8b8-120">Description</span></span>|  
|------------------------------|-----------------|  
|<span data-ttu-id="9d8b8-121">Pattern (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-121">Pattern (required)</span></span>|<span data-ttu-id="9d8b8-122">Expression régulière avec laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-122">The regular expression to search with.</span></span>|  
|<span data-ttu-id="9d8b8-123">Input (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-123">Input (required)</span></span>|<span data-ttu-id="9d8b8-124">Chaîne d'entrée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-124">The input string to search.</span></span>|  
|<span data-ttu-id="9d8b8-125">RegexOptions</span><span class="sxs-lookup"><span data-stu-id="9d8b8-125">RegexOptions</span></span>|<span data-ttu-id="9d8b8-126">Combinaison d’opérations OR [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-126">Bitwise OR combination of [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) enumeration values.</span></span>|  
|<span data-ttu-id="9d8b8-127">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-127">Return value</span></span>|<span data-ttu-id="9d8b8-128">`true` si l'entrée trouve une correspondance dans le modèle fourni ; sinon `false`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-128">`true` if the input finds a match in the provided pattern; otherwise `false`.</span></span>|  
  
 <span data-ttu-id="9d8b8-129">L'exemple de code suivant montre comment utiliser l'activité personnalisée `IsMatch`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-129">The following code example demonstrates how to use the `IsMatch` custom activity.</span></span>  
  
```  
new IsMatch  
{  
    Pattern = new InArgument<string>( @"^-?\d+(\.\d{2})?$"),  
    Input = "20.00",  
};  
```  
  
## <a name="matches"></a><span data-ttu-id="9d8b8-130">Correspondance</span><span class="sxs-lookup"><span data-stu-id="9d8b8-130">Matches</span></span>  
 <span data-ttu-id="9d8b8-131">L'activité personnalisée `Matches` recherche une chaîne d'entrée pour toutes les occurrences d'une expression régulière et retourne toutes les correspondances réussies.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-131">The `Matches` custom activity searches an input string for all occurrences of a regular expression and returns all the successful matches.</span></span> <span data-ttu-id="9d8b8-132">L'activité dérive de <xref:System.Activities.CodeActivity%601> et, dans la méthode <xref:System.Activities.CodeActivity%601.Execute%2A>, appelle la méthode <xref:System.Text.RegularExpressions.Regex.Matches%2A>.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-132">The activity derives from <xref:System.Activities.CodeActivity%601> and within the <xref:System.Activities.CodeActivity%601.Execute%2A> method calls the <xref:System.Text.RegularExpressions.Regex.Matches%2A> method.</span></span>  
  
 <span data-ttu-id="9d8b8-133">Le tableau suivant décrit les propriétés et la valeur de retour pour l'activité personnalisée `IsMatch`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-133">The following table describes the properties and return value for the `IsMatch` custom activity.</span></span>  
  
|<span data-ttu-id="9d8b8-134">Propriété ou valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-134">Property or Return Value</span></span>|<span data-ttu-id="9d8b8-135">Description</span><span class="sxs-lookup"><span data-stu-id="9d8b8-135">Description</span></span>|  
|------------------------------|-----------------|  
|<span data-ttu-id="9d8b8-136">Pattern (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-136">Pattern (required)</span></span>|<span data-ttu-id="9d8b8-137">Expression régulière avec laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-137">The regular expression to search with.</span></span>|  
|<span data-ttu-id="9d8b8-138">Input (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-138">Input (required)</span></span>|<span data-ttu-id="9d8b8-139">Chaîne d'entrée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-139">The input string to search.</span></span>|  
|<span data-ttu-id="9d8b8-140">RegexOptions</span><span class="sxs-lookup"><span data-stu-id="9d8b8-140">RegexOptions</span></span>|<span data-ttu-id="9d8b8-141">Combinaison d’opérations OR [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-141">Bitwise OR combination of [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) enumeration values.</span></span>|  
|<span data-ttu-id="9d8b8-142">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-142">Return Value</span></span>|<span data-ttu-id="9d8b8-143"><xref:System.Text.RegularExpressions.MatchCollection> qui contient la collection des correspondances réussies.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-143">A <xref:System.Text.RegularExpressions.MatchCollection> that contains the collection of successful matches.</span></span>|  
  
 <span data-ttu-id="9d8b8-144">L'exemple de code suivant montre comment utiliser l'activité personnalisée `Matches`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-144">The following code example demonstrates how to use the `Matches` custom activity.</span></span>  
  
```  
new Matches  
{  
    Pattern = @"\b(?<word>\w+)\s+(\k<word>)\b",  
    Input = "The quick brown fox  fox jumped over over the lazy dog dog.",  
};  
```  
  
## <a name="replace"></a><span data-ttu-id="9d8b8-145">Remplacer</span><span class="sxs-lookup"><span data-stu-id="9d8b8-145">Replace</span></span>  
 <span data-ttu-id="9d8b8-146">L'activité personnalisée `Replace` recherche une chaîne d'entrée et remplace toutes les chaînes qui correspondent à une expression régulière spécifiée par une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-146">The `Replace` custom activity searches an input string and replaces all strings that match a specified regular expression with a string.</span></span> <span data-ttu-id="9d8b8-147">L'activité dérive de <xref:System.Activities.CodeActivity%601> et, dans la méthode <xref:System.Activities.CodeActivity%601.Execute%2A>, appelle la méthode <xref:System.Text.RegularExpressions.Regex.Replace%2A>.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-147">The activity derives from <xref:System.Activities.CodeActivity%601> and within the <xref:System.Activities.CodeActivity%601.Execute%2A> method calls the <xref:System.Text.RegularExpressions.Regex.Replace%2A> method.</span></span>  
  
 <span data-ttu-id="9d8b8-148">Le tableau suivant décrit les propriétés et la valeur de retour pour l'activité personnalisée `Replace`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-148">The following table describes the properties and return value for the `Replace` custom activity.</span></span>  
  
|<span data-ttu-id="9d8b8-149">Propriété ou valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-149">Property or Return Value</span></span>|<span data-ttu-id="9d8b8-150">Description</span><span class="sxs-lookup"><span data-stu-id="9d8b8-150">Description</span></span>|  
|------------------------------|-----------------|  
|<span data-ttu-id="9d8b8-151">Pattern (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-151">Pattern (required)</span></span>|<span data-ttu-id="9d8b8-152">Expression régulière avec laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-152">The regular expression to search with.</span></span>|  
|<span data-ttu-id="9d8b8-153">Input (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="9d8b8-153">Input (required)</span></span>|<span data-ttu-id="9d8b8-154">Chaîne d'entrée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-154">The input string to search.</span></span>|  
|<span data-ttu-id="9d8b8-155">Replacement</span><span class="sxs-lookup"><span data-stu-id="9d8b8-155">Replacement</span></span>|<span data-ttu-id="9d8b8-156">Chaîne de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-156">The replacement string.</span></span><br /><br /> <span data-ttu-id="9d8b8-157">Si un `Replacement` est spécifié, la propriété `MatchEvaluator` est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-157">If a `Replacement` is specified, then the `MatchEvaluator` property is ignored.</span></span> <span data-ttu-id="9d8b8-158">La propriété `Replacement` ou `MatchEvaluator` doit être définie.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-158">Either the `Replacement` or `MatchEvaluator` property must be set.</span></span>|  
|<span data-ttu-id="9d8b8-159">MatchEvaluator</span><span class="sxs-lookup"><span data-stu-id="9d8b8-159">MatchEvaluator</span></span>|<span data-ttu-id="9d8b8-160">Méthode personnalisée qui examine chaque correspondance et retourne la chaîne correspondante d'origine ou une chaîne de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-160">A custom method that examines each match and returns either the original matched string or a replacement string.</span></span><br /><br /> <span data-ttu-id="9d8b8-161">Si un `Replacement` est spécifié, la propriété `MatchEvaluator` est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-161">If a `Replacement` is specified, then the `MatchEvaluator` property is ignored.</span></span> <span data-ttu-id="9d8b8-162">La propriété `Replacement` ou `MatchEvaluator` doit être définie.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-162">Either the `Replacement` or `MatchEvaluator` property must be set.</span></span>|  
|<span data-ttu-id="9d8b8-163">RegexOptions</span><span class="sxs-lookup"><span data-stu-id="9d8b8-163">RegexOptions</span></span>|<span data-ttu-id="9d8b8-164">Combinaison d’opérations OR [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-164">Bitwise OR combination of [RegexOptions](https://go.microsoft.com/fwlink/?LinkId=150446) enumeration values.</span></span>|  
|<span data-ttu-id="9d8b8-165">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9d8b8-165">Return Value</span></span>|<span data-ttu-id="9d8b8-166"><xref:System.Text.RegularExpressions.MatchCollection> qui contient la collection des correspondances réussies.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-166">A <xref:System.Text.RegularExpressions.MatchCollection> that contains the collection of successful matches.</span></span>|  
  
 <span data-ttu-id="9d8b8-167">L'exemple de code suivant montre comment utiliser l'activité personnalisée `Replace`.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-167">The following code example demonstrates how to use the `Replace` custom activity.</span></span>  
  
```  
// Using the replacement string.  
new Replace  
{  
    Pattern = @"\bWorld\b",  
    Input = "Hello World! This is a wonderful World",  
    Replacement = "Universe"  
};  
  
// Using a match evaluator.  
new Replace  
{  
    Pattern = new InArgument<string>(pattern),  
    Input = new InArgument<string>(input),  
    MatchEvaluator = new MatchEvaluator(CapText)                  
};  
```  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="9d8b8-168">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="9d8b8-168">To use this sample</span></span>  
  
1.  <span data-ttu-id="9d8b8-169">À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution RegexActivities.sln.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-169">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the RegexActivities.sln solution file.</span></span>  
  
2.  <span data-ttu-id="9d8b8-170">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-170">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="9d8b8-171">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-171">To run the solution, press CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="9d8b8-172">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-172">The samples may already be installed on your machine.</span></span> <span data-ttu-id="9d8b8-173">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-173">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="9d8b8-174">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-174">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9d8b8-175">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="9d8b8-175">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\Regex`