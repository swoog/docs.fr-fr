---
title: Alimenter un modèle Machine Learning dans l’API web ASP.NET Core
description: Alimentez un modèle Machine Learning d’analyse des sentiments ML.NET sur Internet avec l’API web ASP.NET Core.
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 07b751caff8ef0ca9a23bed68ddf88feb7b5ae4f
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57856701"
---
# <a name="how-to-serve-machine-learning-model-through-aspnet-core-web-api"></a><span data-ttu-id="ebddf-103">Guide pratique : Alimenter un modèle Machine Learning par le biais de l’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ebddf-103">How-To: Serve Machine Learning Model Through ASP.NET Core Web API</span></span>

<span data-ttu-id="ebddf-104">Ce guide pratique montre comment alimenter un modèle Machine Learning ML.NET prédéfini sur le web avec une API web ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ebddf-104">This how-to shows how to serve a pre-built ML.NET machine learning model to the web using an ASP.NET Core Web API.</span></span> <span data-ttu-id="ebddf-105">Les utilisateurs peuvent ainsi accéder à l’API à des fins de prédiction à l’aide de méthodes HTTP standard.</span><span class="sxs-lookup"><span data-stu-id="ebddf-105">By doing so it allows for users to access the API for prediction purposes via standard HTTP methods.</span></span>

> [!NOTE]
> <span data-ttu-id="ebddf-106">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="ebddf-106">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="ebddf-107">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="ebddf-107">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="ebddf-108">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-108">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="ebddf-109">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="ebddf-109">For more information, see the release notes at the [dotnet/machinelearning github repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ebddf-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ebddf-110">Prerequisites</span></span>

- <span data-ttu-id="ebddf-111">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="ebddf-111">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>
- <span data-ttu-id="ebddf-112">PowerShell ;</span><span class="sxs-lookup"><span data-stu-id="ebddf-112">Powershell.</span></span>
- <span data-ttu-id="ebddf-113">un modèle préentraîné :</span><span class="sxs-lookup"><span data-stu-id="ebddf-113">Pre-trained model.</span></span>
    - <span data-ttu-id="ebddf-114">Suivez le [tutoriel Analyse des sentiments ML.NET](../tutorials/sentiment-analysis.md) pour créer votre propre modèle.</span><span class="sxs-lookup"><span data-stu-id="ebddf-114">Use the [ML.NET Sentiment Analysis tutorial](../tutorials/sentiment-analysis.md) to build your own model.</span></span>
    - <span data-ttu-id="ebddf-115">Téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).</span><span class="sxs-lookup"><span data-stu-id="ebddf-115">Download this [pre-trained sentiment analysis machine learning model](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip)</span></span>

## <a name="create-aspnet-core-web-api-project"></a><span data-ttu-id="ebddf-116">Créer un projet d’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ebddf-116">Create ASP.NET Core Web API Project</span></span>

1. <span data-ttu-id="ebddf-117">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="ebddf-117">Open Visual Studio 2017.</span></span> <span data-ttu-id="ebddf-118">Sélectionnez **Fichier > Nouveau > Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="ebddf-118">Select **File > New > Project** from the menu bar.</span></span> <span data-ttu-id="ebddf-119">Dans la boîte de dialogue Nouveau projet, sélectionnez le nœud **Visual C#**, suivi du nœud **Web**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-119">In the New Project dialog, select the **Visual C#** node followed by the **Web** node.</span></span> <span data-ttu-id="ebddf-120">Ensuite, sélectionnez le modèle de projet **Application web ASP.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-120">Then select the **ASP.NET Core Web Application** project template.</span></span> <span data-ttu-id="ebddf-121">Dans la zone de texte **Nom**, tapez « SentimentAnalysisWebAPI », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-121">In the **Name** text box, type "SentimentAnalysisWebAPI" and then select the **OK** button.</span></span>
1. <span data-ttu-id="ebddf-122">Dans la fenêtre qui affiche les différents types de projets ASP.NET Core, sélectionnez **API**, puis le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-122">In the window that displays the different types of ASP.NET Core Projects, select **API** and the select the **OK** button.</span></span>
1. <span data-ttu-id="ebddf-123">Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer les fichiers de votre modèle Machine Learning prédéfini :</span><span class="sxs-lookup"><span data-stu-id="ebddf-123">Create a directory named *MLModels* in your project to save your pre-built machine learning model files:</span></span>

    <span data-ttu-id="ebddf-124">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="ebddf-124">In Solution Explorer, right-click on your project and select Add > New Folder.</span></span> <span data-ttu-id="ebddf-125">Tapez « MLModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="ebddf-125">Type "MLModels" and hit Enter.</span></span>

