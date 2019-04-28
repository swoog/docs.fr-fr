---
title: 'Procédure : Récupérer plusieurs objets à la fois'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 18aff4d8-bde8-461b-9960-ccabb24e9d22
ms.openlocfilehash: dd53c2fd16a82ce0f69a33e0b7d7ffef7815b91b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61877147"
---
# <a name="how-to-retrieve-many-objects-at-once"></a><span data-ttu-id="7731f-102">Procédure : Récupérer plusieurs objets à la fois</span><span class="sxs-lookup"><span data-stu-id="7731f-102">How to: Retrieve Many Objects At Once</span></span>
<span data-ttu-id="7731f-103">Vous pouvez récupérer plusieurs objets dans une requête en utilisant <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span><span class="sxs-lookup"><span data-stu-id="7731f-103">You can retrieve many objects in one query by using <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7731f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7731f-104">Example</span></span>  
 <span data-ttu-id="7731f-105">Le code suivant utilise la méthode <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> pour récupérer des objets `Customer` et `Order`.</span><span class="sxs-lookup"><span data-stu-id="7731f-105">The following code uses the <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> method to retrieve both `Customer` and `Order` objects.</span></span>  
  
 [!code-csharp[DLinqQueryConcepts#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#9)]
 [!code-vb[DLinqQueryConcepts#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="7731f-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7731f-106">See also</span></span>

- [<span data-ttu-id="7731f-107">Concepts relatifs aux requêtes</span><span class="sxs-lookup"><span data-stu-id="7731f-107">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
