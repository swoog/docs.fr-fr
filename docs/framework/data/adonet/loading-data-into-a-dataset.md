---
title: Chargement de données dans un DataSet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a53e5dc1-9669-49d4-828d-efa633237066
ms.openlocfilehash: cb5578d790e5d3f54f75f964bb3288d861c9d7c3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59074051"
---
# <a name="loading-data-into-a-dataset"></a><span data-ttu-id="28648-102">Chargement de données dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="28648-102">Loading Data Into a DataSet</span></span>
<span data-ttu-id="28648-103">Un objet <xref:System.Data.DataSet> doit être rempli avant que vous puissiez l'interroger avec [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span><span class="sxs-lookup"><span data-stu-id="28648-103">A <xref:System.Data.DataSet> object must first be populated before you can query over it with [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span></span> <span data-ttu-id="28648-104">Il existe plusieurs manières de remplir le <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="28648-104">There are several different ways to populate the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="28648-105">Par exemple, vous pouvez utiliser [!INCLUDE[vbtecdlinq](../../../../includes/vbtecdlinq-md.md)] pour interroger la base de données et de charger les résultats dans le <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="28648-105">For example, you can use [!INCLUDE[vbtecdlinq](../../../../includes/vbtecdlinq-md.md)] to query the database and load the results into the <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="28648-106">Pour plus d’informations, consultez [LINQ to SQL](../../../../docs/framework/data/adonet/sql/linq/index.md).</span><span class="sxs-lookup"><span data-stu-id="28648-106">For more information, see [LINQ to SQL](../../../../docs/framework/data/adonet/sql/linq/index.md).</span></span>  
  
 <span data-ttu-id="28648-107">Une autre manière de charger des données dans un <xref:System.Data.DataSet> consiste à utiliser la classe <xref:System.Data.Common.DataAdapter> pour extraire des données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="28648-107">Another common way to load data into a <xref:System.Data.DataSet> is to use the <xref:System.Data.Common.DataAdapter> class to retrieve data from the database.</span></span> <span data-ttu-id="28648-108">L'exemple suivant illustre cette opération.</span><span class="sxs-lookup"><span data-stu-id="28648-108">This is illustrated in the following example.</span></span>  
  
## <a name="example"></a><span data-ttu-id="28648-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="28648-109">Example</span></span>  
 <span data-ttu-id="28648-110">Cet exemple utilise un <xref:System.Data.Common.DataAdapter> pour interroger la base de données AdventureWorks et en extraire des informations de vente à partir de l'année 2002, et charge les résultats dans un <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="28648-110">This example uses a <xref:System.Data.Common.DataAdapter> to query the AdventureWorks database for sales information from the year 2002, and loads the results into a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="28648-111">Une fois que le <xref:System.Data.DataSet> a été rempli, vous pouvez y exécuter des requêtes à l'aide de [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span><span class="sxs-lookup"><span data-stu-id="28648-111">After the <xref:System.Data.DataSet> has been populated, you can write queries against it by using [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span></span> <span data-ttu-id="28648-112">Le `FillDataSet` méthode dans cet exemple est utilisée dans les exemples de requêtes de [exemples LINQ to DataSet](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md).</span><span class="sxs-lookup"><span data-stu-id="28648-112">The `FillDataSet` method in this example is used in the example queries in [LINQ to DataSet Examples](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md).</span></span> <span data-ttu-id="28648-113">Pour plus d’informations, consultez [interrogation de DataSets](../../../../docs/framework/data/adonet/querying-datasets-linq-to-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="28648-113">For more information, see [Querying DataSets](../../../../docs/framework/data/adonet/querying-datasets-linq-to-dataset.md).</span></span>  
  
 [!code-csharp[DP LINQ to DataSet Examples#FillDataSet](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#filldataset)]
 [!code-vb[DP LINQ to DataSet Examples#FillDataSet](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#filldataset)]  
  
## <a name="see-also"></a><span data-ttu-id="28648-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28648-114">See also</span></span>

- [<span data-ttu-id="28648-115">Vue d'ensemble de LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="28648-115">LINQ to DataSet Overview</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-overview.md)
- [<span data-ttu-id="28648-116">Interrogation de DataSets</span><span class="sxs-lookup"><span data-stu-id="28648-116">Querying DataSets</span></span>](../../../../docs/framework/data/adonet/querying-datasets-linq-to-dataset.md)
- [<span data-ttu-id="28648-117">Exemples de LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="28648-117">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)
