---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 06/04/2018
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: 57ade448f5773bee3474cb46bec8ad33e3afbee3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43391057"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a>Tutoriel : Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Cet exemple de tutoriel illustre l’utilisation de ML.NET pour créer un classifieur de sentiments via une application console .NET Core à l’aide de C# dans Visual Studio 2017.

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer vos données
> * Créer le pipeline d’apprentissage
> * Charger un classifieur
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle avec un autre jeu de données
> * Prédire les résultats des données de test avec le modèle

## <a name="sentiment-analysis-sample-overview"></a>Vue d’ensemble d’un exemple d’analyse des sentiments

L’exemple est une application console qui utilise ML.NET pour effectuer l’apprentissage d’un modèle qui classifie et prédit un sentiment positif ou négatif. Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité. Les jeux de données de sentiments proviennent du projet WikiDetox.

## <a name="prerequisites"></a>Prérequis

* [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

* Le [fichier Wikipédia séparé par des onglets, contenant des données sur la ligne de désintoxication (wikiPedia-detox-250-line-data.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv).
* Le [fichier Wikipédia séparé par des onglets, contenant le test de la ligne de désintoxication (wikipedia-detox-250-line-test.tsv)](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv).

## <a name="machine-learning-workflow"></a>Flux de travail de l’apprentissage automatique

Ce didacticiel suit un flux de travail d’apprentissage automatique permettant au processus de se dérouler de manière ordonnée.

Les phases du flux de travail sont les suivantes :

1. **Comprendre le problème**
2. **Ingérer les données**
3. **Prétraiter les données et générer les fonctionnalités**
4. **Effectuer l’apprentissage du modèle et le prédire**
5. **Évaluer le modèle**
6. **Opérationnalisation du modèle**

### <a name="understand-the-problem"></a>Comprendre le problème

Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle. La décomposition du problème vous permet de prédire et d’évaluer les résultats.

Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.

Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.

Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Pour ce problème, vous disposez des éléments suivants :

Données d’apprentissage : les commentaires sur le site web peuvent être positifs ou négatifs (**sentiment**).
Prédisez le **sentiment** d’un nouveau commentaire sur le site web, positif ou négatif, comme dans les exemples suivants :

* Évitez d’ajouter des informations non pertinentes à Wikipédia.
* C’est le meilleur, et l’article doit le souligner.

La tâche d’apprentissage automatique de classification est idéale pour ce scénario.

### <a name="about-the-classification-task"></a>À propos de la tâche de classification

La classification est une tâche d’apprentissage automatique qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données. Par exemple, vous pouvez utiliser la classification pour :

* Identifier un sentiment positif ou négatif.
* Classer un e-mail comme spam, indésirable ou autorisé.
* Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.
* Classer des clients selon leur tendance à répondre à une campagne commerciale.

Les tâches de classification sont souvent de ce type :

* Binaire : A ou B.
* Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue *Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.

2. Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

3. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

### <a name="prepare-your-data"></a>Préparer vos données

1. Téléchargez les jeux de données [WikiPedia detox-250-line-data.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) et [wikipedia-detox-250-line-test.tsv](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment. Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.

2. Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

### <a name="create-classes-and-define-paths"></a>Créer des classes et définir des chemins

Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#1 "Add necessary usings")]

Vous devez créer trois champs globaux pour contenir les chemins des fichiers récemment téléchargés :

* `_dataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.
* `_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.
* `_modelPath` contient le chemin d’accès où le modèle formé est enregistré.

Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins :

[!code-csharp[Declare file variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#2 "Declare variables to store data files")]

Vous devez créer des classes pour vos données d’entrée et prévisions. Ajoutez une nouvelle classe à votre projet :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.

1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.

    Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code. Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#1 "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#2 "Declare data record types")]

`SentimentData` représente la classe du jeu de données d’entrée et contient un élément `float` (`Sentiment`) qui a une valeur de sentiment positive ou négative ainsi qu’une chaîne pour le commentaire (`SentimentText`). Les deux champs sont associés à des attributs `Column`. Cet attribut décrit l’ordre de chaque champ dans le fichier de données, et désigne le champ `Label`. `SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé. Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`. L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle. L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation. L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.

Dans le fichier *Program.cs*, modifiez la signature de la méthode `Main` en remplaçant `void` par `async Task`, comme dans l’exemple suivant :

```csharp
static async Task Main(string[] args) 
{

}
```

Vous ajoutez `async` à `Main` avec un type de retour <xref:System.Threading.Tasks.Task> car vous enregistrerez ultérieurement le modèle dans un fichier zip, et le programme doit attendre que cette tâche externe se termine.

> [!NOTE]
> Une méthode *async main* vous permet d’utiliser `await` dans votre méthode `Main`. Pour plus d’informations, consultez la rubrique [async main](../../../docs/csharp/programming-guide/main-and-command-args/index.md) du guide de programmation C#.

Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :

[!code-csharp[Train](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#3 "Train your model")]

La méthode `Train` exécute les tâches suivantes :

* Charge ou ingère les données.
* Prétraite et fonctionnalise les données.
* Effectue l’apprentissage du modèle.
* Prédit les sentiments en fonction des données de test.

Créez la méthode `Train` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
public static async Task<PredictionModel<SentimentData, SentimentPrediction>> Train()
{

}
```

## <a name="ingest-the-data"></a>Ingérer les données

Initialise une nouvelle instance de <xref:Microsoft.ML.LearningPipeline>, qui inclut le chargement des données, le traitement/la fonctionnalisation des données, et le modèle. Ajoutez le code suivant comme première ligne de la méthode `Train` :

[!code-csharp[LearningPipeline](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#5 "Create a learning pipeline")]

L’objet <xref:Microsoft.ML.Data.TextLoader> est la première partie du pipeline, et charge les données du fichier d’apprentissage.

[!code-csharp[TextLoader](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#6 "Add a text loader to the pipeline")]

## <a name="data-preprocess-and-feature-engineering"></a>Prétraiter les données et générer les fonctionnalités

Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage. Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs. L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs. Les pipelines de transformation ML.NET vous permettent de composer un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test. Les transformations servent principalement à fonctionnaliser les données. Un pipeline de transformation offre l’avantage suivant : après définition du pipeline de transformation, vous pouvez enregistrer le pipeline pour tester les données.

Appliquez un pipeline <xref:Microsoft.ML.Transforms.TextFeaturizer> pour convertir la colonne `SentimentText` en un [vecteur numérique](../resources/glossary.md#numerical-feature-vector) appelé `Features` utilisé par l’algorithme d’apprentissage automatique. Il s’agit de l’étape de prétraitement/fonctionnalisation. L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle. Ajoutez `TextFeaturizer` au pipeline comme ligne de code suivante :

[!code-csharp[TextFeaturizer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#7 "Add a TextFeaturizer to the pipeline")]

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

L’objet <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier> est un apprenant d’arbre de décision que vous utiliserez dans ce pipeline. Comme pour l’étape de fonctionnalisation, si vous testez les différents apprenants disponibles dans ML.NET et modifiez leurs paramètres, vous obtenez des résultats différents. Pour le paramétrage, vous pouvez définir des [hyperparamètres](../resources/glossary.md#hyperparameter) comme <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumTrees>, <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.NumLeaves> et <xref:Microsoft.ML.Trainers.FastTreeBinaryClassifier.MinDocumentsInLeafs>. Spécifiques au modèle, ces hyperparamètres sont définis avant qu’un élément quelconque n’affecte le modèle. Ils sont utilisés pour paramétrer l’arbre de décision pour les performances et, par conséquent, les valeurs trop grandes peuvent nuire à ces performances.

Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[BinaryClassifier](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#8 "Add a fast binary tree classifier")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.PredictionModel%602>, selon le jeu de données qui a été chargé et transformé. `pipeline.Train<SentimentData, SentimentPrediction>()` effectue l’apprentissage du pipeline (charge les données, forme le générateur de fonctionnalités et l’apprenant). L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.

Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#9 "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a>Enregistrer et revenir au modèle formé à utiliser pour l’évaluation

À ce stade, vous disposez d’un modèle qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code à la ligne suivante dans `Train` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#10 "Save the model")]

Retournez le modèle à la fin de la méthode `Train`.

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#11 "Return the model")]

## <a name="evaluate-the-model"></a>Évaluer le modèle

Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation. Dans la méthode `Evaluate`, le modèle créé dans `Train` est passé pour évaluation. Créez la méthode `Evaluate` juste après `Train`, comme dans le code suivant :

```csharp
public static void Evaluate(PredictionModel<SentimentData, SentimentPrediction> model)
{

}
```

La méthode `Evaluate` exécute les tâches suivantes :

* Charge le jeu de données de test.
* Crée l’évaluateur binaire.
* Évalue le modèle et crée des métriques.
* Affiche les métriques.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#12 "Call the Evaluate method")]

La classe <xref:Microsoft.ML.Data.TextLoader> charge le nouveau jeu de données de test avec le même schéma. Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité. Ajoutez le code suivant à la méthode `Evaluate` :

[!code-csharp[LoadText](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#13 "Load the test dataset")]

L’objet <xref:Microsoft.ML.Models.BinaryClassificationEvaluator> calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié. Pour afficher ces métriques, ajoutez l’évaluateur comme ligne suivante dans la méthode `Evaluate`, avec le code suivant :

[!code-csharp[BinaryEvaluator](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#14 "Create the binary evaluator")]

<xref:Microsoft.ML.Models.BinaryClassificationMetrics> contient les métriques globales calculées par les évaluateurs de classification binaire. Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques. Ajoutez le code suivant :

[!code-csharp[CreateMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#15 "Evaluate the model and create metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a>Affichage des métriques pour la validation du modèle

Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#16 "Display selected metrics")]

## <a name="predict-the-test-data-outcomes-with-the-model"></a>Prédire les résultats des données de test avec le modèle

Créez la méthode `Predict` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
public static void Predict(PredictionModel<SentimentData, SentimentPrediction> model)
{

}
```

La méthode `Predict` exécute les tâches suivantes :

* Crée les données de test.
* Prédit les sentiments en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#17 "Call the Predict method")]

Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `Predict` :

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#18 "Create test data for predictions")]

Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.PredictionModel.Predict%2A?displayProperty=nameWithType>. Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#19 "Create predictions of sentiments")]

### <a name="model-operationalization-prediction"></a>Opérationnalisation du modèle : prédiction

Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence. Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles. Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#20 "Display prediction outputs")]

Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit. Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#21 "Build the pairs of sentiment data and predictions")]

Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#22 "Display the predictions")]

Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.
Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="results"></a>Résultats

Vos résultats doivent être similaires à ce qui suit. Lors du traitement, le pipeline affiche des messages. Vous pouvez voir des avertissements ou des messages de traitement. Ils ont été supprimés des résultats ci-dessous par souci de clarté.

```

PredictionModel quality metrics evaluation
------------------------------------------
Accuracy: 66.67%
Auc: 94.44%
F1Score: 75.00%

Sentiment Predictions
---------------------
Sentiment: Please refrain from adding nonsense to Wikipedia. | Prediction: Negative
Sentiment: He is the best, and the article should say that. | Prediction: Positive

```

Félicitations ! Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction des sentiments de messages. Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner la tâche d’apprentissage automatique appropriée
> * Préparer vos données
> * Créer le pipeline d’apprentissage
> * Charger un classifieur
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle avec un autre jeu de données
> * Prédire les résultats des données de test avec le modèle

Passer au tutoriel suivant pour en savoir plus
> [!div class="nextstepaction"]
> [Prédiction du prix d’une course de taxi](taxi-fare.md)
