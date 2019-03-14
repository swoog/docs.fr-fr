---
title: Concepts de base pour l’entraînement de modèles dans ML.NET
description: Cet article explique les concepts de base couvrant les scénarios d’*entraînement de modèles* dans ML.NET. Tous les concepts ne sont pas pertinents pour le scénario le plus simple de *prédiction avec un modèle existant*.
ms.date: 03/05/2019
ms.topic: overview
ms.custom: mvc
ms.openlocfilehash: 78554cfd1dfdb3dba82a325d47245aeb313bb6fe
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57675561"
---
# <a name="basic-concepts-for-model-training-in-mlnet"></a><span data-ttu-id="637fb-104">Concepts de base pour l’entraînement de modèles dans ML.NET</span><span class="sxs-lookup"><span data-stu-id="637fb-104">Basic concepts for model training in ML.NET</span></span>

<span data-ttu-id="637fb-105">Cet article explique les concepts de base couvrant les scénarios d’*entraînement de modèles* dans ML.NET.</span><span class="sxs-lookup"><span data-stu-id="637fb-105">This article explains the basic concepts covering *model training* scenarios in ML.NET.</span></span> <span data-ttu-id="637fb-106">Tous les concepts ne sont pas pertinents pour le scénario le plus simple de *prédiction avec un modèle existant*.</span><span class="sxs-lookup"><span data-stu-id="637fb-106">Not all concepts are relevant to the more simple scenario of *prediction with an existing model*.</span></span>

<span data-ttu-id="637fb-107">Cet article et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="637fb-107">This article and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="637fb-108">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="637fb-108">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

## <a name="model-training-concepts"></a><span data-ttu-id="637fb-109">Concepts de l’entraînement de modèles</span><span class="sxs-lookup"><span data-stu-id="637fb-109">Model training concepts</span></span>

<span data-ttu-id="637fb-110">Ce document aborde les concepts suivants liés à l’entraînement de modèles dans ML.NET :</span><span class="sxs-lookup"><span data-stu-id="637fb-110">This document covers the following concepts related to model training in ML.NET:</span></span>

