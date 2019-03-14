---
title: Utiliser un modèle Machine Learning formé dans des applications - ML.NET
description: Découvrez comment utiliser ML.NET pour consommer un modèle Machine Learning formé et évalué dans des applications.
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: be6906c939b82d00067babaeebe809dae3de413a
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57675132"
---
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a><span data-ttu-id="1bfc3-103">Utiliser un modèle Machine Learning formé dans des applications - ML.NET</span><span class="sxs-lookup"><span data-stu-id="1bfc3-103">Operationalize a trained machine learning model in apps - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="1bfc3-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="1bfc3-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="1bfc3-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="1bfc3-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="1bfc3-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="1bfc3-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="1bfc3-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="1bfc3-107">For more information, see the release notes at the [dotnet/machinelearning github repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes)</span></span>

<span data-ttu-id="1bfc3-108">Lorsque les métriques du modèle vous semblent correctes, il est temps « d’opérationnaliser » le modèle.</span><span class="sxs-lookup"><span data-stu-id="1bfc3-108">When the model metrics look good to you, it's time to 'operationalize' the model.</span></span> <span data-ttu-id="1bfc3-109">L’objet `model` que vous avez créé peut être consommé, persistant et réutilisé dans différents environnements, en appliquant les mêmes étapes « apprises » lors de la formation.</span><span class="sxs-lookup"><span data-stu-id="1bfc3-109">The `model` object you built can be consumed, persisted, and reused in different environments, applying the same steps that it 'learned' during training.</span></span>

<span data-ttu-id="1bfc3-110">Pour enregistrer le modèle dans un fichier et le recharger (potentiellement dans un contexte différent), utilisez l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1bfc3-110">To save the model to a file, and reload it (potentially in a different context), use the following example:</span></span>

```csharp
using (var stream = File.Create(modelPath))
{
    // Saving and loading happens to 'dynamic' models.
    mlContext.Model.Save(model, stream);
}

// Potentially, the lines below can be in a different process altogether.

// When you load the model, it's a transformer.
ITransformer loadedModel;
using (var stream = File.OpenRead(modelPath))
    loadedModel = mlContext.Model.Load(stream);
```
