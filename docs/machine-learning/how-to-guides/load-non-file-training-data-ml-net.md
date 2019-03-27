---
title: Entraîner un modèle Machine Learning avec des données qui ne sont pas dans un fichier texte - ML.NET
description: Découvrez comment utiliser ML.NET pour charger des données d’entraînement non-fichier pour l’entraînement de modèles Machine Learning dans le cadre d’un pipeline de prédiction.
ms.date: 03/18/2019
ms.custom: mvc,how-to
ms.openlocfilehash: 32de37e45b9e19669ea06d74c7f252ec885fe004
ms.sourcegitcommit: 462dc41a13942e467984e48f4018d1f79ae67346
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "58186089"
---
# <a name="train-a-machine-learning-model-with-data-thats-not-in-a-text-file---mlnet"></a><span data-ttu-id="3d0fb-103">Entraîner un modèle Machine Learning avec des données qui ne sont pas dans un fichier texte - ML.NET</span><span class="sxs-lookup"><span data-stu-id="3d0fb-103">Train a machine learning model with data that's not in a text file - ML.NET</span></span>

> [!NOTE]
> <span data-ttu-id="3d0fb-104">Cette rubrique fait référence à ML.NET, actuellement en préversion, et les ressources sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-104">This topic refers to ML.NET, which is currently in Preview, and material may be subject to change.</span></span> <span data-ttu-id="3d0fb-105">Pour plus d’informations, consultez [l’introduction à ML.NET](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span><span class="sxs-lookup"><span data-stu-id="3d0fb-105">For more information, visit [the ML.NET introduction](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).</span></span>

<span data-ttu-id="3d0fb-106">Ce guide pratique et l’exemple associé utilisent actuellement **ML.NET version 0.11**.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-106">This how-to and related sample are currently using **ML.NET version 0.11**.</span></span> <span data-ttu-id="3d0fb-107">Pour plus d’informations, voir les notes de publication dans le référentiel GitHub [dotnet/machinelearning](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span><span class="sxs-lookup"><span data-stu-id="3d0fb-107">For more information, see the release notes at the [dotnet/machinelearning GitHub repo](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).</span></span>

<span data-ttu-id="3d0fb-108">Le cas d’usage couramment illustré pour ML.NET est l’utilisation de `TextLoader` pour lire les données d’entraînement d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-108">The commonly demonstrated use case for ML.NET is use the `TextLoader` to read the training data from a file.</span></span>
<span data-ttu-id="3d0fb-109">Toutefois, dans les scénarios d’entraînement en temps réel, les données peuvent être ailleurs, par exemple :</span><span class="sxs-lookup"><span data-stu-id="3d0fb-109">However, in real-time training scenarios the data can be elsewhere, such as:</span></span>

* <span data-ttu-id="3d0fb-110">dans des tables SQL</span><span class="sxs-lookup"><span data-stu-id="3d0fb-110">in SQL tables</span></span>
* <span data-ttu-id="3d0fb-111">JSON/XML</span><span class="sxs-lookup"><span data-stu-id="3d0fb-111">JSON/XML</span></span>
* <span data-ttu-id="3d0fb-112">extraites de fichiers journaux</span><span class="sxs-lookup"><span data-stu-id="3d0fb-112">extracted from log files</span></span>
* <span data-ttu-id="3d0fb-113">générées à la volée</span><span class="sxs-lookup"><span data-stu-id="3d0fb-113">generated on the fly</span></span>

<span data-ttu-id="3d0fb-114">Utilisez [schema comprehension](https://github.com/dotnet/machinelearning/tree/master/docs/code/SchemaComprehension.md) pour apporter un `IEnumerable` C# existant dans ML.NET comme `DataView`.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-114">Use [schema comprehension](https://github.com/dotnet/machinelearning/tree/master/docs/code/SchemaComprehension.md) to bring an existing C# `IEnumerable` into ML.NET as a `DataView`.</span></span>

<span data-ttu-id="3d0fb-115">Pour cet exemple, vous allez générer le modèle de prédiction de baisse du client et extraire les fonctionnalités suivantes à partir de votre système de production :</span><span class="sxs-lookup"><span data-stu-id="3d0fb-115">For this example, you'll build the customer churn prediction model, and extract the following features from your production system:</span></span>

* <span data-ttu-id="3d0fb-116">ID du client (ignoré par le modèle)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-116">Customer ID (ignored by the model)</span></span>
* <span data-ttu-id="3d0fb-117">Si le client a baissé (« l'étiquette » cible)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-117">Whether the customer has churned (the target 'label')</span></span>
* <span data-ttu-id="3d0fb-118">La « catégorie démographique » (une chaîne, comme « jeunes adultes » etc.)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-118">The 'demographic category' (one string, like 'young adult' etc.)</span></span>
* <span data-ttu-id="3d0fb-119">Le nombre de visites des 5 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-119">The number of visits from the last 5 days.</span></span>

```csharp
private class CustomerChurnInfo
{
    public string CustomerID { get; set; }
    public bool HasChurned { get; set; }
    public string DemographicCategory { get; set; }
    // Visits during last 5 days, latest to newest.
    [VectorType(5)]
    public float[] LastVisits { get; set; }
}
```

<span data-ttu-id="3d0fb-120">Chargez ces données dans le `DataView` et entraînez le modèle avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3d0fb-120">Load this data into the `DataView` and train the model, using the following code:</span></span>

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging,
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Step one: read the data as an IDataView.
// Let's assume that 'GetChurnData()' fetches and returns the training data from somewhere.
IEnumerable<CustomerChurnInfo> churnData = GetChurnInfo();

// Turn the data into the ML.NET data view.
// We can use CreateDataView or CreateStreamingDataView, depending on whether 'churnData' is an IList,
// or merely an IEnumerable.
var trainData = mlContext.Data.LoadFromEnumerable(churnData);

// Build the learning pipeline.
// In our case, we will one-hot encode the demographic category, and concatenate that with the number of visits.
// We apply our FastTree binary classifier to predict the 'HasChurned' label.

var pipeline = mlContext.Transforms.Categorical.OneHotEncoding("DemographicCategory")
    .Append(mlContext.Transforms.Concatenate("Features", "DemographicCategory", "LastVisits"))
    .Append(mlContext.BinaryClassification.Trainers.FastTree("HasChurned", "Features", numTrees: 20));

var model = pipeline.Fit(trainData);
```