1. <span data-ttu-id="ebddf-126">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="ebddf-126">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="ebddf-127">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-127">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="ebddf-128">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton Installer.</span><span class="sxs-lookup"><span data-stu-id="ebddf-128">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the Install button.</span></span> <span data-ttu-id="ebddf-129">Sélectionnez le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis le bouton **J’accepte** dans la boîte de dialogue Acceptation de la licence si vous acceptez les termes du contrat de licence pour les packages de la liste.</span><span class="sxs-lookup"><span data-stu-id="ebddf-129">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the License Acceptance dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="add-model-to-aspnet-core-web-api-project"></a><span data-ttu-id="ebddf-130">Ajouter un modèle au projet d’API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ebddf-130">Add Model to ASP.NET Core Web API Project</span></span>

1. <span data-ttu-id="ebddf-131">Copiez votre modèle prédéfini dans le répertoire *MLModels*.</span><span class="sxs-lookup"><span data-stu-id="ebddf-131">Copy your pre-built model to the *MLModels* directory</span></span>
1. <span data-ttu-id="ebddf-132">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le fichier zip du modèle et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="ebddf-132">In Solution Explorer, right-click the model zip file and select Properties.</span></span> <span data-ttu-id="ebddf-133">Sous Avancé, remplacez la valeur Copier dans le répertoire de sortie par Copier si plus récent.</span><span class="sxs-lookup"><span data-stu-id="ebddf-133">Under Advanced, change the value of Copy to Output Directory to Copy if newer.</span></span>

## <a name="build-data-models"></a><span data-ttu-id="ebddf-134">Créer des modèles de données</span><span class="sxs-lookup"><span data-stu-id="ebddf-134">Build Data Models</span></span>

<span data-ttu-id="ebddf-135">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="ebddf-135">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="ebddf-136">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="ebddf-136">Add a new class to your project:</span></span>

1. <span data-ttu-id="ebddf-137">Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données :</span><span class="sxs-lookup"><span data-stu-id="ebddf-137">Create a directory named *DataModels* in your project to save your data models:</span></span>

    <span data-ttu-id="ebddf-138">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez Ajouter > Nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="ebddf-138">In Solution Explorer, right-click on your project and select Add > New Folder.</span></span> <span data-ttu-id="ebddf-139">Tapez « DataModels » et appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-139">Type "DataModels" and hit **Enter**.</span></span>

2. <span data-ttu-id="ebddf-140">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez Ajouter > Nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="ebddf-140">In Solution Explorer, right-click the *DataModels* directory, and then select Add > New Item.</span></span>
3. <span data-ttu-id="ebddf-141">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="ebddf-141">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="ebddf-142">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-142">Then, select the **Add** button.</span></span> <span data-ttu-id="ebddf-143">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="ebddf-143">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="ebddf-144">Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-144">Add the following using statement to the top of *SentimentData.cs*:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML.Data;
```

<span data-ttu-id="ebddf-145">Supprimez la définition de classe existante et ajoutez le code suivant au fichier **SentimentData.cs** :</span><span class="sxs-lookup"><span data-stu-id="ebddf-145">Remove the existing class definition and add the following code to the **SentimentData.cs** file:</span></span>

```csharp
public class SentimentData
{
    [LoadColumn(0)]
    public bool Label { get; set; }
    [LoadColumn(1)]
    public string Text { get; set; }   
}
```

4. <span data-ttu-id="ebddf-146">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-146">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
5. <span data-ttu-id="ebddf-147">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*.</span><span class="sxs-lookup"><span data-stu-id="ebddf-147">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentPrediction.cs*.</span></span> <span data-ttu-id="ebddf-148">Ensuite, sélectionnez le bouton Ajouter.</span><span class="sxs-lookup"><span data-stu-id="ebddf-148">Then, select the Add button.</span></span> <span data-ttu-id="ebddf-149">Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="ebddf-149">The *SentimentPrediction.cs* file opens in the code editor.</span></span> <span data-ttu-id="ebddf-150">Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-150">Add the following using statement to the top of *SentimentPrediction.cs*:</span></span>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML.Data;
```

<span data-ttu-id="ebddf-151">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-151">Remove the existing class definition and add the following code to the *SentimentPrediction.cs* file:</span></span>

```csharp
public class SentimentPrediction
{
    [ColumnName("PredictedLabel")]
    public bool Prediction { get; set; }
}
```

## <a name="create-prediction-service"></a><span data-ttu-id="ebddf-152">Créer un service de prédiction</span><span class="sxs-lookup"><span data-stu-id="ebddf-152">Create Prediction Service</span></span>

<span data-ttu-id="ebddf-153">Pour organiser et réutiliser la logique de prédiction dans toute l’application, créez un service de prédiction.</span><span class="sxs-lookup"><span data-stu-id="ebddf-153">To organize and re-use the prediction logic throughout the entire application, create a prediction service.</span></span>

