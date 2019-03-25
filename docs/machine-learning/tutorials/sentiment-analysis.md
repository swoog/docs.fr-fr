---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 03/07/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: a88ed38b76a230095f35304aa2b52af0a7c9c22d
ms.sourcegitcommit: 77854e8704b9689b73103d691db34d71c2bf1dad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "58307939"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a><span data-ttu-id="c8d7e-103">Tutoriel : Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments</span><span class="sxs-lookup"><span data-stu-id="c8d7e-103">Tutorial: Use ML.NET in a sentiment analysis binary classification scenario</span></span>

<span data-ttu-id="c8d7e-104">Cet exemple de tutoriel montre comment utiliser ML.NET pour créer un classifieur de sentiments permettant de prédire un sentiment positif ou négatif dans une application console .NET Core avec C# dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-104">This sample tutorial illustrates using ML.NET to create a sentiment classifier to predict either positive or negative sentiment via a .NET Core console application using C# in Visual Studio 2017.</span></span> <span data-ttu-id="c8d7e-105">Dans le monde du Machine Learning, ce type de prédiction est connu sous le nom de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-105">In the world of machine learning, this type of prediction is known as binary classification.</span></span>

> [!NOTE]
> <span data-ttu-id="c8d7e-106">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-106">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="c8d7e-107">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-107">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="c8d7e-108">Ce tutoriel et l’exemple associé utilisent actuellement **ML.NET version 0.11**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-108">This tutorial and related sample are currently using **ML.NET version 0.11**.</span></span> <span data-ttu-id="c8d7e-109">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-109">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes)</span></span>

<span data-ttu-id="c8d7e-110">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-110">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="c8d7e-111">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="c8d7e-111">Understand the problem</span></span>
> * <span data-ttu-id="c8d7e-112">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="c8d7e-112">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="c8d7e-113">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-113">Prepare your data</span></span>
> * <span data-ttu-id="c8d7e-114">Transformer les données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-114">Transform the data</span></span>
> * <span data-ttu-id="c8d7e-115">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-115">Train the model</span></span>
> * <span data-ttu-id="c8d7e-116">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-116">Evaluate the model</span></span>
> * <span data-ttu-id="c8d7e-117">Prédire avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="c8d7e-117">Predict with the trained model</span></span>
> * <span data-ttu-id="c8d7e-118">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="c8d7e-118">Deploy and Predict with a loaded model</span></span>

## <a name="sentiment-analysis-sample-overview"></a><span data-ttu-id="c8d7e-119">Vue d’ensemble d’un exemple d’analyse des sentiments</span><span class="sxs-lookup"><span data-stu-id="c8d7e-119">Sentiment analysis sample overview</span></span>

<span data-ttu-id="c8d7e-120">L’exemple est une application console qui utilise ML.NET pour effectuer l’apprentissage d’un modèle qui classifie et prédit un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-120">The sample is a console app that uses ML.NET to train a model that classifies and predicts sentiment as either positive or negative.</span></span> <span data-ttu-id="c8d7e-121">Le jeu de données de sentiments Yelp, qui provient de l’université de Californie à Irvine (UCI), se divise en un jeu de données d’apprentissage et un jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-121">The Yelp sentiment dataset is from University of California, Irvine (UCI), which is split into a train dataset and a test dataset.</span></span> <span data-ttu-id="c8d7e-122">L’exemple évalue le modèle avec le jeu de données de test à des fins d’analyse de la qualité.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-122">The sample evaluates the model with the test dataset for quality analysis.</span></span> 

<span data-ttu-id="c8d7e-123">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-123">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8d7e-124">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c8d7e-124">Prerequisites</span></span>

* <span data-ttu-id="c8d7e-125">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-125">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

* [<span data-ttu-id="c8d7e-126">Le fichier zip du jeu de données UCI Sentiment Labeled Sentences</span><span class="sxs-lookup"><span data-stu-id="c8d7e-126">The UCI Sentiment Labeled Sentences dataset zip file</span></span>](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/sentiment%20labelled%20sentences.zip)

## <a name="machine-learning-workflow"></a><span data-ttu-id="c8d7e-127">Flux de travail de l’apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="c8d7e-127">Machine learning workflow</span></span>

<span data-ttu-id="c8d7e-128">Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-128">This tutorial follows a machine learning workflow that enables the process to move in an orderly fashion.</span></span>

<span data-ttu-id="c8d7e-129">Les phases du flux de travail sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-129">The workflow phases are as follows:</span></span>

1. <span data-ttu-id="c8d7e-130">**Comprendre le problème**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-130">**Understand the problem**</span></span>
2. <span data-ttu-id="c8d7e-131">**Préparer vos données**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-131">**Prepare your data**</span></span>
   * <span data-ttu-id="c8d7e-132">**Charger les données**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-132">**Load the data**</span></span>
   * <span data-ttu-id="c8d7e-133">**Extraire des caractéristiques (transformer vos données)**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-133">**Extract features (Transform your data)**</span></span>
3. <span data-ttu-id="c8d7e-134">**Générer et former**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-134">**Build and train**</span></span> 
   * <span data-ttu-id="c8d7e-135">**Effectuer l’apprentissage du modèle**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-135">**Train the model**</span></span>
   * <span data-ttu-id="c8d7e-136">**Évaluer le modèle**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-136">**Evaluate the model**</span></span>
4. <span data-ttu-id="c8d7e-137">**Déployer le modèle**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-137">**Deploy Model**</span></span>
   * <span data-ttu-id="c8d7e-138">**Utiliser le modèle pour prédire**</span><span class="sxs-lookup"><span data-stu-id="c8d7e-138">**Use the Model to predict**</span></span>

### <a name="understand-the-problem"></a><span data-ttu-id="c8d7e-139">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="c8d7e-139">Understand the problem</span></span>

