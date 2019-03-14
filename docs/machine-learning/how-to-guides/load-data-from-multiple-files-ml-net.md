---
title: Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET
description: Découvrez comment charger des données à partir de plusieurs fichiers pour les utiliser lors de la création, l’entraînement et le scoring de modèles Machine Learning avec ML.NET
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: fbf5e4b5ab9a1a686edb933bdec818fc532bbf42
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57679019"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="aca37-103">Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="aca37-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="aca37-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="aca37-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="aca37-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="aca37-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="aca37-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.10**.</span><span class="sxs-lookup"><span data-stu-id="aca37-106">This how-to and related sample are currently using **ML.NET version 0.10**.</span></span> <span data-ttu-id="aca37-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="aca37-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="aca37-108">Utilisez `TextLoader` et spécifiez un tableau de fichiers à la méthode `Read`.</span><span class="sxs-lookup"><span data-stu-id="aca37-108">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="aca37-109">Les fichiers doivent avoir le même schéma (même nombre et type de colonnes) :</span><span class="sxs-lookup"><span data-stu-id="aca37-109">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="aca37-110">Exemple de fichier1</span><span class="sxs-lookup"><span data-stu-id="aca37-110">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="aca37-111">Exemple de fichier2</span><span class="sxs-lookup"><span data-stu-id="aca37-111">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

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

// Now read the files (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(exampleFile1, exampleFile2);
```