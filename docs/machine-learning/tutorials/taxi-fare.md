---
title: Prédire des prix en utilisant un apprenant de régression avec ML.NET
description: Prédisez des prix en utilisant un apprenant de régression avec ML.NET.
author: aditidugar
ms.author: johalex
ms.date: 02/08/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 10e0fa2cedff3e31575ad2b9c8bc2d9ecc81f3e8
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092538"
---
# <a name="tutorial-predict-prices-using-a-regression-learner-with-mlnet"></a><span data-ttu-id="36d45-103">Tutoriel : Prédire des prix en utilisant un apprenant de régression avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="36d45-103">Tutorial: Predict prices using a regression learner with ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="36d45-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="36d45-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="36d45-105">Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="36d45-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="36d45-106">Ce tutoriel montre comment utiliserML.NET pour créer un [modèle de régression](../resources/glossary.md#regression) afin de prédire des prix, plus précisément, des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="36d45-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting prices, specifically, New York City taxi fares.</span></span>

<span data-ttu-id="36d45-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="36d45-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="36d45-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="36d45-108">Understand the problem</span></span>
> * <span data-ttu-id="36d45-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="36d45-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="36d45-110">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="36d45-110">Prepare and understand the data</span></span>
> * <span data-ttu-id="36d45-111">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="36d45-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="36d45-112">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="36d45-112">Load and transform the data</span></span>
> * <span data-ttu-id="36d45-113">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="36d45-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="36d45-114">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-114">Train the model</span></span>
> * <span data-ttu-id="36d45-115">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-115">Evaluate the model</span></span>
> * <span data-ttu-id="36d45-116">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="36d45-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36d45-117">Prérequis</span><span class="sxs-lookup"><span data-stu-id="36d45-117">Prerequisites</span></span>

* <span data-ttu-id="36d45-118">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="36d45-118">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="36d45-119">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="36d45-119">Understand the problem</span></span>

<span data-ttu-id="36d45-120">Ce problème consiste à prédire le prix d’une course de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="36d45-120">This problem is about predicting the fare of a taxi trip in New York City.</span></span> <span data-ttu-id="36d45-121">À première vue, ce prix semble dépendre simplement de la distance parcourue.</span><span class="sxs-lookup"><span data-stu-id="36d45-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="36d45-122">Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.</span><span class="sxs-lookup"><span data-stu-id="36d45-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="36d45-123">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="36d45-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="36d45-124">Vous souhaitez prédire le prix, qui est une valeur réelle, en fonction des autres facteurs du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="36d45-124">You want to predict the price value, which is a real value, based on the other factors in the data set.</span></span> <span data-ttu-id="36d45-125">Pour ce faire, choisissez une tâche d’apprentissage automatique par [régression](../resources/glossary.md#regression).</span><span class="sxs-lookup"><span data-stu-id="36d45-125">To do that you choose a [regression](../resources/glossary.md#regression) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="36d45-126">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="36d45-126">Create a console application</span></span>

1. <span data-ttu-id="36d45-127">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="36d45-127">Open Visual Studio 2017.</span></span> <span data-ttu-id="36d45-128">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="36d45-128">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="36d45-129">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="36d45-129">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="36d45-130">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="36d45-130">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="36d45-131">Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="36d45-131">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

1. <span data-ttu-id="36d45-132">Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :</span><span class="sxs-lookup"><span data-stu-id="36d45-132">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="36d45-133">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="36d45-133">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="36d45-134">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="36d45-134">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="36d45-135">Installez le package NuGet **Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="36d45-135">Install the **Microsoft.ML** NuGet Package:</span></span>

    <span data-ttu-id="36d45-136">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="36d45-136">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="36d45-137">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="36d45-137">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="36d45-138">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="36d45-138">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="36d45-139">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="36d45-139">Prepare and understand the data</span></span>

1. <span data-ttu-id="36d45-140">Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="36d45-140">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="36d45-141">Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-141">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="36d45-142">Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span><span class="sxs-lookup"><span data-stu-id="36d45-142">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

1. <span data-ttu-id="36d45-143">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="36d45-143">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="36d45-144">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="36d45-144">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

