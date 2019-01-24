---
title: Tâches Machine Learning - ML.NET
description: Explorez les différentes tâches Machine Learning ainsi que les tâches associées prises en charge dans ML.NET.
ms.custom: seodec18
ms.date: 01/15/2019
author: jralexander
ms.openlocfilehash: 02b454d18eca36c94c27ae15665af5df2ec87905
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415700"
---
# <a name="machine-learning-tasks-in-mlnet"></a>Tâches Machine Learning dans ML.NET

Lorsque vous créez un modèle d’apprentissage automatique, vous devez tout d’abord définir ce que vous souhaitez obtenir avec vos données. Ensuite, vous pouvez choisir la tâche Machine Learning adaptée à votre situation. La liste suivante décrit les différentes tâches d’apprentissage automatique disponibles et présente certains cas d’usage courants.

> [!NOTE]
> ML.NET est actuellement en préversion. Actuellement, les tâches d’apprentissage automatique ne sont pas toutes prises en charge. Pour envoyer une requête pour une tâche particulière, signalez un problème dans le [référentiel dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues).

## <a name="binary-classification"></a>Classification binaire

Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire à laquelle des deux classes (catégories) appartient une instance de données. L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés, où chaque étiquette est un entier ayant pour valeur 0 ou 1. La sortie d’un algorithme de classification binaire est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette. Voici quelques exemples de scénarios de classification binaire :

* [Déterminer si des commentaires Twitter](../tutorials/sentiment-analysis.md) sont « positifs » ou « négatifs ».
* Diagnostiquer si un patient est atteint ou non d’une certaine maladie.
* Décider si un e-mail doit être considéré comme « spam » ou non.
* Déterminer si une photo contient un chien ou un fruit.

