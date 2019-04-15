---
title: Entraîner un modèle Machine Learning en utilisant la validation croisée - ML.NET
description: Découvrez comment entraîner un modèle Machine Learning en utilisant la validation croisée avec ML.NET pour avoir un niveau de précision supérieur des prédictions du modèle
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 9508835e613cf4f78d7f95a25cc98c3c3aade7ff
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231316"
---
# <a name="train-a-machine-learning-model-using-cross-validation---mlnet"></a><span data-ttu-id="3b01f-103">Entraîner un modèle Machine Learning en utilisant la validation croisée - ML.NET</span><span class="sxs-lookup"><span data-stu-id="3b01f-103">Train a machine learning model using cross-validation - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="3b01f-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="3b01f-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="3b01f-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="3b01f-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="3b01f-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="3b01f-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="3b01f-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="3b01f-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="3b01f-108">La [validation croisée](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) est une technique pratique pour les applications de Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="3b01f-108">[Cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) is a useful technique for ML applications.</span></span> <span data-ttu-id="3b01f-109">Elle vous aide à estimer la variation de la qualité du modèle d’une exécution à l’autre et vous évite aussi de devoir extraire un jeu de test distinct pour l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="3b01f-109">It helps estimate the variance of the model quality from one run to another and also eliminates the need to extract a separate test set for evaluation.</span></span>

<span data-ttu-id="3b01f-110">ML.NET applique automatiquement une caractérisation correcte (à condition que tout le prétraitement se trouve dans un même pipeline d’entraînement), puis utilise le concept de « colonne de stratification » pour que les exemples connexes ne soient pas séparés.</span><span class="sxs-lookup"><span data-stu-id="3b01f-110">ML.NET automatically applies featurization correctly (as long as all of the preprocessing resides in one learning pipeline) then use the 'stratification column' concept to make sure that related examples don't get separated.</span></span>

<span data-ttu-id="3b01f-111">Voici un exemple d’entraînement sur un jeu de données Iris utilisant une division entraînement-test aléatoire de 90/10 et une validation croisée de 5 tranches :</span><span class="sxs-lookup"><span data-stu-id="3b01f-111">Here's a training example on an Iris dataset using randomized 90/10 train-test split, and a 5-fold cross-validation:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Step one: read the data as an IDataView.
// First, we define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextLoader(
    columns: new TextLoader.Column[]
    {
        // The four features of the Iris dataset will be grouped together as one Features column.
        new TextLoader.Column("SepalLength",DataKind.R4,0),
        new TextLoader.Column("SepalWidth",DataKind.R4,1),
        new TextLoader.Column("PetalLength",DataKind.R4,2),
        new TextLoader.Column("PetalWidth",DataKind.R4,3),
        // Label: kind of iris.
        new TextLoader.Column("Label",DataKind.TX,4)
    },
    // Default separator is tab, but the dataset has semicolon.
    separatorChar: ',',
    // First line of the file is a header, not a data row.
    hasHeader: true
);

// Read the data.
var data = reader.Read(dataPath);

// Build the training pipeline.
var dynamicPipeline =
    // Concatenate all the features together into one column 'Features'.
    mlContext.Transforms.Concatenate("Features", "SepalLength", "SepalWidth", "PetalLength", "PetalWidth")
    // Note that the label is text, so it needs to be converted to key.
    .Append(mlContext.Transforms.Conversion.MapValueToKey("Label"), TransformerScope.TrainTest)
    // Use the multi-class SDCA model to predict the label using features.
    .Append(mlContext.MulticlassClassification.Trainers.StochasticDualCoordinateAscent());

// Split the data 90:10 into train and test sets, train and evaluate.
var (trainData, testData) = mlContext.MulticlassClassification.TrainTestSplit(data, testFraction: 0.1);

// Train the model.
var model = dynamicPipeline.Fit(trainData);
// Compute quality metrics on the test set.
var metrics = mlContext.MulticlassClassification.Evaluate(model.Transform(testData));
Console.WriteLine(metrics.AccuracyMicro);

// Now run the 5-fold cross-validation experiment, using the same pipeline.
var cvResults = mlContext.MulticlassClassification.CrossValidate(data, dynamicPipeline, numFolds: 5);

// The results object is an array of 5 elements. For each of the 5 folds, we have metrics, model and scored test data.
// Let's compute the average micro-accuracy.
var microAccuracies = cvResults.Select(r => r.metrics.AccuracyMicro);
Console.WriteLine(microAccuracies.Average());
```
