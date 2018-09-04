---
title: Navigation sur les DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 202026a1-ec79-435e-b507-12a77f5011b2
ms.openlocfilehash: f00e2171c1adf4ff99a669085131ebc8d38f7006
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43538803"
---
# <a name="navigating-datatables"></a><span data-ttu-id="36258-102">Navigation sur les DataTable</span><span class="sxs-lookup"><span data-stu-id="36258-102">Navigating DataTables</span></span>
<span data-ttu-id="36258-103">L'objet <xref:System.Data.DataTableReader> obtient le contenu d'un ou plusieurs objets <xref:System.Data.DataTable> sous la forme d'un ou plusieurs jeux de résultats en lecture seule et en avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="36258-103">The <xref:System.Data.DataTableReader> obtains the contents of one or more <xref:System.Data.DataTable> objects in the form of one or more read-only, forward-only result sets.</span></span>  
  
 <span data-ttu-id="36258-104">Un objet <xref:System.Data.DataTableReader> peut contenir plusieurs jeux de résultats s'il est créé à l'aide de la méthode <xref:System.Data.DataSet.CreateDataReader%2A>.</span><span class="sxs-lookup"><span data-stu-id="36258-104">A <xref:System.Data.DataTableReader> may contain multiple result sets if it is created by using the <xref:System.Data.DataSet.CreateDataReader%2A> method.</span></span> <span data-ttu-id="36258-105">S'il y a plusieurs jeux de résultats, la méthode <xref:System.Data.DataTableReader.NextResult%2A> déplace le curseur sur le jeu de résultats suivant.</span><span class="sxs-lookup"><span data-stu-id="36258-105">When there is more than one result set, the <xref:System.Data.DataTableReader.NextResult%2A> method advances the cursor to the next result set.</span></span> <span data-ttu-id="36258-106">Il s'agit d'un processus en avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="36258-106">This is a forward-only process.</span></span> <span data-ttu-id="36258-107">Il n'est pas possible de revenir à un jeu de résultats précédent.</span><span class="sxs-lookup"><span data-stu-id="36258-107">It is not possible to return to a previous result set.</span></span>  
  
## <a name="example"></a><span data-ttu-id="36258-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="36258-108">Example</span></span>  
 <span data-ttu-id="36258-109">Dans l’exemple suivant, le `TestConstructor` méthode crée deux <xref:System.Data.DataTable> instances.</span><span class="sxs-lookup"><span data-stu-id="36258-109">In the following example, the `TestConstructor` method creates two <xref:System.Data.DataTable> instances.</span></span> <span data-ttu-id="36258-110">Pour montrer ce constructeur pour le <xref:System.Data.DataTableReader> (classe), l’exemple crée un **DataTableReader** basé sur un tableau qui contient les deux **DataTables**et effectue une opération simple, impression du contenu à partir des premières colonnes dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="36258-110">In order to demonstrate this constructor for the <xref:System.Data.DataTableReader> class, the sample creates a new **DataTableReader** based on an array that contains the two **DataTables**, and performs a simple operation, printing the contents from the first few columns to the console window.</span></span>  
  
 [!code-csharp[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/CS/source.cs#1)]
 [!code-vb[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="36258-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36258-111">See Also</span></span>  
 [<span data-ttu-id="36258-112">DataTableReaders</span><span class="sxs-lookup"><span data-stu-id="36258-112">DataTableReaders</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatablereaders.md)  
 [<span data-ttu-id="36258-113">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="36258-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