<span data-ttu-id="c8d7e-140">Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-140">You first need to understand the problem, so you can break it down to parts that can support building and training the model.</span></span> <span data-ttu-id="c8d7e-141">La décomposition du problème vous permet de prédire et d’évaluer les résultats.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-141">Breaking the problem down allows you to predict and evaluate the results.</span></span>

<span data-ttu-id="c8d7e-142">Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-142">The problem for this tutorial is to understand incoming website comment sentiment to take the appropriate action.</span></span>

<span data-ttu-id="c8d7e-143">Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-143">You can break down the problem to the sentiment text and sentiment value for the data you want to train the model with, and a predicted sentiment value that you can evaluate and then use operationally.</span></span>

<span data-ttu-id="c8d7e-144">Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-144">You then need to **determine** the sentiment, which helps you with the machine learning task selection.</span></span>

## <a name="select-the-appropriate-machine-learning-algorithm"></a><span data-ttu-id="c8d7e-145">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="c8d7e-145">Select the appropriate machine learning algorithm</span></span>

<span data-ttu-id="c8d7e-146">Pour ce problème, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-146">With this problem, you know the following facts:</span></span>

<span data-ttu-id="c8d7e-147">Données d’apprentissage : les commentaires sur le site web peuvent être positifs (1) ou négatifs (0) (**sentiment**).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-147">Training data: website comments can be positive (1) or negative (0) (**sentiment**).</span></span>

<span data-ttu-id="c8d7e-148">Prédisez le **sentiment** d’un nouveau commentaire sur le site web, positif ou négatif, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-148">Predict the **sentiment** of a new website comment, either positive or negative, such as in the following examples:</span></span>

* <span data-ttu-id="c8d7e-149">J’adore les serveurs de cet endroit.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-149">I love the wait staff here.</span></span> <span data-ttu-id="c8d7e-150">Ils sont super.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-150">They rock.</span></span>
* <span data-ttu-id="c8d7e-151">Je n’ai jamais mangé une soupe aussi mauvaise qu’ici.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-151">This place has the worst soup.</span></span>

<span data-ttu-id="c8d7e-152">L’algorithme de machine learning de classification est idéal pour ce scénario.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-152">The classification machine learning algorithm is best suited for this scenario.</span></span>

### <a name="about-the-classification-algorithm"></a><span data-ttu-id="c8d7e-153">À propos de l’algorithme de classification</span><span class="sxs-lookup"><span data-stu-id="c8d7e-153">About the classification algorithm</span></span>

<span data-ttu-id="c8d7e-154">La classification est un algorithme de machine learning qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-154">Classification is a machine learning algorithm that uses data to **determine** the category, type, or class of an item or row of data.</span></span> <span data-ttu-id="c8d7e-155">Par exemple, vous pouvez utiliser la classification pour :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-155">For example, you can use classification to:</span></span>

* <span data-ttu-id="c8d7e-156">Identifier un sentiment positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-156">Identify sentiment as positive or negative.</span></span>
* <span data-ttu-id="c8d7e-157">Classer un e-mail comme spam, indésirable ou autorisé.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-157">Classify email as spam, junk, or good.</span></span>
* <span data-ttu-id="c8d7e-158">Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-158">Determine whether a patient's lab sample is cancerous.</span></span>
* <span data-ttu-id="c8d7e-159">Classer des clients selon leur tendance à répondre à une campagne commerciale.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-159">Categorize customers by their propensity to respond to a sales campaign.</span></span>

<span data-ttu-id="c8d7e-160">Les algorithmes de classification sont souvent de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-160">Classification algorithms are frequently one of the following types:</span></span>

* <span data-ttu-id="c8d7e-161">Binaire : A ou B.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-161">Binary: either A or B.</span></span>
* <span data-ttu-id="c8d7e-162">Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-162">Multiclass: multiple categories that can be predicted by using a single model.</span></span>

<span data-ttu-id="c8d7e-163">Dans la mesure où les commentaires du site web doivent être classés comme positifs ou négatifs, on utilise l’algorithme de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-163">Because the website comments need to be classified as either positive or negative, you use the Binary Classification algorithm.</span></span> 

## <a name="create-a-console-application"></a><span data-ttu-id="c8d7e-164">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="c8d7e-164">Create a console application</span></span>

1. <span data-ttu-id="c8d7e-165">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-165">Open Visual Studio 2017.</span></span> <span data-ttu-id="c8d7e-166">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-166">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="c8d7e-167">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-167">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="c8d7e-168">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-168">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="c8d7e-169">Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-169">In the **Name** text box, type "SentimentAnalysis" and then select the **OK** button.</span></span>

2. <span data-ttu-id="c8d7e-170">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-170">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="c8d7e-171">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-171">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="c8d7e-172">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-172">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="c8d7e-173">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-173">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="c8d7e-174">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-174">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="c8d7e-175">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-175">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="c8d7e-176">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-176">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-your-data"></a><span data-ttu-id="c8d7e-177">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-177">Prepare your data</span></span>

1. <span data-ttu-id="c8d7e-178">Téléchargez le [fichier zip du jeu de données UCI Sentiment Labeled Sentences (voir les citations dans la remarque ci-dessous)](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/sentiment%20labelled%20sentences.zip) et décompressez-le.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-178">Download [The UCI Sentiment Labeled Sentences dataset zip file (see citations in the following note)](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/sentiment%20labelled%20sentences.zip), and unzip.</span></span>

2. <span data-ttu-id="c8d7e-179">Copiez le fichier `yelp_labelled.txt` dans le répertoire *Données* que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-179">Copy the `yelp_labelled.txt` file into the *Data* directory you created.</span></span>

