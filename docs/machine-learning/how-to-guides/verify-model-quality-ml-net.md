---
title: Calculer des métriques pour évaluer la qualité du modèle Machine Learning - ML.NET
description: Découvrez comment calculer des métriques pour évaluer et vérifier la qualité du modèle Machine Learning avec ML.NET
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: 6fd4dfab6104b4398918e42ed70584b04169a8c1
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149521"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a>Calculer des métriques pour évaluer la qualité du modèle Machine Learning - ML.NET

Comment évaluer la qualité après avoir entraîné le modèle ? Chaque tâche de machine learning expose des métriques pour l’évaluation de la qualité.

Vous pouvez utiliser le « contexte » correspondant de la tâche pour évaluer le modèle, comme dans l’exemple suivant :

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```