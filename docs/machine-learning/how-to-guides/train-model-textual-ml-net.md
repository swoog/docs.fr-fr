---
title: Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données textuelles - ML.NET
description: Découvrez comment appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données textuelles avec ML.NET
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: e26a4b293869b7cdad3c439237bd0145cafa314a
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57844355"
---
# <a name="apply-feature-engineering-for-machine-learning-model-training-on-textual-data-with-mlnet"></a><span data-ttu-id="e1d9b-103">Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles Machine Learning sur des données textuelles avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="e1d9b-103">Apply feature engineering for machine learning model training on textual data with ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="e1d9b-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="e1d9b-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="e1d9b-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="e1d9b-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="e1d9b-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="e1d9b-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="e1d9b-108">Vous devez convertir les données non flottantes en types de données `float`, car tous les `learners` ML.NET attendent les caractéristiques sous forme de `float vector`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-108">You need to convert any non float data to `float` data types since all ML.NET `learners` expect features as a `float vector`.</span></span>

<span data-ttu-id="e1d9b-109">Pour effectuer un entraînement sur des données textuelles, vous devez extraire des caractéristiques textuelles.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-109">To learn on textual data, you need to extract text features.</span></span> <span data-ttu-id="e1d9b-110">ML.NET a quelques mécanismes de base pour l’extraction de caractéristiques textuelles :</span><span class="sxs-lookup"><span data-stu-id="e1d9b-110">ML.NET has some basic text feature extraction mechanisms:</span></span>

- <span data-ttu-id="e1d9b-111">`Text normalization` (suppression des signes de ponctuation, suppression des signes diacritiques, conversion en minuscules, etc.)</span><span class="sxs-lookup"><span data-stu-id="e1d9b-111">`Text normalization` (removing punctuation, diacritics, switching to lowercase etc.)</span></span>
- <span data-ttu-id="e1d9b-112">`Separator-based tokenization`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-112">`Separator-based tokenization`.</span></span>
- <span data-ttu-id="e1d9b-113">Suppression des `Stopword`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-113">`Stopword` removal.</span></span>
- <span data-ttu-id="e1d9b-114">Extraction des `Ngram` et des `skip-gram`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-114">`Ngram` and `skip-gram` extraction.</span></span>
- <span data-ttu-id="e1d9b-115">Redimensionnement de `TF-IDF`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-115">`TF-IDF` rescaling.</span></span>
- <span data-ttu-id="e1d9b-116">Conversion de `Bag of words`.</span><span class="sxs-lookup"><span data-stu-id="e1d9b-116">`Bag of words` conversion.</span></span>

<span data-ttu-id="e1d9b-117">L’exemple suivant montre les mécanismes d’extraction de caractéristiques textuelles de ML.NET avec le [jeu de données detox de Wikipédia](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) :</span><span class="sxs-lookup"><span data-stu-id="e1d9b-117">The following example demonstrates ML.NET text feature extraction mechanisms using the [Wikipedia detox dataset](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv):</span></span>

<!-- markdownlint-disable MD010 -->
```console
Sentiment   SentimentText
1   Stop trolling, zapatancas, calling me a liar merely demonstartes that you arer Zapatancas. You may choose to chase every legitimate editor from this site and ignore me but I am an editor with a record that isnt 99% trolling and therefore my wishes are not to be completely ignored by a sockpuppet like yourself. The consensus is overwhelmingly against you and your trolling lover Zapatancas,  
1   ::::: Why are you threatening me? I'm not being disruptive, its you who is being disruptive.   
0   " *::Your POV and propaganda pushing is dully noted. However listing interesting facts in a netral and unacusitory tone is not POV. You seem to be confusing Censorship with POV monitoring. I see nothing POV expressed in the listing of intersting facts. If you want to contribute more facts or edit wording of the cited fact to make them sound more netral then go ahead. No need to CENSOR interesting factual information. "
0   ::::::::This is a gross exaggeration. Nobody is setting a kangaroo court. There was a simple addition concerning the airline. It is the only one disputed here.   
```
<!-- markdownlint-enable MD010 -->

```csharp
// Define the reader: specify the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextLoader(new[] 
    {
        new TextLoader.Column("IsToxic", DataKind.BL, 0),
        new TextLoader.Column("Message", DataKind.TX, 1),
    },
    hasHeader: true
);

// Read the data.
var data = reader.Read(dataPath);

// Inspect the message texts that are read from the file.
var messageTexts = data.GetColumn<string>(mlContext, "Message").Take(20).ToArray();

// Apply various kinds of text operations supported by ML.NET.
var pipeline =
    // One-stop shop to run the full text featurization.
    mlContext.Transforms.Text.FeaturizeText("TextFeatures", "Message")

    // Normalize the message for later transforms
    .Append(mlContext.Transforms.Text.NormalizeText("NormalizedMessage", "Message"))

    // NLP pipeline 1: bag of words.
    .Append(new WordBagEstimator(mlContext, "BagOfWords", "NormalizedMessage"))

    // NLP pipeline 2: bag of bigrams, using hashes instead of dictionary indices.
    .Append(new WordHashBagEstimator(mlContext, "BagOfBigrams","NormalizedMessage", 
                ngramLength: 2, allLengths: false))

    // NLP pipeline 3: bag of tri-character sequences with TF-IDF weighting.
    .Append(mlContext.Transforms.Text.TokenizeCharacters("MessageChars", "Message"))
    .Append(new NgramExtractingEstimator(mlContext, "BagOfTrichar", "MessageChars", 
                ngramLength: 3, weighting: NgramExtractingEstimator.WeightingCriteria.TfIdf))

    // NLP pipeline 4: word embeddings.
    .Append(mlContext.Transforms.Text.TokenizeWords("TokenizedMessage", "NormalizedMessage"))
    .Append(mlContext.Transforms.Text.ExtractWordEmbeddings("Embeddings", "TokenizedMessage",
                WordEmbeddingsExtractingTransformer.PretrainedModelKind.GloVeTwitter25D));

// Let's train our pipeline, and then apply it to the same data.
// Note that even on a small dataset of 70KB the pipeline above can take up to a minute to completely train.
var transformedData = pipeline.Fit(data).Transform(data);

// Inspect some columns of the resulting dataset.
var embeddings = transformedData.GetColumn<float[]>(mlContext, "Embeddings").Take(10).ToArray();
var unigrams = transformedData.GetColumn<float[]>(mlContext, "BagOfWords").Take(10).ToArray();
```
