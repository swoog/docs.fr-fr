---
title: Déployer un modèle sur Azure Functions
description: Alimentez un modèle Machine Learning d’analyse des sentiments ML.NET à des fins de prédiction sur Internet avec Azure Functions.
ms.date: 05/03/2019
author: luisquintanilla
ms.author: luquinta
ms.custom: mvc, how-to
ms.openlocfilehash: 9e62d8826227aed07451387cc733d27094327f99
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645095"
---
# <a name="deploy-a-model-to-azure-functions"></a><span data-ttu-id="e1794-103">Déployer un modèle sur Azure Functions</span><span class="sxs-lookup"><span data-stu-id="e1794-103">Deploy a model to Azure Functions</span></span>

<span data-ttu-id="e1794-104">Découvrez comment déployer un modèle Machine Learning ML.NET préentraîné pour effectuer des prédictions sur HTTP par le bais d’un environnement serverless Azure Functions.</span><span class="sxs-lookup"><span data-stu-id="e1794-104">Learn how to deploy a pre-trained ML.NET machine learning model for predictions over HTTP through an Azure Functions serverless environment.</span></span>

> [!NOTE]
> <span data-ttu-id="e1794-105">L’extension de service `PredictionEnginePool` est disponible en préversion.</span><span class="sxs-lookup"><span data-stu-id="e1794-105">`PredictionEnginePool` service extension is currently in preview.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1794-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e1794-106">Prerequisites</span></span>

