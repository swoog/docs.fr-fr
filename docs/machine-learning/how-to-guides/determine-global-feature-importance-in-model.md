---
title: Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
description: Comprendre l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET
ms.date: 12/04/2018
ms.custom: mvc,how-to
ms.openlocfilehash: ebad89aaee1155d7c116b8536307756227dced31
ms.sourcegitcommit: 75567a3cb437009db55949c6092f4e77ed1a9da4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "54307108"
---
# <a name="determine-the-feature-importance-of-models-with-permutation-feature-importance-in-mlnet"></a>Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance dans ML.NET

Lorsque vous créez des modèles Machine Learning, se contenter de faire des prédictions n’est souvent pas suffisant. Les développeurs Machine Learning, les décideurs et les personnes affectées par les modèles doivent souvent comprendre comment les modèles Machine Learning prennent les décisions et connaître les fonctionnalités qui affectent leurs performances. `Permutation Feature Importance` (PFI) est un outil d’explainability de modèle qui est utilisé en interne chez Microsoft pour aider les développeurs de machine learning à mieux comprendre l’importance de fonctionnalité de modèles.

PFI est une technique permettant de déterminer l’**importance de fonctionnalité globale** d’un modèle Machine Learning formé, comme l’explique Breiman dans son article [« Random Forests », section 10](https://www.stat.berkeley.edu/~breiman/randomforest2001.pdf). PFI mesure l’importance de fonctionnalité en posant la question suivante : « Quel serait l’effet sur le modèle si les valeurs d’une fonctionnalité étaient définies selon une valeur * aléatoire ? ». PFI offre l’avantage d’être une méthode indépendante du modèle : elle fonctionne avec n’importe quel modèle pouvant être évalué, et permet d’utiliser n’importe quel jeu de données, pas seulement le jeu d’apprentissage, pour calculer l’importance de fonctionnalité. Vous pouvez donc utiliser PFI pour produire des importances de fonctionnalité comme ce graphique :

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

Pour obtenir un exemple utilisant PFI pour analyser l’importance de fonctionnalité d’un modèle, consultez [le référentiel GitHub dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/samples/Microsoft.ML.Samples/Dynamic/PermutationFeatureImportance).

/* Cette valeur n’est pas exactement aléatoire, mais permutée sur l’ensemble des exemples.
