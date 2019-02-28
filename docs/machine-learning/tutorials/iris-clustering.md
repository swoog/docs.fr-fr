---
title: Créer un cluster de fleurs d’iris à l’aide d’un apprenant de clustering - ML.NET
description: Découvrez comment utiliser ML.NET dans un scénario de clustering
author: pkulikov
ms.author: johalex
ms.date: 02/19/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: fcbd75597d6fdce8dceffc9d47d06cc13dd11570
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56664469"
---
# <a name="tutorial-cluster-iris-flowers-using-a-clustering-learner-with-mlnet"></a><span data-ttu-id="f4ef8-103">Tutoriel : créer un cluster de fleurs d’iris à l’aide d’un apprenant de clustering avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="f4ef8-103">Tutorial: Cluster iris flowers using a clustering learner with ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="f4ef8-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="f4ef8-105">Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="f4ef8-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="f4ef8-106">Ce tutoriel montre comment utiliser ML.NET pour générer un [modèle de clustering](../resources/tasks.md#clustering) pour le [jeu de données Iris](https://en.wikipedia.org/wiki/Iris_flower_data_set).</span><span class="sxs-lookup"><span data-stu-id="f4ef8-106">This tutorial illustrates how to use ML.NET to build a [clustering model](../resources/tasks.md#clustering) for the [iris flower data set](https://en.wikipedia.org/wiki/Iris_flower_data_set).</span></span>

<span data-ttu-id="f4ef8-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="f4ef8-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="f4ef8-108">Understand the problem</span></span>
> - <span data-ttu-id="f4ef8-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="f4ef8-109">Select the appropriate machine learning task</span></span>
> - <span data-ttu-id="f4ef8-110">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-110">Prepare the data</span></span>
> - <span data-ttu-id="f4ef8-111">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-111">Load and transform the data</span></span>
> - <span data-ttu-id="f4ef8-112">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="f4ef8-112">Choose a learning algorithm</span></span>
> - <span data-ttu-id="f4ef8-113">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="f4ef8-113">Train the model</span></span>
> - <span data-ttu-id="f4ef8-114">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="f4ef8-114">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4ef8-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f4ef8-115">Prerequisites</span></span>

- <span data-ttu-id="f4ef8-116">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-116">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="f4ef8-117">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="f4ef8-117">Understand the problem</span></span>

<span data-ttu-id="f4ef8-118">Ce problème concerne la division de l’ensemble des iris en différents groupes basés sur les caractéristiques de la fleur.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-118">This problem is about dividing the set of iris flowers in different groups based on the flower features.</span></span> <span data-ttu-id="f4ef8-119">Ces caractéristiques sont la longueur et la largeur d’un sépale, ainsi que la longueur et la largeur d’un pétale.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-119">Those features are the length and width of a sepal and the length and width of a petal.</span></span> <span data-ttu-id="f4ef8-120">Pour ce tutoriel, supposons que le type de chaque fleur est inconnu.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-120">For this tutorial, assume that the type of each flower is unknown.</span></span> <span data-ttu-id="f4ef8-121">Vous souhaitez connaître la structure d’un jeu de données à partir des caractéristiques et prédire la façon dont une instance de données s’intègre à cette structure.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-121">You want to learn the structure of a data set from the features and predict how a data instance fits this structure.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="f4ef8-122">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="f4ef8-122">Select the appropriate machine learning task</span></span>

