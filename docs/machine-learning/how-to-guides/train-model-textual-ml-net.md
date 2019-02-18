---
title: Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données textuelles - ML.NET
description: Découvrez comment appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles sur des données textuelles avec ML.NET
ms.date: 02/06/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 4206bfe1e840c420c90e62957036a629ecf34445
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092213"
---
# <a name="apply-feature-engineering-for-machine-learning-model-training-on-textual-data-with-mlnet"></a><span data-ttu-id="4391e-103">Appliquer l’ingénierie des caractéristiques pour l’entraînement des modèles Machine Learning sur des données textuelles avec ML.NET</span><span class="sxs-lookup"><span data-stu-id="4391e-103">Apply feature engineering for machine learning model training on textual data with ML.NET</span></span>

<span data-ttu-id="4391e-104">Vous devez convertir les données non flottantes en types de données `float`, car tous les `learners` ML.NET attendent les caractéristiques sous forme de `float vector`.</span><span class="sxs-lookup"><span data-stu-id="4391e-104">You need to convert any non float data to `float` data types since all ML.NET `learners` expect features as a `float vector`.</span></span>

<span data-ttu-id="4391e-105">Pour effectuer un entraînement sur des données textuelles, vous devez extraire des caractéristiques textuelles.</span><span class="sxs-lookup"><span data-stu-id="4391e-105">To learn on textual data, you need to extract text features.</span></span> <span data-ttu-id="4391e-106">ML.NET a quelques mécanismes de base pour l’extraction de caractéristiques textuelles :</span><span class="sxs-lookup"><span data-stu-id="4391e-106">ML.NET has some basic text feature extraction mechanisms:</span></span>

- <span data-ttu-id="4391e-107">`Text normalization` (suppression des signes de ponctuation, suppression des signes diacritiques, conversion en minuscules, etc.)</span><span class="sxs-lookup"><span data-stu-id="4391e-107">`Text normalization` (removing punctuation, diacritics, switching to lowercase etc.)</span></span>
- <span data-ttu-id="4391e-108">`Separator-based tokenization`.</span><span class="sxs-lookup"><span data-stu-id="4391e-108">`Separator-based tokenization`.</span></span>
- <span data-ttu-id="4391e-109">Suppression des `Stopword`.</span><span class="sxs-lookup"><span data-stu-id="4391e-109">`Stopword` removal.</span></span>
- <span data-ttu-id="4391e-110">Extraction des `Ngram` et des `skip-gram`.</span><span class="sxs-lookup"><span data-stu-id="4391e-110">`Ngram` and `skip-gram` extraction.</span></span>
- <span data-ttu-id="4391e-111">Redimensionnement de `TF-IDF`.</span><span class="sxs-lookup"><span data-stu-id="4391e-111">`TF-IDF` rescaling.</span></span>
- <span data-ttu-id="4391e-112">Conversion de `Bag of words`.</span><span class="sxs-lookup"><span data-stu-id="4391e-112">`Bag of words` conversion.</span></span>

<span data-ttu-id="4391e-113">L’exemple suivant montre les mécanismes d’extraction de caractéristiques textuelles de ML.NET avec le [jeu de données detox de Wikipédia](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv) :</span><span class="sxs-lookup"><span data-stu-id="4391e-113">The following example demonstrates ML.NET text feature extraction mechanisms using the [Wikipedia detox dataset](https://github.com/dotnet/machinelearning/blob/master/test/data/wikipedia-detox-250-line-data.tsv):</span></span>

```console
Sentiment   SentimentText
1   Stop trolling, zapatancas, calling me a liar merely demonstartes that you arer Zapatancas. You may choose to chase every legitimate editor from this site and ignore me but I am an editor with a record that isnt 99% trolling and therefore my wishes are not to be completely ignored by a sockpuppet like yourself. The consensus is overwhelmingly against you and your trolling lover Zapatancas,  
1   ::::: Why are you threatening me? I'm not being disruptive, its you who is being disruptive.   
0   " *::Your POV and propaganda pushing is dully noted. However listing interesting facts in a netral and unacusitory tone is not POV. You seem to be confusing Censorship with POV monitoring. I see nothing POV expressed in the listing of intersting facts. If you want to contribute more facts or edit wording of the cited fact to make them sound more netral then go ahead. No need to CENSOR interesting factual information. "
0   ::::::::This is a gross exaggeration. Nobody is setting a kangaroo court. There was a simple addition concerning the airline. It is the only one disputed here.   
```

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
