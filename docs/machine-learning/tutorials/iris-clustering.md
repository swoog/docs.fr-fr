---
title: Créer un cluster de fleurs d’iris à l’aide d’un apprenant de clustering - ML.NET
description: Découvrez comment utiliser ML.NET dans un scénario de clustering
author: pkulikov
ms.author: johalex
ms.date: 07/02/2018
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 5bd73c774f60466daaf52215c34e7e17b5f5cc9c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53145624"
---
# <a name="tutorial-cluster-iris-flowers-using-a-clustering-learner-with-mlnet"></a><span data-ttu-id="d438f-103">Tutoriel : créer un cluster de fleurs d’iris à l’aide d’un apprenant de clustering avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="d438f-103">Tutorial: Cluster iris flowers using a clustering learner with ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="d438f-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="d438f-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="d438f-105">Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="d438f-105">For more information, see the [ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="d438f-106">Ce tutoriel montre comment utiliser ML.NET pour générer un [modèle de clustering](../resources/tasks.md#clustering) pour le [jeu de données Iris](https://en.wikipedia.org/wiki/Iris_flower_data_set).</span><span class="sxs-lookup"><span data-stu-id="d438f-106">This tutorial illustrates how to use ML.NET to build a [clustering model](../resources/tasks.md#clustering) for the [iris flower data set](https://en.wikipedia.org/wiki/Iris_flower_data_set).</span></span>

<span data-ttu-id="d438f-107">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="d438f-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="d438f-108">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d438f-108">Understand the problem</span></span>
> - <span data-ttu-id="d438f-109">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d438f-109">Select the appropriate machine learning task</span></span>
> - <span data-ttu-id="d438f-110">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-110">Prepare the data</span></span>
> - <span data-ttu-id="d438f-111">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-111">Load and transform the data</span></span>
> - <span data-ttu-id="d438f-112">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d438f-112">Choose a learning algorithm</span></span>
> - <span data-ttu-id="d438f-113">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d438f-113">Train the model</span></span>
> - <span data-ttu-id="d438f-114">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d438f-114">Use the model for predictions</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d438f-115">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d438f-115">Prerequisites</span></span>