1. <span data-ttu-id="36d45-145">Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne.</span><span class="sxs-lookup"><span data-stu-id="36d45-145">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="36d45-146">Examinons chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="36d45-146">Take a look at each of the columns.</span></span> <span data-ttu-id="36d45-147">Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="36d45-147">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="36d45-148">**L’étiquette** est l’identificateur de la colonne à prédire.</span><span class="sxs-lookup"><span data-stu-id="36d45-148">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="36d45-149">Les **fonctionnalités** identifiées servent à prédire l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="36d45-149">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="36d45-150">Le jeu de données fourni contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="36d45-150">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="36d45-151">**vendor_id :** l’ID du taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36d45-151">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="36d45-152">**rate_code :** le type de tarif de la course de taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36d45-152">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="36d45-153">**passenger_count :** le nombre de passagers embarqués est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36d45-153">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="36d45-154">**trip_time_in_secs :** durée totale de la course.</span><span class="sxs-lookup"><span data-stu-id="36d45-154">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="36d45-155">Vous voulez prédire le prix de la course avant de l’effectuer.</span><span class="sxs-lookup"><span data-stu-id="36d45-155">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="36d45-156">À ce stade vous ne connaissez pas la durée de la course.</span><span class="sxs-lookup"><span data-stu-id="36d45-156">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="36d45-157">Par conséquent, la durée de la course n’est pas une fonctionnalité et vous devez exclure cette colonne du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-157">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="36d45-158">**trip_distance :** la distance de la course est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36d45-158">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="36d45-159">**payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="36d45-159">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="36d45-160">**fare_amount :** le prix total payé pour la course est l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="36d45-160">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="36d45-161">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="36d45-161">Create data classes</span></span>

