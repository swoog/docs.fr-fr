---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 06/04/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 7d2935fafe9dbad28205c8a896d97d80474a686f
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47436139"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a><span data-ttu-id="eac40-103">Tutoriel : Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments</span><span class="sxs-lookup"><span data-stu-id="eac40-103">Tutorial: Use ML.NET in a sentiment analysis binary classification scenario</span></span>

> [!NOTE]
> <span data-ttu-id="eac40-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="eac40-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="eac40-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="eac40-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="eac40-106">Cet exemple de tutoriel illustre l’utilisation de ML.NET pour créer un classifieur de sentiments via une application console .NET Core à l’aide de C# dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="eac40-106">This sample tutorial illustrates using ML.NET to create a sentiment classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="eac40-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="eac40-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="eac40-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="eac40-108">Understand the problem</span></span>
> * <span data-ttu-id="eac40-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="eac40-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="eac40-110">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="eac40-110">Prepare your data</span></span>
> * <span data-ttu-id="eac40-111">Créer le pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="eac40-111">Create the learning pipeline</span></span>
> * <span data-ttu-id="eac40-112">Charger un classifieur</span><span class="sxs-lookup"><span data-stu-id="eac40-112">Load a classifier</span></span>
> * <span data-ttu-id="eac40-113">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-113">Train the model</span></span>
> * <span data-ttu-id="eac40-114">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="eac40-114">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="eac40-115">Prédire les résultats des données de test avec le modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-115">Predict the test data outcomes with the model</span></span>

## <a name="sentiment-analysis-sample-overview"></a><span data-ttu-id="eac40-116">Vue d’ensemble d’un exemple d’analyse des sentiments</span><span class="sxs-lookup"><span data-stu-id="eac40-116">Sentiment analysis sample overview</span></span>

<span data-ttu-id="eac40-117">L’exemple est une application console qui utilise ML.NET pour effectuer l’apprentissage d’un modèle qui classifie et prédit un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="eac40-117">The sample is a console app that uses ML.NET to train a model that classifies and predicts sentiment as either positive or negative.</span></span> <span data-ttu-id="eac40-118">Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité.</span><span class="sxs-lookup"><span data-stu-id="eac40-118">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="eac40-119">Les jeux de données de sentiments proviennent du projet WikiDetox.</span><span class="sxs-lookup"><span data-stu-id="eac40-119">The sentiment datasets are from the WikiDetox project.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eac40-120">Prérequis</span><span class="sxs-lookup"><span data-stu-id="eac40-120">Prerequisites</span></span>

