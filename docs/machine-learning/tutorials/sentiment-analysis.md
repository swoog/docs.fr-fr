---
title: Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments
description: Découvrez comment utiliser ML.NET dans un scénario de classification binaire pour comprendre comment utiliser la prédiction de sentiment afin d’effectuer l’action appropriée.
ms.date: 03/07/2019
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: b0d02babd126a62ef9a87b251f525a08376069aa
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57845789"
---
# <a name="tutorial-use-mlnet-in-a-sentiment-analysis-binary-classification-scenario"></a>Tutoriel : Utiliser ML.NET dans un scénario de classification binaire d’une analyse de sentiments

Cet exemple de tutoriel montre comment utiliser ML.NET pour créer un classifieur de sentiments permettant de prédire un sentiment positif ou négatif dans une application console .NET Core avec C# dans Visual Studio 2017. Dans le monde du Machine Learning, ce type de prédiction est connu sous le nom de classification binaire.

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Ce tutoriel et l’exemple associé utilisent actuellement **ML.NET version 0.11**. Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Dans ce didacticiel, vous apprendrez à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner l’algorithme de machine learning approprié
> * Préparer vos données
> * Transformer les données
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Prédire avec le modèle entraîné
> * Déployer et prédire avec un modèle chargé

## <a name="sentiment-analysis-sample-overview"></a>Vue d’ensemble d’un exemple d’analyse des sentiments

L’exemple est une application console qui utilise ML.NET pour effectuer l’apprentissage d’un modèle qui classifie et prédit un sentiment positif ou négatif. Le jeu de données de sentiments Yelp, qui provient de l’université de Californie à Irvine (UCI), se divise en un jeu de données d’apprentissage et un jeu de données de test. L’exemple évalue le modèle avec le jeu de données de test à des fins d’analyse de la qualité. 

Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).

## <a name="prerequisites"></a>Prérequis

* [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

* [Le fichier zip du jeu de données UCI Sentiment Labeled Sentences](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/sentiment%20labelled%20sentences.zip)

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
4. **Déployer le modèle**
   * **Utiliser le modèle pour prédire**

### <a name="understand-the-problem"></a>Comprendre le problème

Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle. La décomposition du problème vous permet de prédire et d’évaluer les résultats.

Dans ce tutoriel, le problème consiste à comprendre les sentiments formulés pour le site web afin d’effectuer l’action appropriée.

Vous pouvez décomposer le problème en un texte et une valeur de sentiment pour les données avec lesquelles vous souhaitez effectuer l’apprentissage du modèle, puis une valeur de sentiment prédite que vous pouvez évaluer puis utiliser de façon opérationnelle.

Vous devez ensuite **déterminer** le sentiment, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.

## <a name="select-the-appropriate-machine-learning-algorithm"></a>Sélectionner l’algorithme de machine learning approprié

Pour ce problème, vous disposez des éléments suivants :

Données d’apprentissage : les commentaires sur le site web peuvent être positifs (1) ou négatifs (0) (**sentiment**).

Prédisez le **sentiment** d’un nouveau commentaire sur le site web, positif ou négatif, comme dans les exemples suivants :

* J’adore les serveurs de cet endroit. Ils sont super.
* Je n’ai jamais mangé une soupe aussi mauvaise qu’ici.

L’algorithme de machine learning de classification est idéal pour ce scénario.

### <a name="about-the-classification-algorithm"></a>À propos de l’algorithme de classification

La classification est un algorithme de machine learning qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données. Par exemple, vous pouvez utiliser la classification pour :

* Identifier un sentiment positif ou négatif.
* Classer un e-mail comme spam, indésirable ou autorisé.
* Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.
* Classer des clients selon leur tendance à répondre à une campagne commerciale.

Les algorithmes de classification sont souvent de l’un des types suivants :

* Binaire : A ou B.
* Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.

Dans la mesure où les commentaires du site web doivent être classés comme positifs ou négatifs, on utilise l’algorithme de classification binaire. 

## <a name="create-a-console-application"></a>Créer une application console

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « SentimentAnalysis », puis cliquez sur le bouton **OK**.

2. Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

3. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

### <a name="prepare-your-data"></a>Préparer vos données

1. Téléchargez le [fichier zip du jeu de données UCI Sentiment Labeled Sentences (voir les citations dans la remarque ci-dessous)](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/sentiment%20labelled%20sentences.zip) et décompressez-le.

2. Copiez le fichier `yelp_labelled.txt` dans le répertoire *Données* que vous avez créé.

> [!NOTE]
> Les jeux de données utilisés par ce tutoriel proviennent de « From Group to Individual Labels using Deep Features » (Kotzias et. al., KDD 2015), hébergé dans le référentiel UCI Machine Learning (Dua, D. et Karra Taniskidou, E., 2017). Référentiel UCI Machine Learning [http://archive.ics.uci.edu/ml]. Irvine (Californie) : Université de Californie, School of Information and Computer Science.

3. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le fichier `yelp_labeled.txt` et sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

### <a name="create-classes-and-define-paths"></a>Créer des classes et définir des chemins

Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddUsings "Add necessary usings")]

