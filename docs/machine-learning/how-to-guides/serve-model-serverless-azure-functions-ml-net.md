---
title: Déployer un modèle ML.NET sur Azure Functions
description: Alimentez un modèle Machine Learning d’analyse des sentiments ML.NET à des fins de prédiction sur Internet avec Azure Functions.
ms.date: 03/08/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 4681b37da64097dd8e537b4c956917277ecff96b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59330634"
---
# <a name="how-to-use-mlnet-model-in-azure-functions"></a>Guide pratique : Utiliser un modèle ML.NET dans Azure Functions

Ce guide pratique montre comment faire des prédictions avec un modèle Machine Learning ML.NET prédéfini, par Internet, dans un environnement serverless comme Azure Functions.

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

## <a name="prerequisites"></a>Prérequis

- [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .NET Core » et « Développement Azure » ; 
- [Azure Functions Tools](/azure/azure-functions/functions-develop-vs#check-your-tools-version) ;
- PowerShell ;
- un modèle préentraîné : 
    - Suivez le [tutoriel Analyse des sentiments ML.NET](../tutorials/sentiment-analysis.md) pour créer votre propre modèle.
    - Téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).

## <a name="create-azure-functions-project"></a>Créer un projet Azure Functions

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#**, suivi du nœud **Cloud**. Ensuite, sélectionnez le modèle de projet **Azure Functions**. Dans la zone de texte **Nom**, tapez « SentimentAnalysisFunctionsApp », puis sélectionnez le bouton **OK**.
1. Dans la boîte de dialogue **Nouveau projet**, ouvrez la liste déroulante au-dessus des options du projet et sélectionnez **Azure Functions v2 (.NET Core)**. Ensuite, sélectionnez le projet **Déclencheur HTTP**, puis sélectionnez le bouton **OK**.
1. Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer votre modèle :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « MLModels » et appuyez sur Entrée.

1. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

## <a name="add-pre-built-model-to-project"></a>Ajouter un modèle prédéfini au projet

1. Copiez votre modèle prédéfini dans le dossier *MLModels*.
1. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre fichier de modèle prédéfini et sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

## <a name="create-function-to-analyze-sentiment"></a>Créer une fonction d’analyse des sentiments

Créez une classe pour prédire le sentiment. Ajoutez une nouvelle classe à votre projet :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.

1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Fonction Azure** et remplacez la valeur du champ **Nom** par *AnalyzeSentiment.cs*. Ensuite, sélectionnez le bouton **Ajouter**.

1. Dans la boîte de dialogue **Nouvelle fonction Azure**, sélectionnez **Déclencheur HTTP**. Ensuite, sélectionnez le bouton **OK**.

    Le fichier *AnalyzeSentiment.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction `using` suivante en haut de *GitHubIssueData.cs* :

```csharp
using System;
using System.IO;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Azure.WebJobs;
using Microsoft.Azure.WebJobs.Extensions.Http;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.Logging;
using Newtonsoft.Json;
using Microsoft.ML;
using Microsoft.ML.Core.Data;
using Microsoft.ML.Data;
using MLNETServerless.DataModels;
```

### <a name="create-data-models"></a>Créer des modèles de données

Vous devez créer des classes pour vos données d’entrée et prévisions. Ajoutez une nouvelle classe à votre projet :

1. Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données : Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez **Ajouter > Nouveau dossier**. Tapez « DataModels » et appuyez sur Entrée.
2. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.
3. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*. Ensuite, sélectionnez le bouton **Ajouter**. Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :

```csharp
using Microsoft.ML.Data;
```

Supprimez la définition de classe existante et ajoutez le code suivant au fichier SentimentData.cs :

```csharp
public class SentimentData
{
    [LoadColumn(0)]
    public bool Label { get; set; }
    [LoadColumn(1)]
    public string Text { get; set; }
}
```

4. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.
5. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*. Ensuite, sélectionnez le bouton **Ajouter**. Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :

```csharp
using Microsoft.ML.Data;
```

Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentPrediction.cs* :

```csharp
public class SentimentPrediction
{
    [ColumnName("PredictedLabel")]
    public bool Prediction { get; set; }
}
```

### <a name="add-prediction-logic"></a>Ajouter une logique de prédiction

Remplacez l’implémentation existante de la méthode *Run* dans la classe *AnalyzeSentiment* par le code suivant :

```csharp
    public static async Task<IActionResult> Run(
        [HttpTrigger(AuthorizationLevel.Function,"post", Route = null)] HttpRequest req,
        ILogger log)
    {
        log.LogInformation("C# HTTP trigger function processed a request.");

        //Create Context
        MLContext mlContext = new MLContext();

        //Load Model
        using (var fs = File.OpenRead("MLModels/sentiment_model.zip"))
        {
            model = mlContext.Model.Load(fs);
        }

        //Parse HTTP Request Body
        string requestBody = await new StreamReader(req.Body).ReadToEndAsync();
        SentimentData data = JsonConvert.DeserializeObject<SentimentData>(requestBody);

        //Create Prediction Engine
        PredictionEngine<SentimentData, SentimentPrediction> predictionEngine = model.CreatePredictionEngine<SentimentData, SentimentPrediction>(mlContext);

        //Make Prediction
        SentimentPrediction prediction = predictionEngine.Predict(data);

        //Convert prediction to string
        string isToxic = Convert.ToBoolean(prediction.Prediction) ? "Toxic" : "Not Toxic";

        //Return Prediction
        return (ActionResult)new OkObjectResult(isToxic);
    }
}
```

## <a name="test-locally"></a>Tester localement

Maintenant que tout est configuré, il est temps de tester l’application :

1. Exécuter l'application
1. Ouvrez PowerShell et entrez le code dans l’invite, où PORT est le port sur lequel s’exécute votre application, en règle générale 7071. 

```powershell
Invoke-RestMethod "http://localhost:<PORT>/api/AnalyzeSentiment" -Method Post -Body (@{Text="This is a very rude movie"} | ConvertTo-Json) -ContentType "application/json"
```

En cas de réussite, la sortie devrait se présenter ainsi :

```powershell
Toxic
```

Félicitations ! Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une fonction Azure.

## <a name="next-steps"></a>Étapes suivantes

- [Déployer sur Azure](/azure/azure-functions/functions-develop-vs#publish-to-azure)