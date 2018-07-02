---
title: Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)
description: Découvrez comment utiliser ML.NET dans un scénario de régression.
author: aditidugar
ms.author: johalex
ms.date: 06/05/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 048ed1d38408c1ba4901c554cae33d5552c9e303
ms.sourcegitcommit: 5b0802832fb9ad684d34e69b8644a16a5b7c4810
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34860671"
---
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a><span data-ttu-id="bb77a-103">Tutoriel : Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)</span><span class="sxs-lookup"><span data-stu-id="bb77a-103">Tutorial: Use ML.NET to predict New York taxi fares (regression)</span></span>

> [!NOTE]
> <span data-ttu-id="bb77a-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="bb77a-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="bb77a-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="bb77a-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="bb77a-106">Ce tutoriel montre l’utilisation de ML.NET pour générer un [modèle de régression](../resources/glossary.md#regression) afin de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="bb77a-106">This tutorial illustrates how to use ML.NET to build a [regression model](../resources/glossary.md#regression) for predicting New York City taxi fares.</span></span>

<span data-ttu-id="bb77a-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="bb77a-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="bb77a-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="bb77a-108">Understand the problem</span></span>
> * <span data-ttu-id="bb77a-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="bb77a-109">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="bb77a-110">Préparer et comprendre vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-110">Prepare and understand your data</span></span>
> * <span data-ttu-id="bb77a-111">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-111">Create a learning pipeline</span></span>
> * <span data-ttu-id="bb77a-112">Charger et transformer vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-112">Load and transform your data</span></span>
> * <span data-ttu-id="bb77a-113">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-113">Choose a learning algorithm</span></span>
> * <span data-ttu-id="bb77a-114">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-114">Train the model</span></span>
> * <span data-ttu-id="bb77a-115">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-115">Evaluate the model</span></span>
> * <span data-ttu-id="bb77a-116">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="bb77a-116">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb77a-117">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bb77a-117">Prerequisites</span></span>

* <span data-ttu-id="bb77a-118">[Visual Studio 2017 15.6 ou version ultérieure](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="bb77a-118">[Visual Studio 2017 15.6 or later](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="bb77a-119">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="bb77a-119">Understand the problem</span></span>

<span data-ttu-id="bb77a-120">Ce problème est centré autour de la **prédiction du prix d’une course de taxi à New York**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-120">This problem is centered around **predicting the fare of a taxi trip in New York City**.</span></span> <span data-ttu-id="bb77a-121">À première vue, ce prix semble dépendre simplement de la distance parcourue.</span><span class="sxs-lookup"><span data-stu-id="bb77a-121">At first glance, it may seem to depend simply on the distance traveled.</span></span> <span data-ttu-id="bb77a-122">Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.</span><span class="sxs-lookup"><span data-stu-id="bb77a-122">However, taxi vendors in New York charge varying amounts for other factors such as additional passengers or paying with a credit card instead of cash.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="bb77a-123">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="bb77a-123">Select the appropriate machine learning task</span></span>

<span data-ttu-id="bb77a-124">Pour prédire le prix de la course de taxi, vous sélectionnez d’abord la tâche d’apprentissage automatique appropriée.</span><span class="sxs-lookup"><span data-stu-id="bb77a-124">To predict the taxi fare, you first select the appropriate machine learning task.</span></span> <span data-ttu-id="bb77a-125">Vous devez prédire une valeur réelle (valeur double qui représente le prix) en fonction des autres facteurs du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="bb77a-125">You are looking to predict a real value (a double that represents price) based on the other factors in the dataset.</span></span> <span data-ttu-id="bb77a-126">Vous choisissez une tâche de [**régression**](../resources/glossary.md#regression).</span><span class="sxs-lookup"><span data-stu-id="bb77a-126">You choose a [**regression**](../resources/glossary.md#regression) task.</span></span>

<span data-ttu-id="bb77a-127">Le processus d’apprentissage du modèle identifie les facteurs du jeu de données qui impactent le plus la prédiction du prix final de la course.</span><span class="sxs-lookup"><span data-stu-id="bb77a-127">The process of training the model identifies which factors in the dataset are most influential when predicting the final fare price.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="bb77a-128">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="bb77a-128">Create a console application</span></span>

1. <span data-ttu-id="bb77a-129">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="bb77a-129">Open Visual Studio 2017.</span></span> <span data-ttu-id="bb77a-130">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="bb77a-130">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="bb77a-131">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-131">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="bb77a-132">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-132">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="bb77a-133">Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-133">In the **Name** text box, type "TaxiFarePrediction" and then select the **OK** button.</span></span>

2. <span data-ttu-id="bb77a-134">Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :</span><span class="sxs-lookup"><span data-stu-id="bb77a-134">Create a directory named *Data* in your project to save your data set files:</span></span>

    <span data-ttu-id="bb77a-135">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-135">In **Solution Explorer**, right-click on your project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="bb77a-136">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="bb77a-136">Type "Data" and hit Enter.</span></span>

3. <span data-ttu-id="bb77a-137">Installez le **package NuGet Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="bb77a-137">Install the **Microsoft.ML NuGet Package**:</span></span>

    <span data-ttu-id="bb77a-138">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-138">In Solution Explorer, right-click on your project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="bb77a-139">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-139">Choose "nuget.org" as the Package source, select the Browse tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="bb77a-140">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="bb77a-140">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

### <a name="prepare-and-understand-your-data"></a><span data-ttu-id="bb77a-141">Préparer et comprendre vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-141">Prepare and understand your data</span></span>

1. <span data-ttu-id="bb77a-142">Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="bb77a-142">Download the [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) and the [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv) data sets and save them to the *Data* folder previously created.</span></span> <span data-ttu-id="bb77a-143">Le jeu de données Taxi Trip effectue l’apprentissage automatique du modèle et peut servir à évaluer la précision de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-143">The Taxi Trip data set trains the machine learning model and can be used to evaluate how accurate your model is.</span></span> <span data-ttu-id="bb77a-144">Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span><span class="sxs-lookup"><span data-stu-id="bb77a-144">These data sets are originally from the [NYC TLC Taxi Trip data set](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).</span></span>

2. <span data-ttu-id="bb77a-145">Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-145">In Solution Explorer, right-click each of the \*.csv files and select **Properties**.</span></span> <span data-ttu-id="bb77a-146">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Toujours**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-146">Under **Advanced**, change the value of **Copy to Output Directory** to **Always**.</span></span>

3. <span data-ttu-id="bb77a-147">Ouvrez le jeu de données **taxi-fare-train.csv** dans l’éditeur de code et examinez les en-têtes de colonne dans la première ligne.</span><span class="sxs-lookup"><span data-stu-id="bb77a-147">Open the **taxi-fare-train.csv** data set in the code editor and look at column headers in the first row.</span></span> <span data-ttu-id="bb77a-148">Examinons chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="bb77a-148">Take a look at each of the columns.</span></span> <span data-ttu-id="bb77a-149">Analysez les données et identifiez les colonnes qui représentent des **fonctionnalités** et celle qui constitue l’**étiquette**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-149">Understand the data and decide which columns are **features** and which is the **label**.</span></span>

<span data-ttu-id="bb77a-150">L’**étiquette** est l’identificateur de la colonne que vous tentez de prédire.</span><span class="sxs-lookup"><span data-stu-id="bb77a-150">The **label** is the identifier of the column you are trying to predict.</span></span> <span data-ttu-id="bb77a-151">Les **fonctionnalités** identifiées servent à prédire l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="bb77a-151">The identified **features** are used to predict the label.</span></span>

* <span data-ttu-id="bb77a-152">**vendor_id :** l’ID du taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb77a-152">**vendor_id:** The ID of the taxi vendor is a feature.</span></span>
* <span data-ttu-id="bb77a-153">**rate_code :** le type de tarif de la course de taxi est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb77a-153">**rate_code:** The rate type of the taxi trip is a feature.</span></span>
* <span data-ttu-id="bb77a-154">**passenger_count :** le nombre de passagers embarqués est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb77a-154">**passenger_count:** The number of passengers on the trip is a feature.</span></span>
* <span data-ttu-id="bb77a-155">**trip_time_in_secs :** durée totale de la course.</span><span class="sxs-lookup"><span data-stu-id="bb77a-155">**trip_time_in_secs:** The amount of time the trip took.</span></span> <span data-ttu-id="bb77a-156">Vous ne connaissez la durée de la course qu’une fois celle-ci terminée.</span><span class="sxs-lookup"><span data-stu-id="bb77a-156">You won't know how long the trip takes until after it is completed.</span></span> <span data-ttu-id="bb77a-157">Vous excluez cette colonne du modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-157">You exclude this column from the model.</span></span>
* <span data-ttu-id="bb77a-158">**trip_distance :** la distance de la course est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb77a-158">**trip_distance:** The distance of the trip is a feature.</span></span>
* <span data-ttu-id="bb77a-159">**payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bb77a-159">**payment_type:** The payment method (cash or credit card) is a feature.</span></span>
* <span data-ttu-id="bb77a-160">**fare_amount :** le prix total payé pour la course est l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="bb77a-160">**fare_amount:** The total taxi fare paid is the label.</span></span>

### <a name="create-classes-and-define-paths"></a><span data-ttu-id="bb77a-161">Créer des classes et définir des chemins</span><span class="sxs-lookup"><span data-stu-id="bb77a-161">Create classes and define paths</span></span>

<span data-ttu-id="bb77a-162">Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="bb77a-162">Add the following additional `using` statements to the top of the *Program.cs* file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

<span data-ttu-id="bb77a-163">Vous devez créer trois variables globales pour contenir les chemins d’accès aux fichiers récemment téléchargés et pour enregistrer le modèle :</span><span class="sxs-lookup"><span data-stu-id="bb77a-163">You need to create three global variables to hold the paths to the recently downloaded files and to save the model:</span></span>

* <span data-ttu-id="bb77a-164">`_datapath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-164">`_datapath` has the path to the data set used to train the model.</span></span>
* <span data-ttu-id="bb77a-165">`_testdatapath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-165">`_testdatapath` has the path to the data set used to evaluate the model.</span></span>
* <span data-ttu-id="bb77a-166">`_modelpath` contient le chemin d’accès où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="bb77a-166">`_modelpath` has the path where the trained model is stored.</span></span>

<span data-ttu-id="bb77a-167">Ajoutez le code suivant à la ligne directement au-dessus de `Main` pour spécifier les fichiers récemment téléchargés :</span><span class="sxs-lookup"><span data-stu-id="bb77a-167">Add the following code to the line right above `Main` to specify the recently downloaded files:</span></span>

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

<span data-ttu-id="bb77a-168">Ensuite, créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="bb77a-168">Next, create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="bb77a-169">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-169">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="bb77a-170">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*.</span><span class="sxs-lookup"><span data-stu-id="bb77a-170">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TaxiTrip.cs*.</span></span> <span data-ttu-id="bb77a-171">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-171">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="bb77a-172">Ajoutez les instructions `using` suivantes au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="bb77a-172">Add the following `using` statements to the new file:</span></span>

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

<span data-ttu-id="bb77a-173">Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :</span><span class="sxs-lookup"><span data-stu-id="bb77a-173">Remove the existing class definition and add the following code, which has two classes `TaxiTrip` and `TaxiTripFarePrediction`, to the *TaxiTrip.cs* file:</span></span>

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

<span data-ttu-id="bb77a-174">`TaxiTrip` est la classe du jeu de données d’entrée et contient des définitions pour chacune des colonnes du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="bb77a-174">`TaxiTrip` is the input data set class and has definitions for each of the data set columns.</span></span> <span data-ttu-id="bb77a-175">La classe `TaxiTripFarePrediction` est utilisée pour la prédiction, une fois le modèle formé.</span><span class="sxs-lookup"><span data-stu-id="bb77a-175">The `TaxiTripFarePrediction` class is used for prediction after the model has been trained.</span></span> <span data-ttu-id="bb77a-176">Elle contient une valeur flottante unique (`FareAmount`) et un attribut `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) appliqué.</span><span class="sxs-lookup"><span data-stu-id="bb77a-176">It has a single float (`FareAmount`) and a `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) attribute applied.</span></span>

<span data-ttu-id="bb77a-177">Revenez maintenant au fichier **Program.cs**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-177">Now go back to the **Program.cs** file.</span></span> <span data-ttu-id="bb77a-178">Dans `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-178">In `Main`, replace the `Console.WriteLine("Hello World!")` with the following code:</span></span>

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

<span data-ttu-id="bb77a-179">La méthode `Train` effectue l’apprentissage de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-179">The `Train` method trains your model.</span></span> <span data-ttu-id="bb77a-180">Créez cette fonction juste sous `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-180">Create that function just below `Main`, using the following code:</span></span>

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="bb77a-181">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-181">Create a learning pipeline</span></span>

<span data-ttu-id="bb77a-182">Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-182">The learning pipeline loads all of the data and algorithms necessary to train the model.</span></span> <span data-ttu-id="bb77a-183">Ajoutez le code suivant à la méthode `Train()` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-183">Add the following code into the `Train()` method:</span></span>

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-your-data"></a><span data-ttu-id="bb77a-184">Charger et transformer vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-184">Load and transform your data</span></span>

<span data-ttu-id="bb77a-185">Ensuite, chargez vos données dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb77a-185">Next, load your data into the pipeline.</span></span> <span data-ttu-id="bb77a-186">Pointez vers le chemin `_datapath` créé initialement, puis spécifiez le délimiteur de fichier .csv (,).</span><span class="sxs-lookup"><span data-stu-id="bb77a-186">Point to the `_datapath` created initially and specify the delimiter of the .csv file (,).</span></span> <span data-ttu-id="bb77a-187">Ajoutez le code suivant dans la méthode `Train()`, sous la dernière étape :</span><span class="sxs-lookup"><span data-stu-id="bb77a-187">Add the following code into the `Train()` method underneath the last step:</span></span>

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(separator:','));
```

<span data-ttu-id="bb77a-188">Vous ferez référence aux colonnes sans les traits de soulignement dans le code que vous créez.</span><span class="sxs-lookup"><span data-stu-id="bb77a-188">You'll refer to the columns without the underscores in the code you're creating.</span></span> <span data-ttu-id="bb77a-189">Copiez la colonne `FareAmount` dans une nouvelle colonne appelée « Étiquette » à l’aide de la fonction `ColumnCopier()`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-189">Copy the `FareAmount` column into a new column called "Label" using the `ColumnCopier()` function.</span></span> <span data-ttu-id="bb77a-190">Cette colonne est l’**étiquette**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-190">This column is the **Label**.</span></span>

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

<span data-ttu-id="bb77a-191">Effectuez une **ingénierie de fonctionnalité** pour transformer les données afin de les utiliser efficacement pour l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="bb77a-191">Conduct some **feature engineering** to transform the data so that it can be used effectively for machine learning.</span></span> <span data-ttu-id="bb77a-192">L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques** car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres.</span><span class="sxs-lookup"><span data-stu-id="bb77a-192">The algorithm that trains the model requires **numeric** features, you transform the categorical data (`VendorId`, `RateCode`, and `PaymentType`) into numbers.</span></span> <span data-ttu-id="bb77a-193">La fonction `CategoricalOneHotVectorizer()` attribue une clé numérique aux valeurs de chacune de ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="bb77a-193">The `CategoricalOneHotVectorizer()` function assigns a numeric key to the values in each of these columns.</span></span> <span data-ttu-id="bb77a-194">Transformez vos données en ajoutant ce code :</span><span class="sxs-lookup"><span data-stu-id="bb77a-194">Transform your data by adding this code:</span></span>

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

<span data-ttu-id="bb77a-195">La dernière étape de la préparation des données combine toutes vos **fonctionnalités** dans un vecteur à l’aide de la fonction `ColumnConcatenator()`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-195">The last step in data preparation combines all of your **features** into one vector using the `ColumnConcatenator()` function.</span></span> <span data-ttu-id="bb77a-196">Cette étape nécessaire permet à l’algorithme de traiter facilement vos fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bb77a-196">This necessary step helps the algorithm easily process your features.</span></span> <span data-ttu-id="bb77a-197">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-197">Add the following code:</span></span>

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

<span data-ttu-id="bb77a-198">Notez que la colonne `trip_time_in_secs` n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="bb77a-198">Notice that the `trip_time_in_secs` column isn't included.</span></span> <span data-ttu-id="bb77a-199">Vous avez déterminé que cette fonctionnalité de prévision n’est pas utile.</span><span class="sxs-lookup"><span data-stu-id="bb77a-199">You already determined that it isn't a useful prediction feature.</span></span>

> [!NOTE]
> <span data-ttu-id="bb77a-200">Ces étapes doivent être ajoutées au pipeline dans l’ordre spécifié ci-dessus pour garantir une exécution réussie.</span><span class="sxs-lookup"><span data-stu-id="bb77a-200">These steps must be added to Pipeline in the order specified above for successful execution.</span></span>

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="bb77a-201">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-201">Choose a learning algorithm</span></span>

<span data-ttu-id="bb77a-202">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="bb77a-202">After adding the data to the pipeline and transforming it into the correct input format, you select a learning algorithm (**learner**).</span></span> <span data-ttu-id="bb77a-203">L’algorithme d’apprentissage forme le modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-203">The learning algorithm trains the model.</span></span> <span data-ttu-id="bb77a-204">Vous avez choisi une **tâche de régression** pour ce problème. Par conséquent, vous ajoutez un apprenant appelé `FastTreeRegressor()` au pipeline qui utilise un **boosting de gradient**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-204">You chose a **regression task** for this problem, so you add a learner called `FastTreeRegressor()` to the pipeline that utilizes **gradient boosting**.</span></span>

<span data-ttu-id="bb77a-205">Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="bb77a-205">Gradient boosting is a machine learning technique for regression problems.</span></span> <span data-ttu-id="bb77a-206">Il génère chaque arbre de régression étape par étape.</span><span class="sxs-lookup"><span data-stu-id="bb77a-206">It builds each regression tree in a step-wise fashion.</span></span> <span data-ttu-id="bb77a-207">Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine.</span><span class="sxs-lookup"><span data-stu-id="bb77a-207">It uses a pre-defined loss function to measure the error in each step and correct for it in the next.</span></span> <span data-ttu-id="bb77a-208">Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces.</span><span class="sxs-lookup"><span data-stu-id="bb77a-208">The result is a prediction model that is actually an ensemble of weaker prediction models.</span></span> <span data-ttu-id="bb77a-209">Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span><span class="sxs-lookup"><span data-stu-id="bb77a-209">For more information about gradient boosting, see [Boosted Decision Tree Regression](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).</span></span>

<span data-ttu-id="bb77a-210">Ajoutez le code suivant dans la méthode `Train()`, après le code de traitement des données ajouté à la dernière étape :</span><span class="sxs-lookup"><span data-stu-id="bb77a-210">Add the following code into the `Train()` method following the data processing code added in the last step:</span></span>

```csharp
pipeline.Add(new FastTreeRegressor());
```

<span data-ttu-id="bb77a-211">Vous avez ajouté toutes les étapes précédentes au pipeline en tant qu’instructions individuelles, mais C# propose une syntaxe d’initialisation de collection pratique qui facilite la création et l’initialisation du pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb77a-211">You added all the preceding steps to the pipeline as individual statements, but C# has a handy collection initialization syntax that makes it simpler to create and initialize the pipeline.</span></span> <span data-ttu-id="bb77a-212">Remplacez le code que vous avez ajouté à la méthode `Train()` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-212">Replace the code you added so far to the `Train()` method with the following code:</span></span>

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a><span data-ttu-id="bb77a-213">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-213">Train the model</span></span>

<span data-ttu-id="bb77a-214">La dernière étape consiste à effectuer l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-214">The final step is to train the model.</span></span> <span data-ttu-id="bb77a-215">À ce stade, rien dans le pipeline n’a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="bb77a-215">Until this point, nothing in the pipeline has been executed.</span></span> <span data-ttu-id="bb77a-216">La fonction `pipeline.Train<T_Input, T_Output>()` sélectionne le type de classe `TaxiTrip` prédéfini et génère un type `TaxiTripFarePrediction`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-216">The `pipeline.Train<T_Input, T_Output>()` function takes in the pre-defined `TaxiTrip` class type and outputs a `TaxiTripFarePrediction` type.</span></span> <span data-ttu-id="bb77a-217">Ajoutez cette dernière partie de code à la fonction `Train()` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-217">Add this final piece of code into the `Train()` function:</span></span>

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

<span data-ttu-id="bb77a-218">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="bb77a-218">And that's it!</span></span> <span data-ttu-id="bb77a-219">Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York.</span><span class="sxs-lookup"><span data-stu-id="bb77a-219">You have successfully trained a machine learning model that can predict taxi fares in NYC.</span></span> <span data-ttu-id="bb77a-220">Examinons maintenant le niveau de précision de votre modèle et comment l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb77a-220">Now take a look to understand how accurate your model is and learn how to consume it.</span></span>

## <a name="save-the-model"></a><span data-ttu-id="bb77a-221">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-221">Save the model</span></span>

<span data-ttu-id="bb77a-222">Avant de passer à l’étape suivante, enregistrez votre modèle dans un fichier .zip, en ajoutant le code suivant à la fin de votre fonction `Train()` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-222">Before you go onto the next step, save your model to a .zip file by adding the following code at the end of your `Train()` function:</span></span>

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

<span data-ttu-id="bb77a-223">L’ajout de l’instruction `await` à l’appel `model.WriteAsync()` signifie que la méthode `Train()` doit être remplacée par une méthode asynchrone qui retourne un élément `Task`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-223">Adding the `await` statement to the `model.WriteAsync()` call means that the `Train()` method must be changed to an async method that returns a `Task`.</span></span> <span data-ttu-id="bb77a-224">Modifiez la signature de `Train`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-224">Modify the signature of `Train` as shown in the following code:</span></span>

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

<span data-ttu-id="bb77a-225">La modification du type de retour de la méthode `Train` signifie que vous devez ajouter un élément `await` au code qui appelle `Train` dans la méthode `Main`, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-225">Changing the return type of the `Train` method means you have to add an `await` to the code that calls `Train` in the `Main` method as shown in the following code:</span></span>

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

<span data-ttu-id="bb77a-226">L’ajout d’un élément `await` à votre méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-226">Adding an `await` in your `Main` method means the `Main` method must have the `async` modifier and return a `Task`:</span></span>

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

<span data-ttu-id="bb77a-227">Vous devez également ajouter l'instruction suivante en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="bb77a-227">You also need to add the following using statement at the top of the file:</span></span>

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

<span data-ttu-id="bb77a-228">Comme la méthode `async Main` constitue une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bb77a-228">Because the `async Main` method is a new feature in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span>
<span data-ttu-id="bb77a-229">Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-229">To do that, right-click on the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="bb77a-230">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-230">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="bb77a-231">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="bb77a-231">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="bb77a-232">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-232">Select the **OK** button.</span></span>

## <a name="evaluate-the-model"></a><span data-ttu-id="bb77a-233">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-233">Evaluate the model</span></span>

<span data-ttu-id="bb77a-234">L’évaluation est le processus de vérification du fonctionnement du modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-234">Evaluation is the process of checking how well the model works.</span></span> <span data-ttu-id="bb77a-235">Il est important que votre modèle effectue des prévisions correctes sur les données qu’il n’a pas utilisées lors de son apprentissage.</span><span class="sxs-lookup"><span data-stu-id="bb77a-235">It's important that your model makes good predictions on data that it didn't use when it was trained.</span></span> <span data-ttu-id="bb77a-236">Pour cela, vous pouvez fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme vous l’avez fait dans ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="bb77a-236">One way to do this is by splitting the data into train and test datasets, as you did in this tutorial.</span></span> <span data-ttu-id="bb77a-237">Maintenant que vous avez formé le modèle avec les données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="bb77a-237">Now that you've trained the model on the train data, you can see how well it performs on the test data.</span></span>

<span data-ttu-id="bb77a-238">Revenez à votre fonction `Main` et ajoutez le code suivant sous l’appel à la méthode `Train()` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-238">Go back to your `Main` function and add the following code beneath the call to the `Train()`method:</span></span>

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

<span data-ttu-id="bb77a-239">La fonction `Evaluate()` évalue votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-239">The `Evaluate()` function evaluates your model.</span></span> <span data-ttu-id="bb77a-240">Créez cette fonction sous `Train()`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-240">Create that function below `Train()`.</span></span> <span data-ttu-id="bb77a-241">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-241">Add the following code:</span></span>

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

<span data-ttu-id="bb77a-242">Chargez les données de test à l’aide de la fonction `TextLoader()`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-242">Load the test data using the `TextLoader()` function.</span></span> <span data-ttu-id="bb77a-243">Ajoutez le code suivant à la méthode `Evaluate()` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-243">Add the following code into the `Evaluate()` method:</span></span>

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

<span data-ttu-id="bb77a-244">Ajoutez le code suivant pour évaluer le modèle et produire les métriques pour celui-ci :</span><span class="sxs-lookup"><span data-stu-id="bb77a-244">Add the following code to evaluate the model and produce the metrics for it:</span></span>

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

<span data-ttu-id="bb77a-245">RMS est une métrique permettant d’évaluer les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="bb77a-245">RMS is one metric for evaluating regression problems.</span></span> <span data-ttu-id="bb77a-246">Plus sa valeur est faible, meilleur est votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-246">The lower it is, the better your model.</span></span> <span data-ttu-id="bb77a-247">Ajoutez le code suivant à la fonction `Evaluate()` afin d’imprimer la métrique RMS pour votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-247">Add the following code into the `Evaluate()` function to print the RMS for your model.</span></span>

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

<span data-ttu-id="bb77a-248">RSquared est une autre métrique permettant d’évaluer les problèmes de régression.</span><span class="sxs-lookup"><span data-stu-id="bb77a-248">RSquared is another metric for evaluating regression problems.</span></span> <span data-ttu-id="bb77a-249">RSquared sera une valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="bb77a-249">RSquared will be a value between 0 and 1.</span></span> <span data-ttu-id="bb77a-250">Plus cette valeur est proche de 1, meilleur est votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-250">The closer you are to 1, the better your model.</span></span> <span data-ttu-id="bb77a-251">Ajoutez le code suivant à la fonction `Evaluate()` afin d’imprimer la valeur RSquared pour votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bb77a-251">Add the following code into the `Evaluate()` function to print the RSquared value for your model.</span></span>

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="bb77a-252">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="bb77a-252">Use the model for predictions</span></span>

<span data-ttu-id="bb77a-253">Créez maintenant une classe qui contiendra les scénarios de test que vous pouvez utiliser pour vérifier le bon fonctionnement de votre modèle :</span><span class="sxs-lookup"><span data-stu-id="bb77a-253">Next, create a class to house test scenarios that you can use to make sure your model is working correctly:</span></span>

1. <span data-ttu-id="bb77a-254">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-254">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="bb77a-255">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestTrips.cs*.</span><span class="sxs-lookup"><span data-stu-id="bb77a-255">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestTrips.cs*.</span></span> <span data-ttu-id="bb77a-256">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="bb77a-256">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="bb77a-257">Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="bb77a-257">Modify the class to be static like in the following example:</span></span>

[!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

<span data-ttu-id="bb77a-258">Ce tutoriel utilise une course test au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="bb77a-258">This tutorial uses one test trip within this class.</span></span> <span data-ttu-id="bb77a-259">Plus tard, vous pourrez ajouter d’autres scénarios pour effectuer des essais avec cet exemple.</span><span class="sxs-lookup"><span data-stu-id="bb77a-259">Later you can add other scenarios to experiment with this sample.</span></span> <span data-ttu-id="bb77a-260">Ajoutez le code suivant à la classe `TestTrips` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-260">Add the following code into the `TestTrips` class:</span></span>

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

<span data-ttu-id="bb77a-261">Le prix réel de la course est de 29,5, mais utilisez la valeur 0 comme espace réservé.</span><span class="sxs-lookup"><span data-stu-id="bb77a-261">This trip's actual fare is 29.5, but use 0 as a placeholder.</span></span> <span data-ttu-id="bb77a-262">L’algorithme d’apprentissage automatique prédit le prix.</span><span class="sxs-lookup"><span data-stu-id="bb77a-262">The machine learning algorithm will predict the fare.</span></span>

<span data-ttu-id="bb77a-263">Ajoutez le code suivant à votre fonction `Main`.</span><span class="sxs-lookup"><span data-stu-id="bb77a-263">Add the following code in your `Main` function.</span></span> <span data-ttu-id="bb77a-264">Il teste votre modèle à l’aide des données `TestTrip` :</span><span class="sxs-lookup"><span data-stu-id="bb77a-264">It tests out your model using the `TestTrip` data:</span></span>

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

<span data-ttu-id="bb77a-265">Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.</span><span class="sxs-lookup"><span data-stu-id="bb77a-265">Run the program to see the predicted taxi fare for your test case.</span></span>

<span data-ttu-id="bb77a-266">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="bb77a-266">Congratulations!</span></span> <span data-ttu-id="bb77a-267">Vous avez correctement créé un modèle d’apprentissage automatique pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez testé.</span><span class="sxs-lookup"><span data-stu-id="bb77a-267">You've now successfully built a machine learning model for predicting taxi fares, evaluated its accuracy, and tested it.</span></span> <span data-ttu-id="bb77a-268">Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).</span><span class="sxs-lookup"><span data-stu-id="bb77a-268">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction) repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb77a-269">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="bb77a-269">Next steps</span></span>

<span data-ttu-id="bb77a-270">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="bb77a-270">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="bb77a-271">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="bb77a-271">Understand the problem</span></span>
> * <span data-ttu-id="bb77a-272">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="bb77a-272">Select the appropriate machine learning task</span></span>
> * <span data-ttu-id="bb77a-273">Préparer et comprendre vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-273">Prepare and understand your data</span></span>
> * <span data-ttu-id="bb77a-274">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-274">Create a learning pipeline</span></span>
> * <span data-ttu-id="bb77a-275">Charger et transformer vos données</span><span class="sxs-lookup"><span data-stu-id="bb77a-275">Load and transform your data</span></span>
> * <span data-ttu-id="bb77a-276">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="bb77a-276">Choose a learning algorithm</span></span>
> * <span data-ttu-id="bb77a-277">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-277">Train the model</span></span>
> * <span data-ttu-id="bb77a-278">Évaluer le modèle</span><span class="sxs-lookup"><span data-stu-id="bb77a-278">Evaluate the model</span></span>
> * <span data-ttu-id="bb77a-279">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="bb77a-279">Use the model for predictions</span></span>

<span data-ttu-id="bb77a-280">Consultez notre référentiel GitHub pour continuer l’apprentissage et obtenir d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="bb77a-280">Check out our GitHub repository to continue learning and find more samples.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="bb77a-281">Référentiel GitHub dotnet/machinelearning</span><span class="sxs-lookup"><span data-stu-id="bb77a-281">dotnet/machinelearning GitHub repository</span></span>](https://github.com/dotnet/machinelearning/)
