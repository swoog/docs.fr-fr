---
title: Charger des données à partir d’un fichier texte pour le traitement Machine Learning - ML.NET
description: Découvrez comment charger des données à partir d’un fichier texte pour les utiliser lors de la création, l’entraînement et le scoring de modèles Machine Learning avec ML.NET.
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 14b1f8c99da6f1b8da436d9afef5b2ac8d36ecae
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57843367"
---
# <a name="load-data-from-a-text-file-for-machine-learning-processing---mlnet"></a><span data-ttu-id="594fc-103">Charger des données à partir d’un fichier texte pour le traitement Machine Learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="594fc-103">Load data from a text file for machine learning processing - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="594fc-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="594fc-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="594fc-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="594fc-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="594fc-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="594fc-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="594fc-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="594fc-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="594fc-108">`TextLoader` sert à charger des données à partir de fichiers texte.</span><span class="sxs-lookup"><span data-stu-id="594fc-108">`TextLoader` is used to load data from text files.</span></span> <span data-ttu-id="594fc-109">Vous devez spécifier les colonnes de données, leurs types et leur emplacement dans le fichier texte.</span><span class="sxs-lookup"><span data-stu-id="594fc-109">You need to specify the data columns, their types, and their location in the text file.</span></span>

<span data-ttu-id="594fc-110">Notez qu’il est parfaitement acceptable de lire certaines colonnes d’un fichier ou de lire la même colonne plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="594fc-110">Note that it's perfectly acceptable to read some columns of a file, or read the same column multiple times.</span></span>

<span data-ttu-id="594fc-111">[Exemple de fichier](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt) :</span><span class="sxs-lookup"><span data-stu-id="594fc-111">[Example file](https://github.com/dotnet/machinelearning/blob/master/test/data/adult.tiny.with-schema.txt):</span></span>

<!-- markdownlint-disable MD010 -->
```console
Label   Workclass   education   marital-status
0   Private 11th    Never-married
0   Private HS-grad Married-civ-spouse
1   Local-gov   Assoc-acdm  Married-civ-spouse
1   Private Some-college    Married-civ-spouse
```
<!-- markdownlint-enable MD010 -->

<span data-ttu-id="594fc-112">Pour charger les données d’un fichier texte :</span><span class="sxs-lookup"><span data-stu-id="594fc-112">To load the data from a text file:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging,
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextLoader(
    columns: new TextLoader.Column[]
    {
        // A boolean column depicting the 'target label'.
        new TextLoader.Column("IsOver50k",DataKind.BL,0),
        // Three text columns.
        new TextLoader.Column("WorkClass",DataKind.TX,1),
        new TextLoader.Column("Education",DataKind.TX,2),
        new TextLoader.Column("MaritalStatus",DataKind.TX,3)
    },
    hasHeader: true
);

// Now read the file (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(dataPath);
```
