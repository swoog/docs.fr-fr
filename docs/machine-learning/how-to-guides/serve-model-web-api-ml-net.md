---
title: Alimenter un modèle Machine Learning dans l’API web ASP.NET Core
description: Alimentez un modèle Machine Learning d’analyse des sentiments ML.NET sur Internet avec l’API web ASP.NET Core.
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: af51ccaac263202fc34d36e746722d2da46404f8
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59321227"
---
# <a name="how-to-serve-machine-learning-model-through-aspnet-core-web-api"></a><span data-ttu-id="671fc-103">Guide pratique : Alimenter un modèle Machine Learning par le biais de l’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="671fc-103">How-To: Serve Machine Learning Model Through ASP.NET Core Web API</span></span>

<span data-ttu-id="671fc-104">Ce guide pratique montre comment alimenter un modèle Machine Learning ML.NET prédéfini sur le web avec une API web ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="671fc-104">This how-to shows how to serve a pre-built ML.NET machine learning model to the web using an ASP.NET Core Web API.</span></span> <span data-ttu-id="671fc-105">Les utilisateurs peuvent ainsi accéder à l’API à des fins de prédiction à l’aide de méthodes HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="671fc-105">By doing so it allows for users to access the API for prediction purposes via standard HTTP methods.</span></span>

> [!NOTE]
> <span data-ttu-id="671fc-106">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="671fc-106">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="671fc-107">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="671fc-107">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="671fc-108">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="671fc-108">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="671fc-109">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="671fc-109">For more information, see the release notes at the [dotnet/machinelearning github repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="671fc-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="671fc-110">Prerequisites</span></span>

- <span data-ttu-id="671fc-111">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="671fc-111">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>
- <span data-ttu-id="671fc-112">PowerShell ;</span><span class="sxs-lookup"><span data-stu-id="671fc-112">Powershell.</span></span>
- <span data-ttu-id="671fc-113">un modèle préentraîné :</span><span class="sxs-lookup"><span data-stu-id="671fc-113">Pre-trained model.</span></span>
    - <span data-ttu-id="671fc-114">Suivez le [tutoriel Analyse des sentiments ML.NET](../tutorials/sentiment-analysis.md) pour créer votre propre modèle.</span><span class="sxs-lookup"><span data-stu-id="671fc-114">Use the [ML.NET Sentiment Analysis tutorial](../tutorials/sentiment-analysis.md) to build your own model.</span></span>
    - <span data-ttu-id="671fc-115">Téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).</span><span class="sxs-lookup"><span data-stu-id="671fc-115">Download this [pre-trained sentiment analysis machine learning model](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip)</span></span>

## <a name="create-aspnet-core-web-api-project"></a><span data-ttu-id="671fc-116">Créer un projet d’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="671fc-116">Create ASP.NET Core Web API Project</span></span>

1. <span data-ttu-id="671fc-117">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="671fc-117">Open Visual Studio 2017.</span></span> <span data-ttu-id="671fc-118">Sélectionnez **Fichier > Nouveau > Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="671fc-118">Select **File > New > Project** from the menu bar.</span></span> <span data-ttu-id="671fc-119">Dans la boîte de dialogue Nouveau projet, sélectionnez le nœud **Visual C#**, suivi du nœud **Web**.</span><span class="sxs-lookup"><span data-stu-id="671fc-119">In the New Project dialog, select the **Visual C#** node followed by the **Web** node.</span></span> <span data-ttu-id="671fc-120">Ensuite, sélectionnez le modèle de projet **Application web ASP.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="671fc-120">Then select the **ASP.NET Core Web Application** project template.</span></span> <span data-ttu-id="671fc-121">Dans la zone de texte **Nom**, tapez « SentimentAnalysisWebAPI », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="671fc-121">In the **Name** text box, type "SentimentAnalysisWebAPI" and then select the **OK** button.</span></span>
1. <span data-ttu-id="671fc-122">Dans la fenêtre qui affiche les différents types de projets ASP.NET Core, sélectionnez **API**, puis le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="671fc-122">In the window that displays the different types of ASP.NET Core Projects, select **API** and the select the **OK** button.</span></span>
1. <span data-ttu-id="671fc-123">Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer les fichiers de votre modèle Machine Learning prédéfini :</span><span class="sxs-lookup"><span data-stu-id="671fc-123">Create a directory named *MLModels* in your project to save your pre-built machine learning model files:</span></span>

    <span data-ttu-id="671fc-124">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="671fc-124">In Solution Explorer, right-click on your project and select Add > New Folder.</span></span> <span data-ttu-id="671fc-125">Tapez « MLModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="671fc-125">Type "MLModels" and hit Enter.</span></span>

