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
# <a name="how-to-use-mlnet-model-in-azure-functions"></a><span data-ttu-id="4bc0d-103">Guide pratique : Utiliser un modèle ML.NET dans Azure Functions</span><span class="sxs-lookup"><span data-stu-id="4bc0d-103">How-To: Use ML.NET Model in Azure Functions</span></span>

<span data-ttu-id="4bc0d-104">Ce guide pratique montre comment faire des prédictions avec un modèle Machine Learning ML.NET prédéfini, par Internet, dans un environnement serverless comme Azure Functions.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-104">This how-to shows how individual predictions can be made using a pre-built ML.NET machine learning model through the internet in a serverless environment such as Azure Functions.</span></span>

> [!NOTE]
> <span data-ttu-id="4bc0d-105">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-105">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="4bc0d-106">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-106">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="4bc0d-107">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-107">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="4bc0d-108">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-108">For more information, see the release notes at the [dotnet/machinelearning github repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4bc0d-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4bc0d-109">Prerequisites</span></span>

- <span data-ttu-id="4bc0d-110">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .NET Core » et « Développement Azure » ;</span><span class="sxs-lookup"><span data-stu-id="4bc0d-110">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload and "Azure development" installed.</span></span> 
- <span data-ttu-id="4bc0d-111">[Azure Functions Tools](/azure/azure-functions/functions-develop-vs#check-your-tools-version) ;</span><span class="sxs-lookup"><span data-stu-id="4bc0d-111">[Azure Functions Tools](/azure/azure-functions/functions-develop-vs#check-your-tools-version)</span></span>
- <span data-ttu-id="4bc0d-112">PowerShell ;</span><span class="sxs-lookup"><span data-stu-id="4bc0d-112">Powershell</span></span>
- <span data-ttu-id="4bc0d-113">un modèle préentraîné :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-113">Pre-trained model.</span></span> 
    - <span data-ttu-id="4bc0d-114">Suivez le [tutoriel Analyse des sentiments ML.NET](../tutorials/sentiment-analysis.md) pour créer votre propre modèle.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-114">Use the [ML.NET Sentiment Analysis tutorial](../tutorials/sentiment-analysis.md) to build your own model.</span></span>
    - <span data-ttu-id="4bc0d-115">Téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).</span><span class="sxs-lookup"><span data-stu-id="4bc0d-115">Download this [pre-trained sentiment analysis machine learning model](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip)</span></span>

## <a name="create-azure-functions-project"></a><span data-ttu-id="4bc0d-116">Créer un projet Azure Functions</span><span class="sxs-lookup"><span data-stu-id="4bc0d-116">Create Azure Functions Project</span></span>

1. <span data-ttu-id="4bc0d-117">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-117">Open Visual Studio 2017.</span></span> <span data-ttu-id="4bc0d-118">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-118">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="4bc0d-119">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#**, suivi du nœud **Cloud**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-119">In the **New Project** dialog, select the **Visual C#** node followed by the **Cloud** node.</span></span> <span data-ttu-id="4bc0d-120">Ensuite, sélectionnez le modèle de projet **Azure Functions**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-120">Then select the **Azure Functions** project template.</span></span> <span data-ttu-id="4bc0d-121">Dans la zone de texte **Nom**, tapez « SentimentAnalysisFunctionsApp », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-121">In the **Name** text box, type "SentimentAnalysisFunctionsApp" and then select the **OK** button.</span></span>
1. <span data-ttu-id="4bc0d-122">Dans la boîte de dialogue **Nouveau projet**, ouvrez la liste déroulante au-dessus des options du projet et sélectionnez **Azure Functions v2 (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-122">In the **New Project** dialog, open the dropdown above the project options and select **Azure Functions v2 (.NET Core)**.</span></span> <span data-ttu-id="4bc0d-123">Ensuite, sélectionnez le projet **Déclencheur HTTP**, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-123">Then, select the **Http trigger** project and then select the **OK** button.</span></span>
1. <span data-ttu-id="4bc0d-124">Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer votre modèle :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-124">Create a directory named *MLModels* in your project to save your model:</span></span>

    <span data-ttu-id="4bc0d-125">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-125">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="4bc0d-126">Tapez « MLModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-126">Type "MLModels" and hit Enter.</span></span>

1. <span data-ttu-id="4bc0d-127">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-127">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="4bc0d-128">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-128">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="4bc0d-129">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-129">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="4bc0d-130">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-130">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="add-pre-built-model-to-project"></a><span data-ttu-id="4bc0d-131">Ajouter un modèle prédéfini au projet</span><span class="sxs-lookup"><span data-stu-id="4bc0d-131">Add Pre-built Model To Project</span></span>

1. <span data-ttu-id="4bc0d-132">Copiez votre modèle prédéfini dans le dossier *MLModels*.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-132">Copy your pre-built model to the *MLModels* folder.</span></span>
1. <span data-ttu-id="4bc0d-133">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre fichier de modèle prédéfini et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-133">In Solution Explorer, right-click your pre-built model file and select **Properties**.</span></span> <span data-ttu-id="4bc0d-134">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-134">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

## <a name="create-function-to-analyze-sentiment"></a><span data-ttu-id="4bc0d-135">Créer une fonction d’analyse des sentiments</span><span class="sxs-lookup"><span data-stu-id="4bc0d-135">Create Function to Analyze Sentiment</span></span>

<span data-ttu-id="4bc0d-136">Créez une classe pour prédire le sentiment.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-136">Create a class to predict sentiment.</span></span> <span data-ttu-id="4bc0d-137">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-137">Add a new class to your project:</span></span>

1. <span data-ttu-id="4bc0d-138">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-138">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="4bc0d-139">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Fonction Azure** et remplacez la valeur du champ **Nom** par *AnalyzeSentiment.cs*.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-139">In the **Add New Item** dialog box, select **Azure Function** and change the **Name** field to *AnalyzeSentiment.cs*.</span></span> <span data-ttu-id="4bc0d-140">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-140">Then, select the **Add** button.</span></span>

1. <span data-ttu-id="4bc0d-141">Dans la boîte de dialogue **Nouvelle fonction Azure**, sélectionnez **Déclencheur HTTP**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-141">In the **New Azure Function** dialog box, select **Http Trigger**.</span></span> <span data-ttu-id="4bc0d-142">Ensuite, sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-142">Then, select the **OK** button.</span></span>

    <span data-ttu-id="4bc0d-143">Le fichier *AnalyzeSentiment.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-143">The *AnalyzeSentiment.cs* file opens in the code editor.</span></span> <span data-ttu-id="4bc0d-144">Ajoutez l’instruction `using` suivante en haut de *GitHubIssueData.cs* :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-144">Add the following `using` statement to the top of *GitHubIssueData.cs*:</span></span>

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

### <a name="create-data-models"></a><span data-ttu-id="4bc0d-145">Créer des modèles de données</span><span class="sxs-lookup"><span data-stu-id="4bc0d-145">Create Data Models</span></span>

<span data-ttu-id="4bc0d-146">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-146">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="4bc0d-147">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-147">Add a new class to your project:</span></span>

1. <span data-ttu-id="4bc0d-148">Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données : Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez **Ajouter > Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-148">Create a directory named *DataModels* in your project to save your data models: In Solution Explorer, right-click on your project and select **Add > New Folder**.</span></span> <span data-ttu-id="4bc0d-149">Tapez « DataModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-149">Type "DataModels" and hit Enter.</span></span>
2. <span data-ttu-id="4bc0d-150">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-150">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
3. <span data-ttu-id="4bc0d-151">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-151">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="4bc0d-152">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-152">Then, select the **Add** button.</span></span> <span data-ttu-id="4bc0d-153">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-153">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="4bc0d-154">Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-154">Add the following using statement to the top of *SentimentData.cs*:</span></span>

```csharp
using Microsoft.ML.Data;
```

<span data-ttu-id="4bc0d-155">Supprimez la définition de classe existante et ajoutez le code suivant au fichier SentimentData.cs :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-155">Remove the existing class definition and add the following code to the SentimentData.cs file:</span></span>

```csharp
public class SentimentData
{
    [LoadColumn(0)]
    public bool Label { get; set; }
    [LoadColumn(1)]
    public string Text { get; set; }
}
```

4. <span data-ttu-id="4bc0d-156">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-156">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
5. <span data-ttu-id="4bc0d-157">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-157">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentPrediction.cs*.</span></span> <span data-ttu-id="4bc0d-158">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-158">Then, select the **Add** button.</span></span> <span data-ttu-id="4bc0d-159">Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-159">The *SentimentPrediction.cs* file opens in the code editor.</span></span> <span data-ttu-id="4bc0d-160">Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-160">Add the following using statement to the top of *SentimentPrediction.cs*:</span></span>

```csharp
using Microsoft.ML.Data;
```

<span data-ttu-id="4bc0d-161">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-161">Remove the existing class definition and add the following code to the *SentimentPrediction.cs* file:</span></span>

```csharp
public class SentimentPrediction
{
    [ColumnName("PredictedLabel")]
    public bool Prediction { get; set; }
}
```

### <a name="add-prediction-logic"></a><span data-ttu-id="4bc0d-162">Ajouter une logique de prédiction</span><span class="sxs-lookup"><span data-stu-id="4bc0d-162">Add Prediction Logic</span></span>

<span data-ttu-id="4bc0d-163">Remplacez l’implémentation existante de la méthode *Run* dans la classe *AnalyzeSentiment* par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-163">Replace the existing implementation of *Run* method in *AnalyzeSentiment* class with the following code:</span></span>

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

## <a name="test-locally"></a><span data-ttu-id="4bc0d-164">Tester localement</span><span class="sxs-lookup"><span data-stu-id="4bc0d-164">Test Locally</span></span>

<span data-ttu-id="4bc0d-165">Maintenant que tout est configuré, il est temps de tester l’application :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-165">Now that everything is set up, it's time to test the application:</span></span>

1. <span data-ttu-id="4bc0d-166">Exécuter l'application</span><span class="sxs-lookup"><span data-stu-id="4bc0d-166">Run the application</span></span>
1. <span data-ttu-id="4bc0d-167">Ouvrez PowerShell et entrez le code dans l’invite, où PORT est le port sur lequel s’exécute votre application,</span><span class="sxs-lookup"><span data-stu-id="4bc0d-167">Open PowerShell and enter the code into the prompt where PORT is the port your application is running on.</span></span> <span data-ttu-id="4bc0d-168">en règle générale 7071.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-168">Typically the port is 7071.</span></span> 

```powershell
Invoke-RestMethod "http://localhost:<PORT>/api/AnalyzeSentiment" -Method Post -Body (@{Text="This is a very rude movie"} | ConvertTo-Json) -ContentType "application/json"
```

<span data-ttu-id="4bc0d-169">En cas de réussite, la sortie devrait se présenter ainsi :</span><span class="sxs-lookup"><span data-stu-id="4bc0d-169">If successful, the output should look similar to the text below:</span></span>

```powershell
Toxic
```

<span data-ttu-id="4bc0d-170">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="4bc0d-170">Congratulations!</span></span> <span data-ttu-id="4bc0d-171">Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une fonction Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc0d-171">You have successfully served your model to make predictions over the internet using an Azure Function.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4bc0d-172">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4bc0d-172">Next Steps</span></span>

- [<span data-ttu-id="4bc0d-173">Déployer sur Azure</span><span class="sxs-lookup"><span data-stu-id="4bc0d-173">Deploy to Azure</span></span>](/azure/azure-functions/functions-develop-vs#publish-to-azure)