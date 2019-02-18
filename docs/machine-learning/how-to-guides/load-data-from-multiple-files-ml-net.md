---
title: Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET
description: Découvrez comment charger des données à partir de plusieurs fichiers pour les utiliser lors de la création, l’entraînement et le scoring de modèles Machine Learning avec ML.NET
ms.date: 02/06/2019
ms.custom: mvc,how-to
ms.openlocfilehash: f5108aaed80769f2bc7ed2f974f9a729abe8455e
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092044"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="e3453-103">Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="e3453-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

<span data-ttu-id="e3453-104">Utilisez `TextLoader` et spécifiez un tableau de fichiers à la méthode `Read`.</span><span class="sxs-lookup"><span data-stu-id="e3453-104">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="e3453-105">Les fichiers doivent avoir le même schéma (même nombre et type de colonnes) :</span><span class="sxs-lookup"><span data-stu-id="e3453-105">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="e3453-106">Exemple de fichier1</span><span class="sxs-lookup"><span data-stu-id="e3453-106">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="e3453-107">Exemple de fichier2</span><span class="sxs-lookup"><span data-stu-id="e3453-107">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

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