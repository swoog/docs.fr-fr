---
title: Entraîner un modèle Machine Learning avec des données qui ne sont pas dans un fichier texte - ML.NET
description: Découvrez comment utiliser ML.NET pour charger des données d’entraînement non-fichier pour l’entraînement de modèles Machine Learning dans le cadre d’un pipeline de prédiction.
ms.date: 03/18/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 32de37e45b9e19669ea06d74c7f252ec885fe004
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "58186089"
---
# <a name="train-a-machine-learning-model-with-data-thats-not-in-a-text-file---mlnet"></a>Entraîner un modèle Machine Learning avec des données qui ne sont pas dans un fichier texte - ML.NET

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.11**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Le cas d’usage couramment illustré pour ML.NET est l’utilisation de `TextLoader` pour lire les données d’entraînement d’un fichier.
Toutefois, dans les scénarios d’entraînement en temps réel, les données peuvent être ailleurs, par exemple :

* dans des tables SQL
* JSON/XML
* extraites de fichiers journaux
* générées à la volée

Utilisez [schema comprehension](https://github.com/dotnet/machinelearning/tree/master/docs/code/SchemaComprehension.md) pour apporter un `IEnumerable` C# existant dans ML.NET comme `DataView`.

Pour cet exemple, vous allez générer le modèle de prédiction de baisse du client et extraire les fonctionnalités suivantes à partir de votre système de production :

* ID du client (ignoré par le modèle)
* Si le client a baissé (« l'étiquette » cible)
* La « catégorie démographique » (une chaîne, comme « jeunes adultes » etc.)
* Le nombre de visites des 5 derniers jours.

```csharp
private class CustomerChurnInfo
{
    public string CustomerID { get; set; }
    public bool HasChurned { get; set; }
    public string DemographicCategory { get; set; }
    // Visits during last 5 days, latest to newest.
    [VectorType(5)]
    public float[] LastVisits { get; set; }
}
```

Chargez ces données dans le `DataView` et entraînez le modèle avec le code suivant :

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging,
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Step one: read the data as an IDataView.
// Let's assume that 'GetChurnData()' fetches and returns the training data from somewhere.
IEnumerable<CustomerChurnInfo> churnData = GetChurnInfo();

// Turn the data into the ML.NET data view.
// We can use CreateDataView or CreateStreamingDataView, depending on whether 'churnData' is an IList,
// or merely an IEnumerable.
var trainData = mlContext.Data.LoadFromEnumerable(churnData);

// Build the learning pipeline.
// In our case, we will one-hot encode the demographic category, and concatenate that with the number of visits.
// We apply our FastTree binary classifier to predict the 'HasChurned' label.

var pipeline = mlContext.Transforms.Categorical.OneHotEncoding("DemographicCategory")
    .Append(mlContext.Transforms.Concatenate("Features", "DemographicCategory", "LastVisits"))
    .Append(mlContext.BinaryClassification.Trainers.FastTree("HasChurned", "Features", numTrees: 20));

var model = pipeline.Fit(trainData);
```