> [!NOTE]
> <span data-ttu-id="c8d7e-180">Les jeux de données utilisés par ce tutoriel proviennent de « From Group to Individual Labels using Deep Features » (Kotzias et.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-180">The datasets this tutorial uses are from the 'From Group to Individual Labels using Deep Features', Kotzias et.</span></span> <span data-ttu-id="c8d7e-181">al.,</span><span class="sxs-lookup"><span data-stu-id="c8d7e-181">al,.</span></span> <span data-ttu-id="c8d7e-182">KDD 2015), hébergé dans le référentiel UCI Machine Learning (Dua, D. et Karra Taniskidou, E., 2017).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-182">KDD 2015, and hosted at the UCI Machine Learning Repository - Dua, D. and Karra Taniskidou, E. (2017).</span></span> <span data-ttu-id="c8d7e-183">Référentiel UCI Machine Learning [http://archive.ics.uci.edu/ml].</span><span class="sxs-lookup"><span data-stu-id="c8d7e-183">UCI Machine Learning Repository [http://archive.ics.uci.edu/ml].</span></span> <span data-ttu-id="c8d7e-184">Irvine (Californie) : Université de Californie, School of Information and Computer Science.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-184">Irvine, CA: University of California, School of Information and Computer Science.</span></span>

3. <span data-ttu-id="c8d7e-185">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le fichier `yelp_labeled.txt` et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-185">In Solution Explorer, right-click the `yelp_labeled.txt` file and select **Properties**.</span></span> <span data-ttu-id="c8d7e-186">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-186">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="c8d7e-187">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="c8d7e-187">Create classes and define paths</span></span>

<span data-ttu-id="c8d7e-188">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-188">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddUsings "Add necessary usings")]

<span data-ttu-id="c8d7e-189">Il faut créer deux champs globaux pour le chemin d’accès du fichier de jeu de données téléchargé et celui du fichier de modèle enregistré :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-189">You need to create two global fields to hold the recently downloaded dataset file path and the saved model file path:</span></span>

* <span data-ttu-id="c8d7e-190">`_dataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-190">`_dataPath` has the path to the dataset used to train the model.</span></span>
* <span data-ttu-id="c8d7e-191">`_modelPath` contient le chemin d’accès où le modèle formé est enregistré.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-191">`_modelPath` has the path where the trained model is saved.</span></span>

<span data-ttu-id="c8d7e-192">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-192">Add the following code to the line right above the `Main` method to specify those paths:</span></span>

[!code-csharp[Declare global variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DeclareGlobalVariables "Declare global variables")]

<span data-ttu-id="c8d7e-193">Vous devez créer des classes pour vos données d’entrée et prévisions.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-193">You need to create some classes for your input data and predictions.</span></span> <span data-ttu-id="c8d7e-194">Ajoutez une nouvelle classe à votre projet :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-194">Add a new class to your project:</span></span>

1. <span data-ttu-id="c8d7e-195">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-195">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="c8d7e-196">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-196">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *SentimentData.cs*.</span></span> <span data-ttu-id="c8d7e-197">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-197">Then, select the **Add** button.</span></span>

    <span data-ttu-id="c8d7e-198">Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-198">The *SentimentData.cs* file opens in the code editor.</span></span> <span data-ttu-id="c8d7e-199">Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-199">Add the following `using` statement to the top of *SentimentData.cs*:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#AddUsings "Add necessary usings")]

<span data-ttu-id="c8d7e-200">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-200">Remove the existing class definition and add the following code, which has two classes `SentimentData` and `SentimentPrediction`, to the *SentimentData.cs* file:</span></span>

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#DeclareTypes "Declare data record types")]

<span data-ttu-id="c8d7e-201">La classe du jeu de données d’entrée, `SentimentData`, contient une `string` pour le commentaire (`SentimentText`) et un `bool` (`Sentiment`) qui a une valeur de sentiment positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-201">The input dataset class, `SentimentData`, has a `string` for the comment (`SentimentText`) and a `bool` (`Sentiment`) that has a value for sentiment of either positive or negative.</span></span> <span data-ttu-id="c8d7e-202">Les deux champs sont associés à des attributs <xref:Microsoft.ML.Data.LoadColumnAttribute.%23ctor%28System.Int32%29>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-202">Both fields have <xref:Microsoft.ML.Data.LoadColumnAttribute.%23ctor%28System.Int32%29> attributes attached to them.</span></span> <span data-ttu-id="c8d7e-203">Cet attribut décrit l’ordre des champs dans le fichier de données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-203">This attribute describes the order of each field in the data file.</span></span>  <span data-ttu-id="c8d7e-204">Par ailleurs, la propriété `Sentiment` comporte un <xref:Microsoft.ML.Data.ColumnNameAttribute.%23ctor%2A> qui la désigne comme le champ `Label`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-204">In addition, the `Sentiment` property has a <xref:Microsoft.ML.Data.ColumnNameAttribute.%23ctor%2A> to designate it as the `Label` field.</span></span> <span data-ttu-id="c8d7e-205">`SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-205">`SentimentPrediction` is the class used for prediction after the model has been trained.</span></span> <span data-ttu-id="c8d7e-206">Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-206">It has a single boolean (`Sentiment`) and a `PredictedLabel` `ColumnName` attribute.</span></span> <span data-ttu-id="c8d7e-207">L’attribut `Label` sert à créer le modèle et à effectuer son apprentissage, mais il est aussi utilisé avec le jeu de données de test fractionné pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-207">The `Label` is used to create and train the model, and it's also used with the split out test dataset to evaluate the model.</span></span> <span data-ttu-id="c8d7e-208">L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-208">The `PredictedLabel` is used during prediction and evaluation.</span></span> <span data-ttu-id="c8d7e-209">L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-209">For evaluation, an input with training data, the predicted values, and the model are used.</span></span>

<span data-ttu-id="c8d7e-210">Lors de la création d’un modèle avec ML .NET, vous commencez par créer un <xref:Microsoft.ML.MLContext>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-210">When building a model with ML.NET you start by creating an <xref:Microsoft.ML.MLContext>.</span></span> <span data-ttu-id="c8d7e-211">D’un point de vue conceptuel, `MLContext` est comparable à `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-211">`MLContext` is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="c8d7e-212">L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-212">The environment provides a context for your ML job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="c8d7e-213">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="c8d7e-213">Initialize variables in Main</span></span>

<span data-ttu-id="c8d7e-214">Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-214">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="c8d7e-215">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-215">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateMLContext "Create the ML Context")]

