---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 12/20/2018
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: c6ef4da7f429b92591c90daa3fb06f367d8a578a
ms.sourcegitcommit: 3b9b7ae6771712337d40374d2fef6b25b0d53df6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54030156"
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
> * Prédire une seule instance de résultat du test de données avec le modèle
> * Prédire les résultats des données de test avec un modèle chargé

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
2. **Préparer vos données**
   * **Charger les données**
   * **Extraire des caractéristiques (transformer vos données)**
3. **Générer et former** 
   * **Effectuer l’apprentissage du modèle**
   * **Évaluer le modèle**
4. **Exécuter**
   * **Consommation de modèle**

### <a name="understand-the-problem"></a>Comprendre le problème

Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle. La décomposition du problème vous permet de prédire et d’évaluer les résultats.

Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.

Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.

Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.

## <a name="select-the-appropriate-machine-learning-task"></a>Sélectionner la tâche d’apprentissage automatique appropriée

Pour ce problème, vous disposez des éléments suivants :

Données d’apprentissage : les commentaires sur le site web peuvent être positifs (1) ou négatifs (0) (**sentiment**).
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

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.

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

Vous devez créer trois champs globaux pour contenir les chemins d’accès aux fichiers récemment téléchargés, et une variable globale pour `TextLoader` :

* `_trainDataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.
* `_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.
* `_modelPath` contient le chemin d’accès où le modèle formé est enregistré.
* `_textLoader` est l’élément <xref:Microsoft.ML.Runtime.Data.TextLoader> utilisé pour charger et transformer les jeux de données.

Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins et la variable `_textLoader` :