- <span data-ttu-id="d438f-116">[Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.</span><span class="sxs-lookup"><span data-stu-id="d438f-116">[Visual Studio 2017 15.6 or later](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) with the ".NET Core cross-platform development" workload installed.</span></span>

## <a name="understand-the-problem"></a><span data-ttu-id="d438f-117">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d438f-117">Understand the problem</span></span>

<span data-ttu-id="d438f-118">Ce problème concerne la division de l’ensemble des iris en différents groupes basés sur les caractéristiques de la fleur.</span><span class="sxs-lookup"><span data-stu-id="d438f-118">This problem is about dividing the set of iris flowers in different groups based on the flower features.</span></span> <span data-ttu-id="d438f-119">Ces caractéristiques sont la longueur et la largeur d’un sépale, ainsi que la longueur et la largeur d’un pétale.</span><span class="sxs-lookup"><span data-stu-id="d438f-119">Those features are the length and width of a sepal and the length and width of a petal.</span></span> <span data-ttu-id="d438f-120">Pour ce tutoriel, supposons que le type de chaque fleur est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d438f-120">For this tutorial, assume that the type of each flower is unknown.</span></span> <span data-ttu-id="d438f-121">Vous souhaitez connaître la structure d’un jeu de données à partir des caractéristiques et prédire la façon dont une instance de données s’intègre à cette structure.</span><span class="sxs-lookup"><span data-stu-id="d438f-121">You want to learn the structure of a data set from the features and predict how a data instance fits this structure.</span></span>

## <a name="select-the-appropriate-machine-learning-task"></a><span data-ttu-id="d438f-122">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d438f-122">Select the appropriate machine learning task</span></span>

<span data-ttu-id="d438f-123">Comme vous ne savez pas à quel groupe appartient chaque fleur, vous choisissez la tâche [Apprentissage automatique non supervisé](../resources/glossary.md#unsupervised-machine-learning).</span><span class="sxs-lookup"><span data-stu-id="d438f-123">As you don't know to which group each flower belongs to, you choose the [unsupervised machine learning](../resources/glossary.md#unsupervised-machine-learning) task.</span></span> <span data-ttu-id="d438f-124">Pour diviser un jeu de données en groupes de telle sorte que les éléments dans le même groupe soient plus similaires les uns aux autres qu’à ceux des autres groupes, utilisez une tâche d’apprentissage automatique de [clustering](../resources/tasks.md#clustering).</span><span class="sxs-lookup"><span data-stu-id="d438f-124">To divide a data set in groups in such a way that elements in the same group are more similar to each other than to those in other groups, use a [clustering](../resources/tasks.md#clustering) machine learning task.</span></span>

## <a name="create-a-console-application"></a><span data-ttu-id="d438f-125">Créer une application console</span><span class="sxs-lookup"><span data-stu-id="d438f-125">Create a console application</span></span>

1. <span data-ttu-id="d438f-126">Ouvrez Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="d438f-126">Open Visual Studio 2017.</span></span> <span data-ttu-id="d438f-127">Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="d438f-127">Select **File** > **New** > **Project** from the menu bar.</span></span> <span data-ttu-id="d438f-128">Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="d438f-128">In the **New Project** dialog, select the **Visual C#** node followed by the **.NET Core** node.</span></span> <span data-ttu-id="d438f-129">Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**.</span><span class="sxs-lookup"><span data-stu-id="d438f-129">Then select the **Console App (.NET Core)** project template.</span></span> <span data-ttu-id="d438f-130">Dans la zone de texte **Nom**, tapez « IrisClustering », puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d438f-130">In the **Name** text box, type "IrisClustering" and then select the **OK** button.</span></span>

1. <span data-ttu-id="d438f-131">Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :</span><span class="sxs-lookup"><span data-stu-id="d438f-131">Create a directory named *Data* in your project to store the data set and model files:</span></span>

    <span data-ttu-id="d438f-132">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**.</span><span class="sxs-lookup"><span data-stu-id="d438f-132">In **Solution Explorer**, right-click the project and select **Add** > **New Folder**.</span></span> <span data-ttu-id="d438f-133">Tapez « Données » et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="d438f-133">Type "Data" and hit Enter.</span></span>

1. <span data-ttu-id="d438f-134">Installez le package NuGet **Microsoft.ML** :</span><span class="sxs-lookup"><span data-stu-id="d438f-134">Install the **Microsoft.ML** NuGet package:</span></span>

    <span data-ttu-id="d438f-135">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="d438f-135">In **Solution Explorer**, right-click the project and select **Manage NuGet Packages**.</span></span> <span data-ttu-id="d438f-136">Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d438f-136">Choose "nuget.org" as the Package source, select the **Browse** tab, search for **Microsoft.ML**, select that package in the list, and select the **Install** button.</span></span> <span data-ttu-id="d438f-137">Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.</span><span class="sxs-lookup"><span data-stu-id="d438f-137">Select the **OK** button on the **Preview Changes** dialog and then select the **I Accept** button on the **License Acceptance** dialog if you agree with the license terms for the packages listed.</span></span>

## <a name="prepare-the-data"></a><span data-ttu-id="d438f-138">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-138">Prepare the data</span></span>

1. <span data-ttu-id="d438f-139">Téléchargez le jeu de données [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) et enregistrez-le dans le dossier *Data* que vous avez créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="d438f-139">Download the [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) data set and save it to the *Data* folder you've created at the previous step.</span></span> <span data-ttu-id="d438f-140">Pour plus d’informations sur le jeu de données Iris, consultez la page Wikipédia [Iris de Fisher](https://en.wikipedia.org/wiki/Iris_flower_data_set) et la page [Iris Data Set](http://archive.ics.uci.edu/ml/datasets/Iris), qui est la source du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d438f-140">For more information about the iris data set, see the [Iris flower data set](https://en.wikipedia.org/wiki/Iris_flower_data_set) Wikipedia page and the [Iris Data Set](http://archive.ics.uci.edu/ml/datasets/Iris) page, which is the source of the data set.</span></span>

1. <span data-ttu-id="d438f-141">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier *iris.data* et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d438f-141">In **Solution Explorer**, right-click the *iris.data* file and select **Properties**.</span></span> <span data-ttu-id="d438f-142">Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.</span><span class="sxs-lookup"><span data-stu-id="d438f-142">Under **Advanced**, change the value of **Copy to Output Directory** to **Copy if newer**.</span></span>

<span data-ttu-id="d438f-143">Le fichier *iris.data* contient cinq colonnes qui représentent :</span><span class="sxs-lookup"><span data-stu-id="d438f-143">The *iris.data* file contains five columns that represent:</span></span>

- <span data-ttu-id="d438f-144">la longueur des sépales en centimètres</span><span class="sxs-lookup"><span data-stu-id="d438f-144">sepal length in centimetres</span></span>
- <span data-ttu-id="d438f-145">la largeur des sépales en centimètres</span><span class="sxs-lookup"><span data-stu-id="d438f-145">sepal width in centimetres</span></span>
- <span data-ttu-id="d438f-146">la longueur des pétales en centimètres</span><span class="sxs-lookup"><span data-stu-id="d438f-146">petal length in centimetres</span></span>
- <span data-ttu-id="d438f-147">la largeur des pétales en centimètres</span><span class="sxs-lookup"><span data-stu-id="d438f-147">petal width in centimetres</span></span>
- <span data-ttu-id="d438f-148">le type d’iris</span><span class="sxs-lookup"><span data-stu-id="d438f-148">type of iris flower</span></span>

<span data-ttu-id="d438f-149">Dans le cadre de cet exemple de clustering, ce tutoriel ignore la dernière colonne.</span><span class="sxs-lookup"><span data-stu-id="d438f-149">For the sake of the clustering example, this tutorial ignores the last column.</span></span>

## <a name="create-data-classes"></a><span data-ttu-id="d438f-150">Créer des classes de données</span><span class="sxs-lookup"><span data-stu-id="d438f-150">Create data classes</span></span>

<span data-ttu-id="d438f-151">Créez des classes pour les données d’entrée et les prédictions :</span><span class="sxs-lookup"><span data-stu-id="d438f-151">Create classes for the input data and the predictions:</span></span>

1. <span data-ttu-id="d438f-152">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="d438f-152">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="d438f-153">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et définissez la valeur du champ **Nom** sur *IrisData.cs*.</span><span class="sxs-lookup"><span data-stu-id="d438f-153">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *IrisData.cs*.</span></span> <span data-ttu-id="d438f-154">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d438f-154">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="d438f-155">Ajoutez la directive `using` suivante au nouveau fichier :</span><span class="sxs-lookup"><span data-stu-id="d438f-155">Add the following `using` directive to the new file:</span></span>

   [!code-csharp[Add necessary usings](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#1)]

<span data-ttu-id="d438f-156">Supprimez la définition de classe existante et ajoutez le code suivant, qui définit les classes `IrisData` et `ClusterPrediction`, au fichier *IrisData.cs* :</span><span class="sxs-lookup"><span data-stu-id="d438f-156">Remove the existing class definition and add the following code, which defines the classes `IrisData` and `ClusterPrediction`, to the *IrisData.cs* file:</span></span>

[!code-csharp[Define data classes](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#2)]

<span data-ttu-id="d438f-157">`IrisData` est la classe des données d’entrée et a des définitions pour chaque caractéristique du jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d438f-157">`IrisData` is the input data class and has definitions for each feature from the data set.</span></span> <span data-ttu-id="d438f-158">Utilisez l’attribut [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) pour spécifier les index des colonnes sources dans le fichier de jeu de données.</span><span class="sxs-lookup"><span data-stu-id="d438f-158">Use the [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) attribute to specify the indices of the source columns in the data set file.</span></span>

<span data-ttu-id="d438f-159">La classe `ClusterPrediction` représente la sortie du modèle de clustering appliqué à une instance `IrisData`.</span><span class="sxs-lookup"><span data-stu-id="d438f-159">The `ClusterPrediction` class represents the output of the clustering model applied to an `IrisData` instance.</span></span> <span data-ttu-id="d438f-160">Utilisez l’attribut [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) pour lier les champs `PredictedClusterId` et `Distances` aux colonnes **PredictedLabel** et **Score** respectivement.</span><span class="sxs-lookup"><span data-stu-id="d438f-160">Use the [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) attribute to bind the `PredictedClusterId` and `Distances` fields to the **PredictedLabel** and **Score** columns respectively.</span></span> <span data-ttu-id="d438f-161">Dans le cas de la tâche de clustering, ces colonnes ont la signification suivante :</span><span class="sxs-lookup"><span data-stu-id="d438f-161">In case of the clustering task those columns have the following meaning:</span></span>

- <span data-ttu-id="d438f-162">La colonne **PredictedLabel** contient l’ID du cluster prédit.</span><span class="sxs-lookup"><span data-stu-id="d438f-162">**PredictedLabel** column contains the ID of the predicted cluster.</span></span>
- <span data-ttu-id="d438f-163">La colonne **Score** contient un tableau avec les distances Euclidiennes au carré jusqu’aux centroïdes des clusters.</span><span class="sxs-lookup"><span data-stu-id="d438f-163">**Score** column contains an array with squared Euclidean distances to the cluster centroids.</span></span> <span data-ttu-id="d438f-164">La longueur du tableau est égale au nombre de clusters.</span><span class="sxs-lookup"><span data-stu-id="d438f-164">The array length is equal to the number of clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="d438f-165">Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.</span><span class="sxs-lookup"><span data-stu-id="d438f-165">Use the `float` type to represent floating-point values in the input and prediction data classes.</span></span>

## <a name="define-data-and-model-paths"></a><span data-ttu-id="d438f-166">Définir des chemins de données et de modèle</span><span class="sxs-lookup"><span data-stu-id="d438f-166">Define data and model paths</span></span>

<span data-ttu-id="d438f-167">Revenez au fichier *Program.cs* et ajoutez deux champs pour contenir les chemins du fichier de jeu de données et du fichier pour enregistrer le modèle :</span><span class="sxs-lookup"><span data-stu-id="d438f-167">Go back to the *Program.cs* file and add two fields to hold the paths to the data set file and to the file to save the model:</span></span>

- <span data-ttu-id="d438f-168">`_dataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d438f-168">`_dataPath` contains the path to the file with the data set used to train the model.</span></span>
- <span data-ttu-id="d438f-169">`_modelPath` contient le chemin du fichier où le modèle formé est stocké.</span><span class="sxs-lookup"><span data-stu-id="d438f-169">`_modelPath` contains the path to the file where the trained model is stored.</span></span>

<span data-ttu-id="d438f-170">Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins :</span><span class="sxs-lookup"><span data-stu-id="d438f-170">Add the following code right above the `Main` method to specify those paths:</span></span>

[!code-csharp[Initialize paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#1)]

<span data-ttu-id="d438f-171">Pour compiler le code précédent, ajoutez les directives `using` suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="d438f-171">To make the preceding code compile, add the following `using` directives at the top of the *Program.cs* file:</span></span>

[!code-csharp[Add usings for paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#2)]

## <a name="create-a-learning-pipeline"></a><span data-ttu-id="d438f-172">Créer un pipeline d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d438f-172">Create a learning pipeline</span></span>

<span data-ttu-id="d438f-173">Ajoutez les directives `using` supplémentaires suivantes en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="d438f-173">Add the following additional `using` directives to the top of the *Program.cs* file:</span></span>

[!code-csharp[Add Microsoft.ML usings](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#3)]

<span data-ttu-id="d438f-174">Dans la méthode `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d438f-174">In the `Main` method, replace the `Console.WriteLine("Hello World!")` with the following code:</span></span>

[!code-csharp[Call the Train method](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#4)]

<span data-ttu-id="d438f-175">La méthode `Train` effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d438f-175">The `Train` method trains the model.</span></span> <span data-ttu-id="d438f-176">Créez cette méthode juste en dessous de la méthode `Main`, en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d438f-176">Create that method just below the `Main` method, using the following code:</span></span>

```csharp
private static PredictionModel<IrisData, ClusterPrediction> Train()
{

}
```

<span data-ttu-id="d438f-177">Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d438f-177">The learning pipeline loads all of the data and algorithms necessary to train the model.</span></span> <span data-ttu-id="d438f-178">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d438f-178">Add the following code into the `Train` method:</span></span>

[!code-csharp[Initialize pipeline](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#5)]

## <a name="load-and-transform-data"></a><span data-ttu-id="d438f-179">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-179">Load and transform data</span></span>

<span data-ttu-id="d438f-180">La première étape à effectuer consiste à charger le jeu de données d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="d438f-180">The first step to perform is to load the training data set.</span></span> <span data-ttu-id="d438f-181">Dans notre cas, le jeu de données d’apprentissage est stocké dans le fichier texte avec un chemin défini par le champ `_dataPath`.</span><span class="sxs-lookup"><span data-stu-id="d438f-181">In our case, the training data set is stored in the text file with a path defined by the `_dataPath` field.</span></span> <span data-ttu-id="d438f-182">Dans le fichier, les colonnes sont séparées par une virgule (« , »).</span><span class="sxs-lookup"><span data-stu-id="d438f-182">Columns in the file are separated by the comma (",").</span></span> <span data-ttu-id="d438f-183">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d438f-183">Add the following code into the `Train` method:</span></span>

[!code-csharp[Add step to load data](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#6)]

<span data-ttu-id="d438f-184">L’étape suivante consiste à combiner toutes les colonnes de caractéristiques dans la colonne **Features** à l’aide de la classe de transformation <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator>.</span><span class="sxs-lookup"><span data-stu-id="d438f-184">The next step is to combine all of the feature columns into the **Features** column using the <xref:Microsoft.ML.Legacy.Transforms.ColumnConcatenator> transformation class.</span></span> <span data-ttu-id="d438f-185">Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**.</span><span class="sxs-lookup"><span data-stu-id="d438f-185">By default, a learning algorithm processes only features from the **Features** column.</span></span> <span data-ttu-id="d438f-186">Ajoutez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d438f-186">Add the following code:</span></span>

[!code-csharp[Add step to concatenate columns](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#7)]

## <a name="choose-a-learning-algorithm"></a><span data-ttu-id="d438f-187">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d438f-187">Choose a learning algorithm</span></span>

<span data-ttu-id="d438f-188">Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**).</span><span class="sxs-lookup"><span data-stu-id="d438f-188">After adding the data to the pipeline and transforming it into the correct input format, you select a learning algorithm (**learner**).</span></span> <span data-ttu-id="d438f-189">L’apprenant effectue l’apprentissage du modèle.</span><span class="sxs-lookup"><span data-stu-id="d438f-189">The learner trains the model.</span></span> <span data-ttu-id="d438f-190">ML.NET fournit un apprenant <xref:Microsoft.ML.Legacy.Trainers.KMeansPlusPlusClusterer> qui implémente l’[algorithme k-means](https://en.wikipedia.org/wiki/K-means_clustering) avec une méthode améliorée pour le choix des centroïdes de clusters initiaux.</span><span class="sxs-lookup"><span data-stu-id="d438f-190">ML.NET provides a <xref:Microsoft.ML.Legacy.Trainers.KMeansPlusPlusClusterer> learner that implements [k-means algorithm](https://en.wikipedia.org/wiki/K-means_clustering) with an improved method for choosing the initial cluster centroids.</span></span>

<span data-ttu-id="d438f-191">Ajoutez le code suivant dans la méthode `Train` après le code de traitement des données ajouté à l’étape précédente :</span><span class="sxs-lookup"><span data-stu-id="d438f-191">Add the following code into the `Train` method following the data processing code added in the previous step:</span></span>

[!code-csharp[Add a learner step](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#8)]

<span data-ttu-id="d438f-192">Utilisez la propriété <xref:Microsoft.ML.Legacy.Trainers.KMeansPlusPlusClusterer.K?displayProperty=nameWithType> pour spécifier le nombre de clusters.</span><span class="sxs-lookup"><span data-stu-id="d438f-192">Use the <xref:Microsoft.ML.Legacy.Trainers.KMeansPlusPlusClusterer.K?displayProperty=nameWithType> property to specify number of clusters.</span></span> <span data-ttu-id="d438f-193">Le code ci-dessus spécifie que le jeu de données doit être divisé en trois clusters.</span><span class="sxs-lookup"><span data-stu-id="d438f-193">The code above specifies that the data set should be split in three clusters.</span></span>

## <a name="train-the-model"></a><span data-ttu-id="d438f-194">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d438f-194">Train the model</span></span>

<span data-ttu-id="d438f-195">Les étapes ajoutées dans les sections précédentes ont préparé le pipeline pour l’apprentissage, toutefois, aucune n’a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="d438f-195">The steps added in the preceding sections prepared the pipeline for training, however, none have been executed.</span></span> <span data-ttu-id="d438f-196">La méthode `pipeline.Train<TInput, TOutput>` génère le modèle qui prend une instance du type `TInput` et génère une instance du type `TOutput`.</span><span class="sxs-lookup"><span data-stu-id="d438f-196">The `pipeline.Train<TInput, TOutput>` method produces the model that takes in an instance of the `TInput` type and outputs an instance of the `TOutput` type.</span></span> <span data-ttu-id="d438f-197">Ajoutez le code suivant à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d438f-197">Add the following code into the `Train` method:</span></span>

[!code-csharp[Train the model and return](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#9)]

### <a name="save-the-model"></a><span data-ttu-id="d438f-198">Enregistrer le modèle</span><span class="sxs-lookup"><span data-stu-id="d438f-198">Save the model</span></span>

<span data-ttu-id="d438f-199">À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles.</span><span class="sxs-lookup"><span data-stu-id="d438f-199">At this point, you have a model that can be integrated into any of your existing or new .NET applications.</span></span> <span data-ttu-id="d438f-200">Pour enregistrer votre modèle dans un fichier .zip, ajoutez le code suivant à la méthode `Main` sous l’appel à la méthode `Train` :</span><span class="sxs-lookup"><span data-stu-id="d438f-200">To save your model to a .zip file, add the following code to the `Main` method below the call to the `Train` method:</span></span>

[!code-csharp[Save the model](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#10)]

<span data-ttu-id="d438f-201">L’utilisation de l’élément `await` dans la méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :</span><span class="sxs-lookup"><span data-stu-id="d438f-201">Using `await` in the `Main` method means the `Main` method must have the `async` modifier and return a `Task`:</span></span>

[!code-csharp[Make the Main method async](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#11)]

<span data-ttu-id="d438f-202">Vous devez également ajouter la directive `using` suivante en haut du fichier *Program.cs* :</span><span class="sxs-lookup"><span data-stu-id="d438f-202">You also need to add the following `using` directive at the top of the *Program.cs* file:</span></span>

[!code-csharp[Add System.Threading.Tasks using](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#12)]

<span data-ttu-id="d438f-203">Comme la méthode `async Main` est la fonctionnalité ajoutée dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version de langage par C# 7.1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d438f-203">Because the `async Main` method is the feature added in C# 7.1 and the default language version of the project is C# 7.0, you need to change the language version to C# 7.1 or higher.</span></span> <span data-ttu-id="d438f-204">Pour ce faire, cliquez avec le bouton droit sur le nœud de projet dans **l’Explorateur de solutions** et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d438f-204">To do that, right-click the project node in **Solution Explorer** and select **Properties**.</span></span> <span data-ttu-id="d438f-205">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="d438f-205">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="d438f-206">Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="d438f-206">In the dropdown, select  **C# 7.1** (or a higher version).</span></span> <span data-ttu-id="d438f-207">Sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="d438f-207">Select the **OK** button.</span></span>

## <a name="use-the-model-for-predictions"></a><span data-ttu-id="d438f-208">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d438f-208">Use the model for predictions</span></span>

<span data-ttu-id="d438f-209">Créez la classe `TestIrisData` qui contiendra les instances de données de test :</span><span class="sxs-lookup"><span data-stu-id="d438f-209">Create the `TestIrisData` class to house test data instances:</span></span>

1. <span data-ttu-id="d438f-210">Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="d438f-210">In **Solution Explorer**, right-click the project, and then select **Add** > **New Item**.</span></span>
1. <span data-ttu-id="d438f-211">Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestIrisData.cs*.</span><span class="sxs-lookup"><span data-stu-id="d438f-211">In the **Add New Item** dialog box, select **Class** and change the **Name** field to *TestIrisData.cs*.</span></span> <span data-ttu-id="d438f-212">Ensuite, sélectionnez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d438f-212">Then, select the **Add** button.</span></span>
1. <span data-ttu-id="d438f-213">Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d438f-213">Modify the class to be static like in the following example:</span></span>

   [!code-csharp[Make class static](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#1)]

<span data-ttu-id="d438f-214">Ce tutoriel présente une instance de données d’iris au sein de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d438f-214">This tutorial introduces one iris data instance within this class.</span></span> <span data-ttu-id="d438f-215">Vous pouvez ajouter d’autres scénarios à tester avec le modèle.</span><span class="sxs-lookup"><span data-stu-id="d438f-215">You can add other scenarios to experiment with the model.</span></span> <span data-ttu-id="d438f-216">Ajoutez le code suivant à la classe `TestIrisData` :</span><span class="sxs-lookup"><span data-stu-id="d438f-216">Add the following code into the `TestIrisData` class:</span></span>

[!code-csharp[Test data](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#2)]

<span data-ttu-id="d438f-217">Pour déterminer à quel cluster l’élément spécifié appartient, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main`:</span><span class="sxs-lookup"><span data-stu-id="d438f-217">To find out the cluster to which the specified item belongs to, go back to the *Program.cs* file and add the following code into the `Main` method:</span></span>

[!code-csharp[Predict and output results](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#13)]

<span data-ttu-id="d438f-218">Exécutez le programme pour voir quel cluster contient l’instance de données spécifiée et les distances au carré à partir de cette instance jusqu’aux centroïdes des clusters.</span><span class="sxs-lookup"><span data-stu-id="d438f-218">Run the program to see which cluster contains the specified data instance and squared distances from that instance to the cluster centroids.</span></span> <span data-ttu-id="d438f-219">Vos résultats doivent être similaires à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="d438f-219">Your results should be similar to the following.</span></span> <span data-ttu-id="d438f-220">Lors du traitement, le pipeline peut afficher des avertissements ou des messages de traitement.</span><span class="sxs-lookup"><span data-stu-id="d438f-220">As the pipeline processes, it might display warnings or processing messages.</span></span> <span data-ttu-id="d438f-221">Ils ont été supprimés de la sortie suivante par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="d438f-221">These have been removed from the following output for clarity.</span></span>

```text
Cluster: 2
Distances: 0.4192338 0.0008847713 0.9660053
```

<span data-ttu-id="d438f-222">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="d438f-222">Congratulations!</span></span> <span data-ttu-id="d438f-223">Vous venez de créer un modèle d’apprentissage automatique de clustering des iris et l’avez utilisé pour réaliser des prédictions.</span><span class="sxs-lookup"><span data-stu-id="d438f-223">You've now successfully built a machine learning model for iris clustering and used it to make predictions.</span></span> <span data-ttu-id="d438f-224">Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisClustering).</span><span class="sxs-lookup"><span data-stu-id="d438f-224">You can find the source code for this tutorial at the [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisClustering) GitHub repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d438f-225">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d438f-225">Next steps</span></span>

<span data-ttu-id="d438f-226">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="d438f-226">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="d438f-227">Comprendre le problème</span><span class="sxs-lookup"><span data-stu-id="d438f-227">Understand the problem</span></span>
> - <span data-ttu-id="d438f-228">Sélectionner la tâche d’apprentissage automatique appropriée</span><span class="sxs-lookup"><span data-stu-id="d438f-228">Select the appropriate machine learning task</span></span>
> - <span data-ttu-id="d438f-229">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-229">Prepare the data</span></span>
> - <span data-ttu-id="d438f-230">Charger et transformer les données</span><span class="sxs-lookup"><span data-stu-id="d438f-230">Load and transform the data</span></span>
> - <span data-ttu-id="d438f-231">Choisir un algorithme d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="d438f-231">Choose a learning algorithm</span></span>
> - <span data-ttu-id="d438f-232">Effectuer l’apprentissage du modèle</span><span class="sxs-lookup"><span data-stu-id="d438f-232">Train the model</span></span>
> - <span data-ttu-id="d438f-233">Utiliser le modèle pour les prévisions</span><span class="sxs-lookup"><span data-stu-id="d438f-233">Use the model for predictions</span></span>

<span data-ttu-id="d438f-234">Consultez notre référentiel GitHub pour continuer l’apprentissage et obtenir d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="d438f-234">Check out our GitHub repository to continue learning and find more samples.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="d438f-235">Référentiel GitHub dotnet/machinelearning</span><span class="sxs-lookup"><span data-stu-id="d438f-235">dotnet/machinelearning GitHub repository</span></span>](https://github.com/dotnet/machinelearning/)
