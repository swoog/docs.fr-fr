---
title: Alimenter un modèle Machine Learning dans l’API web ASP.NET Core
description: Alimentez un modèle Machine Learning d’analyse des sentiments ML.NET sur Internet avec l’API web ASP.NET Core.
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 0cc13ec22b3a8805ec4aa17bf10560b2564ccd63
ms.sourcegitcommit: 77854e8704b9689b73103d691db34d71c2bf1dad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58307913"
---
# <a name="how-to-serve-machine-learning-model-through-aspnet-core-web-api"></a>Guide pratique : Alimenter un modèle Machine Learning par le biais de l’API web ASP.NET Core

Ce guide pratique montre comment alimenter un modèle Machine Learning ML.NET prédéfini sur le web avec une API web ASP.NET Core. Les utilisateurs peuvent ainsi accéder à l’API à des fins de prédiction à l’aide de méthodes HTTP standard.

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

## <a name="prerequisites"></a>Prérequis

- [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.
- PowerShell ;
- un modèle préentraîné :
    - Suivez le [tutoriel Analyse des sentiments ML.NET](../tutorials/sentiment-analysis.md) pour créer votre propre modèle.
    - Téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).

## <a name="create-aspnet-core-web-api-project"></a>Créer un projet d’API web ASP.NET Core

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier > Nouveau > Projet** dans la barre de menus. Dans la boîte de dialogue Nouveau projet, sélectionnez le nœud **Visual C#**, suivi du nœud **Web**. Ensuite, sélectionnez le modèle de projet **Application web ASP.NET Core**. Dans la zone de texte **Nom**, tapez « SentimentAnalysisWebAPI », puis sélectionnez le bouton **OK**.
1. Dans la fenêtre qui affiche les différents types de projets ASP.NET Core, sélectionnez **API**, puis le bouton **OK**.
1. Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer les fichiers de votre modèle Machine Learning prédéfini :

    Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier. Tapez « MLModels » et appuyez sur Entrée.

1. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton Installer. Sélectionnez le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis le bouton **J’accepte** dans la boîte de dialogue Acceptation de la licence si vous acceptez les termes du contrat de licence pour les packages de la liste.

### <a name="add-model-to-aspnet-core-web-api-project"></a>Ajouter un modèle au projet d’API web ASP.NET Core

1. Copiez votre modèle prédéfini dans le répertoire *MLModels*.
1. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le fichier zip du modèle et sélectionnez Propriétés. Sous Avancé, remplacez la valeur Copier dans le répertoire de sortie par Copier si plus récent.

## <a name="build-data-models"></a>Créer des modèles de données

Vous devez créer des classes pour vos données d’entrée et prévisions. Ajoutez une nouvelle classe à votre projet :

1. Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données :

    Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier. Tapez « DataModels » et appuyez sur **Entrée**.

2. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez Ajouter > Nouvel élément.
3. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*. Ensuite, sélectionnez le bouton **Ajouter**. Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML.Data;
```

Supprimez la définition de classe existante et ajoutez le code suivant au fichier **SentimentData.cs** :

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
5. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*. Ensuite, sélectionnez le bouton Ajouter. Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
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

## <a name="register-predictionengine-for-use-in-application"></a>Inscrire PredictionEngine pour l’utiliser dans l’application

Pour établir une prédiction unique, vous pouvez utiliser `PredictionEngine`. Pour pouvoir utiliser `PredictionEngine` dans votre application, vous devrez le créer chaque fois qu’il sera nécessaire. Dans ce cas, il est recommandé d’utiliser l’injection de dépendances ASP.NET Core.

Pour plus d’informations, voir [Injection de dépendances](https://docs.microsoft.com/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1).

1. Ouvrez la classe *Startup.cs* et ajoutez l’instruction using suivante en haut du fichier :

```csharp
using System.IO;
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Extensions.Configuration;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.ML;
using Microsoft.ML.Core.Data;
using SentimentAnalysisWebAPI.DataModels;
```

2. Ajoutez les lignes de code suivantes à la classe méthode *ConfigureServices* :

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddMvc().SetCompatibilityVersion(CompatibilityVersion.Version_2_1);

    services.AddScoped<MLContext>();
    services.AddScoped<PredictionEngine<SentimentData, SentimentPrediction>>((ctx) =>
    {
        MLContext mlContext = ctx.GetRequiredService<MLContext>();
        string modelFilePathName = "MLModels/sentiment_model.zip";

        //Load model from file
        ITransformer model;
        using (var stream = File.OpenRead(modelFilePathName))
        {
            model = mlContext.Model.Load(stream);
        }

        // Return prediction engine
        return model.CreatePredictionEngine<SentimentData, SentimentPrediction>(mlContext);
    });
}
```

