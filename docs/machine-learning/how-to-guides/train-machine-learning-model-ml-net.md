---
title: Entraîner et évaluer un modèle
description: Découvrez comment entraîner et évaluer des modèles Machine Learning dans ML.NET
ms.date: 05/03/2019
author: luisquintanilla
ms.author: luquinta
ms.custom: mvc, how-to
ms.openlocfilehash: 3a3f1f672ed078754162dc377cf5c239d206b715
ms.sourcegitcommit: 682c64df0322c7bda016f8bfea8954e9b31f1990
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2019
ms.locfileid: "65557848"
---
# <a name="train-and-evaluate-a-model"></a><span data-ttu-id="e5b7f-103">Entraîner et évaluer un modèle</span><span class="sxs-lookup"><span data-stu-id="e5b7f-103">Train and evaluate a model</span></span>

<span data-ttu-id="e5b7f-104">Découvrez comment créer des modèles Machine Learning, extraire des paramètres appris et mesurer les performances avec ML.NET.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-104">Learn how to build machine learning models, extract learned parameters and measure performance with ML.NET.</span></span> <span data-ttu-id="e5b7f-105">Bien que cet exemple entraîne un modèle de régression, les concepts s’appliquent à la majorité des autres algorithmes.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-105">Although this sample trains a regression model, the concepts are applicable throughout a majority of the other algorithms.</span></span>

## <a name="split-data-for-training-and-testing"></a><span data-ttu-id="e5b7f-106">Fractionner les données à des fins d’entraînement et de test</span><span class="sxs-lookup"><span data-stu-id="e5b7f-106">Split data for training and testing</span></span>

<span data-ttu-id="e5b7f-107">L’objectif d’un modèle Machine Learning consiste à identifier des modèles au sein de données d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-107">The goal of a machine learning model is to identify patterns within training data.</span></span> <span data-ttu-id="e5b7f-108">Ces modèles sont utilisés pour effectuer des prédictions à l’aide de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-108">These patterns are used to make predictions using new data.</span></span>

<span data-ttu-id="e5b7f-109">Soit le modèle de données suivant :</span><span class="sxs-lookup"><span data-stu-id="e5b7f-109">Given the following data model:</span></span>

```csharp
public class HousingData
{
    [LoadColumn(0)]
    public float Size { get; set; }

    [LoadColumn(1, 3)]
    [VectorType(3)]
    public float[] HistoricalPrices { get; set; }

    [LoadColumn(4)]
    [ColumnName("Label")]
    public float CurrentPrice { get; set; }
}
```

<span data-ttu-id="e5b7f-110">Chargez les données dans un [`IDataView`](xref:Microsoft.ML.IDataView) :</span><span class="sxs-lookup"><span data-stu-id="e5b7f-110">Load the data into an [`IDataView`](xref:Microsoft.ML.IDataView):</span></span>

```csharp
HousingData[] housingData = new HousingData[]
{
    new HousingData
    {
        Size = 600f,
        HistoricalPrices = new float[] { 100000f ,125000f ,122000f },
        CurrentPrice = 170000f
    },
    new HousingData
    {
        Size = 1000f,
        HistoricalPrices = new float[] { 200000f, 250000f, 230000f },
        CurrentPrice = 225000f
    },
    new HousingData
    {
        Size = 1000f,
        HistoricalPrices = new float[] { 126000f, 130000f, 200000f },
        CurrentPrice = 195000f
    },
    new HousingData
    {
        Size = 850f,
        HistoricalPrices = new float[] { 150000f,175000f,210000f },
        CurrentPrice = 205000f
    },
    new HousingData
    {
        Size = 900f,
        HistoricalPrices = new float[] { 155000f, 190000f, 220000f },
        CurrentPrice = 210000f
    },
    new HousingData
    {
        Size = 550f,
        HistoricalPrices = new float[] { 99000f, 98000f, 130000f },
        CurrentPrice = 180000f
    }
};
```

