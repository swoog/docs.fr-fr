---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 02/15/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: d6d5cae107e25000add5c8430a35131a79696bc2
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092759"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a><span data-ttu-id="3e49f-103">Tutoriel : Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments</span><span class="sxs-lookup"><span data-stu-id="3e49f-103">Tutorial: Use ML.NET in a sentiment analysis binary classification scenario</span></span>

> [!NOTE]
> <span data-ttu-id="3e49f-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="3e49f-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="3e49f-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="3e49f-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="3e49f-106">Cet exemple de tutoriel illustre l’utilisation de ML.NET pour créer un classifieur de sentiments via une application console .NET Core à l’aide de C# dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="3e49f-106">This sample tutorial illustrates using ML.NET to create a sentiment classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="3e49f-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="3e49f-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="3e49f-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="3e49f-108">Understand the problem</span></span>
> * <span data-ttu-id="3e49f-109">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="3e49f-109">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="3e49f-110">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="3e49f-110">Prepare your data</span></span>
> * <span data-ttu-id="3e49f-111">Transformer les données</span><span class="sxs-lookup"><span data-stu-id="3e49f-111">Transform the data</span></span>
> * <span data-ttu-id="3e49f-112">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-112">Train the model</span></span>
> * <span data-ttu-id="3e49f-113">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-113">Evaluate the model</span></span>
> * <span data-ttu-id="3e49f-114">Prédire avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="3e49f-114">Predict with the trained model</span></span>
> * <span data-ttu-id="3e49f-115">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="3e49f-115">Deploy and Predict with a loaded model</span></span>

## <a name="sentiment-analysis-sample-overview"></a><span data-ttu-id="3e49f-116">Vue d’ensemble d’un exemple d’analyse des sentiments</span><span class="sxs-lookup"><span data-stu-id="3e49f-116">Sentiment analysis sample overview</span></span>

<span data-ttu-id="3e49f-117">L’exemple est une application console qui utilise ML.NET pour effectuer l’apprentissage d’un modèle qui classifie et prédit un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="3e49f-117">The sample is a console app that uses ML.NET to train a model that classifies and predicts sentiment as either positive or negative.</span></span> <span data-ttu-id="3e49f-118">Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité.</span><span class="sxs-lookup"><span data-stu-id="3e49f-118">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="3e49f-119">Les jeux de données de sentiments proviennent du projet WikiDetox.</span><span class="sxs-lookup"><span data-stu-id="3e49f-119">The sentiment datasets are from the WikiDetox project.</span></span>

<span data-ttu-id="3e49f-120">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).</span><span class="sxs-lookup"><span data-stu-id="3e49f-120">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e49f-121">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3e49f-121">Prerequisites</span></span>

