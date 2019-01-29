---
title: Utiliser ML.NET dans un scénario de classification multiclasse de problèmes GitHub
description: Découvrez comment utiliser ML.NET dans un scénario de classification multiclasse pour classer des problèmes GitHub et les affecter à une zone donnée.
ms.date: 01/24/2019
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 6f01357906fd4398f68dadfb35dbce816f4302c0
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066205"
---
# <a name="tutorial-use-mlnet-in-a-multiclass-classification-scenario-to-classify-github-issues"></a><span data-ttu-id="784e4-103">Tutoriel : Utilisez ML.NET dans un scénario de classification multiclasse pour classer des problèmes GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-103">Tutorial: Use ML.NET in a multiclass classification scenario to classify GitHub issues.</span></span>

<span data-ttu-id="784e4-104">Ce tutoriel montre comment utiliser ML.NET pour créer dans Visual Studio 2017 une application console .NET Core en C# faisant office de classifieur de problèmes GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-104">This sample tutorial illustrates using ML.NET to create a GitHub issue classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="784e4-105">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="784e4-105">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="784e4-106">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="784e4-106">Understand the problem</span></span>
> * <span data-ttu-id="784e4-107">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="784e4-107">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="784e4-108">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="784e4-108">Prepare your data</span></span>
> * <span data-ttu-id="784e4-109">Créer le pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="784e4-109">Create the learning pipeline</span></span>
> * <span data-ttu-id="784e4-110">Charger un classifieur</span><span class="sxs-lookup"><span data-stu-id="784e4-110">Load a classifier</span></span>
> * <span data-ttu-id="784e4-111">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-111">Train the model</span></span>
> * <span data-ttu-id="784e4-112">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="784e4-112">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="784e4-113">Prédire une seule instance de résultat du test de données avec le modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-113">Predict a single instance of test data outcome with the model</span></span>
> * <span data-ttu-id="784e4-114">Prédire les résultats des données de test avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="784e4-114">Predict the test data outcomes with a loaded model</span></span>

> [!NOTE]
> <span data-ttu-id="784e4-115">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="784e4-115">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="784e4-116">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="784e4-116">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

## <a name="github-issue-sample-overview"></a><span data-ttu-id="784e4-117">Vue d’ensemble de l’exemple traitant des problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="784e4-117">GitHub issue sample overview</span></span>

<span data-ttu-id="784e4-118">L’exemple est une application console qui utilise ML.NET pour entraîner un modèle qui classe et prédit l’étiquette Area d’un problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-118">The sample is a console app that uses ML.NET to train a model that classifies and predicts the Area label for a GitHub issue.</span></span> <span data-ttu-id="784e4-119">Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité.</span><span class="sxs-lookup"><span data-stu-id="784e4-119">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="784e4-120">Les jeux de données de problèmes proviennent du dépôt GitHub dotnet/corefx.</span><span class="sxs-lookup"><span data-stu-id="784e4-120">The issue datasets are from the dotnet/corefx GitHub repo.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="784e4-121">Prérequis</span><span class="sxs-lookup"><span data-stu-id="784e4-121">Prerequisites</span></span>

