---
title: Entraîner un modèle Machine Learning en utilisant la validation croisée - ML.NET
description: Découvrez comment entraîner un modèle Machine Learning en utilisant la validation croisée avec ML.NET pour avoir un niveau de précision supérieur des prédictions du modèle
ms.date: 02/01/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 9ed139aacb41e8f8529f30747486ab1b13183df0
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55739330"
---
# <a name="train-a-machine-learning-model-using-cross-validation---mlnet"></a>Entraîner un modèle Machine Learning en utilisant la validation croisée - ML.NET

La [validation croisée](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) est une technique pratique pour les applications de Machine Learning. Elle vous aide à estimer la variation de la qualité du modèle d’une exécution à l’autre et vous évite aussi de devoir extraire un jeu de test distinct pour l’évaluation.

ML.NET applique automatiquement une caractérisation correcte (à condition que tout le prétraitement se trouve dans un même pipeline d’entraînement), puis utilise le concept de « colonne de stratification » pour que les exemples connexes ne soient pas séparés.

Voici un exemple d’entraînement sur un jeu de données Iris utilisant une division entraînement-test aléatoire de 90/10 et une validation croisée de 5 tranches :

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Step one: read the data as an IDataView.
// First, we define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
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
