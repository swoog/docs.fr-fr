---
title: Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
description: Comprendre l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
ms.date: 12/04/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 4b93e085dbb99e7f6f5a0a839b863aad1c69c7ba
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156567"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a><span data-ttu-id="f59e0-103">Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET</span><span class="sxs-lookup"><span data-stu-id="f59e0-103">Determine the feature importance of models with Permutation Feature Importance in ML.NET</span></span>

<span data-ttu-id="f59e0-104">Lorsque vous créez des modèles Machine Learning, se contenter de faire des prédictions n’est souvent pas suffisant.</span><span class="sxs-lookup"><span data-stu-id="f59e0-104">When creating machine learning models, it is often not enough to simply make predictions.</span></span> <span data-ttu-id="f59e0-105">Les développeurs Machine Learning, les décideurs et les personnes affectées par les modèles doivent souvent comprendre comment les modèles Machine Learning prennent les décisions et connaître les fonctionnalités qui affectent leurs performances.</span><span class="sxs-lookup"><span data-stu-id="f59e0-105">Often, machine learning developers, decision makers, and those affected by the models need to understand how machine learning models make decisions and which features contribute to their performance.</span></span> <span data-ttu-id="f59e0-106">`Permutation Feature Importance` (PFI) est un outil d’explainability de modèle qui est utilisé en interne chez Microsoft pour aider les développeurs de machine learning à mieux comprendre l’importance de fonctionnalité de modèles.</span><span class="sxs-lookup"><span data-stu-id="f59e0-106">`Permutation Feature Importance` (PFI) is a model explainability tool that is used internally at Microsoft to help machine learning developers better understand the feature importance of models.</span></span>

<span data-ttu-id="f59e0-107">PFI est une technique permettant de déterminer l’**importance de fonctionnalité globale** d’un modèle Machine Learning formé, comme l’explique Breiman dans son article [« Random Forests », section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf).</span><span class="sxs-lookup"><span data-stu-id="f59e0-107">PFI is a technique to determine **global feature importance** in a trained machine learning model, motivated by Breiman in the ["Random Forests" paper, section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf).</span></span> <span data-ttu-id="f59e0-108">PFI mesure l’importance de fonctionnalité en posant la question suivante : « Quel serait l’effet sur le modèle si les valeurs d’une fonctionnalité étaient définies selon une valeur \* aléatoire ? ».</span><span class="sxs-lookup"><span data-stu-id="f59e0-108">PFI measures feature importance by asking the question, "What would the effect on the model be if the values for a feature were set to a random\* value?".</span></span> <span data-ttu-id="f59e0-109">PFI offre l’avantage d’être une méthode indépendante du modèle : elle fonctionne avec n’importe quel modèle pouvant être évalué, et permet d’utiliser n’importe quel jeu de données, pas seulement le jeu d’apprentissage, pour calculer l’importance de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f59e0-109">The advantage of the PFI method is that it is model agnostic — it works with any model that can be evaluated — and it can use any dataset, not just the training set, to compute feature importance.</span></span> <span data-ttu-id="f59e0-110">Vous pouvez donc utiliser PFI pour produire des importances de fonctionnalité comme ce graphique :</span><span class="sxs-lookup"><span data-stu-id="f59e0-110">You can use PFI like so to produce feature importances like this graph:</span></span>

![Graphique d’importance de fonctionnalité de permutation](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model, data);
 
// Get the feature names from the training set
var featureNames = data.Schema.GetColumns()
                .Select(tuple => tuple.column.Name) // Get the column names
                .Where(name => name != labelName) // Drop the Label
                .ToArray();
 
// Write out the feature names and their importance to the model's R-squared value
for (int i = 0; i < featureNames.Length; i++)
  Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].rSquared:G4}");
```

<span data-ttu-id="f59e0-112">Pour obtenir un exemple utilisant PFI pour analyser l’importance de fonctionnalité d’un modèle, consultez [le référentiel GitHub dotnet/machinelearning](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance.cs).</span><span class="sxs-lookup"><span data-stu-id="f59e0-112">For a sample using PFI to analyze the feature importance of a model, see [the dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance.cs).</span></span>

<span data-ttu-id="f59e0-113">/\* Cette valeur n’est pas exactement aléatoire, mais permutée sur l’ensemble des exemples.</span><span class="sxs-lookup"><span data-stu-id="f59e0-113">/\* Well, not random exactly, but permuted across the set of examples.</span></span>
