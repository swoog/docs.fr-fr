---
title: Prédire des prix en utilisant un apprenant de régression avec ML.NET
description: Prédisez des prix en utilisant un apprenant de régression avec ML.NET.
author: aditidugar
ms.author: johalex
ms.date: 03/20/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 49770672ebcff98d8779a888372b5c9f40a55b1d
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59611807"
---
# <a name="tutorial-predict-prices-using-a-regression-learner-with-mlnet"></a>Tutoriel : Prédire des prix en utilisant un apprenant de régression avec ML.NET

Ce tutoriel montre comment utiliserML.NET pour créer un [modèle de régression](../resources/glossary.md#regression) afin de prédire des prix, plus précisément, des courses de taxi à New York.

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez l’[introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce tutoriel et l’exemple associé utilisent actuellement **ML.NET version 0.11**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer et comprendre les données
> * Créer un pipeline d’apprentissage
> * Charger et transformer les données
> * Choisir un algorithme d’apprentissage
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Utiliser le modèle pour les prévisions

## <a name="prerequisites"></a>Prérequis

* [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

## <a name="understand-the-problem"></a>Comprendre le problème

Ce problème consiste à prédire le prix d’une course de taxi à New York. À première vue, ce prix semble dépendre simplement de la distance parcourue. Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Vous souhaitez prédire le prix, qui est une valeur réelle, en fonction des autres facteurs du jeu de données. Pour ce faire, choisissez une tâche d’apprentissage automatique par [régression](../resources/glossary.md#regression).

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.

1. Créez un répertoire nommé *Data* dans votre projet pour enregistrer le jeu de données et les fichiers de modèle :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

1. Installez le package NuGet **Microsoft.ML** :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

## <a name="prepare-and-understand-the-data"></a>Préparer et comprendre les données

1. Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente. Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle. Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).

1. Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

1. Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne. Examinons chacune des colonnes. Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.

**L’étiquette** est l’identificateur de la colonne à prédire. Les **fonctionnalités** identifiées servent à prédire l’étiquette.

Le jeu de données fourni contient les colonnes suivantes :

* **vendor_id :** l’ID du taxi est une fonctionnalité.
* **rate_code :** le type de tarif de la course de taxi est une fonctionnalité.
* **passenger_count :** le nombre de passagers embarqués est une fonctionnalité.
* **trip_time_in_secs :** durée totale de la course. Vous voulez prédire le prix de la course avant de l’effectuer. À ce stade vous ne connaissez pas la durée de la course. Par conséquent, la durée de la course n’est pas une fonctionnalité et vous devez exclure cette colonne du modèle.
* **trip_distance :** la distance de la course est une fonctionnalité.
* **payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.
* **fare_amount :** le prix total payé pour la course est l’étiquette.

## <a name="create-data-classes"></a>Créer des classes de données

Créez des classes pour les données d’entrée et les prédictions :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Ajoutez les directives `using` suivantes au nouveau fichier :

   [!code-csharp[AddUsings](~/samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :

[!code-csharp[DefineTaxiTrip](~/samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données. Utilisez l’attribut <xref:Microsoft.ML.Data.LoadColumnAttribute> pour spécifier les index des colonnes sources dans le jeu de données.

La classe `TaxiTripFarePrediction` représente les résultats prédits. Elle comporte un seul champ float, `FareAmount`, avec un attribut `Score` <xref:Microsoft.ML.Data.ColumnNameAttribute> appliqué. Dans le cas de la tâche de régression, la colonne **Score** contient les valeurs d’étiquette prédites.

> [!NOTE]
> Utilisez le type `float` pour représenter les valeurs à virgule flottante dans les classes de données d’entrée et de prédiction.

## <a name="define-data-and-model-paths"></a>Définir des chemins de données et de modèle

Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

Il faut créer trois champs qui contiendront les chemins des fichiers comportant des jeux de données et le fichier permettant d’enregistrer le modèle :

* `_trainDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.
* `_testDataPath` contient le chemin du fichier avec le jeu de données utilisé pour l’évaluation du modèle.
* `_modelPath` contient le chemin du fichier où le modèle formé est stocké.

Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins et pour la variable `_textLoader` :

[!code-csharp[InitializePaths](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

Lors de la création d’un modèle avec ML.NET, vous commencez par créer un contexte ML. Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework. L’environnement fournit un contexte pour votre tâche Machine Learning et qui peut être utilisé pour le suivi des exceptions et la journalisation.

### <a name="initialize-variables-in-main"></a>Initialiser les variables dans Principal

Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.  Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :

[!code-csharp[CreateMLContext](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create the ML Context")]

Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` afin d’appeler la méthode `Train` :

[!code-csharp[Train](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Train your model")]

La méthode `Train` exécute les tâches suivantes :

* Charge les données.
* Extrait et transforme les données.
* Effectue l’apprentissage du modèle.
* Enregistre le modèle en tant que fichier .zip.
* Retourne le modèle.

La méthode `Train` effectue l’apprentissage du modèle. Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :

```csharp
public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

Nous passons deux paramètres à la méthode `Train` ; un paramètre `MLContext` pour le contexte (`mlContext`) et une chaîne pour le chemin d’accès au jeu de données (`dataPath`). Nous allons réutiliser cette méthode pour le chargement des jeux de données.

## <a name="load-and-transform-data"></a>Charger et transformer les données

Chargez les données avec le wrapper `MLContext.Data.LoadFromTextFile` de la [méthode LoadFromTextFile](xref:Microsoft.ML.TextLoaderSaverCatalog.LoadFromTextFile%60%601%28Microsoft.ML.DataOperationsCatalog,System.String,System.Char,System.Boolean,System.Boolean,System.Boolean,System.Boolean%29). Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>.

En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.

Dans ML.NET, les données sont semblables à une vue SQL. Elles sont évaluées tardivement, schématisées et hétérogènes. L’objet est la première partie du pipeline, et charge les données. Pour ce tutoriel, il charge un jeu de données avec des informations sur les prix des courses de taxi. Cette méthode permet de créer puis de former le modèle.

Ajoutez le code suivant comme première ligne de la méthode `Train` :

[!code-csharp[LoadTrainData](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "loading training dataset")]

Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.

Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire. Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**. Pour ce faire, utilisez la classe de transformation `CopyColumnsEstimator`, et ajoutez le code suivant :

[!code-csharp[CopyColumnsEstimator](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Use the CopyColumnsEstimator")]

L’algorithme qui effectue l’apprentissage du modèle exige des fonctionnalités **numériques**. Il faut donc transformer les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres (`VendorIdEncoded`, `RateCodeEncoded` et `PaymentTypeEncoded`). Pour cela, utilisez la classe de transformation Microsoft.ML.Transforms.OneHotEncodingTransformer>, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :

[!code-csharp[OneHotEncodingEstimator](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Use the OneHotEncodingEstimator")]

La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `mlContext.Transforms.Concatenate`. Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**. Ajoutez le code suivant :

[!code-csharp[ColumnConcatenatingEstimator](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Use the ColumnConcatenatingEstimator")]

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnons un algorithme d’apprentissage (**apprenant**). L’apprenant effectue l’apprentissage du modèle. Nous avez choisi une tâche de **régression** pour ce problème. Nous utilisons donc un apprenant `FastTreeRegressionTrainer`, qui est l’un des apprenants de régression fournis par ML.NET.

L’algorithme d’apprentissage `FastTreeRegressionTrainer` s’appuie sur le boosting de gradient. Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression. Il génère chaque arbre de régression étape par étape. Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine. Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces. Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).

Ajoutez le code suivant dans la méthode `Train` afin d’ajouter le `FastTreeRegressionTrainer` au code de traitement des données ajouté à l’étape précédente :

[!code-csharp[FastTreeRegressionTrainer](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Add the FastTreeRegressionTrainer")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

La dernière étape consiste à effectuer l’apprentissage du modèle. Nous effectuons l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain>, selon le jeu de données qui a été chargé et transformé. Une fois l’estimation définie, nous formons le modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées. Cette méthode retourne un modèle à utiliser pour les prédictions. `pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis. L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.

[!code-csharp[TrainModel](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#11 "Train the model")]

### <a name="save-the-model"></a>Enregistrer le modèle

À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Pour enregistrer le modèle dans un fichier .zip, ajoutez le code suivant à la fin de la méthode `Train` :

[!code-csharp[SaveModel](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Save the model as a .zip file and return the model")]

## <a name="save-the-model-as-a-zip-file"></a>Enregistrer le modèle en tant que fichier .zip

Créez la méthode `SaveModelAsFile` juste après la méthode `Train`, en utilisant le code suivant :

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

La méthode `SaveModelAsFile` exécute les tâches suivantes :

* Enregistre le modèle sous la forme d’un fichier .zip.

Nous devons créer une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications. Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>. Comme nous souhaitons l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`. Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :

[!code-csharp[SaveToMethod](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Add the SaveTo Method")]

Nous pouvons également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="evaluate-the-model"></a>Évaluer le modèle

L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette. Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage. Pour ce faire, vous pouvez, par exemple, fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme indiqué dans ce tutoriel. Une fois que vous avez formé le modèle à l’aide des données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.

La méthode `Evaluate` évalue le modèle. Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :

```csharp
private static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```

La méthode `Evaluate` exécute les tâches suivantes :

* Charge le jeu de données de test.
* Crée l’évaluateur de régression.
* Évalue le modèle et crée des métriques.
* Affiche les métriques.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Call the Evaluate method")]

Chargez le jeu de données de test à l’aide du wrapper `MLContext.Data.LoadFromTextFile`. Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité. Ajoutez le code suivant à la méthode `Evaluate` :

[!code-csharp[LoadTestDataset](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Load the test dataset")]

Utilisons maintenant le paramètre Machine Learning `model` (transformateur) pour passer en entrée les fonctionnalités et retourner des prédictions. Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :

[!code-csharp[PredictWithTransformer](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Predict using the Transformer")]

La méthode `RegressionContext.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié. Elle retourne un objet <xref:Microsoft.ML.Data.RegressionMetrics> qui contient les métriques globales calculées par les évaluateurs de régression. Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques. Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :

[!code-csharp[ComputeMetrics](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Compute Metrics")]

Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :

```csharp
Console.WriteLine();
Console.WriteLine($"*************************************************");
Console.WriteLine($"*       Model quality metrics evaluation         ");
Console.WriteLine($"*------------------------------------------------");
```

[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression. RSquared prend des valeurs entre 0 et 1. Plus sa valeur est proche de 1, plus le modèle est bon. Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :

[!code-csharp[DisplayRSquared](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#18 "Display the RSquared metric.")]

[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression. Plus sa valeur est faible, plus le modèle est bon. Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :

[!code-csharp[DisplayRMS](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#19 "Display the RMS metric.")]

## <a name="use-the-model-for-predictions"></a>Utiliser le modèle pour les prévisions

## <a name="predict-the-test-data-outcome-with-the-model-and-a-single-comment"></a>Prédire le résultat de données de test avec le modèle et un commentaire unique

Créez la méthode `TestSinglePrediction` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void TestSinglePrediction(MLContext mlContext)
{

}
```

La méthode `TestSinglePrediction` exécute les tâches suivantes :

* Crée un commentaire unique de données de test.
* Prédit le prix de la course en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :

[!code-csharp[CallTestSinglePrediction](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#20 "Call the TestSinglePrediction method")]

Étant donné que nous voulons charger le modèle à partir du fichier zip que nous avons enregistré, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `Load`. Ajoutez comme nouvelle ligne le code suivant à la méthode `TestSinglePrediction` :

[!code-csharp[LoadTheModel](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#21 "Load the model")]

Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels. Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`. Ajoutons le code suivant pour créer le `PredictionEngine` comme ligne suivante dans la méthode `TestSinglePrediction` :

[!code-csharp[MakePredictionEngine](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#22 "Create the PredictionFunction")]

Ce tutoriel utilise une course test au sein de cette classe. Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle. Ajoutez une course pour tester la prédiction de coût du modèle formé dans la méthode `TestSinglePrediction` en créant une instance de `TaxiTrip` :

[!code-csharp[PredictionData](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#23 "Create test data for single prediction")]

Nous pouvons utiliser ces éléments pour prédire le prix basé sur une instance unique des données d’une course de taxi. Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.

[!code-csharp[Predict](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#24 "Create a prediction of taxi fare")]

Pour afficher le prix prédit de la course spécifiée, ajoutez le code suivant à la méthode `TestSinglePrediction` :

[!code-csharp[Predict](~/samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#25 "Display the prediction.")]

Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.

Félicitations ! Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions. Vous trouverez le code source de ce tutoriel dans le dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :

> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer et comprendre les données
> * Créer un pipeline d’apprentissage
> * Charger et transformer les données
> * Choisir un algorithme d’apprentissage
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Utiliser le modèle pour les prévisions

Passez au tutoriel suivant pour en savoir plus.

> [!div class="nextstepaction"]
> [Clustering Iris](iris-clustering.md)