* <span data-ttu-id="784e4-122">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="784e4-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="784e4-123">[Fichier de problèmes GitHub séparés par des tabulations (issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span><span class="sxs-lookup"><span data-stu-id="784e4-123">The [Github issues tab separated file (issues_train.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span></span>
* <span data-ttu-id="784e4-124">[Fichier de test des problèmes GitHub séparés par des tabulations (issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span><span class="sxs-lookup"><span data-stu-id="784e4-124">The [Github issues test tab separated file (issues_test.tsv)](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="784e4-125">Flux de travail de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="784e4-125">Machine learning workflow</span></span>

<span data-ttu-id="784e4-126">Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="784e4-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="784e4-127">Les phases du flux de travail sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="784e4-128">**Comprendre le problème**</span><span class="sxs-lookup"><span data-stu-id="784e4-128">**Understand the problem**</span></span>
2. <span data-ttu-id="784e4-129">**Préparer vos données**</span><span class="sxs-lookup"><span data-stu-id="784e4-129">**Prepare your data**</span></span>
   * <span data-ttu-id="784e4-130">**Charger les données**</span><span class="sxs-lookup"><span data-stu-id="784e4-130">**Load the data**</span></span>
   * <span data-ttu-id="784e4-131">**Extraire des caractéristiques (transformer vos données)**</span><span class="sxs-lookup"><span data-stu-id="784e4-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="784e4-132">**Générer et former**</span><span class="sxs-lookup"><span data-stu-id="784e4-132">**Build and train**</span></span> 
   * <span data-ttu-id="784e4-133">**Effectuer l’apprentissage du modèle**</span><span class="sxs-lookup"><span data-stu-id="784e4-133">**Train the model**</span></span>
   * <span data-ttu-id="784e4-134">**Évaluer le modèle**</span><span class="sxs-lookup"><span data-stu-id="784e4-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="784e4-135">**Exécuter**</span><span class="sxs-lookup"><span data-stu-id="784e4-135">**Run**</span></span>
   * <span data-ttu-id="784e4-136">**Consommation de modèle**</span><span class="sxs-lookup"><span data-stu-id="784e4-136">**Model consumption**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="784e4-137">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="784e4-137">Understand the problem</span></span>

<span data-ttu-id="784e4-138">Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="784e4-139">La décomposition de la problématique vous permet de prédire et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="784e4-139">Breaking  down the problem allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="784e4-140">Dans ce tutoriel, vous devez comprendre à quelle zone les problèmes GitHub entrants appartiennent afin de les étiqueter correctement pour la définition des priorités et la planification.</span><span class="sxs-lookup"><span data-stu-id="784e4-140">The problem for this tutorial is to understand what area incoming GitHub issues belong to in order to label them correctly for prioritization and scheduling.</span></span>

<span data-ttu-id="784e4-141">Vous pouvez décomposer la problématique comme ceci :</span><span class="sxs-lookup"><span data-stu-id="784e4-141">You can break down the problem to the following:</span></span>

* <span data-ttu-id="784e4-142">Texte de titre du problème</span><span class="sxs-lookup"><span data-stu-id="784e4-142">the issue title text</span></span>
* <span data-ttu-id="784e4-143">Texte de description du problème</span><span class="sxs-lookup"><span data-stu-id="784e4-143">the issue description text</span></span>
* <span data-ttu-id="784e4-144">Valeur de zone pour les données d’entraînement du modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-144">an area value for the model training data</span></span>
* <span data-ttu-id="784e4-145">Valeur de zone prédite que vous pouvez évaluer et utiliser opérationnellement</span><span class="sxs-lookup"><span data-stu-id="784e4-145">a predicted area value that you can evaluate and then use operationally</span></span>

<span data-ttu-id="784e4-146">Vous devez ensuite **déterminer** la zone, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="784e4-146">You then need to **determine** the area, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="784e4-147">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="784e4-147">Select the appropriate machine learning task</span></span>

<span data-ttu-id="784e4-148">Pour ce problème, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="784e4-148">With this problem, you know the following facts:</span></span>

<span data-ttu-id="784e4-149">Données d’entraînement :</span><span class="sxs-lookup"><span data-stu-id="784e4-149">Training data:</span></span>

<span data-ttu-id="784e4-150">Les problèmes GitHub peuvent être étiquetés dans plusieurs zones (**Area**), comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="784e4-150">GitHub issues can be labeled in several areas (**Area**) as in the following examples:</span></span>

* <span data-ttu-id="784e4-151">area-System.Numerics</span><span class="sxs-lookup"><span data-stu-id="784e4-151">area-System.Numerics</span></span>
* <span data-ttu-id="784e4-152">area-System.Xml</span><span class="sxs-lookup"><span data-stu-id="784e4-152">area-System.Xml</span></span>
* <span data-ttu-id="784e4-153">area-Infrastructure</span><span class="sxs-lookup"><span data-stu-id="784e4-153">area-Infrastructure</span></span>
* <span data-ttu-id="784e4-154">area-System.Linq</span><span class="sxs-lookup"><span data-stu-id="784e4-154">area-System.Linq</span></span>
* <span data-ttu-id="784e4-155">area-System.IO</span><span class="sxs-lookup"><span data-stu-id="784e4-155">area-System.IO</span></span>

<span data-ttu-id="784e4-156">Prédisez la zone (**Area**) d’un nouveau problème GitHub, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="784e4-156">Predict the **Area** of a new GitHub Issue such as in the following examples:</span></span>

* <span data-ttu-id="784e4-157">Contract.Assert et Debug.Assert</span><span class="sxs-lookup"><span data-stu-id="784e4-157">Contract.Assert vs Debug.Assert</span></span>
* <span data-ttu-id="784e4-158">Configurer les champs en lecture seule dans System.Xml</span><span class="sxs-lookup"><span data-stu-id="784e4-158">Make fields readonly in System.Xml</span></span>

<span data-ttu-id="784e4-159">La tâche d’apprentissage automatique de classification est idéale pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="784e4-159">The classification machine learning task is best suited for this scenario.</span></span>

### <a name="about-the-classification-task"></a><span data-ttu-id="784e4-160">À propos de la tâche de classification</span><span class="sxs-lookup"><span data-stu-id="784e4-160">About the classification task</span></span>

<span data-ttu-id="784e4-161">La classification est une tâche d’apprentissage automatique qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="784e4-161">Classification is a machine learning task that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="784e4-162">Par exemple, vous pouvez utiliser la classification pour :</span><span class="sxs-lookup"><span data-stu-id="784e4-162">For example, you can use classification to:</span></span>

* <span data-ttu-id="784e4-163">Identifier un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="784e4-163">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="784e4-164">Classer un e-mail comme spam, indésirable ou autorisé.</span><span class="sxs-lookup"><span data-stu-id="784e4-164">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="784e4-165">Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.</span><span class="sxs-lookup"><span data-stu-id="784e4-165">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="784e4-166">Classer des clients selon leur tendance à répondre à une campagne commerciale.</span><span class="sxs-lookup"><span data-stu-id="784e4-166">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="784e4-167">Les tâches de classification sont souvent de ce type :</span><span class="sxs-lookup"><span data-stu-id="784e4-167">Classification tasks are frequently one of the following types:</span></span>

* <span data-ttu-id="784e4-168">Binaire : A ou B.</span><span class="sxs-lookup"><span data-stu-id="784e4-168">Binary: either A or B.</span></span>
* <span data-ttu-id="784e4-169">Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.</span><span class="sxs-lookup"><span data-stu-id="784e4-169">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="784e4-170">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="784e4-170">Create a console application</span></span>

### <a name="create-a-project"></a><span data-ttu-id="784e4-171">Créer un projet</span><span class="sxs-lookup"><span data-stu-id="784e4-171">Create a project</span></span>

1. <span data-ttu-id="784e4-172">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="784e4-172">Open Visual Studio 2017.</span></span> <span data-ttu-id="784e4-173">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="784e4-173">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="784e4-174">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="784e4-174">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="784e4-175">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="784e4-175">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="784e4-176">Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="784e4-176">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="784e4-177">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="784e4-177">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="784e4-178">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="784e4-178">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="784e4-179">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="784e4-179">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="784e4-180">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="784e4-180">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="784e4-181">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="784e4-181">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="784e4-182">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="784e4-182">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="784e4-183">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="784e4-183">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="784e4-184">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="784e4-184">Prepare your data</span></span>

1. <span data-ttu-id="784e4-185">Téléchargez les jeux de données [issues_train.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) et [issues_test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="784e4-185">Download the [issues_train.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) and the [issues_test.tsv](https://github.com/dotnet/samples/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="784e4-186">Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-186">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="784e4-187">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="784e4-187">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="784e4-188">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="784e4-188">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="784e4-189">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="784e4-189">Create classes and define paths</span></span>

<span data-ttu-id="784e4-190">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="784e4-190">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddUsings)]

<span data-ttu-id="784e4-191">Vous devez créer trois champs globaux pour contenir les chemins d’accès aux fichiers récemment téléchargés, et une variable globale pour `TextLoader` :</span><span class="sxs-lookup"><span data-stu-id="784e4-191">You need to create three global fields to hold the paths to the recently downloaded files, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="784e4-192">`_trainDataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-192">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="784e4-193">`_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-193">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="784e4-194">`_modelPath` contient le chemin d’accès où le modèle formé est enregistré.</span><span class="sxs-lookup"><span data-stu-id="784e4-194">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="784e4-195">`_mlContext` est le <xref:Microsoft.ML.MLContext> qui fournit le contexte de traitement.</span><span class="sxs-lookup"><span data-stu-id="784e4-195">`_mlContext` is the <xref:Microsoft.ML.MLContext> that provides processing context.</span></span>
* <span data-ttu-id="784e4-196">`_trainingDataView` est le <xref:Microsoft.ML.Data.IDataView> utilisé pour traiter le jeu de données d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="784e4-196">`_trainingDataView` is the <xref:Microsoft.ML.Data.IDataView> used to process the training dataset.</span></span>
* <span data-ttu-id="784e4-197">`_predEngine` est le <xref:Microsoft.ML.PredictionEngine%602> utilisé pour des prédictions uniques.</span><span class="sxs-lookup"><span data-stu-id="784e4-197">`_predEngine` is the <xref:Microsoft.ML.PredictionEngine%602> used for single predictions.</span></span>
* <span data-ttu-id="784e4-198">`_reader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.</span><span class="sxs-lookup"><span data-stu-id="784e4-198">`_reader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="784e4-199">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins et les autres variables :</span><span class="sxs-lookup"><span data-stu-id="784e4-199">Add the following code to the line right above the `Main` method to specify those paths and the other variables:</span></span>

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DeclareGlobalVariables)]

<span data-ttu-id="784e4-200">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="784e4-200">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="784e4-201">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="784e4-201">Add a new class to your project:</span></span>

1. <span data-ttu-id="784e4-202">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="784e4-202">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="784e4-203">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *GitHubIssueData.cs*.</span><span class="sxs-lookup"><span data-stu-id="784e4-203">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *GitHubIssueData.cs*.</span></span> <span data-ttu-id="784e4-204">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="784e4-204">Then, select the **Add** button.</span></span>

    <span data-ttu-id="784e4-205">Le fichier *GitHubIssueData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="784e4-205">The *GitHubIssueData.cs* file opens in the code editor.</span></span> <span data-ttu-id="784e4-206">Ajoutez l’instruction `using` suivante en haut de *GitHubIssueData.cs* :</span><span class="sxs-lookup"><span data-stu-id="784e4-206">Add the following `using` statement to the top of *GitHubIssueData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#AddUsings)]

<span data-ttu-id="784e4-207">Supprimez la définition de classe existante et ajoutez le code suivant, lequel contient deux classes (`GitHubIssue` et `IssuePrediction`), au fichier *GitHubIssueData.cs* :</span><span class="sxs-lookup"><span data-stu-id="784e4-207">Remove the existing class definition and add the following code, which has two classes `GitHubIssue` and `IssuePrediction`, to the *GitHubIssueData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#DeclareTypes)]

<span data-ttu-id="784e4-208">`GitHubIssue`, la classe de jeu de données d’entrée, comprend les champs <xref:System.String> suivants :</span><span class="sxs-lookup"><span data-stu-id="784e4-208">`GitHubIssue` is the input dataset class and has the following <xref:System.String> fields:</span></span>

* <span data-ttu-id="784e4-209">`ID` contient une valeur pour l’ID du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-209">`ID` contains a value for the GitHub issue ID</span></span>
* <span data-ttu-id="784e4-210">`Area` contient une valeur pour l’étiquette `Area`.</span><span class="sxs-lookup"><span data-stu-id="784e4-210">`Area` contains a value for the `Area` label</span></span>
* <span data-ttu-id="784e4-211">`Title` contient le titre du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-211">`Title` contains the GitHub issue title</span></span>
* <span data-ttu-id="784e4-212">`Description` contient la description du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-212">`Description` contains the GitHub issue description</span></span>

<span data-ttu-id="784e4-213">`IssuePrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="784e4-213">`IssuePrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="784e4-214">Il comporte une valeur `string` unique (`Area`) et un attribut `ColumnName` `PredictedLabel`.</span><span class="sxs-lookup"><span data-stu-id="784e4-214">It has a single `string` (`Area`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="784e4-215">L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-215">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="784e4-216">L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="784e4-216">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="784e4-217">L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-217">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="784e4-218">Lors de la création d’un modèle avec ML.NET, vous commencez par créer un <xref:Microsoft.ML.MLContext>.</span><span class="sxs-lookup"><span data-stu-id="784e4-218">When building a model with ML.NET, you start by creating an <xref:Microsoft.ML.MLContext>.</span></span> <span data-ttu-id="784e4-219">Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="784e4-219">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="784e4-220">L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="784e4-220">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="784e4-221">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="784e4-221">Initialize variables in Main</span></span>

<span data-ttu-id="784e4-222">Initialisez la variable globale `_mlContext` à l’aide d’une nouvelle instance de `MLContext` avec une valeur de départ aléatoire (`seed: 0`) pour obtenir des résultats reproductibles/déterministes dans différents entraînements.</span><span class="sxs-lookup"><span data-stu-id="784e4-222">Initialize the `_mlContext` global variable  with a new instance of `MLContext` with a random seed (`seed: 0`) for repeatable/deterministic results across multiple trainings.</span></span>  <span data-ttu-id="784e4-223">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="784e4-223">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateMLContext)]