<span data-ttu-id="c8d7e-216">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-216">Add the following as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallLoadData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallLoadData)]

<span data-ttu-id="c8d7e-217">La méthode `LoadData` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-217">The `LoadData` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-218">Charge les données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-218">Loads the data.</span></span>
* <span data-ttu-id="c8d7e-219">Fractionne le jeu de données chargé en jeux de données d’apprentissage et de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-219">Splits the loaded dataset into train and test datasets.</span></span>
* <span data-ttu-id="c8d7e-220">Retourne les jeux de données d’apprentissage et de test fractionnés.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-220">Returns the split train and test datasets.</span></span>

<span data-ttu-id="c8d7e-221">Créez la méthode `LoadData` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-221">Create the `LoadData` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static TrainCatalogBase.TrainTestData LoadData(MLContext mlContext)
{

}
```
## <a name="load-the-data"></a><span data-ttu-id="c8d7e-222">Charger les données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-222">Load the data</span></span>

<span data-ttu-id="c8d7e-223">Comme le type de modèle de données `SentimentData` créé précédemment correspond au schéma du jeu de données, il est possible de combiner l’initialisation, le mappage et le chargement du jeu de données en une seule ligne de code avec le wrapper `MLContext.Data.LoadFromTextFile` de la [méthode LoadFromTextFile](xref:Microsoft.ML.TextLoaderSaverCatalog.LoadFromTextFile%60%601%28Microsoft.ML.DataOperationsCatalog,System.String,System.Char,System.Boolean,System.Boolean,System.Boolean,System.Boolean%29).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-223">Since your previously created `SentimentData` data model type matches the dataset schema, you can combine the initialization, mapping, and dataset loading into one line of code using the `MLContext.Data.LoadFromTextFile` wrapper for the [LoadFromTextFile method](xref:Microsoft.ML.TextLoaderSaverCatalog.LoadFromTextFile%60%601%28Microsoft.ML.DataOperationsCatalog,System.String,System.Char,System.Boolean,System.Boolean,System.Boolean,System.Boolean%29).</span></span> <span data-ttu-id="c8d7e-224">Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-224">It returns a <xref:Microsoft.Data.DataView.IDataView>.</span></span> 

 <span data-ttu-id="c8d7e-225">En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-225">As the input and output of `Transforms`, a `DataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="c8d7e-226">Dans ML.NET, les données sont semblables à une vue SQL.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-226">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="c8d7e-227">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-227">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="c8d7e-228">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-228">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="c8d7e-229">Pour ce tutoriel, il charge un jeu de données avec des commentaires et les sentiments positifs ou négatifs correspondants.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-229">For this tutorial, it loads a dataset with comments and corresponding toxic or non toxic sentiment.</span></span> <span data-ttu-id="c8d7e-230">Cette méthode permet de créer puis de former le modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-230">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="c8d7e-231">Ajoutez le code suivant comme première ligne de la méthode `LoadData` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-231">Add the following code as the first line of the `LoadData` method:</span></span>

