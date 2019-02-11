---
title: Prétraiter les données d’entraînement avec des normaliseurs pour les utiliser dans le traitement des données - ML.NET
description: Découvrez comment utiliser des normaliseurs pour prétraiter les données d’entraînement à utiliser dans la création, l’entraînement et le scoring de modèles Machine Learning avec ML.NET
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 4311307f5410a96bb4a30fcedd88bc43afd25c12
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738576"
---
# <a name="preprocess-training-data-with-normalizers-to-use-in-data-processing---mlnet"></a><span data-ttu-id="cc96a-103">Prétraiter les données d’entraînement avec des normaliseurs pour les utiliser dans le traitement des données - ML.NET</span><span class="sxs-lookup"><span data-stu-id="cc96a-103">Preprocess training data with normalizers to use in data processing - ML.NET</span></span>

<span data-ttu-id="cc96a-104">ML.NET expose plusieurs [algorithmes paramétriques et non paramétriques](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/).</span><span class="sxs-lookup"><span data-stu-id="cc96a-104">ML.NET exposes a number of [parametric and non-parametric algorithms](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/).</span></span>

<span data-ttu-id="cc96a-105">Le choix du normaliseur que vous choisissez d’utiliser est **moins** important que celui d’**utiliser** un normaliseur lors de l’entraînement de modèles linéaires ou d’autres modèles paramétriques.</span><span class="sxs-lookup"><span data-stu-id="cc96a-105">It's **not** as important which normalizer you choose as it is to **use** a normalizer when training linear or other parametric models.</span></span>

<span data-ttu-id="cc96a-106">Ajoutez toujours le normaliseur directement dans le pipeline d’entraînement de ML.NET, pour :</span><span class="sxs-lookup"><span data-stu-id="cc96a-106">Always include the normalizer directly in the ML.NET learning pipeline, so it:</span></span>

- <span data-ttu-id="cc96a-107">L’entraîner seulement sur les données d’entraînement et non pas sur vos données de test</span><span class="sxs-lookup"><span data-stu-id="cc96a-107">is only trained on the training data, and not on your test data,</span></span>
- <span data-ttu-id="cc96a-108">L’appliquer correctement à toutes les nouvelles données entrantes, sans nécessiter de prétraitement supplémentaire au moment de la prédiction.</span><span class="sxs-lookup"><span data-stu-id="cc96a-108">is correctly applied to all the new incoming data, without the need for extra pre-processing at prediction time.</span></span>

<span data-ttu-id="cc96a-109">Voici un extrait de code qui montre la normalisation dans les pipelines d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="cc96a-109">Here's a snippet of code that demonstrates normalization in learning pipelines.</span></span> <span data-ttu-id="cc96a-110">Il suppose l’existence du jeu de données Iris :</span><span class="sxs-lookup"><span data-stu-id="cc96a-110">It assumes the Iris dataset:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
    columns: new TextLoader.Column[]
    {
        // The four features of the Iris dataset will be grouped together as one Features column.
        new TextLoader.Column("Features",DataKind.R4,0,3),
        // Label: kind of iris.
        new TextLoader.Column("Label",DataKind.TX,4)
    },
    // Default separator is tab, but the dataset has comma.
    separatorChar: ',',
    // First line of the file is a header, not a data row.
    hasHeader: true
);

// Read the training data.
var trainData = reader.Read(dataPath);

// Apply all kinds of standard ML.NET normalization to the raw features.
var pipeline =
    mlContext.Transforms.Normalize(
        new NormalizingEstimator.MinMaxColumn("Features", "MinMaxNormalized", fixZero: true),
        new NormalizingEstimator.MeanVarColumn("Features", "MeanVarNormalized", fixZero: true),
        new NormalizingEstimator.BinningColumn("Features", "BinNormalized", numBins: 256));

// Let's train our pipeline of normalizers, and then apply it to the same data.
var normalizedData = pipeline.Fit(trainData).Transform(trainData);

// Inspect one column of the resulting dataset.
var meanVarValues = normalizedData.GetColumn<float[]>(mlContext, "MeanVarNormalized").ToArray();
```