* <span data-ttu-id="eac40-121">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="eac40-121">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="eac40-122">Le [fichier Wikipédia séparé par des onglets, contenant des données sur la ligne de désintoxication (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span><span class="sxs-lookup"><span data-stu-id="eac40-122">The [Wikipedia detox line data tab separated file (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span></span>
* <span data-ttu-id="eac40-123">Le [fichier Wikipédia séparé par des onglets, contenant le test de la ligne de désintoxication (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span><span class="sxs-lookup"><span data-stu-id="eac40-123">The [Wikipedia detox line test tab separated file (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="eac40-124">Flux de travail de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="eac40-124">Machine learning workflow</span></span>

<span data-ttu-id="eac40-125">Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="eac40-125">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="eac40-126">Les phases du flux de travail sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eac40-126">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="eac40-127">**Comprendre le problème**</span><span class="sxs-lookup"><span data-stu-id="eac40-127">**Understand the problem**</span></span>
2. <span data-ttu-id="eac40-128">**Ingérer les données**</span><span class="sxs-lookup"><span data-stu-id="eac40-128">**Ingest the data**</span></span>
3. <span data-ttu-id="eac40-129">**Prétraiter les données et générer les fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="eac40-129">**Data preprocess and feature engineering**</span></span>
4. <span data-ttu-id="eac40-130">**Effectuer l’apprentissage du modèle et le prédire**</span><span class="sxs-lookup"><span data-stu-id="eac40-130">**Train and predict the model**</span></span>
5. <span data-ttu-id="eac40-131">**Évaluer le modèle**</span><span class="sxs-lookup"><span data-stu-id="eac40-131">**Evaluate the model**</span></span>
6. <span data-ttu-id="eac40-132">**Opérationnalisation du modèle**</span><span class="sxs-lookup"><span data-stu-id="eac40-132">**Model operationalization**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="eac40-133">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="eac40-133">Understand the problem</span></span>

<span data-ttu-id="eac40-134">Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-134">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="eac40-135">La décomposition du problème vous permet de prédire et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="eac40-135">Breaking the problem down allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="eac40-136">Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="eac40-136">The problem for this tutorial is to understand incoming website comment sentiment to take the appropriate action.</span></span>

<span data-ttu-id="eac40-137">Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="eac40-137">You can break down the problem to the sentiment text and sentiment value for the data you want to train the model with, and a predicted sentiment value that you can evaluate and then use operationally.</span></span>

<span data-ttu-id="eac40-138">Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="eac40-138">You then need to **determine** the sentiment, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="eac40-139">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="eac40-139">Select the appropriate machine learning task</span></span>

<span data-ttu-id="eac40-140">Pour ce problème, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="eac40-140">With this problem, you know the following facts:</span></span>

<span data-ttu-id="eac40-141">Données d’apprentissage : les commentaires sur le site web peuvent être positifs ou négatifs (**sentiment**).</span><span class="sxs-lookup"><span data-stu-id="eac40-141">Training data: website comments can be positive or negative (**sentiment**).</span></span>
<span data-ttu-id="eac40-142">Prédisez le **sentiment** d’un nouveau commentaire sur le site web, positif ou négatif, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="eac40-142">Predict the **sentiment** of a new website comment, either positive or negative, such as in the following examples:</span></span>

* <span data-ttu-id="eac40-143">Évitez d’ajouter des informations non pertinentes à Wikipédia.</span><span class="sxs-lookup"><span data-stu-id="eac40-143">Please refrain from adding nonsense to Wikipedia.</span></span>
* <span data-ttu-id="eac40-144">C’est le meilleur, et l’article doit le souligner.</span><span class="sxs-lookup"><span data-stu-id="eac40-144">He is the best, and the article should say that.</span></span>

<span data-ttu-id="eac40-145">La tâche d’apprentissage automatique de classification est idéale pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="eac40-145">The classification machine learning task is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="eac40-146">À propos de la tâche de classification</span><span class="sxs-lookup"><span data-stu-id="eac40-146">About the classification task</span></span>

<span data-ttu-id="eac40-147">La classification est une tâche d’apprentissage automatique qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="eac40-147">Classification is a machine learning task that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="eac40-148">Par exemple, vous pouvez utiliser la classification pour :</span><span class="sxs-lookup"><span data-stu-id="eac40-148">For example, you can use classification to:</span></span>

* <span data-ttu-id="eac40-149">Identifier un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="eac40-149">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="eac40-150">Classer un e-mail comme spam, indésirable ou autorisé.</span><span class="sxs-lookup"><span data-stu-id="eac40-150">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="eac40-151">Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.</span><span class="sxs-lookup"><span data-stu-id="eac40-151">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="eac40-152">Classer des clients selon leur tendance à répondre à une campagne commerciale.</span><span class="sxs-lookup"><span data-stu-id="eac40-152">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="eac40-153">Les tâches de classification sont souvent de ce type :</span><span class="sxs-lookup"><span data-stu-id="eac40-153">Classification tasks are frequently one of the following types:</span></span>

* <span data-ttu-id="eac40-154">Binaire : A ou B.</span><span class="sxs-lookup"><span data-stu-id="eac40-154">Binary: either A or B.</span></span>
* <span data-ttu-id="eac40-155">Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.</span><span class="sxs-lookup"><span data-stu-id="eac40-155">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="eac40-156">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="eac40-156">Create a console application</span></span>

1. <span data-ttu-id="eac40-157">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="eac40-157">Open Visual Studio 2017.</span></span> <span data-ttu-id="eac40-158">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="eac40-158">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="eac40-159">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="eac40-159">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="eac40-160">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="eac40-160">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="eac40-161">Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="eac40-161">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="eac40-162">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="eac40-162">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="eac40-163">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="eac40-163">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="eac40-164">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="eac40-164">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="eac40-165">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="eac40-165">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="eac40-166">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="eac40-166">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="eac40-167">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="eac40-167">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="eac40-168">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="eac40-168">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="eac40-169">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="eac40-169">Prepare your data</span></span>

1. <span data-ttu-id="eac40-170">Téléchargez les jeux de données [WikiPedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) et [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="eac40-170">Download the [WikiPedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) and the [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="eac40-171">Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-171">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="eac40-172">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="eac40-172">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="eac40-173">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="eac40-173">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="eac40-174">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="eac40-174">Create classes and define paths</span></span>

<span data-ttu-id="eac40-175">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="eac40-175">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="eac40-176">Vous devez créer trois champs globaux pour contenir les chemins des fichiers récemment téléchargés :</span><span class="sxs-lookup"><span data-stu-id="eac40-176">You need to create three global fields to hold the paths to the recently downloaded files:</span></span>

* <span data-ttu-id="eac40-177">`_dataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-177">`_dataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="eac40-178">`_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-178">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="eac40-179">`_modelPath` contient le chemin d’accès où le modèle formé est enregistré.</span><span class="sxs-lookup"><span data-stu-id="eac40-179">`_modelPath` has the path where the trained model is saved.</span></span>

<span data-ttu-id="eac40-180">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="eac40-180">Add the following code to the line right above the `Main` method to specify those paths:</span></span>

[!code-csharp[Declare file variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#2 "Declare variables to store data files")]

<span data-ttu-id="eac40-181">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="eac40-181">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="eac40-182">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="eac40-182">Add a new class to your project:</span></span>

1. <span data-ttu-id="eac40-183">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="eac40-183">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="eac40-184">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="eac40-184">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="eac40-185">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="eac40-185">Then, select the **Add** button.</span></span>

    <span data-ttu-id="eac40-186">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="eac40-186">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="eac40-187">Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="eac40-187">Add the following `using` statement to the top of *SentimentData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#1 "Add necessary usings")]

<span data-ttu-id="eac40-188">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="eac40-188">Remove the existing class definition and add the following code, which has two classes `SentimentData` and `SentimentPrediction`, to the *SentimentData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#2 "Declare data record types")]

<span data-ttu-id="eac40-189">`SentimentData` représente la classe du jeu de données d’entrée et contient un élément `float` (`Sentiment`) qui a une valeur de sentiment positive ou négative ainsi qu’une chaîne pour le commentaire (`SentimentText`).</span><span class="sxs-lookup"><span data-stu-id="eac40-189">`SentimentData` is the input dataset class and has a `float` (`Sentiment`) that has a value for sentiment of either positive or negative, and a string for the comment (`SentimentText`).</span></span> <span data-ttu-id="eac40-190">Les deux champs sont associés à des attributs `Column`.</span><span class="sxs-lookup"><span data-stu-id="eac40-190">Both fields have `Column` attributes attached to them.</span></span> <span data-ttu-id="eac40-191">Cet attribut décrit l’ordre de chaque champ dans le fichier de données, et désigne le champ `Label`.</span><span class="sxs-lookup"><span data-stu-id="eac40-191">This attribute describes the order of each field in the data file, and which is the `Label` field.</span></span> <span data-ttu-id="eac40-192">`SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="eac40-192">`SentimentPrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="eac40-193">Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`.</span><span class="sxs-lookup"><span data-stu-id="eac40-193">It has a single boolean (`Sentiment`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="eac40-194">L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-194">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="eac40-195">L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="eac40-195">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="eac40-196">L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-196">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="eac40-197">Dans le fichier *Program.cs*, modifiez la signature de la méthode `Main` en remplaçant `void` par `async Task`, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-197">In the *Program.cs* file, change the `Main` method signature by replacing `void` with `async Task`, as in the following example:</span></span>

```csharp
static async Task Main(string[] args) 
{

}
```

<span data-ttu-id="eac40-198">Vous ajoutez `async` à `Main` avec un type de retour <xref:System.Threading.Tasks.Task> car vous enregistrerez ultérieurement le modèle dans un fichier zip, et le programme doit attendre que cette tâche externe se termine.</span><span class="sxs-lookup"><span data-stu-id="eac40-198">You add `async` to `Main` with a <xref:System.Threading.Tasks.Task> return type because you're saving the model to a zip file later, and the program needs to wait until that external task completes.</span></span>

> [!NOTE]
> <span data-ttu-id="eac40-199">Une méthode *async main* vous permet d’utiliser `await` dans votre méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="eac40-199">An *async main* method enables you to use `await` in your `Main` method.</span></span> <span data-ttu-id="eac40-200">Pour plus d’informations, consultez la rubrique [async main](../../../docs/csharp/programming-guide/main-and-command-args/index.md) du guide de programmation C#.</span><span class="sxs-lookup"><span data-stu-id="eac40-200">For more information, see the [async main](../../../docs/csharp/programming-guide/main-and-command-args/index.md) topic in the C# programming guide.</span></span>

<span data-ttu-id="eac40-201">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="eac40-201">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#3 "Train your model")]

<span data-ttu-id="eac40-202">La méthode `Train` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="eac40-202">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="eac40-203">Charge ou ingère les données.</span><span class="sxs-lookup"><span data-stu-id="eac40-203">Loads or ingests the data.</span></span>
* <span data-ttu-id="eac40-204">Prétraite et fonctionnalise les données.</span><span class="sxs-lookup"><span data-stu-id="eac40-204">Preprocesses and featurizes the data.</span></span>
* <span data-ttu-id="eac40-205">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-205">Trains the model.</span></span>
* <span data-ttu-id="eac40-206">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="eac40-206">Predicts sentiment based on test data.</span></span>

<span data-ttu-id="eac40-207">Créez la méthode `Train` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-207">Create the `Train` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static async Task<PredictionModel<SentimentData, SentimentPrediction>> Train()
{

}
```

## <a name="ingest-the-data"></a><span data-ttu-id="eac40-208">Ingérer les données</span><span class="sxs-lookup"><span data-stu-id="eac40-208">Ingest the data</span></span>

<span data-ttu-id="eac40-209">Initialise une nouvelle instance de <xref:Microsoft.ML.LearningPipeline>, qui inclut le chargement des données, le traitement/la fonctionnalisation des données, et le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-209">Initialize a new instance of <xref:Microsoft.ML.LearningPipeline> that will include the data loading, data processing/featurization, and model.</span></span> <span data-ttu-id="eac40-210">Ajoutez le code suivant comme première ligne de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="eac40-210">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LearningPipeline](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#5 "Create a learning pipeline")]

<span data-ttu-id="eac40-211">L’objet <xref:Microsoft.ML.Data.TextLoader> est la première partie du pipeline, et charge les données du fichier d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="eac40-211">The <xref:Microsoft.ML.Data.TextLoader> object is the first part of the pipeline, and loads the training file data.</span></span>

[!code-csharp[TextLoader](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#6 "Add a text loader to the pipeline")]

## <a name="data-preprocess-and-feature-engineering"></a><span data-ttu-id="eac40-212">Prétraiter les données et générer les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="eac40-212">Data preprocess and feature engineering</span></span>

<span data-ttu-id="eac40-213">Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="eac40-213">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="eac40-214">Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="eac40-214">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="eac40-215">L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.</span><span class="sxs-lookup"><span data-stu-id="eac40-215">Using data without these modeling tasks can produce misleading results.</span></span> <span data-ttu-id="eac40-216">Les pipelines de transformation ML.NET vous permettent de composer un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test.</span><span class="sxs-lookup"><span data-stu-id="eac40-216">ML.NET's transform pipelines allow you to compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="eac40-217">Les transformations servent principalement à fonctionnaliser les données.</span><span class="sxs-lookup"><span data-stu-id="eac40-217">The transforms' primary purpose is for data featurization.</span></span> <span data-ttu-id="eac40-218">Un pipeline de transformation offre l’avantage suivant : après définition du pipeline de transformation, vous pouvez enregistrer le pipeline pour tester les données.</span><span class="sxs-lookup"><span data-stu-id="eac40-218">A transform pipeline's advantage is that after transform pipeline definition, save the pipeline to apply it to test data.</span></span>

<span data-ttu-id="eac40-219">Appliquez un pipeline <xref:Microsoft.ML.Transforms.TextFeaturizer> pour convertir la colonne `SentimentText` en un [vecteur numérique](../resources/glossary.md#numerical-feature-vector) appelé `Features` utilisé par l’algorithme d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="eac40-219">Apply a <xref:Microsoft.ML.Transforms.TextFeaturizer> to convert the `SentimentText` column into a [numeric vector](../resources/glossary.md#numerical-feature-vector) called `Features` used by the machine learning algorithm.</span></span> <span data-ttu-id="eac40-220">Il s’agit de l’étape de prétraitement/fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="eac40-220">This is the preprocessing/featurization step.</span></span> <span data-ttu-id="eac40-221">L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-221">Using additional components available in ML.NET can enable better results with your model.</span></span> <span data-ttu-id="eac40-222">Ajoutez `TextFeaturizer` au pipeline comme ligne de code suivante :</span><span class="sxs-lookup"><span data-stu-id="eac40-222">Add `TextFeaturizer` to the pipeline as the next line of code:</span></span>

[!code-csharp[TextFeaturizer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#7 "Add a TextFeaturizer to the pipeline")]

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="eac40-223">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="eac40-223">Choose a learning algorithm</span></span>

<span data-ttu-id="eac40-224">L’objet <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier> est un apprenant d’arbre de décision que vous utiliserez dans ce pipeline.</span><span class="sxs-lookup"><span data-stu-id="eac40-224">The <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier> object is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="eac40-225">Comme pour l’étape de fonctionnalisation, si vous testez les différents apprenants disponibles dans ML.NET et modifiez leurs paramètres, vous obtenez des résultats différents.</span><span class="sxs-lookup"><span data-stu-id="eac40-225">Similar to the featurization step, trying out different learners available in ML.NET and changing their parameters leads to different results.</span></span> <span data-ttu-id="eac40-226">Pour le paramétrage, vous pouvez définir des [hyperparamètres](../resources/glossary.md#hyperparameter) comme <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumTrees>, <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumLeaves> et <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.MinDocumentsInLeafs>.</span><span class="sxs-lookup"><span data-stu-id="eac40-226">For tuning, you can set [hyperparameters](../resources/glossary.md#hyperparameter) like <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumTrees>, <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumLeaves>, and <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.MinDocumentsInLeafs>.</span></span> <span data-ttu-id="eac40-227">Spécifiques au modèle, ces hyperparamètres sont définis avant qu’un élément quelconque n’affecte le modèle.</span><span class="sxs-lookup"><span data-stu-id="eac40-227">These hyperparameters are set before anything affects the model and are model-specific.</span></span> <span data-ttu-id="eac40-228">Ils sont utilisés pour paramétrer l’arbre de décision pour les performances et, par conséquent, les valeurs trop grandes peuvent nuire à ces performances.</span><span class="sxs-lookup"><span data-stu-id="eac40-228">They're used to tune the decision tree for performance, so larger values can negatively impact performance.</span></span>

<span data-ttu-id="eac40-229">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="eac40-229">Add the following code to the `Train` method:</span></span>

[!code-csharp[BinaryClassifier](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#8 "Add a fast binary tree classifier")]

## <a name="train-the-model"></a><span data-ttu-id="eac40-230">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-230">Train the model</span></span>

<span data-ttu-id="eac40-231">Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.PredictionModel%602>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="eac40-231">You train the model, <xref:Microsoft.ML.PredictionModel%602>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="eac40-232">`pipeline.Train<SentimentData, SentimentPrediction>()` effectue l’apprentissage du pipeline (charge les données, forme le générateur de fonctionnalités et l’apprenant).</span><span class="sxs-lookup"><span data-stu-id="eac40-232">`pipeline.Train<SentimentData, SentimentPrediction>()` trains the pipeline (loads the data, trains the featurizer and learner).</span></span> <span data-ttu-id="eac40-233">L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="eac40-233">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="eac40-234">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="eac40-234">Add the following code to the `Train` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#9 "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="eac40-235">Enregistrer et revenir au modèle formé à utiliser pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="eac40-235">Save and Return the model trained to use for evaluation</span></span>

<span data-ttu-id="eac40-236">À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="eac40-236">At this point, you have a model that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="eac40-237">Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code à la ligne suivante dans `Train` :</span><span class="sxs-lookup"><span data-stu-id="eac40-237">To save your model to a .zip file before returning, add the following code to the next line in `Train`:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#10 "Save the model")]

<span data-ttu-id="eac40-238">Retournez le modèle à la fin de la méthode `Train`.</span><span class="sxs-lookup"><span data-stu-id="eac40-238">Return the model at the end of the `Train` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#11 "Return the model")]

## <a name="evaluate-the-model"></a><span data-ttu-id="eac40-239">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-239">Evaluate the model</span></span>

<span data-ttu-id="eac40-240">Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation.</span><span class="sxs-lookup"><span data-stu-id="eac40-240">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="eac40-241">Dans la méthode `Evaluate`, le modèle créé dans `Train` est passé pour évaluation.</span><span class="sxs-lookup"><span data-stu-id="eac40-241">In the `Evaluate` method, the model created in `Train` is passed in to be evaluated.</span></span> <span data-ttu-id="eac40-242">Créez la méthode `Evaluate` juste après `Train`, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-242">Create the `Evaluate` method, just after `Train`, as in the following code:</span></span>

```csharp
public static void Evaluate(PredictionModel<SentimentData, SentimentPrediction> model)
{

}
```

<span data-ttu-id="eac40-243">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="eac40-243">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="eac40-244">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="eac40-244">Loads the test dataset.</span></span>
* <span data-ttu-id="eac40-245">Crée l’évaluateur binaire.</span><span class="sxs-lookup"><span data-stu-id="eac40-245">Creates the binary evaluator.</span></span>
* <span data-ttu-id="eac40-246">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="eac40-246">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="eac40-247">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="eac40-247">Displays the metrics.</span></span>

<span data-ttu-id="eac40-248">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-248">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#12 "Call the Evaluate method")]

<span data-ttu-id="eac40-249">La classe <xref:Microsoft.ML.Data.TextLoader> charge le nouveau jeu de données de test avec le même schéma.</span><span class="sxs-lookup"><span data-stu-id="eac40-249">The <xref:Microsoft.ML.Data.TextLoader> class loads the new test dataset with the same schema.</span></span> <span data-ttu-id="eac40-250">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="eac40-250">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="eac40-251">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="eac40-251">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadText](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#13 "Load the test dataset")]

<span data-ttu-id="eac40-252">L’objet <xref:Microsoft.ML.Models.BinaryClassificationEvaluator> calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="eac40-252">The <xref:Microsoft.ML.Models.BinaryClassificationEvaluator> object computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="eac40-253">Pour afficher ces métriques, ajoutez l’évaluateur comme ligne suivante dans la méthode `Evaluate`, avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-253">To see those metrics, add the evaluator as the next line in the `Evaluate` method, with the following code:</span></span>

[!code-csharp[BinaryEvaluator](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#14 "Create the binary evaluator")]

<span data-ttu-id="eac40-254"><xref:Microsoft.ML.Models.BinaryClassificationMetrics> contient les métriques globales calculées par les évaluateurs de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="eac40-254">The <xref:Microsoft.ML.Models.BinaryClassificationMetrics> contains the overall metrics computed by binary classification evaluators.</span></span> <span data-ttu-id="eac40-255">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="eac40-255">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="eac40-256">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-256">Add the following code:</span></span>

[!code-csharp[CreateMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#15 "Evaluate the model and create metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="eac40-257">Affichage des métriques pour la validation du modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-257">Displaying the metrics for model validation</span></span>

<span data-ttu-id="eac40-258">Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :</span><span class="sxs-lookup"><span data-stu-id="eac40-258">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#16 "Display selected metrics")]

## <a name="predict-the-test-data-outcomes-with-the-model"></a><span data-ttu-id="eac40-259">Prédire les résultats des données de test avec le modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-259">Predict the test data outcomes with the model</span></span>

<span data-ttu-id="eac40-260">Créez la méthode `Predict` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-260">Create the `Predict` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
public static void Predict(PredictionModel<SentimentData, SentimentPrediction> model)
{

}
```

<span data-ttu-id="eac40-261">La méthode `Predict` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="eac40-261">The `Predict` method executes the following tasks:</span></span>

* <span data-ttu-id="eac40-262">Crée les données de test.</span><span class="sxs-lookup"><span data-stu-id="eac40-262">Creates test data.</span></span>
* <span data-ttu-id="eac40-263">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="eac40-263">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="eac40-264">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="eac40-264">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="eac40-265">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="eac40-265">Displays the predicted results.</span></span>

<span data-ttu-id="eac40-266">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-266">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#17 "Call the Predict method")]

<span data-ttu-id="eac40-267">Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `Predict` :</span><span class="sxs-lookup"><span data-stu-id="eac40-267">Add some comments to test the trained model's predictions in the `Predict` method:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#18 "Create test data for predictions")]

<span data-ttu-id="eac40-268">Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.PredictionModel.Predict%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="eac40-268">Now that you have a model, you can use that to predict the positive or negative sentiment of the comment data using the <xref:Microsoft.ML.PredictionModel.Predict%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="eac40-269">Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="eac40-269">To get a prediction, use `Predict` on new data.</span></span> <span data-ttu-id="eac40-270">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="eac40-270">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="eac40-271">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="eac40-271">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="eac40-272">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="eac40-272">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#19 "Create predictions of sentiments")]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="eac40-273">Opérationnalisation du modèle : prédiction</span><span class="sxs-lookup"><span data-stu-id="eac40-273">Model operationalization: prediction</span></span>

<span data-ttu-id="eac40-274">Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="eac40-274">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="eac40-275">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="eac40-275">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="eac40-276">Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-276">Create a header for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#20 "Display prediction outputs")]

<span data-ttu-id="eac40-277">Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit.</span><span class="sxs-lookup"><span data-stu-id="eac40-277">Before displaying the predicted results, combine the sentiment and prediction together to see the original comment with its predicted sentiment.</span></span> <span data-ttu-id="eac40-278">Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="eac40-278">The following code uses the <xref:System.Linq.Enumerable.Zip%2A> method to make that happen, so add that code next:</span></span>

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#21 "Build the pairs of sentiment data and predictions")]

<span data-ttu-id="eac40-279">Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :</span><span class="sxs-lookup"><span data-stu-id="eac40-279">Now that you've combined the `SentimentText` and `Sentiment` into a class, you can display the results using the <xref:System.Console.WriteLine?displayProperty=nameWithType> method:</span></span>

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#22 "Display the predictions")]

<span data-ttu-id="eac40-280">Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="eac40-280">Because inferred tuple element names are a new feature in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span>
<span data-ttu-id="eac40-281">Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="eac40-281">To do that, right-click on the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="eac40-282">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="eac40-282">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="eac40-283">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="eac40-283">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="eac40-284">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="eac40-284">Select the **OK** button.</span></span>

## <a name="results"></a><span data-ttu-id="eac40-285">Résultats</span><span class="sxs-lookup"><span data-stu-id="eac40-285">Results</span></span>

<span data-ttu-id="eac40-286">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="eac40-286">Your results should be similar to the following.</span></span> <span data-ttu-id="eac40-287">Lors du traitement, le pipeline affiche des messages.</span><span class="sxs-lookup"><span data-stu-id="eac40-287">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="eac40-288">Vous pouvez voir des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="eac40-288">You may see warnings, or processing messages.</span></span> <span data-ttu-id="eac40-289">Ils ont été supprimés des résultats ci-dessous par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="eac40-289">These have been removed from the following results for clarity.</span></span>

```

PredictionModel quality metrics evaluation
------------------------------------------
Accuracy: 66.67%
Auc: 94.44%
F1Score: 75.00%

Sentiment Predictions
---------------------
Sentiment: Please refrain from adding nonsense to Wikipedia. | Prediction: Negative
Sentiment: He is the best, and the article should say that. | Prediction: Positive

```

<span data-ttu-id="eac40-290">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="eac40-290">Congratulations!</span></span> <span data-ttu-id="eac40-291">Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction des sentiments de messages.</span><span class="sxs-lookup"><span data-stu-id="eac40-291">You've now successfully built a machine learning model for classifying and predicting messages sentiment.</span></span> <span data-ttu-id="eac40-292">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).</span><span class="sxs-lookup"><span data-stu-id="eac40-292">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eac40-293">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eac40-293">Next steps</span></span>

<span data-ttu-id="eac40-294">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="eac40-294">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="eac40-295">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="eac40-295">Understand the problem</span></span>
> * <span data-ttu-id="eac40-296">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="eac40-296">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="eac40-297">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="eac40-297">Prepare your data</span></span>
> * <span data-ttu-id="eac40-298">Créer le pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="eac40-298">Create the learning pipeline</span></span>
> * <span data-ttu-id="eac40-299">Charger un classifieur</span><span class="sxs-lookup"><span data-stu-id="eac40-299">Load a classifier</span></span>
> * <span data-ttu-id="eac40-300">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-300">Train the model</span></span>
> * <span data-ttu-id="eac40-301">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="eac40-301">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="eac40-302">Prédire les résultats des données de test avec le modèle</span><span class="sxs-lookup"><span data-stu-id="eac40-302">Predict the test data outcomes with the model</span></span>

<span data-ttu-id="eac40-303">Passer au tutoriel suivant pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="eac40-303">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="eac40-304">Prédiction du prix d’une course de taxi</span><span class="sxs-lookup"><span data-stu-id="eac40-304">Taxi Fare Predictor</span></span>](taxi-fare.md)
