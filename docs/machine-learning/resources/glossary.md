---
title: Glossaire Machine Learning - ML.NET
description: La liste suivante est une compilation des principaux termes Machine Learning, utiles lorsque vous générez vos modèles personnalisés.
ms.custom: seodec18
ms.date: 12/06/2018
ms.openlocfilehash: 4db28a62fccca2e8bedc9f48485a61b6f4ab1801
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53150574"
---
# <a name="machine-learning-glossary-of-important-terms"></a>Glossaire Machine Learning des principaux termes

La liste suivante est une compilation des principaux termes Machine Learning, utiles lorsque vous générez vos modèles personnalisés dans ML.NET.

## <a name="accuracy"></a>Précision

Dans la [classification](#classification), la précision correspond au nombre d’éléments correctement classifiés, divisé par le nombre total d’éléments dans le jeu de test. Cette valeur est comprise entre 0 (la moins précise) et 1 (la plus précise). La précision est une des métriques d’évaluation des performances de votre modèle. Utilisez-la conjointement avec les options [précision](#precision), [rappel](#recall) et [F-score](#f-score).

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.Accuracy?displayProperty=nameWithType>.

## <a name="area-under-the-curve-auc"></a>Zone sous la courbe (AUC)

Dans la [classification binaire](#binary-classification), une métrique d’évaluation qui correspond à la valeur de la zone sous la courbe qui trace le taux de vrais positifs (sur l’axe des y) par rapport au taux de faux positifs (sur l’axe des x). Cette valeur est comprise entre 0,5 (pire) et 1 (meilleur). Également appelée zone sous la courbe ROC (Receiver Operating Characteristic). Pour plus d’informations, consultez l’article Wikipédia [Courbe ROC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic).

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.Auc?displayProperty=nameWithType>.

## <a name="binary-classification"></a>Classification binaire

Cas de [classification](#classification) où l’[étiquette](#label) provient uniquement d’une de deux classes. Pour plus d’informations, consultez la section [Classification binaire](tasks.md#binary-classification) de la rubrique [Tâches d’apprentissage automatique](tasks.md).

## <a name="classification"></a>Classification

Lorsque les données sont utilisées pour prédire une catégorie, la tâche [Apprentissage automatique supervisé](#supervised-machine-learning) est appelée classification. [Classification binaire](#binary-classification) fait référence à la prédiction de deux catégories uniquement (par exemple, la classification d’une image en tant qu’image de « chat » ou de « chien »). [Classification multiclasse](#multiclass-classification) fait référence à la prédiction de plusieurs catégories (par exemple, lors de la classification d’une image en tant qu’image d’une race spécifique de chien).

## <a name="coefficient-of-determination"></a>Coefficient de détermination

Dans une [régression](#regression), une métrique d’évaluation qui indique la manière dont les données s’intègrent à un modèle. Cette valeur est comprise entre 0 et 1. Une valeur de 0 signifie que les données sont aléatoires ou ne s’intègrent pas au modèle. Une valeur de 1 signifie que le modèle correspond exactement aux données. Cette valeur est souvent désignée sous le terme r<sup>2</sup>, R<sup>2</sup> ou R carré.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.RegressionMetrics.RSquared?displayProperty=nameWithType>.

## <a name="feature"></a>Fonctionnalité

Propriété mesurable du phénomène mesuré, en général, une valeur (double) numérique. Plusieurs fonctionnalités sont appelées **vecteur de fonctionnalité** et sont généralement stockées en tant que `double[]`. Les fonctionnalités définissent les principales caractéristiques du phénomène mesuré. Pour plus d’informations, consultez l’article Wikipédia [Fonctionnalité](https://en.wikipedia.org/wiki/Feature_(machine_learning)).

## <a name="feature-engineering"></a>Ingénierie de fonctionnalité

L’ingénierie de fonctionnalité est le processus qui consiste à définir un ensemble de [fonctionnalités](#feature) et à développer des logiciels qui produisent des vecteurs de fonctionnalité à partir des données de phénomène disponibles, par exemple, l’extraction d’une fonctionnalité. Pour plus d’informations, consultez l’article Wikipédia [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering).

## <a name="f-score"></a>F-score

Dans une [classification](#classification), une métrique d’évaluation qui équilibre [précision](#precision) et [rappel](#recall).

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.F1Score?displayProperty=nameWithType>.

## <a name="hyperparameter"></a>Hyperparamètre

Un paramètre d’un algorithme d’apprentissage automatique. Par exemple, le nombre d’arbres à assimiler dans une forêt décisionnelle ou la taille d’étape dans un algorithme de jambage descendant dégradé. Les valeurs des *hyperparamètres* sont définies avant l’apprentissage du modèle et régissent le processus de recherche des paramètres de la fonction de prédiction, par exemple, les points de comparaison dans un arbre de décision ou les pondérations dans un modèle de régression linéaire. Pour plus d’informations, consultez l’article Wikipédia [Hyperparamètre](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)).

## <a name="label"></a>Etiquette

L’élément à prédire avec le modèle d’apprentissage automatique. Par exemple, la race d’un chien ou le futur cours d’une action.

## <a name="log-loss"></a>Perte du journal

Dans une [classification](#classification), une métrique d’évaluation qui caractérise la précision d’un classifieur. Plus la perte du journal est faible, plus un classifieur est précis.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.LogLoss?displayProperty=nameWithType>.

## <a name="mean-absolute-error-mae"></a>Erreur d'absolue moyenne

Dans une [régression](#regression), une métrique d’évaluation qui représente la moyenne de toutes les erreurs du modèle, où l’erreur de modèle est la distance entre la valeur d’[étiquette](#label) prédite et la valeur d’étiquette correcte.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.RegressionMetrics.L1?displayProperty=nameWithType>.

## <a name="model"></a>Modèle

En règle générale, les paramètres de la fonction de prédiction. Par exemple, les pondérations dans un modèle de régression linéaire ou les points de fractionnement dans un arbre de décision. Dans ML.NET, un modèle contient toutes les informations nécessaires pour prédire l’[étiquette](#label) d’un objet de domaine (par exemple, une image ou un texte). Cela signifie que les modèles ML.NET incluent les étapes de fonctionnalisation nécessaires ainsi que les paramètres de la fonction de prédiction.

## <a name="multiclass-classification"></a>Classification multiclasse

Cas de [classification](#classification) où l’[étiquette](#label) provient d’une de trois classes ou plus. Pour plus d’informations, consultez la section [Classification multiclasse](tasks.md#multiclass-classification) de la rubrique [Tâches d’apprentissage automatique](tasks.md).

## <a name="n-gram"></a>N-gramme

Un schéma d’extraction de fonctionnalité pour les données texte : toute séquence de N termes se transforme en une valeur [fonctionnalité](#feature).

## <a name="numerical-feature-vector"></a>Vecteur de fonctionnalité numérique

Un vecteur de [fonctionnalité](#feature) constitué uniquement de valeurs numériques. Cette valeur est similaire à `double[]`.

## <a name="pipeline"></a>Pipeline

Toutes les opérations nécessaires pour adapter un modèle à un jeu de données. Un pipeline se compose des étapes d’importation, de transformation, de fonctionnalisation et d’apprentissage des données. Une fois son apprentissage terminé, le pipeline se transforme en modèle.

## <a name="precision"></a>Précision

Dans une [classification](#classification), la précision d’une classe correspond au nombre d’éléments correctement prévus comme appartenant à cette classe, divisé par le nombre total d’éléments prévus comme appartenant à la classe.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.NegativePrecision?displayProperty=nameWithType>, <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.PositivePrecision?displayProperty=nameWithType>.

## <a name="recall"></a>Rappel

Dans une [classification](#classification), le rappel d’une classe correspond au nombre d’éléments correctement prévus comme appartenant à cette classe, divisé par le nombre total d’éléments appartenant effectivement à la classe.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.NegativeRecall?displayProperty=nameWithType>, <xref:Microsoft.ML.Legacy.Models.BinaryClassificationMetrics.PositiveRecall?displayProperty=nameWithType>.

## <a name="regression"></a>Régression

Une tâche [Apprentissage automatique supervisé](#supervised-machine-learning) où la sortie est une valeur réelle, par exemple, double. Exemple : prédiction de cours d’actions. Pour plus d’informations, consultez la section [Régression](tasks.md#regression) de la rubrique [Tâches d’apprentissage automatique](tasks.md).

## <a name="relative-absolute-error"></a>Erreur absolue relative

Dans une [régression](#regression), une métrique d’évaluation correspondant à la somme de toutes les erreurs absolues, divisée par la somme des distances entre les valeurs d’[étiquette](#label) correctes et la moyenne de toutes les valeurs d’étiquette correctes.

## <a name="relative-squared-error"></a>Erreur quadratique relative

Dans une [régression](#regression), une métrique d’évaluation correspondant à la somme de toutes les erreurs absolues quadratiques, divisée par la somme des distances quadratiques entre les valeurs d’[étiquette](#label) correctes et la moyenne de toutes les valeurs d’étiquette correctes.

## <a name="root-of-mean-squared-error-rmse"></a>Racine de l’erreur quadratique moyenne (RMSE)

Dans une [régression](#regression), une métrique d’évaluation correspondant à la racine carrée de la moyenne des carrés des erreurs.

API ML.NET connexe : <xref:Microsoft.ML.Legacy.Models.RegressionMetrics.Rms?displayProperty=nameWithType>.

## <a name="supervised-machine-learning"></a>Apprentissage automatique supervisé

Une sous-classe d’apprentissage automatique dans laquelle un modèle souhaité prévoit l’étiquette pour les données encore invisibles. Exemples : classification, régression et prédiction structurée. Pour plus d’informations, consultez l’article Wikipédia [Apprentissage supervisé](https://en.wikipedia.org/wiki/Supervised_learning).

## <a name="training"></a>Formation

Le processus d’identification d’un [modèle](#model) pour un jeu de données d’apprentissage spécifique. Pour un modèle linéaire, cela signifie rechercher les pondérations. Pour un arbre, cette opération implique l’identification des points de fractionnement.

## <a name="transform"></a>Transformer

Un composant de [pipeline](#pipeline) qui transforme les données. Par exemple, d’un texte à un vecteur de valeurs numériques.

## <a name="unsupervised-machine-learning"></a>Apprentissage automatique non supervisé

Une sous-classe d’apprentissage automatique dans laquelle un modèle souhaité trouve une structure masquée (ou latente) dans les données. Exemples : clustering, modélisation de rubrique et réduction de dimensionnalité. Pour plus d’informations, consultez l’article Wikipédia [Apprentissage non supervisé](https://en.wikipedia.org/wiki/Unsupervised_learning).
