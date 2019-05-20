---
title: Calculer des métriques pour évaluer la qualité du modèle Machine Learning
description: Découvrez comment calculer des métriques pour évaluer et vérifier la qualité du modèle Machine Learning avec ML.NET
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 3e55c329ff12ffdbec41716ca95b4a77d5d082c8
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64655192"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality"></a>Calculer des métriques pour évaluer la qualité du modèle Machine Learning 

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Comment évaluer la qualité après avoir entraîné le modèle ? Chaque tâche de machine learning expose des métriques pour l’évaluation de la qualité.

Vous pouvez utiliser le « contexte » correspondant de la tâche pour évaluer le modèle, comme dans l’exemple suivant :

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```