> [!WARNING]
> `PredictionEngine` n’est pas thread‑safe. L’une des façons de limiter le coût de création de l’objet consiste à rendre sa durée de vie de service *Scoped*. Les objets *Scoped* sont les mêmes au sein d’une requête, mais ils diffèrent entre les requêtes. Pour en savoir plus sur les [durées de vie de service](/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1#service-lifetimes), consultez le lien suivant.

À haut niveau, ce code initialise automatiquement les objets et les services à la demande de l’application, ce qui évite d’avoir à le faire manuellement.

## <a name="create-predict-controller"></a>Créer un contrôleur de prédictions

Pour traiter les requêtes HTTP entrantes, il est nécessaire de créer un contrôleur.

1. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *Contrôleurs*, puis sélectionnez **Ajouter > Contrôleur**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Contrôleur d’API vide** et **Ajouter**.
1. À l’invite, remplacez la valeur du champ **Nom du contrôleur** par *PredictController.cs*. Ensuite, sélectionnez le bouton Ajouter. Le fichier *PredictController.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction using suivante en haut du fichier *PredictController.cs* :

```csharp
using System;
using Microsoft.AspNetCore.Mvc;
using SentimentAnalysisWebAPI.DataModels;
using Microsoft.ML;
```

Supprimez la définition de classe existante et ajoutez le code suivant au fichier *PredictController.cs* :

```csharp
public class PredictController : ControllerBase
{
    
    private readonly PredictionEngine<SentimentData,SentimentPrediction> _predictionEngine;

    public PredictController(PredictionEngine<SentimentData, SentimentPrediction> predictionEngine)
    {
        _predictionEngine = predictionEngine; //Define prediction engine
    }

    [HttpPost]
    public ActionResult<string> Post([FromBody]SentimentData input)
    {
        if(!ModelState.IsValid)
        {
            return BadRequest();
        }

        // Make a prediction
        SentimentPrediction prediction = _predictionEngine.Predict(input);

        //If prediction is true then it is toxic. If it is false, the it is not.
        string isToxic = Convert.ToBoolean(prediction.Prediction) ? "Toxic" : "Not Toxic";

        return Ok(isToxic);
    }
    
}
```

Cette opération permet d’affecter le `PredictionEngine` en le passant au constructeur du contrôleur, obtenu par injection de dépendances. Ensuite, dans la méthode POST de ce contrôleur, le `PredictionEngine` est utilisé pour établir des prédictions et retourner les résultats à l’utilisateur en cas de réussite.

## <a name="test-web-api-locally"></a>Test l’API web localement

Maintenant que tout est configuré, il est temps de tester l’application.

1. Exécutez l'application.
1. Ouvrez PowerShell et entrez le code suivant, où PORT est le port d’écoute de votre application.

```powershell
Invoke-RestMethod "https://localhost:<PORT>/api/predict" -Method Post -Body (@{Text="This is a very rude movie"} | ConvertTo-Json) -ContentType "application/json"
```

En cas de réussite, la sortie devrait se présenter ainsi :

```powershell
Toxic
```

Félicitations ! Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une API ASP.NET Core.

## <a name="next-steps"></a>Étapes suivantes

- [Déployer sur Azure](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs?view=aspnetcore-2.1#deploy-the-app-to-azure)