<span data-ttu-id="36d45-162">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="36d45-162">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="36d45-163">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="36d45-163">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="36d45-164">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*.</span><span class="sxs-lookup"><span data-stu-id="36d45-164">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="36d45-165">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="36d45-165">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="36d45-166">Ajoutez les directives `using` suivantes au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="36d45-166">Add the following `using` directives to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="36d45-167">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :</span><span class="sxs-lookup"><span data-stu-id="36d45-167">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="36d45-168">`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="36d45-168">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="36d45-169">Utilisez l’attribut <xref:Microsoft.ML.Data.ColumnAttribute> pour spécifier les index des colonnes sources dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="36d45-169">Use the <xref:Microsoft.ML.Data.ColumnAttribute> attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="36d45-170">La classe `TaxiTripFarePrediction` représente les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="36d45-170">The `TaxiTripFarePrediction` class represents predicted results.</span></span> <span data-ttu-id="36d45-171">Elle comporte un seul champ float, `FareAmount`, avec un attribut `Score` <xref:Microsoft.ML.Data.ColumnNameAttribute> appliqué.</span><span class="sxs-lookup"><span data-stu-id="36d45-171">It has a single float field, `FareAmount`, with a `Score` <xref:Microsoft.ML.Data.ColumnNameAttribute> attribute applied.</span></span> <span data-ttu-id="36d45-172">Dans le cas de la tâche de régression, la colonne **Score** contient les valeurs d’étiquette prédites.</span><span class="sxs-lookup"><span data-stu-id="36d45-172">In case of the regression task the **Score** column contains predicted label values.</span></span>

> [!NOTE]
> <span data-ttu-id="36d45-173">Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="36d45-173">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="36d45-174">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-174">Define data and model paths</span></span>

<span data-ttu-id="36d45-175">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="36d45-175">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="36d45-176">Vous devez créer trois champs pour contenir les chemins des fichiers avec des jeux de données et le fichier pour enregistrer le modèle, ainsi qu’une variable globale pour `TextLoader` :</span><span class="sxs-lookup"><span data-stu-id="36d45-176">You need to create three fields to hold the paths to the files with data sets and the file to save the model, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="36d45-177">`_trainDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-177">`_trainDataPath` contains the path to the file with the data set used to train the model.</span></span>
* <span data-ttu-id="36d45-178">`_testDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’évaluation du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-178">`_testDataPath` contains the path to the file with the data set used to evaluate the model.</span></span>
* <span data-ttu-id="36d45-179">`_modelPath` contient le chemin du fichier où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="36d45-179">`_modelPath` contains the path to the file where the trained model is stored.</span></span>
* <span data-ttu-id="36d45-180">`_textLoader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.</span><span class="sxs-lookup"><span data-stu-id="36d45-180">`_textLoader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="36d45-181">Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins et pour la variable `_textLoader` :</span><span class="sxs-lookup"><span data-stu-id="36d45-181">Add the following code right above the `Main` method to specify those paths and for the `_textLoader` variable:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="36d45-182">Lors de la création d’un modèle avec ML.NET, vous commencez par créer un contexte ML.</span><span class="sxs-lookup"><span data-stu-id="36d45-182">When building a model with ML.NET you start by creating an ML Context.</span></span> <span data-ttu-id="36d45-183">Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="36d45-183">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="36d45-184">L’environnement fournit un contexte pour votre tâche Machine Learning et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="36d45-184">The environment provides a context for your machine learning job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="36d45-185">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="36d45-185">Initialize variables in Main</span></span>

<span data-ttu-id="36d45-186">Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.</span><span class="sxs-lookup"><span data-stu-id="36d45-186">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="36d45-187">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="36d45-187">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create the ML Context")]

<span data-ttu-id="36d45-188">Ensuite, pour configurer le chargement des données, initialisez variable globale `_textLoader` afin de la réutiliser.</span><span class="sxs-lookup"><span data-stu-id="36d45-188">Next, to setup for data loading initialize the `_textLoader` global variable in order to reuse it.</span></span> <span data-ttu-id="36d45-189">Quand vous créez un `TextLoader`, vous passez le contexte nécessaire et la classe <xref:Microsoft.ML.Data.TextLoader.Arguments> qui permet la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="36d45-189">When you create a `TextLoader`, you pass in the context needed and the <xref:Microsoft.ML.Data.TextLoader.Arguments> class which enables customization.</span></span> <span data-ttu-id="36d45-190">Spécifiez le schéma de données en passant un tableau d’objets <xref:Microsoft.ML.Data.TextLoader.Column> au `TextLoader` contenant tous les noms de colonne et leurs types.</span><span class="sxs-lookup"><span data-stu-id="36d45-190">Specify the data schema by passing an array of <xref:Microsoft.ML.Data.TextLoader.Column> objects to the `TextLoader` containing all the column names and their types.</span></span> <span data-ttu-id="36d45-191">Nous avons défini précédemment le schéma de données en créant notre classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="36d45-191">We defined the data schema previously when we created our `TaxiTrip` class.</span></span>

<span data-ttu-id="36d45-192">La classe `TextLoader` retourne une variable <xref:Microsoft.ML.Data.TextLoader> totalement initialisée</span><span class="sxs-lookup"><span data-stu-id="36d45-192">The `TextLoader` class returns a fully initialized <xref:Microsoft.ML.Data.TextLoader></span></span>  

<span data-ttu-id="36d45-193">Pour initialiser la variable globale `_textLoader` afin de la réutiliser pour les jeux de données nécessaires, ajoutez le code suivant après l’initialisation de `mlContext` :</span><span class="sxs-lookup"><span data-stu-id="36d45-193">To initialize the `_textLoader` global variable in order to reuse it for the needed datasets, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[initTextLoader](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Initialize the TextLoader")]

<span data-ttu-id="36d45-194">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` afin d’appeler la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="36d45-194">Add the following as the next line of code in the `Main` method to call the `Train` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Train your model")]

<span data-ttu-id="36d45-195">La méthode `Train` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="36d45-195">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="36d45-196">Charge les données.</span><span class="sxs-lookup"><span data-stu-id="36d45-196">Loads the data.</span></span>
* <span data-ttu-id="36d45-197">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="36d45-197">Extracts and transforms the data.</span></span>
* <span data-ttu-id="36d45-198">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-198">Trains the model.</span></span>
* <span data-ttu-id="36d45-199">Enregistre le modèle en tant que fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="36d45-199">Saves the model as .zip file.</span></span>
* <span data-ttu-id="36d45-200">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-200">Returns the model.</span></span>

<span data-ttu-id="36d45-201">La méthode `Train` effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-201">The `Train` method trains the model.</span></span> <span data-ttu-id="36d45-202">Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-202">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