Il faut créer deux champs globaux pour le chemin d’accès du fichier de jeu de données téléchargé et celui du fichier de modèle enregistré :

* `_dataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.
* `_modelPath` contient le chemin d’accès où le modèle formé est enregistré.

Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins :

[!code-csharp[Declare global variables](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DeclareGlobalVariables "Declare global variables")]

Vous devez créer des classes pour vos données d’entrée et prévisions. Ajoutez une nouvelle classe à votre projet :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.

1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *SentimentData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.

    Le fichier *SentimentData.cs* s’ouvre dans l’éditeur de code. Ajoutez l'instruction suivante `using` en haut du fichier *SentimentData.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#AddUsings "Add necessary usings")]

Supprimez la définition de classe existante et ajoutez le code suivant, qui contient deux classes, `SentimentData` et `SentimentPrediction`, au fichier *SentimentData.cs* :

[!code-csharp[DeclareTypes](../../../samples/machine-learning/tutorials/SentimentAnalysis/SentimentData.cs#DeclareTypes "Declare data record types")]

La classe du jeu de données d’entrée, `SentimentData`, contient une `string` pour le commentaire (`SentimentText`) et un `bool` (`Sentiment`) qui a une valeur de sentiment positive ou négative. Les deux champs sont associés à des attributs <xref:Microsoft.ML.Data.LoadColumnAttribute.%23ctor%28System.Int32%29>. Cet attribut décrit l’ordre des champs dans le fichier de données.  Par ailleurs, la propriété `Sentiment` comporte un <xref:Microsoft.ML.Data.ColumnNameAttribute.%23ctor%2A> qui la désigne comme le champ `Label`. `SentimentPrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé. Il comporte une valeur booléenne unique (`Sentiment`) et un attribut `PredictedLabel` `ColumnName`. L’attribut `Label` sert à créer le modèle et à effectuer son apprentissage, mais il est aussi utilisé avec le jeu de données de test fractionné pour évaluer le modèle. L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation. L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.

Lors de la création d’un modèle avec ML .NET, vous commencez par créer un <xref:Microsoft.ML.MLContext>. D’un point de vue conceptuel, `MLContext` est comparable à `DbContext` dans Entity Framework. L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.

### <a name="initialize-variables-in-main"></a>Initialiser les variables dans Principal

Créez une variable appelée `mlContext` et initialisez-la avec une nouvelle instance de `MLContext`.  Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateMLContext "Create the ML Context")]

Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :

[!code-csharp[CallLoadData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallLoadData)]

La méthode `LoadData` exécute les tâches suivantes :

* Charge les données.
* Fractionne le jeu de données chargé en jeux de données d’apprentissage et de test.
* Retourne les jeux de données d’apprentissage et de test fractionnés.