<span data-ttu-id="e5b7f-111">Utilisez la méthode [`TrainTestSplit`](xref:Microsoft.ML.DataOperationsCatalog.TrainTestSplit*) pour fractionner les données en jeux d’entraînement et de test.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-111">Use the [`TrainTestSplit`](xref:Microsoft.ML.DataOperationsCatalog.TrainTestSplit*) method to split the data into train and test sets.</span></span> <span data-ttu-id="e5b7f-112">Le résultat est un objet [`TrainTestData`](xref:Microsoft.ML.DataOperationsCatalog.TrainTestData) qui contient deux membres [`IDataView`](xref:Microsoft.ML.IDataView) : un pour le jeu d’entraînement, l’autre pour le jeu de test.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-112">The result will be a [`TrainTestData`](xref:Microsoft.ML.DataOperationsCatalog.TrainTestData) object which contains two [`IDataView`](xref:Microsoft.ML.IDataView) members, one for the train set and the other for the test set.</span></span> <span data-ttu-id="e5b7f-113">Le pourcentage de fractionnement des données est déterminé par le paramètre `testFraction`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-113">The data split percentage is determined by the `testFraction` parameter.</span></span> <span data-ttu-id="e5b7f-114">L’extrait de code ci-dessous réserve 20 % des données d’origine pour le jeu de test.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-114">The snippet below is holding out 20 percent of the original data for the test set.</span></span>

```csharp
DataOperationsCatalog.TrainTestData dataSplit = mlContext.Data.TrainTestSplit(data, testFraction: 0.2);
IDataView trainData = dataSplit.TrainSet;
IDataView testData = dataSplit.TestSet;
```

## <a name="prepare-the-data"></a><span data-ttu-id="e5b7f-115">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="e5b7f-115">Prepare the data</span></span>

<span data-ttu-id="e5b7f-116">Les données doivent être prétraitées avant l’entraînement d’un modèle Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-116">The data needs to be pre-processed before training a machine learning model.</span></span> <span data-ttu-id="e5b7f-117">Vous trouverez plus d’informations sur la préparation des données dans l’[article sur les procédures de préparation des données](prepare-data-ml-net.md) ainsi qu’à la [`transforms page`](../resources/transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e5b7f-117">More information on data preparation can be found on the [data prep how-to article](prepare-data-ml-net.md) as well as the [`transforms page`](../resources/transforms.md).</span></span>

<span data-ttu-id="e5b7f-118">Les algorithmes ML.NET ont des contraintes sur les types de colonnes d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-118">ML.NET algorithms have constraints on input column types.</span></span> <span data-ttu-id="e5b7f-119">En outre, les valeurs par défaut sont utilisées pour les noms de colonne d’entrée et de sortie quand aucune valeur n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-119">Additionally, default values are used for input and output column names when no values are specified.</span></span>

### <a name="working-with-expected-column-types"></a><span data-ttu-id="e5b7f-120">Utilisation de types de colonnes attendus</span><span class="sxs-lookup"><span data-stu-id="e5b7f-120">Working with expected column types</span></span>

<span data-ttu-id="e5b7f-121">Les algorithmes de machine learning dans ML.NET attendent un vecteur à virgule flottante de taille connue en tant qu’entrée.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-121">The machine learning algorithms in ML.NET expect a float vector of known size as input.</span></span> <span data-ttu-id="e5b7f-122">Appliquez l’attribut [`VectorType`](xref:Microsoft.ML.Data.VectorTypeAttribute) à votre modèle de données quand toutes les données sont déjà au format numérique et sont destinées à être traitées ensemble (par exemple, les pixels d’une image).</span><span class="sxs-lookup"><span data-stu-id="e5b7f-122">Apply the [`VectorType`](xref:Microsoft.ML.Data.VectorTypeAttribute) attribute to your data model when all of the data is already in numerical format and is intended to be processed together (i.e. image pixels).</span></span> 

