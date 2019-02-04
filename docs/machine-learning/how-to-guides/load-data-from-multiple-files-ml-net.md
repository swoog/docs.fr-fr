---
title: Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET
description: Découvrez comment charger des données à partir de plusieurs fichiers pour les utiliser lors de la création, l’entraînement et le scoring de modèles Machine Learning avec ML.NET
ms.date: 01/29/2019
ms.custom: mvc,how-to
ms.openlocfilehash: fe6758e46d923dc07908e1334056ea8394c1085e
ms.sourcegitcommit: dcc8feeff4718664087747529638ec9b47e65234
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55479982"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="d8689-103">Charger des données à partir de plusieurs fichiers pour le traitement machine learning - ML.NET</span><span class="sxs-lookup"><span data-stu-id="d8689-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

<span data-ttu-id="d8689-104">Utilisez `TextLoader` et spécifiez un tableau de fichiers à la méthode `Read`.</span><span class="sxs-lookup"><span data-stu-id="d8689-104">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="d8689-105">Les fichiers doivent avoir le même schéma (même nombre et type de colonnes) :</span><span class="sxs-lookup"><span data-stu-id="d8689-105">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="d8689-106">Exemple de fichier1</span><span class="sxs-lookup"><span data-stu-id="d8689-106">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="d8689-107">Exemple de fichier2</span><span class="sxs-lookup"><span data-stu-id="d8689-107">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextReader(
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