---
title: 'Comment : exécuter directement des commandes SQL'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 04671bb0-40c0-4465-86e5-77986f454661
ms.openlocfilehash: 90fb0d7027946ce4f38c2ba4930ac3510e2a42b7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33351870"
---
# <a name="how-to-directly-execute-sql-commands"></a>Comment : exécuter directement des commandes SQL
En considérant une connexion <xref:System.Data.Linq.DataContext>, vous pouvez utiliser <xref:System.Data.Linq.DataContext.ExecuteCommand%2A> pour exécuter des commandes SQL qui ne retournent pas d'objets.  
  
## <a name="example"></a>Exemple  
 Dans l'exemple, SQL Server augmente de 1 la valeur de UnitPrice.  
  
 [!code-csharp[DLinqCommunicatingWithDatabase#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCommunicatingWithDatabase/cs/Program.cs#3)]
 [!code-vb[DLinqCommunicatingWithDatabase#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCommunicatingWithDatabase/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour exécuter directement des requêtes SQL](../../../../../../docs/framework/data/adonet/sql/linq/how-to-directly-execute-sql-queries.md)  
 [Communication avec la base de données](../../../../../../docs/framework/data/adonet/sql/linq/communicating-with-the-database.md)