- <span data-ttu-id="637fb-111">[*Données*](#data) représentées sous la forme d’une interface `IDataView`.</span><span class="sxs-lookup"><span data-stu-id="637fb-111">[*Data*](#data) represented as an `IDataView` interface.</span></span>
  - <span data-ttu-id="637fb-112">Dans ML.NET, les données sont semblables à une vue SQL : il s’agit d’un jeu de données schématisé, hétérogène, immuable, analysable par un curseur et évalué tardivement.</span><span class="sxs-lookup"><span data-stu-id="637fb-112">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, immutable, cursorable, heterogenous, schematized dataset.</span></span> 
  - <span data-ttu-id="637fb-113">Le document [Principes de conception IDataView](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md) est une excellente source d’information sur l’interface de données.</span><span class="sxs-lookup"><span data-stu-id="637fb-113">An excellent document about the data interface is [IDataView Design Principles](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md).</span></span>
- <span data-ttu-id="637fb-114">[*Transformateur*](#transformer) représenté sous la forme d’une interface `ITransformer`.</span><span class="sxs-lookup"><span data-stu-id="637fb-114">[*Transformer*](#transformer) represented as `ITransformer` interface.</span></span>
  - <span data-ttu-id="637fb-115">Un transformateur est un composant qui prend des données, les manipule, puis retourne de nouvelles données transformées.</span><span class="sxs-lookup"><span data-stu-id="637fb-115">A transformer is a component that takes data, does some work on it, and returns new transformed data.</span></span>
  - <span data-ttu-id="637fb-116">Par exemple, vous pouvez considérer un modèle Machine Learning comme un transformateur qui prend des caractéristiques et retourne des prédictions.</span><span class="sxs-lookup"><span data-stu-id="637fb-116">For example, you can think of a machine learning model as a transformer that takes features and returns predictions.</span></span>
  - <span data-ttu-id="637fb-117">Autre exemple : le générateur de jetons de texte prend une colonne de textes unique et génère une colonne de vecteurs avec des mots individuels extraits des textes.</span><span class="sxs-lookup"><span data-stu-id="637fb-117">Another example, text tokenizer takes a single text column and outputs a vector column with individual words extracted out of the texts.</span></span>
- <span data-ttu-id="637fb-118">[*Lecteur de données*](#data-reader) représenté sous la forme d’une interface `IDataReader<T>`.</span><span class="sxs-lookup"><span data-stu-id="637fb-118">[*Data reader*](#data-reader) represented as an `IDataReader<T>` interface.</span></span>
  - <span data-ttu-id="637fb-119">Le lecteur de données est un composant ML.NET servant à créer des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-119">The data reader is ML.NET component to create data.</span></span> <span data-ttu-id="637fb-120">Il prend une instance de `T` et retourne des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-120">It takes an instance of `T` and returns data out of it.</span></span> 
  - <span data-ttu-id="637fb-121">Par exemple, un *TextLoader* est un `IDataReader<IMultiStreamSource>`.</span><span class="sxs-lookup"><span data-stu-id="637fb-121">For example, a *TextLoader* is an `IDataReader<IMultiStreamSource>`.</span></span> <span data-ttu-id="637fb-122">Il prend la source et génère des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-122">It takes the source and produces data.</span></span> 
- <span data-ttu-id="637fb-123">[*Estimateur*](#estimator) représenté sous la forme d’une interface `IEstimator<T>`.</span><span class="sxs-lookup"><span data-stu-id="637fb-123">[*Estimator*](#estimator) represented as an `IEstimator<T>` interface.</span></span>
  - <span data-ttu-id="637fb-124">Il s’agit d’un objet qui apprend à partir des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-124">This is an object that learns from data.</span></span> <span data-ttu-id="637fb-125">Le résultat de l’entraînement est un *transformateur*.</span><span class="sxs-lookup"><span data-stu-id="637fb-125">The result of the learning is a *transformer*.</span></span>
  - <span data-ttu-id="637fb-126">Vous pouvez considérer un *algorithme* de machine learning comme un estimateur qui apprend à partir de données et génère un *modèle* Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="637fb-126">You can think of a machine learning *algorithm* as an estimator that learns on data and produces a machine learning *model*.</span></span>
- <span data-ttu-id="637fb-127">[*Fonction de prédiction*](#prediction-function) représentée sous la forme d’une classe `PredictionEngine<TSrc, TDst>`.</span><span class="sxs-lookup"><span data-stu-id="637fb-127">[*Prediction function*](#prediction-function) represented as a `PredictionEngine<TSrc, TDst>` class.</span></span>
  - <span data-ttu-id="637fb-128">La fonction de prédiction peut être considérée comme une machine qui applique un transformateur à une seule ligne, comme au moment de la prédiction.</span><span class="sxs-lookup"><span data-stu-id="637fb-128">The prediction function can be seen as a machine that applies a transformer to one row, such as at prediction time.</span></span>

## <a name="data"></a><span data-ttu-id="637fb-129">Données</span><span class="sxs-lookup"><span data-stu-id="637fb-129">Data</span></span>

<span data-ttu-id="637fb-130">Dans ML.NET, les données sont semblables à une vue SQL : il s’agit d’un jeu de données schématisé, hétérogène, analysable par un curseur et évalué tardivement.</span><span class="sxs-lookup"><span data-stu-id="637fb-130">In ML.NET, data is similar to a SQL view: It's a lazily evaluated, cursorable, heterogenous, schematized dataset.</span></span>

- <span data-ttu-id="637fb-131">Il a un *schéma* (instance d’une interface `ISchema`) qui contient des informations sur les colonnes de la vue de données.</span><span class="sxs-lookup"><span data-stu-id="637fb-131">It has *Schema* (an instance of an `ISchema` interface) that contains the information about the data view's columns.</span></span>
  - <span data-ttu-id="637fb-132">Chaque colonne a un *nom*, un *type* et un ensemble arbitraire de *métadonnées* associés.</span><span class="sxs-lookup"><span data-stu-id="637fb-132">Each column has a *Name*, a *Type*, and an arbitrary set of *metadata* associated with it.</span></span>
  - <span data-ttu-id="637fb-133">Les *métadonnées* de la colonne contiennent des informations telles que des noms d’emplacement d’une colonne de vecteurs et autres informations du même ordre.</span><span class="sxs-lookup"><span data-stu-id="637fb-133">The column's *metadata* contains information like slot names of a vector column and the like.</span></span> <span data-ttu-id="637fb-134">Les métadonnées elles-mêmes sont également représentées sous la forme de *données* d’une ligne qui sont propres à chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="637fb-134">The metadata itself is represented as another one-row *data* that is unique to each column.</span></span>
  - <span data-ttu-id="637fb-135">La vue de données est une source de *curseurs*.</span><span class="sxs-lookup"><span data-stu-id="637fb-135">The data view is a source of *cursors*.</span></span> <span data-ttu-id="637fb-136">Pensez aux curseurs SQL : un curseur est un objet qui effectue une itération au sein des données, une ligne à la fois, et présente les données disponibles.</span><span class="sxs-lookup"><span data-stu-id="637fb-136">Think SQL cursors: A cursor is an object that iterates through the data, one row at a time, and presents the available data.</span></span>
  - <span data-ttu-id="637fb-137">Naturellement, les données peuvent être parcourues par autant de curseurs actifs que nécessaires.</span><span class="sxs-lookup"><span data-stu-id="637fb-137">Naturally, data can have as many active cursors over it as needed.</span></span> <span data-ttu-id="637fb-138">Dans la mesure où les données proprement dites sont immuables, les curseurs sont véritablement indépendants.</span><span class="sxs-lookup"><span data-stu-id="637fb-138">Since data itself is immutable, cursors are truly independent.</span></span>
  - <span data-ttu-id="637fb-139">En règle générale, les curseurs accèdent uniquement à un sous-ensemble de colonnes : pour plus d’efficacité, ML.NET calcule uniquement les valeurs de colonnes qui sont requises par le curseur.</span><span class="sxs-lookup"><span data-stu-id="637fb-139">Cursors typically access only a subset of columns: For efficiency, ML.NET computes only the values of columns that are needed by the cursor.</span></span>

## <a name="transformer"></a><span data-ttu-id="637fb-140">Transformateur</span><span class="sxs-lookup"><span data-stu-id="637fb-140">Transformer</span></span>

<span data-ttu-id="637fb-141">Un transformateur est un composant qui prend des données, les manipule, puis retourne de nouvelles données transformées.</span><span class="sxs-lookup"><span data-stu-id="637fb-141">A transformer is a component that takes data, does some work on it, and returns new transformed data.</span></span>

<span data-ttu-id="637fb-142">La plupart des transformateurs dans ML.NET ont tendance à opérer sur une *colonne d’entrée* à la fois et à produire la *colonne de sortie*.</span><span class="sxs-lookup"><span data-stu-id="637fb-142">Most transformers in ML.NET tend to operate on one *input column* at a time, and produce the *output column*.</span></span> <span data-ttu-id="637fb-143">Par exemple, un `new HashTransformer("bar", "foo")` prend les valeurs de la colonne « foo », les hache et les place dans la colonne « bar ».</span><span class="sxs-lookup"><span data-stu-id="637fb-143">For example, a `new HashTransformer("bar", "foo")` takes the values from column "foo", hashes them, and puts them into column "bar".</span></span> 

<span data-ttu-id="637fb-144">Il est également courant que les noms de colonnes d’entrée et de sortie soient identiques.</span><span class="sxs-lookup"><span data-stu-id="637fb-144">It's also common that the input and output column names are the same.</span></span> <span data-ttu-id="637fb-145">Dans ce cas, l’ancienne colonne est remplacée par la nouvelle.</span><span class="sxs-lookup"><span data-stu-id="637fb-145">In this case, the old column is replaced with the new one.</span></span> <span data-ttu-id="637fb-146">Par exemple, un `new HashTransformer("foo")` prend les valeurs de la colonne « foo », les hache et les remet dans « foo ».</span><span class="sxs-lookup"><span data-stu-id="637fb-146">For example, a `new HashTransformer("foo")` takes the values from column "foo", hashes them, and puts them back into "foo".</span></span> 

<span data-ttu-id="637fb-147">Tout transformateur génère une nouvelle vue de données quand `Transform` est appelé.</span><span class="sxs-lookup"><span data-stu-id="637fb-147">Any transformer, produces a new data view when `Transform` is called.</span></span> <span data-ttu-id="637fb-148">N’oubliez pas que les vues de données sont immuables.</span><span class="sxs-lookup"><span data-stu-id="637fb-148">Remember, data views are immutable.</span></span>

<span data-ttu-id="637fb-149">Un autre élément important est que, les données étant évaluées tardivement, les *transformateurs sont tardifs également*.</span><span class="sxs-lookup"><span data-stu-id="637fb-149">Another important consideration is that, because data is lazily evaluated, *transformers are lazy too*.</span></span> <span data-ttu-id="637fb-150">Essentiellement, une fois que vous avez appelé</span><span class="sxs-lookup"><span data-stu-id="637fb-150">Essentially, after you call</span></span>

```csharp
var newData = transformer.Transform(oldData)
```

<span data-ttu-id="637fb-151">aucun calcul réel ne se produit.</span><span class="sxs-lookup"><span data-stu-id="637fb-151">no actual computation happens.</span></span> <span data-ttu-id="637fb-152">C’est seulement une fois que vous obtenez un curseur à partir de `newData` et que vous commencez à utiliser la valeur que `newData` appelle la logique de transformation `transformer` (et même là, cela se produit uniquement si le `transformer` en question est nécessaire pour générer les colonnes demandées).</span><span class="sxs-lookup"><span data-stu-id="637fb-152">Only after you get a cursor from `newData` and start consuming the value does `newData` invoke the `transformer` transformation logic (and even then, it only happens if the `transformer` in question is needed to produce the requested columns).</span></span>

### <a name="transformer-chains"></a><span data-ttu-id="637fb-153">Chaînes de transformateur</span><span class="sxs-lookup"><span data-stu-id="637fb-153">Transformer chains</span></span>

<span data-ttu-id="637fb-154">Une propriété utile d’un transformateur est que *vous pouvez générer une application séquentielle de transformateurs sous la forme d’un autre transformateur* :</span><span class="sxs-lookup"><span data-stu-id="637fb-154">A useful property of a transformer is that *you can build a sequential application of transformers as yet another transformer*:</span></span>

```csharp
var fullTransformer = transformer1.Append(transformer2).Append(transformer3);
```

<span data-ttu-id="637fb-155">Cette propriété est couramment utilisée dans ML.NET : en règle générale, le modèle ML.NET entraîné est une chaîne de transformateurs, qui est, à toutes fins pratiques, un *transformateur*.</span><span class="sxs-lookup"><span data-stu-id="637fb-155">This property is commonly used in ML.NET: typically, the trained ML.NET model is a chain of transformers, which is, for all intents and purposes, a *transformer*.</span></span>

## <a name="data-reader"></a><span data-ttu-id="637fb-156">Lecteur de données</span><span class="sxs-lookup"><span data-stu-id="637fb-156">Data reader</span></span>

<span data-ttu-id="637fb-157">Le lecteur de données est un composant ML.NET servant à « créer » des données : il prend une instance de `T` et retourne des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-157">The data reader is an ML.NET component to 'create' data: it takes an instance of `T` and returns data out of it.</span></span>

<span data-ttu-id="637fb-158">Une propriété intéressante est que vous pouvez créer un lecteur de données en attachant un transformateur à un lecteur de données existant.</span><span class="sxs-lookup"><span data-stu-id="637fb-158">An interesting property to note is that you can create a data reader by attaching a transformer to an existing data reader.</span></span> <span data-ttu-id="637fb-159">De cette façon, vous pouvez avoir un lecteur intégrant un comportement de transformation :</span><span class="sxs-lookup"><span data-stu-id="637fb-159">This way you can have a reader with transformation behavior baked in:</span></span>

```csharp
var newReader = reader.Append(transformer1).Append(transformer2)
```

<span data-ttu-id="637fb-160">Une autre similarité avec les transformateurs est que, dans la mesure où les données sont évaluées tardivement, les *lecteurs sont tardifs* : aucune (ou pratiquement aucune) « lecture » réelle ne se produit quand vous appelez `reader.Read()` ; le lecteur ne commence à travailler que quand un curseur est demandé sur les données résultantes.</span><span class="sxs-lookup"><span data-stu-id="637fb-160">Another similarity to transformers is that, since data is lazily evaluated, *readers are lazy*: no (or minimal) actual 'reading' happens when you call `reader.Read()`: only when a cursor is requested on the resulting data does the reader begin to work.</span></span>

## <a name="estimator"></a><span data-ttu-id="637fb-161">Estimateur</span><span class="sxs-lookup"><span data-stu-id="637fb-161">Estimator</span></span>

<span data-ttu-id="637fb-162">L’*estimateur* est un objet qui apprend à partir des données.</span><span class="sxs-lookup"><span data-stu-id="637fb-162">The *estimator* is an object that learns from data.</span></span> <span data-ttu-id="637fb-163">Le résultat de l’entraînement est un *transformateur*.</span><span class="sxs-lookup"><span data-stu-id="637fb-163">The result of the learning is a *transformer*.</span></span>

<span data-ttu-id="637fb-164">Dans ML.NET, utilisez cette propriété pour créer des pipelines d’entraînement qui chaînent différents estimateurs :</span><span class="sxs-lookup"><span data-stu-id="637fb-164">In ML.NET, use this property to create learning pipelines that chain together different estimators:</span></span>

```csharp
MLContext mlContext = new MLContext(seed: 0);

var pipeline = mlContext.Transforms.CopyColumns("Label","FareAmount")
    .Append(mlContext.Transforms.Categorical.OneHotEncoding("VendorId"))
    .Append(mlContext.Transforms.Categorical.OneHotEncoding("RateCode"))
    .Append(mlContext.Transforms.Categorical.OneHotEncoding("PaymentType"))
    .Append(mlContext.Transforms.Concatenate("Features","VendorId","RateCode","PassengerCount","TripTime","TripDistance","PaymentType"))
    .Append(mlContext.Regression.Trainers.FastTree("Label","Features"));

var model = pipeline.Fit(dataView);
```

<span data-ttu-id="637fb-165">Une des propriétés importantes des estimateurs est que *les estimateurs sont hâtifs, pas tardifs* : chaque appel à `Fit` entraîne un apprentissage, opération qui peut s’avérer longue.</span><span class="sxs-lookup"><span data-stu-id="637fb-165">One important property of estimators is that *estimators are eager, not lazy*: every call to `Fit` is causing learning to happen, which is potentially a time-consuming operation.</span></span>

## <a name="prediction-function"></a><span data-ttu-id="637fb-166">Fonction de prédiction</span><span class="sxs-lookup"><span data-stu-id="637fb-166">Prediction function</span></span>

<span data-ttu-id="637fb-167">La fonction de prédiction peut être considérée comme un composant qui applique un transformateur à une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="637fb-167">The prediction function can be seen as a component that applies a transformer to one row.</span></span>

<span data-ttu-id="637fb-168">Une fois que vous obtenez le modèle (un *transformateur* entraîné par le biais de `Fit()` ou chargé), vous pouvez l’utiliser pour effectuer des prédictions à l’aide d’appels normaux à `model.Transform(data)`.</span><span class="sxs-lookup"><span data-stu-id="637fb-168">Once you get the model (a *transformer* either trained via `Fit()`, or loaded from somewhere), you can use it to make predictions using the normal calls to `model.Transform(data)`.</span></span> <span data-ttu-id="637fb-169">Toutefois, quand vous utilisez ce modèle dans un scénario réel, vous n’avez souvent pas de nombreux exemples à partir desquels effectuer la prédiction.</span><span class="sxs-lookup"><span data-stu-id="637fb-169">However, when you use this model in a real-life scenario, you often don't have many examples to predict on.</span></span> <span data-ttu-id="637fb-170">Au lieu de cela, vous disposez d’un exemple à la fois, et vous devez faire des prédictions en temps voulu sur ces derniers immédiatement.</span><span class="sxs-lookup"><span data-stu-id="637fb-170">Instead, you have one example at a time, and you need to make timely predictions on them immediately.</span></span>

<span data-ttu-id="637fb-171">Bien sûr, vous pouvez réduire la procédure à une prédiction par lot :</span><span class="sxs-lookup"><span data-stu-id="637fb-171">Of course, you can reduce this to the batch prediction:</span></span>

- <span data-ttu-id="637fb-172">Créer une vue de données avec une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="637fb-172">Create a data view with exactly one row.</span></span>
- <span data-ttu-id="637fb-173">Appeler `model.Transform(data)` pour obtenir la vue de données prédites.</span><span class="sxs-lookup"><span data-stu-id="637fb-173">Call `model.Transform(data)` to get the predicted data view.</span></span>
- <span data-ttu-id="637fb-174">Obtenir un curseur sur les données résultantes.</span><span class="sxs-lookup"><span data-stu-id="637fb-174">Get a cursor over the resulting data.</span></span>
- <span data-ttu-id="637fb-175">Faire progresser le curseur d’une étape pour accéder à la première (et unique) ligne.</span><span class="sxs-lookup"><span data-stu-id="637fb-175">Advance the cursor one step to get to the first (and only) row.</span></span>
- <span data-ttu-id="637fb-176">Extraire les valeurs prédites.</span><span class="sxs-lookup"><span data-stu-id="637fb-176">Extract the predicted values out of it.</span></span>

<span data-ttu-id="637fb-177">L’algorithme précédent peut être implémenté à l’aide de la [compréhension du schéma](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md), avec deux objets définis par l’utilisateur `InputExample` et `OutputPrediction` comme suit :</span><span class="sxs-lookup"><span data-stu-id="637fb-177">The preceding algorithm can be implemented using the [schema comprehension](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md), with two user-defined objects `InputExample` and `OutputPrediction` as follows:</span></span>

```csharp
var inputData = mlContext.Data.ReadFromEnumerable(new InputExample[] { example });
var outputData = model.Transform(inputData);
var output = mlContext.CreateEnumerable<OutputPrediction>(outputData,reuseRowObject:false).First();
```

<span data-ttu-id="637fb-178">Mais cela est fastidieux et entraîne des coûts de performances.</span><span class="sxs-lookup"><span data-stu-id="637fb-178">But this is cumbersome and incurs performance costs.</span></span> <span data-ttu-id="637fb-179">À la place, un objet de fonction de prédiction effectue le même travail, mais de façon plus rapide et pratique, par le biais d’une méthode d’extension `CreatePredictionEngine` :</span><span class="sxs-lookup"><span data-stu-id="637fb-179">Instead, a prediction function object performs the same work, but faster and more convenient, via an extension method `CreatePredictionEngine`:</span></span>

```csharp
var predictionEngine = model.CreatePredictionEngine<InputExample,OutputPrediction>(mlContext);
var prediction = predictionEngine.Predict(example);
```

<span data-ttu-id="637fb-180">La fonction de prédiction est *non réentrante/thread-safe*.</span><span class="sxs-lookup"><span data-stu-id="637fb-180">The prediction function is *not re-entrant / thread-safe*.</span></span> <span data-ttu-id="637fb-181">Si vous souhaitez effectuer des prédictions simultanément avec plusieurs threads, vous devez disposer d’une fonction de prédiction par thread.</span><span class="sxs-lookup"><span data-stu-id="637fb-181">If you want to conduct predictions simultaneously with multiple threads, you need to have a prediction function per thread.</span></span>
