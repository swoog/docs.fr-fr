---
title: Inspecter les valeurs de données intermédiaires lors du traitement dans ML.NET
description: Découvrez comment inspecter les valeurs de données intermédiaires pendant le traitement du pipeline de machine learning de ML.NET
ms.date: 04/29/2019
author: luisquintanilla
ms.author: luquinta
ms.custom: mvc, how-to
ms.openlocfilehash: 06c4a473841db62a10dfc24025f842df7ae2c583
ms.sourcegitcommit: ca2ca60e6f5ea327f164be7ce26d9599e0f85fe4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65063518"
---
# <a name="inspect-intermediate-data-values-during-processing"></a><span data-ttu-id="2d579-103">Inspecter les valeurs de données intermédiaires lors du traitement</span><span class="sxs-lookup"><span data-stu-id="2d579-103">Inspect intermediate data values during processing</span></span>

<span data-ttu-id="2d579-104">Découvrez comment inspecter les valeurs pendant les étapes de chargement, de traitement et d’entraînement dans ML.NET.</span><span class="sxs-lookup"><span data-stu-id="2d579-104">Learn how to inspect values during loading, processing and training steps in ML.NET.</span></span>

<span data-ttu-id="2d579-105">Les données telles que celles représentées ci-dessous qui sont chargées dans un [`IDataView`](xref:Microsoft.ML.IDataView) peuvent être inspectées de plusieurs façons dans ML.NET.</span><span class="sxs-lookup"><span data-stu-id="2d579-105">Data like the one represented below which is loaded into an [`IDataView`](xref:Microsoft.ML.IDataView) can be inspected in various ways in ML.NET.</span></span>
 
```csharp
HousingData[] housingData = new HousingData[]
{
    new HousingData
    {
        Size = 600f,
        HistoricalPrices = new float[] { 100000f ,125000f ,122000f },
        CurrentPrice = 170000f
    },
    new HousingData
    {
        Size = 1000f,
        HistoricalPrices = new float[] { 200000f, 250000f, 230000f },
        CurrentPrice = 225000f
    },
    new HousingData
    {
        Size = 1000f,
        HistoricalPrices = new float[] { 126000f, 130000f, 200000f },
        CurrentPrice = 195000f
    },
    new HousingData
    {
        Size = 850f,
        HistoricalPrices = new float[] { 150000f,175000f,210000f },
        CurrentPrice = 205000f
    },
    new HousingData
    {
        Size = 900f,
        HistoricalPrices = new float[] { 155000f, 190000f, 220000f },
        CurrentPrice = 210000f
    },
    new HousingData
    {
        Size = 550f,
        HistoricalPrices = new float[] { 99000f, 98000f, 130000f },
        CurrentPrice = 180000f
    }
};
```

## <a name="convert-idataview-to-ienumerable"></a><span data-ttu-id="2d579-106">Convertir IDataView en IEnumerable</span><span class="sxs-lookup"><span data-stu-id="2d579-106">Convert IDataView to IEnumerable</span></span>

<span data-ttu-id="2d579-107">Un des moyens les plus rapides pour inspecter les valeurs d’un [`IDataView`](xref:Microsoft.ML.IDataView) consiste à le convertir en un [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601).</span><span class="sxs-lookup"><span data-stu-id="2d579-107">One of the quickest ways to inspect the values of an [`IDataView`](xref:Microsoft.ML.IDataView) is to convert it to an [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601).</span></span> <span data-ttu-id="2d579-108">Pour convertir un [`IDataView`](xref:Microsoft.ML.IDataView) en [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601), utilisez la méthode [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*).</span><span class="sxs-lookup"><span data-stu-id="2d579-108">To convert an [`IDataView`](xref:Microsoft.ML.IDataView) to [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) use the [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*) method.</span></span> 