<span data-ttu-id="e5b7f-123">Si les données ne sont pas toutes numériques et que vous souhaitez appliquer différentes transformations de données sur chacune des colonnes individuellement, utilisez la méthode [`Concatenate`](xref:Microsoft.ML.TransformExtensionsCatalog.Concatenate*) une fois que toutes les colonnes ont été traitées pour combiner toutes les colonnes individuelles en un vecteur de caractéristiques unique qui est généré dans une nouvelle colonne.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-123">If data is not all numerical and you want to apply different data transformations on each of the columns individually, use the [`Concatenate`](xref:Microsoft.ML.TransformExtensionsCatalog.Concatenate*) method after all of the columns have been processed to combine all of the individual columns into a single feature vector that is output to a new column.</span></span> 

<span data-ttu-id="e5b7f-124">L’extrait de code suivant combine les colonnes `Size` et `HistoricalPrices` en un vecteur de caractéristiques unique qui est généré dans une nouvelle colonne appelée `Features`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-124">The following snippet combines the `Size` and `HistoricalPrices` columns into a single feature vector that is output to a new column called `Features`.</span></span> <span data-ttu-id="e5b7f-125">Les échelles étant différentes, [`NormalizeMinMax`](xref:Microsoft.ML.NormalizationCatalog.NormalizeMinMax*) est appliqué à la colonne `Features` pour normaliser les données.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-125">Because there is a difference in scales, [`NormalizeMinMax`](xref:Microsoft.ML.NormalizationCatalog.NormalizeMinMax*) is applied to the `Features` column to normalize the data.</span></span>

```csharp
// Define Data Prep Estimator
// 1. Concatenate Size and Historical into a single feature vector output to a new column called Features
// 2. Normalize Features vector
IEstimator<ITransformer> dataPrepEstimator =
    mlContext.Transforms.Concatenate("Features", "Size", "HistoricalPrices")
        .Append(mlContext.Transforms.NormalizeMinMax("Features"));

// Create data prep transformer
ITransformer dataPrepTransformer = dataPrepEstimator.Fit(trainData);

// Apply tranforms to training data
IDataView transformedTrainingData = dataPrepTransformer.Transform(trainData);
```

### <a name="working-with-default-column-names"></a><span data-ttu-id="e5b7f-126">Utilisation de noms de colonne par défaut</span><span class="sxs-lookup"><span data-stu-id="e5b7f-126">Working with default column names</span></span>

<span data-ttu-id="e5b7f-127">Les algorithmes ML.NET utilisent des noms de colonne par défaut quand aucun n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-127">ML.NET algorithms use default column names when none are specified.</span></span> <span data-ttu-id="e5b7f-128">Tous les entraîneurs ont un paramètre appelé `featureColumnName` pour les entrées de l’algorithme et, le cas échéant, ils ont également un paramètre pour la valeur attendue appelé `labelColumnName`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-128">All trainers have a parameter called `featureColumnName` for the inputs of the algorithm and when applicable they also have a parameter for the expected value called `labelColumnName`.</span></span> <span data-ttu-id="e5b7f-129">Par défaut, ces valeurs sont `Features` et `Label` respectivement.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-129">By default those values are `Features` and `Label` respectively.</span></span> 

<span data-ttu-id="e5b7f-130">La méthode [`Concatenate`](xref:Microsoft.ML.TransformExtensionsCatalog.Concatenate*) ayant été utilisée pendant le prétraitement pour créer une colonne appelée `Features`, il est inutile de spécifier le nom de la colonne des caractéristiques dans les paramètres de l’algorithme dans la mesure où il existe déjà dans le `IDataView` prétraité.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-130">By using the [`Concatenate`](xref:Microsoft.ML.TransformExtensionsCatalog.Concatenate*) method during pre-processing to create a new column called `Features`, there is no need to specify the feature column name in the parameters of the algorithm since it already exists in the pre-processed `IDataView`.</span></span> <span data-ttu-id="e5b7f-131">La colonne des étiquettes est `CurrentPrice`, mais comme l’attribut [`ColumnName`](xref:Microsoft.ML.Data.ColumnNameAttribute) est utilisé dans le modèle de données, ML.NET renomme la colonne `CurrentPrice` en `Label` ; ainsi, il n’est pas nécessaire de fournir le paramètre `labelColumnName` à l’estimateur de l’algorithme de machine learning.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-131">The label column is `CurrentPrice`, but since the [`ColumnName`](xref:Microsoft.ML.Data.ColumnNameAttribute) attribute is used in the data model, ML.NET renames the `CurrentPrice` column to `Label` which removes the need to provide the `labelColumnName` parameter to the machine learning algorithm estimator.</span></span> 

