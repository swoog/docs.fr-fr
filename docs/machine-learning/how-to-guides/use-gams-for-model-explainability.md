---
title: Utiliser des modèles additifs généralisés et des fonctions de forme pour l’explication des modèles dans ML.NET
description: Utiliser des modèles additifs généralisés et des fonctions de forme pour l’explication des modèles dans ML.NET
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 7899c0efb80af178ec4fa8623b0712eb9e438e43
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738888"
---
# <a name="use-generalized-additive-models-and-shape-functions-for-model-explainability-in-mlnet"></a><span data-ttu-id="12468-103">Utiliser des modèles additifs généralisés et des fonctions de forme pour l’explication des modèles dans ML.NET</span><span class="sxs-lookup"><span data-stu-id="12468-103">Use Generalized Additive Models and shape functions for model explainability in ML.NET</span></span>

<span data-ttu-id="12468-104">Lorsque vous créez des modèles Machine Learning, se contenter de faire des prédictions n’est souvent pas suffisant.</span><span class="sxs-lookup"><span data-stu-id="12468-104">When creating machine learning models, it is often not enough to simply make predictions.</span></span> <span data-ttu-id="12468-105">Les développeurs Machine Learning, les décideurs et les personnes affectées par les modèles doivent souvent comprendre comment les modèles Machine Learning prennent les décisions et connaître les fonctionnalités qui affectent leurs performances.</span><span class="sxs-lookup"><span data-stu-id="12468-105">Often, machine learning developers, decision makers, and those affected by the models need to understand how machine learning models make decisions and which features contribute to their performance.</span></span> <span data-ttu-id="12468-106">**Les modèles additifs généralisés (GAM)** sont utilisés en interne chez Microsoft pour expliquer les modèles et aider les développeurs Machine Learning à créer des modèles de grande capacité facilement interprétés par d’autres.</span><span class="sxs-lookup"><span data-stu-id="12468-106">**Generalized Additive Models (GAMs)** are used internally at Microsoft for model explainability to help machine learning developers create high-capacity models that can be easily interpreted by others.</span></span>

<span data-ttu-id="12468-107">Les GAM constituent une catégorie de **modèles interprétables** représentant des modèles linéaires où les termes sont des fonctions non linéaires appelées « fonctions de forme » d’une variable unique.</span><span class="sxs-lookup"><span data-stu-id="12468-107">GAMs are a class of **interpretable models** that are linear models where the terms are nonlinear functions, called "shape functions" of a single variable.</span></span> <span data-ttu-id="12468-108">En tant que modèles linéaires, ils sont interprétés facilement, mais comme les modèles apprennent les fonctions de fonctionnalités au lieu d’une pondération unique, ils peuvent modéliser des relations plus complexes qu’un simple modèle linéaire.</span><span class="sxs-lookup"><span data-stu-id="12468-108">As linear models, they are easily interpreted but because the models learn functions of features instead of a single weight, they can model more complex relationships than a simple linear model.</span></span> <span data-ttu-id="12468-109">La prédiction GAM qui en résulte comporte un terme intercept qui représente la prédiction moyenne sur le jeu d’apprentissage ainsi que des fonctions de forme qui représentent l’écart par rapport à la prédiction moyenne.</span><span class="sxs-lookup"><span data-stu-id="12468-109">The resulting GAM predictor has an intercept term that represents the average prediction over the training set, and shape functions that represent the deviation from the average prediction.</span></span> <span data-ttu-id="12468-110">Les fonctions de forme peuvent être inspectées à l’œil nu pour voir la réponse du modèle à différentes valeurs d’une fonctionnalité, puis visualisées comme dans le graphique suivant créé à la fin de l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="12468-110">The shape functions can be inspected by eye to see the response of the model to different values of a feature, and visualized like the following graph that is created at the end of the code example.</span></span> <span data-ttu-id="12468-111">Le formateur GAM dans ML.NET est implémenté à l’aide d’arborescences étroites avec augmentation du gradient (par exemple des souches) afin d’apprendre les fonctions de forme non paramétriques, et il repose sur la méthode décrite dans l’article [Intelligible Models for Classification and Regression](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf) rédigé par Lou, Caruana et Gehrke.</span><span class="sxs-lookup"><span data-stu-id="12468-111">The GAM trainer in ML.NET is implemented using shallow gradient boosted trees (for example tree stumps) to learn nonparametric shape functions, and is based on the method described in [Intelligible Models for Classification and Regression](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf) by Lou, Caruana, and Gehrke.</span></span>

```csharp
// Train the Generalized Additive Model
var fitPipeline = pipeline.Fit(data);
var gamModel = fitPipeline.LastTransformer.Model;

// The intercept for Generalize Additive Models represent the average prediction for the training data
var intercept = gamModel.Intercept;
Console.WriteLine($"Average predicted cost: {intercept:0.00}");

// Get the feature names from the training set
var featureNames = data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Get the index of a variable from the training data
var myFeatureIndex = featureNames.ToList().FindIndex(str => str.Equals("MyFeature"));

// The shape functions represent the deviation from the average prediction as a function of the feature value
// It is represented by a discrete set of bins
// First, get the array of bin upper bounds from the model for this feature
var myFeatureBins = gamModel.GetFeatureBinUpperBounds(myFeatureIndex);
// Then get the array of bin weights; these are the effect size for each bin
var myFeatureWeights = gamModel.GetFeatureWeights(myFeatureIndex);

// Write out the shape function for the feature (see the following figure for what this looks like)
for (int i = 0; i < myFeatureBins.Length; i++)
{
    Console.WriteLine($"x < {myFeatureBins[i]:0.00} => {myFeatureWeights[i]:0.000}");
}
```

![Graphique de fonction de forme de modèles additifs généralisés](./media/use-gams-for-model-explainability/gam-shape-function-graph.png)

<span data-ttu-id="12468-113">Pour obtenir un exemple montrant comment former un modèle GAM afin d’inspecter et d’interpréter les résultats, consultez [le référentiel GitHub dotnet/machinelearning](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/GeneralizedAdditiveModels.cs).</span><span class="sxs-lookup"><span data-stu-id="12468-113">For a sample of how to train a GAM model and inspect and interpret the results, see [the dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/GeneralizedAdditiveModels.cs).</span></span>