[!code-csharp[LoadData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#LoadData "loading dataset")]

### <a name="split-the-dataset-for-model-training-and-testing"></a><span data-ttu-id="c8d7e-232">Fractionner le jeu de données pour l’apprentissage et le test du modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-232">Split the dataset for model training and testing</span></span>

<span data-ttu-id="c8d7e-233">Deux jeux de données sont maintenant nécessaires : un jeu de données d’apprentissage pour entraîner le modèle et un jeu de données de test pour l’évaluer.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-233">Next, you need both a training dataset to train the model and a test dataset to evaluate the model.</span></span> <span data-ttu-id="c8d7e-234">Utilisez `MLContext.BinaryClassification.TrainTestSplit`, qui inclut <xref:Microsoft.ML.StaticPipe.TrainingStaticExtensions.TrainTestSplit%2A> dans un wrapper, pour fractionner le jeu de données chargé en jeux de données d’apprentissage et de test et les retourner dans <xref:Microsoft.ML.TrainCatalogBase.TrainTestData>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-234">Use the `MLContext.BinaryClassification.TrainTestSplit` which wraps <xref:Microsoft.ML.StaticPipe.TrainingStaticExtensions.TrainTestSplit%2A> to split the loaded dataset into train and test datasets and return them inside of a <xref:Microsoft.ML.TrainCatalogBase.TrainTestData>.</span></span> <span data-ttu-id="c8d7e-235">Pour spécifier la fraction de données réservée au jeu de test, utilisez le paramètre `testFraction`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-235">You can specify the fraction of data for the test set with the `testFraction`parameter.</span></span> <span data-ttu-id="c8d7e-236">La valeur par défaut est 10 %, mais on choisira dans ce cas 20 % pour consacrer davantage de données à l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-236">The default is 10% but you use 20% in this case to use more data for the evaluation.</span></span>  

<span data-ttu-id="c8d7e-237">Pour fractionner les données chargées dans les jeux de données nécessaires, ajoutez le code suivant sur la ligne suivant la méthode `LoadData` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-237">To split the loaded data into the needed datasets, add the following code as the next line in the `LoadData` method:</span></span>

[!code-csharp[SplitData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#SplitData "Split the Data")]

<span data-ttu-id="c8d7e-238">Retournez `splitDataView` à la fin de la méthode `LoadData` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-238">Return the `splitDataView` at the end of the `LoadData` method:</span></span>

[!code-csharp[ReturnSplitData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#ReturnSplitData)]

## <a name="build-and-train-the-model"></a><span data-ttu-id="c8d7e-239">Générer et entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-239">Build and train the model</span></span>

<span data-ttu-id="c8d7e-240">Ajoutez l’appel suivant à la méthode `BuildAndTrainModel` comme prochaine ligne de code dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-240">Add the following call to the `BuildAndTrainModel`method as the next line of code in the `Main` method:</span></span>

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallBuildAndTrainModel)]

<span data-ttu-id="c8d7e-241">La méthode `BuildAndTrainModel` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-241">The `BuildAndTrainModel` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-242">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-242">Extracts and transforms the data.</span></span>
* <span data-ttu-id="c8d7e-243">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-243">Trains the model.</span></span>
* <span data-ttu-id="c8d7e-244">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-244">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="c8d7e-245">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-245">Returns the model.</span></span>

<span data-ttu-id="c8d7e-246">Créez la méthode `BuildAndTrainModel` juste après la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-246">Create the `BuildAndTrainModel` method, just after the `Main` method, using the following code:</span></span>

```csharp
public static ITransformer BuildAndTrainModel(MLContext mlContext, IDataView splitTrainSet)
{

}
```

<span data-ttu-id="c8d7e-247">Deux paramètres sont passés à la méthode Train : `MLContext` pour le contexte (`mlContext`) et `IDataView` pour le jeu de données d’apprentissage (`splitTrainSet`).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-247">Notice that two parameters are passed into the Train method; a `MLContext` for the context (`mlContext`), and an `IDataView`for the training dataset (`splitTrainSet`).</span></span> 

## <a name="extract-and-transform-the-data"></a><span data-ttu-id="c8d7e-248">Extraire et transformer les données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-248">Extract and transform the data</span></span>

<span data-ttu-id="c8d7e-249">Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-249">Pre-processing and cleaning data are important tasks that occur before a dataset is used effectively for machine learning.</span></span> <span data-ttu-id="c8d7e-250">Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-250">Raw data is often noisy and unreliable, and may be missing values.</span></span> <span data-ttu-id="c8d7e-251">L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-251">Using data without these modeling tasks can produce misleading results.</span></span>

<span data-ttu-id="c8d7e-252">Les pipelines de transformation ML.NET composent un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-252">ML.NET's transform pipelines compose a custom set of transforms that are applied to your data before training or testing.</span></span> <span data-ttu-id="c8d7e-253">Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-253">The transforms' primary purpose is data [featurization](../resources/glossary.md#feature-engineering).</span></span> <span data-ttu-id="c8d7e-254">Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-254">Machine learning algorithms understand [featurized](../resources/glossary.md#feature) data, so the next step is to transform our textual data into a format that our ML algorithms recognize.</span></span> <span data-ttu-id="c8d7e-255">Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-255">That format is a [numeric vector](../resources/glossary.md#numerical-feature-vector).</span></span>

<span data-ttu-id="c8d7e-256">Appliquez un pipeline `mlContext.Transforms.Text.FeaturizeText` pour convertir la colonne `SentimentText` en un vecteur numérique appelé `Features` utilisé par l’algorithme Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-256">Next, call `mlContext.Transforms.Text.FeaturizeText` which featurizes the text column (`SentimentText`) column into a numeric vector called `Features` used by the machine learning algorithm.</span></span> <span data-ttu-id="c8d7e-257">Il s’agit d’un appel de wrapper qui retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera un pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-257">This is a wrapper call that returns an <xref:Microsoft.ML.Data.EstimatorChain%601> that will effectively be a pipeline.</span></span> <span data-ttu-id="c8d7e-258">Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-258">Name this `pipeline` as you will then append the trainer to the `EstimatorChain`.</span></span> <span data-ttu-id="c8d7e-259">Ajoutez le contenu suivant comme prochaine ligne de code :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-259">Add this as the next line of code:</span></span>

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#FeaturizeText "Featurize the text")]

>[!WARNING]
> <span data-ttu-id="c8d7e-260">ML.NET version 0.10 a changé l’ordre des paramètres de transformation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-260">ML.NET Version 0.10 changed the order of the Transform parameters.</span></span> <span data-ttu-id="c8d7e-261">Cela ne provoque aucune jusqu’à ce que vous exécutiez l’application et génériez le modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-261">This will not error out until you run the application and build the model.</span></span> <span data-ttu-id="c8d7e-262">Utilisez les noms de paramètre pour les transformations comme illustré dans l’extrait de code précédent.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-262">Use the parameter names for Transforms as illustrated in the previous code snippet.</span></span>

<span data-ttu-id="c8d7e-263">Il s’agit de l’étape de prétraitement/fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-263">This is the preprocessing/featurization step.</span></span> <span data-ttu-id="c8d7e-264">L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-264">Using additional components available in ML.NET can enable better results with your model.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="c8d7e-265">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="c8d7e-265">Choose a learning algorithm</span></span>

<span data-ttu-id="c8d7e-266">Pour ajouter le formateur, appelez la méthode de wrapper `mlContext.BinaryClassification.Trainers.FastTree` qui retourne un objet <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-266">To add the trainer, call the `mlContext.BinaryClassification.Trainers.FastTree` wrapper method which returns a <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer> object.</span></span> <span data-ttu-id="c8d7e-267">Il s’agit d’un apprenant d’arbre de décision que vous utiliserez dans ce pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-267">This is a decision tree learner you'll use in this pipeline.</span></span> <span data-ttu-id="c8d7e-268">L’objet `FastTreeBinaryClassificationTrainer` est ajouté à `pipeline` et accepte les caractéristiques `SentimentText` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir de l’historique des données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-268">The `FastTreeBinaryClassificationTrainer` is appended to the `pipeline` and accepts the featurized `SentimentText` (`Features`) and the `Label` input parameters to learn from the historic data.</span></span>

<span data-ttu-id="c8d7e-269">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-269">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[FastTreeBinaryClassificationTrainer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddTrainer "Add a FastTreeBinaryClassificationTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="c8d7e-270">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-270">Train the model</span></span>

<span data-ttu-id="c8d7e-271">Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-271">You train the model, <xref:Microsoft.ML.Data.TransformerChain%601>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="c8d7e-272">Une fois l’estimateur défini, effectuez l’apprentissage de votre modèle avec la méthode <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-272">Once the estimator has been defined, you train your model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> method while providing the already loaded training data.</span></span> <span data-ttu-id="c8d7e-273">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-273">This returns a model to use for predictions.</span></span> <span data-ttu-id="c8d7e-274">`pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-274">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="c8d7e-275">L’expérience n’est pas exécutée tant que la méthode `.Fit()` s’exécute.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-275">The experiment is not executed until the `.Fit()` method runs.</span></span>

<span data-ttu-id="c8d7e-276">Ajoutez le code suivant à la méthode `BuildAndTrainModel` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-276">Add the following code to the `BuildAndTrainModel` method:</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#TrainModel "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a><span data-ttu-id="c8d7e-277">Enregistrer et revenir au modèle formé à utiliser pour l’évaluation</span><span class="sxs-lookup"><span data-stu-id="c8d7e-277">Save and Return the model trained to use for evaluation</span></span>

<span data-ttu-id="c8d7e-278">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-278">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain%601> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="c8d7e-279">Retournez le modèle à la fin de la méthode `BuildAndTrainModel`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-279">Return the model at the end of the `BuildAndTrainModel` method.</span></span>

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#ReturnModel "Return the model")]

## <a name="evaluate-the-model"></a><span data-ttu-id="c8d7e-280">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-280">Evaluate the model</span></span>

<span data-ttu-id="c8d7e-281">Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-281">Now that you've created and trained the model, you need to evaluate it with a different dataset for quality assurance and validation.</span></span> <span data-ttu-id="c8d7e-282">Dans la méthode `Evaluate`, le modèle créé dans `BuildAndTrainModel` est passé pour évaluation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-282">In the `Evaluate` method, the model created in `BuildAndTrainModel` is passed in to be evaluated.</span></span> <span data-ttu-id="c8d7e-283">Créez la méthode `Evaluate` juste après `BuildAndTrainModel`, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-283">Create the `Evaluate` method, just after `BuildAndTrainModel`, as in the following code:</span></span>

```csharp
public static void Evaluate(MLContext mlContext, ITransformer model, IDataView splitTestSet)
{

}
```

<span data-ttu-id="c8d7e-284">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-284">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-285">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-285">Loads the test dataset.</span></span>
* <span data-ttu-id="c8d7e-286">Crée l’évaluateur de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-286">Creates the binaryclassification evaluator.</span></span>
* <span data-ttu-id="c8d7e-287">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-287">Evaluates the model and creates metrics.</span></span>
* <span data-ttu-id="c8d7e-288">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-288">Displays the metrics.</span></span>

<span data-ttu-id="c8d7e-289">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-289">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallEvaluate "Call the Evaluate method")]

<span data-ttu-id="c8d7e-290">Utilisons maintenant le paramètre `model` Machine Learning (transformateur) et le paramètre `splitTestSet` pour donner en entrée les caractéristiques et retourner des prédictions.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-290">Next, you'll use the machine learning `model` parameter (a transformer) and the `splitTestSet` parameter to input the features and return predictions.</span></span> <span data-ttu-id="c8d7e-291">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-291">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#TransformData "Predict using the Transformer")]

<span data-ttu-id="c8d7e-292">La méthode `mlContext.BinaryClassification.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-292">The `mlContext.BinaryClassification.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="c8d7e-293">Elle retourne un objet <xref:Microsoft.ML.Data.CalibratedBinaryClassificationMetrics> contenant les mesures globales calculées par les évaluateurs de classification binaire.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-293">It returns a <xref:Microsoft.ML.Data.CalibratedBinaryClassificationMetrics> object that contains the overall metrics computed by binary classification evaluators.</span></span> <span data-ttu-id="c8d7e-294">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-294">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="c8d7e-295">Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-295">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Evaluate "Compute Metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a><span data-ttu-id="c8d7e-296">Affichage des métriques pour la validation du modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-296">Displaying the metrics for model validation</span></span>

<span data-ttu-id="c8d7e-297">Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-297">Use the following code to display the metrics, share the results, and then act on them:</span></span>

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DisplayMetrics "Display selected metrics")]

<span data-ttu-id="c8d7e-298">Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-298">To save your model to a .zip file before returning, add the following code to call the `SaveModelAsFile` method as the next line in `Evaluate`:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallSaveModel "Save the model")]

## <a name="save-the-model-as-azip-file"></a><span data-ttu-id="c8d7e-299">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="c8d7e-299">Save the model as a.zip file</span></span>

<span data-ttu-id="c8d7e-300">Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-300">Create the `SaveModelAsFile` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="c8d7e-301">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-301">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-302">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-302">Saves the model as a .zip file.</span></span>

<span data-ttu-id="c8d7e-303">Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-303">Next, create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="c8d7e-304">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-304">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="c8d7e-305">Pour l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-305">To save this as a zip file, you'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="c8d7e-306">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-306">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#SaveModel "Add the SaveTo Method")]

<span data-ttu-id="c8d7e-307">Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-307">You could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a><span data-ttu-id="c8d7e-308">Prédire le résultat des données de test avec le modèle enregistré</span><span class="sxs-lookup"><span data-stu-id="c8d7e-308">Predict the test data outcome with the saved model</span></span>

<span data-ttu-id="c8d7e-309">Créez la méthode `UseModelWithSingleItem` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-309">Create the `UseModelWithSingleItem` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void UseModelWithSingleItem(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="c8d7e-310">La méthode `UseModelWithSingleItem` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-310">The `UseModelWithSingleItem` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-311">Crée un commentaire unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-311">Creates a single comment of test data.</span></span>
* <span data-ttu-id="c8d7e-312">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-312">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="c8d7e-313">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-313">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="c8d7e-314">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-314">Displays the predicted results.</span></span>

<span data-ttu-id="c8d7e-315">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-315">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallUseModelWithSingleItem](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallUseModelWithSingleItem "Call the UseModelWithSingleItem method")]

<span data-ttu-id="c8d7e-316">Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-316">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="c8d7e-317">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-317">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="c8d7e-318">Nous allons ajouter le code suivant pour créer le `PredictionEngine` comme première ligne dans la méthode `Predict` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-318">Let's add the following code to create the `PredictionEngine` as the first line in the `Predict` Method:</span></span>

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreatePredictionEngine1 "Create the PredictionEngine")]
  
