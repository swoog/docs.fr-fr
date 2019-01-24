---
title: 'Procédure : Envoi de données entre parenthèses à l’aide de Transactions'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 94044a31-de90-479b-935a-8159b4ae5c5a
ms.openlocfilehash: 2cbb50cc8762780849c337b597bbb36631c6ac1b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584530"
---
# <a name="how-to-bracket-data-submissions-by-using-transactions"></a><span data-ttu-id="e742d-102">Procédure : Envoi de données entre parenthèses à l’aide de Transactions</span><span class="sxs-lookup"><span data-stu-id="e742d-102">How to: Bracket Data Submissions by Using Transactions</span></span>
<span data-ttu-id="e742d-103">Vous pouvez utiliser <xref:System.Transactions.TransactionScope> pour mettre entre parenthèses vos soumissions à la base de données.</span><span class="sxs-lookup"><span data-stu-id="e742d-103">You can use <xref:System.Transactions.TransactionScope> to bracket your submissions to the database.</span></span> <span data-ttu-id="e742d-104">Pour plus d’informations, consultez [prise en charge de la Transaction](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md).</span><span class="sxs-lookup"><span data-stu-id="e742d-104">For more information, see [Transaction Support](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e742d-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="e742d-105">Example</span></span>  
 <span data-ttu-id="e742d-106">Le code suivant place la soumission de base de données dans un <xref:System.Transactions.TransactionScope>.</span><span class="sxs-lookup"><span data-stu-id="e742d-106">The following code encloses the database submission in a <xref:System.Transactions.TransactionScope>.</span></span>  
  
 [!code-csharp[DLinqSubmittingChanges#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#3)]
 [!code-vb[DLinqSubmittingChanges#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="e742d-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e742d-107">See also</span></span>
- [<span data-ttu-id="e742d-108">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="e742d-108">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
- [<span data-ttu-id="e742d-109">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="e742d-109">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
- [<span data-ttu-id="e742d-110">Prise en charge des transactions</span><span class="sxs-lookup"><span data-stu-id="e742d-110">Transaction Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md)
