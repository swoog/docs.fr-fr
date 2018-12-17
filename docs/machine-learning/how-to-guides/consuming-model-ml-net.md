---
title: Utiliser un modèle Machine Learning formé dans des applications - ML.NET
description: Découvrez comment utiliser ML.NET pour consommer un modèle Machine Learning formé et évalué dans des applications.
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: ff3f0a8856382d020129693bcf722f572fd87606
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131643"
---
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a><span data-ttu-id="b2bba-103">Utiliser un modèle Machine Learning formé dans des applications - ML.NET</span><span class="sxs-lookup"><span data-stu-id="b2bba-103">Operationalize a trained machine learning model in apps - ML.NET</span></span>

<span data-ttu-id="b2bba-104">Lorsque les métriques du modèle vous semblent correctes, il est temps « d’opérationnaliser » le modèle.</span><span class="sxs-lookup"><span data-stu-id="b2bba-104">When the model metrics look good to you, it's time to 'operationalize' the model.</span></span> <span data-ttu-id="b2bba-105">L’objet `model` que vous avez créé peut être consommé, persistant et réutilisé dans différents environnements, en appliquant les mêmes étapes « apprises » lors de la formation.</span><span class="sxs-lookup"><span data-stu-id="b2bba-105">The `model` object you built can be consumed, persisted, and reused in different environments, applying the same steps that it 'learned' during training.</span></span>

<span data-ttu-id="b2bba-106">Pour enregistrer le modèle dans un fichier et le recharger (potentiellement dans un contexte différent), utilisez l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b2bba-106">To save the model to a file, and reload it (potentially in a different context), use the following example:</span></span>

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
