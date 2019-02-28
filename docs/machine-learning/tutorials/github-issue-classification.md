---
title: Utiliser ML.NET dans un scénario de classification multiclasse de problèmes GitHub
description: Découvrez comment utiliser ML.NET dans un scénario de classification multiclasse pour classer des problèmes GitHub et les affecter à une zone donnée.
ms.date: 02/20/2019
ms.topic: tutorial
ms.custom: mvc
ms.openlocfilehash: fdb6621078854d80f0af484ae1b92526f0f9cbb8
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584289"
---
# <a name="tutorial-use-mlnet-in-a-multiclass-classification-scenario-to-classify-github-issues"></a>Tutoriel : Utiliser ML.NET dans un scénario de classification multiclasse pour classifier les problèmes GitHub

Ce tutoriel montre comment utiliser ML.NET pour créer dans Visual Studio 2017 une application console .NET Core en C# faisant office de classifieur de problèmes GitHub.

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

> [!NOTE]
> Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées. Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

## <a name="github-issue-sample-overview"></a>Vue d’ensemble de l’exemple traitant des problèmes GitHub

L’exemple est une application console qui utilise ML.NET pour entraîner un modèle qui classe et prédit l’étiquette Area d’un problème GitHub. Il évalue également le modèle avec un second jeu de données pour l’analyse de la qualité. Les jeux de données de problèmes proviennent du dépôt GitHub dotnet/corefx.

Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification).

## <a name="prerequisites"></a>Prérequis

* [Visual Studio 2017 15.6 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), avec la charge de travail « Développement multiplateforme .Net Core » installée.