1. <span data-ttu-id="ebddf-154">Créez un répertoire nommé *Services* dans votre projet pour conserver les services utilisés par l’application :</span><span class="sxs-lookup"><span data-stu-id="ebddf-154">Create a directory named *Services* in your project to hold services to be used by the application:</span></span>

    <span data-ttu-id="ebddf-155">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez **Ajouter > Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-155">In Solution Explorer, right-click on your project and select **Add > New Folder**.</span></span> <span data-ttu-id="ebddf-156">Tapez « Services » et appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-156">Type "Services" and hit **Enter**.</span></span>

1. <span data-ttu-id="ebddf-157">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *Services*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-157">In Solution Explorer, right-click the *Services* directory, and then select **Add > New Item**.</span></span>
1. <span data-ttu-id="ebddf-158">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *PredictionService.cs*.</span><span class="sxs-lookup"><span data-stu-id="ebddf-158">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *PredictionService.cs*.</span></span> <span data-ttu-id="ebddf-159">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-159">Then, select the **Add** button.</span></span> <span data-ttu-id="ebddf-160">Le fichier *PredictionService.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="ebddf-160">The *PredictionService.cs* file opens in the code editor.</span></span> <span data-ttu-id="ebddf-161">Ajoutez l’instruction using suivante en haut du fichier *PredictionService.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-161">Add the following using statement to the top of *PredictionService.cs*:</span></span>

```csharp
using System;
using System.IO;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.ML;
using Microsoft.ML.Core.Data;
using SentimentAnalysisWebAPI.DataModels;
```

<span data-ttu-id="ebddf-162">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *PredictionService.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-162">Remove the existing class definition and add the following code to the *PredictionService.cs* file:</span></span>

```csharp
public class PredictionService
{
    private readonly PredictionEngine<SentimentData, SentimentPrediction> _predictionEngine;
    public PredictionService(PredictionEngine<SentimentData,SentimentPrediction> predictionEngine)
    {
        _predictionEngine = predictionEngine;
    }

    public string Predict(SentimentData input)
    {
        // Make a prediction
        SentimentPrediction prediction = _predictionEngine.Predict(input);

        //If prediction is true then it is toxic. If it is false, the it is not.
        string isToxic = Convert.ToBoolean(prediction.Prediction) ? "Toxic" : "Not Toxic";

        return isToxic;

    }
}
```

## <a name="register-predictions-service-for-use-in-application"></a><span data-ttu-id="ebddf-163">Inscrire le service de prédiction pour l’utiliser dans l’application</span><span class="sxs-lookup"><span data-stu-id="ebddf-163">Register Predictions Service for Use in Application</span></span>

<span data-ttu-id="ebddf-164">Pour pouvoir utiliser le service de prédiction dans votre application, vous devrez le créer chaque fois qu’il sera nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ebddf-164">To use the prediction service in your application you will have to create it every time it is needed.</span></span> <span data-ttu-id="ebddf-165">Dans ce cas, il est recommandé d’utiliser l’injection de dépendances ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ebddf-165">In that case, a best practice to consider is ASP.NET Core dependency injection.</span></span>