## <a name="load-the-data"></a><span data-ttu-id="784e4-224">Charger les données</span><span class="sxs-lookup"><span data-stu-id="784e4-224">Load the data</span></span>

<span data-ttu-id="784e4-225">Ensuite, initialisez la variable globale `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> et chargez les données avec le paramètre `_trainDataPath`.</span><span class="sxs-lookup"><span data-stu-id="784e4-225">Next, initialize the `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> global variable and load the data with the `_trainDataPath` parameter.</span></span>

 <span data-ttu-id="784e4-226">En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="784e4-226">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="784e4-227">Dans ML.NET, les données sont semblables à un `SQL view`.</span><span class="sxs-lookup"><span data-stu-id="784e4-227">In ML.NET, data is similar to a `SQL view`.</span></span> <span data-ttu-id="784e4-228">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="784e4-228">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="784e4-229">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="784e4-229">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="784e4-230">Pour ce tutoriel, il charge un jeu de données avec les titres et les descriptions des problèmes ainsi que l’étiquette GitHub de la zone correspondante.</span><span class="sxs-lookup"><span data-stu-id="784e4-230">For this tutorial, it loads a dataset with issue titles, descriptions, and corresponding area GitHub label.</span></span> <span data-ttu-id="784e4-231">`DataView` est utilisé pour créer et entraîner le modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-231">The `DataView` is used to create and train the model.</span></span>