<span data-ttu-id="e5b7f-132">Si vous ne souhaitez pas utiliser les noms de colonne par défaut, passez les noms des colonnes des caractéristiques et des étiquettes en tant que paramètres lors de la définition de l’estimateur de l’algorithme de machine learning, comme illustré dans l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="e5b7f-132">If you don't want to use the default column names, pass in the names of the feature and label columns as parameters when defining the machine learning algorithm estimator as demonstrated by the subsequent snippet:</span></span>

```csharp
var UserDefinedColumnSdcaEstimator = mlContext.Regression.Trainers.Sdca(labelColumnName: "MyLabelColumnName", featureColumnName: "MyFeatureColumnName");
```

## <a name="train-the-machine-learning-model"></a><span data-ttu-id="e5b7f-133">Entraîner le modèle Machine Learning</span><span class="sxs-lookup"><span data-stu-id="e5b7f-133">Train the machine learning model</span></span>

<span data-ttu-id="e5b7f-134">Une fois les données prétraitées, utilisez la méthode [`Fit`](xref:Microsoft.ML.Trainers.TrainerEstimatorBase`2.Fit*) pour entraîner le modèle Machine Learning avec l’algorithme de régression [`StochasticDualCoordinateAscent`](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer).</span><span class="sxs-lookup"><span data-stu-id="e5b7f-134">Once the data is pre-processed, use the [`Fit`](xref:Microsoft.ML.Trainers.TrainerEstimatorBase`2.Fit*) method to train the machine learning model with the [`StochasticDualCoordinateAscent`](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer) regression algorithm.</span></span>

```csharp
// Define StochasticDualCoodrinateAscent regression algorithm estimator
var sdcaEstimator = mlContext.Regression.Trainers.Sdca();

// Build machine learning model
var trainedModel = sdcaEstimator.Fit(transformedTrainingData);
```

## <a name="extract-model-parameters"></a><span data-ttu-id="e5b7f-135">Extraire les paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="e5b7f-135">Extract model parameters</span></span>

<span data-ttu-id="e5b7f-136">Une fois le modèle entraîné, extrayez les [`ModelParameters`](xref:Microsoft.ML.Trainers.ModelParametersBase%601) appris à des fins d’inspection ou de réentraînement.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-136">After the model has been trained, extract the learned [`ModelParameters`](xref:Microsoft.ML.Trainers.ModelParametersBase%601) for inspection or re-training.</span></span> <span data-ttu-id="e5b7f-137">Les [`LinearRegressionModelParameters`](xref:Microsoft.ML.Trainers.LinearRegressionModelParameters) fournissent les coefficients de biais et appris ou les pondérations du modèle entraîné.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-137">The [`LinearRegressionModelParameters`](xref:Microsoft.ML.Trainers.LinearRegressionModelParameters) provide the bias and learned coefficients or weights of the trained model.</span></span> 

```csharp
var trainedModelParameters = trainedModel.Model as LinearRegressionModelParameters;
```

> [!NOTE]
> <span data-ttu-id="e5b7f-138">D’autres modèles ont des paramètres qui sont spécifiques de leurs tâches.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-138">Other models have parameters that are specific to their tasks.</span></span> <span data-ttu-id="e5b7f-139">Par exemple, l’[algorithme k-moyennes](xref:Microsoft.ML.Trainers.KMeansTrainer) place les données dans un cluster basé sur des centroïdes et [`KMeansModelParameters`](xref:Microsoft.ML.Trainers.KMeansModelParameters) contient une propriété qui stocke ces centroïdes appris.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-139">For example, the [K-Means algorithm](xref:Microsoft.ML.Trainers.KMeansTrainer) puts data into cluster based on centroids and the [`KMeansModelParameters`](xref:Microsoft.ML.Trainers.KMeansModelParameters) contains a property that stores these learned centroids.</span></span> <span data-ttu-id="e5b7f-140">Pour en savoir plus, consultez la [documentation de l’API `Microsoft.ML.Trainers`](xref:Microsoft.ML.Trainers) et recherchez les classes dont le nom contient `ModelParameters`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-140">To learn more, visit the [`Microsoft.ML.Trainers` API Documentation](xref:Microsoft.ML.Trainers) and look for classes that contain `ModelParameters` in their name.</span></span> 