<span data-ttu-id="2d579-109">Pour optimiser les performances, définissez la valeur de `reuseRowObject` sur `true`.</span><span class="sxs-lookup"><span data-stu-id="2d579-109">To optimize performance, set the value of `reuseRowObject` to `true`.</span></span> <span data-ttu-id="2d579-110">Cette opération remplit tardivement le même objet avec les données de la ligne actuelle au moment de son évaluation, par opposition à la création d’un objet pour chaque ligne dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="2d579-110">Doing so will lazily populate the same object with the data of the current row as it's being evaluated as opposed to creating a new object for each row in the dataset.</span></span>

```csharp
// Create an IEnumerable of HousingData objects from IDataView
IEnumerable<HousingData> housingDataEnumerable =
    mlContext.Data.CreateEnumerable<HousingData>(data, reuseRowObject: true);

// Iterate over each row
foreach (HousingData row in housingDataEnumerable)
{
    // Do something (print out Size property) with current Housing Data object being evaluated
    Console.WriteLine(row.Size);
}
```

<span data-ttu-id="2d579-111">Si vous devez uniquement accéder à une partie des données ou à des index spécifiques, utilisez [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*) et définissez la valeur du paramètre `reuseRowObject` sur `false` afin qu’un objet soit créé pour chaque ligne demandée dans le jeu de données.</span><span class="sxs-lookup"><span data-stu-id="2d579-111">If you only need access to a portion of the data or specific indices, use [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*) and set the `reuseRowObject` parameter value to `false` so a new object is created for each of the requested rows in the dataset.</span></span> <span data-ttu-id="2d579-112">Convertissez ensuite le [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) en tableau ou liste.</span><span class="sxs-lookup"><span data-stu-id="2d579-112">Then, convert the [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) to an array or list.</span></span>

> [!WARNING]
> <span data-ttu-id="2d579-113">La conversion du résultat de [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*) en tableau ou liste charge en mémoire toutes les lignes [`IDataView`](xref:Microsoft.ML.IDataView) demandées, ce qui peut affecter les performances.</span><span class="sxs-lookup"><span data-stu-id="2d579-113">Converting the result of [`CreateEnumerable`](xref:Microsoft.ML.DataOperationsCatalog.CreateEnumerable*) to an array or list will load all the requested [`IDataView`](xref:Microsoft.ML.IDataView) rows into memory which may affect performance.</span></span>

<span data-ttu-id="2d579-114">Une fois la collection créée, vous pouvez effectuer des opérations sur les données.</span><span class="sxs-lookup"><span data-stu-id="2d579-114">Once the collection has been created, you can perform operations on the data.</span></span> <span data-ttu-id="2d579-115">L’extrait de code ci-dessous prend les trois premières lignes du jeu de données et calcule le prix moyen actuel.</span><span class="sxs-lookup"><span data-stu-id="2d579-115">The code snippet below takes the first three rows in the dataset and calculates the average current price.</span></span>

```csharp
// Create an Array of HousingData objects from IDataView
HousingData[] housingDataArray =
    mlContext.Data.CreateEnumerable<HousingData>(data, reuseRowObject: false)
        .Take(3)
        .ToArray();

// Calculate Average CurrentPrice of First Three Elements
HousingData firstRow = housingDataArray[0];
HousingData secondRow = housingDataArray[1];
HousingData thirdRow = housingDataArray[2];
float averageCurrentPrice = (firstRow.CurrentPrice + secondRow.CurrentPrice + thirdRow.CurrentPrice) / 3;
``` 

## <a name="inspect-values-in-a-single-column"></a><span data-ttu-id="2d579-116">Inspecter les valeurs d’une colonne spécifique</span><span class="sxs-lookup"><span data-stu-id="2d579-116">Inspect values in a single column</span></span>

