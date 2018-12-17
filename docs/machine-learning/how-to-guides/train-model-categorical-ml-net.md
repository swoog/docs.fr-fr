---
title: Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données catégoriques - ML.NET
description: Découvrez comment appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles Machine Learning sur des données catégoriques avec ML.NET.
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 10441ed4bfad4cccc51ebbf589ef313d1fe53f6e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156607"
---
# <a name="apply-feature-engineering-for-model-training-on-categorical-data---mlnet"></a><span data-ttu-id="3408a-103">Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données catégoriques - ML.NET</span><span class="sxs-lookup"><span data-stu-id="3408a-103">Apply feature engineering for model training on categorical data - ML.NET</span></span>

<span data-ttu-id="3408a-104">Vous devez convertir les données non flottantes en types de données `float`, car tous les `learners` ML.NET attendent les caractéristiques sous forme de `float vector`.</span><span class="sxs-lookup"><span data-stu-id="3408a-104">You need to convert any non float data to `float` data types since all ML.NET `learners` expect features as a `float vector`.</span></span>

<span data-ttu-id="3408a-105">Si le jeu de données contient des données `categorical` (par exemple, 'enum'), ML.NET offre plusieurs façons de les convertir en caractéristiques :</span><span class="sxs-lookup"><span data-stu-id="3408a-105">If the dataset contains `categorical` data (for example, 'enum'), ML.NET offers several ways of converting it to features:</span></span>

- <span data-ttu-id="3408a-106">Encodage one-hot</span><span class="sxs-lookup"><span data-stu-id="3408a-106">One-hot encoding</span></span>
- <span data-ttu-id="3408a-107">Encodage one-hot en fonction du hachage</span><span class="sxs-lookup"><span data-stu-id="3408a-107">Hash-based one-hot encoding</span></span>
- <span data-ttu-id="3408a-108">Encodage binaire (convertir l’index de catégorie en une séquence de bits et utiliser ces bits comme caractéristiques)</span><span class="sxs-lookup"><span data-stu-id="3408a-108">Binary encoding (convert category index into a bit sequence and use bits as features)</span></span>

<span data-ttu-id="3408a-109">Un `one-hot encoding` peut entraîner un certain gaspillage si certaines catégories affichent une cardinalité très élevée (un grand nombre de valeurs différentes avec un jeu restreint fréquemment utilisé).</span><span class="sxs-lookup"><span data-stu-id="3408a-109">A `one-hot encoding` can be wasteful if some categories are very high-cardinality (lots of different values, with a small set commonly occurring.</span></span> <span data-ttu-id="3408a-110">Dans ce cas, réduisez le nombre d’emplacements à encoder en sélectionnant des caractéristiques selon un nombre.</span><span class="sxs-lookup"><span data-stu-id="3408a-110">In that case, reduce the number of slots to encode with count-based feature selection.</span></span>

<span data-ttu-id="3408a-111">Incluez une caractérisation catégorielle directement dans le pipeline d’apprentissage ML.NET pour vous assurer que la transformation par catégorie :</span><span class="sxs-lookup"><span data-stu-id="3408a-111">Include categorical featurization directly in the ML.NET learning pipeline to ensure that the categorical transformation:</span></span>

- <span data-ttu-id="3408a-112">est formée seulement sur les données d’entraînement et non pas sur vos données de test ;</span><span class="sxs-lookup"><span data-stu-id="3408a-112">is only 'trained' on the training data, and not on your test data,</span></span>
- <span data-ttu-id="3408a-113">est correctement appliquée aux nouvelles données entrantes, sans prétraitement supplémentaire au moment de la prédiction.</span><span class="sxs-lookup"><span data-stu-id="3408a-113">is correctly applied to new incoming data, without extra pre-processing at prediction time.</span></span>

<span data-ttu-id="3408a-114">L’exemple suivant montre un traitement par catégorie pour le [jeu de données adult census](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt) :</span><span class="sxs-lookup"><span data-stu-id="3408a-114">The following example illustrates categorical handling for the [adult census dataset](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt):</span></span>

```console
Label   Workclass   education   marital-status  occupation  relationship    ethnicity   sex native-country-region   age fnlwgt  education-num   capital-gain    capital-loss    hours-per-week
0   Private 11th    Never-married   Machine-op-inspct   Own-child   Black   Male    United-States   25  226802  7   0   0   40
0   Private HS-grad Married-civ-spouse  Farming-fishing Husband White   Male    United-States   38  89814   9   0   0   50
1   Local-gov   Assoc-acdm  Married-civ-spouse  Protective-serv Husband White   Male    United-States   28  336951  12  0   0   40
1   Private Some-college    Married-civ-spouse  Machine-op-inspct   Husband Black   Male    United-States   44  160323  10  7688    0   40
```

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        new TextLoader.Column("Label", DataKind.BL, 0),
        // We will load all the categorical features into one vector column of size 8.
        new TextLoader.Column("CategoricalFeatures", DataKind.TX, 1, 8),
        // Similarly, load all numerical features into one vector of size 6.
        new TextLoader.Column("NumericalFeatures", DataKind.R4, 9, 14),
        // Let's also separately load the 'Workclass' column.
        new TextLoader.Column("Workclass", DataKind.TX, 1),
    },
    HasHeader = true
});

// Read the data.
var data = reader.Read(dataPath);

// Inspect the first 10 records of the categorical columns to check that they are correctly read.
var catColumns = data.GetColumn<string[]>(mlContext, "CategoricalFeatures").Take(10).ToArray();

// Build several alternative featurization pipelines.
var dynamicPipeline =
    // Convert each categorical feature into one-hot encoding independently.
    mlContext.Transforms.Categorical.OneHotEncoding("CategoricalFeatures", "CategoricalOneHot")
    // Convert all categorical features into indices, and build a 'word bag' of these.
    .Append(mlContext.Transforms.Categorical.OneHotEncoding("CategoricalFeatures", "CategoricalBag", CategoricalTransform.OutputKind.Bag))
    // One-hot encode the workclass column, then drop all the categories that have fewer than 10 instances in the train set.
    .Append(mlContext.Transforms.Categorical.OneHotEncoding("Workclass", "WorkclassOneHot"))
    .Append(new CountFeatureSelector(mlContext, "WorkclassOneHot", "WorkclassOneHotTrimmed", count: 10));

// Let's train our pipeline, and then apply it to the same data.
var transformedData = dynamicPipeline.Fit(data).Transform(data);

// Inspect some columns of the resulting dataset.
var categoricalBags = transformedData.GetColumn<float[]>(mlContext, "CategoricalBag").Take(10).ToArray();
var workclasses = transformedData.GetColumn<float[]>(mlContext, "WorkclassOneHotTrimmed").Take(10).ToArray();

// Of course, if we want to train the model, we will need to compose a single float vector of all the features.
// Here's how we could do this:

var fullLearningPipeline = dynamicPipeline
    // Concatenate two of the 3 categorical pipelines, and the numeric features.
    .Append(mlContext.Transforms.Concatenate("Features", "NumericalFeatures", "CategoricalBag", "WorkclassOneHotTrimmed"))
    // Now we're ready to train. We chose our FastTree trainer for this classification task.
    .Append(mlContext.BinaryClassification.Trainers.FastTree(numTrees: 50));

// Train the model.
var model = fullLearningPipeline.Fit(data);
```