## <a name="evaluate-model-quality"></a><span data-ttu-id="e5b7f-141">Évaluer la qualité du modèle</span><span class="sxs-lookup"><span data-stu-id="e5b7f-141">Evaluate model quality</span></span>

<span data-ttu-id="e5b7f-142">Pour choisir plus facilement le modèle le plus performant, il est essentiel d’évaluer ses performances sur des données de test.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-142">To help choose the best performing model, it is essential to evaluate its performance on test data.</span></span> <span data-ttu-id="e5b7f-143">Utilisez la méthode [`Evaluate`](xref:Microsoft.ML.RegressionCatalog.Evaluate*) afin de mesurer diverses métriques pour le modèle entraîné.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-143">Use the [`Evaluate`](xref:Microsoft.ML.RegressionCatalog.Evaluate*) method, to measure various metrics for the trained model.</span></span>

> [!NOTE]
> <span data-ttu-id="e5b7f-144">La méthode `Evaluate` produit différentes métriques en fonction de la tâche de machine learning qui a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-144">The `Evaluate` method produces different metrics depending on which machine learning task was was performed.</span></span> <span data-ttu-id="e5b7f-145">Pour plus d’informations, consultez la [documentation de l’API `Microsoft.ML.Data`](xref:Microsoft.ML.Data) et recherchez les classes dont le nom contient `Metrics`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-145">For more details, visit the [`Microsoft.ML.Data` API Documentation](xref:Microsoft.ML.Data) and look for classes that contain `Metrics` in their name.</span></span> 

```csharp
// Measure trained model performance
// Apply data prep transformer to test data
IDataView transformedTestData = dataPrepTransformer.Transform(testData);

// Use trained model to make inferences on test data
IDataView testDataPredictions = trainedModel.Transform(transformedTestData);

// Extract model metrics and get RSquared
RegressionMetrics trainedModelMetrics = mlContext.Regression.Evaluate(testDataPredictions);
double rSquared = trainedModelMetrics.RSquared;
```

<span data-ttu-id="e5b7f-146">Dans l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="e5b7f-146">In the previous code sample:</span></span>  
1. <span data-ttu-id="e5b7f-147">Le jeu de données de test est prétraité à l’aide de transformations de préparation de données préalablement définies.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-147">Test data set is pre-processed using the data preparation transforms previously defined.</span></span> 
2. <span data-ttu-id="e5b7f-148">Le modèle Machine Learning entraîné est utilisé pour effectuer des prédictions sur les données de test.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-148">The trained machine learning model is used to make predictions on the test data.</span></span>
3. <span data-ttu-id="e5b7f-149">Dans la méthode `Evaluate`, les valeurs de la colonne `CurrentPrice` du jeu de données de test sont comparées à la colonne `Score` des prédictions qui viennent d’être générées pour calculer les métriques du modèle de régression, dont l’une, le coefficient de détermination, est stockée dans la variable `rSquared`.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-149">In the `Evaluate` method, the values in the `CurrentPrice` column of the test data set are compared against the `Score` column of the newly output predictions to calculate the metrics for the regression model, one of which, R-Squared is stored in the `rSquared` variable.</span></span>

> [!NOTE]
> <span data-ttu-id="e5b7f-150">Dans ce petit exemple, le coefficient de détermination est un nombre qui n’appartient pas à la plage 0-1 en raison de la taille limitée des données.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-150">In this small example, the R-Squared is a number not in the range of 0-1 because of the limited size of the data.</span></span> <span data-ttu-id="e5b7f-151">Dans un scénario réel, vous devez vous attendre à une valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="e5b7f-151">In a real-world scenario, you should expect to see a value between 0 and 1.</span></span>