<span data-ttu-id="c8d7e-319">Ajoutez un commentaire pour tester la prédiction du modèle formé dans la méthode `Predict` en créant une instance de `SentimentData` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-319">Add a comment to test the trained model's prediction in the `Predict` method by creating an instance of `SentimentData`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateTestIssue1 "Create test data for single prediction")]

 <span data-ttu-id="c8d7e-320">Vous pouvez l’utiliser pour prédire le sentiment positif ou négatif d’une seule instance de données de commentaires.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-320">You can use that to predict the positive or negative sentiment of a single instance of the comment data.</span></span> <span data-ttu-id="c8d7e-321">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-321">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="c8d7e-322">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-322">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="c8d7e-323">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-323">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="c8d7e-324">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-324">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Predict "Create a prediction of sentiment")]

### <a name="use-the-model-prediction"></a><span data-ttu-id="c8d7e-325">Utiliser le modèle à des fins de prédiction</span><span class="sxs-lookup"><span data-stu-id="c8d7e-325">Use the model: prediction</span></span>

<span data-ttu-id="c8d7e-326">Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-326">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="c8d7e-327">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-327">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="c8d7e-328">Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-328">Create a display for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#OutputPrediction "Display prediction output")]

## <a name="deploy-and-predict-with-a-loaded-model"></a><span data-ttu-id="c8d7e-329">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="c8d7e-329">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="c8d7e-330">Créez la méthode `UseLoadedModelWithBatchItems` juste avant la méthode `SaveModelAsFile`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-330">Create the `UseLoadedModelWithBatchItems` method, just before the `SaveModelAsFile` method, using the following code:</span></span>

