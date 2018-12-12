---
title: Guides pratiques pour l’utilisation de Machine Learning avec .NET - ML.NET
description: Découvrez comment effectuer des tâches spécifiques pour faciliter la création de solutions IA personnalisées et l’intégration de Machine Learning dans vos applications .NET.
ms.custom: seodec18
ms.date: 12/04/2018
ms.openlocfilehash: edff20b36d11dec169e1a4318a473533c8664842
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235187"
---
# <a name="net-machine-learning-how-to-guides---mlnet"></a><span data-ttu-id="8b147-103">Guides pratiques pour l’utilisation de Machine Learning avec .NET - ML.NET</span><span class="sxs-lookup"><span data-stu-id="8b147-103">.NET Machine learning how-to guides - ML.NET</span></span>

<span data-ttu-id="8b147-104">Dans la section Procédures du guide ML.NET, vous trouverez rapidement des réponses à des questions courantes.</span><span class="sxs-lookup"><span data-stu-id="8b147-104">In the How to section of the ML.NET Guide, you can find quick answers to common questions.</span></span> <span data-ttu-id="8b147-105">Dans certains cas, les articles peuvent figurer dans plusieurs sections pour les trouver facilement.</span><span class="sxs-lookup"><span data-stu-id="8b147-105">In some cases, articles may be listed in multiple sections to make them easy to find.</span></span>

## <a name="prepare-data"></a><span data-ttu-id="8b147-106">Préparer les données</span><span class="sxs-lookup"><span data-stu-id="8b147-106">Prepare data</span></span>

### <a name="load-data"></a><span data-ttu-id="8b147-107">Charger les données</span><span class="sxs-lookup"><span data-stu-id="8b147-107">Load data</span></span>

* [<span data-ttu-id="8b147-108">Charger des données avec de nombreuses colonnes à partir d’un fichier CSV pour le traitement Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="8b147-108">Load data with many columns from a CSV file for machine learning processing.</span></span>](load-data-from-mult-column-csv-ml-net.md)

* [<span data-ttu-id="8b147-109">Charger des données à partir de plusieurs fichiers pour le traitement Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="8b147-109">Load data from multiple files for machine learning processing.</span></span>](load-data-from-multiple-files-ml-net.md)

* [<span data-ttu-id="8b147-110">Charger des données à partir d’un fichier texte pour le traitement Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="8b147-110">Load data from a text file for machine learning processing.</span></span>](load-data-from-text-file-ml-net.md)

* [<span data-ttu-id="8b147-111">Prétraiter les données d’entraînement avec des normaliseurs pour les utiliser dans le traitement des données.</span><span class="sxs-lookup"><span data-stu-id="8b147-111">Preprocess training data with normalizers to use in data processing.</span></span>](normalizers-preprocess-data-ml-net.md)

## <a name="train-model"></a><span data-ttu-id="8b147-112">Former le modèle</span><span class="sxs-lookup"><span data-stu-id="8b147-112">Train model</span></span>

* [<span data-ttu-id="8b147-113">Former un modèle Machine Learning avec des données qui ne sont pas dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="8b147-113">Train a machine learning model with data that's not in a text file.</span></span>](load-non-file-training-data-ml-net.md)

* [<span data-ttu-id="8b147-114">Former un modèle Machine Learning en utilisant la validation croisée.</span><span class="sxs-lookup"><span data-stu-id="8b147-114">Train a machine learning model using cross-validation.</span></span>](train-cross-validation-ml-net.md)

* [<span data-ttu-id="8b147-115">Former un modèle de régression pour prédire une valeur à l’aide de ML.NET.</span><span class="sxs-lookup"><span data-stu-id="8b147-115">Train a regression model to predict a value using ML.NET.</span></span>](train-regression-model-ml-net.md)

### <a name="evaluate-model-quality"></a><span data-ttu-id="8b147-116">Évaluer la qualité du modèle</span><span class="sxs-lookup"><span data-stu-id="8b147-116">Evaluate model quality</span></span>

* [<span data-ttu-id="8b147-117">Calculer les métriques pour évaluer la qualité du modèle.</span><span class="sxs-lookup"><span data-stu-id="8b147-117">Calculate metrics to evaluate model quality.</span></span>](verify-model-quality-ml-net.md)

### <a name="model-explainability"></a><span data-ttu-id="8b147-118">Explication du modèle</span><span class="sxs-lookup"><span data-stu-id="8b147-118">Model explainability</span></span>

* [<span data-ttu-id="8b147-119">Déterminer l’importance des caractéristiques des modèles avec l’option Permutation Feature Importance.</span><span class="sxs-lookup"><span data-stu-id="8b147-119">Determine the feature importance of models with Permutation Feature Importance.</span></span>](determine-global-feature-importance-in-model.md)

* [<span data-ttu-id="8b147-120">Utiliser des modèles additifs généralisés et des fonctions de forme pour l’explication des modèles.</span><span class="sxs-lookup"><span data-stu-id="8b147-120">Use Generalized Additive Models and shape functions for model explainability.</span></span>](use-gams-for-model-explainability.md)

### <a name="feature-engineering"></a><span data-ttu-id="8b147-121">Ingénierie de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8b147-121">Feature engineering</span></span>

* [<span data-ttu-id="8b147-122">Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données catégoriques.</span><span class="sxs-lookup"><span data-stu-id="8b147-122">Apply feature engineering for model training on categorical data.</span></span>](train-model-categorical-ml-net.md)

* [<span data-ttu-id="8b147-123">Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données textuelles avec ML.NET.</span><span class="sxs-lookup"><span data-stu-id="8b147-123">Apply feature engineering for model training on textual data with ML.NET.</span></span>](train-model-textual-ml-net.md)

## <a name="run"></a><span data-ttu-id="8b147-124">Exécuter</span><span class="sxs-lookup"><span data-stu-id="8b147-124">Run</span></span> 

* [<span data-ttu-id="8b147-125">Inspecter les valeurs de données intermédiaires lors du traitement du pipeline ML.NET.</span><span class="sxs-lookup"><span data-stu-id="8b147-125">Inspect intermediate data values during ML.NET pipeline processing.</span></span>](inspect-intermediate-data-ml-net.md)

* [<span data-ttu-id="8b147-126">Utiliser un modèle Machine Learning formé dans des applications.</span><span class="sxs-lookup"><span data-stu-id="8b147-126">Operationalize a trained machine learning model in apps.</span></span>](consuming-model-ml-net.md)

* [<span data-ttu-id="8b147-127">Utiliser PredictionFunction pour créer une prédiction à la fois.</span><span class="sxs-lookup"><span data-stu-id="8b147-127">Use the PredictionFunction to make one prediction at a time.</span></span>](single-predict-model-ml-net.md)

## <a name="probabalistic-infernet"></a><span data-ttu-id="8b147-128">Probabiliste (Infer.NET)</span><span class="sxs-lookup"><span data-stu-id="8b147-128">Probabalistic (Infer.NET)</span></span>

* [<span data-ttu-id="8b147-129">Créer une application de tableau de matchs avec Infer.NET et la programmation probabiliste.</span><span class="sxs-lookup"><span data-stu-id="8b147-129">Create a game match up list app with Infer.NET and probabilistic programming.</span></span>](matchup-app-infer-net.md)