<span data-ttu-id="784e4-232">Étant donné que le type de modèle de données `GitHubIssue` créé précédemment correspond au schéma du jeu de données, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données en une seule ligne de code.</span><span class="sxs-lookup"><span data-stu-id="784e4-232">Since your previously created `GitHubIssue` data model type matches the dataset schema, you can combine the initialization, mapping, and dataset loading into one line of code.</span></span>

<span data-ttu-id="784e4-233">La première partie de la ligne (`CreateTextReader<GitHubIssue>(hasHeader: true)`) crée un <xref:Microsoft.ML.Data.TextLoader> en déduisant le schéma du jeu de données à partir du type de modèle de données `GitHubIssue` et en utilisant l’en-tête du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="784e4-233">The first part of the line (`CreateTextReader<GitHubIssue>(hasHeader: true)`) creates a <xref:Microsoft.ML.Data.TextLoader> by inferencing the dataset schema from the `GitHubIssue` data model type and using the dataset header.</span></span>

<span data-ttu-id="784e4-234">Vous avez défini précédemment le schéma de données quand vous avez créé la classe `GitHubIssue`.</span><span class="sxs-lookup"><span data-stu-id="784e4-234">You defined the data schema previously when you created the `GitHubIssue` class.</span></span> <span data-ttu-id="784e4-235">Pour votre schéma :</span><span class="sxs-lookup"><span data-stu-id="784e4-235">For your schema:</span></span>

* <span data-ttu-id="784e4-236">La première colonne `ID` est l’ID du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-236">the first column `ID` (GitHub Issue ID)</span></span>
* <span data-ttu-id="784e4-237">La deuxième colonne `Area` est la prédiction pour l’entraînement.</span><span class="sxs-lookup"><span data-stu-id="784e4-237">the second column `Area` (the prediction for training)</span></span>
* <span data-ttu-id="784e4-238">La troisième colonne `Title` (titre du problème GitHub) est la première [caractéristique](../resources/glossary.md##feature) utilisée pour prédire `Area`.</span><span class="sxs-lookup"><span data-stu-id="784e4-238">the third column `Title` (GitHub issue title) is the first [feature](../resources/glossary.md##feature)  used for predicting the `Area`</span></span>
* <span data-ttu-id="784e4-239">La quatrième colonne `Description` est la deuxième caractéristique utilisée pour prédire `Area`.</span><span class="sxs-lookup"><span data-stu-id="784e4-239">the fourth column  `Description` is the second feature used for predicting the `Area`</span></span>

<span data-ttu-id="784e4-240">La deuxième partie de la ligne (`.Read(_trainDataPath)`) utilise la méthode <xref:Microsoft.ML.Data.TextLoader.Read%2A> pour charger le fichier texte d’entraînement avec `_trainDataPath` dans la variable globale `IDataView` (`_trainingDataView`).</span><span class="sxs-lookup"><span data-stu-id="784e4-240">The second part of the line  (`.Read(_trainDataPath)`) uses <xref:Microsoft.ML.Data.TextLoader.Read%2A> method to load the training text file using `_trainDataPath` into the `IDataView` (`_trainingDataView`) global variable.</span></span>  

<span data-ttu-id="784e4-241">Pour initialiser et charger la variable globale `_trainingDataView` afin de l’utiliser pour le pipeline, ajoutez le code suivant après l’initialisation de `mlContext` :</span><span class="sxs-lookup"><span data-stu-id="784e4-241">To initialize and load the `_trainingDataView` global variable in order to use it for the pipeline, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTrainData)]


<span data-ttu-id="784e4-242">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="784e4-242">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallProcessData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallProcessData)]

<span data-ttu-id="784e4-243">La méthode `ProcessData` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-243">The `ProcessData` method executes the following tasks:</span></span>

* <span data-ttu-id="784e4-244">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="784e4-244">Extracts and transforms the data.</span></span>
* <span data-ttu-id="784e4-245">Retourne le pipeline de traitement.</span><span class="sxs-lookup"><span data-stu-id="784e4-245">Returns the processing pipeline.</span></span>