* [Fichier de problèmes GitHub séparés par des tabulations (issues_train.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv).
* [Fichier de test des problèmes GitHub séparés par des tabulations (issues_test.tsv)](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv).

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

Vous devez d’abord comprendre le problème afin de le décomposer en plusieurs parties pouvant prendre en charge la création et l’apprentissage du modèle. La décomposition de la problématique vous permet de prédire et d’évaluer les résultats.

Dans ce tutoriel, vous devez comprendre à quelle zone les problèmes GitHub entrants appartiennent afin de les étiqueter correctement pour la définition des priorités et la planification.

Vous pouvez scinder le problème en différentes parties, à savoir :

* Texte de titre du problème
* Texte de description du problème
* Valeur de zone pour les données d’entraînement du modèle
* Valeur de zone prédite que vous pouvez évaluer et utiliser opérationnellement

Vous devez ensuite **déterminer** la zone, ce qui vous aide à sélectionner la tâche d’apprentissage automatique.

## <a name="select-the-appropriate-machine-learning-algorithm"></a>Sélectionner l’algorithme de machine learning approprié

Pour ce problème, vous disposez des éléments suivants :

Données d’entraînement :

Les problèmes GitHub peuvent être étiquetés dans plusieurs zones (**Area**), comme dans les exemples suivants :

* area-System.Numerics
* area-System.Xml
* area-Infrastructure
* area-System.Linq
* area-System.IO

Prédisez la zone (**Area**) d’un nouveau problème GitHub, comme dans les exemples suivants :

* Contract.Assert et Debug.Assert
* Configurer les champs en lecture seule dans System.Xml

L’algorithme de machine learning de classification est idéal pour ce scénario.

### <a name="about-the-classification-learning-algorithm"></a>À propos de l’algorithme de machine learning de classification

La classification est un algorithme de machine learning qui utilise des données pour **déterminer** la catégorie, le type ou la classe d’un élément ou d’une ligne de données. Par exemple, vous pouvez utiliser la classification pour :

* Identifier un sentiment positif ou négatif.
* Classer un e-mail comme spam, indésirable ou autorisé.
* Déterminer si l’échantillon de laboratoire d’un patient est cancéreux.
* Classer des clients selon leur tendance à répondre à une campagne commerciale.

Les cas d’usage de l’algorithme de machine learning de classification sont souvent l’un des types suivants :

* Binaire : A ou B.
* Multiclasse : plusieurs catégories pouvant être prédites à l’aide d’un modèle unique.

Pour ce type de problème, utilisez un algorithme de machine learning de classification multiclasse, dans la mesure où votre prédiction de catégorie de problème peut appartenir à une catégorie parmi plusieurs possibles (multiclasse) plutôt qu’à une catégorie parmi deux possibles (binaire).

## <a name="create-a-console-application"></a>Créer une application console

### <a name="create-a-project"></a>Créer un projet

1. Ouvrez Visual Studio 2017. Sélectionnez **Fichier** > **Nouveau** > **Projet** dans la barre de menus. Dans la boîte de dialogue **Nouveau projet**, sélectionnez le nœud **Visual C#** suivi du nœud **.NET Core**. Ensuite, sélectionnez le modèle de projet **Application console (.NET Core)**. Dans la zone de texte **Nom**, tapez « GitHubIssueClassification », puis cliquez sur le bouton **OK**.

2. Créez un répertoire nommé *Données* dans votre projet pour enregistrer vos fichiers de jeu de données :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Données » et appuyez sur Entrée.

3. Créez un répertoire nommé *Models* dans votre projet pour enregistrer votre modèle :

    Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Ajouter** > **Nouveau dossier**. Tapez « Models » et appuyez sur Entrée.

4. Installez le **package NuGet Microsoft.ML** :

    Dans l'Explorateur de solutions, cliquez avec le bouton droit sur votre projet, puis sélectionnez **Gérer les packages NuGet**. Choisissez « nuget.org » comme Source du package, sélectionnez l’onglet Parcourir, recherchez **Microsoft.ML**, sélectionnez ce package dans la liste, puis cliquez sur le bouton **Installer**. Cliquez sur le bouton **OK** dans la boîte de dialogue **Aperçu des modifications**, puis sur le bouton **J’accepte** dans la boîte de dialogue **Acceptation de la licence** si vous acceptez les termes du contrat de licence pour les packages répertoriés.

### <a name="prepare-your-data"></a>Préparer vos données

1. Téléchargez les jeux de données [issues_train.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_train.tsv) et [issues_test.tsv](https://raw.githubusercontent.com/dotnet/samples/master/machine-learning/tutorials/GitHubIssueClassification/Data/issues_test.tsv), puis enregistrez-les dans le dossier *Données* créé précédemment. Le premier jeu de données effectue l’apprentissage automatique du modèle, et le second peut servir à évaluer la précision de votre modèle.

2. Dans l'Explorateur de solutions, cliquez avec le bouton droit sur chacun des fichiers \*.tsv, puis sélectionnez **Propriétés**. Sous **Avancé**, définissez la valeur **Copier dans le répertoire de sortie** sur **Copier si plus récent**.

### <a name="create-classes-and-define-paths"></a>Créer des classes et définir des chemins

Ajoutez les instructions `using` supplémentaires suivantes en haut du fichier *Program.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddUsings)]

Créez trois champs globaux pour accueillir les chemins des fichiers récemment téléchargés, puis des variables globales pour `MLContext`, `DataView`, `PredictionEngine` et `TextLoader` :

* `_trainDataPath` contient le chemin d’accès au jeu de données utilisé pour l’apprentissage du modèle.
* `_testDataPath` contient le chemin d’accès au jeu de données utilisé pour évaluer le modèle.
* `_modelPath` contient le chemin d’accès où le modèle formé est enregistré.
* `_mlContext` est le <xref:Microsoft.ML.MLContext> qui fournit le contexte de traitement.
* `_trainingDataView` est le <xref:Microsoft.Data.DataView.IDataView> utilisé pour traiter le jeu de données d’entraînement.
* `_predEngine` est le <xref:Microsoft.ML.PredictionEngine%602> utilisé pour des prédictions uniques.
* `_reader` est l’élément <xref:Microsoft.ML.Data.TextLoader> utilisé pour charger et transformer les jeux de données.