<span data-ttu-id="2d579-117">À n’importe quel point du processus de génération de modèle, les valeurs d’une colonne spécifique d’un [`IDataView`](xref:Microsoft.ML.IDataView) sont accessibles à l’aide de la méthode [`GetColumn`](xref:Microsoft.ML.Data.ColumnCursorExtensions.GetColumn*).</span><span class="sxs-lookup"><span data-stu-id="2d579-117">At any point in the model building process, values in a single column of an [`IDataView`](xref:Microsoft.ML.IDataView) can be accessed using the [`GetColumn`](xref:Microsoft.ML.Data.ColumnCursorExtensions.GetColumn*) method.</span></span> <span data-ttu-id="2d579-118">La méthode [`GetColumn`](xref:Microsoft.ML.Data.ColumnCursorExtensions.GetColumn*) retourne toutes les valeurs d’une colonne spécifique sous la forme d’un [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601).</span><span class="sxs-lookup"><span data-stu-id="2d579-118">The [`GetColumn`](xref:Microsoft.ML.Data.ColumnCursorExtensions.GetColumn*) method returns all of the values in a single column as an [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601).</span></span>

```csharp
IEnumerable<float> sizeColumn = data.GetColumn<float>("Size").ToList();
```

## <a name="inspect-idataview-values-one-row-at-a-time"></a><span data-ttu-id="2d579-119">Inspecter les valeurs d’IDataView une ligne à la fois</span><span class="sxs-lookup"><span data-stu-id="2d579-119">Inspect IDataView values one row at a time</span></span>

<span data-ttu-id="2d579-120">[`IDataView`](xref:Microsoft.ML.IDataView) est évalué tardivement.</span><span class="sxs-lookup"><span data-stu-id="2d579-120">[`IDataView`](xref:Microsoft.ML.IDataView) is lazily evaluated.</span></span> <span data-ttu-id="2d579-121">Pour effectuer une itération sur les lignes d’un [`IDataView`](xref:Microsoft.ML.IDataView) sans opérer de conversion en [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) comme illustré dans les sections précédentes de ce document, créez un [`DataViewRowCursor`](xref:Microsoft.ML.DataViewRowCursor) en utilisant la méthode [`GetRowCursor`](xref:Microsoft.ML.IDataView.GetRowCursor*) et en passant le [DataViewSchema](xref:Microsoft.ML.DataViewSchema) de votre [`IDataView`](xref:Microsoft.ML.IDataView) comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="2d579-121">To iterate over the rows of an [`IDataView`](xref:Microsoft.ML.IDataView) without converting to an [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) as demonstrated in previous sections of this document, create a [`DataViewRowCursor`](xref:Microsoft.ML.DataViewRowCursor) by using the [`GetRowCursor`](xref:Microsoft.ML.IDataView.GetRowCursor*) method and passing in the [DataViewSchema](xref:Microsoft.ML.DataViewSchema) of your [`IDataView`](xref:Microsoft.ML.IDataView) as a parameter.</span></span> <span data-ttu-id="2d579-122">Ensuite, pour effectuer une itération sur les lignes, utilisez la méthode de curseur [`MoveNext`](xref:Microsoft.ML.DataViewRowCursor.MoveNext*) avec des délégués [`ValueGetter`](xref:Microsoft.ML.ValueGetter%601) pour extraire les valeurs respectives de chacune des colonnes.</span><span class="sxs-lookup"><span data-stu-id="2d579-122">Then, to iterate over rows, use the [`MoveNext`](xref:Microsoft.ML.DataViewRowCursor.MoveNext*) cursor method along with [`ValueGetter`](xref:Microsoft.ML.ValueGetter%601) delegates to extract the respective values from each of the columns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d579-123">Pour des raisons de performances, les vecteurs dans ML.NET utilisent [`VBuffer`](xref:Microsoft.ML.Data.VBuffer%601) au lieu de types de collection native (autrement dit, `Vector`,`float[]`).</span><span class="sxs-lookup"><span data-stu-id="2d579-123">For performance purposes, vectors in ML.NET use [`VBuffer`](xref:Microsoft.ML.Data.VBuffer%601) instead of native collection types (that is, `Vector`,`float[]`).</span></span> 