[!code-csharp[Declare global variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#2 "Declare global variables")]

Vous devez créer des classes pour vos données d’entrée et prévisions. Ajoutez une nouvelle classe à votre projet :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.

1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.

    Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code. Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#1 "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#2 "Declare data record types")]

`SentimentData` représente la classe du jeu de données d’entrée et contient un élément `float` (`Sentiment`) qui a une valeur de sentiment positive ou négative ainsi qu’une chaîne pour le commentaire (`SentimentText`). Les deux champs sont associés à des attributs `Column`. Cet attribut décrit l’ordre de chaque champ dans le fichier de données, et désigne le champ `Label`. `SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé. Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`. L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle. L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation. L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.

Lors de la création d’un modèle avec ML .NET, vous commencez par créer un `MLContext`. Cela s’apparente conceptuellement à l’aide `DbContext` dans Entity Framework. L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.

### <a name="initialize-variables-in-main"></a>Initialiser les variables dans Principal

Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.  Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#3 "Create the ML Context")]

Ensuite, pour configurer le chargement des données, initialisez variable globale `_textLoader` afin de la réutiliser.  Notez que vous utilisez un `TextReader`. Lorsque vous créez un `TextLoader` à l’aide d’un `TextReader`, vous passez le contexte nécessaire et la classe <xref:Microsoft.ML.Runtime.Data.TextLoader.Arguments> qui permet la personnalisation.

 Spécifiez le schéma de données en passant un tableau d’objets <xref:Microsoft.ML.Runtime.Data.TextLoader.Column> au chargeur contenant tous les noms de colonne et leurs types. Vous avez défini précédemment le schéma de données en créant notre classe `SentimentData`. Pour notre schéma, la première colonne (étiquette) est une <xref:System.Boolean> (la prédiction) et la deuxième colonne (SentimentText) est la caractéristique de type texte/chaîne utilisée pour prédire le sentiment.
La classe `TextReader` retourne une variable <xref:Microsoft.ML.Runtime.Data.TextLoader> totalement initialisée  

Pour initialiser la variable globale `_textLoader` afin de la réutiliser pour les jeux de données nécessaires, ajoutez le code suivant après l’initialisation de `mlContext` :

[!code-csharp[initTextReader](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#4 "Initialize the TextReader")]

Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :

[!code-csharp[Train](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#5 "Train your model")]

La méthode `Train` exécute les tâches suivantes :

* Charge les données.
* Extrait et transforme les données.
* Effectue l’apprentissage du modèle.
* Prédit les sentiments en fonction des données de test.
* Retourne le modèle.

Créez la méthode `Train` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
 public static ITransformer Train(MLContext mlContext, string dataPath)
{

}
```

Notez que les deux paramètres sont passés dans la méthode Train ; un `MLContext` pour le contexte (`mlContext`) et un <xref:System.String> pour le chemin d’accès au jeu de données (`dataPath`). Vous allez utiliser cette méthode plusieurs fois pour l’apprentissage et le test.

## <a name="load-the-data"></a>Charger les données

Vous allez charger les données en utilisant la variable globale `_textLoader` et le paramètre `dataPath`. Cette méthode retourne un <xref:Microsoft.ML.Runtime.Data.IDataView>. En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.

Dans ML.NET, les données sont semblables à une vue SQL. Elles sont évaluées tardivement, schématisées et hétérogènes. L’objet est la première partie du pipeline, et charge les données. Pour ce tutoriel, il charge un jeu de données avec des commentaires et les sentiments positifs ou négatifs correspondants. Cette méthode permet de créer puis de former le modèle.

 Ajoutez le code suivant comme première ligne de la méthode `Train` :

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#6 "loading training dataset")]

## <a name="extract-and-transform-the-data"></a>Extraire et transformer les données

Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage. Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs. L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.

Les pipelines de transformation ML.NET composent un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test. Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données. Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent. Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).

Appliquez un pipeline `mlContext.Transforms.Text.FeaturizeText` pour convertir la colonne `SentimentText` en un vecteur numérique appelé `Features` utilisé par l’algorithme Machine Learning. Il s’agit d’un appel de wrapper qui retourne un <xref:Microsoft.ML.Runtime.Data.EstimatorChain%601> qui sera un pipeline. Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`. Ajoutez le contenu suivant comme prochaine ligne de code :

[!code-csharp[TextFeaturizingEstimator](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#7 "Add a TextFeaturizingEstimator")]

Il s’agit de l’étape de prétraitement/fonctionnalisation. L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Pour ajouter le formateur, appelez la méthode de wrapper `mlContext.Transforms.Text.FeaturizeText` qui retourne un objet <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer>. Il s’agit d’un apprenant d’arbre de décision que vous utiliserez dans ce pipeline. L’objet `FastTreeBinaryClassificationTrainer` est ajouté à `pipeline` et accepte les caractéristiques `SentimentText` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir de l’historique des données.

Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[FastTreeBinaryClassificationTrainer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#8 "Add a FastTreeBinaryClassificationTrainer")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé. Une fois l’estimation définie, vous formez votre modèle à l’aide du <xref:Microsoft.ML.Runtime.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées. Cette méthode retourne un modèle à utiliser pour les prédictions. `pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis. L’expérience n’est pas exécutée tant que cette opération n’a pas été effectuée.

Ajoutez le code suivant à la méthode `Train` :

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#9 "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a>Enregistrer et revenir au modèle formé à utiliser pour l’évaluation

À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Retournez le modèle à la fin de la méthode `Train`.

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#10 "Return the model")]

## <a name="evaluate-the-model"></a>Évaluer le modèle

Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation. Dans la méthode `Evaluate`, le modèle créé dans `Train` est passé pour évaluation. Créez la méthode `Evaluate` juste après `Train`, comme dans le code suivant :

```csharp
public static void Evaluate(MLContext mlContext, ITransformer model)
{

}
```

La méthode `Evaluate` exécute les tâches suivantes :

* Charge le jeu de données de test.
* Crée l’évaluateur binaire.
* Évalue le modèle et crée des métriques.
* Affiche les métriques.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#11 "Call the Evaluate method")]

Vous allez charger le jeu de données de test à l’aide de la variable globale `_textLoader` précédemment initialisée avec le champ global `_testDataPath`. Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité. Ajoutez le code suivant à la méthode `Evaluate` :

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#12 "Load the test dataset")]

Vous allez ensuite utiliser le paramètre Machine Learning `model` (un transformateur) pour saisir les fonctionnalités et retourner des prédictions. Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#13 "Predict using the Transformer")]

La méthode `BinaryClassificationContext.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié. Elle renvoie un objet `BinaryClassificationEvaluator.CalibratedResult` contenant les métriques globales calculées par les évaluateurs de classification binaire. Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques. Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#14 "Compute Metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a>Affichage des métriques pour la validation du modèle

Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#15 "Display selected metrics")]

Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `TrainFinalModel` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#23 "Save the model")]

## <a name="save-the-model-as-azip-file"></a>Enregistrer le modèle en tant que fichier .zip

Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

La méthode `SaveModelAsFile` exécute les tâches suivantes :

* Enregistre le modèle sous la forme d’un fichier .zip.

Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications. Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.Runtime.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>. Pour l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`. Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#24 "Add the SaveTo Method")]

Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-model-and-a-single-comment"></a>Prédire le résultat de données de test avec le modèle et un commentaire unique

Créez la méthode `Predict` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void Predict(MLContext mlContext, ITransformer model)
{

}
```

La méthode `Predict` exécute les tâches suivantes :

* Crée un commentaire unique de données de test.
* Prédit les sentiments en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :

[!code-csharp[CallPredict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#16 "Call the Predict method")]

Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels. Le <xref:Microsoft.ML.Runtime.Data.PredictionFunction%602> est un wrapper retourné par la méthode `MakePredictionFunction`. Nous allons ajouter le code suivant pour créer PredictionFunction comme première ligne dans la méthode `Predict` :

[!code-csharp[MakePredictionFunction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#17 "Create the PredictionFunction")]
  
Ajoutez un commentaire pour tester la prédiction du modèle formé dans la méthode `Predict` en créant une instance de `SentimentData` :

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#18 "Create test data for single prediction")]


 Vous pouvez l’utiliser pour prédire le sentiment positif ou négatif d’une instance unique de données de commentaires. Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.Runtime.Data.PredictionFunction%602.Predict(%600)> sur les données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#19 "Create a prediction of sentiment")]

### <a name="model-operationalization-prediction"></a>Opérationnalisation du modèle : prédiction

Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence. Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles. Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#20 "Display prediction output")]

## <a name="predict-the-test-data-outcomes-with-the-saved-model"></a>Prédire les résultats des données de test avec le modèle enregistré

Créez la méthode `PredictWithModelLoadedFromFile` juste avant la méthode `SaveModelAsFile`, en utilisant le code suivant :

```csharp
public static void PredictWithModelLoadedFromFile(MLContext mlContext)
{

}
```

La méthode `PredictWithModelLoadedFromFile` exécute les tâches suivantes :

* Crée les données de test par lots.
* Prédit les sentiments en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Predict`, en utilisant le code suivant :

[!code-csharp[CallPredictModelLoaded](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#25 "Call the PredictWithModelLoadedFromFile method")]

Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `PredictWithModelLoadedFromFile` :

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#26 "Create test data for predictions")]

Charger le modèle

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#27 "Load the model")]

Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.Core.Data.ITransformer.Transform(Microsoft.ML.Runtime.Data.IDataView)>. Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique. Ajoutez le code suivant à la méthode `PredictWithModelLoadedFromFile` pour les prédictions :

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#28 "Create predictions of sentiments")]

### <a name="model-operationalization-prediction"></a>Opérationnalisation du modèle : prédiction

Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence. Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles. Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#29 "Display prediction outputs")]

Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit. Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#30 "Build the pairs of sentiment data and predictions")]

Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#31 "Display the predictions")]

Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.
Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="results"></a>Résultats

Vos résultats doivent être similaires à ce qui suit. Lors du traitement, le pipeline affiche des messages. Vous pouvez voir des avertissements ou des messages de traitement. Ils ont été supprimés des résultats ci-dessous par souci de clarté.

```console
Model quality metrics evaluation
--------------------------------
Accuracy: 94.44%
Auc: 98.77%
F1Score: 94.74%
=============== End of model evaluation ===============

=============== Prediction Test of model with a single sample and test dataset ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.5297049
=============== End of Predictions ===============

=============== New iteration of Model ===============
=============== Create and Train the Model ===============
=============== End of training ===============


The model is saved to: C:\Tutorial\SentimentAnalysis\bin\Debug\netcoreapp2.0\Data\Model.zip

=============== Prediction Test of loaded model with a multiple samples ===============

Sentiment: This is a very rude movie | Prediction: Toxic | Probability: 0.4585565
Sentiment: He is the best, and the article should say that. | Prediction: Not Toxic | Probability: 0.9924279

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
