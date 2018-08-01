---
title: Utiliser ML.NET pour créer un cluster d’iris (clustering)
description: Découvrez comment utiliser ML.NET dans un scénario de clustering
author: pkulikov
ms.author: johalex
ms.date: 07/02/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 46db9dc7ff425c483f1a9f61da5e806e598b16d5
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37937164"
---
# <a name="tutorial-use-mlnet-to-cluster-iris-flowers-clustering"></a>Tutoriel : Utiliser ML.NET pour créer un cluster d’iris (clustering)

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce tutoriel montre comment utiliser ML.NET pour générer un [modèle de clustering](../resources/tasks.md#clustering) pour le [jeu de données Iris](https://en.wikipedia.org/wiki/Iris_flower_data_set).

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> - Comprendre le problème
> - Sélectionner la tâche d’apprentissage automatique appropriée
> - Préparer les données
> - Charger et transformer les données
> - Choisir un algorithme d’apprentissage
> - Effectuer l’apprentissage du modèle
> - Utiliser le modèle pour les prévisions

## <a name="prerequisites"></a>Prérequis

- [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

## <a name="understand-the-problem"></a>Comprendre le problème

Ce problème concerne la division de l’ensemble des iris en différents groupes basés sur les caractéristiques de la fleur. Ces caractéristiques sont la longueur et la largeur d’un sépale, ainsi que la longueur et la largeur d’un pétale. Pour ce tutoriel, supposons que le type de chaque fleur est inconnu. Vous souhaitez connaître la structure d’un jeu de données à partir des caractéristiques et prédire la façon dont une instance de données s’intègre à cette structure.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Comme vous ne savez pas à quel groupe appartient chaque fleur, vous choisissez la tâche [Apprentissage automatique non supervisé](../resources/glossary.md#unsupervised-machine-learning). Pour diviser un jeu de données en groupes de telle sorte que les éléments dans le même groupe soient plus similaires les uns aux autres qu’à ceux des autres groupes, utilisez une tâche d’apprentissage automatique de [clustering](../resources/tasks.md#clustering).

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « IrisClustering », puis sélectionnez le bouton **OK**.

1. Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

1. Installez le package NuGet **Microsoft.ML** :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

## <a name="prepare-the-data"></a>Préparer les données

1. Téléchargez le jeu de données [iris.data](https://github.com/dotnet/machinelearning/blob/master/test/data/iris.data) et enregistrez-le dans le dossier *Data* que vous avez créé à l’étape précédente. Pour plus d’informations sur le jeu de données Iris, consultez la page Wikipédia [Iris de Fisher](https://en.wikipedia.org/wiki/Iris_flower_data_set) et la page [Iris Data Set](http://archive.ics.uci.edu/ml/datasets/Iris), qui est la source du jeu de données.

1. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le fichier *iris.data* et sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

Le fichier *iris.data* contient cinq colonnes qui représentent :

- la longueur des sépales en centimètres
- la largeur des sépales en centimètres
- la longueur des pétales en centimètres
- la largeur des pétales en centimètres
- le type d’iris

Dans le cadre de cet exemple de clustering, ce tutoriel ignore la dernière colonne.

## <a name="create-data-classes"></a>Créer des classes de données

Créez des classes pour les données d’entrée et les prédictions :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe** et définissez la valeur du champ **Nom** sur *IrisData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Ajoutez la directive `using` suivante au nouveau fichier :

   [!code-csharp[Add necessary usings](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#1)]

Supprimez la définition de classe existante et ajoutez le code suivant, qui définit les classes `IrisData` et `ClusterPrediction`, au fichier *IrisData.cs* :

[!code-csharp[Define data classes](../../../samples/machine-learning/tutorials/IrisClustering/IrisData.cs#2)]

`IrisData` est la classe des données d’entrée et a des définitions pour chaque caractéristique du jeu de données. Utilisez l’attribut [Column](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) pour spécifier les index des colonnes sources dans le fichier de jeu de données.

La classe `ClusterPrediction` représente la sortie du modèle de clustering appliqué à une instance `IrisData`. Utilisez l’attribut [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) pour lier les champs `PredictedClusterId` et `Distances` aux colonnes **PredictedLabel** et **Score** respectivement. Dans le cas de la tâche de clustering, ces colonnes ont la signification suivante :

- La colonne **PredictedLabel** contient l’ID du cluster prédit.
- La colonne **Score** contient un tableau avec les distances Euclidiennes au carré jusqu’aux centroïdes des clusters. La longueur du tableau est égale au nombre de clusters.

> [!NOTE]
> Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.

## <a name="define-data-and-model-paths"></a>Définir des chemins de données et de modèle

Revenez au fichier *Program.cs* et ajoutez deux champs pour contenir les chemins du fichier de jeu de données et du fichier pour enregistrer le modèle :

- `_dataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.
- `_modelPath` contient le chemin du fichier où le modèle formé est stocké.

Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins :

[!code-csharp[Initialize paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#1)]

Pour compiler le code précédent, ajoutez les directives `using` suivantes en haut du fichier *Program.cs* :

[!code-csharp[Add usings for paths](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#2)]

## <a name="create-a-learning-pipeline"></a>Créer un pipeline d’apprentissage

Ajoutez les directives `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[Add Microsoft.ML usings](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#3)]

Dans la méthode `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :

[!code-csharp[Call the Train method](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#4)]

La méthode `Train` effectue l’apprentissage du modèle. Créez cette méthode juste en dessous de la méthode `Main`, en utilisant le code suivant :

```csharp
private static PredictionModel<IrisData, ClusterPrediction> Train()
{

}
```

Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle. Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[Initialize pipeline](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#5)]

## <a name="load-and-transform-data"></a>Charger et transformer les données

La première étape à effectuer consiste à charger le jeu de données d’apprentissage. Dans notre cas, le jeu de données d’apprentissage est stocké dans le fichier texte avec un chemin défini par le champ `_dataPath`. Dans le fichier, les colonnes sont séparées par une virgule (« , »). Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[Add step to load data](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#6)]

L’étape suivante consiste à combiner toutes les colonnes de caractéristiques dans la colonne **Features** à l’aide de la classe de transformation <xref:Microsoft.ML.Transforms.ColumnConcatenator>. Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**. Ajoutez le code suivant :

[!code-csharp[Add step to concatenate columns](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#7)]

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**). L’apprenant effectue l’apprentissage du modèle. ML.NET fournit un apprenant <xref:Microsoft.ML.Trainers.KMeansPlusPlusClusterer> qui implémente l’[algorithme k-means](https://en.wikipedia.org/wiki/K-means_clustering) avec une méthode améliorée pour le choix des centroïdes de clusters initiaux.

Ajoutez le code suivant dans la méthode `Train` après le code de traitement des données ajouté à l’étape précédente :

[!code-csharp[Add a learner step](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#8)]

Utilisez la propriété <xref:Microsoft.ML.Trainers.KMeansPlusPlusClusterer.K?displayProperty=nameWithType> pour spécifier le nombre de clusters. Le code ci-dessus spécifie que le jeu de données doit être divisé en trois clusters.

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

Les étapes ajoutées dans les sections précédentes ont préparé le pipeline pour l’apprentissage, toutefois, aucune n’a été exécutée. La méthode `pipeline.Train<TInput, TOutput>` génère le modèle qui prend une instance du type `TInput` et génère une instance du type `TOutput`. Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[Train the model and return](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#9)]

### <a name="save-the-model"></a>Enregistrer le modèle

À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Pour enregistrer votre modèle dans un fichier .zip, ajoutez le code suivant à la méthode `Main` sous l’appel à la méthode `Train` :

[!code-csharp[Save the model](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#10)]

L’utilisation de l’élément `await` dans la méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :

[!code-csharp[Make the Main method async](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#11)]

Vous devez également ajouter la directive `using` suivante en haut du fichier *Program.cs* :

[!code-csharp[Add System.Threading.Tasks using](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#12)]

Comme la méthode `async Main` est la fonctionnalité ajoutée dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version de langage par C# 7.1 ou version ultérieure. Pour ce faire, cliquez avec le bouton droit sur le nœud de projet dans **l’Explorateur de solutions** et sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="use-the-model-for-predictions"></a>Utiliser le modèle pour les prévisions

Créez la classe `TestIrisData` qui contiendra les instances de données de test :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestIrisData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :

   [!code-csharp[Make class static](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#1)]

Ce tutoriel présente une instance de données d’iris au sein de cette classe. Vous pouvez ajouter d’autres scénarios à tester avec le modèle. Ajoutez le code suivant à la classe `TestIrisData` :

[!code-csharp[Test data](../../../samples/machine-learning/tutorials/IrisClustering/TestIrisData.cs#2)]

Pour déterminer à quel cluster l’élément spécifié appartient, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main`:

[!code-csharp[Predict and output results](../../../samples/machine-learning/tutorials/IrisClustering/Program.cs#13)]

Exécutez le programme pour voir quel cluster contient l’instance de données spécifiée et les distances au carré à partir de cette instance jusqu’aux centroïdes des clusters. Vos résultats doivent être similaires à ce qui suit. Lors du traitement, le pipeline peut afficher des avertissements ou des messages de traitement. Ils ont été supprimés de la sortie suivante par souci de clarté.

```text
Cluster: 2
Distances: 0.4192338 0.0008847713 0.9660053
```

Félicitations ! Vous venez de créer un modèle d’apprentissage automatique de clustering des iris et l’avez utilisé pour réaliser des prédictions. Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/IrisClustering).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> - Comprendre le problème
> - Sélectionner la tâche d’apprentissage automatique appropriée
> - Préparer les données
> - Charger et transformer les données
> - Choisir un algorithme d’apprentissage
> - Effectuer l’apprentissage du modèle
> - Utiliser le modèle pour les prévisions

Consultez notre dépôt GitHub pour continuer l’apprentissage et obtenir d’autres exemples.
> [!div class="nextstepaction"]
> [dotnet/machinelearning GitHub repository](https://github.com/dotnet/machinelearning/)
