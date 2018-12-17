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
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a>Utiliser un modèle Machine Learning formé dans des applications - ML.NET

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