```csharp
public static void UseLoadedModelWithBatchItems(MLContext mlContext)
{

}
```

<span data-ttu-id="c8d7e-331">La méthode `UseLoadedModelWithBatchItems` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-331">The `UseLoadedModelWithBatchItems` method executes the following tasks:</span></span>

* <span data-ttu-id="c8d7e-332">Crée les données de test par lots.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-332">Creates batch test data.</span></span>
* <span data-ttu-id="c8d7e-333">Prédit les sentiments en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-333">Predicts sentiment based on test data.</span></span>
* <span data-ttu-id="c8d7e-334">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-334">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="c8d7e-335">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-335">Displays the predicted results.</span></span>

<span data-ttu-id="c8d7e-336">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `UseModelWithSingleItem`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-336">Add a call to the new method from the `Main` method, right under the `UseModelWithSingleItem` method call, using the following code:</span></span>

[!code-csharp[CallPredictModelLoaded](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallUseLoadedModelWithBatchItems "Call the CallUseLoadedModelWithBatchItems method")]

<span data-ttu-id="c8d7e-337">Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `UseLoadedModelWithBatchItems` :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-337">Add some comments to test the trained model's predictions in the `UseLoadedModelWithBatchItems` method:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateTestIssues "Create test data for predictions")]

<span data-ttu-id="c8d7e-338">Charger le modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-338">Load the model</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#LoadModel "Load the model")]

<span data-ttu-id="c8d7e-339">Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.ITransformer.Transform%2A>.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-339">Now that you have a model, you can use that to predict the Toxic or Non Toxic sentiment of the comment data using the <xref:Microsoft.ML.ITransformer.Transform%2A> method.</span></span> <span data-ttu-id="c8d7e-340">Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-340">To get a prediction, use `Predict` on new data.</span></span> <span data-ttu-id="c8d7e-341">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-341">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="c8d7e-342">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-342">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="c8d7e-343">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-343">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span> <span data-ttu-id="c8d7e-344">Ajoutez le code suivant à la méthode `UseLoadedModelWithBatchItems` pour les prédictions :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-344">Add the following code to the `UseLoadedModelWithBatchItems` method for the predictions:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Prediction "Create predictions of sentiments")]

### <a name="use-the-loaded-model-for-prediction"></a><span data-ttu-id="c8d7e-345">Utiliser le modèle chargé à des fins de prédiction</span><span class="sxs-lookup"><span data-stu-id="c8d7e-345">Use the loaded model for prediction</span></span>

<span data-ttu-id="c8d7e-346">Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-346">Display `SentimentText` and corresponding sentiment prediction in order to share the results and act on them accordingly.</span></span> <span data-ttu-id="c8d7e-347">Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-347">This is called operationalization, using the returned data as part of the operational policies.</span></span> <span data-ttu-id="c8d7e-348">Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-348">Create a header for the results using the following <xref:System.Console.WriteLine?displayProperty=nameWithType> code:</span></span>

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddInfoMessage "Display prediction outputs")]

