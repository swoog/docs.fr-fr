---
title: Inspecter les valeurs de données intermédiaires lors du traitement du pipeline ML.NET
description: Découvrez comment inspecter les valeurs de données intermédiaires pendant le traitement du pipeline de machine learning de ML.NET
ms.date: 01/30/2019
ms.custom: mvc,how-to
ms.openlocfilehash: b3a554bf7cd88219a66f91a18b9d983bb91c0f0e
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675008"
---
# <a name="inspect-intermediate-data-values-during-mlnet-pipeline-processing"></a>Inspecter les valeurs de données intermédiaires lors du traitement du pipeline ML.NET

Pendant l’expérience, il peut être nécessaire d’observer et de valider les résultats du traitement des données à un moment donné. Ce n’est pas si facile, car les opérations de ML.NET progressent lentement et construisent des objets qui sont des « promesses » de données.

La méthode d’extension `GetColumn<T>` vous permet d’inspecter les données intermédiaires. Elle retourne le contenu d’une colonne de données sous la forme d’un `IEnumerable`.

L’exemple suivant montre comment utiliser la méthode d’extension `GetColumn<T>` :

[Exemple de fichier](https://github.com/dotnet/machinelearning/tree/master/test/data/adult.tiny.with-schema.txt) :
```
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse

```

Notre classe est définie comme suit :

```csharp
public class InspectedRow
{
    [LoadColumn(0)]
    public bool IsOver50K { get; set; }
    [LoadColumn(1)]
    public string WorkClass { get; set; }
    [LoadColumn(2)]
    public string Education { get; set; }
    [LoadColumn(3)]
    public string MaritalStatus { get; set; }
}
```

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Read the data into a data view.
var data = mlContext.Data.ReadFromTextFile<InspectedRow>(dataPath, hasHeader: true);

// Start creating our processing pipeline. For now, let's just concatenate all the text columns
// together into one.
var pipeline = mlContext.Transforms.Concatenate("AllFeatures", "WorkClass", "Education", "MaritalStatus");

// Fit our data pipeline and transform data with it.
var transformedData = pipeline.Fit(data).Transform(data);

// Extract the 'AllFeatures' column.
// This will give the entire dataset: make sure to only take several row
// in case the dataset is huge. The is similar to the static API, except
// you have to specify the column name and type.
var featureColumns =
    transformedData
        .GetColumn<string[]>(mlContext, "AllFeatures")
        .Take(20)
        .ToArray();
```
