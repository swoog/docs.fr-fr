---
title: Transformations de données Machine Learning - ML.NET
description: Explorez les composants d’ingénierie de fonctionnalité pris en charge dans ML.NET.
author: JRAlexander
ms.custom: seodec18
ms.date: 01/14/2019
ms.openlocfilehash: 54dffec37318b79edf546ba1f6e1145e35782bfb
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415349"
---
# <a name="machine-learning-data-transforms---mlnet"></a>Transformations de données Machine Learning - ML.NET

Les tableaux suivants contiennent des informations sur toutes les transformations de données prises en charge dans ML.NET.

> [!NOTE]
> ML.NET est actuellement en préversion. Les transformations de données ne sont pas toutes prises en charge actuellement. Pour envoyer une requête pour une transformation particulière, signalez un problème dans le dépôt GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/issues).

## <a name="combiners-and-segregators"></a>Combinaison et ségrégation

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.GroupTransform> | Regroupe les valeurs d’une colonne scalaire dans un vecteur en fonction d’un ID de groupe contigu. |
| <xref:Microsoft.ML.Transforms.UngroupTransform> | Dissocie des colonnes de vecteur dans des séquences de lignes (inverse de la transformation de regroupement). |

## <a name="conversions"></a>Conversions 

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Conversions.HashingTransformer> | Hache des colonnes à valeurs uniques ou des colonnes de vecteur. Pour les colonnes de vecteur, hache séparément chaque emplacement. Peut hacher des valeurs texte ou de valeurs de clés. |
| <xref:Microsoft.ML.Transforms.Conversions.HashJoiningTransform> | Convertit plusieurs valeurs de colonne en hachages. Cette transformation accepte les entrées numériques et textuelles, les colonnes à la fois uniques et à valeurs vectorielles. |
| <xref:Microsoft.ML.Transforms.Conversions.KeyToBinaryVectorMappingTransformer> | Convertit une clé en colonne de vecteur binaire. |
| <xref:Microsoft.ML.Transforms.Conversions.KeyToValueMappingTransformer > | Utilise les métadonnées KeyValues pour mapper les index de clés aux valeurs correspondantes dans les métadonnées KeyValues. |
| <xref:Microsoft.ML.Transforms.Conversions.KeyToVectorMappingTransformer> | Convertit une clé en colonne de vecteur. |
| <xref:Microsoft.ML.Transforms.Conversions.TypeConvertingTransformer> | Modifie le type de colonne sous-jacent si le type peut être converti. |
| <xref:Microsoft.ML.Transforms.Conversions.ValueToKeyMappingTransformer> | Convertit des valeurs d’entrées (mots, nombres, etc.) en index dans un dictionnaire d’entrées. |


## <a name="deep-learning"></a>Deep Learning

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.OnnxTransform> | Fournit des données à un modèle ONNX existant et retourne le score (prévision). |
| <xref:Microsoft.ML.Transforms.TensorFlowTransform> | Peut retourner un score avec un modèle TensorFlow entraîné ou réentraîner un modèle TensorFlow. |

