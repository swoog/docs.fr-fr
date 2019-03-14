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
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a>Utiliser un modèle Machine Learning formé dans des applications - ML.NET

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Lorsque les métriques du modèle vous semblent correctes, il est temps « d’opérationnaliser » le modèle. L’objet `model` que vous avez créé peut être consommé, persistant et réutilisé dans différents environnements, en appliquant les mêmes étapes « apprises » lors de la formation.

Pour enregistrer le modèle dans un fichier et le recharger (potentiellement dans un contexte différent), utilisez l’exemple suivant :

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