1. <span data-ttu-id="671fc-126">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="671fc-126">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="671fc-127">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="671fc-127">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="671fc-128">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton Installer.</span><span class="sxs-lookup"><span data-stu-id="671fc-128">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the Install button.</span></span> <span data-ttu-id="671fc-129">Sélectionnez le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis le bouton **J’accepte** dans la boîte de dialogue Acceptation de la licence si vous acceptez les termes du contrat de licence pour les packages de la liste.</span><span class="sxs-lookup"><span data-stu-id="671fc-129">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the License Acceptance dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="add-model-to-aspnet-core-web-api-project"></a><span data-ttu-id="671fc-130">Ajouter un modèle au projet d’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="671fc-130">Add Model to ASP.NET Core Web API Project</span></span>

1. <span data-ttu-id="671fc-131">Copiez votre modèle prédéfini dans le répertoire *MLModels*.</span><span class="sxs-lookup"><span data-stu-id="671fc-131">Copy your pre-built model to the *MLModels* directory</span></span>
1. <span data-ttu-id="671fc-132">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le fichier zip du modèle et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="671fc-132">In Solution Explorer, right-click the model zip file and select Properties.</span></span> <span data-ttu-id="671fc-133">Sous Avancé, remplacez la valeur Copier dans le répertoire de sortie par Copier si plus récent.</span><span class="sxs-lookup"><span data-stu-id="671fc-133">Under Advanced, change the value of Copy to Output Directory to Copy if newer.</span></span>

## <a name="build-data-models"></a><span data-ttu-id="671fc-134">Créer des modèles de données</span><span class="sxs-lookup"><span data-stu-id="671fc-134">Build Data Models</span></span>

<span data-ttu-id="671fc-135">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="671fc-135">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="671fc-136">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="671fc-136">Add a new class to your project:</span></span>

1. <span data-ttu-id="671fc-137">Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données :</span><span class="sxs-lookup"><span data-stu-id="671fc-137">Create a directory named *DataModels* in your project to save your data models:</span></span>

    <span data-ttu-id="671fc-138">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="671fc-138">In Solution Explorer, right-click on your project and select Add > New Folder.</span></span> <span data-ttu-id="671fc-139">Tapez « DataModels » et appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="671fc-139">Type "DataModels" and hit **Enter**.</span></span>

2. <span data-ttu-id="671fc-140">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez Ajouter > Nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="671fc-140">In Solution Explorer, right-click the *DataModels* directory, and then select Add > New Item.</span></span>
3. <span data-ttu-id="671fc-141">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="671fc-141">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="671fc-142">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="671fc-142">Then, select the **Add** button.</span></span> <span data-ttu-id="671fc-143">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="671fc-143">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="671fc-144">Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="671fc-144">Add the following using statement to the top of *SentimentData.cs*:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML.Data;
```

<span data-ttu-id="671fc-145">Supprimez la définition de classe existante et ajoutez le code suivant au fichier **SentimentData.cs** :</span><span class="sxs-lookup"><span data-stu-id="671fc-145">Remove the existing class definition and add the following code to the **SentimentData.cs** file:</span></span>

```csharp
public class SentimentData
{
    [LoadColumn(0)]
    public bool Label { get; set; }
    [LoadColumn(1)]
    public string Text { get; set; }   
}
```

4. <span data-ttu-id="671fc-146">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="671fc-146">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
5. <span data-ttu-id="671fc-147">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*.</span><span class="sxs-lookup"><span data-stu-id="671fc-147">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentPrediction.cs*.</span></span> <span data-ttu-id="671fc-148">Ensuite, sélectionnez le bouton Ajouter.</span><span class="sxs-lookup"><span data-stu-id="671fc-148">Then, select the Add button.</span></span> <span data-ttu-id="671fc-149">Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="671fc-149">The *SentimentPrediction.cs* file opens in the code editor.</span></span> <span data-ttu-id="671fc-150">Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="671fc-150">Add the following using statement to the top of *SentimentPrediction.cs*:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML.Data;
```