## <a name="feature-extraction"></a>Extraction de fonctionnalité

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Text.CustomStopWordsRemovingTransform> | Supprime une liste spécifiée de mots vides en comparant des jetons individuels (comparaison sensible à la casse) à des mots vides.| 
| <xref:Microsoft.ML.ImageAnalytics.ImageGrayscaleTransform> | Sélectionne une ou plusieurs colonnes ImageType et les convertit en une représentation en nuances de gris de la même image.|
| <xref:Microsoft.ML.ImageAnalytics.ImageLoaderTransform> | Sélectionne une ou plusieurs colonnes ReadOnlyMemory et les charge au format ImageType. |
| <xref:Microsoft.ML.ImageAnalytics.ImagePixelExtractorTransform> | Sélectionne une ou plusieurs colonnes ImageType et les convertit en représentation de vecteur.|
| <xref:Microsoft.ML.ImageAnalytics.ImageResizerTransform> | Sélectionne une ou plusieurs colonnes ImageType et les redimensionne à la hauteur et à la largeur fournies.|
| <xref:Microsoft.ML.Transforms.Text.LatentDirichletAllocationTransformer> | Implémente LightLDA, une implémentation de pointe de Latent Dirichlet Allocation.|
| <xref:Microsoft.ML.Transforms.LoadTransform> | Charge des transformations spécifiques à partir du fichier de modèle spécifié. Permet des transformations de type « cherry picking » à partir d’une chaîne sérialisée, ou l’application d’une transformation préentraînée dans une vue de données différente (mais toujours compatible). |
| <xref:Microsoft.ML.Transforms.Text.NgramExtractingTransformer> | Produit un conteneur de décomptes de ngrams (séquences de valeurs consécutives de longueur 1-n) dans un vecteur de clés donné. Crée pour cela un dictionnaire de ngrams et utilise l’ID dans le dictionnaire en tant qu’index dans le conteneur. | 
| <xref:Microsoft.ML.Transforms.Text.NgramExtractorTransform> | Convertit une collection de texte tokénisé (vecteur de ReadOnlyMemory) ou des vecteurs de clés en vecteurs de fonctionnalité numériques. Les vecteurs de fonctionnalité sont des décomptes de ngrams (séquences de jetons consécutifs - mots ou clés - de longueur 1-n). | 
| <xref:Microsoft.ML.Transforms.Text.NgramHashExtractingTransformer> | Convertit une collection de texte tokénisé (vecteur de ReadOnlyMemory) en vecteurs de fonctionnalité numériques à l’aide d’un hachage. | 
| <xref:Microsoft.ML.Transforms.Text.NgramHashingTransformer> | Produit un conteneur de décomptes de ngrams (séquences de mots consécutifs de longueur 1-n) dans un texte donné. | 
| <xref:Microsoft.ML.Transforms.Categorical.OneHotEncodingTransformer> | Convertit la valeur catégorique en un tableau d’indicateurs en créant un dictionnaire de catégories selon les données et en utilisant l’ID dans le dictionnaire comme index du tableau |
| <xref:Microsoft.ML.Transforms.Projections.PcaTransform> | Calcule la projection du vecteur de fonctionnalité sur un sous-espace de rang inférieur. |
| <xref:Microsoft.ML.Transforms.Text.SentimentAnalyzingTransformer> | Utilise un modèle de sentiments préformé pour évaluer les chaînes d’entrée. |
| <xref:Microsoft.ML.Transforms.Text.StopWordsRemovingTransformer> | Supprime une liste spécifique à une langue de mots vides (mots les plus courants) en comparant des jetons individuels (comparaison sensible à la casse) à des mots vides. |
| <xref:Microsoft.ML.Transforms.Text.WordBagBuildingTransformer> | Produit un conteneur de décomptes de ngrams (séquences de mots consécutifs) dans un texte donné. Crée pour cela un dictionnaire de ngrams et utilise l’ID dans le dictionnaire en tant qu’index dans le conteneur. |
| <xref:Microsoft.ML.Transforms.Text.WordHashBagProducingTransformer> | Produit un conteneur de décomptes de ngrams (séquences de mots consécutifs de longueur 1-n) dans un texte donné. Pour cela, il hache chaque ngram et utilise la valeur de hachage comme index dans le conteneur. |
| <xref:Microsoft.ML.Transforms.Text.WordTokenizingTransformer> | Fractionne le texte en mots à l’aide de caractères de séparation. |