<span data-ttu-id="784e4-246">Créez la méthode `ProcessData` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-246">Create the `ProcessData` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static EstimatorChain<ITransformer> ProcessData()
{

}
```

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="784e4-247">Extraire et transformer les données</span><span class="sxs-lookup"><span data-stu-id="784e4-247">Extract and transform the data</span></span>

<span data-ttu-id="784e4-248">Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="784e4-248">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="784e4-249">Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="784e4-249">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="784e4-250">L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.</span><span class="sxs-lookup"><span data-stu-id="784e4-250">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="784e4-251">Les pipelines de transformation ML.NET composent un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test.</span><span class="sxs-lookup"><span data-stu-id="784e4-251">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="784e4-252">Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données.</span><span class="sxs-lookup"><span data-stu-id="784e4-252">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="784e4-253">Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="784e4-253">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="784e4-254">Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).</span><span class="sxs-lookup"><span data-stu-id="784e4-254">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="784e4-255">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `GitHubIssue`.</span><span class="sxs-lookup"><span data-stu-id="784e4-255">In the next steps, we refer to the columns by the names defined in the `GitHubIssue` class.</span></span>

<span data-ttu-id="784e4-256">Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="784e4-256">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="784e4-257">Comme nous voulons prédire l’étiquette GitHub Area pour un `GitHubIssue`, copiez la colonne `Area` dans la colonne **Label**.</span><span class="sxs-lookup"><span data-stu-id="784e4-257">As we want to predict the Area GitHub label for a `GitHubIssue`, copy the `Area` column into the **Label** column.</span></span> <span data-ttu-id="784e4-258">Pour ce faire, utilisez `MLContext.Transforms.Conversion.MapValueToKey`, qui est un wrapper pour la classe de transformation <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A>.</span><span class="sxs-lookup"><span data-stu-id="784e4-258">To do that, use the `MLContext.Transforms.Conversion.MapValueToKey`, which is a wrapper for the <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> transformation class.</span></span>  <span data-ttu-id="784e4-259">`MapValueToKey` retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera en fait un pipeline.</span><span class="sxs-lookup"><span data-stu-id="784e4-259">The `MapValueToKey` returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="784e4-260">Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`.</span><span class="sxs-lookup"><span data-stu-id="784e4-260">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="784e4-261">Ajoutez le contenu suivant comme prochaine ligne de code :</span><span class="sxs-lookup"><span data-stu-id="784e4-261">Add this as the next line of code:</span></span>

[!code-csharp[MapValueToKey](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#MapValueToKey)]

<span data-ttu-id="784e4-262">L’algorithme qui entraîne le modèle nécessite des caractéristiques **numériques**. Vous devez donc appeler `mlContext.Transforms.Text.FeaturizeText`, qui caractérise les colonnes texte (`Title` et `Description`) en vecteur numérique pour chaque `TitleFeaturized` et `DescriptionFeaturized` appelé.</span><span class="sxs-lookup"><span data-stu-id="784e4-262">The algorithm that trains the model requires **numeric** features, so you have Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text (`Title` and `Description`) columns into a numeric vector for each called `TitleFeaturized` and `DescriptionFeaturized`.</span></span> <span data-ttu-id="784e4-263">La caractérisation, qui affecte différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, est utilisée par l’algorithme d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="784e4-263">Featurizing assigns different numeric key values to the different values in each of the columns and is used by the machine learning algorithm.</span></span>
<span data-ttu-id="784e4-264">Utilisez le code suivant pour ajouter la caractérisation des deux colonnes au pipeline :</span><span class="sxs-lookup"><span data-stu-id="784e4-264">Append the featurization for both columns to the pipeline with the following code:</span></span>

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#FeaturizeText)]

<span data-ttu-id="784e4-265">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `Concatenate`.</span><span class="sxs-lookup"><span data-stu-id="784e4-265">The last step in data preparation combines all of the feature columns into the **Features** column using the `Concatenate` transformation class.</span></span> <span data-ttu-id="784e4-266">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="784e4-266">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="784e4-267">Utilisez le code suivant pour ajouter cette transformation au pipeline :</span><span class="sxs-lookup"><span data-stu-id="784e4-267">Append this transformation to the pipeline with the following code:</span></span>

[!code-csharp[Concatenate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Concatenate)]

 <span data-ttu-id="784e4-268">Ajoutez ensuite un <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> pour mettre en cache DataView, ce qui peut améliorer les performances quand vous itérez plusieurs fois les données. Le code est le suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-268">Next, append a <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> to cache the DataView so when you iterate over the data multiple times using the cache might get better performance, as with the following code</span></span>

[!code-csharp[AppendCache](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AppendCache)]

<span data-ttu-id="784e4-269">Retournez le pipeline à la fin de la méthode `ProcessData`.</span><span class="sxs-lookup"><span data-stu-id="784e4-269">Return the pipeline at the end of the `ProcessData` method.</span></span>

[!code-csharp[ReturnPipeline](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnPipeline)]

<span data-ttu-id="784e4-270">Cette étape gère le prétraitement/la caractérisation.</span><span class="sxs-lookup"><span data-stu-id="784e4-270">This step handles preprocessing/featurization.</span></span> <span data-ttu-id="784e4-271">L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-271">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="build-and-train-the-model"></a><span data-ttu-id="784e4-272">Générer et entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-272">Build and train the model</span></span>

<span data-ttu-id="784e4-273">Ajoutez l’appel suivant à la méthode `BuildAndTrainModel` comme prochaine ligne de code dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="784e4-273">Add the following call to the `BuildAndTrainModel`method as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallBuildAndTrainModel)]

<span data-ttu-id="784e4-274">La méthode `BuildAndTrainModel` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-274">The `BuildAndTrainModel` method executes the following tasks:</span></span>

* <span data-ttu-id="784e4-275">Crée la classe d’algorithme d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="784e4-275">Creates the training algorithm class.</span></span>
* <span data-ttu-id="784e4-276">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-276">Trains the model.</span></span>
* <span data-ttu-id="784e4-277">Prédit la zone en fonction des données d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="784e4-277">Predicts area based on training data.</span></span>
* <span data-ttu-id="784e4-278">Enregistre le modèle dans un fichier `.zip`.</span><span class="sxs-lookup"><span data-stu-id="784e4-278">Saves the model to a `.zip` file.</span></span>
* <span data-ttu-id="784e4-279">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="784e4-279">Returns the model.</span></span>