Ajoutez le code suivant à la ligne juste au-dessus de la méthode `Main` pour spécifier ces chemins et les autres variables :

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DeclareGlobalVariables)]

Créez des classes pour vos données d’entrée et vos prévisions. Ajoutez une nouvelle classe à votre projet :

1. Dans l **’Explorateur de solutions**, cliquez avec le bouton de droite sur le projet, puis sélectionnez **Ajouter** > **Nouvel élément**.

1. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Classe**, puis remplacez la valeur du champ **Nom** par *GitHubIssueData.cs*. Ensuite, sélectionnez le bouton **Ajouter**.

    Le fichier *GitHubIssueData.cs* s’ouvre dans l’éditeur de code. Ajoutez l’instruction `using` suivante en haut de *GitHubIssueData.cs* :

[!code-csharp[AddUsings](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#AddUsings)]

Supprimez la définition de classe existante et ajoutez le code suivant, lequel contient deux classes (`GitHubIssue` et `IssuePrediction`), au fichier *GitHubIssueData.cs* :

[!code-csharp[DeclareGlobalVariables](../../../samples/machine-learning/tutorials/GitHubIssueClassification/GitHubIssueData.cs#DeclareTypes)]

`GitHubIssue`, la classe de jeu de données d’entrée, comprend les champs <xref:System.String> suivants :

* `ID` contient une valeur pour l’ID du problème GitHub.
* `Area` contient une valeur pour l’étiquette `Area`.
* `Title` contient le titre du problème GitHub.
* `Description` contient la description du problème GitHub.

`IssuePrediction` représente la classe utilisée pour la prédiction, une fois le modèle formé. Il comporte une valeur `string` unique (`Area`) et un attribut `ColumnName` `PredictedLabel`. L’attribut `Label` sert à créer et à effectuer l’apprentissage du modèle et il est utilisé avec un second jeu de données pour évaluer le modèle. L’attribut `PredictedLabel` est utilisé pendant la prédiction et l’évaluation. L’évaluation utilise une entrée avec les données d’apprentissage, les valeurs prédites et le modèle.

Lors de la création d’un modèle avec ML.NET, vous commencez par créer un <xref:Microsoft.ML.MLContext>. D’un point de vue conceptuel, `MLContext` est comparable à `DbContext` dans Entity Framework. L’environnement fournit un contexte pour votre tâche d’apprentissage automatique et qui peut être utilisé pour le suivi des exceptions et la journalisation.

### <a name="initialize-variables-in-main"></a>Initialiser les variables dans Principal

Initialisez la variable globale `_mlContext` à l’aide d’une nouvelle instance de `MLContext` avec une valeur de départ aléatoire (`seed: 0`) pour obtenir des résultats reproductibles/déterministes dans différents entraînements.  Remplacez la ligne `Console.WriteLine("Hello World!")` par le code suivant dans la méthode `Main` :

[!code-csharp[CreateMLContext](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateMLContext)]

## <a name="load-the-data"></a>Charger les données

Ensuite, initialisez la variable globale `_trainingDataView` <xref:Microsoft.Data.DataView.IDataView> et chargez les données avec le paramètre `_trainDataPath`.

 En tant qu’entrée et sortie de [`Transforms`](../basic-concepts-model-training-in-mldotnet.md#transformer), `DataView` est le type de pipeline de données fondamental, comparable à `IEnumerable` pour `LINQ`.

Dans ML.NET, les données sont semblables à un `SQL view`. Elles sont évaluées tardivement, schématisées et hétérogènes. L’objet est la première partie du pipeline, et charge les données. Pour ce tutoriel, il charge un jeu de données avec les titres et les descriptions des problèmes ainsi que l’étiquette GitHub de la zone correspondante. `DataView` est utilisé pour créer et entraîner le modèle.

Étant donné que le type de modèle de données `GitHubIssue` créé précédemment correspond au schéma du jeu de données, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données en une seule ligne de code.

La première partie de la ligne (`CreateTextLoader<GitHubIssue>(hasHeader: true)`) crée un <xref:Microsoft.ML.Data.TextLoader> en déduisant le schéma de jeu de données du type de modèle de données `GitHubIssue` et en utilisant l’en-tête du jeu de données.

Vous avez défini précédemment le schéma de données quand vous avez créé la classe `GitHubIssue`. Pour votre schéma :

* La première colonne `ID` est l’ID du problème GitHub.
* La deuxième colonne `Area` est la prédiction pour l’entraînement.
* La troisième colonne `Title` (titre du problème GitHub) est la première [caractéristique](../resources/glossary.md##feature) utilisée pour prédire `Area`.
* La quatrième colonne `Description` est la deuxième caractéristique utilisée pour prédire `Area`.

La deuxième partie de la ligne (`.Read(_trainDataPath)`) utilise la méthode <xref:Microsoft.ML.Data.TextLoader.Read%2A> pour charger le fichier texte d’entraînement avec `_trainDataPath` dans la variable globale `IDataView` (`_trainingDataView`).  

Pour initialiser et charger la variable globale `_trainingDataView` afin de l’utiliser pour le pipeline, ajoutez le code suivant après l’initialisation de `mlContext` :

[!code-csharp[LoadTrainData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTrainData)]


Ajoutez le code suivant comme prochaine ligne dans la méthode `Main` :

[!code-csharp[CallProcessData](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallProcessData)]

La méthode `ProcessData` exécute les tâches suivantes :

* Extrait et transforme les données.
* Retourne le pipeline de traitement.

Créez la méthode `ProcessData` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
public static EstimatorChain<ITransformer> ProcessData()
{

}
```

## <a name="extract-features-and-transform-the-data"></a>Extraire des caractéristiques et transformer les données

Le prétraitement et le nettoyage des données constituent des tâches importantes qui se produisent avant qu’un jeu de données puisse être utilisé efficacement pour l’apprentissage. Les données brutes sont souvent imprécises, peu fiables, et manquent parfois de certaines valeurs. L’utilisation de données sans effectuer ces tâches de modélisation peut produire des résultats trompeurs.

Les pipelines de transformation ML.NET composent un ensemble `transforms` personnalisé qui s’applique à vos données avant l’entraînement ou le test. Les transformations servent principalement à [fonctionnaliser](../resources/glossary.md#feature-engineering) les données. Comprennent les algorithmes Machine Learning [caractérisées](../resources/glossary.md#feature) données, l’étape suivante consiste donc à transformer nos données textuelles dans un format que nos algorithmes ML reconnaissent. Ce format est un [vecteur numérique](../resources/glossary.md#numerical-feature-vector).

Dans les prochaines étapes, nous référençons les colonnes au moyen des noms définis dans la classe `GitHubIssue`.

Quand le modèle fait l’objet d’un apprentissage et d’une évaluation, les valeurs de la colonne **Label** sont considérées par défaut comme des valeurs correctes à prédire. Comme nous voulons prédire l’étiquette GitHub Area pour un `GitHubIssue`, copiez la colonne `Area` dans la colonne **Label**. Pour ce faire, utilisez `MLContext.Transforms.Conversion.MapValueToKey`, qui est un wrapper pour la classe de transformation <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey%2A>.  `MapValueToKey` retourne un <xref:Microsoft.ML.Data.EstimatorChain%601> qui sera en fait un pipeline. Nommez ce `pipeline` car vous allez ajouter le formateur à `EstimatorChain`. Ajoutez la ligne de code suivante :

[!code-csharp[MapValueToKey](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#MapValueToKey)]

 La caractérisation, qui affecte différentes valeurs de clé numériques aux différentes valeurs de chaque colonne, est utilisée par l’algorithme d’apprentissage automatique. Ensuite, appelez `mlContext.Transforms.Text.FeaturizeText` qui caractérise les colonnes de texte (`Title` et `Description`) en vecteur numérique pour chaque `TitleFeaturized` et `DescriptionFeaturized` appelé. Utilisez le code suivant pour ajouter la caractérisation des deux colonnes au pipeline :

[!code-csharp[FeaturizeText](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#FeaturizeText)]

>[!WARNING]
> ML.NET version 0.10 a changé l’ordre des paramètres de transformation. Cela n’entraîne pas d’erreur tant que vous ne compilez pas. Utilisez les noms de paramètre pour les transformations comme illustré dans l’extrait de code précédent.

La dernière étape de préparation des données regroupe toutes les colonnes de fonctionnalités dans la colonne **Fonctionnalités** à l’aide de la classe de transformation `Concatenate`. Par défaut, un algorithme d’apprentissage traite uniquement les caractéristiques issues de la colonne **Features**. Utilisez le code suivant pour ajouter cette transformation au pipeline :

[!code-csharp[Concatenate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Concatenate)]

 Ajoutez ensuite un <xref:Microsoft.ML.Data.EstimatorChain`1.AppendCacheCheckpoint%2A> pour mettre en cache le DataView. Ainsi, quand vous itérerez plusieurs fois sur les données, l’utilisation du cache vous fera peut-être gagner en performances, à l’instar du code suivant :

[!code-csharp[AppendCache](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AppendCache)]

> [!WARNING]
> Utilisez AppendCacheCheckpoint pour les jeux de données petits/moyens afin de réduire le temps d’apprentissage. Ne l’utilisez PAS (supprimez .AppendCacheCheckpoint()) lors du traitement de jeux de données très volumineux.

Retournez le pipeline à la fin de la méthode `ProcessData`.

[!code-csharp[ReturnPipeline](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnPipeline)]

Cette étape gère le prétraitement/la caractérisation. L’utilisation des composants supplémentaires disponibles dans ML.NET peut améliorer les résultats de votre modèle.

## <a name="build-and-train-the-model"></a>Générer et entraîner le modèle

Ajoutez l’appel suivant à la méthode `BuildAndTrainModel` comme prochaine ligne de code dans la méthode `Main` :

[!code-csharp[CallBuildAndTrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallBuildAndTrainModel)]

La méthode `BuildAndTrainModel` exécute les tâches suivantes :

* Crée la classe d’algorithme d’entraînement.
* Effectue l’apprentissage du modèle.
* Prédit la zone en fonction des données d’entraînement.
* Enregistre le modèle dans un fichier `.zip`.
* Retourne le modèle.

Créez la méthode `BuildAndTrainModel` juste après la méthode `Main`, en utilisant le code suivant :

```csharp
public static EstimatorChain<KeyToValueMappingTransformer> BuildAndTrainModel(IDataView trainingDataView, EstimatorChain<ITransformer> pipeline)
{

}
```

Notez que deux paramètres sont passés dans la méthode BuildAndTrainModel : `IDataView` pour le jeu de données d’entraînement (`trainingDataView`) et <xref:Microsoft.ML.Data.EstimatorChain%601> pour le pipeline de traitement créé dans ProcessData (`pipeline`).

 Ajoutez le code suivant comme première ligne de la méthode `BuildAndTrainModel` :

### <a name="choose-a-learning-algorithm"></a>Choisir un algorithme d’apprentissage

Pour ajouter l’algorithme d’apprentissage, appelez la méthode de wrapper `mlContext.MulticlassClassification.Trainers.StochasticDualCoordinateAscent` qui retourne un objet <xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer>.  `SdcaMultiClassTrainer` est ajouté à `pipeline` et accepte les caractéristiques `Title` et `Description` (`Features`) et les paramètres d’entrée `Label` pour apprendre à partir des données d’historique. Vous devez également mapper l’étiquette à la valeur pour revenir à son état lisible d’origine. Effectuez ces deux actions avec le code suivant :

[!code-csharp[AddTrainer](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTrainer)]

### <a name="train-the-model"></a>Effectuer l’apprentissage du modèle

Vous effectuez l’apprentissage du modèle, <xref:Microsoft.ML.Data.TransformerChain%601>, selon le jeu de données qui a été chargé et transformé. Une fois l’estimation définie, vous formez votre modèle à l’aide du <xref:Microsoft.ML.Data.EstimatorChain%601.Fit%2A> tout en fournissant les données d’apprentissage déjà chargées. Cette méthode retourne un modèle à utiliser pour les prédictions. `trainingPipeline.Fit()` forme le pipeline et renvoie un `Transformer` selon l’élément `DataView` transmis. L’expérience n’est pas exécutée tant que la méthode `.Fit()` s’exécute.

Ajoutez le code suivant à la méthode `BuildAndTrainModel` :

[!code-csharp[TrainModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#TrainModel)]

Bien que `model` soit un `transformer` qui opère sur un grand nombre de lignes de données, le besoin en prédictions sur des exemples individuels est un scénario de production courant. Le <xref:Microsoft.ML.PredictionEngine%602> est un wrapper retourné par la méthode `CreatePredictionEngine`. Ajoutons le code suivant pour créer le `PredictionEngine` comme ligne suivante dans la méthode `BuildAndTrainModel` :

[!code-csharp[CreatePredictionEngine1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine1)]

### <a name="predict-with-the-trained-model"></a>Prédire avec le modèle entraîné

Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :

[!code-csharp[CreateTestIssue1](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreateTestIssue1)]

Vous pouvez l’utiliser pour prédire l’étiquette `Area` d’une instance unique des données de problème. Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données. Les données d’entrée représentent une chaîne et le modèle inclut la caractérisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique.

[!code-csharp[Predict](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Predict)]

### <a name="using-the-model-prediction-results"></a>Utilisation des résultats du modèle : prédiction

Affichez `GitHubIssue` et la prédiction d’étiquette `Area` correspondante pour partager les résultats et prendre les mesures nécessaires.  Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[OutputPrediction](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#OutputPrediction)]

### <a name="return-the-model-trained-to-use-for-evaluation"></a>Retourner le modèle entraîné à utiliser pour l’évaluation

Retournez le modèle à la fin de la méthode `BuildAndTrainModel`.

[!code-csharp[ReturnModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#ReturnModel)]

## <a name="evaluate-the-model"></a>Évaluer le modèle

Maintenant que vous avez créé et effectué l’apprentissage du modèle, vous devez l’évaluer avec un jeu de données différent à des fins d’assurance qualité et de validation. Dans la méthode `Evaluate`, le modèle créé dans `BuildAndTrainModel` est passé pour évaluation. Créez la méthode `Evaluate` juste après `BuildAndTrainModel`, comme dans le code suivant :

```csharp
public static void Evaluate()
{

}
```

La méthode `Evaluate` exécute les tâches suivantes :

* Charge le jeu de données de test.
* Crée l’évaluateur multiclasse.
* Évalue le modèle et crée des métriques.
* Affiche les métriques.

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `BuildAndTrainModel`, en utilisant le code suivant :

[!code-csharp[CallEvaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallEvaluate)]

Comme vous l’avez fait précédemment avec le jeu de données d’entraînement, vous pouvez combiner l’initialisation, le mappage et le chargement du jeu de données de test en une seule ligne de code. Vous pouvez évaluer le modèle à l’aide de ce jeu de données afin de contrôler la qualité. Ajoutez le code suivant à la méthode `Evaluate` :

[!code-csharp[LoadTestDataset](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadTestDataset)]

La méthode `MulticlassClassificationContext.Evaluate` est un wrapper pour la méthode <xref:Microsoft.ML.MulticlassClassificationCatalog.Evaluate%2A> qui calcule les métriques de qualité du modèle à l’aide du jeu de données spécifié. Elle retourne un objet <xref:Microsoft.ML.Data.MultiClassClassifierMetrics> contenant les métriques globales calculées par les évaluateurs de classification multiclasse.
Pour afficher les métriques permettant de déterminer la qualité du modèle, vous devez d’abord les obtenir.
Notez l’utilisation de la méthode `Transform` de la variable globale `_trainedModel` d’apprentissage automatique (un transformateur) pour entrer les caractéristiques et retourner les prédictions. Ajoutez comme nouvelle ligne le code suivant à la méthode `Evaluate` :

[!code-csharp[Evaluate](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#Evaluate)]

Les métriques suivantes sont évaluées pour la classification multiclasse :

* Micro-précision : chaque paire exemple-classe contribue de manière égale à la métrique de précision.  Vous voulez que la micro-précision soit aussi proche de 1 que possible.

* Macro-précision : chaque classe contribue de manière égale à la métrique de précision. Les classes minoritaires sont aussi importantes que les classes plus grandes. Vous voulez que la macro-précision soit aussi proche de 1 que possible.

* Perte logarithmique : consultez [Perte logarithmique](../resources/glossary.md#log-loss). Vous voulez que la perte logarithmique soit aussi proche de zéro que possible.

* Réduction de la perte logarithmique : comprise entre [-inf, 100], où 100 correspond à des prédictions parfaites et 0 à des prédictions moyennes. Vous voulez que la réduction de la perte logarithmique soit aussi proche de zéro que possible.

### <a name="displaying-the-metrics-for-model-validation"></a>Affichage des métriques pour la validation du modèle

Utilisez le code suivant pour afficher les métriques, partager les résultats et agir dessus :

[!code-csharp[DisplayMetrics](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayMetrics)]

### <a name="save-the-trained-and-evaluated-model"></a>Enregistrer le modèle entraîné et évalué

À ce stade, vous disposez d’un modèle de type <xref:Microsoft.ML.Data.TransformerChain%601> qui peut être intégré à n’importe laquelle de vos applications .NET existantes ou nouvelles. Pour enregistrer votre modèle entraîné dans un fichier .zip, ajoutez le code suivant pour appeler la méthode `SaveModelAsFile` comme ligne suivante dans `BuildAndTrainModel` :

[!code-csharp[CallSaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallSaveModel)]

## <a name="save-the-model-as-a-zip-file"></a>Enregistrer le modèle en tant que fichier .zip

Créez la méthode `SaveModelAsFile` juste après la méthode `Evaluate`, en utilisant le code suivant :

```csharp
private static void SaveModelAsFile(MLContext mlContext, ITransformer model)
{

}
```

La méthode `SaveModelAsFile` exécute les tâches suivantes :

* Enregistre le modèle sous la forme d’un fichier .zip.

Créez ensuite une méthode pour enregistrer le modèle afin qu’il puisse être réutilisé et consommé dans d’autres applications. Le `ITransformer` comporte une méthode <xref:Microsoft.ML.Data.TransformerChain%601.SaveTo(Microsoft.ML.IHostEnvironment,System.IO.Stream)> qui accepte le champ global `_modelPath` et un <xref:System.IO.Stream>. Pour enregistrer le modèle sous forme de fichier .zip, vous devez créer `FileStream` juste avant d’appeler la méthode `SaveTo`. Ajoutez comme nouvelle ligne le code suivant à la méthode `SaveModelAsFile` :

[!code-csharp[SaveModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#SaveModel)]

Vous pouvez également afficher l’endroit où le fichier a été écrit en créant un message de console avec l’élément `_modelPath`, et en utilisant le code suivant :

```csharp
Console.WriteLine("The model is saved to {0}", _modelPath);
```

## <a name="deploy-and-predict-with-a-loaded-model"></a>Déployer et prédire avec un modèle chargé

Ajoutez un appel à la nouvelle méthode à partir de la méthode `Main`, juste sous l’appel à la méthode `Evaluate`, en utilisant le code suivant :

[!code-csharp[CallPredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CallPredictIssue)]

Créez la méthode `PredictIssue`, juste après la méthode `Evaluate` (et juste avant la méthode `SaveModelAsFile`), en utilisant le code suivant :

```csharp
private static void PredictIssue()
{

}
```

La méthode `PredictIssue` exécute les tâches suivantes :

* Crée un problème unique de données de test.
* Prédit Area en fonction des données de test.
* Combine les données de test et les prédictions pour générer des rapports.
* Affiche les résultats prédits.

Tout d’abord, chargez le modèle que vous avez enregistré précédemment avec le code suivant :

[!code-csharp[LoadModel](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#LoadModel)]

Ajoutez un problème GitHub pour tester la prédiction du modèle entraîné dans la méthode `Predict` en créant une instance de `GitHubIssue` :

[!code-csharp[AddTestIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#AddTestIssue)]

[!code-csharp[CreatePredictionEngine](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#CreatePredictionEngine)]
  
Maintenant que vous avez un modèle, vous pouvez l’utiliser pour prédire l’étiquette GitHub Area d’une instance unique des données de problème GitHub. Pour obtenir une prédiction, utilisez <xref:Microsoft.ML.PredictionEngine%602.Predict%2A> sur les données. Les données d’entrée représentent une chaîne et le modèle inclut la caractérisation. Votre pipeline est synchronisé durant l’apprentissage et la prédiction. Vous n’aviez pas à écrire le code de prétraitement/fonctionnalisation spécifiquement pour les prédictions, et la même API gère le traitement par lots et les prédictions à usage unique. Ajoutez le code suivant à la méthode `PredictIssue` pour les prédictions :

[!code-csharp[PredictIssue](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#PredictIssue)]

### <a name="using-the-loaded-model-for-prediction"></a>Utilisation du modèle chargé pour la prédiction

Affichez `Area` pour catégoriser le problème et agir en conséquence. Créez une vue des résultats à l’aide du code <xref:System.Console.WriteLine?displayProperty=nameWithType> suivant :

[!code-csharp[DisplayResults](../../../samples/machine-learning/tutorials/GitHubIssueClassification/Program.cs#DisplayResults)]

## <a name="results"></a>Résultats

Vos résultats doivent être similaires à ce qui suit. Lors du traitement, le pipeline affiche des messages. Vous pouvez voir des avertissements ou des messages de traitement. Ces messages ont été supprimés des résultats suivants par souci de clarté.

```console
=============== Single Prediction just-trained-model - Result: area-System.Net ===============
The model is saved to C:\Users\johalex\dotnet-samples\samples\machine-learning\tutorials\GitHubIssueClassification\bin\Debug\netcoreapp2.0\..\..\..\Models\model.zip
*************************************************************************************************************
*       Metrics for Multi-class Classification model - Test Data
*------------------------------------------------------------------------------------------------------------
*       MicroAccuracy:    0.74
*       MacroAccuracy:    0.687
*       LogLoss:          .932
*       LogLossReduction: 63.852
*************************************************************************************************************
=============== Single Prediction - Result: area-System.Data ===============
```

Félicitations ! Vous venez de créer un modèle d’apprentissage automatique pour la classification et la prédiction d’une étiquette Area d’un problème GitHub. Vous trouverez le code source de ce tutoriel dans le référentiel [dotnet/samples](https://github.com/dotnet/samples/tree/master/machine-learning/tutorials/GitHubIssueClassification).

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
> [Prédiction du prix d’une course de taxi](taxi-fare.md)
