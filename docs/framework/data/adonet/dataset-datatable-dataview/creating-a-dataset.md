---
title: Création d'un DataSet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 57629d8f-393e-4677-8b83-29ffde27f5fc
ms.openlocfilehash: d2d17056e6dcd29ef9b5c5e8c3024a32fce32bd5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59118181"
---
# <a name="creating-a-dataset"></a><span data-ttu-id="21b92-102">Création d'un DataSet</span><span class="sxs-lookup"><span data-stu-id="21b92-102">Creating a DataSet</span></span>
<span data-ttu-id="21b92-103">Pour créer une instance d'un objet <xref:System.Data.DataSet>, appelez le constructeur de l'objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="21b92-103">You create an instance of a <xref:System.Data.DataSet> by calling the <xref:System.Data.DataSet> constructor.</span></span> <span data-ttu-id="21b92-104">Vous pouvez également spécifier un argument de nom.</span><span class="sxs-lookup"><span data-stu-id="21b92-104">Optionally specify a name argument.</span></span> <span data-ttu-id="21b92-105">Si vous ne spécifiez pas de nom pour l'objet <xref:System.Data.DataSet>, le nom est défini sur « NewDataSet ».</span><span class="sxs-lookup"><span data-stu-id="21b92-105">If you do not specify a name for the <xref:System.Data.DataSet>, the name is set to "NewDataSet".</span></span>  
  
 <span data-ttu-id="21b92-106">Vous pouvez également créer un objet <xref:System.Data.DataSet> à partir d'un objet <xref:System.Data.DataSet> existant.</span><span class="sxs-lookup"><span data-stu-id="21b92-106">You can also create a new <xref:System.Data.DataSet> based on an existing <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="21b92-107">Le nouvel objet <xref:System.Data.DataSet> peut être : une copie exacte de l'objet <xref:System.Data.DataSet> existant ; un clône de l'objet <xref:System.Data.DataSet> qui copie la structure relationnelle ou le schéma, mais sans aucune des données de l'objet <xref:System.Data.DataSet> existant ; un sous-ensemble de l'objet <xref:System.Data.DataSet>, qui ne contient que les lignes modifiées de l'objet <xref:System.Data.DataSet> existant, à l'aide de la méthode <xref:System.Data.DataSet.GetChanges%2A>.</span><span class="sxs-lookup"><span data-stu-id="21b92-107">The new <xref:System.Data.DataSet> can be an exact copy of the existing <xref:System.Data.DataSet>; a clone of the <xref:System.Data.DataSet> that copies the relational structure or schema but that does not contain any of the data from the existing <xref:System.Data.DataSet>; or a subset of the <xref:System.Data.DataSet>, containing only the modified rows from the existing <xref:System.Data.DataSet> using the <xref:System.Data.DataSet.GetChanges%2A> method.</span></span> <span data-ttu-id="21b92-108">Pour plus d’informations, consultez [contenu d’un DataSet copie](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md).</span><span class="sxs-lookup"><span data-stu-id="21b92-108">For more information, see [Copying DataSet Contents](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md).</span></span>  
  
 <span data-ttu-id="21b92-109">L'exemple de code suivant montre comment construire une instance d'un objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="21b92-109">The following code example demonstrates how to construct an instance of a <xref:System.Data.DataSet>.</span></span>  
  
```vb  
Dim customerOrders As DataSet = New DataSet("CustomerOrders")  
```  
  
```csharp  
DataSet customerOrders = new DataSet("CustomerOrders");  
```  
  
## <a name="see-also"></a><span data-ttu-id="21b92-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21b92-110">See also</span></span>

- [<span data-ttu-id="21b92-111">Remplissage d'un DataSet à partir d'un DataAdapter</span><span class="sxs-lookup"><span data-stu-id="21b92-111">Populating a DataSet from a DataAdapter</span></span>](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)
- [<span data-ttu-id="21b92-112">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="21b92-112">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="21b92-113">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="21b92-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
