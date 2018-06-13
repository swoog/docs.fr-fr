---
title: 'Comment : mettre entre parenthèses des soumissions de données à l’aide de transactions'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 94044a31-de90-479b-935a-8159b4ae5c5a
ms.openlocfilehash: aa77d364d1ee4efc09386dd7e889914aeb2f3f26
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361525"
---
# <a name="how-to-bracket-data-submissions-by-using-transactions"></a><span data-ttu-id="958b6-102">Comment : mettre entre parenthèses des soumissions de données à l’aide de transactions</span><span class="sxs-lookup"><span data-stu-id="958b6-102">How to: Bracket Data Submissions by Using Transactions</span></span>
<span data-ttu-id="958b6-103">Vous pouvez utiliser <xref:System.Transactions.TransactionScope> pour mettre entre parenthèses vos soumissions à la base de données.</span><span class="sxs-lookup"><span data-stu-id="958b6-103">You can use <xref:System.Transactions.TransactionScope> to bracket your submissions to the database.</span></span> <span data-ttu-id="958b6-104">Pour plus d’informations, consultez [prise en charge des transactions](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md).</span><span class="sxs-lookup"><span data-stu-id="958b6-104">For more information, see [Transaction Support](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="958b6-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="958b6-105">Example</span></span>  
 <span data-ttu-id="958b6-106">Le code suivant place la soumission de base de données dans un <xref:System.Transactions.TransactionScope>.</span><span class="sxs-lookup"><span data-stu-id="958b6-106">The following code encloses the database submission in a <xref:System.Transactions.TransactionScope>.</span></span>  
  
 [!code-csharp[DLinqSubmittingChanges#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#3)]
 [!code-vb[DLinqSubmittingChanges#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="958b6-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="958b6-107">See Also</span></span>  
 [<span data-ttu-id="958b6-108">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="958b6-108">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)  
 [<span data-ttu-id="958b6-109">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="958b6-109">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)  
 [<span data-ttu-id="958b6-110">Prise en charge des transactions</span><span class="sxs-lookup"><span data-stu-id="958b6-110">Transaction Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md)