<span data-ttu-id="c8d7e-349">Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-349">Before displaying the predicted results, combine the sentiment and prediction together to see the original comment with its predicted sentiment.</span></span> <span data-ttu-id="c8d7e-350">Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-350">The following code uses the <xref:System.Linq.Enumerable.Zip%2A> method to make that happen, so add that code next:</span></span>

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#BuildSentimentPredictionPairs "Build the pairs of sentiment data and predictions")]

<span data-ttu-id="c8d7e-351">Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-351">Now that you've combined the `SentimentText` and `Sentiment` into a class, you can display the results using the <xref:System.Console.WriteLine?displayProperty=nameWithType> method:</span></span>

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DisplayResults "Display the predictions")]

<span data-ttu-id="c8d7e-352">Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-352">Because inferred tuple element names are a new feature in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span>
<span data-ttu-id="c8d7e-353">Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-353">To do that, right-click on the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="c8d7e-354">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-354">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="c8d7e-355">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-355">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="c8d7e-356">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-356">Select the **OK** button.</span></span>

## <a name="results"></a><span data-ttu-id="c8d7e-357">Résultats</span><span class="sxs-lookup"><span data-stu-id="c8d7e-357">Results</span></span>

<span data-ttu-id="c8d7e-358">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-358">Your results should be similar to the following.</span></span> <span data-ttu-id="c8d7e-359">Lors du traitement, le pipeline affiche des messages.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-359">As the pipeline processes, it displays messages.</span></span> <span data-ttu-id="c8d7e-360">Vous pouvez voir des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-360">You may see warnings, or processing messages.</span></span> <span data-ttu-id="c8d7e-361">Ils ont été supprimés des résultats ci-dessous par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-361">These have been removed from the following results for clarity.</span></span>

```console
Model quality metrics evaluation
--------------------------------
Accuracy: 79.14%
Auc: 86.27%
F1Score: 80.60%

=============== End of model evaluation ===============
The model is saved to C:\Tutorials\SentimentAnalysis\bin\Debug\netcoreapp2.1\Data\Model.zip

=============== Prediction Test of model with a single sample and test dataset ===============

Sentiment: This was a very bad steak | Prediction: Negative | Probability: 0.4641322
=============== End of Predictions ===============


=============== Prediction Test of loaded model with a multiple samples ===============

Sentiment: This was a horrible meal | Prediction: Negative | Probability: 0.1391833
Sentiment: I love this spaghetti. | Prediction: Positive | Probability: 0.9819039
=============== End of predictions ===============

=============== End of process ===============
Press any key to continue . . .

```

<span data-ttu-id="c8d7e-362">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="c8d7e-362">Congratulations!</span></span> <span data-ttu-id="c8d7e-363">Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction des sentiments de messages.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-363">You've now successfully built a machine learning model for classifying and predicting messages sentiment.</span></span> 

<span data-ttu-id="c8d7e-364">La création de modèles efficaces est un processus itératif.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-364">Building successful models is an iterative process.</span></span> <span data-ttu-id="c8d7e-365">Celui-ci présente une qualité initiale médiocre, car le tutoriel utilise de petits jeux de données pour permettre un apprentissage rapide du modèle.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-365">This model has initial lower quality as the tutorial uses small datasets to provide quick model training.</span></span> <span data-ttu-id="c8d7e-366">Si vous n’êtes pas satisfait de la qualité du modèle, vous pouvez essayer de l’améliorer en fournissant de plus gros jeux de données d’apprentissage ou en choisissant d’autres algorithmes d’apprentissage avec différents hyperparamètres pour chacun.</span><span class="sxs-lookup"><span data-stu-id="c8d7e-366">If you aren't satisfied with the model quality, you can try to improve it by providing larger training datasets or by choosing different training algorithms with different hyper-parameters for each algorithm.</span></span>

<span data-ttu-id="c8d7e-367">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).</span><span class="sxs-lookup"><span data-stu-id="c8d7e-367">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c8d7e-368">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c8d7e-368">Next steps</span></span>

<span data-ttu-id="c8d7e-369">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="c8d7e-369">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="c8d7e-370">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="c8d7e-370">Understand the problem</span></span>
> * <span data-ttu-id="c8d7e-371">Sélectionner l’algorithme de machine learning approprié</span><span class="sxs-lookup"><span data-stu-id="c8d7e-371">Select the appropriate machine learning algorithm</span></span>
> * <span data-ttu-id="c8d7e-372">Préparer vos données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-372">Prepare your data</span></span>
> * <span data-ttu-id="c8d7e-373">Transformer les données</span><span class="sxs-lookup"><span data-stu-id="c8d7e-373">Transform the data</span></span>
> * <span data-ttu-id="c8d7e-374">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-374">Train the model</span></span>
> * <span data-ttu-id="c8d7e-375">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="c8d7e-375">Evaluate the model</span></span>
> * <span data-ttu-id="c8d7e-376">Prédire avec le modèle entraîné</span><span class="sxs-lookup"><span data-stu-id="c8d7e-376">Predict with the trained model</span></span>
> * <span data-ttu-id="c8d7e-377">Déployer et prédire avec un modèle chargé</span><span class="sxs-lookup"><span data-stu-id="c8d7e-377">Deploy and Predict with a loaded model</span></span>

<span data-ttu-id="c8d7e-378">Passer au tutoriel suivant pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="c8d7e-378">Advance to the next tutorial to learn more</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="c8d7e-379">Classification des problèmes</span><span class="sxs-lookup"><span data-stu-id="c8d7e-379">Issue Classification</span></span>](github-issue-classification.md)
