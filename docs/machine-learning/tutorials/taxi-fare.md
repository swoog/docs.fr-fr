---
title: Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)
description: Découvrez comment utiliser ML.NET dans un scénario de régression.
author: aditidugar
ms.author: johalex
ms.date: 07/02/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: bfae97d65ec192e9289841c82d84807b4937b09a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183813"
---
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a><span data-ttu-id="51f9c-103">Tutoriel : Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)</span><span class="sxs-lookup"><span data-stu-id="51f9c-103">Tutorial: Use ML.NET to predict New York taxi fares (regression)</span></span>

> [!NOTE]
> <span data-ttu-id="51f9c-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="51f9c-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="51f9c-105">Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="51f9c-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="51f9c-106">Ce tutoriel montre l’utilisation de ML.NET pour générer un [modèle de régression](../resources/glossary.md#regression) afin de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="51f9c-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting New York City taxi fares.</span></span>

<span data-ttu-id="51f9c-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="51f9c-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="51f9c-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="51f9c-108">Understand the problem</span></span>
> * <span data-ttu-id="51f9c-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="51f9c-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="51f9c-110">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-110">Prepare and understand the data</span></span>
> * <span data-ttu-id="51f9c-111">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="51f9c-112">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-112">Load and transform the data</span></span>
> * <span data-ttu-id="51f9c-113">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="51f9c-114">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-114">Train the model</span></span>
> * <span data-ttu-id="51f9c-115">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-115">Evaluate the model</span></span>
> * <span data-ttu-id="51f9c-116">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="51f9c-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="51f9c-117">Prérequis</span><span class="sxs-lookup"><span data-stu-id="51f9c-117">Prerequisites</span></span>

* <span data-ttu-id="51f9c-118">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="51f9c-118">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="51f9c-119">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="51f9c-119">Understand the problem</span></span>

<span data-ttu-id="51f9c-120">Ce problème consiste à prédire le prix d’une course de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="51f9c-120">This problem is about predicting the fare of a taxi trip in New York City.</span></span> <span data-ttu-id="51f9c-121">À première vue, ce prix semble dépendre simplement de la distance parcourue.</span><span class="sxs-lookup"><span data-stu-id="51f9c-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="51f9c-122">Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.</span><span class="sxs-lookup"><span data-stu-id="51f9c-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="51f9c-123">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="51f9c-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="51f9c-124">Vous souhaitez prédire le prix, qui est une valeur réelle, en fonction des autres facteurs du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="51f9c-124">You want to predict the price value, which is a real value, based on the other factors in the data set.</span></span> <span data-ttu-id="51f9c-125">Pour ce faire, choisissez une tâche d’apprentissage automatique par [régression](../resources/glossary.md#regression).</span><span class="sxs-lookup"><span data-stu-id="51f9c-125">To do that you choose a [regression](../resources/glossary.md#regression) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="51f9c-126">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="51f9c-126">Create a console application</span></span>

1. <span data-ttu-id="51f9c-127">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="51f9c-127">Open Visual Studio 2017.</span></span> <span data-ttu-id="51f9c-128">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="51f9c-128">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="51f9c-129">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-129">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="51f9c-130">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-130">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="51f9c-131">Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-131">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

1. <span data-ttu-id="51f9c-132">Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :</span><span class="sxs-lookup"><span data-stu-id="51f9c-132">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="51f9c-133">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-133">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="51f9c-134">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="51f9c-134">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="51f9c-135">Installez le package NuGet **Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="51f9c-135">Install the **Microsoft.ML** NuGet Package:</span></span>

    <span data-ttu-id="51f9c-136">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-136">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="51f9c-137">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-137">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="51f9c-138">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="51f9c-138">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="51f9c-139">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-139">Prepare and understand the data</span></span>

1. <span data-ttu-id="51f9c-140">Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="51f9c-140">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="51f9c-141">Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-141">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="51f9c-142">Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span><span class="sxs-lookup"><span data-stu-id="51f9c-142">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

1. <span data-ttu-id="51f9c-143">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-143">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="51f9c-144">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-144">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

