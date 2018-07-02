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
# <a name="tutorial-use-mlnet-to-predict-new-york-taxi-fares-regression"></a>Tutoriel : Utiliser ML.NET pour prédire le prix des courses de taxi à New York (régression)

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce tutoriel montre l’utilisation de ML.NET pour générer un [modèle de régression](../resources/glossary.md#regression) afin de prédire le prix des courses de taxi à New York.

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer et comprendre vos données
> * Créer un pipeline d’apprentissage
> * Charger et transformer vos données
> * Choisir un algorithme d’apprentissage
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Utiliser le modèle pour les prévisions

## <a name="prerequisites"></a>Prérequis

* [Visual Studio 2017 15.6 ou version ultérieure](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

## <a name="understand-the-problem"></a>Comprendre le problème

Ce problème est centré autour de la **prédiction du prix d’une course de taxi à New York**. À première vue, ce prix semble dépendre simplement de la distance parcourue. Mais les chauffeurs de taxi à New York appliquent différents tarifs selon des facteurs comme le nombre de passagers supplémentaires ou le paiement par carte de crédit plutôt que par espèces.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Pour prédire le prix de la course de taxi, vous sélectionnez d’abord la tâche d’apprentissage automatique appropriée. Vous devez prédire une valeur réelle (valeur double qui représente le prix) en fonction des autres facteurs du jeu de données. Vous choisissez une tâche de [**régression**](../resources/glossary.md#regression).

Le processus d’apprentissage du modèle identifie les facteurs du jeu de données qui impactent le plus la prédiction du prix final de la course.

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez TaxiFarePrediction, puis cliquez sur le bouton **OK**.

2. Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

3. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

### <a name="prepare-and-understand-your-data"></a>Préparer et comprendre vos données

1. Téléchargez les jeux de données [taxi-fare-train.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-train.csv) et [taxi-fare-test.csv](https://github.com/dotnet/machinelearning/blob/master/test/data/taxi-fare-test.csv), puis enregistrez-les dans le dossier *Données* créé précédemment. Le jeu de données Taxi Trip effectue l’apprentissage automatique du modèle et peut servir à évaluer la précision de votre modèle. Ces jeux de données proviennent du [jeu de données NYC TLC Taxi Trip](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml).

2. Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.csv, puis sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Toujours**.

3. Ouvrez le jeu de données **taxi-fare-train.csv** dans l’éditeur de code et examinez les en-têtes de colonne dans la première ligne. Examinons chacune des colonnes. Analysez les données et identifiez les colonnes qui représentent des **fonctionnalités** et celle qui constitue l’**étiquette**.

L’**étiquette** est l’identificateur de la colonne que vous tentez de prédire. Les **fonctionnalités** identifiées servent à prédire l’étiquette.

* **vendor_id :** l’ID du taxi est une fonctionnalité.
* **rate_code :** le type de tarif de la course de taxi est une fonctionnalité.
* **passenger_count :** le nombre de passagers embarqués est une fonctionnalité.
* **trip_time_in_secs :** durée totale de la course. Vous ne connaissez la durée de la course qu’une fois celle-ci terminée. Vous excluez cette colonne du modèle.
* **trip_distance :** la distance de la course est une fonctionnalité.
* **payment_type :** le mode de paiement (espèces ou carte de crédit) est une fonctionnalité.
* **fare_amount :** le prix total payé pour la course est l’étiquette.

### <a name="create-classes-and-define-paths"></a>Créer des classes et définir des chemins

Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#1 "Add necessary usings")]

Vous devez créer trois variables globales pour contenir les chemins d’accès aux fichiers récemment téléchargés et pour enregistrer le modèle :

* `_datapath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.
* `_testdatapath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.
* `_modelpath` contient le chemin d’accès où le modèle formé est stocké.

Ajoutez le code suivant à la ligne directement au-dessus de `Main` pour spécifier les fichiers récemment téléchargés :

[!code-csharp[InitializePaths](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#2 "Define variables to store the data file paths")]

Ensuite, créez des classes pour les données d’entrée et les prédictions :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TaxiTrip.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Ajoutez les instructions `using` suivantes au nouveau fichier :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#1 "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `TaxiTrip` et `TaxiTripFarePrediction`, au fichier *TaxiTrip.cs* :

[!code-csharp[DefineTaxiTrip](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TaxiTrip.cs#2 "Define the taxi trip and fare predictions classes")]

`TaxiTrip` est la classe du jeu de données d’entrée et contient des définitions pour chacune des colonnes du jeu de données. La classe `TaxiTripFarePrediction` est utilisée pour la prédiction, une fois le modèle formé. Elle contient une valeur flottante unique (`FareAmount`) et un attribut `Score` [ColumnName](xref:Microsoft.ML.Runtime.Api.ColumnNameAttribute) appliqué.

Revenez maintenant au fichier **Program.cs**. Dans `Main`, remplacez `Console.WriteLine("Hello World!")` par le code suivant :

```csharp
PredictionModel<TaxiTrip, TaxiTripFarePrediction> model = Train();
```

La méthode `Train` effectue l’apprentissage de votre modèle. Créez cette fonction juste sous `Main`, en utilisant le code suivant :

```csharp
public static PredictionModel<TaxiTrip, TaxiTripFarePrediction> Train()
{

}
```

## <a name="create-a-learning-pipeline"></a>Créer un pipeline d’apprentissage

Le pipeline d’apprentissage charge toutes les données et tous les algorithmes nécessaires à l’apprentissage du modèle. Ajoutez le code suivant à la méthode `Train()` :

```csharp
var pipeline = new LearningPipeline();
```

## <a name="load-and-transform-your-data"></a>Charger et transformer vos données

Ensuite, chargez vos données dans le pipeline. Pointez vers le chemin `_datapath` créé initialement, puis spécifiez le délimiteur de fichier .csv (,). Ajoutez le code suivant dans la méthode `Train()`, sous la dernière étape :

```csharp
pipeline.Add(new TextLoader(_datapath).CreateFrom<TaxiTrip>(separator:','));
```

Vous ferez référence aux colonnes sans les traits de soulignement dans le code que vous créez. Copiez la colonne `FareAmount` dans une nouvelle colonne appelée « Étiquette » à l’aide de la fonction `ColumnCopier()`. Cette colonne est l’**étiquette**.

```csharp
pipeline.Add(new ColumnCopier(("FareAmount", "Label")));
```

Effectuez une **ingénierie de fonctionnalité** pour transformer les données afin de les utiliser efficacement pour l’apprentissage automatique. L’algorithme qui effectue l’apprentissage du modèle nécessite des fonctionnalités **numériques** car vous transformez les données catégoriques (`VendorId`, `RateCode` et `PaymentType`) en nombres. La fonction `CategoricalOneHotVectorizer()` attribue une clé numérique aux valeurs de chacune de ces colonnes. Transformez vos données en ajoutant ce code :

```csharp
pipeline.Add(new CategoricalOneHotVectorizer("VendorId",
                                             "RateCode",
                                             "PaymentType"));
```

La dernière étape de la préparation des données combine toutes vos **fonctionnalités** dans un vecteur à l’aide de la fonction `ColumnConcatenator()`. Cette étape nécessaire permet à l’algorithme de traiter facilement vos fonctionnalités. Ajoutez le code suivant :

```csharp
pipeline.Add(new ColumnConcatenator("Features",
                                    "VendorId",
                                    "RateCode",
                                    "PassengerCount",
                                    "TripDistance",
                                    "PaymentType"));
```

Notez que la colonne `trip_time_in_secs` n’est pas incluse. Vous avez déterminé que cette fonctionnalité de prévision n’est pas utile.

> [!NOTE]
> Ces étapes doivent être ajoutées au pipeline dans l’ordre spécifié ci-dessus pour garantir une exécution réussie.

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Après avoir ajouté les données au pipeline et les avoir transformées au format d’entrée approprié, sélectionnez un algorithme d’apprentissage (**apprenant**). L’algorithme d’apprentissage forme le modèle. Vous avez choisi une **tâche de régression** pour ce problème. Par conséquent, vous ajoutez un apprenant appelé `FastTreeRegressor()` au pipeline qui utilise un **boosting de gradient**.

Le boosting de gradient est une technique d’apprentissage automatique pour résoudre les problèmes de régression. Il génère chaque arbre de régression étape par étape. Il utilise une fonction de perte prédéfinie pour mesurer l’erreur à chaque étape et la corriger à la prochaine. Le résultat est un modèle de prévision qui est en fait un ensemble de modèles de prédiction moins efficaces. Pour plus d’informations sur le boosting de gradient, consultez [Régression d’arbre de décision boostée](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/boosted-decision-tree-regression).

Ajoutez le code suivant dans la méthode `Train()`, après le code de traitement des données ajouté à la dernière étape :

```csharp
pipeline.Add(new FastTreeRegressor());
```

Vous avez ajouté toutes les étapes précédentes au pipeline en tant qu’instructions individuelles, mais C# propose une syntaxe d’initialisation de collection pratique qui facilite la création et l’initialisation du pipeline. Remplacez le code que vous avez ajouté à la méthode `Train()` par le code suivant :

[!code-csharp[CreatePipeline](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#3 "Create and initialize the learning pipeline")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

La dernière étape consiste à effectuer l’apprentissage du modèle. À ce stade, rien dans le pipeline n’a été exécuté. La fonction `pipeline.Train<T_Input, T_Output>()` sélectionne le type de classe `TaxiTrip` prédéfini et génère un type `TaxiTripFarePrediction`. Ajoutez cette dernière partie de code à la fonction `Train()` :

[!code-csharp[TrainMOdel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#4 "Train your model")]

Et voilà ! Vous avez correctement formé un modèle capable de prédire le prix des courses de taxi à New York. Examinons maintenant le niveau de précision de votre modèle et comment l’utiliser.

## <a name="save-the-model"></a>Enregistrer le modèle

Avant de passer à l’étape suivante, enregistrez votre modèle dans un fichier .zip, en ajoutant le code suivant à la fin de votre fonction `Train()` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#5 "Save the model asynchronously and return the model")]

L’ajout de l’instruction `await` à l’appel `model.WriteAsync()` signifie que la méthode `Train()` doit être remplacée par une méthode asynchrone qui retourne un élément `Task`. Modifiez la signature de `Train`, comme indiqué dans le code suivant :

[!code-csharp[AsyncTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#6 "Make the Train method async and return a task.")]

La modification du type de retour de la méthode `Train` signifie que vous devez ajouter un élément `await` au code qui appelle `Train` dans la méthode `Main`, comme indiqué dans le code suivant :

[!code-csharp[AwaitTraining](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#7 "Await the Train method")]

L’ajout d’un élément `await` à votre méthode `Main` signifie que la méthode `Main` doit avoir le modificateur `async` et retourner un élément `Task` :

[!code-csharp[AsyncMain](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#8 "Make the Main method async and return a task.")]

Vous devez également ajouter l'instruction suivante en haut du fichier :

[!code-csharp[UsingTasks](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#9 "Add System.Threading.Tasks. to your usings.")]

Comme la méthode `async Main` constitue une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.
Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="evaluate-the-model"></a>Évaluer le modèle

L’évaluation est le processus de vérification du fonctionnement du modèle. Il est important que votre modèle effectue des prévisions correctes sur les données qu’il n’a pas utilisées lors de son apprentissage. Pour cela, vous pouvez fractionner les données en plusieurs jeux de données d’apprentissage et de test, comme vous l’avez fait dans ce tutoriel. Maintenant que vous avez formé le modèle avec les données d’apprentissage, vous pouvez évaluer son efficacité sur les données de test.

Revenez à votre fonction `Main` et ajoutez le code suivant sous l’appel à la méthode `Train()` :

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#10 "Evaluate the model.")]

La fonction `Evaluate()` évalue votre modèle. Créez cette fonction sous `Train()`. Ajoutez le code suivant :

```csharp
private static void Evaluate(PredictionModel<TaxiTrip, TaxiTripFarePrediction> model)
{

}
```

Chargez les données de test à l’aide de la fonction `TextLoader()`. Ajoutez le code suivant à la méthode `Evaluate()` :

[!code-csharp[LoadTestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#12 "Load the test data.")]

Ajoutez le code suivant pour évaluer le modèle et produire les métriques pour celui-ci :

[!code-csharp[EvaluateAndMeasure](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#13 "Evaluate the model and its predictions.")]

RMS est une métrique permettant d’évaluer les problèmes de régression. Plus sa valeur est faible, meilleur est votre modèle. Ajoutez le code suivant à la fonction `Evaluate()` afin d’imprimer la métrique RMS pour votre modèle.

[!code-csharp[DisplayRMS](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#14 "Display the RMS metric.")]

RSquared est une autre métrique permettant d’évaluer les problèmes de régression. RSquared sera une valeur comprise entre 0 et 1. Plus cette valeur est proche de 1, meilleur est votre modèle. Ajoutez le code suivant à la fonction `Evaluate()` afin d’imprimer la valeur RSquared pour votre modèle.

[!code-csharp[DisplayRSquared](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#15 "Display the RSquared metric.")]

## <a name="use-the-model-for-predictions"></a>Utiliser le modèle pour les prévisions

Créez maintenant une classe qui contiendra les scénarios de test que vous pouvez utiliser pour vérifier le bon fonctionnement de votre modèle :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.
1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *TestTrips.cs*. Ensuite, sélectionnez le bouton **Ajouter**.
1. Modifiez la classe pour la rendre statique, comme dans l’exemple suivant :

[!code-csharp[StaticClass](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#1 "Change class to be a static class.")]

Ce tutoriel utilise une course test au sein de cette classe. Plus tard, vous pourrez ajouter d’autres scénarios pour effectuer des essais avec cet exemple. Ajoutez le code suivant à la classe `TestTrips` :

[!code-csharp[TestData](../../../samples/machine-learning/tutorials/TaxiFarePrediction/TestTrips.cs#2 "Create aq trip to predict its cost.")]

Le prix réel de la course est de 29,5, mais utilisez la valeur 0 comme espace réservé. L’algorithme d’apprentissage automatique prédit le prix.

Ajoutez le code suivant à votre fonction `Main`. Il teste votre modèle à l’aide des données `TestTrip` :

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/TaxiFarePrediction/Program.cs#16 "Try a prediction.")]

Exécutez le programme afin d’afficher le prix prédit de la course pour votre cas de test.

Félicitations ! Vous avez correctement créé un modèle d’apprentissage automatique pour prédire le prix des courses de taxi, avez évalué sa précision et l’avez testé. Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/TaxiFarePrediction).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer et comprendre vos données
> * Créer un pipeline d’apprentissage
> * Charger et transformer vos données
> * Choisir un algorithme d’apprentissage
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Utiliser le modèle pour les prévisions

Consultez notre référentiel GitHub pour continuer l’apprentissage et obtenir d’autres exemples.
> [!div class="nextstepaction"]
> [Référentiel GitHub dotnet/machinelearning](https://github.com/dotnet/machinelearning/)
