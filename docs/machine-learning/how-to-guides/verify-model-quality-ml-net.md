---
title: Calculer des métriques pour évaluer la qualité du modèle Machine Learning - ML.NET
description: Découvrez comment calculer des métriques pour évaluer et vérifier la qualité du modèle Machine Learning avec ML.NET
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: ad71f7da6981ac370e60725f88d3c70b1d5c5237
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57679214"
---
# <a name="calculate-metrics-to-evaluate-machine-learning-model-quality---mlnet"></a><span data-ttu-id="1f178-103">Calculer des métriques pour évaluer la qualité du modèle Machine Learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="1f178-103">Calculate metrics to evaluate machine learning model quality - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="1f178-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="1f178-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="1f178-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="1f178-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="1f178-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="1f178-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="1f178-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="1f178-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="1f178-108">Comment évaluer la qualité après avoir entraîné le modèle ?</span><span class="sxs-lookup"><span data-stu-id="1f178-108">How do you evaluate quality after you train the model?</span></span> <span data-ttu-id="1f178-109">Chaque tâche de machine learning expose des métriques pour l’évaluation de la qualité.</span><span class="sxs-lookup"><span data-stu-id="1f178-109">Each machine learning task exposes metrics for quality evaluation.</span></span>

<span data-ttu-id="1f178-110">Vous pouvez utiliser le « contexte » correspondant de la tâche pour évaluer le modèle, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1f178-110">You can use the corresponding 'context' of the task to evaluate the model, as in the following example:</span></span>

```csharp
// Read the test dataset.
var testData = reader.Read(testDataPath);
// Calculate metrics of the model on the test data.
var metrics = mlContext.Regression.Evaluate(model.Transform(testData), label: "Target");
```