* <span data-ttu-id="3e49f-122">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="3e49f-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="3e49f-123">Le [fichier Wikipédia séparé par des onglets, contenant des données sur la ligne de désintoxication (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span><span class="sxs-lookup"><span data-stu-id="3e49f-123">The [Wikipedia detox line data tab separated file (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).</span></span>
* <span data-ttu-id="3e49f-124">Le [fichier Wikipédia séparé par des onglets, contenant le test de la ligne de désintoxication (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span><span class="sxs-lookup"><span data-stu-id="3e49f-124">The [Wikipedia detox line test tab separated file (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="3e49f-125">Flux de travail de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="3e49f-125">Machine learning workflow</span></span>

<span data-ttu-id="3e49f-126">Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="3e49f-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="3e49f-127">Les phases du flux de travail sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="3e49f-128">**Comprendre le problème**</span><span class="sxs-lookup"><span data-stu-id="3e49f-128">**Understand the problem**</span></span>
2. <span data-ttu-id="3e49f-129">**Préparer vos données**</span><span class="sxs-lookup"><span data-stu-id="3e49f-129">**Prepare your data**</span></span>
   * <span data-ttu-id="3e49f-130">**Charger les données**</span><span class="sxs-lookup"><span data-stu-id="3e49f-130">**Load the data**</span></span>
   * <span data-ttu-id="3e49f-131">**Extraire des caractéristiques (transformer vos données)**</span><span class="sxs-lookup"><span data-stu-id="3e49f-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="3e49f-132">**Générer et former**</span><span class="sxs-lookup"><span data-stu-id="3e49f-132">**Build and train**</span></span> 
   * <span data-ttu-id="3e49f-133">**Effectuer l’apprentissage du modèle**</span><span class="sxs-lookup"><span data-stu-id="3e49f-133">**Train the model**</span></span>
   * <span data-ttu-id="3e49f-134">**Évaluer le modèle**</span><span class="sxs-lookup"><span data-stu-id="3e49f-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="3e49f-135">**Déployer le modèle**</span><span class="sxs-lookup"><span data-stu-id="3e49f-135">**Deploy Model**</span></span>
   * <span data-ttu-id="3e49f-136">**Utiliser le modèle pour prédire**</span><span class="sxs-lookup"><span data-stu-id="3e49f-136">**Use the Model to predict**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="3e49f-137">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="3e49f-137">Understand the problem</span></span>

<span data-ttu-id="3e49f-138">Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="3e49f-139">La décomposition du problème vous permet de prédire et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="3e49f-139">Breaking the problem down allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="3e49f-140">Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="3e49f-140">The problem for this tutorial is to understand incoming website comment sentiment to take the appropriate action.</span></span>

<span data-ttu-id="3e49f-141">Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-141">You can break down the problem to the sentiment text and sentiment value for the data you want to train the model with, and a predicted sentiment value that you can evaluate and then use operationally.</span></span>

<span data-ttu-id="3e49f-142">Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="3e49f-142">You then need to **determine** the sentiment, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-algorithm"></a><span data-ttu-id="3e49f-143">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="3e49f-143">Select the appropriate machine learning algorithm</span></span>

<span data-ttu-id="3e49f-144">Pour ce problème, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3e49f-144">With this problem, you know the following facts:</span></span>

<span data-ttu-id="3e49f-145">Données d’apprentissage : les commentaires sur le site web peuvent être positifs (1) ou négatifs (0) (**sentiment**).</span><span class="sxs-lookup"><span data-stu-id="3e49f-145">Training data: website comments can be toxic (1) or not toxic (0) (**sentiment**).</span></span>
<span data-ttu-id="3e49f-146">Prédisez le **sentiment** d’un nouveau commentaire sur le site web, positif ou négatif, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="3e49f-146">Predict the **sentiment** of a new website comment, either toxic or not toxic, such as in the following examples:</span></span>

* <span data-ttu-id="3e49f-147">Évitez d’ajouter des informations non pertinentes à Wikipédia.</span><span class="sxs-lookup"><span data-stu-id="3e49f-147">Please refrain from adding nonsense to Wikipedia.</span></span>
* <span data-ttu-id="3e49f-148">C’est le meilleur, et l’article doit le souligner.</span><span class="sxs-lookup"><span data-stu-id="3e49f-148">He is the best, and the article should say that.</span></span>

<span data-ttu-id="3e49f-149">L’algorithme de machine learning de classification est idéal pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="3e49f-149">The classification machine learning algorithm is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="3e49f-150">À propos de la tâche de classification</span><span class="sxs-lookup"><span data-stu-id="3e49f-150">About the classification task</span></span>

<span data-ttu-id="3e49f-151">La classification est un algorithme de machine learning qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-151">Classification is a machine learning algorithm that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="3e49f-152">Par exemple, vous pouvez utiliser la classification pour :</span><span class="sxs-lookup"><span data-stu-id="3e49f-152">For example, you can use classification to:</span></span>

* <span data-ttu-id="3e49f-153">Identifier un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="3e49f-153">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="3e49f-154">Classer un e-mail comme spam, indésirable ou autorisé.</span><span class="sxs-lookup"><span data-stu-id="3e49f-154">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="3e49f-155">Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.</span><span class="sxs-lookup"><span data-stu-id="3e49f-155">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="3e49f-156">Classer des clients selon leur tendance à répondre à une campagne commerciale.</span><span class="sxs-lookup"><span data-stu-id="3e49f-156">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="3e49f-157">Les algorithmes de classification sont souvent de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="3e49f-157">Classification algorithms are frequently one of the following types:</span></span>

* <span data-ttu-id="3e49f-158">Binaire : A ou B.</span><span class="sxs-lookup"><span data-stu-id="3e49f-158">Binary: either A or B.</span></span>
* <span data-ttu-id="3e49f-159">Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.</span><span class="sxs-lookup"><span data-stu-id="3e49f-159">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="3e49f-160">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="3e49f-160">Create a console application</span></span>

1. <span data-ttu-id="3e49f-161">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="3e49f-161">Open Visual Studio 2017.</span></span> <span data-ttu-id="3e49f-162">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="3e49f-162">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="3e49f-163">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-163">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="3e49f-164">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-164">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="3e49f-165">Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-165">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="3e49f-166">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="3e49f-166">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="3e49f-167">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-167">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="3e49f-168">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="3e49f-168">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="3e49f-169">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="3e49f-169">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="3e49f-170">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-170">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="3e49f-171">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-171">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="3e49f-172">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="3e49f-172">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="3e49f-173">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="3e49f-173">Prepare your data</span></span>

1. <span data-ttu-id="3e49f-174">Téléchargez les jeux de données [Wikipedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) et [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="3e49f-174">Download the [Wikipedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) and the [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="3e49f-175">Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-175">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="3e49f-176">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-176">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="3e49f-177">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-177">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="3e49f-178">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="3e49f-178">Create classes and define paths</span></span>

<span data-ttu-id="3e49f-179">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="3e49f-179">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="3e49f-180">Vous devez créer trois champs globaux pour contenir les chemins d’accès aux fichiers récemment téléchargés, et une variable globale pour `TextLoader` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-180">You need to create three global fields to hold the paths to the recently downloaded files, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="3e49f-181">`_trainDataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-181">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="3e49f-182">`_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-182">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="3e49f-183">`_modelPath` contient le chemin d’accès où le modèle formé est enregistré.</span><span class="sxs-lookup"><span data-stu-id="3e49f-183">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="3e49f-184">`_textLoader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-184">`_textLoader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="3e49f-185">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins et la variable `_textLoader` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-185">Add the following code to the line right above the `Main` method to specify those paths and the `_textLoader` variable:</span></span>

[!code-csharp[Declare global variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#2 "Declare global variables")]

<span data-ttu-id="3e49f-186">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="3e49f-186">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="3e49f-187">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="3e49f-187">Add a new class to your project:</span></span>

1. <span data-ttu-id="3e49f-188">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-188">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="3e49f-189">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="3e49f-189">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="3e49f-190">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-190">Then, select the **Add** button.</span></span>

    <span data-ttu-id="3e49f-191">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="3e49f-191">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="3e49f-192">Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="3e49f-192">Add the following `using` statement to the top of *SentimentData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#1 "Add necessary usings")]

<span data-ttu-id="3e49f-193">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="3e49f-193">Remove the existing class definition and add the following code, which has two classes `SentimentData` and `SentimentPrediction`, to the *SentimentData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#2 "Declare data record types")]

<span data-ttu-id="3e49f-194">`SentimentData` représente la classe du jeu de données d’entrée et contient un élément `float` (`Sentiment`) qui a une valeur de sentiment positive ou négative ainsi qu’une chaîne pour le commentaire (`SentimentText`).</span><span class="sxs-lookup"><span data-stu-id="3e49f-194">`SentimentData` is the input dataset class and has a `float` (`Sentiment`) that has a value for sentiment of either positive or negative, and a string for the comment (`SentimentText`).</span></span> <span data-ttu-id="3e49f-195">Les deux champs sont associés à des attributs `Column`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-195">Both fields have `Column` attributes attached to them.</span></span> <span data-ttu-id="3e49f-196">Cet attribut décrit l’ordre de chaque champ dans le fichier de données, et désigne le champ `Label`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-196">This attribute describes the order of each field in the data file, and which is the `Label` field.</span></span> <span data-ttu-id="3e49f-197">`SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="3e49f-197">`SentimentPrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="3e49f-198">Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-198">It has a single boolean (`Sentiment`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="3e49f-199">L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-199">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="3e49f-200">L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-200">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="3e49f-201">L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-201">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="3e49f-202">Lors de la création d’un modèle avec ML .NET, vous commencez par créer un `MLContext`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-202">When building a model with ML.NET you start by creating an `MLContext`.</span></span> <span data-ttu-id="3e49f-203">Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="3e49f-203">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="3e49f-204">L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-204">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="3e49f-205">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="3e49f-205">Initialize variables in Main</span></span>

<span data-ttu-id="3e49f-206">Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-206">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="3e49f-207">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-207">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#3 "Create the ML Context")]

<span data-ttu-id="3e49f-208">Ensuite, pour configurer le chargement des données, initialisez variable globale `_textLoader` afin de la réutiliser.</span><span class="sxs-lookup"><span data-stu-id="3e49f-208">Next, to setup for data loading initialize the `_textLoader` global variable in order to reuse it.</span></span>  <span data-ttu-id="3e49f-209">Quand vous créez un `TextLoader` à l’aide d’un `MLContext.Data.CreateTextLoader`, vous passez le contexte nécessaire et la classe <xref:Microsoft.ML.Data.TextLoader.Arguments> qui permet la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-209">When you create a `TextLoader` using  `MLContext.Data.CreateTextLoader`, you pass in the context needed and the <xref:Microsoft.ML.Data.TextLoader.Arguments> class which enables customization.</span></span>

 <span data-ttu-id="3e49f-210">Spécifiez le schéma de données en passant un tableau d’objets <xref:Microsoft.ML.Data.TextLoader.Column> au chargeur contenant tous les noms de colonne et leurs types.</span><span class="sxs-lookup"><span data-stu-id="3e49f-210">Specify the data schema by passing an array of <xref:Microsoft.ML.Data.TextLoader.Column> objects to the loader containing all the column names and their types.</span></span> <span data-ttu-id="3e49f-211">Vous avez défini précédemment le schéma de données en créant notre classe `SentimentData`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-211">You defined the data schema previously when you created our `SentimentData` class.</span></span> <span data-ttu-id="3e49f-212">Pour notre schéma, la première colonne (étiquette) est une <xref:System.Boolean> (la prédiction) et la deuxième colonne (SentimentText) est la caractéristique de type texte/chaîne utilisée pour prédire le sentiment.</span><span class="sxs-lookup"><span data-stu-id="3e49f-212">For our schema, the first column (Label) is a <xref:System.Boolean> (the prediction) and the second column (SentimentText) is the feature of type text/string used for predicting the sentiment.</span></span>
<span data-ttu-id="3e49f-213">La classe `TextLoader` retourne une variable <xref:Microsoft.ML.Data.TextLoader> totalement initialisée</span><span class="sxs-lookup"><span data-stu-id="3e49f-213">The `TextLoader` class returns a fully initialized <xref:Microsoft.ML.Data.TextLoader></span></span>  

<span data-ttu-id="3e49f-214">Pour initialiser la variable globale `_textLoader` afin de la réutiliser pour les jeux de données nécessaires, ajoutez le code suivant après l’initialisation de `mlContext` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-214">To initialize the `_textLoader` global variable in order to reuse it for the needed datasets, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[initTextLoader](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#4 "Initialize the TextLoader")]

<span data-ttu-id="3e49f-215">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-215">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#5 "Train your model")]

<span data-ttu-id="3e49f-216">La méthode `Train` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-216">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="3e49f-217">Charge les données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-217">Loads the data.</span></span>
* <span data-ttu-id="3e49f-218">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-218">Extracts and transforms the data.</span></span>
* <span data-ttu-id="3e49f-219">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-219">Trains the model.</span></span>
* <span data-ttu-id="3e49f-220">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-220">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="3e49f-221">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-221">Returns the model.</span></span>

<span data-ttu-id="3e49f-222">Créez la méthode `Train` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-222">Create the `Train` method, just after the `Main` method, using the following code:</span></span>

```csharp
 public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

<span data-ttu-id="3e49f-223">Notez que les deux paramètres sont passés dans la méthode Train ; un `MLContext` pour le contexte (`mlContext`) et un <xref:System.String> pour le chemin d’accès au jeu de données (`dataPath`).</span><span class="sxs-lookup"><span data-stu-id="3e49f-223">Notice that two parameters are passed into the Train method; a `MLContext` for the context (`mlContext`), and a <xref:System.String> for the dataset path (`dataPath`).</span></span> <span data-ttu-id="3e49f-224">Vous allez utiliser cette méthode plusieurs fois pour l’apprentissage et le test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-224">You're going to use this method more than once for training and testing.</span></span>

## <a name="load-the-data"></a><span data-ttu-id="3e49f-225">Charger les données</span><span class="sxs-lookup"><span data-stu-id="3e49f-225">Load the data</span></span>

<span data-ttu-id="3e49f-226">Vous allez charger les données en utilisant la variable globale `_textLoader` et le paramètre `dataPath`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-226">You'll load the data using the `_textLoader` global variable with the `dataPath` parameter.</span></span> <span data-ttu-id="3e49f-227">Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>.</span><span class="sxs-lookup"><span data-stu-id="3e49f-227">It returns a <xref:Microsoft.Data.DataView.IDataView>.</span></span> <span data-ttu-id="3e49f-228">En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-228">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="3e49f-229">Dans ML.NET, les données sont semblables à une vue SQL.</span><span class="sxs-lookup"><span data-stu-id="3e49f-229">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="3e49f-230">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="3e49f-230">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="3e49f-231">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-231">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="3e49f-232">Pour ce tutoriel, il charge un jeu de données avec des commentaires et les sentiments positifs ou négatifs correspondants.</span><span class="sxs-lookup"><span data-stu-id="3e49f-232">For this tutorial, it loads a dataset with comments and corresponding toxic or non toxic sentiment.</span></span> <span data-ttu-id="3e49f-233">Cette méthode permet de créer puis de former le modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-233">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="3e49f-234">Ajoutez le code suivant comme première ligne de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-234">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#6 "loading training dataset")]

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="3e49f-235">Extraire et transformer les données</span><span class="sxs-lookup"><span data-stu-id="3e49f-235">Extract and transform the data</span></span>

<span data-ttu-id="3e49f-236">Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="3e49f-236">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="3e49f-237">Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="3e49f-237">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="3e49f-238">L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.</span><span class="sxs-lookup"><span data-stu-id="3e49f-238">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="3e49f-239">Les pipelines de transformation ML.NET composent un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-239">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="3e49f-240">Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-240">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="3e49f-241">Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="3e49f-241">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="3e49f-242">Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).</span><span class="sxs-lookup"><span data-stu-id="3e49f-242">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="3e49f-243">Appliquez un pipeline `mlContext.Transforms.Text.FeaturizeText` pour convertir la colonne `SentimentText` en un vecteur numérique appelé `Features` utilisé par l’algorithme Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="3e49f-243">Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text column (`SentimentText`) column into a numeric vector called `Features` used by the machine learning algorithm.</span></span> <span data-ttu-id="3e49f-244">Il s’agit d’un appel de wrapper qui retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera un pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e49f-244">This is a wrapper call that returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="3e49f-245">Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-245">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="3e49f-246">Ajoutez le contenu suivant comme prochaine ligne de code :</span><span class="sxs-lookup"><span data-stu-id="3e49f-246">Add this as the next line of code:</span></span>

[!code-csharp[TextFeaturizingEstimator](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#7 "Add a TextFeaturizingEstimator")]

<span data-ttu-id="3e49f-247">Il s’agit de l’étape de prétraitement/fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-247">This is the preprocessing/featurization step.</span></span> <span data-ttu-id="3e49f-248">L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="3e49f-248">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="3e49f-249">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="3e49f-249">Choose a learning algorithm</span></span>

<span data-ttu-id="3e49f-250">Pour ajouter le formateur, appelez la méthode de wrapper `mlContext.Transforms.Text.FeaturizeText` qui retourne un objet <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer>.</span><span class="sxs-lookup"><span data-stu-id="3e49f-250">To add the trainer, call the `mlContext.Transforms.Text.FeaturizeText` wrapper method which returns a <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer> object.</span></span> <span data-ttu-id="3e49f-251">Il s’agit d’un apprenant d’arbre de décision que vous utiliserez dans ce pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e49f-251">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="3e49f-252">L’objet `FastTreeBinaryClassificationTrainer` est ajouté à `pipeline` et accepte les caractéristiques `SentimentText` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir de l’historique des données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-252">The `FastTreeBinaryClassificationTrainer` is appended to the `pipeline` and accepts the featurized `SentimentText` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="3e49f-253">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-253">Add the following code to the `Train` method:</span></span>

[!code-csharp[FastTreeBinaryClassificationTrainer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#8 "Add a FastTreeBinaryClassificationTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="3e49f-254">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-254">Train the model</span></span>

<span data-ttu-id="3e49f-255">Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="3e49f-255">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="3e49f-256">Une fois l’estimation définie, vous formez votre modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit*> tout en fournissant les données d’apprentissage déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="3e49f-256">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit*> while providing the already loaded training data.</span></span> <span data-ttu-id="3e49f-257">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="3e49f-257">This returns a model to use for predictions.</span></span> <span data-ttu-id="3e49f-258">`pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="3e49f-258">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="3e49f-259">L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="3e49f-259">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="3e49f-260">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-260">Add the following code to the `Train` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#9 "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="3e49f-261">Enregistrer et revenir au modèle formé à utiliser pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="3e49f-261">Save and Return the model trained to use for evaluation</span></span>

<span data-ttu-id="3e49f-262">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="3e49f-262">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="3e49f-263">Retournez le modèle à la fin de la méthode `Train`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-263">Return the model at the end of the `Train` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#10 "Return the model")]

## <a name="evaluate-the-model"></a><span data-ttu-id="3e49f-264">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-264">Evaluate the model</span></span>

<span data-ttu-id="3e49f-265">Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-265">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="3e49f-266">Dans la méthode `Evaluate`, le modèle créé dans `Train` est passé pour évaluation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-266">In the `Evaluate` method, the model created in `Train` is passed in to be evaluated.</span></span> <span data-ttu-id="3e49f-267">Créez la méthode `Evaluate` juste après `Train`, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-267">Create the `Evaluate` method, just after `Train`, as in the following code:</span></span>

```csharp
public static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="3e49f-268">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-268">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="3e49f-269">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-269">Loads the test dataset.</span></span>
* <span data-ttu-id="3e49f-270">Crée l’évaluateur binaire.</span><span class="sxs-lookup"><span data-stu-id="3e49f-270">Creates the binary evaluator.</span></span>
* <span data-ttu-id="3e49f-271">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="3e49f-271">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="3e49f-272">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="3e49f-272">Displays the metrics.</span></span>

<span data-ttu-id="3e49f-273">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-273">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#11 "Call the Evaluate method")]

<span data-ttu-id="3e49f-274">Vous allez charger le jeu de données de test à l’aide de la variable globale `_textLoader` précédemment initialisée avec le champ global `_testDataPath`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-274">You'll load the test dataset using the previously initialized  `_textLoader` global variable with the `_testDataPath` global field.</span></span> <span data-ttu-id="3e49f-275">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="3e49f-275">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="3e49f-276">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-276">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#12 "Load the test dataset")]

<span data-ttu-id="3e49f-277">Vous allez ensuite utiliser le paramètre Machine Learning `model` (un transformateur) pour saisir les fonctionnalités et retourner des prédictions.</span><span class="sxs-lookup"><span data-stu-id="3e49f-277">Next, you'll use the machine learning `model` parameter (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="3e49f-278">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-278">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#13 "Predict using the Transformer")]

<span data-ttu-id="3e49f-279">La méthode `BinaryClassificationContext.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e49f-279">The `BinaryClassificationContext.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="3e49f-280">Elle renvoie un objet `BinaryClassificationEvaluator.CalibratedResult` contenant les métriques globales calculées par les évaluateurs de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="3e49f-280">It returns a `BinaryClassificationEvaluator.CalibratedResult` object contains the overall metrics computed by binary classification evaluators.</span></span> <span data-ttu-id="3e49f-281">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="3e49f-281">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="3e49f-282">Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-282">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#14 "Compute Metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="3e49f-283">Affichage des métriques pour la validation du modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-283">Displaying the metrics for model validation</span></span>

<span data-ttu-id="3e49f-284">Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :</span><span class="sxs-lookup"><span data-stu-id="3e49f-284">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#15 "Display selected metrics")]

<span data-ttu-id="3e49f-285">Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-285">To save your model to a .zip file before returning, add the following code to call the `SaveModelAsFile` method as the next line in `Evaluate`:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#23 "Save the model")]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="3e49f-286">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="3e49f-286">Save the model as a.zip file</span></span>

<span data-ttu-id="3e49f-287">Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-287">Create the `SaveModelAsFile` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="3e49f-288">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-288">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="3e49f-289">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="3e49f-289">Saves the model as a .zip file.</span></span>

<span data-ttu-id="3e49f-290">Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="3e49f-290">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="3e49f-291">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="3e49f-291">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="3e49f-292">Pour l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-292">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="3e49f-293">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-293">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#24 "Add the SaveTo Method")]
<span data-ttu-id="3e49f-294">Déployer et prédire avec un modèle chargé Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-294">Deploy and Predict with a loaded model You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="3e49f-295">Prédire le résultat des données de test avec le modèle enregistré</span><span class="sxs-lookup"><span data-stu-id="3e49f-295">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="3e49f-296">Créez la méthode `Predict` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-296">Create the `Predict` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void Predict(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="3e49f-297">La méthode `Predict` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-297">The `Predict` method executes the following tasks:</span></span>

* <span data-ttu-id="3e49f-298">Crée un commentaire unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-298">Creates a single comment of test data.</span></span>
* <span data-ttu-id="3e49f-299">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-299">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="3e49f-300">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="3e49f-300">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="3e49f-301">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="3e49f-301">Displays the predicted results.</span></span>

<span data-ttu-id="3e49f-302">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-302">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#16 "Call the Predict method")]

<span data-ttu-id="3e49f-303">Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels.</span><span class="sxs-lookup"><span data-stu-id="3e49f-303">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="3e49f-304">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="3e49f-304">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="3e49f-305">Nous allons ajouter le code suivant pour créer le `PredictionEngine` comme première ligne dans la méthode `Predict` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-305">Let's add the following code to create the `PredictionEngine` as the first line in the `Predict` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#17 "Create the PredictionEngine")]
  
<span data-ttu-id="3e49f-306">Ajoutez un commentaire pour tester la prédiction du modèle formé dans la méthode `Predict` en créant une instance de `SentimentData` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-306">Add a comment to test the trained model's prediction in the `Predict` method by creating an instance of `SentimentData`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#18 "Create test data for single prediction")]

 <span data-ttu-id="3e49f-307">Vous pouvez l’utiliser pour prédire le sentiment positif ou négatif d’une instance unique de données de commentaires.</span><span class="sxs-lookup"><span data-stu-id="3e49f-307">You can use that to predict the Toxic or Non Toxic sentiment of a single instance of the comment data.</span></span> <span data-ttu-id="3e49f-308">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-308">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="3e49f-309">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-309">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="3e49f-310">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="3e49f-310">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="3e49f-311">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="3e49f-311">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#19 "Create a prediction of sentiment")]

### <a name="using-the-model-prediction"></a><span data-ttu-id="3e49f-312">Utilisation du modèle : prédiction</span><span class="sxs-lookup"><span data-stu-id="3e49f-312">Using the model: prediction</span></span>

<span data-ttu-id="3e49f-313">Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="3e49f-313">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="3e49f-314">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="3e49f-314">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="3e49f-315">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-315">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#20 "Display prediction output")]

## <a name="deploy-and-predict-with-a-loaded-model"></a><span data-ttu-id="3e49f-316">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="3e49f-316">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="3e49f-317">Créez la méthode `PredictWithModelLoadedFromFile` juste avant la méthode `SaveModelAsFile`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-317">Create the `PredictWithModelLoadedFromFile` method, just before the `SaveModelAsFile` method, using the following code:</span></span>

```csharp
public static void PredictWithModelLoadedFromFile(MLContext mlContext)
{

}
```

<span data-ttu-id="3e49f-318">La méthode `PredictWithModelLoadedFromFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e49f-318">The `PredictWithModelLoadedFromFile` method executes the following tasks:</span></span>

* <span data-ttu-id="3e49f-319">Crée les données de test par lots.</span><span class="sxs-lookup"><span data-stu-id="3e49f-319">Creates batch test data.</span></span>
* <span data-ttu-id="3e49f-320">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="3e49f-320">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="3e49f-321">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="3e49f-321">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="3e49f-322">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="3e49f-322">Displays the predicted results.</span></span>

<span data-ttu-id="3e49f-323">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Predict`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-323">Add a call to the new method from the `Main` method, right under the `Predict` method call, using the following code:</span></span>

[!code-csharp[CallPredictModelLoaded](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#25 "Call the PredictWithModelLoadedFromFile method")]

<span data-ttu-id="3e49f-324">Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `PredictWithModelLoadedFromFile` :</span><span class="sxs-lookup"><span data-stu-id="3e49f-324">Add some comments to test the trained model's predictions in the `PredictWithModelLoadedFromFile` method:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#26 "Create test data for predictions")]

<span data-ttu-id="3e49f-325">Charger le modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-325">Load the model</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#27 "Load the model")]

<span data-ttu-id="3e49f-326">Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.Core.Data.ITransformer.Transform%2A>.</span><span class="sxs-lookup"><span data-stu-id="3e49f-326">Now that you have a model, you can use that to predict the Toxic or Non Toxic sentiment of the comment data using the <xref:Microsoft.ML.Core.Data.ITransformer.Transform%2A> method.</span></span> <span data-ttu-id="3e49f-327">Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="3e49f-327">To get a prediction, use `Predict` on new data.</span></span> <span data-ttu-id="3e49f-328">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="3e49f-328">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="3e49f-329">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="3e49f-329">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="3e49f-330">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="3e49f-330">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="3e49f-331">Ajoutez le code suivant à la méthode `PredictWithModelLoadedFromFile` pour les prédictions :</span><span class="sxs-lookup"><span data-stu-id="3e49f-331">Add the following code to the `PredictWithModelLoadedFromFile` method for the predictions:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#28 "Create predictions of sentiments")]

### <a name="using-the-loaded-model-for-prediction"></a><span data-ttu-id="3e49f-332">Utilisation du modèle chargé pour la prédiction</span><span class="sxs-lookup"><span data-stu-id="3e49f-332">Using the loaded model for prediction</span></span>

<span data-ttu-id="3e49f-333">Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="3e49f-333">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="3e49f-334">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="3e49f-334">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="3e49f-335">Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-335">Create a header for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#29 "Display prediction outputs")]

<span data-ttu-id="3e49f-336">Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit.</span><span class="sxs-lookup"><span data-stu-id="3e49f-336">Before displaying the predicted results, combine the sentiment and prediction together to see the original comment with its predicted sentiment.</span></span> <span data-ttu-id="3e49f-337">Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3e49f-337">The following code uses the <xref:System.Linq.Enumerable.Zip%2A> method to make that happen, so add that code next:</span></span>

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#30 "Build the pairs of sentiment data and predictions")]

<span data-ttu-id="3e49f-338">Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :</span><span class="sxs-lookup"><span data-stu-id="3e49f-338">Now that you've combined the `SentimentText` and `Sentiment` into a class, you can display the results using the <xref:System.Console.WriteLine?displayProperty=nameWithType> method:</span></span>

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#31 "Display the predictions")]

<span data-ttu-id="3e49f-339">Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3e49f-339">Because inferred tuple element names are a new feature in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span>
<span data-ttu-id="3e49f-340">Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-340">To do that, right-click on the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="3e49f-341">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-341">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="3e49f-342">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="3e49f-342">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="3e49f-343">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e49f-343">Select the **OK** button.</span></span>

## <a name="results"></a><span data-ttu-id="3e49f-344">Résultats</span><span class="sxs-lookup"><span data-stu-id="3e49f-344">Results</span></span>

<span data-ttu-id="3e49f-345">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="3e49f-345">Your results should be similar to the following.</span></span> <span data-ttu-id="3e49f-346">Lors du traitement, le pipeline affiche des messages.</span><span class="sxs-lookup"><span data-stu-id="3e49f-346">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="3e49f-347">Vous pouvez voir des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="3e49f-347">You may see warnings, or processing messages.</span></span> <span data-ttu-id="3e49f-348">Ils ont été supprimés des résultats ci-dessous par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="3e49f-348">These have been removed from the following results for clarity.</span></span>

```console
Model quality metrics evaluation
--------------------------------
Accuracy: 94.44%
Auc: 98.77%
F1Score: 94.74%
=============== End of model evaluation ===============

=============== Prediction Test of model with a single sample and test dataset ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.5297049
=============== End of Predictions ===============

=============== New iteration of Model ===============
=============== Create and Train the Model ===============
=============== End of training ===============


The model is saved to: C:\Tutorial\SentimentAnalysis\bin\Debug\netcoreapp2.1\Data\Model.zip

=============== Prediction Test of loaded model with a multiple sample ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.4585565
Sentiment: I love this article. | Prediction: Not Toxic | Probability: 0.09454837

```

<span data-ttu-id="3e49f-349">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="3e49f-349">Congratulations!</span></span> <span data-ttu-id="3e49f-350">Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction des sentiments de messages.</span><span class="sxs-lookup"><span data-stu-id="3e49f-350">You've now successfully built a machine learning model for classifying and predicting messages sentiment.</span></span> <span data-ttu-id="3e49f-351">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).</span><span class="sxs-lookup"><span data-stu-id="3e49f-351">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3e49f-352">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3e49f-352">Next steps</span></span>

<span data-ttu-id="3e49f-353">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="3e49f-353">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="3e49f-354">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="3e49f-354">Understand the problem</span></span>
> * <span data-ttu-id="3e49f-355">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="3e49f-355">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="3e49f-356">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="3e49f-356">Prepare your data</span></span>
> * <span data-ttu-id="3e49f-357">Transformer les données</span><span class="sxs-lookup"><span data-stu-id="3e49f-357">Transform the data</span></span>
> * <span data-ttu-id="3e49f-358">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-358">Train the model</span></span>
> * <span data-ttu-id="3e49f-359">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="3e49f-359">Evaluate the model</span></span>
> * <span data-ttu-id="3e49f-360">Prédire avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="3e49f-360">Predict with the trained model</span></span>
> * <span data-ttu-id="3e49f-361">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="3e49f-361">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="3e49f-362">Passer au tutoriel suivant pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="3e49f-362">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="3e49f-363">Classification des problèmes</span><span class="sxs-lookup"><span data-stu-id="3e49f-363">Issue Classification</span></span>](github-issue-classification.md)
