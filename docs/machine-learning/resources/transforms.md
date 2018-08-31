---
title: Transformations de données
description: Explorez les différentes transformations de données prises en charge dans ML.NET.
ms.date: 08/08/2018
author: jralexander
ms.author: johalex
ms.openlocfilehash: 3c483f4a263052eb15435775a47f514893eee049
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000867"
---
# <a name="data-transforms"></a>Transformations de données

Les tableaux suivants contiennent des informations sur toutes les transformations de données prises en charge dans ML.NET (sélectionnez le type de transformation de données pour accéder au tableau correspondant) :

* [Catégorie](#categorical)
* [Combinaison et ségrégation](#combiners-and-segregators)
* [Sélection de caractéristique](#feature-selection)
* [Personnaliseurs](#featurizers)
* [Analyse d’étiquette](#label-parsing)
* [Valeurs manquantes](#missing-values)
* [Normalisation](#normalization)
* [Filtres de lignes](#row-filters)
* [Schéma](#schema)
* [Traitement de texte et personnalisation](#text-processing-and-featurization)
* [Divers](#miscellaneous)

> [!NOTE]
> ML.NET est actuellement en préversion. Les transformations de données ne sont pas toutes prises en charge actuellement. Pour envoyer une requête pour une transformation particulière, signalez un problème dans le dépôt GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues).

## <a name="categorical"></a>Catégorie

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CategoricalHashOneHotVectorizer> | Encode la variable catégorielle avec un encodage basé sur le hachage. |
| <xref:Microsoft.ML.Transforms.CategoricalOneHotVectorizer> | Encode la variable catégorielle avec un encodage à chaud en fonction d’un dictionnaire de termes. |

## <a name="combiners-and-segregators"></a>Combinaison et ségrégation

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CombinerByContiguousGroupId> | Regroupe les valeurs d’une colonne scalaire dans un vecteur en fonction d’un ID de groupe contigu. |
| <xref:Microsoft.ML.Transforms.FeatureCombiner> | Combine toutes les caractéristiques dans une colonne de caractéristique. |
| <xref:Microsoft.ML.Transforms.ManyHeterogeneousModelCombiner> | Combine une séquence de TransformModels et un PredictorModel dans un seul PredictorModel. |
| <xref:Microsoft.ML.Transforms.ModelCombiner> | Combine une série de TransformModels dans un seul modèle. |
| <xref:Microsoft.ML.Transforms.Segregator> | Dissocie des colonnes de vecteur dans des séquences de lignes (inverse de la transformation de regroupement). |
| <xref:Microsoft.ML.Transforms.TwoHeterogeneousModelCombiner> | Combine un TransformModel et un PredictorModel dans un seul PredictorModel. |

## <a name="feature-selection"></a>Sélection de caractéristique

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByCount> | Sélectionne les emplacements pour lesquels le nombre de valeurs autres que des valeurs par défaut est supérieur ou égal à un seuil. |
| <xref:Microsoft.ML.Transforms.FeatureSelectorByMutualInformation> | Sélectionne les k premiers emplacements parmi toutes les colonnes spécifiées, classés d’après leurs informations mutuelles avec la colonne d’étiquette. |

## <a name="featurizers"></a>Personnaliseurs

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.HashConverter> | Convertit des valeurs de colonne en hachages. Cette transformation accepte les entrées numériques et textuelles, les colonnes à la fois uniques et à valeurs vectorielles. |
| <xref:Microsoft.ML.Transforms.TreeLeafFeaturizer> | Effectue l’apprentissage d’un ensemble d’arborescences, ou le charge à partir d’un fichier, puis mappe un vecteur de caractéristique numérique à trois sorties : 1. Un vecteur contenant les sorties d’arborescences individuelles de l’ensemble d’arborescences. 2. Un vecteur indiquant les feuilles sur lesquelles le vecteur de caractéristique tombe dans l’ensemble d’arborescences. 3. Un vecteur indiquant les chemins sur lesquels le vecteur de caractéristique tombe dans l’ensemble d’arborescences. Si vous spécifiez à la fois un fichier de modèle et un formateur, le vecteur utilise le fichier de modèle. Si vous ne spécifiez ni l’un ni l’autre, le vecteur effectue l’apprentissage d’un modèle FastTree par défaut. Cela peut permettre de gérer des étiquettes de clés en effectuant l’apprentissage d’un modèle de régression vers leurs index éventuellement permutés. |

## <a name="label-parsing"></a>Analyse d’étiquette

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Dictionarizer> | Convertit des valeurs d’entrées (mots, nombres, etc.) en index dans un dictionnaire d’entrées. |
| <xref:Microsoft.ML.Transforms.LabelColumnKeyBooleanConverter> | Transforme l’étiquette en clé ou valeur booléenne (si nécessaire) afin de la rendre utilisable pour la classification. |
| <xref:Microsoft.ML.Transforms.LabelIndicator> | Remappeur d’étiquette utilisé par OVA. |
| <xref:Microsoft.ML.Transforms.LabelToFloatConverter> | Transforme l’étiquette en valeur flottante afin de la rendre utilisable pour la régression. |
| <xref:Microsoft.ML.Transforms.PredictedLabelColumnOriginalValueConverter> | Transforme une colonne d’étiquette prédite en ses valeurs d’origine, sauf si elle est de type booléen. |

## <a name="missing-values"></a>Valeurs manquantes

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.MissingValueHandler> | Gérer les valeurs manquantes en les remplaçant par la valeur par défaut ou la valeur moyenne/min/max (pour les colonnes non textuelles uniquement). Une colonne d’indicateur peut éventuellement être concaténée, si le type de colonne d’entrée est numérique. |
| <xref:Microsoft.ML.Transforms.MissingValueIndicator> | Créer une colonne de sortie booléenne avec le même nombre d’emplacements que la colonne d’entrée, où la valeur de sortie est true si la valeur dans la colonne d’entrée est manquante. |
| <xref:Microsoft.ML.Transforms.MissingValuesDropper> | Supprime les N/A des colonnes de vecteur. |
| <xref:Microsoft.ML.Transforms.MissingValuesRowDropper> | Filtre les lignes qui contiennent des valeurs manquantes. |
| <xref:Microsoft.ML.Transforms.MissingValueSubstitutor> | Créer une colonne de sortie du même type et de la même taille que la colonne d’entrée, où les valeurs manquantes sont remplacées par la valeur par défaut ou par la valeur moyenne/min/max (pour les colonnes non textuelles uniquement). |

## <a name="normalization"></a>Normalisation

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.BinNormalizer> | Les valeurs sont affectées à des emplacements d’équidensité et une valeur est mappée à son bin_number / number_of_bins. |
| <xref:Microsoft.ML.Transforms.ConditionalNormalizer> | Normaliser les colonnes uniquement si nécessaire. |
| <xref:Microsoft.ML.Transforms.GlobalContrastNormalizer> | Effectue une normalisation de contraste globale sur des valeurs d’entrée : Y = (s * X - M) / D, où s est une échelle, M est la moyenne et D est l’écart type ou la norme L2. | 
| <xref:Microsoft.ML.Transforms.LogMeanVarianceNormalizer> | Normalise les données d’après la moyenne calculée et la variance du logarithme des données. |
| <xref:Microsoft.ML.Transforms.LpNormalizer> | Normaliser les vecteurs (lignes) individuellement par remise à l’échelle à la norme unitaire (L2, L1 ou LInf). Effectue l’opération suivante sur un vecteur X : Y = (X - M) / D, où M est la moyenne et D est la norme L2, la norme L1 ou la norme LInf. |
| <xref:Microsoft.ML.Transforms.MeanVarianceNormalizer> | Normalise les données d’après la moyenne calculée et la variance des données. |
| <xref:Microsoft.ML.Transforms.MinMaxNormalizer> | Normalise les données d’après les valeurs minimales et maximales observées des données. |
| <xref:Microsoft.ML.Transforms.SupervisedBinNormalizer> | Similaire à <xref:Microsoft.ML.Transforms.BinNormalizer>, mais calcule les emplacements d’après la corrélation avec la colonne d’étiquette, et non l’équidensité. La nouvelle valeur est bin_number / number_of_bins. |

## <a name="row-filters"></a>Filtres de lignes

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.RowRangeFilter> | Filtre un DataView sur une colonne de type Single, Double ou Clé (contiguë). Conserve les valeurs qui se trouvent dans la plage min/max spécifiée. Les valeurs NaN sont toujours exclues. Si l’entrée est un type Clé, les valeurs min/max sont considérées comme des pourcentages du nombre de valeurs. |
| <xref:Microsoft.ML.Transforms.RowSkipAndTakeFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes à un décalage facultatif. Peut être utilisé pour implémenter la pagination des données. |
| <xref:Microsoft.ML.Transforms.RowSkipFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes en ignorant un nombre de lignes. |
| <xref:Microsoft.ML.Transforms.RowTakeFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes en prenant les N premières lignes. |

## <a name="schema"></a>Schéma

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ColumnConcatenator> | Concatène deux colonnes du même type d’élément. |
| <xref:Microsoft.ML.Transforms.ColumnCopier> | Duplique des colonnes du jeu de données.|
| <xref:Microsoft.ML.Transforms.ColumnDropper> | Supprime des colonnes du jeu de données. |
| <xref:Microsoft.ML.Transforms.ColumnSelector> | Sélectionne un ensemble de colonnes et supprime toutes les autres. |
| <xref:Microsoft.ML.Transforms.ColumnTypeConverter> | Convertit une colonne en un type différent, en utilisant la conversion standard. |
| <xref:Microsoft.ML.Transforms.KeyToTextConverter> | KeyToValueTransform utilise les métadonnées KeyValues pour mapper les index de clés aux valeurs correspondantes dans les métadonnées KeyValues. |
| <xref:Microsoft.ML.Transforms.NGramTranslator> | Produit un conteneur de décomptes de ngrams (séquences de valeurs consécutives de longueur 1-n) dans un vecteur de clés donné. Crée pour cela un dictionnaire de ngrams et utilise l’ID dans le dictionnaire en tant qu’index dans le conteneur. | 
| <xref:Microsoft.ML.Transforms.OptionalColumnCreator> | Si la colonne source n’existe pas après la désérialisation, créer une colonne avec le type correct et les valeurs par défaut. |

## <a name="text-processing-and-featurization"></a>Traitement de texte et personnalisation

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CharacterTokenizer> | Générateur de jetons orienté caractère où le texte est considéré comme une séquence de caractères. |
| <xref:Microsoft.ML.Transforms.TextFeaturizer> | Transformation qui convertit une collection de documents textuels en vecteurs de caractéristiques numériques. Les vecteurs de caractéristiques sont des décomptes normalisés de ngrams (mot et/ou caractère) dans un texte tokenisé donné. |
| <xref:Microsoft.ML.Transforms.TextToKeyConverter> | Convertit des valeurs d’entrées (mots, nombres, etc.) en index dans un dictionnaire d’entrées. |
| <xref:Microsoft.ML.Transforms.WordEmbeddings> | Transformation qui convertit des vecteurs de jetons textuels en vecteurs numériques à l’aide d’un modèle préformé. Pour plus d’informations sur la technique, consultez la page Wikipédia [Word embedding](https://en.wikipedia.org/wiki/Word_embedding). |
| <xref:Microsoft.ML.Transforms.WordTokenizer> | L’entrée de cette transformation est un texte, et la sortie est un vecteur de texte contenant les mots (jetons) dans le texte d’origine. Le séparateur est l’espace, mais vous pouvez spécifier tout autre caractère (ou plusieurs caractères). |

## <a name="miscellaneous"></a>Divers

| Transformation | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ApproximateBootstrapSampler> | Échantillonnage d’amorçage approximatif. |
| <xref:Microsoft.ML.Transforms.BinaryPredictionScoreColumnsRenamer> | Pour la prédiction binaire, renomme les colonnes PredictedLabel et Score de façon à inclure le nom de la classe positive.|
| <xref:Microsoft.ML.Transforms.DataCache> | Met en cache à l’aide de l’option de cache spécifiée. |
| <xref:Microsoft.ML.Transforms.DatasetScorer> | Évalue un jeu de données avec un modèle de prédiction. |
| <xref:Microsoft.ML.Transforms.DatasetTransformScorer> | Évalue un jeu de données avec un modèle de transformation. |
| <xref:Microsoft.ML.Transforms.NoOperation> | Sans effet. |
| <xref:Microsoft.ML.Transforms.RandomNumberGenerator> | Ajoute une colonne avec une séquence de nombres générée. |
| <xref:Microsoft.ML.Transforms.ScoreColumnSelector> | Sélectionne uniquement les dernières colonnes de score et les colonnes supplémentaires spécifiées dans les arguments. |
| <xref:Microsoft.ML.Transforms.Scorer> | Convertit le modèle de prédiction en modèle de transformation. |
| <xref:Microsoft.ML.Transforms.SentimentAnalyzer> | Utilise un modèle de sentiments préformé pour évaluer les chaînes d’entrée. |
| <xref:Microsoft.ML.Transforms.TrainTestDatasetSplitter> | Fractionne le jeu de données en jeux d’apprentissage et de test. |
