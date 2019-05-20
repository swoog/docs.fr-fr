---
title: Transformations de données
description: Explorez les composants d’ingénierie de fonctionnalité pris en charge dans ML.NET.
author: natke
ms.author: nakersha
ms.date: 04/02/2019
ms.openlocfilehash: 7ea06e19b4651017079a6ae57136f033e0ce981c
ms.sourcegitcommit: 682c64df0322c7bda016f8bfea8954e9b31f1990
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2019
ms.locfileid: "65558011"
---
# <a name="data-transformations"></a>Transformations de données

Les transformations de données servent à préparer les données en vue d’effectuer l’apprentissage du modèle. Les transformations abordées dans ce guide retournent des classes qui implémentent l’interface [IEstimator](xref:Microsoft.ML.IEstimator%601). Les transformations de données peuvent s’enchaîner. Chacune transformation attend et génère des données de type et de format spécifiques, indiqués dans le lien de la documentation de référence.

Certaines transformations de données ont besoin de données d’apprentissage pour calculer leurs paramètres. Par exemple, le transformateur <xref:Microsoft.ML.NormalizationCatalog.NormalizeMeanVariance%2A> calcule la moyenne et la variance des données d’apprentissage au cours de l’opération `Fit()` et utilise ces paramètres dans l’opération `Transform()`. 

D’autres transformations de données n’exigent pas les données d’apprentissage. Par exemple, la transformation <xref:Microsoft.ML.ImageEstimatorsCatalog.ConvertToGrayscale*> peut effectuer l’opération `Transform()` sans consulter ces données durant l’opération `Fit()`.

## <a name="column-mapping-and-grouping"></a>Mappage et regroupement de colonnes

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.TransformExtensionsCatalog.Concatenate%2A> | Concaténer une ou plusieurs colonnes d’entrée en une nouvelle colonne de sortie |
| <xref:Microsoft.ML.TransformExtensionsCatalog.CopyColumns%2A> | Copier et renommer une ou plusieurs colonnes d’entrée |
| <xref:Microsoft.ML.TransformExtensionsCatalog.DropColumns%2A> | Supprimer une ou plusieurs colonnes d’entrée |
| <xref:Microsoft.ML.TransformExtensionsCatalog.SelectColumns%2A> | Sélectionner une ou plusieurs colonnes à exclure des données d’entrée |