1. <span data-ttu-id="51f9c-145">Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne.</span><span class="sxs-lookup"><span data-stu-id="51f9c-145">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="51f9c-146">Examinons chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="51f9c-146">Take a look at each of the columns.</span></span> <span data-ttu-id="51f9c-147">Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-147">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="51f9c-148">**L’étiquette** est l’identificateur de la colonne à prédire.</span><span class="sxs-lookup"><span data-stu-id="51f9c-148">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="51f9c-149">Les **fonctionnalités** identifiées servent à prédire l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="51f9c-149">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="51f9c-150">Le jeu de données fourni contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="51f9c-150">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="51f9c-151">**vendor_id :** l’ID du taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="51f9c-151">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="51f9c-152">**rate_code :** le type de tarif de la course de taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="51f9c-152">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="51f9c-153">**passenger_count :** le nombre de passagers embarqués est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="51f9c-153">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="51f9c-154">**trip_time_in_secs :** durée totale de la course.</span><span class="sxs-lookup"><span data-stu-id="51f9c-154">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="51f9c-155">Vous voulez prédire le prix de la course avant de l’effectuer.</span><span class="sxs-lookup"><span data-stu-id="51f9c-155">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="51f9c-156">À ce stade vous ne connaissez pas la durée de la course.</span><span class="sxs-lookup"><span data-stu-id="51f9c-156">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="51f9c-157">Par conséquent, la durée de la course n’est pas une fonctionnalité et vous devez exclure cette colonne du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-157">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="51f9c-158">**trip_distance :** la distance de la course est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="51f9c-158">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="51f9c-159">**payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="51f9c-159">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="51f9c-160">**fare_amount :** le prix total payé pour la course est l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="51f9c-160">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="51f9c-161">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="51f9c-161">Create data classes</span></span>

<span data-ttu-id="51f9c-162">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="51f9c-162">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="51f9c-163">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-163">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="51f9c-164">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*.</span><span class="sxs-lookup"><span data-stu-id="51f9c-164">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="51f9c-165">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-165">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="51f9c-166">Ajoutez les directives `using` suivantes au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="51f9c-166">Add the following `using` directives to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="51f9c-167">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :</span><span class="sxs-lookup"><span data-stu-id="51f9c-167">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="51f9c-168">`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="51f9c-168">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="51f9c-169">Utilisez l’attribut [Colonne](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) pour spécifier les index des colonnes sources dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="51f9c-169">Use the [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="51f9c-170">La classe `TaxiTripFarePrediction` représente les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="51f9c-170">The `TaxiTripFarePrediction` class represents predicted results.</span></span> <span data-ttu-id="51f9c-171">Elle comporte un seul champ float, `FareAmount`, avec un attribut `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) appliqué.</span><span class="sxs-lookup"><span data-stu-id="51f9c-171">It has a single float field, `FareAmount`, with a `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) attribute applied.</span></span> <span data-ttu-id="51f9c-172">Dans le cas de la tâche de régression, la colonne **Score** contient les valeurs d’étiquette prédites.</span><span class="sxs-lookup"><span data-stu-id="51f9c-172">In case of the regression task the **Score** column contains predicted label values.</span></span>

> [!NOTE]
> <span data-ttu-id="51f9c-173">Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="51f9c-173">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="51f9c-174">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-174">Define data and model paths</span></span>

<span data-ttu-id="51f9c-175">Revenez au fichier *Program.cs* et ajoutez trois champs pour contenir les chemins des fichiers avec des jeux de données et le fichier pour enregistrer le modèle :</span><span class="sxs-lookup"><span data-stu-id="51f9c-175">Go back to the *Program.cs* file and add three fields to hold the paths to the files with data sets and the file to save the model:</span></span>

* <span data-ttu-id="51f9c-176">`_datapath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-176">`_datapath` contains the path to the file with the data set used to train the model.</span></span>
* <span data-ttu-id="51f9c-177">`_testdatapath` contient le chemin du fichier avec le jeu de données utilisé pour l’évaluation du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-177">`_testdatapath` contains the path to the file with the data set used to evaluate the model.</span></span>
* <span data-ttu-id="51f9c-178">`_modelpath` contient le chemin du fichier où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="51f9c-178">`_modelpath` contains the path to the file where the trained model is stored.</span></span>