Créez la méthode `LoadData` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
public static (IDataView trainSet, IDataView testSet) LoadData(MLContext mlContext)
{

}
```
## <a name="load-the-data"></a>Charger les données

Comme le type de modèle de données `SentimentData` créé précédemment correspond au schéma du jeu de données, il est possible de combiner l’initialisation, le mappage et le chargement du jeu de données en une seule ligne de code avec le wrapper `MLContext.Data.LoadFromTextFile` de la [méthode LoadFromTextFile](xref:Microsoft.ML.TextLoaderSaverCatalog.LoadFromTextFile%60%601%28Microsoft.ML.DataOperationsCatalog,System.String,System.Char,System.Boolean,System.Boolean,System.Boolean,System.Boolean%29). Cette méthode retourne un <xref:Microsoft.Data.DataView.IDataView>. 

 En tant qu’entrée et sortie de `Transforms`, un `DataView` est le type de pipeline de données fondamental, similaire à `IEnumerable` pour `LINQ`.

Dans ML.NET, les données sont semblables à une vue SQL. Elles sont évaluées tardivement, schématisées et hétérogènes. L’objet est la première partie du pipeline, et charge les données. Pour ce tutoriel, il charge un jeu de données avec des commentaires et les sentiments positifs ou négatifs correspondants. Cette méthode permet de créer puis de former le modèle.

 Ajoutez le code suivant comme première ligne de la méthode `LoadData` :

[!code-csharp[LoadData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#LoadData "loading dataset")]

### <a name="split-the-dataset-for-model-training-and-testing"></a>Fractionner le jeu de données pour l’apprentissage et le test du modèle

Deux jeux de données sont maintenant nécessaires : un jeu de données d’apprentissage pour entraîner le modèle et un jeu de données de test pour l’évaluer. Utilisez `MLContext.BinaryClassification.TrainTestSplit`, qui inclut <xref:Microsoft.ML.StaticPipe.TrainingStaticExtensions.TrainTestSplit%2A> dans un wrapper, pour fractionner le jeu de données chargé en jeux de données d’apprentissage et de test et les retourner dans <xref:Microsoft.ML.TrainCatalogBase.TrainTestData>. Pour spécifier la fraction de données réservée au jeu de test, utilisez le paramètre `testFraction`. La valeur par défaut est 10 %, mais on choisira dans ce cas 20 % pour consacrer davantage de données à l’évaluation.  

Pour fractionner les données chargées dans les jeux de données nécessaires, ajoutez le code suivant sur la ligne suivant la méthode `LoadData` :

[!code-csharp[SplitData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#SplitData "Split the Data")]

Retournez `splitDataView` à la fin de la méthode `LoadData` :

[!code-csharp[ReturnSplitData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#ReturnSplitData)]

## <a name="build-and-train-the-model"></a>Générer et entraîner le modèle

Ajoutez l’appel suivant à la méthode `BuildAndTrainModel` comme prochaine ligne de code dans la méthode `Main` :

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallBuildAndTrainModel)]

La méthode `BuildAndTrainModel` exécute les tâches suivantes :

* Extrait et transforme les données.
* Effectue l’apprentissage du modèle.
* Prédit les sentiments en fonction des données de test.
* Retourne le modèle.

Créez la méthode `BuildAndTrainModel` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
public static ITransformer BuildAndTrainModel(MLContext mlContext, IDataView splitTrainSet)
{

}
```

Deux paramètres sont passés à la méthode Train : `MLContext` pour le contexte (`mlContext`) et `IDataView` pour le jeu de données d’apprentissage (`splitTrainSet`). 

## <a name="extract-and-transform-the-data"></a>Extraire et transformer les données

Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage. Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs. L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.

Les pipelines de transformation ML.NET composent un ensemble personnalisé de transformations appliquées à vos données avant l’apprentissage ou le test. Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données. Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent. Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).

Appliquez un pipeline `mlContext.Transforms.Text.FeaturizeText` pour convertir la colonne `SentimentText` en un vecteur numérique appelé `Features` utilisé par l’algorithme Machine Learning. Il s’agit d’un appel de wrapper qui retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera un pipeline. Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`. Ajoutez le contenu suivant comme prochaine ligne de code :

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#FeaturizeText "Featurize the text")]

>[!WARNING]
> ML.NET version 0.10 a changé l’ordre des paramètres de transformation. Cela ne provoque aucune jusqu’à ce que vous exécutiez l’application et génériez le modèle. Utilisez les noms de paramètre pour les transformations comme illustré dans l’extrait de code précédent.

Il s’agit de l’étape de prétraitement/fonctionnalisation. L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.

## <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Pour ajouter le formateur, appelez la méthode de wrapper `mlContext.BinaryClassification.Trainers.FastTree` qui retourne un objet <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer>. Il s’agit d’un apprenant d’arbre de décision que vous utiliserez dans ce pipeline. L’objet `FastTreeBinaryClassificationTrainer` est ajouté à `pipeline` et accepte les caractéristiques `SentimentText` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir de l’historique des données.

Ajoutez le code suivant à la méthode `BuildAndTrainModel` :

[!code-csharp[FastTreeBinaryClassificationTrainer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddTrainer "Add a FastTreeBinaryClassificationTrainer")]

## <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé. Une fois l’estimateur défini, effectuez l’apprentissage de votre modèle avec la méthode <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées. Cette méthode retourne un modèle à utiliser pour les prédictions. `pipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis. L’expérience n’est pas exécutée tant que la méthode `.Fit()` s’exécute.

Ajoutez le code suivant à la méthode `BuildAndTrainModel` :

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#TrainModel "Train the model")]

### <a name="save-and-return-the-model-trained-to-use-for-evaluation"></a>Enregistrer et revenir au modèle formé à utiliser pour l’évaluation

À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Retournez le modèle à la fin de la méthode `BuildAndTrainModel`.

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#ReturnModel "Return the model")]