## <a name="image-model-featurizers"></a>Personnaliseurs de modèle d’image

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.AlexNetExtension> | Il s’agit d’une méthode d’extension à utiliser avec <xref:Microsoft.ML.Transforms.DnnImageFeaturizerEstimator> afin d’utiliser un modèle [AlexNet](https://en.wikipedia.org/wiki/AlexNet) préentraîné. Le package NuGet contenant cette extension est également garanti pour inclure le fichier modèle binaire. | 
| <xref:Microsoft.ML.Transforms.ResNet18Extension> | Il s’agit d’une méthode d’extension à utiliser avec <xref:Microsoft.ML.Transforms.DnnImageFeaturizerEstimator> afin d’utiliser un modèle ResNet18 préentraîné. Le package NuGet contenant cette extension est également garanti pour inclure le fichier modèle binaire. |
| <xref:Microsoft.ML.Transforms.ResNet50Extension> | Il s’agit d’une méthode d’extension à utiliser avec <xref:Microsoft.ML.Transforms.DnnImageFeaturizerEstimator> afin d’utiliser un modèle ResNet50 préentraîné. Le package NuGet contenant cette extension est également garanti pour inclure le fichier modèle binaire. |
| <xref:Microsoft.ML.Transforms.ResNet101Extension> | Il s’agit d’une méthode d’extension à utiliser avec <xref:Microsoft.ML.Transforms.DnnImageFeaturizerEstimator> afin d’utiliser un modèle ResNet101 préentraîné. Le package NuGet contenant cette extension est également garanti pour inclure le fichier modèle binaire. |

## <a name="label-parsing"></a>Analyse d’étiquette

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.LabelConvertTransform> |  Convertit des étiquettes. |
| <xref:Microsoft.ML.Transforms.LabelIndicatorTransform> | Remappe les étiquettes multiclasses au format True binaire, étiquettes False, principalement pour une utilisation avec OVA.|

## <a name="missing-values"></a>Valeurs manquantes

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.MissingValueDroppingTransformer> | Supprime les valeurs manquantes des colonnes. |
| <xref:Microsoft.ML.Transforms.MissingValueIndicatorTransform> | Crée une colonne de sortie booléenne avec le même nombre d’emplacements que la colonne d’entrée, où la valeur de sortie est true si la valeur dans la colonne d’entrée est manquante. |
| <xref:Microsoft.ML.Transforms.MissingValueReplacingTransformer> | Gérer les valeurs manquantes en les remplaçant par la valeur par défaut ou la valeur moyenne/min/max (pour les colonnes non textuelles uniquement). |

## <a name="normalization"></a>Normalisation

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Projections.LpNormalizingTransformer> | Transformation de normalisation Lp-Norm (selon les vecteurs/lignes). |
| <xref:Microsoft.ML.Transforms.Normalizers.MeanVarDblAggregator> | Calcule la moyenne et la variance d’une colonne de valeurs de vecteur. Effectue le suivi de la moyenne actuelle et de la valeur M2 (somme des différences au carré des valeurs à partir de la moyenne), le nombre de valeurs NaN et le nombre d’éléments non nuls. |
| <xref:Microsoft.ML.Transforms.Normalizers.MeanVarSngAggregator> | Calcule la moyenne et la variance d’une colonne de valeurs de vecteur. Effectue le suivi de la moyenne actuelle et de la valeur M2 (somme des différences au carré des valeurs à partir de la moyenne), le nombre de valeurs NaN et le nombre d’éléments non nuls. |
| <xref:Microsoft.ML.Transforms.Normalizers.MinMaxDblAggregator> | Effectue le suivi des valeurs min, max, du nombre de valeurs non éparses (vCount) et du nombre d’appels ProcessValue() (trainCount) pour une colonne de valeurs de vecteur. |
| <xref:Microsoft.ML.Transforms.Normalizers.NormalizeTransform> | Normalise des plages de fonctionnalité. |
| <xref:Microsoft.ML.Transforms.Normalizers.NormalizingTransformer> |Normalise des plages de fonctionnalité. |

## <a name="onnx"></a>Onnx

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.OnnxTransform> | Retourne le score des modèles ONNX préformés qui utilisent la norme ONNX 1.2 |

## <a name="preprocessing"></a>Prétraitement
| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.BootstrapSamplingTransformer> | Effectue une approximation de l’échantillonnage d’amorçage en utilisant l’échantillonnage de Poisson. |
| <xref:Microsoft.ML.Transforms.Projections.RandomFourierFeaturizingTransformer> | Produit une fonctionnalité de Fourier aléatoire. |
| <xref:Microsoft.ML.Transforms.Text.TokenizingByCharactersTransformer> | Générateur de jetons orienté caractère où le texte est considéré comme une séquence de caractères. |
| <xref:Microsoft.ML.Transforms.Projections.VectorWhiteningTransformer> | Simplifie l’optimisation pour vous aider à identifier les pondérations. |

## <a name="row-filters"></a>Filtres de lignes

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.RowShufflingTransformer> | Lit de façon aléatoire une tentative d’utilisation d’un curseur aléatoire avec un pool d’un nombre donné de lignes.  |
| <xref:Microsoft.ML.Transforms.SkipFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes en ignorant un nombre de lignes. |
| <xref:Microsoft.ML.Transforms.SkipTakeFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes à un décalage facultatif. Peut être utilisé pour implémenter la pagination des données. Lors de la création avec SkipTakeFilter.SkipArguments, se comporte comme `SkipFilter`.
| <xref:Microsoft.ML.Transforms.TakeFilter> | Permet de limiter l’entrée à un sous-ensemble de lignes en prenant les N premières lignes. |


## <a name="schema"></a>Schéma

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.ColumnCopyingTransformer> | Duplique des colonnes du jeu de données.|
| <xref:Microsoft.ML.Transforms.ColumnSelectingTransformer> | Sélectionne un ensemble de colonnes à supprimer ou à conserver à partir d’une entrée donnée. |
| <xref:Microsoft.ML.Transforms.FeatureSelection.SlotsDroppingTransformer> | Supprime des emplacements des colonnes.|
| <xref:Microsoft.ML.Transforms.OptionalColumnTransform> | Crée une nouvelle colonne avec le type et les valeurs par défaut spécifiés. |
| <xref:Microsoft.ML.Transforms.RangeFilter> | Filtre un DataView sur une colonne de type Single, Double ou Clé (contiguë). Conserve les valeurs qui se trouvent dans la plage min/max spécifiée. Les valeurs NaN sont toujours exclues. Si l’entrée est un type Clé, les valeurs min/max sont considérées comme des pourcentages du nombre de valeurs. |

## <a name="tensorflow"></a>TensorFlow

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.TensorFlowTransform> | Retourne un score avec un modèle TensorFlow entraîné ou réentraîne un modèle TensorFlow. |

## <a name="text-processing-and-featurization"></a>Traitement de texte et personnalisation

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.Text.TextNormalizingTransformer> | Une transformation de normalisation de texte qui permet de normaliser la casse du texte, en supprimant des signes diacritiques, des signes de ponctuation et/ou des nombres. La transformation s’exécute sur l’entrée de texte ainsi que le vecteur de jetons/texte (vecteur de ReadOnlyMemory). |
| <xref:Microsoft.ML.Transforms.Text.TokenizingByCharactersTransformer> | Générateur de jetons orienté caractère où le texte est considéré comme une séquence de caractères. |

## <a name="time-series"></a>Série chronologique

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.TimeSeriesProcessing.ExponentialAverageTransform> | Sélectionne une moyenne pondérée des valeurs : ExpAvg(y_t) = a * y_t + (1-a) * ExpAvg(y_(t-1)). |
| <xref:Microsoft.ML.TimeSeriesProcessing.IidChangePointDetector> | Implémente la transformation du détecteur de point de modification pour une séquence i.i.d. (échantillon aléatoire) en fonction d’une estimation de densité de noyau adaptative et de martingales. |
| <xref:Microsoft.ML.TimeSeriesProcessing.IidSpikeDetector> | Implémente la transformation du détecteur de pic pour une séquence i.i.d. (échantillon aléatoire) en fonction d’une estimation de densité de noyau adaptative. |
| <xref:Microsoft.ML.TimeSeriesProcessing.MovingAverageTransform> | Fournit une moyenne pondérée des valeurs de fenêtre glissante. |
| <xref:Microsoft.ML.TimeSeriesProcessing.PercentileThresholdTransform> | Détermine si la valeur actuelle de la série chronologique appartient au centile de valeurs supérieures de la fenêtre glissante. |
| <xref:Microsoft.ML.TimeSeriesProcessing.PValueTransform> | Calcule la valeur empirique p-valeur actuelle de la série en fonction des autres valeurs de la fenêtre glissante. |
| <xref:Microsoft.ML.TimeSeriesProcessing.SlidingWindowTransform> | Génère une fenêtre glissante sur une série chronologique de type Single. |
| <xref:Microsoft.ML.TimeSeriesProcessing.SsaChangePointDetector> | Implémente la transformation de détecteur de point de modification en fonction d’une modélisation Singular Spectrum de la série chronologique. |
| <xref:Microsoft.ML.TimeSeriesProcessing.SsaSpikeDetector> | Implémente la transformation de détecteur de pic en fonction d’une modélisation Singular Spectrum de la série chronologique. |

## <a name="miscellaneous"></a>Divers

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.Transforms.CompositeTransformer> | Crée une transformation de données composite. |
| <xref:Microsoft.ML.Transforms.CustomMappingTransformer%602> | Génère des colonnes supplémentaires et les ajoute à la collection `IDataView`. Ne modifie pas le nombre de lignes et peut être considéré comme le résultat d’une application de la fonction de l’utilisateur à chaque ligne des données d’entrée.|
| <xref:Microsoft.ML.Transforms.GenerateNumberTransform> | Ajoute une colonne avec une séquence de nombres générée. |
| <xref:Microsoft.ML.Transforms.ProduceIdTransform> | Produit une colonne avec l’ID du curseur en tant que colonne. |
| <xref:Microsoft.ML.Transforms.RandomNumberGenerator> | Génère un nombre aléatoire. |
