---
title: Prédire des prix en utilisant un apprenant de régression avec ML.NET
description: Prédisez des prix en utilisant un apprenant de régression avec ML.NET.
author: aditidugar
ms.author: johalex
ms.date: 03/05/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 543411f58f2d7c5c4e8658bd90cf52c7a3291ec3
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57678389"
---
# <a name="tutorial-predict-prices-using-a-regression-learner-with-mlnet"></a><span data-ttu-id="d8f0d-103">Tutoriel : Prédire des prix en utilisant un apprenant de régression avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="d8f0d-103">Tutorial: Predict prices using a regression learner with ML.NET</span></span>

<span data-ttu-id="d8f0d-104">Ce tutoriel montre comment utiliserML.NET pour créer un [modèle de régression](../resources/glossary.md#regression) afin de prédire des prix, plus précisément, des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-104">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting prices, specifically, New York City taxi fares.</span></span>

> [!NOTE]
> <span data-ttu-id="d8f0d-105">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-105">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="d8f0d-106">Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-106">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="d8f0d-107">Ce tutoriel et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-107">This tutorial and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="d8f0d-108">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-108">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="d8f0d-109">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-109">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="d8f0d-110">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d8f0d-110">Understand the problem</span></span>
> * <span data-ttu-id="d8f0d-111">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d8f0d-111">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="d8f0d-112">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-112">Prepare and understand the data</span></span>
> * <span data-ttu-id="d8f0d-113">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d8f0d-113">Create a learning pipeline</span></span>
> * <span data-ttu-id="d8f0d-114">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-114">Load and transform the data</span></span>
> * <span data-ttu-id="d8f0d-115">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d8f0d-115">Choose a learning algorithm</span></span>
> * <span data-ttu-id="d8f0d-116">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-116">Train the model</span></span>
> * <span data-ttu-id="d8f0d-117">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-117">Evaluate the model</span></span>
> * <span data-ttu-id="d8f0d-118">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d8f0d-118">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8f0d-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d8f0d-119">Prerequisites</span></span>

* <span data-ttu-id="d8f0d-120">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-120">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="d8f0d-121">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d8f0d-121">Understand the problem</span></span>

<span data-ttu-id="d8f0d-122">Ce problème consiste à prédire le prix d’une course de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-122">This problem is about predicting the fare of a taxi trip in New York City.</span></span> <span data-ttu-id="d8f0d-123">À première vue, ce prix semble dépendre simplement de la distance parcourue.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-123">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="d8f0d-124">Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-124">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="d8f0d-125">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d8f0d-125">Select the appropriate machine learning task</span></span>

<span data-ttu-id="d8f0d-126">Vous souhaitez prédire le prix, qui est une valeur réelle, en fonction des autres facteurs du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-126">You want to predict the price value, which is a real value, based on the other factors in the data set.</span></span> <span data-ttu-id="d8f0d-127">Pour ce faire, choisissez une tâche d’apprentissage automatique par [régression](../resources/glossary.md#regression).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-127">To do that you choose a [regression](../resources/glossary.md#regression) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="d8f0d-128">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="d8f0d-128">Create a console application</span></span>

1. <span data-ttu-id="d8f0d-129">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-129">Open Visual Studio 2017.</span></span> <span data-ttu-id="d8f0d-130">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-130">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="d8f0d-131">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-131">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="d8f0d-132">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-132">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="d8f0d-133">Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-133">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

1. <span data-ttu-id="d8f0d-134">Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-134">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="d8f0d-135">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-135">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="d8f0d-136">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-136">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="d8f0d-137">Installez le package NuGet **Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-137">Install the **Microsoft.ML** NuGet Package:</span></span>

    <span data-ttu-id="d8f0d-138">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-138">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="d8f0d-139">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-139">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="d8f0d-140">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-140">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-and-understand-the-data"></a><span data-ttu-id="d8f0d-141">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-141">Prepare and understand the data</span></span>

1. <span data-ttu-id="d8f0d-142">Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-142">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="d8f0d-143">Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-143">We use these data sets to train the machine learning model and then evaluate how accurate the model is.</span></span> <span data-ttu-id="d8f0d-144">Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-144">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

1. <span data-ttu-id="d8f0d-145">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-145">In **Solution Explorer**, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="d8f0d-146">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-146">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

1. <span data-ttu-id="d8f0d-147">Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-147">Open the **taxi-fare-train.csv** data set and look at column headers in the first row.</span></span> <span data-ttu-id="d8f0d-148">Examinons chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-148">Take a look at each of the columns.</span></span> <span data-ttu-id="d8f0d-149">Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-149">Understand the data and decide which columns are **features** and which one is the **label**.</span></span>

<span data-ttu-id="d8f0d-150">**L’étiquette** est l’identificateur de la colonne à prédire.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-150">The **label** is the identifier of the column you want to predict.</span></span> <span data-ttu-id="d8f0d-151">Les **fonctionnalités** identifiées servent à prédire l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-151">The identified **features** are used to predict the label.</span></span>

<span data-ttu-id="d8f0d-152">Le jeu de données fourni contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-152">The provided data set contains the following columns:</span></span>

* <span data-ttu-id="d8f0d-153">**vendor_id :** l’ID du taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-153">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="d8f0d-154">**rate_code :** le type de tarif de la course de taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-154">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="d8f0d-155">**passenger_count :** le nombre de passagers embarqués est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-155">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="d8f0d-156">**trip_time_in_secs :** durée totale de la course.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-156">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="d8f0d-157">Vous voulez prédire le prix de la course avant de l’effectuer.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-157">You want to predict the fare of the trip before the trip is completed.</span></span> <span data-ttu-id="d8f0d-158">À ce stade vous ne connaissez pas la durée de la course.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-158">At that moment you don't know how long the trip would take.</span></span> <span data-ttu-id="d8f0d-159">Par conséquent, la durée de la course n’est pas une fonctionnalité et vous devez exclure cette colonne du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-159">Thus, the trip time is not a feature and you'll exclude this column from the model.</span></span>
* <span data-ttu-id="d8f0d-160">**trip_distance :** la distance de la course est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-160">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="d8f0d-161">**payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-161">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="d8f0d-162">**fare_amount :** le prix total payé pour la course est l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-162">**fare_amount:** The total taxi fare paid is the label.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="d8f0d-163">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-163">Create data classes</span></span>

<span data-ttu-id="d8f0d-164">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-164">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="d8f0d-165">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-165">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="d8f0d-166">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-166">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="d8f0d-167">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-167">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="d8f0d-168">Ajoutez les directives `using` suivantes au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-168">Add the following `using` directives to the new file:</span></span>

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="d8f0d-169">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-169">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="d8f0d-170">`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-170">`TaxiTrip` is the input data class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="d8f0d-171">Utilisez l’attribut <xref:Microsoft.ML.Data.ColumnAttribute> pour spécifier les index des colonnes sources dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-171">Use the <xref:Microsoft.ML.Data.ColumnAttribute> attribute to specify the indices of the source columns in the data set.</span></span>

<span data-ttu-id="d8f0d-172">La classe `TaxiTripFarePrediction` représente les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-172">The `TaxiTripFarePrediction` class represents predicted results.</span></span> <span data-ttu-id="d8f0d-173">Elle comporte un seul champ float, `FareAmount`, avec un attribut `Score` <xref:Microsoft.ML.Data.ColumnNameAttribute> appliqué.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-173">It has a single float field, `FareAmount`, with a `Score` <xref:Microsoft.ML.Data.ColumnNameAttribute> attribute applied.</span></span> <span data-ttu-id="d8f0d-174">Dans le cas de la tâche de régression, la colonne **Score** contient les valeurs d’étiquette prédites.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-174">In case of the regression task the **Score** column contains predicted label values.</span></span>

> [!NOTE]
> <span data-ttu-id="d8f0d-175">Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-175">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="d8f0d-176">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-176">Define data and model paths</span></span>

<span data-ttu-id="d8f0d-177">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-177">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="d8f0d-178">Vous devez créer trois champs pour contenir les chemins des fichiers avec des jeux de données et le fichier pour enregistrer le modèle, ainsi qu’une variable globale pour `TextLoader` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-178">You need to create three fields to hold the paths to the files with data sets and the file to save the model, and a global variable for the `TextLoader`:</span></span>

* <span data-ttu-id="d8f0d-179">`_trainDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-179">`_trainDataPath` contains the path to the file with the data set used to train the model.</span></span>
* <span data-ttu-id="d8f0d-180">`_testDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’évaluation du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-180">`_testDataPath` contains the path to the file with the data set used to evaluate the model.</span></span>
* <span data-ttu-id="d8f0d-181">`_modelPath` contient le chemin du fichier où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-181">`_modelPath` contains the path to the file where the trained model is stored.</span></span>
* <span data-ttu-id="d8f0d-182">`_textLoader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-182">`_textLoader` is the <xref:Microsoft.ML.Data.TextLoader> used to load and transform the datasets.</span></span>

<span data-ttu-id="d8f0d-183">Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins et pour la variable `_textLoader` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-183">Add the following code right above the `Main` method to specify those paths and for the `_textLoader` variable:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="d8f0d-184">Lors de la création d’un modèle avec ML.NET, vous commencez par créer un contexte ML.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-184">When building a model with ML.NET you start by creating an ML Context.</span></span> <span data-ttu-id="d8f0d-185">Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-185">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span> <span data-ttu-id="d8f0d-186">L’environnement fournit un contexte pour votre tâche Machine Learning et qui peut être utilisé pour le suivi des exceptions et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-186">The environment provides a context for your machine learning job that can be used for exception tracking and logging.</span></span>

### <a name="initialize-variables-in-main"></a><span data-ttu-id="d8f0d-187">Initialiser les variables dans Principal</span><span class="sxs-lookup"><span data-stu-id="d8f0d-187">Initialize variables in Main</span></span>

<span data-ttu-id="d8f0d-188">Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-188">Create a variable called `mlContext` and initialize it with a new instance of `MLContext`.</span></span>  <span data-ttu-id="d8f0d-189">Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-189">Replace the `Console.WriteLine("Hello World!")` line with the following code in the `Main` method:</span></span>

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create the ML Context")]

<span data-ttu-id="d8f0d-190">Ensuite, pour configurer le chargement des données, initialisez variable globale `_textLoader` afin de la réutiliser.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-190">Next, to setup for data loading initialize the `_textLoader` global variable in order to reuse it.</span></span> <span data-ttu-id="d8f0d-191">Quand vous créez un `TextLoader`, vous passez le contexte nécessaire et la classe <xref:Microsoft.ML.Data.TextLoader.Arguments> qui permet la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-191">When you create a `TextLoader`, you pass in the context needed and the <xref:Microsoft.ML.Data.TextLoader.Arguments> class which enables customization.</span></span> <span data-ttu-id="d8f0d-192">Spécifiez le schéma de données en passant un tableau d’objets <xref:Microsoft.ML.Data.TextLoader.Column> au `TextLoader` contenant tous les noms de colonne et leurs types.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-192">Specify the data schema by passing an array of <xref:Microsoft.ML.Data.TextLoader.Column> objects to the `TextLoader` containing all the column names and their types.</span></span> <span data-ttu-id="d8f0d-193">Nous avons défini précédemment le schéma de données en créant notre classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-193">We defined the data schema previously when we created our `TaxiTrip` class.</span></span>

<span data-ttu-id="d8f0d-194">La classe `TextLoader` retourne une variable <xref:Microsoft.ML.Data.TextLoader> totalement initialisée</span><span class="sxs-lookup"><span data-stu-id="d8f0d-194">The `TextLoader` class returns a fully initialized <xref:Microsoft.ML.Data.TextLoader></span></span>  

<span data-ttu-id="d8f0d-195">Pour initialiser la variable globale `_textLoader` afin de la réutiliser pour les jeux de données nécessaires, ajoutez le code suivant après l’initialisation de `mlContext` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-195">To initialize the `_textLoader` global variable in order to reuse it for the needed datasets, add the following code after the  `mlContext` initialization:</span></span>

[!code-csharp[initTextLoader](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Initialize the TextLoader")]

<span data-ttu-id="d8f0d-196">Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` afin d’appeler la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-196">Add the following as the next line of code in the `Main` method to call the `Train` method:</span></span>

[!code-csharp[Train](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Train your model")]

<span data-ttu-id="d8f0d-197">La méthode `Train` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-197">The `Train` method executes the following tasks:</span></span>

* <span data-ttu-id="d8f0d-198">Charge les données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-198">Loads the data.</span></span>
* <span data-ttu-id="d8f0d-199">Extrait et transforme les données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-199">Extracts and transforms the data.</span></span>
* <span data-ttu-id="d8f0d-200">Effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-200">Trains the model.</span></span>
* <span data-ttu-id="d8f0d-201">Enregistre le modèle en tant que fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-201">Saves the model as .zip file.</span></span>
* <span data-ttu-id="d8f0d-202">Retourne le modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-202">Returns the model.</span></span>

<span data-ttu-id="d8f0d-203">La méthode `Train` effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-203">The `Train` method trains the model.</span></span> <span data-ttu-id="d8f0d-204">Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-204">Create that method just below `Main`, using the following code:</span></span>

```csharp
public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

<span data-ttu-id="d8f0d-205">Nous passons deux paramètres à la méthode `Train` ; un paramètre `MLContext` pour le contexte (`mlContext`) et une chaîne pour le chemin d’accès au jeu de données (`dataPath`).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-205">We are passing two parameters into the `Train` method; an `MLContext` for the context (`mlContext`), and a string for the dataset path (`dataPath`).</span></span> <span data-ttu-id="d8f0d-206">Nous allons réutiliser cette méthode pour le chargement des jeux de données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-206">We're going to reuse this method for loading datasets.</span></span>

## <a name="load-and-transform-data"></a><span data-ttu-id="d8f0d-207">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-207">Load and transform data</span></span>

<span data-ttu-id="d8f0d-208">Nous allons charger les données en utilisant la variable globale `_textLoader` et le paramètre `dataPath`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-208">We'll load the data using the `_textLoader` global variable with the `dataPath` parameter.</span></span> <span data-ttu-id="d8f0d-209">Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-209">It returns a <xref:Microsoft.Data.DataView.IDataView>.</span></span> <span data-ttu-id="d8f0d-210">Comme entrée et sortie de transformations, un `IDataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-210">As the input and output of Transforms, an `IDataView` is the fundamental data pipeline type, comparable to `IEnumerable` for `LINQ`.</span></span>

<span data-ttu-id="d8f0d-211">Dans ML.NET, les données sont semblables à une vue SQL.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-211">In ML.NET, data is similar to a SQL view.</span></span> <span data-ttu-id="d8f0d-212">Elles sont évaluées tardivement, schématisées et hétérogènes.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-212">It is lazily evaluated, schematized, and heterogenous.</span></span> <span data-ttu-id="d8f0d-213">L’objet est la première partie du pipeline, et charge les données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-213">The object is the first part of the pipeline, and loads the data.</span></span> <span data-ttu-id="d8f0d-214">Pour ce tutoriel, il charge un jeu de données avec des informations sur les courses de taxi, utiles pour en prédire le prix.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-214">For this tutorial, it loads a dataset with taxi trip information useful to predict fares.</span></span> <span data-ttu-id="d8f0d-215">Cette méthode permet de créer puis de former le modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-215">This is used to create the model, and train it.</span></span>

 <span data-ttu-id="d8f0d-216">Ajoutez le code suivant comme première ligne de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-216">Add the following code as the first line of the `Train` method:</span></span>

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "loading training dataset")]

<span data-ttu-id="d8f0d-217">Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-217">In the next steps we refer to the columns by the names defined in the `TaxiTrip` class.</span></span>

<span data-ttu-id="d8f0d-218">Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-218">When the model is trained and evaluated, by default, the values in the **Label** column are considered as correct values to be predicted.</span></span> <span data-ttu-id="d8f0d-219">Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-219">As we want to predict the taxi trip fare, copy the `FareAmount` column into the **Label** column.</span></span> <span data-ttu-id="d8f0d-220">Pour ce faire, utilisez la classe de transformation `CopyColumnsEstimator`, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-220">To do that, use the `CopyColumnsEstimator` transformation class, and add the following code:</span></span>

[!code-csharp[CopyColumnsEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Use the CopyColumnsEstimator")]

<span data-ttu-id="d8f0d-221">L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques**, car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-221">The algorithm that trains the model requires **numeric** features, so you have to transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) values into numbers.</span></span> <span data-ttu-id="d8f0d-222">Pour ce faire, utilisez la classe de transformation `OneHotEncodingEstimator`, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-222">To do that, use the `OneHotEncodingEstimator` transformation class, which assigns different numeric key values to the different values in each of the columns, and add the following code:</span></span>

[!code-csharp[OneHotEncodingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Use the OneHotEncodingEstimator")]

<span data-ttu-id="d8f0d-223">La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `ColumnConcatenatingEstimator`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-223">The last step in data preparation combines all of the feature columns into the **Features** column using the `ColumnConcatenatingEstimator` transformation class.</span></span> <span data-ttu-id="d8f0d-224">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-224">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="d8f0d-225">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-225">Add the following code:</span></span>

[!code-csharp[ColumnConcatenatingEstimator](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Use the ColumnConcatenatingEstimator")]

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="d8f0d-226">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d8f0d-226">Choose a learning algorithm</span></span>

<span data-ttu-id="d8f0d-227">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnons un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-227">After adding the data to the pipeline and transforming it into the correct input format, we select a learning algorithm (**learner**).</span></span> <span data-ttu-id="d8f0d-228">L’apprenant effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-228">The learner trains the model.</span></span> <span data-ttu-id="d8f0d-229">Nous avez choisi une tâche de **régression** pour ce problème. Nous utilisons donc un apprenant `FastTreeRegressionTrainer`, qui est l’un des apprenants de régression fournis par ML.NET.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-229">We chose a **regression** task for this problem, so we use a `FastTreeRegressionTrainer` learner, which is one of the regression learners provided by ML.NET.</span></span>

<span data-ttu-id="d8f0d-230">L’apprenant `FastTreeRegressionTrainer` utilise le boosting de gradient.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-230">The `FastTreeRegressionTrainer` learner utilizes gradient boosting.</span></span> <span data-ttu-id="d8f0d-231">Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-231">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="d8f0d-232">Il génère chaque arbre de régression étape par étape.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-232">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="d8f0d-233">Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-233">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="d8f0d-234">Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-234">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="d8f0d-235">Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-235">For more information about gradient boosting, see [Boosted Decision Tree Regression](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="d8f0d-236">Ajoutez le code suivant dans la méthode `Train` afin d’ajouter le `FastTreeRegressionTrainer` au code de traitement des données ajouté à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-236">Add the following code into the `Train` method to add the `FastTreeRegressionTrainer` to the data processing code added in the previous step:</span></span>

[!code-csharp[FastTreeRegressionTrainer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Add the FastTreeRegressionTrainer")]

## <a name="train-the-model"></a><span data-ttu-id="d8f0d-237">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-237">Train the model</span></span>

<span data-ttu-id="d8f0d-238">La dernière étape consiste à effectuer l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-238">The final step is to train the model.</span></span> <span data-ttu-id="d8f0d-239">Nous effectuons l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain>, selon le jeu de données qui a été chargé et transformé.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-239">We train the model, <xref:Microsoft.ML.Data.TransformerChain>, based on the dataset that has been loaded and transformed.</span></span> <span data-ttu-id="d8f0d-240">Une fois l’estimation définie, nous formons le modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-240">Once the estimator has been defined, we train the model using the <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> while providing the already loaded training data.</span></span> <span data-ttu-id="d8f0d-241">Cette méthode retourne un modèle à utiliser pour les prédictions.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-241">This returns a model to use for predictions.</span></span> <span data-ttu-id="d8f0d-242">`pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-242">`pipeline.Fit()` trains the pipeline and returns a `Transformer` based on the `DataView` passed in.</span></span> <span data-ttu-id="d8f0d-243">L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-243">The experiment is not executed until this happens.</span></span>

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#11 "Train the model")]

<span data-ttu-id="d8f0d-244">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="d8f0d-244">And that's it!</span></span> <span data-ttu-id="d8f0d-245">Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-245">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="d8f0d-246">Nous allons maintenant essayer de déterminer la précision du modèle et découvrir comment l’utiliser pour prédire les valeurs des tarifs de taxi.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-246">Now let's take a look to understand how accurate the model is and learn how to use it to predict taxi fare values.</span></span>

### <a name="save-the-model"></a><span data-ttu-id="d8f0d-247">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-247">Save the model</span></span>

<span data-ttu-id="d8f0d-248">À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-248">At this point, you have a model of type <xref:Microsoft.ML.Data.TransformerChain> that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="d8f0d-249">Pour enregistrer le modèle dans un fichier .zip, ajoutez le code suivant à la fin de la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-249">To save the model to a .zip file, add the following code at the end of the `Train` method:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Save the model as a .zip file and return the model")]

## <a name="save-the-model-as-a-zip-file"></a><span data-ttu-id="d8f0d-250">Enregistrer le modèle en tant que fichier .zip</span><span class="sxs-lookup"><span data-stu-id="d8f0d-250">Save the model as a .zip file</span></span>

<span data-ttu-id="d8f0d-251">Créez la méthode `SaveModelAsFile` juste après la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-251">Create the `SaveModelAsFile` method, just after the `Train` method, using the following code:</span></span>

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

<span data-ttu-id="d8f0d-252">La méthode `SaveModelAsFile` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-252">The `SaveModelAsFile` method executes the following tasks:</span></span>

* <span data-ttu-id="d8f0d-253">Enregistre le modèle sous la forme d’un fichier .zip.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-253">Saves the model as a .zip file.</span></span>

<span data-ttu-id="d8f0d-254">Nous devons créer une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-254">We need to create a method to save the model so that it can be reused and consumed in other applications.</span></span> <span data-ttu-id="d8f0d-255">Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-255">The `ITransformer` has a <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> method that takes in the `_modelPath` global field, and a <xref:System.IO.Stream>.</span></span> <span data-ttu-id="d8f0d-256">Comme nous souhaitons l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-256">Since we want to save this as a zip file, we'll create the `FileStream` immediately before calling the `SaveTo` method.</span></span> <span data-ttu-id="d8f0d-257">Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-257">Add the following code to the `SaveModelAsFile` method as the next line:</span></span>

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Add the SaveTo Method")]

<span data-ttu-id="d8f0d-258">Nous pouvons également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-258">We could also display where the file was written by writing a console message with the `_modelPath`, using the following code:</span></span>

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a><span data-ttu-id="d8f0d-259">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-259">Evaluate the model</span></span>

<span data-ttu-id="d8f0d-260">L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-260">Evaluation is the process of checking how well the model predicts label values.</span></span> <span data-ttu-id="d8f0d-261">Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-261">It's important that the model makes good predictions on data that was not used to train the model.</span></span> <span data-ttu-id="d8f0d-262">Pour ce faire, vous pouvez, par exemple, fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme indiqué dans ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-262">One way to do this is to split the data into training and test data sets, as it's done in this tutorial.</span></span> <span data-ttu-id="d8f0d-263">Une fois que vous avez formé le modèle à l’aide des données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-263">Now that you've trained the model on the training data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="d8f0d-264">La méthode `Evaluate` évalue le modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-264">The `Evaluate` method evaluates the model.</span></span> <span data-ttu-id="d8f0d-265">Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-265">To create that method, add the following code below the `Train` method:</span></span>

```csharp
private static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```
<span data-ttu-id="d8f0d-266">La méthode `Evaluate` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-266">The `Evaluate` method executes the following tasks:</span></span>

* <span data-ttu-id="d8f0d-267">Charge le jeu de données de test.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-267">Loads the test dataset.</span></span>
* <span data-ttu-id="d8f0d-268">Crée l’évaluateur de régression.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-268">Creates the regression evaluator.</span></span>
* <span data-ttu-id="d8f0d-269">Évalue le modèle et crée des métriques.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-269">Evaluates the model and creates metrics.</span></span>
* <span data-ttu-id="d8f0d-270">Affiche les métriques.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-270">Displays the metrics.</span></span>

<span data-ttu-id="d8f0d-271">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-271">Add a call to the new method from the `Main` method, right under the `Train` method call, using the following code:</span></span>

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Call the Evaluate method")]

<span data-ttu-id="d8f0d-272">Nous allons charger le jeu de données de test à l’aide de la variable globale `_textLoader` précédemment initialisée avec le champ global `_testDataPath`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-272">We'll load the test dataset using the previously initialized  `_textLoader` global variable with the `_testDataPath` global field.</span></span> <span data-ttu-id="d8f0d-273">Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-273">You can evaluate the model using this dataset as a quality check.</span></span> <span data-ttu-id="d8f0d-274">Ajoutez le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-274">Add the following code to the `Evaluate` method:</span></span>

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Load the test dataset")]

<span data-ttu-id="d8f0d-275">Nous allons ensuite utiliser le paramètre Machine Learning `model` (un transformateur) pour saisir les fonctionnalités et retourner des prédictions.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-275">Next, we'll use the machine learning `model` parameter (a transformer) to input the features and return predictions.</span></span> <span data-ttu-id="d8f0d-276">Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-276">Add the following code to the `Evaluate` method as the next line:</span></span>

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Predict using the Transformer")]

<span data-ttu-id="d8f0d-277">La méthode `RegressionContext.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-277">The `RegressionContext.Evaluate` method computes the quality metrics for the `PredictionModel` using the specified dataset.</span></span> <span data-ttu-id="d8f0d-278">Elle retourne un objet <xref:Microsoft.ML.Data.RegressionMetrics> qui contient les métriques globales calculées par les évaluateurs de régression.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-278">It returns a <xref:Microsoft.ML.Data.RegressionMetrics> object that contains the overall metrics computed by regression evaluators.</span></span> <span data-ttu-id="d8f0d-279">Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-279">To display these to determine the quality of the model, you need to get the metrics first.</span></span> <span data-ttu-id="d8f0d-280">Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-280">Add the following code as the next line in the `Evaluate` method:</span></span>

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Compute Metrics")]

<span data-ttu-id="d8f0d-281">Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-281">Add the following code to evaluate the model and produce the evaluation metrics:</span></span>

```csharp
Console.WriteLine();
Console.WriteLine($"*************************************************");
Console.WriteLine($"*       Model quality metrics evaluation         ");
Console.WriteLine($"*------------------------------------------------");
```

<span data-ttu-id="d8f0d-282">[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-282">[RSquared](../resources/glossary.md#coefficient-of-determination) is another evaluation metric of the regression models.</span></span> <span data-ttu-id="d8f0d-283">RSquared prend des valeurs entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-283">RSquared takes values between 0 and 1.</span></span> <span data-ttu-id="d8f0d-284">Plus sa valeur est proche de 1, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-284">The closer its value is to 1, the better the model is.</span></span> <span data-ttu-id="d8f0d-285">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-285">Add the following code into the `Evaluate` method to display the RSquared value:</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#18 "Display the RSquared metric.")]

<span data-ttu-id="d8f0d-286">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-286">[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) is one of the evaluation metrics of the regression model.</span></span> <span data-ttu-id="d8f0d-287">Plus sa valeur est faible, plus le modèle est bon.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-287">The lower it is, the better the model is.</span></span> <span data-ttu-id="d8f0d-288">Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-288">Add the following code into the `Evaluate` method to display the RMS value:</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#19 "Display the RMS metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="d8f0d-289">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d8f0d-289">Use the model for predictions</span></span>


## <a name="predict-the-test-data-outcome-with-the-model-and-a-single-comment"></a><span data-ttu-id="d8f0d-290">Prédire le résultat de données de test avec le modèle et un commentaire unique</span><span class="sxs-lookup"><span data-stu-id="d8f0d-290">Predict the test data outcome with the model and a single comment</span></span>

<span data-ttu-id="d8f0d-291">Créez la méthode `TestSinglePrediction` juste après la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-291">Create the `TestSinglePrediction` method, just after the `Evaluate` method, using the following code:</span></span>

```csharp
private static void TestSinglePrediction(MLContext mlContext)
{

}
```

<span data-ttu-id="d8f0d-292">La méthode `TestSinglePrediction` exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-292">The `TestSinglePrediction` method executes the following tasks:</span></span>

* <span data-ttu-id="d8f0d-293">Crée un commentaire unique de données de test.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-293">Creates a single comment of test data.</span></span>
* <span data-ttu-id="d8f0d-294">Prédit le prix de la course en fonction des données de test.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-294">Predicts fare amount based on test data.</span></span>
* <span data-ttu-id="d8f0d-295">Combine les données de test et les prédictions pour générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-295">Combines test data and predictions for reporting.</span></span>
* <span data-ttu-id="d8f0d-296">Affiche les résultats prédits.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-296">Displays the predicted results.</span></span>

<span data-ttu-id="d8f0d-297">Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-297">Add a call to the new method from the `Main` method, right under the `Evaluate` method call, using the following code:</span></span>

[!code-csharp[CallTestSinglePrediction](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#20 "Call the TestSinglePrediction method")]

<span data-ttu-id="d8f0d-298">Étant donné que nous voulons charger le modèle à partir du fichier zip que nous avons enregistré, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `Load`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-298">Since we want to load the model from the zip file we saved, we'll create the `FileStream` immediately before calling the `Load` method.</span></span> <span data-ttu-id="d8f0d-299">Ajoutez comme nouvelle ligne le code suivant à la méthode `TestSinglePrediction` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-299">Add the following code to the `TestSinglePrediction` method as the next line:</span></span>

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#21 "Load the model")]

<span data-ttu-id="d8f0d-300">Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-300">While the `model` is a `transformer` that operates on many rows of data, a very common production scenario is a need for predictions on individual examples.</span></span> <span data-ttu-id="d8f0d-301">Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-301">The <xref:Microsoft.ML.PredictionEngine%602> is a wrapper that is returned from the `CreatePredictionEngine` method.</span></span> <span data-ttu-id="d8f0d-302">Ajoutons le code suivant pour créer le `PredictionEngine` comme ligne suivante dans la méthode `TestSinglePrediction` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-302">Let's add the following code to create the `PredictionEngine` as the next line in the `TestSinglePrediction` Method:</span></span>

[!code-csharp[MakePredictionEngine](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#22 "Create the PredictionFunction")]
  
<span data-ttu-id="d8f0d-303">Ce tutoriel utilise une course test au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-303">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="d8f0d-304">Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-304">Later you can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="d8f0d-305">Ajoutez une course pour tester la prédiction de coût du modèle formé dans la méthode `TestSinglePrediction` en créant une instance de `TaxiTrip` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-305">Add a trip to test the trained model's prediction of cost in the `TestSinglePrediction` method by creating an instance of `TaxiTrip`:</span></span>

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#23 "Create test data for single prediction")]

 <span data-ttu-id="d8f0d-306">Nous pouvons utiliser ces éléments pour prédire le prix basé sur une instance unique des données d’une course de taxi.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-306">We can use that to predict the fare based on a single instance of the taxi trip data.</span></span> <span data-ttu-id="d8f0d-307">Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-307">To get a prediction, use <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> on the data.</span></span> <span data-ttu-id="d8f0d-308">Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-308">Note that the input data is a string and the model includes the featurization.</span></span> <span data-ttu-id="d8f0d-309">Votre pipeline est synchronisé durant l’apprentissage et la prédiction.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-309">Your pipeline is in sync during training and prediction.</span></span> <span data-ttu-id="d8f0d-310">Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-310">You didn’t have to write preprocessing/featurization code specifically for predictions, and the same API takes care of both batch and one-time predictions.</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#24 "Create a prediction of taxi fare")]

<span data-ttu-id="d8f0d-311">Pour afficher le prix prédit de la course spécifiée, ajoutez le code suivant à la méthode `TestSinglePrediction` :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-311">To display the predicted fare of the specified trip, add the following code into the `TestSinglePrediction` method:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#25 "Display the prediction.")]

<span data-ttu-id="d8f0d-312">Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-312">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="d8f0d-313">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="d8f0d-313">Congratulations!</span></span> <span data-ttu-id="d8f0d-314">Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-314">You've now successfully built a machine learning model for predicting taxi trip fares, evaluated its accuracy, and used it to make predictions.</span></span> <span data-ttu-id="d8f0d-315">Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).</span><span class="sxs-lookup"><span data-stu-id="d8f0d-315">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d8f0d-316">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d8f0d-316">Next steps</span></span>

<span data-ttu-id="d8f0d-317">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="d8f0d-317">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="d8f0d-318">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d8f0d-318">Understand the problem</span></span>
> * <span data-ttu-id="d8f0d-319">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d8f0d-319">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="d8f0d-320">Préparer et comprendre les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-320">Prepare and understand the data</span></span>
> * <span data-ttu-id="d8f0d-321">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d8f0d-321">Create a learning pipeline</span></span>
> * <span data-ttu-id="d8f0d-322">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d8f0d-322">Load and transform the data</span></span>
> * <span data-ttu-id="d8f0d-323">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d8f0d-323">Choose a learning algorithm</span></span>
> * <span data-ttu-id="d8f0d-324">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-324">Train the model</span></span>
> * <span data-ttu-id="d8f0d-325">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="d8f0d-325">Evaluate the model</span></span>
> * <span data-ttu-id="d8f0d-326">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d8f0d-326">Use the model for predictions</span></span>

<span data-ttu-id="d8f0d-327">Passez au tutoriel suivant pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="d8f0d-327">Advance to the next tutorial to learn more.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="d8f0d-328">Clustering Iris</span><span class="sxs-lookup"><span data-stu-id="d8f0d-328">Iris clustering</span></span>](iris-clustering.md)
