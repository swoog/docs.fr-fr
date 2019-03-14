---
title: Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
description: Comprendre l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: b0457bc07168579403e5a00383864c5612e1d17f
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57675548"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a>Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Lorsque vous créez des modèles Machine Learning, se contenter de faire des prédictions n’est souvent pas suffisant. Les développeurs Machine Learning, les décideurs et les personnes affectées par les modèles doivent souvent comprendre comment les modèles Machine Learning prennent les décisions et connaître les fonctionnalités qui affectent leurs performances. `Permutation Feature Importance` (PFI) est un outil d’explainability de modèle qui est utilisé en interne chez Microsoft pour aider les développeurs de machine learning à mieux comprendre l’importance de fonctionnalité de modèles.

PFI est une technique permettant de déterminer l’**importance de fonctionnalité globale** d’un modèle Machine Learning formé, comme l’explique Breiman dans son article [« Random Forests », section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf). PFI mesure l’importance de fonctionnalité en posant la question suivante : « Quel serait l’effet sur le modèle si les valeurs d’une fonctionnalité étaient définies selon une valeur * aléatoire ? ». PFI offre l’avantage d’être une méthode indépendante du modèle : elle fonctionne avec n’importe quel modèle pouvant être évalué, et permet d’utiliser n’importe quel jeu de données, pas seulement le jeu d’apprentissage, pour calculer l’importance de fonctionnalité. Vous pouvez donc utiliser PFI pour produire des importances de fonctionnalité comme ce graphique :

![Graphique d’importance de fonctionnalité de permutation](./media/determine-global-feature-importance-in-model/pfi-graph.png)

```csharp
// Compute the feature importance using PFI
var permutationMetrics = mlContext.Regression.PermutationFeatureImportance(model.LastTransformer, model.Transform(data), "MedianHomeValue");

// Get the feature names from the training set
var featureNames =
    data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Write out the feature names and their importance to the model's Mean R-squared value
for (int i = 0; i < featureNames.Length;i++)
{
    Console.WriteLine($"{featureNames[i]}\t{permutationMetrics[i].RSquared.Mean:G4}");
}
```

Pour obtenir un exemple utilisant PFI pour analyser l’importance de fonctionnalité d’un modèle, consultez [le référentiel GitHub dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance).

/* Cette valeur n’est pas exactement aléatoire, mais permutée sur l’ensemble des exemples.
