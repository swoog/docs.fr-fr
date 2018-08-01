---
title: Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)
description: Découvrez comment utiliser ML.NET dans un scénario de régression.
author: aditidugar
ms.author: johalex
ms.date: 06/18/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: e3ff2124a43cf42ce26cf94cfd5384387eef0ed9
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37937070"
---
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a>Tutoriel : Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce tutoriel montre l’utilisation de ML.NET pour générer un [modèle de régression](../resources/glossary.md#regression) afin de prédire le prix des courses de taxi à New York.

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

* [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

## <a name="understand-the-problem"></a>Comprendre le problème

Ce problème est centré autour de la **prédiction du prix d’une course de taxi à New York**. À première vue, ce prix semble dépendre simplement de la distance parcourue. Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Pour prédire le prix de la course de taxi, vous sélectionnez d’abord la tâche d’apprentissage automatique appropriée. Vous devez prédire une valeur réelle (valeur double qui représente le prix) en fonction des autres facteurs du jeu de données. Vous choisissez une tâche de [**régression**](../resources/glossary.md#regression).

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.

2. Créez un répertoire nommé *Données* dans votre projet pour enregistrer les fichiers de jeu de données :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

3. Installez le **package NuGet Microsoft.ML** :

    Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur le projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet **Parcourir**, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis sélectionnez le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

## <a name="prepare-and-understand-the-data"></a>Préparer et comprendre les données

1. Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé à l’étape précédente. Nous utilisons ces jeux de données pour le modèle Machine Learning et pour évaluer la précision du modèle. Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).

2. Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Toujours**.

3. Ouvrez le jeu de données **taxi-fare-train.csv** et examinez les en-têtes de colonne dans la première ligne. Examinons chacune des colonnes. Analysez les données et identifiez les colonnes qui sont des **fonctionnalités** et celle qui est **l’étiquette**.

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

   [!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

`TaxiTrip` est la classe des données d’entrée et a des définitions pour chacune des colonnes du jeu de données. Utilisez l’attribut [Colonne](xref:Microsoft.ML.Runtime.Api.ColumnAttribute) pour spécifier les index des colonnes sources dans le jeu de données.

La classe `TaxiTripFarePrediction` est utilisée pour représenter les résultats prédits. Elle a un champ de valeur flottante unique (`FareAmount`) avec un attribut `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) appliqué. La colonne **Score** est la colonne spéciale dans ML.NET. Le modèle génère les valeurs prédites dans cette colonne.

## <a name="define-data-and-model-paths"></a>Définir des chemins de données et de modèle

Revenez au fichier *Program.cs* et ajoutez trois champs pour contenir les chemins des fichiers avec des jeux de données et le fichier pour enregistrer le modèle :

* `_datapath` contient le chemin du fichier avec le jeu de données utilisé pour l’apprentissage du modèle.
* `_testdatapath` contient le chemin du fichier avec le jeu de données utilisé pour l’évaluation du modèle.
* `_modelpath` contient le chemin du fichier où le modèle formé est stocké.

Ajoutez le code suivant juste au-dessus de la méthode `Main` pour spécifier ces chemins :

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

Pour compiler le code précédent, ajoutez les directives `using` suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsingsForPaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#17 "Using statements for path definitions")]

## <a name="create-a-learning-pipeline"></a>Créer un pipeline d’apprentissage

Ajoutez les directives `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

Dans `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

La méthode `Train` effectue l’apprentissage du modèle. Créez cette méthode juste en dessous de `Main`, en utilisant le code suivant :

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle. Ajoutez le code suivant à la méthode `Train` :

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-data"></a>Charger et transformer les données

La première étape du pipeline d’apprentissage est de charger les données du jeu de données d’apprentissage. Dans notre cas, le jeu de données d’apprentissage est stocké dans le fichier texte avec un chemin défini par le champ `_datapath`. Ce fichier contient l’en-tête avec les noms de colonne, la première ligne doit donc être ignorée pendant le chargement des données. Dans le fichier, les colonnes sont séparées par une virgule (« , »). Ajoutez le code suivant à la méthode `Train` :

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(useHeader: true, separator: ','));
```

Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `TaxiTrip`.

Une fois que le modèle est formé et évalué, les valeurs de la colonne **Étiquette** sont considérées comme des valeurs correctes à prédire. Comme nous voulons prédire le prix de la course en taxi, copiez la colonne `FareAmount` dans la colonne **Étiquette**. Pour ce faire, utilisez <xref:Microsoft.ML.Transforms.ColumnCopier> et ajoutez le code suivant :

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques**, car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres. Pour ce faire, utilisez <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer>, qui attribue différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, et ajoutez le code suivant :

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation <xref:Microsoft.ML.Transforms.ColumnConcatenator>. Cette étape est nécessaire, car un apprenant traite uniquement les fonctionnalités de la colonne **Fonctionnalités**. Ajoutez le code suivant :

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

Notez que la colonne `TripTime`, qui correspond à la colonne `trip_time_in_secs` dans le fichier de jeu de données, n’est pas incluse. Vous avez déterminé que cette fonctionnalité de prévision n’est pas utile.

> [!NOTE]
> Ces étapes doivent être ajoutées au pipeline dans l’ordre spécifié ci-dessus pour garantir la bonne exécution.

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**). L’apprenant effectue l’apprentissage du modèle. Vous avez choisi une **tâche de régression** pour ce problème, vous ajoutez donc un apprenant <xref:Microsoft.ML.Trainers.FastTreeRegressor>, qui est un des apprenants de régression fournis par ML.NET.

L’apprenant <xref:Microsoft.ML.Trainers.FastTreeRegressor> utilise le boosting de gradient. Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression. Il génère chaque arbre de régression étape par étape. Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine. Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces. Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).

Ajoutez le code suivant dans la méthode `Train` après le code de traitement des données ajouté à l’étape précédente :

```csharp
pipeline.Add(new FastTreeRegressor());
```

Vous avez ajouté toutes les étapes précédentes au pipeline en tant qu’instructions individuelles, mais C# propose une syntaxe d’initialisation de collection pratique qui facilite la création et l’initialisation du pipeline. Remplacez le code que vous avez ajouté à la méthode `Train` par le code suivant :

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

La dernière étape consiste à effectuer l’apprentissage du modèle. À ce stade, rien dans le pipeline n’a été exécuté. La méthode `pipeline.Train<TInput, TOutput>` génère le modèle qui prend une instance du type `TInput` et génère une instance du type `TOutput`. Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

Et voilà ! Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York. Nous allons maintenant essayer de déterminer la précision du modèle et découvrir comment l’utiliser pour prédire les valeurs des tarifs de taxi.

### <a name="save-the-model"></a>Enregistrer le modèle

Avant de passer à l’étape suivante, enregistrez le modèle dans un fichier .zip, en ajoutant le code suivant à la fin de la méthode `Train` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

L’ajout de l’instruction `await` à l’appel `model.WriteAsync` signifie que la méthode `Train` doit être remplacée par une méthode asynchrone qui retourne une tâche. Modifiez la signature de `Train`, comme indiqué dans le code suivant :

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

La modification du type de retour de la méthode `Train` signifie que vous devez ajouter un élément `await` au code qui appelle `Train` dans la méthode `Main`, comme indiqué dans le code suivant :

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

L’utilisation de l’élément `await` dans la méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

Vous devez également ajouter la directive `using` suivante en haut du fichier :

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

Comme la méthode `async Main` est la fonctionnalité ajoutée dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version de langage par C# 7.1 ou version ultérieure. Pour ce faire, cliquez avec le bouton droit sur le nœud de projet dans **l’Explorateur de solutions** et sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="evaluate-the-model"></a>Évaluer le modèle

L’évaluation est le processus de vérification de la précision avec laquelle le modèle prédit les valeurs d’étiquette. Le modèle doit faire des prévisions correctes sur les données qui n’ont pas été utilisées pour effectuer l’apprentissage. Pour ce faire, vous pouvez fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme expliqué dans ce tutoriel. Maintenant que vous avez formé le modèle avec les données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.

Revenez à la méthode `Main` et ajoutez le code suivant sous l’appel à la méthode `Train` :

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

La méthode `Evaluate` évalue le modèle. Pour créer cette méthode, ajoutez le code suivant sous la méthode `Train` :

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

Ajoutez le code suivant dans la méthode `Evaluate` pour configurer le chargement des données de test :

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

Ajoutez le code suivant pour évaluer le modèle et produire les métriques d’évaluation :

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

[RMS](../resources/glossary.md##root-of-mean-squared-error-rmse) est une des métriques d’évaluation du modèle de régression. Plus sa valeur est faible, plus le modèle est bon. Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RMS :

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

[RSquared](../resources/glossary.md#coefficient-of-determination) est une autre métrique d’évaluation des modèles de régression. RSquared prend des valeurs entre 0 et 1. Plus sa valeur est proche de 1, plus le modèle est bon. Ajoutez le code suivant dans la méthode `Evaluate` pour afficher la valeur RSquared :

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a>Utiliser le modèle pour les prévisions

Ensuite, créez une classe afin d’héberger les scénarios de test à utiliser pour vérifier le bon fonctionnement du modèle :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestTrips.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :

   [!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

Ce tutoriel utilise une course test au sein de cette classe. Par la suite, vous pouvez ajouter d’autres scénarios à tester avec le modèle. Ajoutez le code suivant à la classe `TestTrips` :

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

Le tarif réel de cette course est 29,5. Utilisez 0 comme espace réservé, car le modèle prédit le prix.

Pour prévoir le prix de la course spécifiée, revenez au fichier *Program.cs* et ajoutez le code suivant dans la méthode `Main` :

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.

Félicitations ! Vous avez créé un modèle Machine Learning pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez utilisé pour faire des prédictions. Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).

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