<span data-ttu-id="ebddf-166">Pour plus d’informations, voir [Injection de dépendances](https://docs.microsoft.com/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1).</span><span class="sxs-lookup"><span data-stu-id="ebddf-166">The following link provides more information if you want to learn about [dependency injection](https://docs.microsoft.com/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-2.1).</span></span>

1. <span data-ttu-id="ebddf-167">Ouvrez la classe *Startup.cs* et ajoutez l’instruction using suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="ebddf-167">Open the *Startup.cs* class and add the following using statement to the top of the file:</span></span>

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
using SentimentAnalysisWebAPI.Services;
```

1. <span data-ttu-id="ebddf-168">Ajoutez les lignes de code suivantes à la classe méthode *ConfigureServices* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-168">Add the following lines of code to the *ConfigureServices* method:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddMvc().SetCompatibilityVersion(CompatibilityVersion.Version_2_1);

    services.AddSingleton<MLContext>();
    services.AddSingleton<PredictionEngine<SentimentData, SentimentPrediction>>((ctx) =>
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
    services.AddSingleton<PredictionService>();
}
```

<span data-ttu-id="ebddf-169">À haut niveau, ce code initialise automatiquement les objets et les services à la demande de l’application, ce qui évite d’avoir à le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="ebddf-169">At a high level, this code initializes the objects and services automatically when requested by the application instead of having to manually do it.</span></span>

## <a name="create-predict-controller"></a><span data-ttu-id="ebddf-170">Créer un contrôleur de prédictions</span><span class="sxs-lookup"><span data-stu-id="ebddf-170">Create Predict Controller</span></span>

<span data-ttu-id="ebddf-171">Pour traiter les requêtes HTTP entrantes, il est nécessaire de créer un contrôleur.</span><span class="sxs-lookup"><span data-stu-id="ebddf-171">To process your incoming HTTP requests, you need to create a controller.</span></span>

1. <span data-ttu-id="ebddf-172">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *Contrôleurs*, puis sélectionnez **Ajouter > Contrôleur**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-172">In Solution Explorer, right-click the *Controllers* directory, and then select **Add > Controller**.</span></span>
1. <span data-ttu-id="ebddf-173">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Contrôleur d’API vide** et **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ebddf-173">In the **Add New Item** dialog box, select **API Controller Empty** and select **Add**.</span></span>
1. <span data-ttu-id="ebddf-174">À l’invite, remplacez la valeur du champ **Nom du contrôleur** par *PredictController.cs*.</span><span class="sxs-lookup"><span data-stu-id="ebddf-174">In the prompt change the **Controller Name** field to *PredictController.cs*.</span></span> <span data-ttu-id="ebddf-175">Ensuite, sélectionnez le bouton Ajouter.</span><span class="sxs-lookup"><span data-stu-id="ebddf-175">Then, select the Add button.</span></span> <span data-ttu-id="ebddf-176">Le fichier *PredictController.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="ebddf-176">The *PredictController.cs* file opens in the code editor.</span></span> <span data-ttu-id="ebddf-177">Ajoutez l’instruction using suivante en haut du fichier *PredictController.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-177">Add the following using statement to the top of *PredictController.cs*:</span></span>

```csharp
using Microsoft.AspNetCore.Mvc;
using SentimentAnalysisWebAPI.DataModels;
using SentimentAnalysisWebAPI.Services;
```

<span data-ttu-id="ebddf-178">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *PredictController.cs* :</span><span class="sxs-lookup"><span data-stu-id="ebddf-178">Remove the existing class definition and add the following code to the *PredictController.cs* file:</span></span>

```csharp
public class PredictController : ControllerBase
{

    private readonly PredictionService _predictionService;

    public PredictController(PredictionService predictionService)
    {
        _predictionService = predictionService; //Define prediction service
    }

    [HttpPost]
    public ActionResult<string> Post([FromBody]SentimentData input)
    {
        if(!ModelState.IsValid)
        {
            return BadRequest();
        }
        return Ok(_predictionService.Predict(input));
    }

}
```

<span data-ttu-id="ebddf-179">Cette opération permet d’affecter le service de prédiction en le passant au constructeur du contrôleur, obtenu par injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="ebddf-179">This is assigning the Prediction service by passing it to the controller's constructor which you get via dependency injection.</span></span> <span data-ttu-id="ebddf-180">Ensuite, dans la méthode POST de ce contrôleur, le service de prédiction est utilisé pour faire des prédictions et retourner les résultats à l’utilisateur en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ebddf-180">Then, in the POST method of this controller the Prediction service is being used to make predictions and return the results back to the user if successful.</span></span>

## <a name="test-web-api-locally"></a><span data-ttu-id="ebddf-181">Test l’API web localement</span><span class="sxs-lookup"><span data-stu-id="ebddf-181">Test Web API Locally</span></span>

<span data-ttu-id="ebddf-182">Maintenant que tout est configuré, il est temps de tester l’application.</span><span class="sxs-lookup"><span data-stu-id="ebddf-182">Once everything is set up, it's time to test the application.</span></span>

1. <span data-ttu-id="ebddf-183">Exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="ebddf-183">Run the application.</span></span>
1. <span data-ttu-id="ebddf-184">Ouvrez PowerShell et entrez le code suivant, où PORT est le port d’écoute de votre application.</span><span class="sxs-lookup"><span data-stu-id="ebddf-184">Open Powershell and enter the following code where PORT is the port your application is listening on.</span></span>

```powershell
Invoke-RestMethod "https://localhost:<PORT>/api/predict" -Method Post -Body (@{Text="This is a very rude movie"} | ConvertTo-Json) -ContentType "application/json"
```

<span data-ttu-id="ebddf-185">En cas de réussite, la sortie devrait se présenter ainsi :</span><span class="sxs-lookup"><span data-stu-id="ebddf-185">If successful, the output should look similar to the text below:</span></span>

```powershell
Toxic
```

<span data-ttu-id="ebddf-186">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="ebddf-186">Congratulations!</span></span> <span data-ttu-id="ebddf-187">Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une API ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="ebddf-187">You have successfully served your model to make predictions over the internet using an ASP.NET Core API.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ebddf-188">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ebddf-188">Next Steps</span></span>

- [<span data-ttu-id="ebddf-189">Déployer sur Azure</span><span class="sxs-lookup"><span data-stu-id="ebddf-189">Deploy to Azure</span></span>](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs?view=aspnetcore-2.1#deploy-the-app-to-azure)