<span data-ttu-id="784e4-280">Créez la méthode `BuildAndTrainModel` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-280">Create the `BuildAndTrainModel` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static void BuildAndTrainModel()
{

}
```

<span data-ttu-id="784e4-281">Notez que deux paramètres sont passés dans la méthode BuildAndTrainModel : `IDataView` pour le jeu de données d’entraînement (`trainingDataView`) et <xref:Microsoft.ML.Data.EstimatorChain%601> pour le pipeline de traitement créé dans ProcessData (`pipeline`).</span><span class="sxs-lookup"><span data-stu-id="784e4-281">Notice that two parameters are passed into the BuildAndTrainModel method; an `IDataView` for the training dataset (`trainingDataView`), and a <xref:Microsoft.ML.Data.EstimatorChain%601> for the processing pipeline created in ProcessData (`pipeline`).</span></span>

 <span data-ttu-id="784e4-282">Ajoutez le code suivant comme première ligne de la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="784e4-282">Add the following code as the first line of the `BuildAndTrainModel` method:</span></span>

### <a name="choose-a-trainer-algorithm"></a><span data-ttu-id="784e4-283">Choisir un algorithme entraîneur</span><span class="sxs-lookup"><span data-stu-id="784e4-283">Choose a trainer algorithm</span></span>

<span data-ttu-id="784e4-284">Pour ajouter l’algorithme entraîneur, appelez la méthode de wrapper `mlContext.Transforms.Text.FeaturizeText` qui retourne un objet <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer>.</span><span class="sxs-lookup"><span data-stu-id="784e4-284">To add the trainer algorithm, call the `mlContext.Transforms.Text.FeaturizeText` wrapper method which returns a <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> object.</span></span> <span data-ttu-id="784e4-285">Il s’agit d’un apprenant d’arbre de décision que vous utiliserez dans ce pipeline.</span><span class="sxs-lookup"><span data-stu-id="784e4-285">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="784e4-286">`SdcaMultiClassTrainer` est ajouté à `pipeline` et accepte les caractéristiques `Title` et `Description` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir des données d’historique.</span><span class="sxs-lookup"><span data-stu-id="784e4-286">The `SdcaMultiClassTrainer` is appended to the `pipeline` and accepts the featurized `Title` and `Description` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="784e4-287">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="784e4-287">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[SdcaMultiClassTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SdcaMultiClassTrainer)]

<span data-ttu-id="784e4-288">Maintenant que vous avez créé un algorithme entraîneur, ajoutez-le à `pipeline`.</span><span class="sxs-lookup"><span data-stu-id="784e4-288">Now that you've created a trainer algorithm, append it to the `pipeline`.</span></span> <span data-ttu-id="784e4-289">Vous devez également mapper l’étiquette à la valeur pour revenir à son état lisible d’origine.</span><span class="sxs-lookup"><span data-stu-id="784e4-289">You also need to map the label to the value to return to its original readable state.</span></span> <span data-ttu-id="784e4-290">Effectuez ces deux actions avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-290">Do both of those actions with the following code:</span></span>

[!code-csharp[AddTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTrainer)]

### <a name="train-the-model"></a><span data-ttu-id="784e4-291">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-291">Train the model</span></span>

<span data-ttu-id="784e4-292">Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="784e4-292">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="784e4-293">Une fois l’estimation définie, vous formez votre modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="784e4-293">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="784e4-294">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="784e4-294">This returns a model to use for predictions.</span></span> <span data-ttu-id="784e4-295">`trainingPipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="784e4-295">`trainingPipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="784e4-296">L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="784e4-296">The experiment is not executed until this happens.</span></span>

<span data-ttu-id="784e4-297">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="784e4-297">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#TrainModel)]

<span data-ttu-id="784e4-298">Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels.</span><span class="sxs-lookup"><span data-stu-id="784e4-298">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="784e4-299">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="784e4-299">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="784e4-300">Ajoutons le code suivant pour créer le `PredictionEngine` comme ligne suivante dans la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="784e4-300">Let's add the following code to create the `PredictionEngine` as the next line in the `BuildAndTrainModel` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

<span data-ttu-id="784e4-301">Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :</span><span class="sxs-lookup"><span data-stu-id="784e4-301">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[CreateTestIssue1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateTestIssue1)]

<span data-ttu-id="784e4-302">Vous pouvez l’utiliser pour prédire l’étiquette `Area` d’une instance unique des données de problème.</span><span class="sxs-lookup"><span data-stu-id="784e4-302">You can use that to predict the `Area` label of a single instance of the issue data.</span></span> <span data-ttu-id="784e4-303">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="784e4-303">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="784e4-304">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="784e4-304">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="784e4-305">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="784e4-305">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="784e4-306">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="784e4-306">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Predict)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="784e4-307">Opérationnalisation du modèle : prédiction</span><span class="sxs-lookup"><span data-stu-id="784e4-307">Model operationalization: prediction</span></span>

<span data-ttu-id="784e4-308">Affichez `GitHubIssue` et la prédiction d’étiquette `Area` correspondante pour partager les résultats et prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="784e4-308">Display `GitHubIssue` and corresponding `Area` label prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="784e4-309">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="784e4-309">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="784e4-310">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-310">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#OutputPrediction)]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="784e4-311">Enregistrer et revenir au modèle entraîné à utiliser pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="784e4-311">Save and return the model trained to use for evaluation</span></span>

<span data-ttu-id="784e4-312">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="784e4-312">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="784e4-313">Pour enregistrer votre modèle entraîné dans un fichier .zip, ajoutez le code suivant pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="784e4-313">To save your trained model to a .zip file, add the following code to call the `SaveModelAsFile` method as the next line in `BuildAndTrainModel`:</span></span>

[!code-csharp[CallSaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallSaveModel)]

<span data-ttu-id="784e4-314">Retournez le modèle à la fin de la méthode `BuildAndTrainModel`.</span><span class="sxs-lookup"><span data-stu-id="784e4-314">Return the model at the end of the `BuildAndTrainModel` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnModel)]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="784e4-315">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="784e4-315">Save the model as a.zip file</span></span>

<span data-ttu-id="784e4-316">Créez la méthode `SaveModelAsFile` juste après la méthode `BuildAndTrainModel`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-316">Create the `SaveModelAsFile` method, just after the `BuildAndTrainModel` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="784e4-317">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-317">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="784e4-318">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="784e4-318">Saves the model as a .zip file.</span></span>

<span data-ttu-id="784e4-319">Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="784e4-319">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="784e4-320">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="784e4-320">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="784e4-321">Pour l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="784e4-321">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="784e4-322">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="784e4-322">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SaveModel)]

<span data-ttu-id="784e4-323">Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-323">You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="784e4-324">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-324">Evaluate the model</span></span>

<span data-ttu-id="784e4-325">Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation.</span><span class="sxs-lookup"><span data-stu-id="784e4-325">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="784e4-326">Dans la méthode `Evaluate`, le modèle créé dans `BuildAndTrainModel` est passé pour évaluation.</span><span class="sxs-lookup"><span data-stu-id="784e4-326">In the `Evaluate` method, the model created in `BuildAndTrainModel` is passed in to be evaluated.</span></span> <span data-ttu-id="784e4-327">Créez la méthode `Evaluate` juste après `BuildAndTrainModel`, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-327">Create the `Evaluate` method, just after `BuildAndTrainModel`, as in the following code:</span></span>

```csharp
public static void Evaluate()
{

}
```

<span data-ttu-id="784e4-328">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-328">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="784e4-329">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="784e4-329">Loads the test dataset.</span></span>
* <span data-ttu-id="784e4-330">Crée l’évaluateur multiclasse.</span><span class="sxs-lookup"><span data-stu-id="784e4-330">Creates the multiclass evaluator.</span></span>
* <span data-ttu-id="784e4-331">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="784e4-331">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="784e4-332">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="784e4-332">Displays the metrics.</span></span>

<span data-ttu-id="784e4-333">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `BuildAndTrainModel`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-333">Add a call to the new method from the `Main` method, right under the `BuildAndTrainModel` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallEvaluate)]

<span data-ttu-id="784e4-334">Comme vous l’avez fait précédemment avec le jeu de données d’entraînement, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données de test en une seule ligne de code.</span><span class="sxs-lookup"><span data-stu-id="784e4-334">As you did previously with the training dataset, you can combine the initialization, mapping, and test dataset loading into one line of code.</span></span> <span data-ttu-id="784e4-335">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="784e4-335">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="784e4-336">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="784e4-336">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTestDataset)]

<span data-ttu-id="784e4-337">La méthode `MulticlassClassificationContext.Evaluate` est un wrapper pour la méthode <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> qui calcule les métriques de qualité du modèle à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="784e4-337">The `MulticlassClassificationContext.Evaluate` is a wrapper for the <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> method that computes the quality metrics for the model using the specified dataset.</span></span> <span data-ttu-id="784e4-338">Elle retourne un objet <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> contenant les métriques globales calculées par les évaluateurs de classification multiclasse.</span><span class="sxs-lookup"><span data-stu-id="784e4-338">It returns a <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> object that contains the overall metrics computed by multiclass classification evaluators.</span></span>
<span data-ttu-id="784e4-339">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="784e4-339">To display these to determine the quality of the model, you need to get the metrics first.</span></span>
<span data-ttu-id="784e4-340">Notez l’utilisation de la méthode `Transform` de la variable globale `_trainedModel` d’apprentissage automatique (un transformateur) pour entrer les caractéristiques et retourner les prédictions.</span><span class="sxs-lookup"><span data-stu-id="784e4-340">Notice the use of the `Transform` method of the machine learning `_trainedModel` global variable (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="784e4-341">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="784e4-341">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Evaluate)]

<span data-ttu-id="784e4-342">Les métriques suivantes sont évaluées pour la classification multiclasse :</span><span class="sxs-lookup"><span data-stu-id="784e4-342">The following metrics are evaluated for multiclass classification:</span></span>

* <span data-ttu-id="784e4-343">Micro-précision : chaque paire exemple-classe contribue de manière égale à la métrique de précision.</span><span class="sxs-lookup"><span data-stu-id="784e4-343">Micro Accuracy - Every sample-class pair contributes equally to the accuracy metric.</span></span>  <span data-ttu-id="784e4-344">Vous voulez que la micro-précision soit aussi proche de 1 que possible.</span><span class="sxs-lookup"><span data-stu-id="784e4-344">You want Micro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="784e4-345">Macro-précision : chaque classe contribue de manière égale à la métrique de précision.</span><span class="sxs-lookup"><span data-stu-id="784e4-345">Macro Accuracy - Every class contributes equally to the accuracy metric.</span></span> <span data-ttu-id="784e4-346">Les classes minoritaires sont aussi importantes que les classes plus grandes.</span><span class="sxs-lookup"><span data-stu-id="784e4-346">Minority classes are given equal weight as the larger classes.</span></span> <span data-ttu-id="784e4-347">Vous voulez que la macro-précision soit aussi proche de 1 que possible.</span><span class="sxs-lookup"><span data-stu-id="784e4-347">You want Macro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="784e4-348">Perte logarithmique : consultez [Perte logarithmique](../resources/glossary.md#log-loss).</span><span class="sxs-lookup"><span data-stu-id="784e4-348">Log-loss - see [Log Loss](../resources/glossary.md#log-loss).</span></span> <span data-ttu-id="784e4-349">Vous voulez que la perte logarithmique soit aussi proche de zéro que possible.</span><span class="sxs-lookup"><span data-stu-id="784e4-349">You want Log-loss to be as close to zero as possible.</span></span>

* <span data-ttu-id="784e4-350">Réduction de la perte logarithmique : comprise entre [-inf, 100], où 100 correspond à des prédictions parfaites et 0 à des prédictions moyennes.</span><span class="sxs-lookup"><span data-stu-id="784e4-350">Log-loss reduction - Ranges from [-inf, 100], where 100 is perfect predictions and 0 indicates mean predictions.</span></span> <span data-ttu-id="784e4-351">Vous voulez que la réduction de la perte logarithmique soit aussi proche de zéro que possible.</span><span class="sxs-lookup"><span data-stu-id="784e4-351">You want Log-loss reduction to be as close to zero as possible.</span></span>

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="784e4-352">Affichage des métriques pour la validation du modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-352">Displaying the metrics for model validation</span></span>

<span data-ttu-id="784e4-353">Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :</span><span class="sxs-lookup"><span data-stu-id="784e4-353">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayMetrics)]

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="784e4-354">Prédire le résultat des données de test avec le modèle enregistré</span><span class="sxs-lookup"><span data-stu-id="784e4-354">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="784e4-355">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-355">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallPredictIssue)]

<span data-ttu-id="784e4-356">Créez la méthode `PredictIssue` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-356">Create the `PredictIssue` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void PredictIssue()
{

}
```