## <a name="normalization-and-scaling"></a>Normalisation et pondération

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeMeanVariance%2A> | Soustraire la moyenne (des données d’apprentissage) et diviser par la variance (des données d’apprentissage) |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeLogMeanVariance%2A> | Normaliser selon le logarithme des données d’apprentissage |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeLpNorm%2A> | Mettre à l’échelle des vecteurs d’entrée par leur [norme Lp](https://en.wikipedia.org/wiki/Lp_space#The_p-norm_in_finite_dimensions), où p vaut 1, 2 ou l’infini, avec L² (distance euclidienne) comme valeur par défaut |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeGlobalContrast%2A> | Pondérer chacune des valeurs d’une ligne en soustrayant la moyenne des données de la ligne, diviser par l’écart type ou la norme L² (des données de la ligne) et multiplier par un facteur de proportionnalité configurable (par défaut, 2) |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeBinning%2A> | Affecter à la valeur d’entrée un index d’emplacement (bin) et diviser par le nombre d’emplacements pour produire une valeur float comprise entre 0 et 1, les limites étant calculées pour distribuer uniformément les données d’apprentissage dans les emplacements |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeSupervisedBinning%2A> | Affecter à la valeur d’entrée un emplacement en fonction de sa corrélation avec la colonne d’étiquettes |
| <xref:Microsoft.ML.NormalizationCatalog.NormalizeMinMax%2A> | Pondérer l’entrée selon la différence entre les valeurs minimales et les valeurs maximales des données d’apprentissage |

## <a name="conversions-between-data-types"></a>Conversions entre types de données

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.ConvertType%2A> | Convertir le type d’une colonne d’entrée en un nouveau type |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValue*> | Mapper les valeurs sur les clés (catégories) en fonction du dictionnaire de mappages fourni |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapValueToKey*> | Mapper les valeurs sur les clés (catégories) en créant le mappage à partir des données d’entrée |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapKeyToValue*> | Reconvertir les clés dans leurs valeurs d’origine |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.MapKeyToVector*> | Reconvertir les clés en vecteurs de valeurs d’origine |
| <xref:Microsoft.ML.ConversionsCatalog.MapKeyToBinaryVector*> | Reconvertir les clés en un vecteur binaire de valeurs d’origine |
| <xref:Microsoft.ML.ConversionsExtensionsCatalog.Hash*> | Hacher la valeur dans la colonne d’entrée |

## <a name="text-transformations"></a>Transformations textuelles

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.TextCatalog.FeaturizeText*> | Transformer une colonne de texte en un tableau float de nombres de n-grammes et de car-grammes normalisés | 
| <xref:Microsoft.ML.TextCatalog.TokenizeIntoWords*> | Fractionner une ou plusieurs colonnes de texte en mots |
| <xref:Microsoft.ML.TextCatalog.TokenizeIntoCharactersAsKeys*> | Fractionner une ou plusieurs colonnes de texte en valeurs float de caractères sur un ensemble de rubriques |
| <xref:Microsoft.ML.TextCatalog.NormalizeText*> | Modifier la casse, supprimer les signes diacritiques, les signes de ponctuation et les chiffres |
| <xref:Microsoft.ML.TextCatalog.ProduceNgrams*> | Transformer une colonne de texte en un sac de nombres de n-grammes (séquences de mots consécutifs)|
| <xref:Microsoft.ML.TextCatalog.ProduceWordBags*> | Transformer une colonne de texte en un sac de nombres de vecteur de n-grammes |
| <xref:Microsoft.ML.TextCatalog.ProduceHashedNgrams*> | Transformer la colonne de texte en un vecteur de nombres de n-grammes hachés |
| <xref:Microsoft.ML.TextCatalog.ProduceHashedWordBags*> | Transformer la colonne de texte en un sac de nombres de n-grammes hachés |
| <xref:Microsoft.ML.TextCatalog.RemoveDefaultStopWords*>  | Supprimer les mots vides par défaut des colonnes d’entrée pour la langue spécifiée |
| <xref:Microsoft.ML.TextCatalog.RemoveStopWords*> | Supprimer les mots vides spécifiés des colonnes d’entrée |
| <xref:Microsoft.ML.TextCatalog.LatentDirichletAllocation*> | Transformer un document (représenté sous la forme d’un vecteur de valeurs float) en un vecteur de valeurs float sur un ensemble de rubriques |
| <xref:Microsoft.ML.TextCatalog.ApplyWordEmbedding*> | Convertir des vecteurs de jetons textuels en vecteurs de phrases selon un modèle préentraîné |

## <a name="image-transformations"></a>Transformations d’images

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.ImageEstimatorsCatalog.ConvertToGrayscale*> | Convertir une image en nuances de gris |
| <xref:Microsoft.ML.ImageEstimatorsCatalog.ConvertToImage*> | Convertir un vecteur de pixels en <xref:Microsoft.ML.Transforms.Image.ImageDataViewType> |
| <xref:Microsoft.ML.ImageEstimatorsCatalog.ExtractPixels*> | Convertir les pixels d’une image d’entrée en un vecteur de nombres |
| <xref:Microsoft.ML.ImageEstimatorsCatalog.LoadImages*> | Charger les images d’un dossier en mémoire |
| <xref:Microsoft.ML.ImageEstimatorsCatalog.ResizeImages*> | Redimensionner les images |

## <a name="categorical-data-transformations"></a>Transformations de données catégoriques

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.CategoricalCatalog.OneHotEncoding*> | Convertir une ou plusieurs colonnes de texte en vecteurs encodés [one-hot](https://en.wikipedia.org/wiki/One-hot) |
| <xref:Microsoft.ML.CategoricalCatalog.OneHotHashEncoding*> | Convertir une ou plusieurs colonnes de texte en vecteurs encodés one-hot par hachage |

## <a name="missing-values"></a>Valeurs manquantes

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.ExtensionsCatalog.IndicateMissingValues*> | Créer une colonne de sortie booléenne dont la valeur est true s’il manque la valeur de la colonne d’entrée |
| <xref:Microsoft.ML.ExtensionsCatalog.ReplaceMissingValues*> | Créer une colonne de sortie dont la valeur est définie sur une valeur par défaut s’il manque la valeur de la colonne d’entrée, sur la valeur d’entrée sinon |

## <a name="feature-selection"></a>Sélection de caractéristique

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.FeatureSelectionCatalog.SelectFeaturesBasedOnCount*> | Sélectionner les caractéristiques dont les valeurs par défaut sont supérieures à un seuil |
| <xref:Microsoft.ML.FeatureSelectionCatalog.SelectFeaturesBasedOnMutualInformation*> | Sélectionnez les caractéristiques dont les données de la colonne d’étiquette dépendent le plus |

## <a name="custom-transformations"></a>Transformations personnalisées

| Transformer | Définition |
| --- | --- |
| <xref:Microsoft.ML.CustomMappingCatalog.CustomMapping*> | Transformer des colonnes existantes en de nouvelles colonnes suivant un mappage défini par l’utilisateur |
