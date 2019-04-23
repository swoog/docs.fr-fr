---
title: Tâches Machine Learning - ML.NET
description: Explorez les différentes tâches Machine Learning ainsi que les tâches associées prises en charge dans ML.NET.
ms.custom: seodec18
ms.date: 04/12/2019
author: natke
ms.openlocfilehash: bfed9cf12f8d539c4327549e5305415ce096e022
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59613159"
---
# <a name="machine-learning-tasks-in-mlnet"></a><span data-ttu-id="81b29-103">Tâches Machine Learning dans ML.NET</span><span class="sxs-lookup"><span data-stu-id="81b29-103">Machine learning tasks in ML.NET</span></span>

<span data-ttu-id="81b29-104">Lorsque vous créez un modèle d’apprentissage automatique, vous devez tout d’abord définir ce que vous souhaitez obtenir avec vos données.</span><span class="sxs-lookup"><span data-stu-id="81b29-104">When building a machine learning model, you first need to define what you are hoping to achieve with your data.</span></span> <span data-ttu-id="81b29-105">Ceci vous permet de choisir la tâche Machine Learning adaptée à votre situation.</span><span class="sxs-lookup"><span data-stu-id="81b29-105">This allows you to choose the right machine learning task for your situation.</span></span> <span data-ttu-id="81b29-106">La liste suivante décrit les différentes tâches d’apprentissage automatique disponibles et présente certains cas d’usage courants.</span><span class="sxs-lookup"><span data-stu-id="81b29-106">The following list describes the different machine learning tasks that you can choose from and some common use cases.</span></span>

<span data-ttu-id="81b29-107">Une fois que vous avez décidé de tâche qui fonctionne pour votre scénario, vous devez choisir le meilleur algorithme pour entraîner le modèle.</span><span class="sxs-lookup"><span data-stu-id="81b29-107">Once you have decided which task works for your scenario, then you need to choose the best algorithm to train your model.</span></span> <span data-ttu-id="81b29-108">Les algorithmes disponibles sont listés dans la section pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="81b29-108">The available algorithms are listed in the section for each task.</span></span>

## <a name="binary-classification"></a><span data-ttu-id="81b29-109">Classification binaire</span><span class="sxs-lookup"><span data-stu-id="81b29-109">Binary classification</span></span>

<span data-ttu-id="81b29-110">Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire à laquelle des deux classes (catégories) appartient une instance de données.</span><span class="sxs-lookup"><span data-stu-id="81b29-110">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict which of two classes (categories) an instance of data belongs to.</span></span> <span data-ttu-id="81b29-111">L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés, où chaque étiquette est un entier ayant pour valeur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="81b29-111">The input of a classification algorithm is a set of labeled examples, where each label is an integer of either 0 or 1.</span></span> <span data-ttu-id="81b29-112">La sortie d’un algorithme de classification binaire est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette.</span><span class="sxs-lookup"><span data-stu-id="81b29-112">The output of a binary classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="81b29-113">Voici quelques exemples de scénarios de classification binaire :</span><span class="sxs-lookup"><span data-stu-id="81b29-113">Examples of binary classification scenarios include:</span></span>

* <span data-ttu-id="81b29-114">[Déterminer si des commentaires Twitter](../tutorials/sentiment-analysis.md) sont « positifs » ou « négatifs ».</span><span class="sxs-lookup"><span data-stu-id="81b29-114">[Understanding sentiment of Twitter comments](../tutorials/sentiment-analysis.md) as either "positive" or "negative".</span></span>
* <span data-ttu-id="81b29-115">Diagnostiquer si un patient est atteint ou non d’une certaine maladie.</span><span class="sxs-lookup"><span data-stu-id="81b29-115">Diagnosing whether a patient has a certain disease or not.</span></span>
* <span data-ttu-id="81b29-116">Décider si un e-mail doit être considéré comme « spam » ou non.</span><span class="sxs-lookup"><span data-stu-id="81b29-116">Making a decision to mark an email as "spam" or not.</span></span>
* <span data-ttu-id="81b29-117">Déterminer si une photo contient un chien ou un fruit.</span><span class="sxs-lookup"><span data-stu-id="81b29-117">Determining if a photo contains a dog or fruit.</span></span>

