---
title: Utiliser ML.NET dans un scénario de classification multiclasse de problèmes GitHub
description: Découvrez comment utiliser ML.NET dans un scénario de classification multiclasse pour classer des problèmes GitHub et les affecter à une zone donnée.
ms.date: 02/01/2019
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 79c0ae1ba38b410c0709659a4e5ee1ac2308b983
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55739421"
---
# <a name="tutorial-use-mlnet-in-a-multiclass-classification-scenario-to-classify-github-issues"></a><span data-ttu-id="b43b3-103">Tutoriel : Utiliser ML.NET dans un scénario de classification multiclasse pour classifier les problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="b43b3-103">Tutorial: Use ML.NET in a multiclass classification scenario to classify GitHub issues</span></span>

<span data-ttu-id="b43b3-104">Ce tutoriel montre comment utiliser ML.NET pour créer dans Visual Studio 2017 une application console .NET Core en C# faisant office de classifieur de problèmes GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-104">This sample tutorial illustrates using ML.NET to create a GitHub issue classifier via a .NET Core console application using C# in Visual Studio 2017.</span></span>

<span data-ttu-id="b43b3-105">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="b43b3-105">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="b43b3-106">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="b43b3-106">Understand the problem</span></span>
> * <span data-ttu-id="b43b3-107">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="b43b3-107">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="b43b3-108">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="b43b3-108">Prepare your data</span></span>
> * <span data-ttu-id="b43b3-109">Extraire des caractéristiques et transformer les données</span><span class="sxs-lookup"><span data-stu-id="b43b3-109">Extract Features and transform the data</span></span>
> * <span data-ttu-id="b43b3-110">Entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-110">Train the model</span></span>
> * <span data-ttu-id="b43b3-111">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="b43b3-111">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="b43b3-112">Prédire une seule instance de résultat de données de test avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="b43b3-112">Predict a single instance of test data outcome with the trained model</span></span>
> * <span data-ttu-id="b43b3-113">Prédire une seule instance de données de test avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="b43b3-113">Predict a single instance of test data with a loaded model</span></span>

> [!NOTE]
> <span data-ttu-id="b43b3-114">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="b43b3-114">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="b43b3-115">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="b43b3-115">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

## <a name="github-issue-sample-overview"></a><span data-ttu-id="b43b3-116">Vue d’ensemble de l’exemple traitant des problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="b43b3-116">GitHub issue sample overview</span></span>

<span data-ttu-id="b43b3-117">L’exemple est une application console qui utilise ML.NET pour entraîner un modèle qui classe et prédit l’étiquette Area d’un problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-117">The sample is a console app that uses ML.NET to train a model that classifies and predicts the Area label for a GitHub issue.</span></span> <span data-ttu-id="b43b3-118">Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité.</span><span class="sxs-lookup"><span data-stu-id="b43b3-118">It also evaluates the model with a second dataset for quality analysis.</span></span> <span data-ttu-id="b43b3-119">Les jeux de données de problèmes proviennent du dépôt GitHub dotnet/corefx.</span><span class="sxs-lookup"><span data-stu-id="b43b3-119">The issue datasets are from the dotnet/corefx GitHub repo.</span></span>

<span data-ttu-id="b43b3-120">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification).</span><span class="sxs-lookup"><span data-stu-id="b43b3-120">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) repository.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b43b3-121">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b43b3-121">Prerequisites</span></span>