<span data-ttu-id="784e4-357">La méthode `PredictIssue` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="784e4-357">The `PredictIssue` method executes the following tasks:</span></span>

* <span data-ttu-id="784e4-358">Crée un problème unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="784e4-358">Creates a single issue of test data.</span></span>
* <span data-ttu-id="784e4-359">Prédit Area en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="784e4-359">Predicts Area based on test data.</span></span>
* <span data-ttu-id="784e4-360">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="784e4-360">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="784e4-361">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="784e4-361">Displays the predicted results.</span></span>

<span data-ttu-id="784e4-362">Tout d’abord, chargez le modèle que vous avez enregistré précédemment avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-362">First, load the model that you saved previously with the following code:</span></span>

[!code-csharp[LoadModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadModel)]

<span data-ttu-id="784e4-363">Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :</span><span class="sxs-lookup"><span data-stu-id="784e4-363">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[AddTestIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTestIssue)]

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]
  
<span data-ttu-id="784e4-364">Maintenant que vous avez un modèle, vous pouvez l’utiliser pour prédire l’étiquette GitHub Area d’une instance unique des données de problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-364">Now that you have a model, you can use that to predict the Area GitHub label of a single instance of the GitHub issue data.</span></span> <span data-ttu-id="784e4-365">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="784e4-365">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="784e4-366">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="784e4-366">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="784e4-367">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="784e4-367">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="784e4-368">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="784e4-368">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="784e4-369">Ajoutez le code suivant à la méthode `PredictIssue` pour les prédictions :</span><span class="sxs-lookup"><span data-stu-id="784e4-369">Add the following code to the `PredictIssue` method for the predictions:</span></span>