<span data-ttu-id="36d45-203">Nous passons deux paramètres à la méthode `Train` ; un paramètre `MLContext` pour le contexte (`mlContext`) et une chaîne pour le chemin d’accès au jeu de données (`dataPath`).</span><span class="sxs-lookup"><span data-stu-id="36d45-203">We are passing two parameters into the `Train` method; an `MLContext` for the context (`mlContext`), and a string for the dataset path (`dataPath`).</span></span> <span data-ttu-id="36d45-204">Nous allons réutiliser cette méthode pour le chargement des jeux de données.</span><span class="sxs-lookup"><span data-stu-id="36d45-204">We're going to reuse this method for loading datasets.</span></span>

## <a name="load-and-transform-data"></a><span data-ttu-id="36d45-205">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="36d45-205">Load and transform data</span></span>

<span data-ttu-id="36d45-206">Nous allons charger les données en utilisant la variable globale `_textLoader` et le paramètre `dataPath`.</span><span class="sxs-lookup"><span data-stu-id="36d45-206">We'll load the data using the `_textLoader` global variable with the `dataPath` parameter.</span></span> <span data-ttu-id="36d45-207">Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>.</span><span class="sxs-lookup"><span data-stu-id="36d45-207">It returns a <xref:Microsoft.Data.DataView.IDataView>.</span></span> <span data-ttu-id="36d45-208">Comme entrée et sortie de transformations, un `IDataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="36d45-208">As the input and output of Transforms, an `IDataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="36d45-209">Dans ML.NET, les données sont semblables à une vue SQL.</span><span class="sxs-lookup"><span data-stu-id="36d45-209">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="36d45-210">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="36d45-210">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="36d45-211">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="36d45-211">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="36d45-212">Pour ce tutoriel, il charge un jeu de données avec des informations sur les courses de taxi, utiles pour en prédire le prix.</span><span class="sxs-lookup"><span data-stu-id="36d45-212">For this tutorial, it loads a dataset with taxi trip information useful to predict fares.</span></span> <span data-ttu-id="36d45-213">Cette méthode permet de créer puis de former le modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-213">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="36d45-214">Ajoutez le code suivant comme première ligne de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="36d45-214">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "loading training dataset")]

<span data-ttu-id="36d45-215">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="36d45-215">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="36d45-216">Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="36d45-216">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="36d45-217">Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="36d45-217">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="36d45-218">Pour ce faire, utilisez la classe de transformation `CopyColumnsEstimator`, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-218">To do that, use the `CopyColumnsEstimator` transformation class, and add the following code:</span></span>