Pour plus d’informations, consultez l’article Wikipédia [Classification binaire](https://en.wikipedia.org/wiki/Binary_classification).

Apprenants recommandés pour la classification binaire :

* AveragedPerceptronTrainer
* StochasticGradientDescentClassificationTrainer
* LightGbmBinaryTrainer
* FastTreeBinaryClassificationTrainer
* SymSgdClassificationTrainer

### <a name="binary-classification-learners"></a>Apprenants de classification binaires

Les apprenants suivants sont disponibles pour les tâches de classification binaire :

* [AveragedPerceptronTrainer](xref:Microsoft.ML.Trainers.Online.AveragedPerceptronTrainer)
* [BinaryClassificationGamTrainer](xref:Microsoft.ML.Trainers.FastTree.BinaryClassificationGamTrainer)
* [FastForestClassification](xref:Microsoft.ML.Trainers.FastTree.FastForestClassification)
* [FastTreeBinaryClassificationTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeBinaryClassificationTrainer)
* [FieldAwareFactorizationMachineTrainer](xref:Microsoft.ML.FactorizationMachine.FieldAwareFactorizationMachineTrainer)
* [LightGbmBinaryTrainer](xref:Microsoft.ML.LightGBM.LightGbmBinaryTrainer)
* [LinearSvmTrainer](xref:Microsoft.ML.Trainers.Online.LinearSvmTrainer)
* [LogisticRegression](xref:Microsoft.ML.Learners.LogisticRegression)
* [PriorTrainer](xref:Microsoft.ML.Trainers.PriorTrainer)
* [RandomTrainer](xref:Microsoft.ML.Trainers.RandomTrainer)
* [StochasticGradientDescentClassificationTrainer](xref:Microsoft.ML.Trainers.StochasticGradientDescentClassificationTrainer)
* [SymSgdClassificationTrainer](xref:Microsoft.ML.Trainers.SymSgd.SymSgdClassificationTrainer)

## <a name="multiclass-classification"></a>Classification multiclasse

Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire la classe (catégorie) d’une instance de données. L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés. Chaque étiquette démarre normalement en tant que texte. Elle est ensuite exécutée via TermTransform, qui la convertit en un type de clé (numérique). La sortie d’un algorithme de classification est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette. Voici quelques exemples de scénarios de classification multiclasse :

* Déterminer la race d’un chien, par exemple « Husky de Sibérie », « Golden Retriever », « Caniche », etc.
* Déterminer si des critiques d’un film sont « positives », « neutres » ou « négatives ».
* Classer les évaluations d’un hôtel par « situation géographique », « prix », « propreté », etc.

Pour plus d’informations, consultez l’article Wikipédia [Classification multiclasse](https://en.wikipedia.org/wiki/Multiclass_classification).

Apprenants recommandés pour la classification multiclasse :

* OVA-AveragedPerceptronTrainer
* SdcaMultiClassTrainer
* LightGbmMulticlassTrainer
* OVA-FastTreeBinaryClassificationTrainer

>[!NOTE]
>OVA et PKPD mettent à niveau les [apprenant de classification binaire](#binary-classification) pour agir sur les jeux de données multiclasse. Pour plus d’informations, consultez l’article [Wikipédia] (https://en.wikipedia.org/wiki/Multiclass_classification#One-vs.-rest).

### <a name="multiclass-classification-learners"></a>Apprenants de classification multiclasse

Les apprenants suivants sont disponibles pour les tâches de classification multiclasse :

* [LightGbmMulticlassTrainer](xref:Microsoft.ML.LightGBM.LightGbmMulticlassTrainer)
* [MetaMulticlassTrainer<TTransformer,TModel>](xref:Microsoft.ML.Learners.MetaMulticlassTrainer%602)
* [MultiClassNaiveBayesTrainer](xref:Microsoft.ML.Trainers.MultiClassNaiveBayesTrainer)
* [Ova](xref:Microsoft.ML.Trainers.Ova)
* [Pkpd](xref:Microsoft.ML.Trainers.Pkpd)
* [SdcaMultiClassTrainer](xref:Microsoft.ML.Trainers.SdcaMultiClassTrainer)

## <a name="regression"></a>Régression

Une tâche [Apprentissage automatique supervisée](glossary.md#supervised-machine-learning) utilisée pour prédire la valeur de l’étiquette d’un ensemble de fonctionnalités connexes. L’étiquette peut avoir n’importe quelle valeur réelle et ne provient pas d’un ensemble fini de valeurs comme dans les tâches de classification. Les algorithmes de régression modèlent la dépendance de l’étiquette sur ses fonctionnalités connexes pour déterminer la façon dont l’étiquette change avec des valeurs de fonctionnalités différentes. L’entrée d’un algorithme de régression est un ensemble d’exemples avec des étiquettes de valeurs connues. La sortie d’un algorithme de régression est une fonction, que vous pouvez utiliser pour prédire la valeur de l’étiquette pour tout nouvel ensemble de fonctionnalités d’entrée. Voici quelques exemples de scénarios de régression :

* Prédire le prix d’une maison selon ses attributs, par exemple le nombre de chambres, l’emplacement ou la taille.
* Prédire le cours d’actions en fonction de données historiques et des tendances du marché actuel.
* Prédire les ventes d’un produit en fonction d’un budget publicitaire.

Apprenants recommandés pour la régression :

* FastTreeTweedieTrainer 
* LightGbmRegressorTrainer 
* SdcaRegressionTrainer 
* FastTreeRegressionTrainer

### <a name="regression-learners"></a>Apprenants de régression

Les apprenants suivants sont disponibles pour les tâches de régression :

* [FastTreeRegressionTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRegressionTrainer)
* [FastTreeTweedieTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeTweedieTrainer)
* [LightGbmRegressorTrainer](xref:Microsoft.ML.LightGBM.LightGbmRegressorTrainer)
* [OlsLinearRegressionTrainer](xref:Microsoft.ML.Trainers.HalLearners.OlsLinearRegressionTrainer)
* [OnlineGradientDescentTrainer](xref:Microsoft.ML.Trainers.Online.OnlineGradientDescentTrainer)
* [PoissonRegression](xref:Microsoft.ML.Trainers.PoissonRegression)
* [RegressionGamTrainer](xref:Microsoft.ML.Trainers.FastTree.RegressionGamTrainer)
* [SdcaRegressionTrainer](xref:Microsoft.ML.Trainers.SdcaRegressionTrainer)
* [FastTree.SingleTrainer](xref:Microsoft.ML.Trainers.FastTree.SingleTrainer)
* [LightGBM.SingleTrainer](xref:Microsoft.ML.LightGBM.SingleTrainer)

## <a name="clustering"></a>Clustering

Une tâche [Apprentissage automatique non supervisé](glossary.md#unsupervised-machine-learning) utilisée pour regrouper des instances de données dans des clusters contenant des caractéristiques similaires. Le clustering permet également d’identifier, dans un jeu de données, les relations qui peuvent ne pas être logiquement dérivées par navigation ou simple observation. Les entrées et sorties d’un algorithme de clustering dépendent de la méthode choisie. Vous pouvez adopter une approche de type distribution, centroïde, connectivité ou basée sur la densité. ML.NET prend actuellement en charge une approche de type centroïde à l’aide du clustering K-Means. Voici quelques exemples de scénarios de clustering :

* Évaluer les segments d’une clientèle d’hôtel en fonction de leurs habitudes et des caractéristiques de l’hôtel.
* Identifier les segments d’une clientèle et les données démographiques pour faciliter la mise en œuvre de campagnes publicitaires ciblées.
* Classer un inventaire en fonction de métriques de fabrication.

### <a name="clustering-learners"></a>Apprenants de clustering

Les apprenants suivants sont disponibles pour les tâches de clustering :

* [KMeansPlusPlusTrainer](xref:Microsoft.ML.Trainers.KMeans.KMeansPlusPlusTrainer)

## <a name="anomaly-detection"></a>Détection d’anomalie

Cette tâche crée un modèle de détection d’anomalie à l’aide de la méthode Principal Component Analysis (PCA). La détection d’anomalie PCA vous permet de créer un modèle dans des scénarios où il est facile d’obtenir des données d’apprentissage à partir d’une classe, notamment des transactions valides, mais où il est difficile d’obtenir suffisamment d’échantillons d’anomalies ciblées.

Technique éprouvée dans l’apprentissage automatique (Machine Learning), la méthode PCA est fréquemment utilisée dans l’analyse exploratoire des données car elle révèle la structure interne des données et explique la variance dans les données. PCA fonctionne en analysant les données contenant plusieurs variables. Elle recherche des corrélations entre les variables et détermine la combinaison de valeurs qui identifie le mieux les différences dans les résultats. Ces valeurs de fonctionnalité combinées sont utilisées pour créer un espace de fonctionnalités plus compact, appelé principaux composants.

La détection d’anomalie englobe de nombreuses tâches importantes pour l’apprentissage automatique :

* Identification des transactions potentiellement frauduleuses.
* Modèles d’apprentissage signalant une intrusion sur le réseau.
* Recherche de clusters anormaux de patients.
* Vérification des valeurs entrées dans un système.

Les anomalies constituant, par définition, des événements rares, il peut être difficile de recueillir un échantillon représentatif des données à utiliser pour la modélisation. Les algorithmes inclus dans cette catégorie ont été spécialement conçus pour relever les défis de base qu’impliquent la création et l’apprentissage des modèles à l’aide de jeux de données déséquilibrés.

### <a name="anomaly-detection-learners"></a>Apprenants de détection d’anomalie

Les apprenants suivants sont disponibles pour les tâches de détection d'anomalie :

* [RandomizedPcaTrainer](xref:Microsoft.ML.Trainers.PCA.RandomizedPcaTrainer)

## <a name="ranking"></a>Classement

Une tâche de classement établit un classement à partir d’un ensemble d’exemples étiquetés. Cet exemple d’ensemble se compose de groupes d’instances qui peuvent être évalués selon un critère donné. Les étiquettes de classement sont {0, 1, 2, 3, 4} pour chaque instance.  Le classement est formé pour trier les nouveaux groupes d’instance en attribuant un score inconnu à chaque instance. Les apprenants de classement ML.NET utilisent un [classement basé sur l’apprentissage automatique](https://en.wikipedia.org/wiki/Learning_to_rank).

### <a name="ranking-learners"></a>Apprenants de classement

Les apprenants suivants sont disponibles pour les tâches de classement :

* [FastTreeRankingTrainer](xref:Microsoft.ML.Trainers.FastTree.FastTreeRankingTrainer)
* [LightGbmRankingTrainer](xref:Microsoft.ML.LightGBM.LightGbmRankingTrainer)

## <a name="recommendation"></a>Recommandation

Une tâche de recommandation permet de dresser la liste des produits ou services recommandés. ML.NET utilise la méthode [Factorisation de matrice (MF)](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29), un algorithme de [filtrage collaboratif](https://en.wikipedia.org/wiki/Collaborative_filtering) pour obtenir des recommandations lorsque votre catalogue contient des données d’évaluation de produit historiques. Par exemple, vous disposez des données d’évaluation de films historiques pour vos utilisateurs et souhaitez leur recommander d’autres vidéos.

### <a name="recommendation-learners"></a>Apprenants de recommandation

Les apprenants suivants sont disponibles pour les tâches de recommandation :

* [MatrixFactorizationTrainer](xref:Microsoft.ML.Trainers.MatrixFactorizationTrainer)
* [MatrixFactorizationPredictionTransformer](xref:Microsoft.ML.Trainers.Recommender.MatrixFactorizationPredictionTransformer)