- <span data-ttu-id="e1794-107">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .NET Core » et « Développement Azure » ;</span><span class="sxs-lookup"><span data-stu-id="e1794-107">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload and "Azure development" installed.</span></span>
- <span data-ttu-id="e1794-108">[Azure Functions Tools](/azure/azure-functions/functions-develop-vs#check-your-tools-version) ;</span><span class="sxs-lookup"><span data-stu-id="e1794-108">[Azure Functions Tools](/azure/azure-functions/functions-develop-vs#check-your-tools-version)</span></span>
- <span data-ttu-id="e1794-109">PowerShell ;</span><span class="sxs-lookup"><span data-stu-id="e1794-109">Powershell</span></span>
- <span data-ttu-id="e1794-110">un modèle préentraîné :</span><span class="sxs-lookup"><span data-stu-id="e1794-110">Pre-trained model.</span></span> <span data-ttu-id="e1794-111">Utilisez le [tutoriel Analyse des sentiments dans ML.NET](../tutorials/sentiment-analysis.md) pour générer votre propre modèle ou téléchargez ce [modèle Machine Learning d’analyse des sentiments préentraîné](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip).</span><span class="sxs-lookup"><span data-stu-id="e1794-111">Use the [ML.NET Sentiment Analysis tutorial](../tutorials/sentiment-analysis.md) to build your own model or download this [pre-trained sentiment analysis machine learning model](https://github.com/dotnet/samples/blob/master/machine-learning/models/sentimentanalysis/sentiment_model.zip)</span></span>

## <a name="create-azure-functions-project"></a><span data-ttu-id="e1794-112">Créer un projet Azure Functions</span><span class="sxs-lookup"><span data-stu-id="e1794-112">Create Azure Functions project</span></span>

1. <span data-ttu-id="e1794-113">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="e1794-113">Open Visual Studio 2017.</span></span> <span data-ttu-id="e1794-114">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="e1794-114">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="e1794-115">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#**, suivi du nœud **Cloud**.</span><span class="sxs-lookup"><span data-stu-id="e1794-115">In the **New Project** dialog, select the **Visual C#** node followed by the **Cloud** node.</span></span> <span data-ttu-id="e1794-116">Ensuite, sélectionnez le modèle de projet **Azure Functions**.</span><span class="sxs-lookup"><span data-stu-id="e1794-116">Then select the **Azure Functions** project template.</span></span> <span data-ttu-id="e1794-117">Dans la zone de texte **Nom**, tapez « SentimentAnalysisFunctionsApp », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1794-117">In the **Name** text box, type "SentimentAnalysisFunctionsApp" and then select the **OK** button.</span></span>
1. <span data-ttu-id="e1794-118">Dans la boîte de dialogue **Nouveau projet**, ouvrez la liste déroulante au-dessus des options du projet et sélectionnez **Azure Functions v2 (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="e1794-118">In the **New Project** dialog, open the dropdown above the project options and select **Azure Functions v2 (.NET Core)**.</span></span> <span data-ttu-id="e1794-119">Ensuite, sélectionnez le projet **Déclencheur HTTP**, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1794-119">Then, select the **Http trigger** project and then select the **OK** button.</span></span>
1. <span data-ttu-id="e1794-120">Créez un répertoire nommé *MLModels* dans votre projet pour enregistrer votre modèle :</span><span class="sxs-lookup"><span data-stu-id="e1794-120">Create a directory named *MLModels* in your project to save your model:</span></span>

    <span data-ttu-id="e1794-121">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="e1794-121">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="e1794-122">Tapez « MLModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="e1794-122">Type "MLModels" and hit Enter.</span></span>

1. <span data-ttu-id="e1794-123">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="e1794-123">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="e1794-124">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="e1794-124">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="e1794-125">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="e1794-125">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="e1794-126">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="e1794-126">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

1. <span data-ttu-id="e1794-127">Installez le **package NuGet Microsoft.Extensions.ML** :</span><span class="sxs-lookup"><span data-stu-id="e1794-127">Install the **Microsoft.Extensions.ML NuGet Package**:</span></span>

    <span data-ttu-id="e1794-128">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="e1794-128">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="e1794-129">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.Extensions.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="e1794-129">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.Extensions.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="e1794-130">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="e1794-130">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="add-pre-trained-model-to-project"></a><span data-ttu-id="e1794-131">Ajouter un modèle préentraîné au projet</span><span class="sxs-lookup"><span data-stu-id="e1794-131">Add pre-trained model to project</span></span>

1. <span data-ttu-id="e1794-132">Copiez votre modèle prédéfini dans le dossier *MLModels*.</span><span class="sxs-lookup"><span data-stu-id="e1794-132">Copy your pre-built model to the *MLModels* folder.</span></span>
1. <span data-ttu-id="e1794-133">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre fichier de modèle prédéfini et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="e1794-133">In Solution Explorer, right-click your pre-built model file and select **Properties**.</span></span> <span data-ttu-id="e1794-134">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="e1794-134">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

## <a name="create-azure-function-to-analyze-sentiment"></a><span data-ttu-id="e1794-135">Créer une fonction Azure d’analyse des sentiments</span><span class="sxs-lookup"><span data-stu-id="e1794-135">Create Azure Function to analyze sentiment</span></span>

<span data-ttu-id="e1794-136">Créez une classe pour prédire le sentiment.</span><span class="sxs-lookup"><span data-stu-id="e1794-136">Create a class to predict sentiment.</span></span> <span data-ttu-id="e1794-137">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="e1794-137">Add a new class to your project:</span></span>

1. <span data-ttu-id="e1794-138">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="e1794-138">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="e1794-139">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Fonction Azure** et remplacez la valeur du champ **Nom** par *AnalyzeSentiment.cs*.</span><span class="sxs-lookup"><span data-stu-id="e1794-139">In the **Add New Item** dialog box, select **Azure Function** and change the **Name** field to *AnalyzeSentiment.cs*.</span></span> <span data-ttu-id="e1794-140">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e1794-140">Then, select the **Add** button.</span></span>

1. <span data-ttu-id="e1794-141">Dans la boîte de dialogue **Nouvelle fonction Azure**, sélectionnez **Déclencheur HTTP**.</span><span class="sxs-lookup"><span data-stu-id="e1794-141">In the **New Azure Function** dialog box, select **Http Trigger**.</span></span> <span data-ttu-id="e1794-142">Ensuite, sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1794-142">Then, select the **OK** button.</span></span>

    <span data-ttu-id="e1794-143">Le fichier *AnalyzeSentiment.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1794-143">The *AnalyzeSentiment.cs* file opens in the code editor.</span></span> <span data-ttu-id="e1794-144">Ajoutez l’instruction suivante `using` en haut du fichier *AnalyzeSentiment.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-144">Add the following `using` statement to the top of *AnalyzeSentiment.cs*:</span></span>

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
    using Microsoft.Extensions.ML;
    using SentimentAnalysisFunctionsApp.DataModels;
    ```

    <span data-ttu-id="e1794-145">Par défaut, la classe `AnalyzeSentiment` est `static`.</span><span class="sxs-lookup"><span data-stu-id="e1794-145">By default, the `AnalyzeSentiment` class is `static`.</span></span> <span data-ttu-id="e1794-146">Veillez à supprimer le mot clé `static` de la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="e1794-146">Make sure to remove the `static` keyword from the class definition.</span></span>

    ```csharp
    public class AnalyzeSentiment
    {
    
    }
    ```

## <a name="create-data-models"></a><span data-ttu-id="e1794-147">Créer des modèles de données</span><span class="sxs-lookup"><span data-stu-id="e1794-147">Create data models</span></span>

<span data-ttu-id="e1794-148">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="e1794-148">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="e1794-149">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="e1794-149">Add a new class to your project:</span></span>

1. <span data-ttu-id="e1794-150">Créez un répertoire nommé *DataModels* dans votre projet pour enregistrer vos modèles de données : Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre projet et sélectionnez **Ajouter > Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="e1794-150">Create a directory named *DataModels* in your project to save your data models: In Solution Explorer, right-click on your project and select **Add > New Folder**.</span></span> <span data-ttu-id="e1794-151">Tapez « DataModels » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="e1794-151">Type "DataModels" and hit Enter.</span></span>
2. <span data-ttu-id="e1794-152">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="e1794-152">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
3. <span data-ttu-id="e1794-153">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="e1794-153">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="e1794-154">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e1794-154">Then, select the **Add** button.</span></span> 

    <span data-ttu-id="e1794-155">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1794-155">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="e1794-156">Ajoutez l’instruction using suivante en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-156">Add the following using statement to the top of *SentimentData.cs*:</span></span>

    ```csharp
    using Microsoft.ML.Data;
    ```

    <span data-ttu-id="e1794-157">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-157">Remove the existing class definition and add the following code to the *SentimentData.cs* file:</span></span>
    
    ```csharp
    public class SentimentData
    {
        [LoadColumn(0)]
        public string SentimentText;

        [LoadColumn(1)]
        [ColumnName("Label")]
        public bool Sentiment;
    }
    ```

4. <span data-ttu-id="e1794-158">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le répertoire *DataModels*, puis sélectionnez **Ajouter > Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="e1794-158">In Solution Explorer, right-click the *DataModels* directory, and then select **Add > New Item**.</span></span>
5. <span data-ttu-id="e1794-159">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et remplacez la valeur du champ **Nom** par *SentimentPrediction.cs*.</span><span class="sxs-lookup"><span data-stu-id="e1794-159">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentPrediction.cs*.</span></span> <span data-ttu-id="e1794-160">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e1794-160">Then, select the **Add** button.</span></span> <span data-ttu-id="e1794-161">Le fichier *SentimentPrediction.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1794-161">The *SentimentPrediction.cs* file opens in the code editor.</span></span> <span data-ttu-id="e1794-162">Ajoutez l’instruction using suivante en haut du fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-162">Add the following using statement to the top of *SentimentPrediction.cs*:</span></span>

    ```csharp
    using Microsoft.ML.Data;
    ```

    <span data-ttu-id="e1794-163">Supprimez la définition de classe existante et ajoutez le code suivant au fichier *SentimentPrediction.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-163">Remove the existing class definition and add the following code to the *SentimentPrediction.cs* file:</span></span>

    ```csharp
    public class SentimentPrediction : SentimentData
    {

        [ColumnName("PredictedLabel")]
        public bool Prediction { get; set; }

        public float Probability { get; set; }

        public float Score { get; set; }
    }
    ```

    <span data-ttu-id="e1794-164">`SentimentPrediction` hérite de `SentimentData`, qui fournit l’accès aux données d’origine dans la propriété `SentimentText` ainsi que la sortie générée par le modèle.</span><span class="sxs-lookup"><span data-stu-id="e1794-164">`SentimentPrediction` inherits from `SentimentData` which provides access to the original data in the `SentimentText` property as well as the output generated by the model.</span></span>

## <a name="register-predictionenginepool-service"></a><span data-ttu-id="e1794-165">Inscrire le service PredictionEnginePool</span><span class="sxs-lookup"><span data-stu-id="e1794-165">Register PredictionEnginePool service</span></span>

<span data-ttu-id="e1794-166">Pour établir une prédiction unique, utilisez [`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602).</span><span class="sxs-lookup"><span data-stu-id="e1794-166">To make a single prediction, use [`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602).</span></span> <span data-ttu-id="e1794-167">Pour pouvoir utiliser la classe [`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602) dans votre application, vous devez la créer quand vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="e1794-167">In order to use [`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602) in your application you must create it when it's needed.</span></span> <span data-ttu-id="e1794-168">Dans ce cas, il est recommandé d’utiliser l’injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="e1794-168">In that case, a best practice to consider is dependency injection.</span></span>

<span data-ttu-id="e1794-169">Pour plus d’informations, voir [Injection de dépendances](https://en.wikipedia.org/wiki/Dependency_injection).</span><span class="sxs-lookup"><span data-stu-id="e1794-169">The following link provides more information if you want to learn about [dependency injection](https://en.wikipedia.org/wiki/Dependency_injection).</span></span>

1. <span data-ttu-id="e1794-170">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="e1794-170">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="e1794-171">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et définissez la valeur du champ **Nom** sur *Startup.cs*.</span><span class="sxs-lookup"><span data-stu-id="e1794-171">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *Startup.cs*.</span></span> <span data-ttu-id="e1794-172">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e1794-172">Then, select the **Add** button.</span></span> 

    <span data-ttu-id="e1794-173">Le fichier *Startup.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1794-173">The *Startup.cs* file opens in the code editor.</span></span> <span data-ttu-id="e1794-174">Ajoutez l’instruction using suivante en haut du fichier *Startup.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-174">Add the following using statement to the top of *Startup.cs*:</span></span>

    ```csharp
    using Microsoft.Azure.WebJobs;
    using Microsoft.Azure.WebJobs.Hosting;
    using Microsoft.Extensions.ML;
    using SentimentAnalysisFunctionsApp;
    using SentimentAnalysisFunctionsApp.DataModels;
    ```

    <span data-ttu-id="e1794-175">Supprimez le code sous les instructions using et ajoutez le code suivant au fichier *Startup.cs* :</span><span class="sxs-lookup"><span data-stu-id="e1794-175">Remove the existing code below the using statements and add the following code to the *Startup.cs* file:</span></span>

    ```csharp
    [assembly: WebJobsStartup(typeof(Startup))]
    namespace SentimentAnalysisFunctionsApp
    {
        class Startup : IWebJobsStartup
        {
            public void Configure(IWebJobsBuilder builder)
            {
                builder.Services.AddPredictionEnginePool<SentimentData, SentimentPrediction>()
                    .FromFile("MLModels/sentiment_model.zip");
            }
        }
    }
    ```

<span data-ttu-id="e1794-176">À haut niveau, ce code initialise automatiquement les objets et les services à la demande de l’application, ce qui évite d’avoir à le faire manuellement.</span><span class="sxs-lookup"><span data-stu-id="e1794-176">At a high level, this code initializes the objects and services automatically when requested by the application instead of having to manually do it.</span></span>

> [!WARNING]
> <span data-ttu-id="e1794-177">[`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602) n’est pas thread‑safe.</span><span class="sxs-lookup"><span data-stu-id="e1794-177">[`PredictionEngine`](xref:Microsoft.ML.PredictionEngine%602) is not thread-safe.</span></span> <span data-ttu-id="e1794-178">Pour améliorer les performances et la cohérence de thread, utilisez le service `PredictionEnginePool`, qui crée un [`ObjectPool`](xref:Microsoft.Extensions.ObjectPool.ObjectPool%601) d’objets `PredictionEngine` à utiliser avec l’application.</span><span class="sxs-lookup"><span data-stu-id="e1794-178">For improved performance and thread safety, use the `PredictionEnginePool` service, which creates an [`ObjectPool`](xref:Microsoft.Extensions.ObjectPool.ObjectPool%601) of `PredictionEngine` objects for application use.</span></span> 

## <a name="register-startup-as-an-azure-functions-extension"></a><span data-ttu-id="e1794-179">Inscrire Startup en tant qu’extension Azure Functions</span><span class="sxs-lookup"><span data-stu-id="e1794-179">Register Startup as an Azure Functions extension</span></span>

<span data-ttu-id="e1794-180">Pour pouvoir utiliser `Startup` dans votre application, vous devez l’inscrire en tant qu’extension Azure Functions.</span><span class="sxs-lookup"><span data-stu-id="e1794-180">In order to use `Startup` in your application, you need to register it as an Azure Functions extension.</span></span> <span data-ttu-id="e1794-181">Créez un fichier appelé *extensions.json* dans votre projet si ce fichier n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="e1794-181">Create a new file called *extensions.json* in your project if one does not already exist.</span></span>

1. <span data-ttu-id="e1794-182">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="e1794-182">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="e1794-183">Dans la boîte de dialogue **Nouvel élément**, sélectionnez le nœud **Visual C#**, suivi du nœud **Web**.</span><span class="sxs-lookup"><span data-stu-id="e1794-183">In the **New Item** dialog, select the **Visual C#** node followed by the **Web** node.</span></span> <span data-ttu-id="e1794-184">Ensuite, sélectionnez l’option **Fichier Json**.</span><span class="sxs-lookup"><span data-stu-id="e1794-184">Then select the **Json File** option.</span></span> <span data-ttu-id="e1794-185">Dans la zone de texte **Nom**, tapez « extensions.json », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1794-185">In the **Name** text box, type "extensions.json" and then select the **OK** button.</span></span>

    <span data-ttu-id="e1794-186">Le fichier *extensions.json* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e1794-186">The *extensions.json* file opens in the code editor.</span></span> <span data-ttu-id="e1794-187">Ajoutez le contenu suivant à *extensions.json* :</span><span class="sxs-lookup"><span data-stu-id="e1794-187">Add the following content to *extensions.json*:</span></span>
    
    ```json
    {
      "extensions": [
        {
          "name": "Startup",
          "typename": "SentimentAnalysisFunctionsApp.Startup, SentimentAnalysisFunctionsApp, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null"
        }
      ]
    }
    ```

1. <span data-ttu-id="e1794-188">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur votre fichier *extensions.json* et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="e1794-188">In Solution Explorer, right-click your *extensions.json* file and select **Properties**.</span></span> <span data-ttu-id="e1794-189">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="e1794-189">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

## <a name="load-the-model-into-the-function"></a><span data-ttu-id="e1794-190">Charger le modèle dans la fonction</span><span class="sxs-lookup"><span data-stu-id="e1794-190">Load the model into the function</span></span>

<span data-ttu-id="e1794-191">Insérez le code suivant à l’intérieur de la classe *AnalyzeSentiment* :</span><span class="sxs-lookup"><span data-stu-id="e1794-191">Insert the following code inside the *AnalyzeSentiment* class:</span></span>

```csharp
private readonly PredictionEnginePool<SentimentData, SentimentPrediction> _predictionEnginePool;

// AnalyzeSentiment class constructor
public AnalyzeSentiment(PredictionEnginePool<SentimentData, SentimentPrediction> predictionEnginePool)
{
    _predictionEnginePool = predictionEnginePool;
}
```

<span data-ttu-id="e1794-192">Ce code affecte le `PredictionEnginePool` en le passant au constructeur de la fonction, obtenu par injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="e1794-192">This code assigns the `PredictionEnginePool` by passing it to the function's constructor which you get via dependency injection.</span></span>

## <a name="use-the-model-to-make-predictions"></a><span data-ttu-id="e1794-193">Utiliser le modèle pour élaborer des prédictions</span><span class="sxs-lookup"><span data-stu-id="e1794-193">Use the model to make predictions</span></span>

<span data-ttu-id="e1794-194">Remplacez l’implémentation existante de la méthode *Run* dans la classe *AnalyzeSentiment* par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e1794-194">Replace the existing implementation of *Run* method in *AnalyzeSentiment* class with the following code:</span></span>

```csharp
[FunctionName("AnalyzeSentiment")]
public async Task<IActionResult> Run(
[HttpTrigger(AuthorizationLevel.Function, "post", Route = null)] HttpRequest req,
ILogger log)
{
    log.LogInformation("C# HTTP trigger function processed a request.");

    //Parse HTTP Request Body
    string requestBody = await new StreamReader(req.Body).ReadToEndAsync();
    SentimentData data = JsonConvert.DeserializeObject<SentimentData>(requestBody);
    
    //Make Prediction
    SentimentPrediction prediction = _predictionEnginePool.Predict(data);

    //Convert prediction to string
    string sentiment = Convert.ToBoolean(prediction.Prediction) ? "Positive" : "Negative";

    //Return Prediction
    return (ActionResult)new OkObjectResult(sentiment);
}
```

<span data-ttu-id="e1794-195">Quand la méthode `Run` s’exécute, les données entrantes issues de la requête HTTP sont désérialisées et utilisées comme entrée pour le `PredictionEnginePool`.</span><span class="sxs-lookup"><span data-stu-id="e1794-195">When the `Run` method executes, the incoming data from the HTTP request is deserialized and used as input for the `PredictionEnginePool`.</span></span> <span data-ttu-id="e1794-196">La méthode `Predict` est ensuite appelée pour générer une prédiction et retourner le résultat à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1794-196">The `Predict` method is then called to generate a prediction and return the result to the user.</span></span> 

## <a name="test-locally"></a><span data-ttu-id="e1794-197">Tester localement</span><span class="sxs-lookup"><span data-stu-id="e1794-197">Test locally</span></span>

<span data-ttu-id="e1794-198">Maintenant que tout est configuré, il est temps de tester l’application :</span><span class="sxs-lookup"><span data-stu-id="e1794-198">Now that everything is set up, it's time to test the application:</span></span>

1. <span data-ttu-id="e1794-199">Exécuter l'application</span><span class="sxs-lookup"><span data-stu-id="e1794-199">Run the application</span></span>
1. <span data-ttu-id="e1794-200">Ouvrez PowerShell et entrez le code dans l’invite, où PORT est le port sur lequel s’exécute votre application,</span><span class="sxs-lookup"><span data-stu-id="e1794-200">Open PowerShell and enter the code into the prompt where PORT is the port your application is running on.</span></span> <span data-ttu-id="e1794-201">en règle générale 7071.</span><span class="sxs-lookup"><span data-stu-id="e1794-201">Typically the port is 7071.</span></span>

    ```powershell
    Invoke-RestMethod "http://localhost:<PORT>/api/AnalyzeSentiment" -Method Post -Body (@{SentimentText="This is a very bad steak"} | ConvertTo-Json) -ContentType "application/json"
    ```

    <span data-ttu-id="e1794-202">En cas de réussite, la sortie devrait se présenter ainsi :</span><span class="sxs-lookup"><span data-stu-id="e1794-202">If successful, the output should look similar to the text below:</span></span>
    
    ```powershell
    Negative
    ```

<span data-ttu-id="e1794-203">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="e1794-203">Congratulations!</span></span> <span data-ttu-id="e1794-204">Vous avez réussi à alimenter votre modèle de façon à effectuer des prédictions sur Internet à l’aide d’une fonction Azure.</span><span class="sxs-lookup"><span data-stu-id="e1794-204">You have successfully served your model to make predictions over the internet using an Azure Function.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e1794-205">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e1794-205">Next Steps</span></span>

- [<span data-ttu-id="e1794-206">Déployer sur Azure</span><span class="sxs-lookup"><span data-stu-id="e1794-206">Deploy to Azure</span></span>](/azure/azure-functions/functions-develop-vs#publish-to-azure)
