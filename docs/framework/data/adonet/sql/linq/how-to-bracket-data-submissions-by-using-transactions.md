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
# <a name="how-to-bracket-data-submissions-by-using-transactions"></a>Procédure : Envoi de données entre parenthèses à l’aide de Transactions
Vous pouvez utiliser <xref:System.Transactions.TransactionScope> pour mettre entre parenthèses vos soumissions à la base de données. Pour plus d’informations, consultez [prise en charge de la Transaction](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md).  
  
## <a name="example"></a>Exemple  
 Le code suivant place la soumission de base de données dans un <xref:System.Transactions.TransactionScope>.  
  
 [!code-csharp[DLinqSubmittingChanges#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#3)]
 [!code-vb[DLinqSubmittingChanges#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi
- [Téléchargement d’exemples de base de données](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
- [Apport et soumission de modifications de données](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
- [Prise en charge des transactions](../../../../../../docs/framework/data/adonet/sql/linq/transaction-support.md)
