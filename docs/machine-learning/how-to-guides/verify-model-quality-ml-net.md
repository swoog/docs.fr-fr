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
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a><span data-ttu-id="ed25c-103">Calculer des métriques pour évaluer la qualité du modèle Machine Learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="ed25c-103">Calculate metrics to evaluate machine learning model quality - ML.NET</span></span>

<span data-ttu-id="ed25c-104">Comment évaluer la qualité après avoir entraîné le modèle ?</span><span class="sxs-lookup"><span data-stu-id="ed25c-104">How do you evaluate quality after you train the model?</span></span> <span data-ttu-id="ed25c-105">Chaque tâche de machine learning expose des métriques pour l’évaluation de la qualité.</span><span class="sxs-lookup"><span data-stu-id="ed25c-105">Each machine learning task exposes metrics for quality evaluation.</span></span>

<span data-ttu-id="ed25c-106">Vous pouvez utiliser le « contexte » correspondant de la tâche pour évaluer le modèle, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="ed25c-106">You can use the corresponding 'context' of the task to evaluate the model, as in the following example:</span></span>

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```