## <a name="evaluate-the-model"></a>Évaluer le modèle

Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation. Dans la méthode `Evaluate`, le modèle créé dans `BuildAndTrainModel` est passé pour évaluation. Créez la méthode `Evaluate` juste après `BuildAndTrainModel`, comme dans le code suivant :

```csharp
public static void Evaluate(MLContext mlContext, ITransformer model, IDataView splitTestSet)
{

}
```

La méthode `Evaluate` exécute les tâches suivantes :

* Charge le jeu de données de test.
* Crée l’évaluateur de classification binaire.
* Évalue le modèle et crée des métriques.
* Affiche les métriques.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Train`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallEvaluate "Call the Evaluate method")]

Utilisons maintenant le paramètre `model` Machine Learning (transformateur) et le paramètre `splitTestSet` pour donner en entrée les caractéristiques et retourner des prédictions. Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :

[!code-csharp[PredictWithTransformer](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#TransformData "Predict using the Transformer")]

La méthode `mlContext.BinaryClassification.Evaluate` calcule les métriques de qualité pour `PredictionModel` à l’aide du jeu de données spécifié. Elle retourne un objet <xref:Microsoft.ML.Data.CalibratedBinaryClassificationMetrics> contenant les mesures globales calculées par les évaluateurs de classification binaire. Pour afficher ces informations afin d’évaluer la qualité du modèle, vous devez d’abord obtenir les métriques. Ajoutez le code suivant comme première ligne de la méthode `Evaluate` :

[!code-csharp[ComputeMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Evaluate "Compute Metrics")]

### <a name="displaying-the-metrics-for-model-validation"></a>Affichage des métriques pour la validation du modèle

Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DisplayMetrics "Display selected metrics")]

Pour enregistrer votre modèle dans un fichier .zip avant de le retourner, ajoutez ce code pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `Evaluate` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallSaveModel "Save the model")]

## <a name="save-the-model-as-azip-file"></a>Enregistrer le modèle en tant que fichier .zip

Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

La méthode `SaveModelAsFile` exécute les tâches suivantes :

* Enregistre le modèle sous la forme d’un fichier .zip.

Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications. Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>. Pour l’enregistrer en tant que fichier .zip, nous allons créer le `FileStream` immédiatement avant d’appeler la méthode `SaveTo`. Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :

[!code-csharp[SaveToMethod](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#SaveModel "Add the SaveTo Method")]

## <a name="deploy-and-predict-with-a-loaded-model"></a>Déployer et prédire avec un modèle chargé

Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="predict-the-test-data-outcome-with-the-saved-model"></a>Prédire le résultat des données de test avec le modèle enregistré

Créez la méthode `UseModelWithSingleItem` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void UseModelWithSingleItem(MLContext mlContext, ITransformer model)
{

}
```

La méthode `UseModelWithSingleItem` exécute les tâches suivantes :

* Crée un commentaire unique de données de test.
* Prédit les sentiments en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :

[!code-csharp[CallUseModelWithSingleItem](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallUseModelWithSingleItem "Call the UseModelWithSingleItem method")]