<span data-ttu-id="f4ef8-123">Comme vous ne savez pas à quel groupe appartient chaque fleur, vous choisissez la tâche [Apprentissage automatique non supervisé](../resources/glossary.md#unsupervised-machine-learning).</span><span class="sxs-lookup"><span data-stu-id="f4ef8-123">As you don't know to which group each flower belongs to, you choose the [unsupervised machine learning](../resources/glossary.md#unsupervised-machine-learning) task.</span></span> <span data-ttu-id="f4ef8-124">Pour diviser un jeu de données en groupes de telle sorte que les éléments dans le même groupe soient plus similaires les uns aux autres qu’à ceux des autres groupes, utilisez une tâche d’apprentissage automatique de [clustering](../resources/tasks.md#clustering).</span><span class="sxs-lookup"><span data-stu-id="f4ef8-124">To divide a data set in groups in such a way that elements in the same group are more similar to each other than to those in other groups, use a [clustering](../resources/tasks.md#clustering) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="f4ef8-125">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="f4ef8-125">Create a console application</span></span>

1. <span data-ttu-id="f4ef8-126">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-126">Open Visual Studio 2017.</span></span> <span data-ttu-id="f4ef8-127">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-127">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="f4ef8-128">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-128">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="f4ef8-129">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-129">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="f4ef8-130">Dans la zone de texte **Nom**, tapez « IrisFlowerClustering », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-130">In the **Name** text box, type "IrisFlowerClustering" and then select the **OK** button.</span></span>

1. <span data-ttu-id="f4ef8-131">Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-131">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="f4ef8-132">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-132">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="f4ef8-133">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-133">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="f4ef8-134">Installez le package NuGet **Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-134">Install the **Microsoft.ML** NuGet package:</span></span>

    <span data-ttu-id="f4ef8-135">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-135">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="f4ef8-136">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-136">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="f4ef8-137">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-137">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-the-data"></a><span data-ttu-id="f4ef8-138">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-138">Prepare the data</span></span>

1. <span data-ttu-id="f4ef8-139">Téléchargez le jeu de données [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) et enregistrez-le dans le dossier *Data* que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-139">Download the [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) data set and save it to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="f4ef8-140">Pour plus d’informations sur le jeu de données Iris, consultez la page Wikipédia [Iris de Fisher](https://en.wikipedia.org/wiki/Iris_flower_data_set) et la page [Iris Data Set](https://archive.ics.uci.edu/ml/datasets/Iris), qui est la source du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-140">For more information about the iris data set, see the [Iris flower data set](https://en.wikipedia.org/wiki/Iris_flower_data_set) Wikipedia page and the [Iris Data Set](https://archive.ics.uci.edu/ml/datasets/Iris) page, which is the source of the data set.</span></span>

1. <span data-ttu-id="f4ef8-141">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier *iris.data* et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-141">In **Solution Explorer**, right-click the *iris.data* file and select **Properties**.</span></span> <span data-ttu-id="f4ef8-142">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-142">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

<span data-ttu-id="f4ef8-143">Le fichier *iris.data* contient cinq colonnes qui représentent :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-143">The *iris.data* file contains five columns that represent:</span></span>

- <span data-ttu-id="f4ef8-144">la longueur des sépales en centimètres</span><span class="sxs-lookup"><span data-stu-id="f4ef8-144">sepal length in centimetres</span></span>
- <span data-ttu-id="f4ef8-145">la largeur des sépales en centimètres</span><span class="sxs-lookup"><span data-stu-id="f4ef8-145">sepal width in centimetres</span></span>
- <span data-ttu-id="f4ef8-146">la longueur des pétales en centimètres</span><span class="sxs-lookup"><span data-stu-id="f4ef8-146">petal length in centimetres</span></span>
- <span data-ttu-id="f4ef8-147">la largeur des pétales en centimètres</span><span class="sxs-lookup"><span data-stu-id="f4ef8-147">petal width in centimetres</span></span>
- <span data-ttu-id="f4ef8-148">le type d’iris</span><span class="sxs-lookup"><span data-stu-id="f4ef8-148">type of iris flower</span></span>

<span data-ttu-id="f4ef8-149">Dans le cadre de cet exemple de clustering, ce tutoriel ignore la dernière colonne.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-149">For the sake of the clustering example, this tutorial ignores the last column.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="f4ef8-150">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-150">Create data classes</span></span>

<span data-ttu-id="f4ef8-151">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-151">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="f4ef8-152">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-152">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="f4ef8-153">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et définissez la valeur du champ **Nom** sur *IrisData.cs*.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-153">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *IrisData.cs*.</span></span> <span data-ttu-id="f4ef8-154">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-154">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="f4ef8-155">Ajoutez la directive `using` suivante au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-155">Add the following `using` directive to the new file:</span></span>

   [!code-csharp[Add necessary usings](~/samples/machine-learning/tutorials/IrisFlowerClustering/IrisData.cs#Usings)]

<span data-ttu-id="f4ef8-156">Supprimez la définition de classe existante et ajoutez le code suivant, qui définit les classes `IrisData` et `ClusterPrediction`, au fichier *IrisData.cs* :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-156">Remove the existing class definition and add the following code, which defines the classes `IrisData` and `ClusterPrediction`, to the *IrisData.cs* file:</span></span>

[!code-csharp[Define data classes](~/samples/machine-learning/tutorials/IrisFlowerClustering/IrisData.cs#ClassDefinitions)]

<span data-ttu-id="f4ef8-157">`IrisData` est la classe des données d’entrée et a des définitions pour chaque caractéristique du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-157">`IrisData` is the input data class and has definitions for each feature from the data set.</span></span> <span data-ttu-id="f4ef8-158">Utilisez l’attribut [LoadColumn](xref:Microsoft.ML.Data.LoadColumnAttribute) pour spécifier les index des colonnes sources dans le fichier de jeu de données.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-158">Use the [LoadColumn](xref:Microsoft.ML.Data.LoadColumnAttribute) attribute to specify the indices of the source columns in the data set file.</span></span>

<span data-ttu-id="f4ef8-159">La classe `ClusterPrediction` représente la sortie du modèle de clustering appliqué à une instance `IrisData`.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-159">The `ClusterPrediction` class represents the output of the clustering model applied to an `IrisData` instance.</span></span> <span data-ttu-id="f4ef8-160">Utilisez l’attribut [ColumnName](xref:Microsoft.ML.Data.ColumnNameAttribute) pour lier les champs `PredictedClusterId` et `Distances` aux colonnes **PredictedLabel** et **Score** respectivement.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-160">Use the [ColumnName](xref:Microsoft.ML.Data.ColumnNameAttribute) attribute to bind the `PredictedClusterId` and `Distances` fields to the **PredictedLabel** and **Score** columns respectively.</span></span> <span data-ttu-id="f4ef8-161">Dans le cas de la tâche de clustering, ces colonnes ont la signification suivante :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-161">In case of the clustering task those columns have the following meaning:</span></span>

- <span data-ttu-id="f4ef8-162">La colonne **PredictedLabel** contient l’ID du cluster prédit.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-162">**PredictedLabel** column contains the ID of the predicted cluster.</span></span>
- <span data-ttu-id="f4ef8-163">La colonne **Score** contient un tableau avec les distances Euclidiennes au carré jusqu’aux centroïdes des clusters.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-163">**Score** column contains an array with squared Euclidean distances to the cluster centroids.</span></span> <span data-ttu-id="f4ef8-164">La longueur du tableau est égale au nombre de clusters.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-164">The array length is equal to the number of clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="f4ef8-165">Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-165">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="f4ef8-166">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="f4ef8-166">Define data and model paths</span></span>

<span data-ttu-id="f4ef8-167">Revenez au fichier *Program.cs* et ajoutez deux champs pour contenir les chemins du fichier de jeu de données et du fichier pour enregistrer le modèle :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-167">Go back to the *Program.cs* file and add two fields to hold the paths to the data set file and to the file to save the model:</span></span>

- <span data-ttu-id="f4ef8-168">`_dataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-168">`_dataPath` contains the path to the file with the data set used to train the model.</span></span>
- <span data-ttu-id="f4ef8-169">`_modelPath` contient le chemin du fichier où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-169">`_modelPath` contains the path to the file where the trained model is stored.</span></span>

<span data-ttu-id="f4ef8-170">Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-170">Add the following code right above the `Main` method to specify those paths:</span></span>

[!code-csharp[Initialize paths](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#Paths)]

<span data-ttu-id="f4ef8-171">Pour compiler le code précédent, ajoutez les directives `using` suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-171">To make the preceding code compile, add the following `using` directives at the top of the *Program.cs* file:</span></span>

[!code-csharp[Add usings for paths](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#UsingsForPaths)]

## <a name="create-ml-context"></a><span data-ttu-id="f4ef8-172">Créer un contexte ML</span><span class="sxs-lookup"><span data-stu-id="f4ef8-172">Create ML context</span></span>

<span data-ttu-id="f4ef8-173">Ajoutez les directives `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-173">Add the following additional `using` directives to the top of the *Program.cs* file:</span></span>

[!code-csharp[Add Microsoft.ML usings](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#MLUsings)]

<span data-ttu-id="f4ef8-174">Dans la méthode `Main`, remplacez la ligne `Console.WriteLine("Hello World!");` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-174">In the `Main` method, replace the `Console.WriteLine("Hello World!");` line with the following code:</span></span>

[!code-csharp[Create ML context](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#CreateContext)]

<span data-ttu-id="f4ef8-175">La classe <xref:Microsoft.ML.MLContext?displayProperty=nameWithType> représente l’environnement Machine Learning et fournit des mécanismes de journalisation et des points d’entrée pour le chargement des données, l’apprentissage du modèle, la prédiction et d’autres tâches.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-175">The <xref:Microsoft.ML.MLContext?displayProperty=nameWithType> class represents the machine learning environment and provides mechanisms for logging and entry points for data loading, model training, prediction, and other tasks.</span></span> <span data-ttu-id="f4ef8-176">Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-176">This is comparable conceptually to using `DbContext` in Entity Framework.</span></span>

## <a name="setup-data-loading"></a><span data-ttu-id="f4ef8-177">Configurer le chargement des données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-177">Setup data loading</span></span>

<span data-ttu-id="f4ef8-178">Ajoutez le code suivant à la méthode `Main` pour configurer la façon de charger des données :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-178">Add the following code to the `Main` method to setup the way to load data:</span></span>

[!code-csharp[Create text loader](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#SetupTextLoader)]

<span data-ttu-id="f4ef8-179">Utilisez la méthode [générique `CreateTextLoader`](xref:Microsoft.ML.TextLoaderSaverCatalog.CreateTextLoader%60%601(Microsoft.ML.DataOperationsCatalog,System.Boolean,System.Char,System.Boolean,System.Boolean,System.Boolean)) pour déduire le schéma du jeu de données à partir de la définition de classe `IrisData`.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-179">Use the [generic `CreateTextLoader`](xref:Microsoft.ML.TextLoaderSaverCatalog.CreateTextLoader%60%601(Microsoft.ML.DataOperationsCatalog,System.Boolean,System.Char,System.Boolean,System.Boolean,System.Boolean)) method to infer the dataset schema from the `IrisData` class definition.</span></span>

<span data-ttu-id="f4ef8-180">Utilisez l’instance <xref:Microsoft.ML.Data.TextLoader> pour créer une instance <xref:Microsoft.Data.DataView.IDataView>, qui représente la source de données du jeu de données d’apprentissage :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-180">Use instantiated <xref:Microsoft.ML.Data.TextLoader> instance to create an <xref:Microsoft.Data.DataView.IDataView> instance, which represents the data source for the training data set:</span></span>

[!code-csharp[Create IDataView](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#CreateDataView)]

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="f4ef8-181">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="f4ef8-181">Create a learning pipeline</span></span>

<span data-ttu-id="f4ef8-182">Pour ce tutoriel, le pipeline d’apprentissage de la tâche de clustering comprend les deux étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-182">For this tutorial, the learning pipeline of the clustering task comprises two following steps:</span></span>

- <span data-ttu-id="f4ef8-183">concaténer des colonnes chargées en une seule colonne **Fonctionnalités**, utilisée par un formateur en clustering ;</span><span class="sxs-lookup"><span data-stu-id="f4ef8-183">concatenate loaded columns into one **Features** column, which is used by a clustering trainer;</span></span>
- <span data-ttu-id="f4ef8-184">utiliser un formateur <xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer> pour former le modèle à l’aide de l’algorithme de clustering k-means++.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-184">use a <xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer> trainer to train the model using the k-means++ clustering algorithm.</span></span>

<span data-ttu-id="f4ef8-185">Ajoutez le code suivant à la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-185">Add the following code to the `Main` method:</span></span>

[!code-csharp[Create pipeline](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#CreatePipeline)]

<span data-ttu-id="f4ef8-186">Le code spécifie que le jeu de données doit être divisé en trois clusters.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-186">The code specifies that the data set should be split in three clusters.</span></span>

## <a name="train-the-model"></a><span data-ttu-id="f4ef8-187">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="f4ef8-187">Train the model</span></span>

<span data-ttu-id="f4ef8-188">Les étapes ajoutées dans les sections précédentes ont préparé le pipeline pour l’apprentissage, toutefois, aucune n’a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-188">The steps added in the preceding sections prepared the pipeline for training, however, none have been executed.</span></span> <span data-ttu-id="f4ef8-189">Ajoutez la ligne suivante à la méthode `Main` pour effectuer le chargement des données et l’apprentissage du modèle :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-189">Add the following line to the `Main` method to perform data loading and model training:</span></span>

[!code-csharp[Train the model](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#TrainModel)]

### <a name="save-the-model"></a><span data-ttu-id="f4ef8-190">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="f4ef8-190">Save the model</span></span>

<span data-ttu-id="f4ef8-191">À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-191">At this point, you have a model that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="f4ef8-192">Pour enregistrer votre modèle dans un fichier .zip, ajoutez le code suivant à la méthode `Main` :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-192">To save your model to a .zip file, add the following code to the `Main` method:</span></span>

[!code-csharp[Save the model](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#SaveModel)]

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="f4ef8-193">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="f4ef8-193">Use the model for predictions</span></span>

<span data-ttu-id="f4ef8-194">Pour effectuer des prédictions, utilisez la classe <xref:Microsoft.ML.PredictionEngine%602> qui prend des instances du type d’entrée via le pipeline de transformateur et produit des instances du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-194">To make predictions, use the <xref:Microsoft.ML.PredictionEngine%602> class that takes instances of the input type through the transformer pipeline and produces instances of the output type.</span></span> <span data-ttu-id="f4ef8-195">Ajoutez la ligne suivante à la méthode `Main` pour créer une instance de cette classe :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-195">Add the following line to the `Main` method to create an instance of that class:</span></span>

[!code-csharp[Create predictor](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#Predictor)]

<span data-ttu-id="f4ef8-196">Créez la classe `TestIrisData` qui contiendra les instances de données de test :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-196">Create the `TestIrisData` class to house test data instances:</span></span>

1. <span data-ttu-id="f4ef8-197">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-197">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="f4ef8-198">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestIrisData.cs*.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-198">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestIrisData.cs*.</span></span> <span data-ttu-id="f4ef8-199">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-199">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="f4ef8-200">Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-200">Modify the class to be static like in the following example:</span></span>

   [!code-csharp[Make class static](~/samples/machine-learning/tutorials/IrisFlowerClustering/TestIrisData.cs#Static)]

<span data-ttu-id="f4ef8-201">Ce tutoriel présente une instance de données d’iris au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-201">This tutorial introduces one iris data instance within this class.</span></span> <span data-ttu-id="f4ef8-202">Vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-202">You can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="f4ef8-203">Ajoutez le code suivant à la classe `TestIrisData` :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-203">Add the following code into the `TestIrisData` class:</span></span>

[!code-csharp[Test data](~/samples/machine-learning/tutorials/IrisFlowerClustering/TestIrisData.cs#TestData)]

<span data-ttu-id="f4ef8-204">Pour déterminer à quel cluster l’élément spécifié appartient, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main`:</span><span class="sxs-lookup"><span data-stu-id="f4ef8-204">To find out the cluster to which the specified item belongs to, go back to the *Program.cs* file and add the following code into the `Main` method:</span></span>

[!code-csharp[Predict and output results](~/samples/machine-learning/tutorials/IrisFlowerClustering/Program.cs#PredictionExample)]

<span data-ttu-id="f4ef8-205">Exécutez le programme pour voir quel cluster contient l’instance de données spécifiée et les distances au carré à partir de cette instance jusqu’aux centroïdes des clusters.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-205">Run the program to see which cluster contains the specified data instance and squared distances from that instance to the cluster centroids.</span></span> <span data-ttu-id="f4ef8-206">Vous devriez obtenir les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-206">Your results should be similar to the following:</span></span>

```text
Cluster: 2
Distances: 11.69127 0.02159119 25.59896
```

<span data-ttu-id="f4ef8-207">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="f4ef8-207">Congratulations!</span></span> <span data-ttu-id="f4ef8-208">Vous venez de créer un modèle d’apprentissage automatique de clustering des iris et l’avez utilisé pour réaliser des prédictions.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-208">You've now successfully built a machine learning model for iris clustering and used it to make predictions.</span></span> <span data-ttu-id="f4ef8-209">Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisFlowerClustering).</span><span class="sxs-lookup"><span data-stu-id="f4ef8-209">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisFlowerClustering) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f4ef8-210">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f4ef8-210">Next steps</span></span>

<span data-ttu-id="f4ef8-211">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="f4ef8-211">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="f4ef8-212">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="f4ef8-212">Understand the problem</span></span>
> - <span data-ttu-id="f4ef8-213">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="f4ef8-213">Select the appropriate machine learning task</span></span>
> - <span data-ttu-id="f4ef8-214">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-214">Prepare the data</span></span>
> - <span data-ttu-id="f4ef8-215">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="f4ef8-215">Load and transform the data</span></span>
> - <span data-ttu-id="f4ef8-216">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="f4ef8-216">Choose a learning algorithm</span></span>
> - <span data-ttu-id="f4ef8-217">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="f4ef8-217">Train the model</span></span>
> - <span data-ttu-id="f4ef8-218">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="f4ef8-218">Use the model for predictions</span></span>

<span data-ttu-id="f4ef8-219">Consultez notre référentiel GitHub pour continuer l’apprentissage et obtenir d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="f4ef8-219">Check out our GitHub repository to continue learning and find more samples.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="f4ef8-220">Référentiel GitHub dotnet/machinelearning</span><span class="sxs-lookup"><span data-stu-id="f4ef8-220">dotnet/machinelearning GitHub repository</span></span>](https://github.com/dotnet/machinelearning/)