<span data-ttu-id="51f9c-179">Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="51f9c-179">Add the following code right above the `Main` method to specify those paths:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="51f9c-180">Pour compiler le code précédent, ajoutez les directives `using` suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="51f9c-180">To make the preceding code compile, add the following `using` directives at the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsingsForPaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Using statements for path definitions")]

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="51f9c-181">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-181">Create a learning pipeline</span></span>

<span data-ttu-id="51f9c-182">Ajoutez les directives `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="51f9c-182">Add the following additional `using` directives to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="51f9c-183">Dans la méthode `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-183">In the `Main` method, replace the `Console.WriteLine("Hello World!")` with the following code:</span></span>

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

<span data-ttu-id="51f9c-184">La méthode `Train` effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-184">The `Train` method trains the model.</span></span> <span data-ttu-id="51f9c-185">Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-185">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

<span data-ttu-id="51f9c-186">Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-186">The learning pipeline loads all of the data and algorithms necessary to train the model.</span></span> <span data-ttu-id="51f9c-187">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-187">Add the following code into the `Train` method:</span></span>

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-data"></a><span data-ttu-id="51f9c-188">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-188">Load and transform data</span></span>

<span data-ttu-id="51f9c-189">La première étape à effectuer consiste à charger les données du jeu de données d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="51f9c-189">The first step to perform is to load data from the training data set.</span></span> <span data-ttu-id="51f9c-190">Dans notre cas, le jeu de données d’apprentissage est stocké dans le fichier texte avec un chemin défini par le champ `_datapath`.</span><span class="sxs-lookup"><span data-stu-id="51f9c-190">In our case, training data set is stored in the text file with a path defined by the `_datapath` field.</span></span> <span data-ttu-id="51f9c-191">Ce fichier contient l’en-tête avec les noms de colonnes. La première ligne doit donc être ignorée durant le chargement des données.</span><span class="sxs-lookup"><span data-stu-id="51f9c-191">That file has the header with the column names, so the first row should be ignored while loading data.</span></span> <span data-ttu-id="51f9c-192">Dans le fichier, les colonnes sont séparées par une virgule (« , »).</span><span class="sxs-lookup"><span data-stu-id="51f9c-192">Columns in the file are separated by the comma (",").</span></span> <span data-ttu-id="51f9c-193">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-193">Add the following code into the `Train` method:</span></span>

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(useHeader: true, separator: ','));
```

<span data-ttu-id="51f9c-194">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="51f9c-194">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="51f9c-195">Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="51f9c-195">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="51f9c-196">Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-196">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="51f9c-197">Pour ce faire, utilisez <xref:Microsoft.ML.Legacy.Transforms.ColumnCopier> et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-197">To do that, use <xref:Microsoft.ML.Legacy.Transforms.ColumnCopier> and add the following code:</span></span>

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

<span data-ttu-id="51f9c-198">L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques**, car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres.</span><span class="sxs-lookup"><span data-stu-id="51f9c-198">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="51f9c-199">Pour ce faire, utilisez <xref:Microsoft.ML.Legacy.Transforms.CategoricalOneHotVectorizer>, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-199">To do that, use <xref:Microsoft.ML.Legacy.Transforms.CategoricalOneHotVectorizer>, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

<span data-ttu-id="51f9c-200">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator>.</span><span class="sxs-lookup"><span data-stu-id="51f9c-200">The last step in data preparation combines all of the feature columns into the **Features** column using the <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator> transformation class.</span></span> <span data-ttu-id="51f9c-201">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-201">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="51f9c-202">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-202">Add the following code:</span></span>

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

<span data-ttu-id="51f9c-203">Notez que la colonne `TripTime`, qui correspond à la colonne `trip_time_in_secs` dans le fichier de jeu de données, n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="51f9c-203">Notice that the `TripTime` column, which corresponds to the `trip_time_in_secs` column in the data set file, isn't included.</span></span> <span data-ttu-id="51f9c-204">Vous avez déterminé que cette fonctionnalité de prévision n’est pas utile.</span><span class="sxs-lookup"><span data-stu-id="51f9c-204">You already determined that it isn't a useful prediction feature.</span></span>

> [!NOTE]
> <span data-ttu-id="51f9c-205">Ces étapes doivent être ajoutées au pipeline dans l’ordre spécifié ci-dessus pour garantir la bonne exécution.</span><span class="sxs-lookup"><span data-stu-id="51f9c-205">These steps must be added to the pipeline in the order specified above for successful execution.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="51f9c-206">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-206">Choose a learning algorithm</span></span>

<span data-ttu-id="51f9c-207">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="51f9c-207">After adding the data to the pipeline and transforming it into the correct input format, you select a learning algorithm (**learner**).</span></span> <span data-ttu-id="51f9c-208">L’apprenant effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-208">The learner trains the model.</span></span> <span data-ttu-id="51f9c-209">Vous avez choisi une tâche de **régression** pour ce problème. Vous utilisez donc un apprenant <xref:Microsoft.ML.Legacy.Trainers.FastTreeRegressor>, qui est l’un des apprenants de régression fournis par ML.NET.</span><span class="sxs-lookup"><span data-stu-id="51f9c-209">You chose a **regression** task for this problem, so you use a <xref:Microsoft.ML.Legacy.Trainers.FastTreeRegressor> learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="51f9c-210">L’apprenant <xref:Microsoft.ML.Legacy.Trainers.FastTreeRegressor> utilise le boosting de gradient.</span><span class="sxs-lookup"><span data-stu-id="51f9c-210"><xref:Microsoft.ML.Legacy.Trainers.FastTreeRegressor> learner utilizes gradient boosting.</span></span> <span data-ttu-id="51f9c-211">Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="51f9c-211">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="51f9c-212">Il génère chaque arbre de régression étape par étape.</span><span class="sxs-lookup"><span data-stu-id="51f9c-212">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="51f9c-213">Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine.</span><span class="sxs-lookup"><span data-stu-id="51f9c-213">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="51f9c-214">Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces.</span><span class="sxs-lookup"><span data-stu-id="51f9c-214">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="51f9c-215">Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span><span class="sxs-lookup"><span data-stu-id="51f9c-215">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="51f9c-216">Ajoutez le code suivant dans la méthode `Train` après le code de traitement des données ajouté à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="51f9c-216">Add the following code into the `Train` method following the data processing code added in the previous step:</span></span>

```csharp
pipeline.Add(new FastTreeRegressor());
```

<span data-ttu-id="51f9c-217">Vous avez ajouté toutes les étapes précédentes au pipeline en tant qu’instructions individuelles, mais C# propose une syntaxe d’initialisation de collection pratique qui facilite la création et l’initialisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="51f9c-217">You added all the preceding steps to the pipeline as individual statements, but C# has a handy collection initialization syntax that makes it simpler to create and initialize the pipeline.</span></span> <span data-ttu-id="51f9c-218">Remplacez le code que vous avez ajouté à la méthode `Train` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-218">Replace the code you added so far to the `Train` method with the following code:</span></span>

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a><span data-ttu-id="51f9c-219">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-219">Train the model</span></span>

<span data-ttu-id="51f9c-220">La dernière étape consiste à effectuer l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-220">The final step is to train the model.</span></span> <span data-ttu-id="51f9c-221">À ce stade, rien dans le pipeline n’a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="51f9c-221">Until this point, nothing in the pipeline has been executed.</span></span> <span data-ttu-id="51f9c-222">La méthode `pipeline.Train<TInput, TOutput>` génère le modèle qui prend une instance du type `TInput` et génère une instance du type `TOutput`.</span><span class="sxs-lookup"><span data-stu-id="51f9c-222">The `pipeline.Train<TInput, TOutput>` method produces the model that takes in an instance of the `TInput` type and outputs an instance of the `TOutput` type.</span></span> <span data-ttu-id="51f9c-223">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-223">Add the following code into the `Train` method:</span></span>

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

<span data-ttu-id="51f9c-224">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="51f9c-224">And that's it!</span></span> <span data-ttu-id="51f9c-225">Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="51f9c-225">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="51f9c-226">Nous allons maintenant essayer de déterminer la précision du modèle et découvrir comment l’utiliser pour prédire les valeurs des tarifs de taxi.</span><span class="sxs-lookup"><span data-stu-id="51f9c-226">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="51f9c-227">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-227">Save the model</span></span>

<span data-ttu-id="51f9c-228">À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="51f9c-228">At this point, you have a model that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="51f9c-229">Pour enregistrer le modèle dans un fichier .zip, ajoutez le code suivant à la fin de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-229">To save the model to a .zip file, add the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

<span data-ttu-id="51f9c-230">L’ajout de l’instruction `await` à l’appel `model.WriteAsync` signifie que la méthode `Train` doit être remplacée par une méthode asynchrone qui retourne une tâche.</span><span class="sxs-lookup"><span data-stu-id="51f9c-230">Adding the `await` statement to the `model.WriteAsync` call means that the `Train` method must be changed to an async method that returns a task.</span></span> <span data-ttu-id="51f9c-231">Modifiez la signature de `Train`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-231">Modify the signature of `Train` as shown in the following code:</span></span>

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

<span data-ttu-id="51f9c-232">La modification du type de retour de la méthode `Train` signifie que vous devez ajouter un élément `await` au code qui appelle `Train` dans la méthode `Main`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-232">Changing the return type of the `Train` method means you have to add an `await` to the code that calls `Train` in the `Main` method as shown in the following code:</span></span>

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

<span data-ttu-id="51f9c-233">L’utilisation de l’élément `await` dans la méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-233">Using `await` in the `Main` method means the `Main` method must have the `async` modifier and return a `Task`:</span></span>

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

<span data-ttu-id="51f9c-234">Vous devez également ajouter la directive `using` suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="51f9c-234">You also need to add the following `using` directive at the top of the file:</span></span>

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

<span data-ttu-id="51f9c-235">Comme la méthode `async Main` est la fonctionnalité ajoutée dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version de langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="51f9c-235">Because the `async Main` method is the feature added in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span> <span data-ttu-id="51f9c-236">Pour ce faire, cliquez avec le bouton droit sur le nœud de projet dans **l’Explorateur de solutions** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-236">To do that, right-click the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="51f9c-237">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-237">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="51f9c-238">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="51f9c-238">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="51f9c-239">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-239">Select the **OK** button.</span></span>

## <a name="evaluate-the-model"></a><span data-ttu-id="51f9c-240">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-240">Evaluate the model</span></span>

<span data-ttu-id="51f9c-241">L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="51f9c-241">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="51f9c-242">Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="51f9c-242">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="51f9c-243">Pour ce faire, vous pouvez, par exemple, fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme indiqué dans ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="51f9c-243">One way to do this is to split the data into training and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="51f9c-244">Une fois que vous avez formé le modèle à l’aide des données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="51f9c-244">Now that you've trained the model on the training data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="51f9c-245">Revenez à la méthode `Main` et ajoutez le code suivant sous l’appel à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-245">Go back to the `Main` method and add the following code beneath the call to the `Train`method:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

<span data-ttu-id="51f9c-246">La méthode `Evaluate` évalue le modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-246">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="51f9c-247">Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-247">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

<span data-ttu-id="51f9c-248">Ajoutez le code suivant dans la méthode `Evaluate` pour configurer le chargement des données de test :</span><span class="sxs-lookup"><span data-stu-id="51f9c-248">Add the following code into the `Evaluate` method to setup loading of the test data:</span></span>

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

<span data-ttu-id="51f9c-249">Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="51f9c-249">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

<span data-ttu-id="51f9c-250">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression.</span><span class="sxs-lookup"><span data-stu-id="51f9c-250">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="51f9c-251">Plus sa valeur est faible, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="51f9c-251">The lower it is, the better the model is.</span></span> <span data-ttu-id="51f9c-252">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :</span><span class="sxs-lookup"><span data-stu-id="51f9c-252">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

<span data-ttu-id="51f9c-253">[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression.</span><span class="sxs-lookup"><span data-stu-id="51f9c-253">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="51f9c-254">RSquared prend des valeurs entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="51f9c-254">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="51f9c-255">Plus sa valeur est proche de 1, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="51f9c-255">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="51f9c-256">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :</span><span class="sxs-lookup"><span data-stu-id="51f9c-256">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="51f9c-257">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="51f9c-257">Use the model for predictions</span></span>

<span data-ttu-id="51f9c-258">Créez une classe pour héberger les instances de données de test :</span><span class="sxs-lookup"><span data-stu-id="51f9c-258">Create a class to house test data instances:</span></span>

1. <span data-ttu-id="51f9c-259">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-259">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="51f9c-260">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestTrips.cs*.</span><span class="sxs-lookup"><span data-stu-id="51f9c-260">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestTrips.cs*.</span></span> <span data-ttu-id="51f9c-261">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="51f9c-261">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="51f9c-262">Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="51f9c-262">Modify the class to be static like in the following example:</span></span>

   [!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

<span data-ttu-id="51f9c-263">Ce tutoriel utilise une course test au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="51f9c-263">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="51f9c-264">Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="51f9c-264">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="51f9c-265">Ajoutez le code suivant à la classe `TestTrips` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-265">Add the following code into the `TestTrips` class:</span></span>

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

<span data-ttu-id="51f9c-266">Le tarif réel de cette course est 29,5.</span><span class="sxs-lookup"><span data-stu-id="51f9c-266">This trip's actual fare is 29.5.</span></span> <span data-ttu-id="51f9c-267">Utilisez 0 comme espace réservé, car le modèle prédit le prix.</span><span class="sxs-lookup"><span data-stu-id="51f9c-267">Use 0 as a placeholder, as the model will predict the fare.</span></span>

<span data-ttu-id="51f9c-268">Pour prévoir le prix de la course spécifiée, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="51f9c-268">To predict the fare of the specified trip, go back to the *Program.cs* file and add the following code into the `Main` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

<span data-ttu-id="51f9c-269">Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.</span><span class="sxs-lookup"><span data-stu-id="51f9c-269">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="51f9c-270">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="51f9c-270">Congratulations!</span></span> <span data-ttu-id="51f9c-271">Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions.</span><span class="sxs-lookup"><span data-stu-id="51f9c-271">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="51f9c-272">Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).</span><span class="sxs-lookup"><span data-stu-id="51f9c-272">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51f9c-273">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="51f9c-273">Next steps</span></span>

<span data-ttu-id="51f9c-274">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="51f9c-274">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="51f9c-275">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="51f9c-275">Understand the problem</span></span>
> * <span data-ttu-id="51f9c-276">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="51f9c-276">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="51f9c-277">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-277">Prepare and understand the data</span></span>
> * <span data-ttu-id="51f9c-278">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-278">Create a learning pipeline</span></span>
> * <span data-ttu-id="51f9c-279">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="51f9c-279">Load and transform the data</span></span>
> * <span data-ttu-id="51f9c-280">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="51f9c-280">Choose a learning algorithm</span></span>
> * <span data-ttu-id="51f9c-281">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-281">Train the model</span></span>
> * <span data-ttu-id="51f9c-282">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="51f9c-282">Evaluate the model</span></span>
> * <span data-ttu-id="51f9c-283">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="51f9c-283">Use the model for predictions</span></span>

<span data-ttu-id="51f9c-284">Passez au tutoriel suivant pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="51f9c-284">Advance to the next tutorial to learn more.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="51f9c-285">Clustering Iris</span><span class="sxs-lookup"><span data-stu-id="51f9c-285">Iris clustering</span></span>](iris-clustering.md)