<span data-ttu-id="81b29-118">Pour plus d’informations, consultez l’article Wikipédia [Classification binaire](https://en.wikipedia.org/wiki/Binary_classification).</span><span class="sxs-lookup"><span data-stu-id="81b29-118">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

### <a name="binary-classification-training-algorithms"></a><span data-ttu-id="81b29-119">Algorithmes d’entraînement de classification binaire</span><span class="sxs-lookup"><span data-stu-id="81b29-119">Binary Classification Training Algorithms</span></span>

<span data-ttu-id="81b29-120">Vous pouvez entraîner un modèle de classification binaire en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-120">You can train a binary classification model using the following algorithms:</span></span>

* <xref:Microsoft.ML.Trainers.AveragedPerceptronTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.GamBinaryTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.FastForestBinaryTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryTrainer>
* <xref:Microsoft.ML.Trainers.FieldAwareFactorizationMachineTrainer>
* <xref:Microsoft.ML.Trainers.LightGbm.LightGbmBinaryTrainer>
* <xref:Microsoft.ML.Trainers.LinearSvmTrainer>
* <xref:Microsoft.ML.Trainers.LbfgsLogisticRegressionBinaryTrainer>
* <xref:Microsoft.ML.Trainers.PriorTrainer>
* <xref:Microsoft.ML.Trainers.SdcaLogisticRegressionBinaryTrainer>
* <xref:Microsoft.ML.Trainers.SdcaNonCalibratedBinaryTrainer>
* <xref:Microsoft.ML.Trainers.SymbolicSgdLogisticRegressionBinaryTrainer>

## <a name="multiclass-classification"></a><span data-ttu-id="81b29-121">Classification multiclasse</span><span class="sxs-lookup"><span data-stu-id="81b29-121">Multiclass classification</span></span>

<span data-ttu-id="81b29-122">Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire la classe (catégorie) d’une instance de données.</span><span class="sxs-lookup"><span data-stu-id="81b29-122">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the class (category) of an instance of data.</span></span> <span data-ttu-id="81b29-123">L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés.</span><span class="sxs-lookup"><span data-stu-id="81b29-123">The input of a classification algorithm is a set of labeled examples.</span></span> <span data-ttu-id="81b29-124">Chaque étiquette démarre normalement en tant que texte.</span><span class="sxs-lookup"><span data-stu-id="81b29-124">Each label normally starts as text.</span></span> <span data-ttu-id="81b29-125">Elle est ensuite exécutée via TermTransform, qui la convertit en un type de clé (numérique).</span><span class="sxs-lookup"><span data-stu-id="81b29-125">It is then run through the TermTransform, which converts it to the Key (numeric) type.</span></span> <span data-ttu-id="81b29-126">La sortie d’un algorithme de classification est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette.</span><span class="sxs-lookup"><span data-stu-id="81b29-126">The output of a classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="81b29-127">Voici quelques exemples de scénarios de classification multiclasse :</span><span class="sxs-lookup"><span data-stu-id="81b29-127">Examples of multi-class classification scenarios include:</span></span>

* <span data-ttu-id="81b29-128">Déterminer la race d’un chien, par exemple « Husky de Sibérie », « Golden Retriever », « Caniche », etc.</span><span class="sxs-lookup"><span data-stu-id="81b29-128">Determining the breed of a dog as a "Siberian Husky", "Golden Retriever", "Poodle", etc.</span></span>
* <span data-ttu-id="81b29-129">Déterminer si des critiques d’un film sont « positives », « neutres » ou « négatives ».</span><span class="sxs-lookup"><span data-stu-id="81b29-129">Understanding movie reviews as "positive", "neutral", or "negative".</span></span>
* <span data-ttu-id="81b29-130">Classer les évaluations d’un hôtel par « situation géographique », « prix », « propreté », etc.</span><span class="sxs-lookup"><span data-stu-id="81b29-130">Categorizing hotel reviews as "location", "price", "cleanliness", etc.</span></span>

<span data-ttu-id="81b29-131">Pour plus d’informations, consultez l’article Wikipédia [Classification multiclasse](https://en.wikipedia.org/wiki/Multiclass_classification).</span><span class="sxs-lookup"><span data-stu-id="81b29-131">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

>[!NOTE]
><span data-ttu-id="81b29-132">OvA (One vs all, Un comparé à tous) met à niveau les [learners de classification binaire](#binary-classification) pour agir sur les jeux de données multiclasses.</span><span class="sxs-lookup"><span data-stu-id="81b29-132">One vs all upgrades any [binary classification learner](#binary-classification) to act on multiclass datasets.</span></span> <span data-ttu-id="81b29-133">Pour plus d’informations, consultez l’article [Wikipédia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).</span><span class="sxs-lookup"><span data-stu-id="81b29-133">More information on [Wikipedia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).</span></span>

### <a name="multiclass-classification-training-algorithms"></a><span data-ttu-id="81b29-134">Algorithmes d’entraînement de classification multiclasse</span><span class="sxs-lookup"><span data-stu-id="81b29-134">Multiclass Classification training algorithms</span></span>

<span data-ttu-id="81b29-135">Vous pouvez entraîner un modèle de classification multiclasse en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-135">You can train a multiclass classification model using the following training algorithms:</span></span>

* <xref:Microsoft.ML.Trainers.LbfgsMaximumEntropyMulticlassTrainer>
* <xref:Microsoft.ML.Trainers.LightGbm.LightGbmMulticlassTrainer>
* <xref:Microsoft.ML.Trainers.NaiveBayesMulticlassTrainer>
* <xref:Microsoft.ML.Trainers.OneVersusAllTrainer>
* <xref:Microsoft.ML.Trainers.SdcaMaximumEntropyMulticlassTrainer>
* <xref:Microsoft.ML.Trainers.SdcaNonCalibratedMulticlassTrainer>
* <xref:Microsoft.ML.Trainers.PairwiseCouplingTrainer>

## <a name="regression"></a><span data-ttu-id="81b29-136">Régression</span><span class="sxs-lookup"><span data-stu-id="81b29-136">Regression</span></span>

<span data-ttu-id="81b29-137">Une tâche [Apprentissage automatique supervisée](glossary.md#supervised-machine-learning) utilisée pour prédire la valeur de l’étiquette d’un ensemble de fonctionnalités connexes.</span><span class="sxs-lookup"><span data-stu-id="81b29-137">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the value of the label from a set of related features.</span></span> <span data-ttu-id="81b29-138">L’étiquette peut avoir n’importe quelle valeur réelle et ne provient pas d’un ensemble fini de valeurs comme dans les tâches de classification.</span><span class="sxs-lookup"><span data-stu-id="81b29-138">The label can be of any real value and is not from a finite set of values as in classification tasks.</span></span> <span data-ttu-id="81b29-139">Les algorithmes de régression modèlent la dépendance de l’étiquette sur ses fonctionnalités connexes pour déterminer la façon dont l’étiquette change avec des valeurs de fonctionnalités différentes.</span><span class="sxs-lookup"><span data-stu-id="81b29-139">Regression algorithms model the dependency of the label on its related features to determine how the label will change as the values of the features are varied.</span></span> <span data-ttu-id="81b29-140">L’entrée d’un algorithme de régression est un ensemble d’exemples avec des étiquettes de valeurs connues.</span><span class="sxs-lookup"><span data-stu-id="81b29-140">The input of a regression algorithm is a set of examples with labels of known values.</span></span> <span data-ttu-id="81b29-141">La sortie d’un algorithme de régression est une fonction, que vous pouvez utiliser pour prédire la valeur de l’étiquette pour tout nouvel ensemble de fonctionnalités d’entrée.</span><span class="sxs-lookup"><span data-stu-id="81b29-141">The output of a regression algorithm is a function, which you can use to predict the label value for any new set of input features.</span></span> <span data-ttu-id="81b29-142">Voici quelques exemples de scénarios de régression :</span><span class="sxs-lookup"><span data-stu-id="81b29-142">Examples of regression scenarios include:</span></span>

* <span data-ttu-id="81b29-143">Prédire le prix d’une maison selon ses attributs, par exemple le nombre de chambres, l’emplacement ou la taille.</span><span class="sxs-lookup"><span data-stu-id="81b29-143">Predicting house prices based on house attributes such as number of bedrooms, location, or size.</span></span>
* <span data-ttu-id="81b29-144">Prédire le cours d’actions en fonction de données historiques et des tendances du marché actuel.</span><span class="sxs-lookup"><span data-stu-id="81b29-144">Predicting future stock prices based on historical data and current market trends.</span></span>
* <span data-ttu-id="81b29-145">Prédire les ventes d’un produit en fonction d’un budget publicitaire.</span><span class="sxs-lookup"><span data-stu-id="81b29-145">Predicting sales of a product based on advertising budgets.</span></span>

### <a name="regression-training-algorithms"></a><span data-ttu-id="81b29-146">Algorithmes d’entraînement de régression</span><span class="sxs-lookup"><span data-stu-id="81b29-146">Regression training algorithms</span></span>

<span data-ttu-id="81b29-147">Vous pouvez entraîner un modèle de régression en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-147">You can train a regression model using the following algorithms:</span></span>

* <xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.FastForestRegressionTrainer>
* <xref:Microsoft.ML.Trainers.LightGbm.LightGbmRegressionTrainer>
* <xref:Microsoft.ML.Trainers.OlsTrainer>
* <xref:Microsoft.ML.Trainers.OnlineGradientDescentTrainer>
* <xref:Microsoft.ML.Trainers.LbfgsPoissonRegressionTrainer>
* <xref:Microsoft.ML.Trainers.FastTree.GamRegressionTrainer>
* <xref:Microsoft.ML.Trainers.SdcaRegressionTrainer>

## <a name="clustering"></a><span data-ttu-id="81b29-148">Clustering</span><span class="sxs-lookup"><span data-stu-id="81b29-148">Clustering</span></span>

<span data-ttu-id="81b29-149">Une tâche [Apprentissage automatique non supervisé](glossary.md#unsupervised-machine-learning) utilisée pour regrouper des instances de données dans des clusters contenant des caractéristiques similaires.</span><span class="sxs-lookup"><span data-stu-id="81b29-149">An [unsupervised machine learning](glossary.md#unsupervised-machine-learning) task that is used to group instances of data into clusters that contain similar characteristics.</span></span> <span data-ttu-id="81b29-150">Le clustering permet également d’identifier, dans un jeu de données, les relations qui peuvent ne pas être logiquement dérivées par navigation ou simple observation.</span><span class="sxs-lookup"><span data-stu-id="81b29-150">Clustering can also be used to identify relationships in a dataset that you might not logically derive by browsing or simple observation.</span></span> <span data-ttu-id="81b29-151">Les entrées et sorties d’un algorithme de clustering dépendent de la méthode choisie.</span><span class="sxs-lookup"><span data-stu-id="81b29-151">The inputs and outputs of a clustering algorithm depends on the methodology chosen.</span></span> <span data-ttu-id="81b29-152">Vous pouvez adopter une approche de type distribution, centroïde, connectivité ou basée sur la densité.</span><span class="sxs-lookup"><span data-stu-id="81b29-152">You can take a distribution, centroid, connectivity, or density-based approach.</span></span> <span data-ttu-id="81b29-153">ML.NET prend actuellement en charge une approche de type centroïde à l’aide du clustering K-Means.</span><span class="sxs-lookup"><span data-stu-id="81b29-153">ML.NET currently supports a centroid-based approach using K-Means clustering.</span></span> <span data-ttu-id="81b29-154">Voici quelques exemples de scénarios de clustering :</span><span class="sxs-lookup"><span data-stu-id="81b29-154">Examples of clustering scenarios include:</span></span>

* <span data-ttu-id="81b29-155">Évaluer les segments d’une clientèle d’hôtel en fonction de leurs habitudes et des caractéristiques de l’hôtel.</span><span class="sxs-lookup"><span data-stu-id="81b29-155">Understanding segments of hotel guests based on habits and characteristics of hotel choices.</span></span>
* <span data-ttu-id="81b29-156">Identifier les segments d’une clientèle et les données démographiques pour faciliter la mise en œuvre de campagnes publicitaires ciblées.</span><span class="sxs-lookup"><span data-stu-id="81b29-156">Identifying customer segments and demographics to help build targeted advertising campaigns.</span></span>
* <span data-ttu-id="81b29-157">Classer un inventaire en fonction de métriques de fabrication.</span><span class="sxs-lookup"><span data-stu-id="81b29-157">Categorizing inventory based on manufacturing metrics.</span></span>

### <a name="clustering-training-algorithms"></a><span data-ttu-id="81b29-158">Algorithmes d’entraînement de clustering</span><span class="sxs-lookup"><span data-stu-id="81b29-158">Clustering training algorithms</span></span>

<span data-ttu-id="81b29-159">Vous pouvez entraîner un modèle de clustering en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-159">You can train a clustering model using the following algorithm:</span></span>

* <xref:Microsoft.ML.Trainers.KMeansTrainer>

## <a name="anomaly-detection"></a><span data-ttu-id="81b29-160">Détection d’anomalie</span><span class="sxs-lookup"><span data-stu-id="81b29-160">Anomaly detection</span></span>

<span data-ttu-id="81b29-161">Cette tâche crée un modèle de détection d’anomalie à l’aide de la méthode Principal Component Analysis (PCA).</span><span class="sxs-lookup"><span data-stu-id="81b29-161">This task creates an anomaly detection model by using Principal Component Analysis (PCA).</span></span> <span data-ttu-id="81b29-162">La détection d’anomalie PCA vous permet de créer un modèle dans des scénarios où il est facile d’obtenir des données d’apprentissage à partir d’une classe, notamment des transactions valides, mais où il est difficile d’obtenir suffisamment d’échantillons d’anomalies ciblées.</span><span class="sxs-lookup"><span data-stu-id="81b29-162">PCA-Based Anomaly Detection helps you build a model in scenarios where it is easy to obtain training data from one class, such as valid transactions, but difficult to obtain sufficient samples of the targeted anomalies.</span></span>

<span data-ttu-id="81b29-163">Technique éprouvée dans l’apprentissage automatique (Machine Learning), la méthode PCA est fréquemment utilisée dans l’analyse exploratoire des données car elle révèle la structure interne des données et explique la variance dans les données.</span><span class="sxs-lookup"><span data-stu-id="81b29-163">An established technique in machine learning, PCA is frequently used in exploratory data analysis because it reveals the inner structure of the data and explains the variance in the data.</span></span> <span data-ttu-id="81b29-164">PCA fonctionne en analysant les données contenant plusieurs variables.</span><span class="sxs-lookup"><span data-stu-id="81b29-164">PCA works by analyzing data that contains multiple variables.</span></span> <span data-ttu-id="81b29-165">Elle recherche des corrélations entre les variables et détermine la combinaison de valeurs qui identifie le mieux les différences dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="81b29-165">It looks for correlations among the variables and determines the combination of values that best captures differences in outcomes.</span></span> <span data-ttu-id="81b29-166">Ces valeurs de fonctionnalité combinées sont utilisées pour créer un espace de fonctionnalités plus compact, appelé principaux composants.</span><span class="sxs-lookup"><span data-stu-id="81b29-166">These combined feature values are used to create a more compact feature space called the principal components.</span></span>

<span data-ttu-id="81b29-167">La détection d’anomalie englobe de nombreuses tâches importantes pour l’apprentissage automatique :</span><span class="sxs-lookup"><span data-stu-id="81b29-167">Anomaly detection encompasses many important tasks in machine learning:</span></span>

* <span data-ttu-id="81b29-168">Identification des transactions potentiellement frauduleuses.</span><span class="sxs-lookup"><span data-stu-id="81b29-168">Identifying transactions that are potentially fraudulent.</span></span>
* <span data-ttu-id="81b29-169">Modèles d’apprentissage signalant une intrusion sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="81b29-169">Learning patterns that indicate that a network intrusion has occurred.</span></span>
* <span data-ttu-id="81b29-170">Recherche de clusters anormaux de patients.</span><span class="sxs-lookup"><span data-stu-id="81b29-170">Finding abnormal clusters of patients.</span></span>
* <span data-ttu-id="81b29-171">Vérification des valeurs entrées dans un système.</span><span class="sxs-lookup"><span data-stu-id="81b29-171">Checking values entered into a system.</span></span>

<span data-ttu-id="81b29-172">Les anomalies constituant, par définition, des événements rares, il peut être difficile de recueillir un échantillon représentatif des données à utiliser pour la modélisation.</span><span class="sxs-lookup"><span data-stu-id="81b29-172">Because anomalies are rare events by definition, it can be difficult to collect a representative sample of data to use for modeling.</span></span> <span data-ttu-id="81b29-173">Les algorithmes inclus dans cette catégorie ont été spécialement conçus pour relever les défis de base qu’impliquent la création et l’apprentissage des modèles à l’aide de jeux de données déséquilibrés.</span><span class="sxs-lookup"><span data-stu-id="81b29-173">The algorithms included in this category have been especially designed to address the core challenges of building and training models by using imbalanced data sets.</span></span>

### <a name="anomaly-detection-training-algorithms"></a><span data-ttu-id="81b29-174">Algorithmes d’entraînement de détection d’anomalie</span><span class="sxs-lookup"><span data-stu-id="81b29-174">Anomaly detection training algorithms</span></span>

<span data-ttu-id="81b29-175">Vous pouvez entraîner un modèle de détection d’anomalie en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-175">You can train an anomaly detection model using the following algorithm:</span></span>

* <xref:Microsoft.ML.Trainers.RandomizedPcaTrainer>

## <a name="ranking"></a><span data-ttu-id="81b29-176">Classement</span><span class="sxs-lookup"><span data-stu-id="81b29-176">Ranking</span></span>

<span data-ttu-id="81b29-177">Une tâche de classement établit un classement à partir d’un ensemble d’exemples étiquetés.</span><span class="sxs-lookup"><span data-stu-id="81b29-177">A ranking task constructs a ranker from a set of labeled examples.</span></span> <span data-ttu-id="81b29-178">Cet exemple d’ensemble se compose de groupes d’instances qui peuvent être évalués selon un critère donné.</span><span class="sxs-lookup"><span data-stu-id="81b29-178">This example set consists of instance groups that can be scored with a given criteria.</span></span> <span data-ttu-id="81b29-179">Les étiquettes de classement sont {0, 1, 2, 3, 4} pour chaque instance.</span><span class="sxs-lookup"><span data-stu-id="81b29-179">The ranking labels are { 0, 1, 2, 3, 4 } for each instance.</span></span>  <span data-ttu-id="81b29-180">Le classement est formé pour trier les nouveaux groupes d’instance en attribuant un score inconnu à chaque instance.</span><span class="sxs-lookup"><span data-stu-id="81b29-180">The ranker is trained to rank new instance groups with unknown scores for each instance.</span></span> <span data-ttu-id="81b29-181">Les apprenants de classement ML.NET utilisent un [classement basé sur l’apprentissage automatique](https://en.wikipedia.org/wiki/Learning_to_rank).</span><span class="sxs-lookup"><span data-stu-id="81b29-181">ML.NET ranking learners are [machine learned ranking](https://en.wikipedia.org/wiki/Learning_to_rank) based.</span></span>

### <a name="ranking-training-algorithms"></a><span data-ttu-id="81b29-182">Algorithmes d’entraînement de classement</span><span class="sxs-lookup"><span data-stu-id="81b29-182">Ranking training algorithms</span></span>

<span data-ttu-id="81b29-183">Vous pouvez entraîner un modèle de classement en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-183">You can train a ranking model with the following algorithms:</span></span>

* <xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer>
* <xref:Microsoft.ML.Trainers.LightGbm.LightGbmRankingTrainer>

## <a name="recommendation"></a><span data-ttu-id="81b29-184">Recommandation</span><span class="sxs-lookup"><span data-stu-id="81b29-184">Recommendation</span></span>

<span data-ttu-id="81b29-185">Une tâche de recommandation permet de dresser la liste des produits ou services recommandés.</span><span class="sxs-lookup"><span data-stu-id="81b29-185">A recommendation task enables producing a list of recommended products or services.</span></span> <span data-ttu-id="81b29-186">ML.NET utilise la méthode [Factorisation de matrice (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), un algorithme de [filtrage collaboratif](https://en.wikipedia.org/wiki/Collaborative_filtering) pour obtenir des recommandations lorsque votre catalogue contient des données d’évaluation de produit historiques.</span><span class="sxs-lookup"><span data-stu-id="81b29-186">ML.NET uses [Matrix factorization (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), a [collaborative filtering](https://en.wikipedia.org/wiki/Collaborative_filtering) algorithm for recommendations when you have historical product rating data in your catalog.</span></span> <span data-ttu-id="81b29-187">Par exemple, vous disposez des données d’évaluation de films historiques pour vos utilisateurs et souhaitez leur recommander d’autres vidéos.</span><span class="sxs-lookup"><span data-stu-id="81b29-187">For example, you have historical movie rating data for your users and want to recommend  other movies they are likely to watch next.</span></span>

### <a name="recommendation-training-algorithms"></a><span data-ttu-id="81b29-188">Algorithmes d’entraînement de recommandation</span><span class="sxs-lookup"><span data-stu-id="81b29-188">Recommendation training algorithms</span></span>

<span data-ttu-id="81b29-189">Vous pouvez entraîner un modèle de recommandation en utilisant les algorithmes suivants :</span><span class="sxs-lookup"><span data-stu-id="81b29-189">You can train a recommendation model with the following algorithm:</span></span>

* <xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer>
