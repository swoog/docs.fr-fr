---
title: 'Procédure : Gérer les clés composites dans les requêtes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ce2f14fd-1038-458a-91e3-a078c61f0d10
ms.openlocfilehash: 2621ab4db207d1b868fbe3778c30c744201b0506
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59135250"
---
# <a name="how-to-handle-composite-keys-in-queries"></a><span data-ttu-id="14fd8-102">Procédure : Gérer les clés composites dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="14fd8-102">How to: Handle Composite Keys in Queries</span></span>
<span data-ttu-id="14fd8-103">Certains opérateurs ne peuvent prendre qu’un seul argument.</span><span class="sxs-lookup"><span data-stu-id="14fd8-103">Some operators can take only one argument.</span></span> <span data-ttu-id="14fd8-104">Si votre argument doit inclure plusieurs colonnes de la base de données, vous devez créer un type anonyme pour représenter la combinaison.</span><span class="sxs-lookup"><span data-stu-id="14fd8-104">If your argument must include more than one column from the database, you must create an anonymous type to represent the combination.</span></span>  
  
## <a name="example"></a><span data-ttu-id="14fd8-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="14fd8-105">Example</span></span>  
 <span data-ttu-id="14fd8-106">L’exemple suivant présente une requête qui appelle l’opérateur `GroupBy` et qui peut prendre un seul argument `key`.</span><span class="sxs-lookup"><span data-stu-id="14fd8-106">The following example shows a query that invokes the `GroupBy` operator, which can take only one `key` argument.</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#1)]
 [!code-vb[DLinqCompositeKeys#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="14fd8-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="14fd8-107">Example</span></span>  
 <span data-ttu-id="14fd8-108">La même situation s'applique aux jointures, comme dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="14fd8-108">The same situation pertains to joins, as in the following example:</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#2)]
 [!code-vb[DLinqCompositeKeys#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="14fd8-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14fd8-109">See also</span></span>

- [<span data-ttu-id="14fd8-110">Concepts relatifs aux requêtes</span><span class="sxs-lookup"><span data-stu-id="14fd8-110">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