Bien que le `model` est un `transformer` qui fonctionne sur plusieurs lignes de données, un scénario de production très courant est nécessaire pour les prédictions sur des exemples individuels. Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`. Nous allons ajouter le code suivant pour créer le `PredictionEngine` comme première ligne dans la méthode `Predict` :

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreatePredictionEngine1 "Create the PredictionEngine")]
  
Ajoutez un commentaire pour tester la prédiction du modèle formé dans la méthode `Predict` en créant une instance de `SentimentData` :

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateTestIssue1 "Create test data for single prediction")]

 Vous pouvez l’utiliser pour prédire le sentiment positif ou négatif d’une seule instance de données de commentaires. Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Predict "Create a prediction of sentiment")]

### <a name="use-the-model-prediction"></a>Utiliser le modèle à des fins de prédiction

Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence. Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles. Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#OutputPrediction "Display prediction output")]

## <a name="deploy-and-predict-with-a-loaded-model"></a>Déployer et prédire avec un modèle chargé

Créez la méthode `UseLoadedModelWithBatchItems` juste avant la méthode `SaveModelAsFile`, en utilisant le code suivant :

```csharp
public static void UseLoadedModelWithBatchItems(MLContext mlContext)
{

}
```

La méthode `UseLoadedModelWithBatchItems` exécute les tâches suivantes :

* Crée les données de test par lots.
* Prédit les sentiments en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `UseModelWithSingleItem`, en utilisant le code suivant :

[!code-csharp[CallPredictModelLoaded](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CallUseLoadedModelWithBatchItems "Call the CallUseLoadedModelWithBatchItems method")]

Ajoutez des commentaires pour tester les prédictions du modèle formé dans la méthode `UseLoadedModelWithBatchItems` :

[!code-csharp[PredictionData](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#CreateTestIssues "Create test data for predictions")]

Charger le modèle

[!code-csharp[LoadTheModel](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#LoadModel "Load the model")]

Maintenant que vous disposez d’un modèle, vous pouvez l’utiliser pour prédire le sentiment positif ou négatif des données de commentaires à l’aide de la méthode <xref:Microsoft.ML.ITransformer.Transform%2A>. Pour obtenir une prédiction, utilisez `Predict` sur les nouvelles données. Notez que les données d’entrée constituent une chaîne et que le modèle inclut la fonctionnalisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique. Ajoutez le code suivant à la méthode `UseLoadedModelWithBatchItems` pour les prédictions :

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#Prediction "Create predictions of sentiments")]

### <a name="use-the-loaded-model-for-prediction"></a>Utiliser le modèle chargé à des fins de prédiction

Affichez `SentimentText` et la prédiction de sentiment correspondante afin de partager les résultats et de les modifier en conséquence. Cette étape, appelée opérationnalisation, utilise les données retournées dans le cadre des stratégies opérationnelles. Créez un en-tête des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputHeaders](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#AddInfoMessage "Display prediction outputs")]

Avant d’afficher les résultats prédits, combinez le sentiment et la prédiction pour afficher les commentaires d’origine avec leur sentiment prédit. Pour cela, le code suivant utilise la méthode <xref:System.Linq.Enumerable.Zip%2A> ; alors ajoutez le code suivant :

[!code-csharp[BuildTuples](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#BuildSentimentPredictionPairs "Build the pairs of sentiment data and predictions")]

Maintenant que vous avez combiné `SentimentText` et `Sentiment` dans une classe, vous pouvez afficher les résultats à l’aide de la méthode <xref:System.Console.WriteLine?displayProperty=nameWithType> :

[!code-csharp[DisplayPredictions](../../../samples/machine-learning/tutorials/SentimentAnalysis/Program.cs#DisplayResults "Display the predictions")]

Comme les noms des éléments de tuple inférés constituent une nouvelle fonctionnalité dans C# 7.1 et que la version du langage par défaut du projet est C# 7.0, vous devez remplacer la version du langage par C# 7.1 ou version ultérieure.
Pour cela, cliquez avec le bouton droit sur le nœud de projet dans l’**Explorateur de solutions**, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez **C# 7.1** (ou version ultérieure). Sélectionnez le bouton **OK**.

## <a name="results"></a>Résultats

Vos résultats doivent être similaires à ce qui suit. Lors du traitement, le pipeline affiche des messages. Vous pouvez voir des avertissements ou des messages de traitement. Ils ont été supprimés des résultats ci-dessous par souci de clarté.

```console
Model quality metrics evaluation
--------------------------------
Accuracy: 79.14%
Auc: 86.27%
F1Score: 80.60%

=============== End of model evaluation ===============
The model is saved to C:\Tutorials\SentimentAnalysis\bin\Debug\netcoreapp2.1\Data\Model.zip

=============== Prediction Test of model with a single sample and test dataset ===============

Sentiment: This was a very bad steak | Prediction: Negative | Probability: 0.4641322
=============== End of Predictions ===============


=============== Prediction Test of loaded model with a multiple samples ===============

Sentiment: This was a horrible meal | Prediction: Negative | Probability: 0.1391833
Sentiment: I love this spaghetti. | Prediction: Positive | Probability: 0.9819039
=============== End of predictions ===============

=============== End of process ===============
Press any key to continue . . .

```

Félicitations ! Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction des sentiments de messages. 

La création de modèles efficaces est un processus itératif. Celui-ci présente une qualité initiale médiocre, car le tutoriel utilise de petits jeux de données pour permettre un apprentissage rapide du modèle. Si vous n’êtes pas satisfait de la qualité du modèle, vous pouvez essayer de l’améliorer en fournissant de plus gros jeux de données d’apprentissage ou en choisissant d’autres algorithmes d’apprentissage avec différents hyperparamètres pour chacun.

Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/SentimentAnalysis).

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à :
> [!div class="checklist"]
> * Comprendre le problème
> * Sélectionner l’algorithme de machine learning approprié
> * Préparer vos données
> * Transformer les données
> * Effectuer l’apprentissage du modèle
> * Évaluer le modèle
> * Prédire avec le modèle entraîné
> * Déployer et prédire avec un modèle chargé

Passer au tutoriel suivant pour en savoir plus
> [!div class="nextstepaction"]
> [Classification des problèmes](github-issue-classification.md)