<span data-ttu-id="671fc-151">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="671fc-151">Remove the existing class definition and add the following code to the *SentimentPrediction.cs* file:</span></span>

```csharp
public class SentimentPrediction
{
    [ColumnName("PredictedLabel")]
    public bool Prediction { get; set; }
}
```

## <a name="register-predictionengine-for-use-in-application"></a><span data-ttu-id="671fc-152">Inscrire PredictionEngine pour l’utiliser dans l’application</span><span class="sxs-lookup"><span data-stu-id="671fc-152">Register PredictionEngine for Use in Application</span></span>

<span data-ttu-id="671fc-153">Pour établir une prédiction unique, vous pouvez utiliser `PredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="671fc-153">To make a single prediction, you can use `PredictionEngine`.</span></span> <span data-ttu-id="671fc-154">Pour pouvoir utiliser `PredictionEngine` dans votre application, vous devrez le créer chaque fois qu’il sera nécessaire.</span><span class="sxs-lookup"><span data-stu-id="671fc-154">In order to use `PredictionEngine` in your application you will have to create it every time it is needed.</span></span> <span data-ttu-id="671fc-155">Dans ce cas, il est recommandé d’utiliser l’injection de dépendances ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="671fc-155">In that case, a best practice to consider is ASP.NET Core dependency injection.</span></span>

<span data-ttu-id="671fc-156">Pour plus d’informations, voir [Injection de dépendances](https://docs.microsoft.com/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1).</span><span class="sxs-lookup"><span data-stu-id="671fc-156">The following link provides more information if you want to learn about [dependency injection](https://docs.microsoft.com/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1).</span></span>

1. <span data-ttu-id="671fc-157">Ouvrez la classe *Startup.cs* et ajoutez l’instruction using suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="671fc-157">Open the *Startup.cs* class and add the following using statement to the top of the file:</span></span>

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

2. <span data-ttu-id="671fc-158">Ajoutez les lignes de code suivantes à la classe méthode *ConfigureServices* :</span><span class="sxs-lookup"><span data-stu-id="671fc-158">Add the following lines of code to the *ConfigureServices* method:</span></span>

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
> `PredictionEngine` <span data-ttu-id="671fc-159">n’est pas thread‑safe.</span><span class="sxs-lookup"><span data-stu-id="671fc-159">is not thread-safe.</span></span> <span data-ttu-id="671fc-160">L’une des façons de limiter le coût de création de l’objet consiste à rendre sa durée de vie de service *Scoped*.</span><span class="sxs-lookup"><span data-stu-id="671fc-160">A way that you can limit the cost of creating the object is by making its service lifetime *Scoped*.</span></span> <span data-ttu-id="671fc-161">Les objets *Scoped* sont les mêmes au sein d’une requête, mais ils diffèrent entre les requêtes.</span><span class="sxs-lookup"><span data-stu-id="671fc-161">*Scoped* objects are the same within a request but different across requests.</span></span> <span data-ttu-id="671fc-162">Pour en savoir plus sur les [durées de vie de service](/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1#service-lifetimes), consultez le lien suivant.</span><span class="sxs-lookup"><span data-stu-id="671fc-162">Visit the following link to learn more about [service lifetimes](/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1#service-lifetimes).</span></span>

<span data-ttu-id="671fc-163">À haut niveau, ce code initialise automatiquement les objets et les services à la demande de l’application, ce qui évite d’avoir à le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="671fc-163">At a high level, this code initializes the objects and services automatically when requested by the application instead of having to manually do it.</span></span>

## <a name="create-predict-controller"></a><span data-ttu-id="671fc-164">Créer un contrôleur de prédictions</span><span class="sxs-lookup"><span data-stu-id="671fc-164">Create Predict Controller</span></span>

<span data-ttu-id="671fc-165">Pour traiter les requêtes HTTP entrantes, il est nécessaire de créer un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="671fc-165">To process your incoming HTTP requests, you need to create a controller.</span></span>

1. <span data-ttu-id="671fc-166">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *Contrôleurs*, puis sélectionnez **Ajouter > Contrôleur**.</span><span class="sxs-lookup"><span data-stu-id="671fc-166">In Solution Explorer, right-click the *Controllers* directory, and then select **Add > Controller**.</span></span>
1. <span data-ttu-id="671fc-167">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Contrôleur d’API vide** et **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="671fc-167">In the **Add New Item** dialog box, select **API Controller Empty** and select **Add**.</span></span>
1. <span data-ttu-id="671fc-168">À l’invite, remplacez la valeur du champ **Nom du contrôleur** par *PredictController.cs*.</span><span class="sxs-lookup"><span data-stu-id="671fc-168">In the prompt change the **Controller Name** field to *PredictController.cs*.</span></span> <span data-ttu-id="671fc-169">Ensuite, sélectionnez le bouton Ajouter.</span><span class="sxs-lookup"><span data-stu-id="671fc-169">Then, select the Add button.</span></span> <span data-ttu-id="671fc-170">Le fichier *PredictController.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="671fc-170">The *PredictController.cs* file opens in the code editor.</span></span> <span data-ttu-id="671fc-171">Ajoutez l’instruction using suivante en haut du fichier *PredictController.cs* :</span><span class="sxs-lookup"><span data-stu-id="671fc-171">Add the following using statement to the top of *PredictController.cs*:</span></span>

```csharp
using System;
using Microsoft.AspNetCore.Mvc;
using SentimentAnalysisWebAPI.DataModels;
using Microsoft.ML;
```

<span data-ttu-id="671fc-172">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *PredictController.cs* :</span><span class="sxs-lookup"><span data-stu-id="671fc-172">Remove the existing class definition and add the following code to the *PredictController.cs* file:</span></span>

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

<span data-ttu-id="671fc-173">Cette opération permet d’affecter le `PredictionEngine` en le passant au constructeur du contrôleur, obtenu par injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="671fc-173">This is assigning the `PredictionEngine` by passing it to the controller's constructor which you get via dependency injection.</span></span> <span data-ttu-id="671fc-174">Ensuite, dans la méthode POST de ce contrôleur, le `PredictionEngine` est utilisé pour établir des prédictions et retourner les résultats à l’utilisateur en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="671fc-174">Then, in the POST method of this controller the `PredictionEngine` is being used to make predictions and return the results back to the user if successful.</span></span>

## <a name="test-web-api-locally"></a><span data-ttu-id="671fc-175">Test l’API web localement</span><span class="sxs-lookup"><span data-stu-id="671fc-175">Test Web API Locally</span></span>

<span data-ttu-id="671fc-176">Maintenant que tout est configuré, il est temps de tester l’application.</span><span class="sxs-lookup"><span data-stu-id="671fc-176">Once everything is set up, it's time to test the application.</span></span>

1. <span data-ttu-id="671fc-177">Exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="671fc-177">Run the application.</span></span>
1. <span data-ttu-id="671fc-178">Ouvrez PowerShell et entrez le code suivant, où PORT est le port d’écoute de votre application.</span><span class="sxs-lookup"><span data-stu-id="671fc-178">Open Powershell and enter the following code where PORT is the port your application is listening on.</span></span>

```powershell
Invoke-RestMethod "https://localhost:<PORT>/api/predict" -Method Post -Body (@{Text="This is a very rude movie"} | ConvertTo-Json) -ContentType "application/json"
```

<span data-ttu-id="671fc-179">En cas de réussite, la sortie devrait se présenter ainsi :</span><span class="sxs-lookup"><span data-stu-id="671fc-179">If successful, the output should look similar to the text below:</span></span>

```powershell
Toxic
```

<span data-ttu-id="671fc-180">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="671fc-180">Congratulations!</span></span> <span data-ttu-id="671fc-181">Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une API ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="671fc-181">You have successfully served your model to make predictions over the internet using an ASP.NET Core API.</span></span>

## <a name="next-steps"></a><span data-ttu-id="671fc-182">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="671fc-182">Next Steps</span></span>

- [<span data-ttu-id="671fc-183">Déployer sur Azure</span><span class="sxs-lookup"><span data-stu-id="671fc-183">Deploy to Azure</span></span>](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs?view=aspnetcore-2.1#deploy-the-app-to-azure)