[!code-csharp[PredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]

### <a name="model-operationalization-prediction"></a><span data-ttu-id="784e4-370">Opérationnalisation du modèle : prédiction</span><span class="sxs-lookup"><span data-stu-id="784e4-370">Model operationalization: prediction</span></span>

<span data-ttu-id="784e4-371">Affichez `Area` pour catégoriser le problème et agir en conséquence.</span><span class="sxs-lookup"><span data-stu-id="784e4-371">Display `Area` in order to categorize the issue and act on it accordingly.</span></span> <span data-ttu-id="784e4-372">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="784e4-372">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="784e4-373">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="784e4-373">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[DisplayResults](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayResults)]

## <a name="results"></a><span data-ttu-id="784e4-374">Résultats</span><span class="sxs-lookup"><span data-stu-id="784e4-374">Results</span></span>

<span data-ttu-id="784e4-375">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="784e4-375">Your results should be similar to the following.</span></span> <span data-ttu-id="784e4-376">Lors du traitement, le pipeline affiche des messages.</span><span class="sxs-lookup"><span data-stu-id="784e4-376">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="784e4-377">Vous pouvez voir des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="784e4-377">You may see warnings, or processing messages.</span></span> <span data-ttu-id="784e4-378">Ils ont été supprimés des résultats ci-dessous par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="784e4-378">These have been removed from the following results for clarity.</span></span>

```console
=============== Single Prediction just-trained-model - Result: area-System.Net ===============
The model is saved to C:\Users\johalex\dotnet-samples\samples\machine-learning\tutorials\GitHubIssueClassification\bin\Debug\netcoreapp2.0\..\..\..\Models\model.zip
*************************************************************************************************************
*       Metrics for Multi-class Classification model - Test Data
*------------------------------------------------------------------------------------------------------------
*       MicroAccuracy:    0.74
*       MacroAccuracy:    0.687
*       LogLoss:          .932
*       LogLossReduction: 63.852
*************************************************************************************************************
=============== Single Prediction - Result: area-System.Data ===============
```

<span data-ttu-id="784e4-379">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="784e4-379">Congratulations!</span></span> <span data-ttu-id="784e4-380">Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction d’une étiquette Area d’un problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="784e4-380">You've now successfully built a machine learning model for classifying and predicting an Area label for a GitHub issue.</span></span> <span data-ttu-id="784e4-381">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification).</span><span class="sxs-lookup"><span data-stu-id="784e4-381">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="784e4-382">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="784e4-382">Next steps</span></span>

<span data-ttu-id="784e4-383">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="784e4-383">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="784e4-384">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="784e4-384">Understand the problem</span></span>
> * <span data-ttu-id="784e4-385">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="784e4-385">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="784e4-386">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="784e4-386">Prepare your data</span></span>
> * <span data-ttu-id="784e4-387">Créer le pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="784e4-387">Create the learning pipeline</span></span>
> * <span data-ttu-id="784e4-388">Charger un classifieur</span><span class="sxs-lookup"><span data-stu-id="784e4-388">Load a classifier</span></span>
> * <span data-ttu-id="784e4-389">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-389">Train the model</span></span>
> * <span data-ttu-id="784e4-390">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="784e4-390">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="784e4-391">Prédire les résultats des données de test avec le modèle</span><span class="sxs-lookup"><span data-stu-id="784e4-391">Predict the test data outcomes with the model</span></span>

<span data-ttu-id="784e4-392">Passer au tutoriel suivant pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="784e4-392">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="784e4-393">Prédiction du prix d’une course de taxi</span><span class="sxs-lookup"><span data-stu-id="784e4-393">Taxi Fare Predictor</span></span>](taxi-fare.md)
