---
title: Concepts de base pour l’entraînement de modèles dans ML.NET
description: Cet article explique les concepts de base couvrant les scénarios d’*entraînement de modèles* dans ML.NET. Tous les concepts ne sont pas pertinents pour le scénario le plus simple de *prédiction avec un modèle existant*.
ms.date: 11/06/2018
ms.topic: overview
ms.custom: mvc
ms.openlocfilehash: cff833b45583bc752bb42616820a95ca6c5c6b12
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "55252438"
---
# <a name="basic-concepts-for-model-training-in-mlnet"></a>Concepts de base pour l’entraînement de modèles dans ML.NET

Cet article explique les concepts de base couvrant les scénarios d’*entraînement de modèles* dans ML.NET. Tous les concepts ne sont pas pertinents pour le scénario le plus simple de *prédiction avec un modèle existant*.

## <a name="model-training-concepts"></a>Concepts de l’entraînement de modèles

Ce document aborde les concepts suivants liés à l’entraînement de modèles dans ML.NET :

- [*Données*](#data) représentées sous la forme d’une interface `IDataView`.
  - Dans ML.NET, les données sont semblables à une vue SQL : il s’agit d’un jeu de données schématisé, hétérogène, immuable, analysable par un curseur et évalué tardivement. 
  - Le document [Principes de conception IDataView](https://github.com/dotnet/machinelearning/blob/master/docs/code/IDataViewDesignPrinciples.md) est une excellente source d’information sur l’interface de données.
- [*Transformateur*](#transformer) représenté sous la forme d’une interface `ITransformer`.
  - Un transformateur est un composant qui prend des données, les manipule, puis retourne de nouvelles données transformées.
  - Par exemple, vous pouvez considérer un modèle Machine Learning comme un transformateur qui prend des caractéristiques et retourne des prédictions.
  - Autre exemple : le générateur de jetons de texte prend une colonne de textes unique et génère une colonne de vecteurs avec des mots individuels extraits des textes.
- [*Lecteur de données*](#data-reader) représenté sous la forme d’une interface `IDataReader<T>`.
  - Le lecteur de données est un composant ML.NET servant à créer des données. Il prend une instance de `T` et retourne des données. 
  - Par exemple, un *TextLoader* est un `IDataReader<FileSource>`. Il prend le fichier source et génère des données. 
- [*Estimateur*](#estimator) représenté sous la forme d’une interface `IEstimator<T>`.
  - Il s’agit d’un objet qui apprend à partir des données. Le résultat de l’entraînement est un *transformateur*.
  - Vous pouvez considérer un *algorithme* de machine learning comme un estimateur qui apprend à partir de données et génère un *modèle* Machine Learning.
- [*Fonction de prédiction*](#prediction-function) représentée sous la forme d’une classe `PredictionFunction<TSrc, TDst>`.
  - La fonction de prédiction peut être considérée comme une machine qui applique un transformateur à une seule ligne, comme au moment de la prédiction.

## <a name="data"></a>Données

Dans ML.NET, les données sont semblables à une vue SQL : il s’agit d’un jeu de données schématisé, hétérogène, analysable par un curseur et évalué tardivement.

- Il a un *schéma* (instance d’une interface `ISchema`) qui contient des informations sur les colonnes de la vue de données.
  - Chaque colonne a un *nom*, un *type* et un ensemble arbitraire de *métadonnées* associés.
  - Les *métadonnées* de la colonne contiennent des informations telles que des noms d’emplacement d’une colonne de vecteurs et autres informations du même ordre. Les métadonnées elles-mêmes sont également représentées sous la forme de *données* d’une ligne qui sont propres à chaque colonne.
  - La vue de données est une source de *curseurs*. Pensez aux curseurs SQL : un curseur est un objet qui effectue une itération au sein des données, une ligne à la fois, et présente les données disponibles.
  - Naturellement, les données peuvent être parcourues par autant de curseurs actifs que nécessaires. Dans la mesure où les données proprement dites sont immuables, les curseurs sont véritablement indépendants.
  - En règle générale, les curseurs accèdent uniquement à un sous-ensemble de colonnes : pour plus d’efficacité, ML.NET calcule uniquement les valeurs de colonnes qui sont requises par le curseur.

## <a name="transformer"></a>Transformateur

Un transformateur est un composant qui prend des données, les manipule, puis retourne de nouvelles données transformées.

La plupart des transformateurs dans ML.NET ont tendance à opérer sur une *colonne d’entrée* à la fois et à produire la *colonne de sortie*. Par exemple, un `new HashTransformer("foo", "bar")` prend les valeurs de la colonne « foo », les hache et les place dans la colonne « bar ». 

Il est également courant que les noms de colonnes d’entrée et de sortie soient identiques. Dans ce cas, l’ancienne colonne est remplacée par la nouvelle. Par exemple, un `new HashTransformer("foo")` prend les valeurs de la colonne « foo », les hache et les place dans « foo ». 

Naturellement, tout transformateur génère une nouvelle vue de données quand `Transform` est appelé. N’oubliez pas que les vues de données sont immuables.

Un autre élément important est que, les données étant évaluées tardivement, les *transformateurs sont tardifs également*. Essentiellement, une fois que vous avez appelé

```csharp
var newData = transformer.Transform(oldData)
```

aucun calcul réel ne se produit. C’est seulement une fois que vous obtenez un curseur à partir de `newData` et que vous commencez à utiliser la valeur que `newData` appelle la logique de transformation `transformer` (sous réserve que le `transformer` en question soit nécessaire pour produire les colonnes demandées).

### <a name="transformer-chains"></a>Chaînes de transformateur

Une propriété utile d’un transformateur est que *vous pouvez formuler une application séquentielle de transformateurs sous la forme d’un autre transformateur* :

```csharp
var fullTransformer = transformer1.Append(transformer2).Append(transformer3);
```

Cette propriété est couramment utilisée dans ML.NET : en règle générale, le modèle ML.NET entraîné est une chaîne de transformateurs, qui est, à toutes fins pratiques, un *transformateur*. 

## <a name="data-reader"></a>Lecteur de données

Le lecteur de données est le composant ML.NET servant à « créer » des données : il prend une instance de `T` et retourne des données.

Une propriété intéressante est que vous pouvez créer un lecteur de données en attachant un transformateur à un lecteur de données existant. De cette façon, vous pouvez avoir un lecteur intégrant un comportement de transformation :

```c#
var newReader = reader.Append(transformer1).Append(transformer2)
```

Une autre similarité avec les transformateurs est que, dans la mesure où les données sont évaluées tardivement, les *lecteurs sont tardifs* : aucune (ou pratiquement aucune) « lecture » réelle ne se produit quand vous appelez `dataReader.Read()` ; le lecteur ne commence à travailler que quand un curseur est demandé sur les données résultantes.

## <a name="estimator"></a>Estimateur

L’*estimateur* est un objet qui apprend à partir des données. Le résultat de l’entraînement est un *transformateur*.

Dans ML.NET, utilisez cette propriété pour créer des pipelines d’entraînement qui chaînent différents estimateurs :

```csharp
MLContext mlContext = new MLContext(seed: 0);

var pipeline = new CopyColumnsEstimator(mlContext, "FareAmount", "Label")
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "VendorId"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "RateCode"))
.Append(mlContextml.Transforms.Categorical.OneHotEncoding(mlContext, "PaymentType"))
.Append(new ColumnConcatenatingEstimator(mlContext, "Features", "VendorId", "RateCode", "PassengerCount", "TripTime", "TripDistance", "PaymentType"))
.Append(mlContext.Regression.Trainers.FastTree("Label", "Features"));

var model = pipeline.Fit(dataView);
```

Une des propriétés importantes des estimateurs est que *les estimateurs sont hâtifs, pas tardifs* : chaque appel à `Fit` entraîne un apprentissage, opération qui peut s’avérer longue.

## <a name="prediction-function"></a>Fonction de prédiction

La fonction de prédiction peut être considérée comme une machine qui applique un transformateur à une seule ligne.

Une fois que vous obtenez le modèle (un *transformateur* entraîné par le biais de `Fit()` ou chargé), vous pouvez l’utiliser pour effectuer des prédictions à l’aide d’appels normaux à `model.Transform(data)`. Toutefois, quand vous utilisez ce modèle dans un scénario réel, vous n’avez souvent pas de nombreux exemples à partir desquels effectuer la prédiction. Au lieu de cela, vous disposez d’un exemple à la fois, et vous devez faire des prédictions en temps voulu sur ces derniers immédiatement.

Bien sûr, vous pouvez réduire la procédure à une prédiction par lot :

- Créer une vue de données avec une seule ligne.
- Appeler `model.Transform(data)` pour obtenir la vue de données prédites.
- Obtenir un curseur sur les données résultantes.
- Faire progresser le curseur d’une étape pour accéder à la première (et unique) ligne.
- Extraire les valeurs prédites.

L’algorithme précédent peut être implémenté à l’aide de la [compréhension du schéma](https://github.com/dotnet/machinelearning/blob/master/docs/code/SchemaComprehension.md), avec deux objets définis par l’utilisateur `InputExample` et `OutputPrediction` comme suit :

```c#
var inputData = env.CreateDataView(new InputExample[] { example });
var outputData = model.Transform(inputData);
var output = outputData.AsDynamic.AsEnumerable<OutputPrediction>(env, reuseRowObject: false).Single();
```

Mais cela est fastidieux et entraîne des coûts de performances. À la place, un objet de fonction de prédiction effectue le même travail, mais de façon plus rapide et pratique, par le biais d’une méthode d’extension `MakePredictionFunction` :

```c#
var predictionFunc = model.MakePredictionFunction<InputExample, OutputPrediction>(env);
var output = predictionFunc.Predict(example);
```

La fonction de prédiction est *non réentrante/thread-safe*. Si vous souhaitez effectuer des prédictions simultanément avec plusieurs threads, vous devez disposer d’une fonction de prédiction par thread.
