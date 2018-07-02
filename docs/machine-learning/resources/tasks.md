---
title: Tâches d’apprentissage automatique
description: Explorez les différentes tâches d’apprentissage automatique prises en charge dans ML.NET.
ms.date: 06/04/2018
author: aditidugar
ms.author: johalex
ms.openlocfilehash: 22249ac2d275a4168dbd8b03b90d9698fe90f2d1
ms.sourcegitcommit: d8bf4976eafe3289275be3811e7cb721bfff7e1e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34860665"
---
# <a name="machine-learning-tasks"></a>Tâches d’apprentissage automatique

Lorsque vous créez un modèle d’apprentissage automatique, vous devez tout d’abord définir ce que vous souhaitez obtenir avec vos données. Ensuite, vous pouvez choisir la tâche d’apprentissage automatique adaptée à votre situation. La liste suivante décrit les différentes tâches d’apprentissage automatique disponibles et présente certains cas d’usage courants. 

> [!NOTE]
> ML.NET est actuellement en préversion. Actuellement, les tâches d’apprentissage automatique ne sont pas toutes prises en charge. Pour envoyer une requête pour une tâche particulière, signalez un problème dans le [référentiel dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues).

> [!NOTE]
> Actuellement, ML.NET ne prend pas en charge les tâches d’apprentissage automatique avec des images. Cette prise en charge sera ajoutée aux prochaines versions. 

## <a name="binary-classification"></a>Classification binaire

Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire à laquelle des deux classes (catégories) appartient une instance de données. L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés, où chaque étiquette est un entier ayant pour valeur 0 ou 1. La sortie d’un algorithme de classification binaire est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette. Voici quelques exemples de scénarios de classification binaire :

* [Déterminer si des commentaires Twitter](../tutorials/sentiment-analysis.md) sont « positifs » ou « négatifs ».
* Diagnostiquer si un patient est atteint ou non d’une certaine maladie.
* Décider si un e-mail doit être considéré comme « spam » ou non.

## <a name="multi-class-classification"></a>Classification multiclasse

Une tâche [Apprentissage automatique supervisé](glossary.md#supervised-machine-learning) utilisée pour prédire la classe (catégorie) d’une instance de données. L’entrée d’un algorithme de classification est un ensemble d’exemples étiquetés. Chaque étiquette est un entier compris entre 0 et k-1, où k est le nombre de classes. La sortie d’un algorithme de classification est un classifieur, que vous pouvez utiliser pour prédire la classe de nouvelles instances sans étiquette. Voici quelques exemples de scénarios de classification multiclasse :

* Déterminer la race d’un chien, par exemple « Husky de Sibérie », « Golden Retriever », « Caniche », etc.
* Déterminer si des critiques d’un film sont « positives », « neutres » ou « négatives ».
* Classer les évaluations d’un hôtel par « situation géographique », « prix », « propreté », etc.

## <a name="regression"></a>Régression

Une tâche [Apprentissage automatique supervisée](glossary.md#supervised-machine-learning) utilisée pour prédire la valeur de l’étiquette d’un ensemble de fonctionnalités connexes. L’étiquette peut avoir n’importe quelle valeur réelle et ne provient pas d’un ensemble fini de valeurs comme dans les tâches de classification. Les algorithmes de régression modèlent la dépendance de l’étiquette sur ses fonctionnalités connexes pour déterminer la façon dont l’étiquette change avec des valeurs de fonctionnalités différentes. L’entrée d’un algorithme de régression est un ensemble d’exemples avec des étiquettes de valeurs connues. La sortie d’un algorithme de régression est une fonction, que vous pouvez utiliser pour prédire la valeur de l’étiquette pour tout nouvel ensemble de fonctionnalités d’entrée. Voici quelques exemples de scénarios de régression :

* Prédire le prix d’une maison selon ses attributs, par exemple le nombre de chambres, l’emplacement ou la taille.
* Prédire le cours d’actions en fonction de données historiques et des tendances du marché actuel.
* Prédire les ventes d’un produit en fonction d’un budget publicitaire.

> [!NOTE]
> ML.NET prépare actuellement la prise en charge des tâches de régression qui impliquent des séries chronologiques.

## <a name="clustering"></a>Clustering

Une tâche [Apprentissage automatique non supervisé](glossary.md#unsupervised-machine-learning) utilisée pour regrouper des instances de données dans des clusters contenant des caractéristiques similaires. Le clustering permet également d’identifier, dans un jeu de données, les relations qui peuvent ne pas être logiquement dérivées par navigation ou simple observation. Les entrées et sorties d’un algorithme de clustering dépendent de la méthode choisie. Vous pouvez adopter une approche de type distribution, centroïde, connectivité ou basée sur la densité. ML.NET prend actuellement en charge une approche de type centroïde à l’aide du clustering K-Means. Voici quelques exemples de scénarios de clustering :

* Évaluer les segments d’une clientèle d’hôtel en fonction de leurs habitudes et des caractéristiques de l’hôtel.
* Identifier les segments d’une clientèle et les données démographiques pour faciliter la mise en œuvre de campagnes publicitaires ciblées.
* Classer un inventaire en fonction de métriques de fabrication.

## <a name="anomaly-detection-coming-soon"></a>Détection d’anomalie (*bientôt disponible*)

## <a name="ranking-coming-soon"></a>Classement (*bientôt disponible*)

## <a name="recommendation-coming-soon"></a>Suggestion (*bientôt disponible*)

