---
title: Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)
description: Découvrez comment utiliser ML.NET dans un scénario de régression.
author: aditidugar
ms.author: johalex
ms.date: 06/18/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 690e39dcbd02d81b8d4afe918a74795aa02f7fc6
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36314963"
---
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a><span data-ttu-id="95ce7-103">Tutoriel : Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)</span><span class="sxs-lookup"><span data-stu-id="95ce7-103">Tutorial: Use ML.NET to predict New York taxi fares (regression)</span></span>

> [!NOTE]
> <span data-ttu-id="95ce7-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="95ce7-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="95ce7-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="95ce7-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="95ce7-106">Ce tutoriel montre l’utilisation de ML.NET pour générer un [modèle de régression](../resources/glossary.md#regression) afin de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="95ce7-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting New York City taxi fares.</span></span>

<span data-ttu-id="95ce7-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="95ce7-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="95ce7-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="95ce7-108">Understand the problem</span></span>
> * <span data-ttu-id="95ce7-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="95ce7-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="95ce7-110">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-110">Prepare and understand the data</span></span>
> * <span data-ttu-id="95ce7-111">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="95ce7-112">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-112">Load and transform the data</span></span>
> * <span data-ttu-id="95ce7-113">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="95ce7-114">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-114">Train the model</span></span>
> * <span data-ttu-id="95ce7-115">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-115">Evaluate the model</span></span>
> * <span data-ttu-id="95ce7-116">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="95ce7-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95ce7-117">Prérequis</span><span class="sxs-lookup"><span data-stu-id="95ce7-117">Prerequisites</span></span>

* <span data-ttu-id="95ce7-118">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="95ce7-118">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="95ce7-119">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="95ce7-119">Understand the problem</span></span>

<span data-ttu-id="95ce7-120">Ce problème est centré autour de la **prédiction du prix d’une course de taxi à New York**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-120">This problem is centered around **predicting the fare of a taxi trip in New York City**.</span></span> <span data-ttu-id="95ce7-121">À première vue, ce prix semble dépendre simplement de la distance parcourue.</span><span class="sxs-lookup"><span data-stu-id="95ce7-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="95ce7-122">Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.</span><span class="sxs-lookup"><span data-stu-id="95ce7-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="95ce7-123">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="95ce7-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="95ce7-124">Pour prédire le prix de la course de taxi, vous sélectionnez d’abord la tâche d’apprentissage automatique appropriée.</span><span class="sxs-lookup"><span data-stu-id="95ce7-124">To predict the taxi fare, you first select the appropriate machine learning task.</span></span> <span data-ttu-id="95ce7-125">Vous devez prédire une valeur réelle (valeur double qui représente le prix) en fonction des autres facteurs du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="95ce7-125">You are looking to predict a real value (a double that represents price) based on the other factors in the dataset.</span></span> <span data-ttu-id="95ce7-126">Vous choisissez une tâche de [**régression**](../resources/glossary.md#regression).</span><span class="sxs-lookup"><span data-stu-id="95ce7-126">You choose a [**regression**](../resources/glossary.md#regression) task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="95ce7-127">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="95ce7-127">Create a console application</span></span>

1. <span data-ttu-id="95ce7-128">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="95ce7-128">Open Visual Studio 2017.</span></span> <span data-ttu-id="95ce7-129">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="95ce7-129">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="95ce7-130">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-130">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="95ce7-131">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-131">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="95ce7-132">Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-132">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

2. <span data-ttu-id="95ce7-133">Créez un répertoire nommé *Données* dans votre projet pour enregistrer les fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="95ce7-133">Create a directory named *Data* in your project to save the data set files:</span></span>

    <span data-ttu-id="95ce7-134">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-134">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="95ce7-135">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="95ce7-135">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="95ce7-136">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="95ce7-136">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="95ce7-137">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-137">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="95ce7-138">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-138">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="95ce7-139">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="95ce7-139">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="95ce7-140">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-140">Prepare and understand the data</span></span>

1. <span data-ttu-id="95ce7-141">Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="95ce7-141">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="95ce7-142">Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-142">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="95ce7-143">Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span><span class="sxs-lookup"><span data-stu-id="95ce7-143">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

2. <span data-ttu-id="95ce7-144">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-144">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="95ce7-145">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Toujours**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-145">Under **Advanced**, change the value of **Copy to Output Directory** to **Always**.</span></span>

3. <span data-ttu-id="95ce7-146">Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne.</span><span class="sxs-lookup"><span data-stu-id="95ce7-146">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="95ce7-147">Examinons chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="95ce7-147">Take a look at each of the columns.</span></span> <span data-ttu-id="95ce7-148">Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-148">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="95ce7-149">**L’étiquette** est l’identificateur de la colonne à prédire.</span><span class="sxs-lookup"><span data-stu-id="95ce7-149">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="95ce7-150">Les **fonctionnalités** identifiées servent à prédire l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="95ce7-150">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="95ce7-151">Le jeu de données fourni contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="95ce7-151">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="95ce7-152">**vendor_id :** l’ID du taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="95ce7-152">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="95ce7-153">**rate_code :** le type de tarif de la course de taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="95ce7-153">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="95ce7-154">**passenger_count :** le nombre de passagers embarqués est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="95ce7-154">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="95ce7-155">**trip_time_in_secs :** durée totale de la course.</span><span class="sxs-lookup"><span data-stu-id="95ce7-155">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="95ce7-156">Vous voulez prédire le prix de la course avant de l’effectuer.</span><span class="sxs-lookup"><span data-stu-id="95ce7-156">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="95ce7-157">À ce stade vous ne connaissez pas la durée de la course.</span><span class="sxs-lookup"><span data-stu-id="95ce7-157">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="95ce7-158">Par conséquent, la durée de la course n’est pas une fonctionnalité et vous devez exclure cette colonne du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-158">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="95ce7-159">**trip_distance :** la distance de la course est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="95ce7-159">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="95ce7-160">**payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="95ce7-160">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="95ce7-161">**fare_amount :** le prix total payé pour la course est l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="95ce7-161">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="95ce7-162">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="95ce7-162">Create data classes</span></span>

<span data-ttu-id="95ce7-163">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="95ce7-163">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="95ce7-164">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-164">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="95ce7-165">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*.</span><span class="sxs-lookup"><span data-stu-id="95ce7-165">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="95ce7-166">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-166">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="95ce7-167">Ajoutez les instructions `using` suivantes au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="95ce7-167">Add the following `using` statements to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="95ce7-168">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :</span><span class="sxs-lookup"><span data-stu-id="95ce7-168">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="95ce7-169">`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="95ce7-169">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="95ce7-170">Utilisez l’attribut [Colonne](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) pour spécifier les index des colonnes sources dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="95ce7-170">Use the [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="95ce7-171">La classe `TaxiTripFarePrediction` est utilisée pour représenter les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="95ce7-171">The `TaxiTripFarePrediction` class is used to represent predicted results.</span></span> <span data-ttu-id="95ce7-172">Elle a un champ de valeur flottante unique (`FareAmount`) avec un attribut `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) appliqué.</span><span class="sxs-lookup"><span data-stu-id="95ce7-172">It has a single float (`FareAmount`) field with a `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) attribute applied.</span></span> <span data-ttu-id="95ce7-173">La colonne **Score** est la colonne spéciale dans ML.NET.</span><span class="sxs-lookup"><span data-stu-id="95ce7-173">The **Score** column is the special column in ML.NET.</span></span> <span data-ttu-id="95ce7-174">Le modèle génère les valeurs prédites dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="95ce7-174">The model outputs predicted values into that column.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="95ce7-175">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-175">Define data and model paths</span></span>

<span data-ttu-id="95ce7-176">Revenez au fichier *Program.cs* et créez trois constantes globales pour contenir les chemins des fichiers avec des jeux de données et pour enregistrer le modèle :</span><span class="sxs-lookup"><span data-stu-id="95ce7-176">Go back to the *Program.cs* file and create three global constants to hold the paths to the files with data sets and to save the model:</span></span>

* <span data-ttu-id="95ce7-177">`_datapath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-177">`_datapath` has the path to the data set used to train the model.</span></span>
* <span data-ttu-id="95ce7-178">`_testdatapath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-178">`_testdatapath` has the path to the data set used to evaluate the model.</span></span>
* <span data-ttu-id="95ce7-179">`_modelpath` contient le chemin d’accès où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="95ce7-179">`_modelpath` has the path where the trained model is stored.</span></span>

<span data-ttu-id="95ce7-180">Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="95ce7-180">Add the following code to the line right above the `Main` method to specify those paths:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="95ce7-181">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-181">Create a learning pipeline</span></span>

<span data-ttu-id="95ce7-182">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="95ce7-182">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="95ce7-183">Dans `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-183">In `Main`, replace the `Console.WriteLine("Hello World!")` with the following code:</span></span>

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

<span data-ttu-id="95ce7-184">La méthode `Train` effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-184">The `Train` method trains the model.</span></span> <span data-ttu-id="95ce7-185">Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-185">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

<span data-ttu-id="95ce7-186">Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-186">The learning pipeline loads all of the data and algorithms necessary to train the model.</span></span> <span data-ttu-id="95ce7-187">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-187">Add the following code into the `Train` method:</span></span>

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-data"></a><span data-ttu-id="95ce7-188">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-188">Load and transform data</span></span>

<span data-ttu-id="95ce7-189">La première étape du pipeline d’apprentissage est de charger les données du jeu de données d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="95ce7-189">The first step that the learning pipeline performs is loading data from the training data set.</span></span> <span data-ttu-id="95ce7-190">Dans notre cas, le jeu de données d’apprentissage est stocké dans le fichier texte avec un chemin défini par la constante `_datapath`.</span><span class="sxs-lookup"><span data-stu-id="95ce7-190">In our case, training data set is stored in the text file with a path defined by the `_datapath` constant.</span></span> <span data-ttu-id="95ce7-191">Ce fichier contient l’en-tête avec les noms de colonne, la première ligne doit donc être ignorée pendant le chargement des données.</span><span class="sxs-lookup"><span data-stu-id="95ce7-191">That file contains the header with the column names, so the first row should be ignored while loading data.</span></span> <span data-ttu-id="95ce7-192">Dans le fichier, les colonnes sont séparées par une virgule (« , »).</span><span class="sxs-lookup"><span data-stu-id="95ce7-192">Columns in the file are separated by the comma (",").</span></span> <span data-ttu-id="95ce7-193">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-193">Add the following code into the `Train` method:</span></span>

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(useHeader: true, separator: ','));
```

<span data-ttu-id="95ce7-194">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="95ce7-194">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="95ce7-195">Une fois que le modèle est formé et évalué, les valeurs de la colonne **Étiquette** sont considérées comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="95ce7-195">When the model is trained and evaluated, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="95ce7-196">Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-196">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="95ce7-197">Pour ce faire, utilisez <xref:Microsoft.ML.Transforms.ColumnCopier> et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-197">To do that, use <xref:Microsoft.ML.Transforms.ColumnCopier> and add the following code:</span></span>

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

<span data-ttu-id="95ce7-198">L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques**, car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres.</span><span class="sxs-lookup"><span data-stu-id="95ce7-198">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="95ce7-199">Pour ce faire, utilisez <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer>, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-199">To do that, use <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer>, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

<span data-ttu-id="95ce7-200">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation <xref:Microsoft.ML.Transforms.ColumnConcatenator>.</span><span class="sxs-lookup"><span data-stu-id="95ce7-200">The last step in data preparation combines all of the feature columns into the **Features** column using the <xref:Microsoft.ML.Transforms.ColumnConcatenator> transformation class.</span></span> <span data-ttu-id="95ce7-201">Cette étape est nécessaire, car un apprenant traite uniquement les fonctionnalités de la colonne **Fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-201">This step is necessary as a learner processes only features from the **Features** column.</span></span> <span data-ttu-id="95ce7-202">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-202">Add the following code:</span></span>

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

<span data-ttu-id="95ce7-203">Notez que la colonne `TripTime`, qui correspond à la colonne `trip_time_in_secs` dans le fichier de jeu de données, n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="95ce7-203">Notice that the `TripTime` column, which corresponds to the `trip_time_in_secs` column in the data set file, isn't included.</span></span> <span data-ttu-id="95ce7-204">Vous avez déterminé que cette fonctionnalité de prévision n’est pas utile.</span><span class="sxs-lookup"><span data-stu-id="95ce7-204">You already determined that it isn't a useful prediction feature.</span></span>

> [!NOTE]
> <span data-ttu-id="95ce7-205">Ces étapes doivent être ajoutées au pipeline dans l’ordre spécifié ci-dessus pour garantir la bonne exécution.</span><span class="sxs-lookup"><span data-stu-id="95ce7-205">These steps must be added to the pipeline in the order specified above for successful execution.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="95ce7-206">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-206">Choose a learning algorithm</span></span>

<span data-ttu-id="95ce7-207">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="95ce7-207">After adding the data to the pipeline and transforming it into the correct input format, you select a learning algorithm (**learner**).</span></span> <span data-ttu-id="95ce7-208">L’apprenant effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-208">The learner trains the model.</span></span> <span data-ttu-id="95ce7-209">Vous avez choisi une **tâche de régression** pour ce problème, vous ajoutez donc un apprenant <xref:Microsoft.ML.Trainers.FastTreeRegressor>, qui est un des apprenants de régression fournis par ML.NET.</span><span class="sxs-lookup"><span data-stu-id="95ce7-209">You chose a **regression task** for this problem, so you add a <xref:Microsoft.ML.Trainers.FastTreeRegressor> learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="95ce7-210">L’apprenant <xref:Microsoft.ML.Trainers.FastTreeRegressor> utilise le boosting de gradient.</span><span class="sxs-lookup"><span data-stu-id="95ce7-210"><xref:Microsoft.ML.Trainers.FastTreeRegressor> learner utilizes gradient boosting.</span></span> <span data-ttu-id="95ce7-211">Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="95ce7-211">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="95ce7-212">Il génère chaque arbre de régression étape par étape.</span><span class="sxs-lookup"><span data-stu-id="95ce7-212">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="95ce7-213">Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine.</span><span class="sxs-lookup"><span data-stu-id="95ce7-213">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="95ce7-214">Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces.</span><span class="sxs-lookup"><span data-stu-id="95ce7-214">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="95ce7-215">Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span><span class="sxs-lookup"><span data-stu-id="95ce7-215">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="95ce7-216">Ajoutez le code suivant dans la méthode `Train` après le code de traitement des données ajouté à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="95ce7-216">Add the following code into the `Train` method following the data processing code added in the previous step:</span></span>

```csharp
pipeline.Add(new FastTreeRegressor());
```

<span data-ttu-id="95ce7-217">Vous avez ajouté toutes les étapes précédentes au pipeline en tant qu’instructions individuelles, mais C# propose une syntaxe d’initialisation de collection pratique qui facilite la création et l’initialisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="95ce7-217">You added all the preceding steps to the pipeline as individual statements, but C# has a handy collection initialization syntax that makes it simpler to create and initialize the pipeline.</span></span> <span data-ttu-id="95ce7-218">Remplacez le code que vous avez ajouté à la méthode `Train` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-218">Replace the code you added so far to the `Train` method with the following code:</span></span>

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a><span data-ttu-id="95ce7-219">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-219">Train the model</span></span>

<span data-ttu-id="95ce7-220">La dernière étape consiste à effectuer l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-220">The final step is to train the model.</span></span> <span data-ttu-id="95ce7-221">À ce stade, rien dans le pipeline n’a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="95ce7-221">Until this point, nothing in the pipeline has been executed.</span></span> <span data-ttu-id="95ce7-222">La méthode `pipeline.Train<TInput, TOutput>` génère le modèle qui prend une instance du type `TInput` et génère une instance du type `TOutput`.</span><span class="sxs-lookup"><span data-stu-id="95ce7-222">The `pipeline.Train<TInput, TOutput>` method produces the model that takes in an instance of the `TInput` type and outputs an instance of the `TOutput` type.</span></span> <span data-ttu-id="95ce7-223">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-223">Add the following code into the `Train` method:</span></span>

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

<span data-ttu-id="95ce7-224">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="95ce7-224">And that's it!</span></span> <span data-ttu-id="95ce7-225">Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="95ce7-225">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="95ce7-226">Nous allons maintenant essayer de déterminer la précision du modèle et découvrir comment l’utiliser pour prédire les valeurs des tarifs de taxi.</span><span class="sxs-lookup"><span data-stu-id="95ce7-226">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="95ce7-227">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-227">Save the model</span></span>

<span data-ttu-id="95ce7-228">Avant de passer à l’étape suivante, enregistrez le modèle dans un fichier .zip, en ajoutant le code suivant à la fin de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-228">Before you go onto the next step, save the model to a .zip file by adding the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

<span data-ttu-id="95ce7-229">L’ajout de l’instruction `await` à l’appel `model.WriteAsync` signifie que la méthode `Train` doit être remplacée par une méthode asynchrone qui retourne une tâche.</span><span class="sxs-lookup"><span data-stu-id="95ce7-229">Adding the `await` statement to the `model.WriteAsync` call means that the `Train` method must be changed to an async method that returns a task.</span></span> <span data-ttu-id="95ce7-230">Modifiez la signature de `Train`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-230">Modify the signature of `Train` as shown in the following code:</span></span>

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

<span data-ttu-id="95ce7-231">La modification du type de retour de la méthode `Train` signifie que vous devez ajouter un élément `await` au code qui appelle `Train` dans la méthode `Main`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-231">Changing the return type of the `Train` method means you have to add an `await` to the code that calls `Train` in the `Main` method as shown in the following code:</span></span>

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

<span data-ttu-id="95ce7-232">L’utilisation de l’élément `await` dans la méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-232">Using `await` in the `Main` method means the `Main` method must have the `async` modifier and return a `Task`:</span></span>

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

<span data-ttu-id="95ce7-233">Vous devez également ajouter l’instruction `using` suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="95ce7-233">You also need to add the following `using` statement at the top of the file:</span></span>

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

<span data-ttu-id="95ce7-234">Comme la méthode `async Main` est la fonctionnalité ajoutée dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version de langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="95ce7-234">Because the `async Main` method is the feature added in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span> <span data-ttu-id="95ce7-235">Pour ce faire, cliquez avec le bouton droit sur le nœud de projet dans **l’Explorateur de solutions** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-235">To do that, right-click the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="95ce7-236">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-236">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="95ce7-237">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="95ce7-237">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="95ce7-238">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-238">Select the **OK** button.</span></span>

## <a name="evaluate-the-model"></a><span data-ttu-id="95ce7-239">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-239">Evaluate the model</span></span>

<span data-ttu-id="95ce7-240">L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="95ce7-240">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="95ce7-241">Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="95ce7-241">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="95ce7-242">Pour ce faire, vous pouvez fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme expliqué dans ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="95ce7-242">One way to do this is to split the data into train and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="95ce7-243">Maintenant que vous avez formé le modèle avec les données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="95ce7-243">Now that you've trained the model on the train data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="95ce7-244">Revenez à la méthode `Main` et ajoutez le code suivant sous l’appel à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-244">Go back to the `Main` method and add the following code beneath the call to the `Train`method:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

<span data-ttu-id="95ce7-245">La méthode `Evaluate` évalue le modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-245">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="95ce7-246">Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-246">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

<span data-ttu-id="95ce7-247">Ajoutez le code suivant dans la méthode `Evaluate` pour configurer le chargement des données de test :</span><span class="sxs-lookup"><span data-stu-id="95ce7-247">Add the following code into the `Evaluate` method to setup loading of the test data:</span></span>

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

<span data-ttu-id="95ce7-248">Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="95ce7-248">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

<span data-ttu-id="95ce7-249">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression.</span><span class="sxs-lookup"><span data-stu-id="95ce7-249">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="95ce7-250">Plus sa valeur est faible, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="95ce7-250">The lower it is, the better the model is.</span></span> <span data-ttu-id="95ce7-251">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :</span><span class="sxs-lookup"><span data-stu-id="95ce7-251">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

<span data-ttu-id="95ce7-252">[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression.</span><span class="sxs-lookup"><span data-stu-id="95ce7-252">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="95ce7-253">RSquared prend des valeurs entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="95ce7-253">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="95ce7-254">Plus sa valeur est proche de 1, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="95ce7-254">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="95ce7-255">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :</span><span class="sxs-lookup"><span data-stu-id="95ce7-255">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="95ce7-256">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="95ce7-256">Use the model for predictions</span></span>

<span data-ttu-id="95ce7-257">Ensuite, créez une classe afin d’héberger les scénarios de test à utiliser pour vérifier le bon fonctionnement du modèle :</span><span class="sxs-lookup"><span data-stu-id="95ce7-257">Next, create a class to house test scenarios that you can use to make sure the model is working correctly:</span></span>

1. <span data-ttu-id="95ce7-258">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-258">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="95ce7-259">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestTrips.cs*.</span><span class="sxs-lookup"><span data-stu-id="95ce7-259">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestTrips.cs*.</span></span> <span data-ttu-id="95ce7-260">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="95ce7-260">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="95ce7-261">Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="95ce7-261">Modify the class to be static like in the following example:</span></span>

   [!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

<span data-ttu-id="95ce7-262">Ce tutoriel utilise une course test au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="95ce7-262">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="95ce7-263">Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="95ce7-263">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="95ce7-264">Ajoutez le code suivant à la classe `TestTrips` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-264">Add the following code into the `TestTrips` class:</span></span>

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

<span data-ttu-id="95ce7-265">Le tarif réel de cette course est 29,5.</span><span class="sxs-lookup"><span data-stu-id="95ce7-265">This trip's actual fare is 29.5.</span></span> <span data-ttu-id="95ce7-266">Utilisez 0 comme espace réservé, car le modèle prédit le prix.</span><span class="sxs-lookup"><span data-stu-id="95ce7-266">Use 0 as a placeholder, as the model will predict the fare.</span></span>

<span data-ttu-id="95ce7-267">Pour prévoir le prix de la course spécifiée, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="95ce7-267">To predict the fare of the specified trip, go back to the *Program.cs* file and add the following code into the `Main` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

<span data-ttu-id="95ce7-268">Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.</span><span class="sxs-lookup"><span data-stu-id="95ce7-268">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="95ce7-269">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="95ce7-269">Congratulations!</span></span> <span data-ttu-id="95ce7-270">Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions.</span><span class="sxs-lookup"><span data-stu-id="95ce7-270">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="95ce7-271">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).</span><span class="sxs-lookup"><span data-stu-id="95ce7-271">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="95ce7-272">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="95ce7-272">Next steps</span></span>

<span data-ttu-id="95ce7-273">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="95ce7-273">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="95ce7-274">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="95ce7-274">Understand the problem</span></span>
> * <span data-ttu-id="95ce7-275">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="95ce7-275">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="95ce7-276">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-276">Prepare and understand the data</span></span>
> * <span data-ttu-id="95ce7-277">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-277">Create a learning pipeline</span></span>
> * <span data-ttu-id="95ce7-278">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="95ce7-278">Load and transform the data</span></span>
> * <span data-ttu-id="95ce7-279">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="95ce7-279">Choose a learning algorithm</span></span>
> * <span data-ttu-id="95ce7-280">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-280">Train the model</span></span>
> * <span data-ttu-id="95ce7-281">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="95ce7-281">Evaluate the model</span></span>
> * <span data-ttu-id="95ce7-282">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="95ce7-282">Use the model for predictions</span></span>

<span data-ttu-id="95ce7-283">Consultez notre référentiel GitHub pour continuer l’apprentissage et obtenir d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="95ce7-283">Check out our GitHub repository to continue learning and find more samples.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="95ce7-284">Référentiel GitHub dotnet/machinelearning</span><span class="sxs-lookup"><span data-stu-id="95ce7-284">dotnet/machinelearning GitHub repository</span></span>](https://github.com/dotnet/machinelearning/)