```csharp
// Get DataViewSchema of IDataView
DataViewSchema columns = data.Schema;

// Create DataViewCursor
using (DataViewRowCursor cursor = data.GetRowCursor(columns))
{
    // Define variables where extracted values will be stored to
    float size = default;
    VBuffer<float> historicalPrices = default;
    float currentPrice = default;

    // Define delegates for extracting values from columns
    ValueGetter<float> sizeDelegate = cursor.GetGetter<float>(columns[0]);
    ValueGetter<VBuffer<float>> historicalPriceDelegate = cursor.GetGetter<VBuffer<float>>(columns[1]);
    ValueGetter<float> currentPriceDelegate = cursor.GetGetter<float>(columns[2]);
    
    // Iterate over each row
    while (cursor.MoveNext())
    {
        //Get values from respective columns
        sizeDelegate.Invoke(ref size);
        historicalPriceDelegate.Invoke(ref historicalPrices);
        currentPriceDelegate.Invoke(ref currentPrice);
    }
}
```

## <a name="preview-result-of-pre-processing-or-training-on-a-subset-of-the-data"></a><span data-ttu-id="2d579-124">Obtenir un aperçu du résultat du prétraitement ou de l’entraînement sur un sous-ensemble des données</span><span class="sxs-lookup"><span data-stu-id="2d579-124">Preview result of pre-processing or training on a subset of the data</span></span>

> [!WARNING]
> <span data-ttu-id="2d579-125">N’utilisez pas `Preview` dans le code de production, car celui-ci est destiné au débogage et peut réduire les performances.</span><span class="sxs-lookup"><span data-stu-id="2d579-125">Do not use `Preview` in production code because it is intended for debugging and may reduce performance.</span></span>

<span data-ttu-id="2d579-126">Le processus de génération de modèle est expérimental et itératif.</span><span class="sxs-lookup"><span data-stu-id="2d579-126">The model building process is experimental and iterative.</span></span> <span data-ttu-id="2d579-127">Pour obtenir un aperçu de ce à quoi ressembleraient les données après le prétraitement ou l’entraînement d’un modèle Machine Learning sur un sous-ensemble des données, utilisez la méthode [`Preview`](xref:Microsoft.ML.DebuggerExtensions.Preview*), qui retourne un [`DataDebuggerPreview`](xref:Microsoft.ML.Data.DataDebuggerPreview).</span><span class="sxs-lookup"><span data-stu-id="2d579-127">To preview what data would look like after pre-processing or training a machine learning model on a subset of the data, use the [`Preview`](xref:Microsoft.ML.DebuggerExtensions.Preview*) method which returns a [`DataDebuggerPreview`](xref:Microsoft.ML.Data.DataDebuggerPreview).</span></span> <span data-ttu-id="2d579-128">Le résultat est un objet avec des propriétés `ColumnView` et `RowView` qui sont toutes deux un [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) et contiennent les valeurs dans une ligne ou une colonne particulière.</span><span class="sxs-lookup"><span data-stu-id="2d579-128">The result is an object with `ColumnView` and `RowView` properties which are both an [`IEnumerable`](xref:System.Collections.Generic.IEnumerable%601) and contain the values in a particular column or row.</span></span> <span data-ttu-id="2d579-129">Spécifiez le nombre de lignes auxquelles appliquer la transformation à l’aide du paramètre `maxRows`.</span><span class="sxs-lookup"><span data-stu-id="2d579-129">Specify the number of rows to apply the transformation to with the `maxRows` parameter.</span></span>

![Débogueur de données : aperçu de l’objet](./media/inspect-intermediate-data-ml-net/data-debugger-preview-01.png)

<span data-ttu-id="2d579-131">Le résultat de l’inspection d’un [`IDataView`](xref:Microsoft.ML.IDataView) devrait être semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="2d579-131">The result of inspecting an [`IDataView`](xref:Microsoft.ML.IDataView) would look similar to the following:</span></span>

![Débogueur de données : aperçu de la vue de ligne](./media/inspect-intermediate-data-ml-net/data-debugger-preview-02.png)