[!code-csharp[CopyColumnsEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Use the CopyColumnsEstimator")]

<span data-ttu-id="36d45-219">L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques**, car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres.</span><span class="sxs-lookup"><span data-stu-id="36d45-219">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="36d45-220">Pour ce faire, utilisez la classe de transformation `OneHotEncodingEstimator`, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-220">To do that, use the `OneHotEncodingEstimator` transformation class, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

[!code-csharp[OneHotEncodingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Use the OneHotEncodingEstimator")]

<span data-ttu-id="36d45-221">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `ColumnConcatenatingEstimator`.</span><span class="sxs-lookup"><span data-stu-id="36d45-221">The last step in data preparation combines all of the feature columns into the **Features** column using the `ColumnConcatenatingEstimator` transformation class.</span></span> <span data-ttu-id="36d45-222">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="36d45-222">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="36d45-223">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-223">Add the following code:</span></span>

[!code-csharp[ColumnConcatenatingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Use the ColumnConcatenatingEstimator")]

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="36d45-224">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="36d45-224">Choose a learning algorithm</span></span>

<span data-ttu-id="36d45-225">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnons un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="36d45-225">After adding the data to the pipeline and transforming it into the correct input format, we select a learning algorithm (**learner**).</span></span> <span data-ttu-id="36d45-226">L’apprenant effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-226">The learner trains the model.</span></span> <span data-ttu-id="36d45-227">Nous avez choisi une tâche de **régression** pour ce problème. Nous utilisons donc un apprenant `FastTreeRegressionTrainer`, qui est l’un des apprenants de régression fournis par ML.NET.</span><span class="sxs-lookup"><span data-stu-id="36d45-227">We chose a **regression** task for this problem, so we use a `FastTreeRegressionTrainer` learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="36d45-228">L’apprenant `FastTreeRegressionTrainer` utilise le boosting de gradient.</span><span class="sxs-lookup"><span data-stu-id="36d45-228">The `FastTreeRegressionTrainer` learner utilizes gradient boosting.</span></span> <span data-ttu-id="36d45-229">Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="36d45-229">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="36d45-230">Il génère chaque arbre de régression étape par étape.</span><span class="sxs-lookup"><span data-stu-id="36d45-230">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="36d45-231">Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine.</span><span class="sxs-lookup"><span data-stu-id="36d45-231">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="36d45-232">Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces.</span><span class="sxs-lookup"><span data-stu-id="36d45-232">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="36d45-233">Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span><span class="sxs-lookup"><span data-stu-id="36d45-233">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="36d45-234">Ajoutez le code suivant dans la méthode `Train` afin d’ajouter le `FastTreeRegressionTrainer` au code de traitement des données ajouté à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="36d45-234">Add the following code into the `Train` method to add the `FastTreeRegressionTrainer` to the data processing code added in the previous step:</span></span>

[!code-csharp[FastTreeRegressionTrainer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Add the FastTreeRegressionTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="36d45-235">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-235">Train the model</span></span>

<span data-ttu-id="36d45-236">La dernière étape consiste à effectuer l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-236">The final step is to train the model.</span></span> <span data-ttu-id="36d45-237">Nous effectuons l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="36d45-237">We train the model, <xref:Microsoft.ML.Data.TransformerChain>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="36d45-238">Une fois l’estimation définie, nous formons le modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="36d45-238">Once the estimator has been defined, we train the model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="36d45-239">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="36d45-239">This returns a model to use for predictions.</span></span> <span data-ttu-id="36d45-240">`pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="36d45-240">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="36d45-241">L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="36d45-241">The experiment is not executed until this happens.</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#11 "Train the model")]

<span data-ttu-id="36d45-242">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="36d45-242">And that's it!</span></span> <span data-ttu-id="36d45-243">Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="36d45-243">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="36d45-244">Nous allons maintenant essayer de déterminer la précision du modèle et découvrir comment l’utiliser pour prédire les valeurs des tarifs de taxi.</span><span class="sxs-lookup"><span data-stu-id="36d45-244">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="36d45-245">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-245">Save the model</span></span>

<span data-ttu-id="36d45-246">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="36d45-246">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="36d45-247">Pour enregistrer le modèle dans un fichier .zip, ajoutez le code suivant à la fin de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="36d45-247">To save the model to a .zip file, add the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Save the model as a .zip file and return the model")]

## <a name="save-the-model-as-a-zip-file"></a><span data-ttu-id="36d45-248">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="36d45-248">Save the model as a .zip file</span></span>

<span data-ttu-id="36d45-249">Créez la méthode `SaveModelAsFile` juste après la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-249">Create the `SaveModelAsFile` method, just after the `Train` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="36d45-250">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="36d45-250">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="36d45-251">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="36d45-251">Saves the model as a .zip file.</span></span>

<span data-ttu-id="36d45-252">Nous devons créer une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="36d45-252">We need to create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="36d45-253">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="36d45-253">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="36d45-254">Comme nous souhaitons l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="36d45-254">Since we want to save this as a zip file, we'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="36d45-255">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="36d45-255">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Add the SaveTo Method")]

<span data-ttu-id="36d45-256">Nous pouvons également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-256">We could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="36d45-257">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-257">Evaluate the model</span></span>

<span data-ttu-id="36d45-258">L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="36d45-258">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="36d45-259">Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="36d45-259">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="36d45-260">Pour ce faire, vous pouvez, par exemple, fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme indiqué dans ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="36d45-260">One way to do this is to split the data into training and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="36d45-261">Une fois que vous avez formé le modèle à l’aide des données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="36d45-261">Now that you've trained the model on the training data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="36d45-262">La méthode `Evaluate` évalue le modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-262">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="36d45-263">Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="36d45-263">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```
<span data-ttu-id="36d45-264">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="36d45-264">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="36d45-265">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="36d45-265">Loads the test dataset.</span></span>
* <span data-ttu-id="36d45-266">Crée l’évaluateur de régression.</span><span class="sxs-lookup"><span data-stu-id="36d45-266">Creates the regression evaluator.</span></span>
* <span data-ttu-id="36d45-267">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="36d45-267">Evaluates the model and creates metrics.</span></span>
* <span data-ttu-id="36d45-268">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="36d45-268">Displays the metrics.</span></span>

<span data-ttu-id="36d45-269">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-269">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Call the Evaluate method")]

<span data-ttu-id="36d45-270">Nous allons charger le jeu de données de test à l’aide de la variable globale `_textLoader` précédemment initialisée avec le champ global `_testDataPath`.</span><span class="sxs-lookup"><span data-stu-id="36d45-270">We'll load the test dataset using the previously initialized  `_textLoader` global variable with the `_testDataPath` global field.</span></span> <span data-ttu-id="36d45-271">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="36d45-271">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="36d45-272">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="36d45-272">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Load the test dataset")]

<span data-ttu-id="36d45-273">Nous allons ensuite utiliser le paramètre Machine Learning `model` (un transformateur) pour saisir les fonctionnalités et retourner des prédictions.</span><span class="sxs-lookup"><span data-stu-id="36d45-273">Next, we'll use the machine learning `model` parameter (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="36d45-274">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="36d45-274">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Predict using the Transformer")]

<span data-ttu-id="36d45-275">La méthode `RegressionContext.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="36d45-275">The `RegressionContext.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="36d45-276">Elle retourne un objet <xref:Microsoft.ML.Data.RegressionMetrics> qui contient les métriques globales calculées par les évaluateurs de régression.</span><span class="sxs-lookup"><span data-stu-id="36d45-276">It returns a <xref:Microsoft.ML.Data.RegressionMetrics> object that contains the overall metrics computed by regression evaluators.</span></span> <span data-ttu-id="36d45-277">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="36d45-277">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="36d45-278">Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="36d45-278">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Compute Metrics")]

<span data-ttu-id="36d45-279">Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="36d45-279">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

```csharp
Console.WriteLine();
Console.WriteLine($"*************************************************");
Console.WriteLine($"*       Model quality metrics evaluation         ");
Console.WriteLine($"*------------------------------------------------");
```

<span data-ttu-id="36d45-280">[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression.</span><span class="sxs-lookup"><span data-stu-id="36d45-280">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="36d45-281">RSquared prend des valeurs entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="36d45-281">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="36d45-282">Plus sa valeur est proche de 1, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="36d45-282">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="36d45-283">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :</span><span class="sxs-lookup"><span data-stu-id="36d45-283">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#18 "Display the RSquared metric.")]

<span data-ttu-id="36d45-284">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression.</span><span class="sxs-lookup"><span data-stu-id="36d45-284">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="36d45-285">Plus sa valeur est faible, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="36d45-285">The lower it is, the better the model is.</span></span> <span data-ttu-id="36d45-286">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :</span><span class="sxs-lookup"><span data-stu-id="36d45-286">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#19 "Display the RMS metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="36d45-287">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="36d45-287">Use the model for predictions</span></span>


## <a name="predict-the-test-data-outcome-with-the-model-and-a-single-comment"></a><span data-ttu-id="36d45-288">Prédire le résultat de données de test avec le modèle et un commentaire unique</span><span class="sxs-lookup"><span data-stu-id="36d45-288">Predict the test data outcome with the model and a single comment</span></span>

<span data-ttu-id="36d45-289">Créez la méthode `TestSinglePrediction` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-289">Create the `TestSinglePrediction` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void TestSinglePrediction(MLContext mlContext)
{

}
```

<span data-ttu-id="36d45-290">La méthode `TestSinglePrediction` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="36d45-290">The `TestSinglePrediction` method executes the following tasks:</span></span>

* <span data-ttu-id="36d45-291">Crée un commentaire unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="36d45-291">Creates a single comment of test data.</span></span>
* <span data-ttu-id="36d45-292">Prédit le prix de la course en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="36d45-292">Predicts fare amount based on test data.</span></span>
* <span data-ttu-id="36d45-293">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="36d45-293">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="36d45-294">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="36d45-294">Displays the predicted results.</span></span>

<span data-ttu-id="36d45-295">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="36d45-295">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallTestSinglePrediction](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#20 "Call the TestSinglePrediction method")]

<span data-ttu-id="36d45-296">Étant donné que nous voulons charger le modèle à partir du fichier zip que nous avons enregistré, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `Load`.</span><span class="sxs-lookup"><span data-stu-id="36d45-296">Since we want to load the model from the zip file we saved, we'll create the `FileStream` immediately before calling the `Load` method.</span></span> <span data-ttu-id="36d45-297">Ajoutez comme nouvelle ligne le code suivant à la méthode `TestSinglePrediction` :</span><span class="sxs-lookup"><span data-stu-id="36d45-297">Add the following code to the `TestSinglePrediction` method as the next line:</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#21 "Load the model")]

<span data-ttu-id="36d45-298">Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels.</span><span class="sxs-lookup"><span data-stu-id="36d45-298">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="36d45-299">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="36d45-299">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="36d45-300">Nous allons ajouter le code suivant pour créer le `PredictionEngine` comme première ligne dans la méthode `Predict` :</span><span class="sxs-lookup"><span data-stu-id="36d45-300">Let's add the following code to create the `PredictionEngine` as the first line in the `Predict` Method:</span></span>

[!code-csharp[MakePredictionEngine](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#22 "Create the PredictionFunction")]
  
<span data-ttu-id="36d45-301">Ce tutoriel utilise une course test au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="36d45-301">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="36d45-302">Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="36d45-302">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="36d45-303">Ajoutez une course pour tester la prédiction de coût du modèle formé dans la méthode `Predict` en créant une instance de `TaxiTrip` :</span><span class="sxs-lookup"><span data-stu-id="36d45-303">Add a trip to test the trained model's prediction of cost in the `Predict` method by creating an instance of `TaxiTrip`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#23 "Create test data for single prediction")]

 <span data-ttu-id="36d45-304">Nous pouvons utiliser ces éléments pour prédire le prix basé sur une instance unique des données d’une course de taxi.</span><span class="sxs-lookup"><span data-stu-id="36d45-304">We can use that to predict the fare based on a single instance of the taxi trip data.</span></span> <span data-ttu-id="36d45-305">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="36d45-305">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="36d45-306">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="36d45-306">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="36d45-307">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="36d45-307">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="36d45-308">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="36d45-308">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#24 "Create a prediction of taxi fare")]

<span data-ttu-id="36d45-309">Pour afficher le prix prédit de la course spécifiée, ajoutez le code suivant à la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="36d45-309">To display the predicted fare of the specified trip, add the following code into the `Main` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#25 "Display the prediction.")]

<span data-ttu-id="36d45-310">Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.</span><span class="sxs-lookup"><span data-stu-id="36d45-310">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="36d45-311">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="36d45-311">Congratulations!</span></span> <span data-ttu-id="36d45-312">Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions.</span><span class="sxs-lookup"><span data-stu-id="36d45-312">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="36d45-313">Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).</span><span class="sxs-lookup"><span data-stu-id="36d45-313">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="36d45-314">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="36d45-314">Next steps</span></span>

<span data-ttu-id="36d45-315">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="36d45-315">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="36d45-316">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="36d45-316">Understand the problem</span></span>
> * <span data-ttu-id="36d45-317">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="36d45-317">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="36d45-318">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="36d45-318">Prepare and understand the data</span></span>
> * <span data-ttu-id="36d45-319">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="36d45-319">Create a learning pipeline</span></span>
> * <span data-ttu-id="36d45-320">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="36d45-320">Load and transform the data</span></span>
> * <span data-ttu-id="36d45-321">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="36d45-321">Choose a learning algorithm</span></span>
> * <span data-ttu-id="36d45-322">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-322">Train the model</span></span>
> * <span data-ttu-id="36d45-323">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="36d45-323">Evaluate the model</span></span>
> * <span data-ttu-id="36d45-324">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="36d45-324">Use the model for predictions</span></span>

<span data-ttu-id="36d45-325">Passez au tutoriel suivant pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="36d45-325">Advance to the next tutorial to learn more.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="36d45-326">Clustering Iris</span><span class="sxs-lookup"><span data-stu-id="36d45-326">Iris clustering</span></span>](iris-clustering.md)