* <span data-ttu-id="b43b3-122">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="b43b3-122">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* <span data-ttu-id="b43b3-123">[Fichier de problèmes GitHub séparés par des tabulations (issues_train.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span><span class="sxs-lookup"><span data-stu-id="b43b3-123">The [Github issues tab separated file (issues_train.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).</span></span>
* <span data-ttu-id="b43b3-124">[Fichier de test des problèmes GitHub séparés par des tabulations (issues_test.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span><span class="sxs-lookup"><span data-stu-id="b43b3-124">The [Github issues test tab separated file (issues_test.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).</span></span>

## <a name="machine-learning-workflow"></a><span data-ttu-id="b43b3-125">Flux de travail de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="b43b3-125">Machine learning workflow</span></span>

<span data-ttu-id="b43b3-126">Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="b43b3-126">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="b43b3-127">Les phases du flux de travail sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-127">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="b43b3-128">**Comprendre le problème**</span><span class="sxs-lookup"><span data-stu-id="b43b3-128">**Understand the problem**</span></span>
2. <span data-ttu-id="b43b3-129">**Préparer vos données**</span><span class="sxs-lookup"><span data-stu-id="b43b3-129">**Prepare your data**</span></span>
   * <span data-ttu-id="b43b3-130">**Charger les données**</span><span class="sxs-lookup"><span data-stu-id="b43b3-130">**Load the data**</span></span>
   * <span data-ttu-id="b43b3-131">**Extraire des caractéristiques (transformer vos données)**</span><span class="sxs-lookup"><span data-stu-id="b43b3-131">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="b43b3-132">**Générer et former**</span><span class="sxs-lookup"><span data-stu-id="b43b3-132">**Build and train**</span></span> 
   * <span data-ttu-id="b43b3-133">**Effectuer l’apprentissage du modèle**</span><span class="sxs-lookup"><span data-stu-id="b43b3-133">**Train the model**</span></span>
   * <span data-ttu-id="b43b3-134">**Évaluer le modèle**</span><span class="sxs-lookup"><span data-stu-id="b43b3-134">**Evaluate the model**</span></span>
4. <span data-ttu-id="b43b3-135">**Exécuter**</span><span class="sxs-lookup"><span data-stu-id="b43b3-135">**Run**</span></span>
   * <span data-ttu-id="b43b3-136">**Consommation de modèle**</span><span class="sxs-lookup"><span data-stu-id="b43b3-136">**Model consumption**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="b43b3-137">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="b43b3-137">Understand the problem</span></span>

<span data-ttu-id="b43b3-138">Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-138">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="b43b3-139">La décomposition de la problématique vous permet de prédire et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="b43b3-139">Breaking  down the problem allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="b43b3-140">Dans ce tutoriel, vous devez comprendre à quelle zone les problèmes GitHub entrants appartiennent afin de les étiqueter correctement pour la définition des priorités et la planification.</span><span class="sxs-lookup"><span data-stu-id="b43b3-140">The problem for this tutorial is to understand what area incoming GitHub issues belong to in order to label them correctly for prioritization and scheduling.</span></span>

<span data-ttu-id="b43b3-141">Vous pouvez scinder le problème en différentes parties, à savoir :</span><span class="sxs-lookup"><span data-stu-id="b43b3-141">You can break down the problem to the following parts:</span></span>

* <span data-ttu-id="b43b3-142">Texte de titre du problème</span><span class="sxs-lookup"><span data-stu-id="b43b3-142">the issue title text</span></span>
* <span data-ttu-id="b43b3-143">Texte de description du problème</span><span class="sxs-lookup"><span data-stu-id="b43b3-143">the issue description text</span></span>
* <span data-ttu-id="b43b3-144">Valeur de zone pour les données d’entraînement du modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-144">an area value for the model training data</span></span>
* <span data-ttu-id="b43b3-145">Valeur de zone prédite que vous pouvez évaluer et utiliser opérationnellement</span><span class="sxs-lookup"><span data-stu-id="b43b3-145">a predicted area value that you can evaluate and then use operationally</span></span>

<span data-ttu-id="b43b3-146">Vous devez ensuite **déterminer** la zone, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-146">You then need to **determine** the area, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-algorithm"></a><span data-ttu-id="b43b3-147">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="b43b3-147">Select the appropriate machine learning algorithm</span></span>

<span data-ttu-id="b43b3-148">Pour ce problème, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b43b3-148">With this problem, you know the following facts:</span></span>

<span data-ttu-id="b43b3-149">Données d’entraînement :</span><span class="sxs-lookup"><span data-stu-id="b43b3-149">Training data:</span></span>

<span data-ttu-id="b43b3-150">Les problèmes GitHub peuvent être étiquetés dans plusieurs zones (**Area**), comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="b43b3-150">GitHub issues can be labeled in several areas (**Area**) as in the following examples:</span></span>

* <span data-ttu-id="b43b3-151">area-System.Numerics</span><span class="sxs-lookup"><span data-stu-id="b43b3-151">area-System.Numerics</span></span>
* <span data-ttu-id="b43b3-152">area-System.Xml</span><span class="sxs-lookup"><span data-stu-id="b43b3-152">area-System.Xml</span></span>
* <span data-ttu-id="b43b3-153">area-Infrastructure</span><span class="sxs-lookup"><span data-stu-id="b43b3-153">area-Infrastructure</span></span>
* <span data-ttu-id="b43b3-154">area-System.Linq</span><span class="sxs-lookup"><span data-stu-id="b43b3-154">area-System.Linq</span></span>
* <span data-ttu-id="b43b3-155">area-System.IO</span><span class="sxs-lookup"><span data-stu-id="b43b3-155">area-System.IO</span></span>

<span data-ttu-id="b43b3-156">Prédisez la zone (**Area**) d’un nouveau problème GitHub, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="b43b3-156">Predict the **Area** of a new GitHub Issue such as in the following examples:</span></span>

* <span data-ttu-id="b43b3-157">Contract.Assert et Debug.Assert</span><span class="sxs-lookup"><span data-stu-id="b43b3-157">Contract.Assert vs Debug.Assert</span></span>
* <span data-ttu-id="b43b3-158">Configurer les champs en lecture seule dans System.Xml</span><span class="sxs-lookup"><span data-stu-id="b43b3-158">Make fields readonly in System.Xml</span></span>

<span data-ttu-id="b43b3-159">L’algorithme de machine learning de classification est idéal pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="b43b3-159">The classification machine learning algorithm is best suited for this scenario.</span></span>

### <a name="about-the-classification-learning-algorithm"></a><span data-ttu-id="b43b3-160">À propos de l’algorithme de machine learning de classification</span><span class="sxs-lookup"><span data-stu-id="b43b3-160">About the classification learning algorithm</span></span>

<span data-ttu-id="b43b3-161">La classification est un algorithme de machine learning qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-161">Classification is a machine learning algorithm that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="b43b3-162">Par exemple, vous pouvez utiliser la classification pour :</span><span class="sxs-lookup"><span data-stu-id="b43b3-162">For example, you can use classification to:</span></span>

* <span data-ttu-id="b43b3-163">Identifier un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="b43b3-163">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="b43b3-164">Classer un e-mail comme spam, indésirable ou autorisé.</span><span class="sxs-lookup"><span data-stu-id="b43b3-164">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="b43b3-165">Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.</span><span class="sxs-lookup"><span data-stu-id="b43b3-165">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="b43b3-166">Classer des clients selon leur tendance à répondre à une campagne commerciale.</span><span class="sxs-lookup"><span data-stu-id="b43b3-166">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="b43b3-167">Les cas d’usage de l’algorithme de machine learning de classification sont souvent l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b43b3-167">Classification learning algorithm use cases are frequently one of the following types:</span></span>

* <span data-ttu-id="b43b3-168">Binaire : A ou B.</span><span class="sxs-lookup"><span data-stu-id="b43b3-168">Binary: either A or B.</span></span>
* <span data-ttu-id="b43b3-169">Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-169">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

<span data-ttu-id="b43b3-170">Pour ce type de problème, utilisez un algorithme de machine learning de classification multiclasse, dans la mesure où votre prédiction de catégorie de problème peut appartenir à une catégorie parmi plusieurs possibles (multiclasse) plutôt qu’à une catégorie parmi deux possibles (binaire).</span><span class="sxs-lookup"><span data-stu-id="b43b3-170">For this type of problem, use a Multiclass classification learning algorithm, since your issue category prediction can be one of multiple categories (multiclass) rather than just two (binary).</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="b43b3-171">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="b43b3-171">Create a console application</span></span>

### <a name="create-a-project"></a><span data-ttu-id="b43b3-172">Créer un projet</span><span class="sxs-lookup"><span data-stu-id="b43b3-172">Create a project</span></span>

1. <span data-ttu-id="b43b3-173">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="b43b3-173">Open Visual Studio 2017.</span></span> <span data-ttu-id="b43b3-174">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="b43b3-174">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="b43b3-175">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-175">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="b43b3-176">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-176">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="b43b3-177">Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-177">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="b43b3-178">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="b43b3-178">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="b43b3-179">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-179">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="b43b3-180">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="b43b3-180">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="b43b3-181">Créez un répertoire nommé *Models* dans votre projet pour enregistrer votre modèle :</span><span class="sxs-lookup"><span data-stu-id="b43b3-181">Create a directory named *Models* in your project to save your model:</span></span>

    <span data-ttu-id="b43b3-182">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-182">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="b43b3-183">Tapez « Models » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="b43b3-183">Type "Models" and hit Enter.</span></span>

4. <span data-ttu-id="b43b3-184">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="b43b3-184">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="b43b3-185">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-185">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="b43b3-186">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-186">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="b43b3-187">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="b43b3-187">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="b43b3-188">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="b43b3-188">Prepare your data</span></span>

1. <span data-ttu-id="b43b3-189">Téléchargez les jeux de données [issues_train.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) et [issues_test.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="b43b3-189">Download the [issues_train.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) and the [issues_test.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="b43b3-190">Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-190">The first dataset trains the machine learning model and the second can be used to evaluate how accurate your model is.</span></span>

2. <span data-ttu-id="b43b3-191">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-191">In Solution Explorer, right-click each of the \*.tsv files and select **Properties**.</span></span> <span data-ttu-id="b43b3-192">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-192">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="b43b3-193">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="b43b3-193">Create classes and define paths</span></span>

<span data-ttu-id="b43b3-194">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="b43b3-194">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddUsings)]

<span data-ttu-id="b43b3-195">Créez trois champs globaux pour accueillir les chemins des fichiers récemment téléchargés, puis des variables globales pour `MLContext`, `DataView`, `PredictionEngine` et `TextLoader` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-195">Create three global fields to hold the paths to the recently downloaded files, and global variables for the `MLContext`,`DataView`, `PredictionEngine`, and `TextLoader`:</span></span>

* <span data-ttu-id="b43b3-196">`_trainDataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-196">`_trainDataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="b43b3-197">`_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-197">`_testDataPath` has the path to the dataset used to evaluate the model.</span></span>
* <span data-ttu-id="b43b3-198">`_modelPath` contient le chemin d’accès où le modèle formé est enregistré.</span><span class="sxs-lookup"><span data-stu-id="b43b3-198">`_modelPath` has the path where the trained model is saved.</span></span>
* <span data-ttu-id="b43b3-199">`_mlContext` est le <xref:Microsoft.ML.MLContext> qui fournit le contexte de traitement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-199">`_mlContext` is the <xref:Microsoft.ML.MLContext> that provides processing context.</span></span>
* <span data-ttu-id="b43b3-200">`_trainingDataView` est le <xref:Microsoft.ML.Data.IDataView> utilisé pour traiter le jeu de données d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-200">`_trainingDataView` is the <xref:Microsoft.ML.Data.IDataView> used to process the training dataset.</span></span>
* <span data-ttu-id="b43b3-201">`_predEngine` est le <xref:Microsoft.ML.PredictionEngine%602> utilisé pour des prédictions uniques.</span><span class="sxs-lookup"><span data-stu-id="b43b3-201">`_predEngine` is the <xref:Microsoft.ML.PredictionEngine%602> used for single predictions.</span></span>
* <span data-ttu-id="b43b3-202">`_reader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-202">`_reader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="b43b3-203">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins et les autres variables :</span><span class="sxs-lookup"><span data-stu-id="b43b3-203">Add the following code to the line right above the `Main` method to specify those paths and the other variables:</span></span>

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DeclareGlobalVariables)]

<span data-ttu-id="b43b3-204">Créez des classes pour vos données d’entrée et vos prévisions.</span><span class="sxs-lookup"><span data-stu-id="b43b3-204">Create some classes for your input data and predictions.</span></span> <span data-ttu-id="b43b3-205">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="b43b3-205">Add a new class to your project:</span></span>

1. <span data-ttu-id="b43b3-206">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-206">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="b43b3-207">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *GitHubIssueData.cs*.</span><span class="sxs-lookup"><span data-stu-id="b43b3-207">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *GitHubIssueData.cs*.</span></span> <span data-ttu-id="b43b3-208">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-208">Then, select the **Add** button.</span></span>

    <span data-ttu-id="b43b3-209">Le fichier *GitHubIssueData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="b43b3-209">The *GitHubIssueData.cs* file opens in the code editor.</span></span> <span data-ttu-id="b43b3-210">Ajoutez l’instruction `using` suivante en haut de *GitHubIssueData.cs* :</span><span class="sxs-lookup"><span data-stu-id="b43b3-210">Add the following `using` statement to the top of *GitHubIssueData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#AddUsings)]

<span data-ttu-id="b43b3-211">Supprimez la définition de classe existante et ajoutez le code suivant, lequel contient deux classes (`GitHubIssue` et `IssuePrediction`), au fichier *GitHubIssueData.cs* :</span><span class="sxs-lookup"><span data-stu-id="b43b3-211">Remove the existing class definition and add the following code, which has two classes `GitHubIssue` and `IssuePrediction`, to the *GitHubIssueData.cs* file:</span></span>

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#DeclareTypes)]

<span data-ttu-id="b43b3-212">`GitHubIssue`, la classe de jeu de données d’entrée, comprend les champs <xref:System.String> suivants :</span><span class="sxs-lookup"><span data-stu-id="b43b3-212">`GitHubIssue` is the input dataset class and has the following <xref:System.String> fields:</span></span>

* <span data-ttu-id="b43b3-213">`ID` contient une valeur pour l’ID du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-213">`ID` contains a value for the GitHub issue ID</span></span>
* <span data-ttu-id="b43b3-214">`Area` contient une valeur pour l’étiquette `Area`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-214">`Area` contains a value for the `Area` label</span></span>
* <span data-ttu-id="b43b3-215">`Title` contient le titre du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-215">`Title` contains the GitHub issue title</span></span>
* <span data-ttu-id="b43b3-216">`Description` contient la description du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-216">`Description` contains the GitHub issue description</span></span>

<span data-ttu-id="b43b3-217">`IssuePrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="b43b3-217">`IssuePrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="b43b3-218">Il comporte une valeur `string` unique (`Area`) et un attribut `ColumnName` `PredictedLabel`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-218">It has a single `string` (`Area`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="b43b3-219">L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-219">The `Label` is used to create and train the model, and it's also used with a second dataset to evaluate the model.</span></span> <span data-ttu-id="b43b3-220">L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-220">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="b43b3-221">L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-221">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="b43b3-222">Lors de la création d’un modèle avec ML.NET, vous commencez par créer un <xref:Microsoft.ML.MLContext>.</span><span class="sxs-lookup"><span data-stu-id="b43b3-222">When building a model with ML.NET, you start by creating an <xref:Microsoft.ML.MLContext>.</span></span> <span data-ttu-id="b43b3-223">D’un point de vue conceptuel, `MLContext` est comparable à `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="b43b3-223">`MLContext` is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="b43b3-224">L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-224">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="b43b3-225">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="b43b3-225">Initialize variables in Main</span></span>

<span data-ttu-id="b43b3-226">Initialisez la variable globale `_mlContext` à l’aide d’une nouvelle instance de `MLContext` avec une valeur de départ aléatoire (`seed: 0`) pour obtenir des résultats reproductibles/déterministes dans différents entraînements.</span><span class="sxs-lookup"><span data-stu-id="b43b3-226">Initialize the `_mlContext` global variable  with a new instance of `MLContext` with a random seed (`seed: 0`) for repeatable/deterministic results across multiple trainings.</span></span>  <span data-ttu-id="b43b3-227">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-227">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateMLContext)]

## <a name="load-the-data"></a><span data-ttu-id="b43b3-228">Charger les données</span><span class="sxs-lookup"><span data-stu-id="b43b3-228">Load the data</span></span>

<span data-ttu-id="b43b3-229">Ensuite, initialisez la variable globale `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> et chargez les données avec le paramètre `_trainDataPath`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-229">Next, initialize the `_trainingDataView` <xref:Microsoft.ML.Data.IDataView> global variable and load the data with the `_trainDataPath` parameter.</span></span>

 <span data-ttu-id="b43b3-230">En tant qu’entrée et sortie de [`Transforms`](../basic-concepts-model-training-in-mldotnet.md#transformer), `DataView` est le type de pipeline de données fondamental, comparable à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-230">As the input and output of [`Transforms`](../basic-concepts-model-training-in-mldotnet.md#transformer), a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="b43b3-231">Dans ML.NET, les données sont semblables à un `SQL view`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-231">In ML.NET, data is similar to a `SQL view`.</span></span> <span data-ttu-id="b43b3-232">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="b43b3-232">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="b43b3-233">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-233">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="b43b3-234">Pour ce tutoriel, il charge un jeu de données avec les titres et les descriptions des problèmes ainsi que l’étiquette GitHub de la zone correspondante.</span><span class="sxs-lookup"><span data-stu-id="b43b3-234">For this tutorial, it loads a dataset with issue titles, descriptions, and corresponding area GitHub label.</span></span> <span data-ttu-id="b43b3-235">`DataView` est utilisé pour créer et entraîner le modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-235">The `DataView` is used to create and train the model.</span></span>

<span data-ttu-id="b43b3-236">Étant donné que le type de modèle de données `GitHubIssue` créé précédemment correspond au schéma du jeu de données, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données en une seule ligne de code.</span><span class="sxs-lookup"><span data-stu-id="b43b3-236">Since your previously created `GitHubIssue` data model type matches the dataset schema, you can combine the initialization, mapping, and dataset loading into one line of code.</span></span>

<span data-ttu-id="b43b3-237">La première partie de la ligne (`CreateTextReader<GitHubIssue>(hasHeader: true)`) crée un <xref:Microsoft.ML.Data.TextLoader> en déduisant le schéma de jeu de données du type de modèle de données `GitHubIssue` et en utilisant l’en-tête du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-237">The first part of the line (`CreateTextReader<GitHubIssue>(hasHeader: true)`) creates a <xref:Microsoft.ML.Data.TextLoader> by inferring the dataset schema from the `GitHubIssue` data model type and using the dataset header.</span></span>

<span data-ttu-id="b43b3-238">Vous avez défini précédemment le schéma de données quand vous avez créé la classe `GitHubIssue`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-238">You defined the data schema previously when you created the `GitHubIssue` class.</span></span> <span data-ttu-id="b43b3-239">Pour votre schéma :</span><span class="sxs-lookup"><span data-stu-id="b43b3-239">For your schema:</span></span>

* <span data-ttu-id="b43b3-240">La première colonne `ID` est l’ID du problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-240">the first column `ID` (GitHub Issue ID)</span></span>
* <span data-ttu-id="b43b3-241">La deuxième colonne `Area` est la prédiction pour l’entraînement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-241">the second column `Area` (the prediction for training)</span></span>
* <span data-ttu-id="b43b3-242">La troisième colonne `Title` (titre du problème GitHub) est la première [caractéristique](../resources/glossary.md##feature) utilisée pour prédire `Area`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-242">the third column `Title` (GitHub issue title) is the first [feature](../resources/glossary.md##feature)  used for predicting the `Area`</span></span>
* <span data-ttu-id="b43b3-243">La quatrième colonne `Description` est la deuxième caractéristique utilisée pour prédire `Area`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-243">the fourth column  `Description` is the second feature used for predicting the `Area`</span></span>

<span data-ttu-id="b43b3-244">La deuxième partie de la ligne (`.Read(_trainDataPath)`) utilise la méthode <xref:Microsoft.ML.Data.TextLoader.Read%2A> pour charger le fichier texte d’entraînement avec `_trainDataPath` dans la variable globale `IDataView` (`_trainingDataView`).</span><span class="sxs-lookup"><span data-stu-id="b43b3-244">The second part of the line  (`.Read(_trainDataPath)`) uses <xref:Microsoft.ML.Data.TextLoader.Read%2A> method to load the training text file using `_trainDataPath` into the `IDataView` (`_trainingDataView`) global variable.</span></span>  

<span data-ttu-id="b43b3-245">Pour initialiser et charger la variable globale `_trainingDataView` afin de l’utiliser pour le pipeline, ajoutez le code suivant après l’initialisation de `mlContext` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-245">To initialize and load the `_trainingDataView` global variable in order to use it for the pipeline, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTrainData)]


<span data-ttu-id="b43b3-246">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-246">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallProcessData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallProcessData)]

<span data-ttu-id="b43b3-247">La méthode `ProcessData` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-247">The `ProcessData` method executes the following tasks:</span></span>

* <span data-ttu-id="b43b3-248">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-248">Extracts and transforms the data.</span></span>
* <span data-ttu-id="b43b3-249">Retourne le pipeline de traitement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-249">Returns the processing pipeline.</span></span>

<span data-ttu-id="b43b3-250">Créez la méthode `ProcessData` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-250">Create the `ProcessData` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static EstimatorChain<ITransformer> ProcessData()
{

}
```

## <a name="extract-features-and-transform-the-data"></a><span data-ttu-id="b43b3-251">Extraire des caractéristiques et transformer les données</span><span class="sxs-lookup"><span data-stu-id="b43b3-251">Extract Features and transform the data</span></span>

<span data-ttu-id="b43b3-252">Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="b43b3-252">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="b43b3-253">Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="b43b3-253">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="b43b3-254">L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.</span><span class="sxs-lookup"><span data-stu-id="b43b3-254">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="b43b3-255">Les pipelines de transformation ML.NET composent un ensemble `transforms` personnalisé qui s’applique à vos données avant l’entraînement ou le test.</span><span class="sxs-lookup"><span data-stu-id="b43b3-255">ML.NET's transform pipelines compose a custom `transforms`set that is applied to your data before training or testing.</span></span> <span data-ttu-id="b43b3-256">Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-256">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="b43b3-257">Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="b43b3-257">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="b43b3-258">Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).</span><span class="sxs-lookup"><span data-stu-id="b43b3-258">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="b43b3-259">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `GitHubIssue`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-259">In the next steps, we refer to the columns by the names defined in the `GitHubIssue` class.</span></span>

<span data-ttu-id="b43b3-260">Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="b43b3-260">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="b43b3-261">Comme nous voulons prédire l’étiquette GitHub Area pour un `GitHubIssue`, copiez la colonne `Area` dans la colonne **Label**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-261">As we want to predict the Area GitHub label for a `GitHubIssue`, copy the `Area` column into the **Label** column.</span></span> <span data-ttu-id="b43b3-262">Pour ce faire, utilisez `MLContext.Transforms.Conversion.MapValueToKey`, qui est un wrapper pour la classe de transformation <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A>.</span><span class="sxs-lookup"><span data-stu-id="b43b3-262">To do that, use the `MLContext.Transforms.Conversion.MapValueToKey`, which is a wrapper for the <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A> transformation class.</span></span>  <span data-ttu-id="b43b3-263">`MapValueToKey` retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera en fait un pipeline.</span><span class="sxs-lookup"><span data-stu-id="b43b3-263">The `MapValueToKey` returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="b43b3-264">Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-264">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="b43b3-265">Ajoutez la ligne de code suivante :</span><span class="sxs-lookup"><span data-stu-id="b43b3-265">Add the next line of code:</span></span>

[!code-csharp[MapValueToKey](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#MapValueToKey)]

 <span data-ttu-id="b43b3-266">La caractérisation, qui affecte différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, est utilisée par l’algorithme d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-266">Featurizing assigns different numeric key values to the different values in each of the columns and is used by the machine learning algorithm.</span></span> <span data-ttu-id="b43b3-267">Ensuite, appelez `mlContext.Transforms.Text.FeaturizeText` qui caractérise les colonnes de texte (`Title` et `Description`) en vecteur numérique pour chaque `TitleFeaturized` et `DescriptionFeaturized` appelé.</span><span class="sxs-lookup"><span data-stu-id="b43b3-267">Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text (`Title` and `Description`) columns into a numeric vector for each called `TitleFeaturized` and `DescriptionFeaturized`.</span></span> <span data-ttu-id="b43b3-268">Utilisez le code suivant pour ajouter la caractérisation des deux colonnes au pipeline :</span><span class="sxs-lookup"><span data-stu-id="b43b3-268">Append the featurization for both columns to the pipeline with the following code:</span></span>

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#FeaturizeText)]

<span data-ttu-id="b43b3-269">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `Concatenate`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-269">The last step in data preparation combines all of the feature columns into the **Features** column using the `Concatenate` transformation class.</span></span> <span data-ttu-id="b43b3-270">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="b43b3-270">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="b43b3-271">Utilisez le code suivant pour ajouter cette transformation au pipeline :</span><span class="sxs-lookup"><span data-stu-id="b43b3-271">Append this transformation to the pipeline with the following code:</span></span>

[!code-csharp[Concatenate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Concatenate)]

 <span data-ttu-id="b43b3-272">Ajoutez ensuite un <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> pour mettre en cache le DataView. Ainsi, quand vous itérerez plusieurs fois sur les données, l’utilisation du cache vous fera peut-être gagner en performances, à l’instar du code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-272">Next, append a <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> to cache the DataView so when you iterate over the data multiple times using the cache might get better performance, as with the following code:</span></span>

[!code-csharp[AppendCache](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AppendCache)]

<span data-ttu-id="b43b3-273">Retournez le pipeline à la fin de la méthode `ProcessData`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-273">Return the pipeline at the end of the `ProcessData` method.</span></span>

[!code-csharp[ReturnPipeline](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnPipeline)]

<span data-ttu-id="b43b3-274">Cette étape gère le prétraitement/la caractérisation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-274">This step handles preprocessing/featurization.</span></span> <span data-ttu-id="b43b3-275">L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-275">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="build-and-train-the-model"></a><span data-ttu-id="b43b3-276">Générer et entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-276">Build and train the model</span></span>

<span data-ttu-id="b43b3-277">Ajoutez l’appel suivant à la méthode `BuildAndTrainModel` comme prochaine ligne de code dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-277">Add the following call to the `BuildAndTrainModel`method as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallBuildAndTrainModel)]

<span data-ttu-id="b43b3-278">La méthode `BuildAndTrainModel` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-278">The `BuildAndTrainModel` method executes the following tasks:</span></span>

* <span data-ttu-id="b43b3-279">Crée la classe d’algorithme d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-279">Creates the training algorithm class.</span></span>
* <span data-ttu-id="b43b3-280">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-280">Trains the model.</span></span>
* <span data-ttu-id="b43b3-281">Prédit la zone en fonction des données d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-281">Predicts area based on training data.</span></span>
* <span data-ttu-id="b43b3-282">Enregistre le modèle dans un fichier `.zip`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-282">Saves the model to a `.zip` file.</span></span>
* <span data-ttu-id="b43b3-283">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="b43b3-283">Returns the model.</span></span>

<span data-ttu-id="b43b3-284">Créez la méthode `BuildAndTrainModel` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-284">Create the `BuildAndTrainModel` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static EstimatorChain<KeyToValueMappingTransformer> BuildAndTrainModel(IDataView trainingDataView, EstimatorChain<ITransformer> pipeline)
{

}
```

<span data-ttu-id="b43b3-285">Notez que deux paramètres sont passés dans la méthode BuildAndTrainModel : `IDataView` pour le jeu de données d’entraînement (`trainingDataView`) et <xref:Microsoft.ML.Data.EstimatorChain%601> pour le pipeline de traitement créé dans ProcessData (`pipeline`).</span><span class="sxs-lookup"><span data-stu-id="b43b3-285">Notice that two parameters are passed into the BuildAndTrainModel method; an `IDataView` for the training dataset (`trainingDataView`), and a <xref:Microsoft.ML.Data.EstimatorChain%601> for the processing pipeline created in ProcessData (`pipeline`).</span></span>

 <span data-ttu-id="b43b3-286">Ajoutez le code suivant comme première ligne de la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-286">Add the following code as the first line of the `BuildAndTrainModel` method:</span></span>

### <a name="choose-a-learning-algorithm"></a><span data-ttu-id="b43b3-287">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="b43b3-287">Choose a learning algorithm</span></span>

<span data-ttu-id="b43b3-288">Pour ajouter l’algorithme de machine learning, utilisez l’objet <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer>.</span><span class="sxs-lookup"><span data-stu-id="b43b3-288">To add the learning algorithm, use the <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer> object.</span></span>  <span data-ttu-id="b43b3-289">`SdcaMultiClassTrainer` est ajouté à `pipeline` et accepte les caractéristiques `Title` et `Description` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir des données d’historique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-289">The `SdcaMultiClassTrainer` is appended to the `pipeline` and accepts the featurized `Title` and `Description` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="b43b3-290">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-290">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[SdcaMultiClassTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SdcaMultiClassTrainer)]

<span data-ttu-id="b43b3-291">Maintenant que vous avez créé un algorithme de machine learning, ajoutez-le à `pipeline`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-291">Now that you've created a learning algorithm, append it to the `pipeline`.</span></span> <span data-ttu-id="b43b3-292">Vous devez également mapper l’étiquette à la valeur pour revenir à son état lisible d’origine.</span><span class="sxs-lookup"><span data-stu-id="b43b3-292">You also need to map the label to the value to return to its original readable state.</span></span> <span data-ttu-id="b43b3-293">Effectuez ces deux actions avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-293">Do both of those actions with the following code:</span></span>

[!code-csharp[AddTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTrainer)]

### <a name="train-the-model"></a><span data-ttu-id="b43b3-294">Entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-294">Train the model</span></span>

<span data-ttu-id="b43b3-295">Vous entraînez le modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="b43b3-295">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="b43b3-296">Une fois l’estimation définie, vous entraînez votre modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’entraînement déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="b43b3-296">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="b43b3-297">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="b43b3-297">This  method returns a model to use for predictions.</span></span> <span data-ttu-id="b43b3-298">`trainingPipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="b43b3-298">`trainingPipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="b43b3-299">L’expérience n’est pas exécutée tant que la méthode `.Fit()` s’exécute.</span><span class="sxs-lookup"><span data-stu-id="b43b3-299">The experiment is not executed until the `.Fit()` method runs.</span></span>

<span data-ttu-id="b43b3-300">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-300">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#TrainModel)]

<span data-ttu-id="b43b3-301">Bien que `model` soit un `transformer` qui opère sur un grand nombre de lignes de données, le besoin en prédictions sur des exemples individuels est un scénario de production courant.</span><span class="sxs-lookup"><span data-stu-id="b43b3-301">While the `model` is a `transformer` that operates on many rows of data, a need for predictions on individual examples is a common production scenario.</span></span> <span data-ttu-id="b43b3-302">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-302">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="b43b3-303">Ajoutons le code suivant pour créer le `PredictionEngine` comme ligne suivante dans la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-303">Let's add the following code to create the `PredictionEngine` as the next line in the `BuildAndTrainModel` Method:</span></span>

[!code-csharp[CreatePredictionEngine1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine1)]

<span data-ttu-id="b43b3-304">Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-304">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[CreateTestIssue1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateTestIssue1)]

<span data-ttu-id="b43b3-305">Vous pouvez l’utiliser pour prédire l’étiquette `Area` d’une instance unique des données de problème.</span><span class="sxs-lookup"><span data-stu-id="b43b3-305">You can use that to predict the `Area` label of a single instance of the issue data.</span></span> <span data-ttu-id="b43b3-306">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-306">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="b43b3-307">Les données d’entrée représentent une chaîne et le modèle inclut la caractérisation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-307">The input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="b43b3-308">Votre pipeline est synchronisé durant l’entraînement et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="b43b3-308">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="b43b3-309">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-309">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Predict)]

### <a name="using-the-model-prediction"></a><span data-ttu-id="b43b3-310">Utilisation du modèle : prédiction</span><span class="sxs-lookup"><span data-stu-id="b43b3-310">Using the model: prediction</span></span>

<span data-ttu-id="b43b3-311">Affichez `GitHubIssue` et la prédiction d’étiquette `Area` correspondante pour partager les résultats et prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b43b3-311">Display `GitHubIssue` and corresponding `Area` label prediction in order to share the results and act on them accordingly.</span></span>  <span data-ttu-id="b43b3-312">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-312">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#OutputPrediction)]

### <a name="return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="b43b3-313">Retourner le modèle entraîné à utiliser pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="b43b3-313">Return the model trained to use for evaluation</span></span>

<span data-ttu-id="b43b3-314">Retournez le modèle à la fin de la méthode `BuildAndTrainModel`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-314">Return the model at the end of the `BuildAndTrainModel` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnModel)]

## <a name="evaluate-the-model"></a><span data-ttu-id="b43b3-315">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-315">Evaluate the model</span></span>

<span data-ttu-id="b43b3-316">Maintenant que vous avez créé et entraîné le modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-316">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="b43b3-317">Dans la méthode `Evaluate`, le modèle créé dans `BuildAndTrainModel` est passé pour évaluation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-317">In the `Evaluate` method, the model created in `BuildAndTrainModel` is passed in to be evaluated.</span></span> <span data-ttu-id="b43b3-318">Créez la méthode `Evaluate` juste après `BuildAndTrainModel`, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-318">Create the `Evaluate` method, just after `BuildAndTrainModel`, as in the following code:</span></span>

```csharp
public static void Evaluate()
{

}
```

<span data-ttu-id="b43b3-319">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-319">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="b43b3-320">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="b43b3-320">Loads the test dataset.</span></span>
* <span data-ttu-id="b43b3-321">Crée l’évaluateur multiclasse.</span><span class="sxs-lookup"><span data-stu-id="b43b3-321">Creates the multiclass evaluator.</span></span>
* <span data-ttu-id="b43b3-322">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="b43b3-322">Evaluates the model and create metrics.</span></span>
* <span data-ttu-id="b43b3-323">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="b43b3-323">Displays the metrics.</span></span>

<span data-ttu-id="b43b3-324">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `BuildAndTrainModel`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-324">Add a call to the new method from the `Main` method, right under the `BuildAndTrainModel` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallEvaluate)]

<span data-ttu-id="b43b3-325">Comme vous l’avez fait précédemment avec le jeu de données d’entraînement, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données de test en une seule ligne de code.</span><span class="sxs-lookup"><span data-stu-id="b43b3-325">As you did previously with the training dataset, you can combine the initialization, mapping, and test dataset loading into one line of code.</span></span> <span data-ttu-id="b43b3-326">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="b43b3-326">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="b43b3-327">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-327">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTestDataset)]

<span data-ttu-id="b43b3-328">La méthode `MulticlassClassificationContext.Evaluate` est un wrapper pour la méthode <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> qui calcule les métriques de qualité du modèle à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="b43b3-328">The `MulticlassClassificationContext.Evaluate` is a wrapper for the <xref:Microsoft.ML.MulticlassClassificationContext.Evaluate%2A> method that computes the quality metrics for the model using the specified dataset.</span></span> <span data-ttu-id="b43b3-329">Elle retourne un objet <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> contenant les métriques globales calculées par les évaluateurs de classification multiclasse.</span><span class="sxs-lookup"><span data-stu-id="b43b3-329">It returns a <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> object that contains the overall metrics computed by multiclass classification evaluators.</span></span>
<span data-ttu-id="b43b3-330">Pour afficher les métriques permettant de déterminer la qualité du modèle, vous devez d’abord les obtenir.</span><span class="sxs-lookup"><span data-stu-id="b43b3-330">To display the metrics to determine the quality of the model, you need to get them first.</span></span>
<span data-ttu-id="b43b3-331">Notez l’utilisation de la méthode `Transform` de la variable globale `_trainedModel` d’apprentissage automatique (un transformateur) pour entrer les caractéristiques et retourner les prédictions.</span><span class="sxs-lookup"><span data-stu-id="b43b3-331">Notice the use of the `Transform` method of the machine learning `_trainedModel` global variable (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="b43b3-332">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-332">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Evaluate)]

<span data-ttu-id="b43b3-333">Les métriques suivantes sont évaluées pour la classification multiclasse :</span><span class="sxs-lookup"><span data-stu-id="b43b3-333">The following metrics are evaluated for multiclass classification:</span></span>

* <span data-ttu-id="b43b3-334">Micro-précision : chaque paire exemple-classe contribue de manière égale à la métrique de précision.</span><span class="sxs-lookup"><span data-stu-id="b43b3-334">Micro Accuracy - Every sample-class pair contributes equally to the accuracy metric.</span></span>  <span data-ttu-id="b43b3-335">Vous voulez que la micro-précision soit aussi proche de 1 que possible.</span><span class="sxs-lookup"><span data-stu-id="b43b3-335">You want Micro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="b43b3-336">Macro-précision : chaque classe contribue de manière égale à la métrique de précision.</span><span class="sxs-lookup"><span data-stu-id="b43b3-336">Macro Accuracy - Every class contributes equally to the accuracy metric.</span></span> <span data-ttu-id="b43b3-337">Les classes minoritaires sont aussi importantes que les classes plus grandes.</span><span class="sxs-lookup"><span data-stu-id="b43b3-337">Minority classes are given equal weight as the larger classes.</span></span> <span data-ttu-id="b43b3-338">Vous voulez que la macro-précision soit aussi proche de 1 que possible.</span><span class="sxs-lookup"><span data-stu-id="b43b3-338">You want Macro Accuracy to be as close to 1 as possible.</span></span>

* <span data-ttu-id="b43b3-339">Perte logarithmique : consultez [Perte logarithmique](../resources/glossary.md#log-loss).</span><span class="sxs-lookup"><span data-stu-id="b43b3-339">Log-loss - see [Log Loss](../resources/glossary.md#log-loss).</span></span> <span data-ttu-id="b43b3-340">Vous voulez que la perte logarithmique soit aussi proche de zéro que possible.</span><span class="sxs-lookup"><span data-stu-id="b43b3-340">You want Log-loss to be as close to zero as possible.</span></span>

* <span data-ttu-id="b43b3-341">Réduction de la perte logarithmique : comprise entre [-inf, 100], où 100 correspond à des prédictions parfaites et 0 à des prédictions moyennes.</span><span class="sxs-lookup"><span data-stu-id="b43b3-341">Log-loss reduction - Ranges from [-inf, 100], where 100 is perfect predictions and 0 indicates mean predictions.</span></span> <span data-ttu-id="b43b3-342">Vous voulez que la réduction de la perte logarithmique soit aussi proche de zéro que possible.</span><span class="sxs-lookup"><span data-stu-id="b43b3-342">You want Log-loss reduction to be as close to zero as possible.</span></span>

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="b43b3-343">Affichage des métriques pour la validation du modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-343">Displaying the metrics for model validation</span></span>

<span data-ttu-id="b43b3-344">Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :</span><span class="sxs-lookup"><span data-stu-id="b43b3-344">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayMetrics)]

### <a name="save-the-trained-and-evaluated-model"></a><span data-ttu-id="b43b3-345">Enregistrer le modèle entraîné et évalué</span><span class="sxs-lookup"><span data-stu-id="b43b3-345">Save the trained and evaluated model</span></span>

<span data-ttu-id="b43b3-346">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="b43b3-346">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="b43b3-347">Pour enregistrer votre modèle entraîné dans un fichier .zip, ajoutez le code suivant pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-347">To save your trained model to a .zip file, add the following code to call the `SaveModelAsFile` method as the next line in `BuildAndTrainModel`:</span></span>

[!code-csharp[CallSaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallSaveModel)]

## <a name="save-the-model-as-a-zip-file"></a><span data-ttu-id="b43b3-348">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="b43b3-348">Save the model as a .zip file</span></span>

<span data-ttu-id="b43b3-349">Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-349">Create the `SaveModelAsFile` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="b43b3-350">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-350">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="b43b3-351">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="b43b3-351">Saves the model as a .zip file.</span></span>

<span data-ttu-id="b43b3-352">Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="b43b3-352">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="b43b3-353">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="b43b3-353">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="b43b3-354">Pour enregistrer le modèle sous forme de fichier .zip, vous devez créer `FileStream` juste avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="b43b3-354">To save the model as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="b43b3-355">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-355">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SaveModel)]

<span data-ttu-id="b43b3-356">Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-356">You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="b43b3-357">Prédire le résultat des données de test avec le modèle enregistré</span><span class="sxs-lookup"><span data-stu-id="b43b3-357">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="b43b3-358">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-358">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallPredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallPredictIssue)]

<span data-ttu-id="b43b3-359">Créez la méthode `PredictIssue`, juste après la méthode `Evaluate` (et juste avant la méthode `SaveModelAsFile`), en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-359">Create the `PredictIssue` method, just after the `Evaluate` method (and just before the `SaveModelAsFile` method), using the following code:</span></span>

```csharp
private static void PredictIssue()
{

}
```

<span data-ttu-id="b43b3-360">La méthode `PredictIssue` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b43b3-360">The `PredictIssue` method executes the following tasks:</span></span>

* <span data-ttu-id="b43b3-361">Crée un problème unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="b43b3-361">Creates a single issue of test data.</span></span>
* <span data-ttu-id="b43b3-362">Prédit Area en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="b43b3-362">Predicts Area based on test data.</span></span>
* <span data-ttu-id="b43b3-363">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="b43b3-363">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="b43b3-364">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="b43b3-364">Displays the predicted results.</span></span>

<span data-ttu-id="b43b3-365">Tout d’abord, chargez le modèle que vous avez enregistré précédemment avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-365">First, load the model that you saved previously with the following code:</span></span>

[!code-csharp[LoadModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadModel)]

<span data-ttu-id="b43b3-366">Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :</span><span class="sxs-lookup"><span data-stu-id="b43b3-366">Add a GitHub issue to test the trained model's prediction in the `Predict` method by creating an instance of `GitHubIssue`:</span></span>

[!code-csharp[AddTestIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTestIssue)]

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]
  
<span data-ttu-id="b43b3-367">Maintenant que vous avez un modèle, vous pouvez l’utiliser pour prédire l’étiquette GitHub Area d’une instance unique des données de problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-367">Now that you have a model, you can use that to predict the Area GitHub label of a single instance of the GitHub issue data.</span></span> <span data-ttu-id="b43b3-368">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="b43b3-368">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="b43b3-369">Les données d’entrée représentent une chaîne et le modèle inclut la caractérisation.</span><span class="sxs-lookup"><span data-stu-id="b43b3-369">The input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="b43b3-370">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="b43b3-370">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="b43b3-371">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="b43b3-371">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="b43b3-372">Ajoutez le code suivant à la méthode `PredictIssue` pour les prédictions :</span><span class="sxs-lookup"><span data-stu-id="b43b3-372">Add the following code to the `PredictIssue` method for the predictions:</span></span>

[!code-csharp[PredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#PredictIssue)]

### <a name="using-the-loaded-model-for-prediction"></a><span data-ttu-id="b43b3-373">Utilisation du modèle chargé pour la prédiction</span><span class="sxs-lookup"><span data-stu-id="b43b3-373">Using the loaded model for prediction</span></span>

<span data-ttu-id="b43b3-374">Affichez `Area` pour catégoriser le problème et agir en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b43b3-374">Display `Area` in order to categorize the issue and act on it accordingly.</span></span> <span data-ttu-id="b43b3-375">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="b43b3-375">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[DisplayResults](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayResults)]

## <a name="results"></a><span data-ttu-id="b43b3-376">Résultats</span><span class="sxs-lookup"><span data-stu-id="b43b3-376">Results</span></span>

<span data-ttu-id="b43b3-377">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="b43b3-377">Your results should be similar to the following.</span></span> <span data-ttu-id="b43b3-378">Lors du traitement, le pipeline affiche des messages.</span><span class="sxs-lookup"><span data-stu-id="b43b3-378">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="b43b3-379">Vous pouvez voir des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="b43b3-379">You may see warnings, or processing messages.</span></span> <span data-ttu-id="b43b3-380">Ces messages ont été supprimés des résultats suivants par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="b43b3-380">These messages have been removed from the following results for clarity.</span></span>

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

<span data-ttu-id="b43b3-381">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="b43b3-381">Congratulations!</span></span> <span data-ttu-id="b43b3-382">Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction d’une étiquette Area d’un problème GitHub.</span><span class="sxs-lookup"><span data-stu-id="b43b3-382">You've now successfully built a machine learning model for classifying and predicting an Area label for a GitHub issue.</span></span> <span data-ttu-id="b43b3-383">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification).</span><span class="sxs-lookup"><span data-stu-id="b43b3-383">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b43b3-384">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b43b3-384">Next steps</span></span>

<span data-ttu-id="b43b3-385">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="b43b3-385">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="b43b3-386">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="b43b3-386">Understand the problem</span></span>
> * <span data-ttu-id="b43b3-387">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="b43b3-387">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="b43b3-388">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="b43b3-388">Prepare your data</span></span>
> * <span data-ttu-id="b43b3-389">Extraire des caractéristiques et transformer les données</span><span class="sxs-lookup"><span data-stu-id="b43b3-389">Extract Features and transform the data</span></span>
> * <span data-ttu-id="b43b3-390">Entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="b43b3-390">Train the model</span></span>
> * <span data-ttu-id="b43b3-391">Évaluer le modèle avec un autre jeu de données</span><span class="sxs-lookup"><span data-stu-id="b43b3-391">Evaluate the model with a different dataset</span></span>
> * <span data-ttu-id="b43b3-392">Prédire une seule instance de résultat de données de test avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="b43b3-392">Predict a single instance of test data outcome with the trained model</span></span>
> * <span data-ttu-id="b43b3-393">Prédire une seule instance de données de test avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="b43b3-393">Predict a single instance of test data with a loaded model</span></span>

<span data-ttu-id="b43b3-394">Passer au tutoriel suivant pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="b43b3-394">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="b43b3-395">Prédiction du prix d’une course de taxi</span><span class="sxs-lookup"><span data-stu-id="b43b3-395">Taxi Fare Predictor</span></span>](taxi-fare.md)
