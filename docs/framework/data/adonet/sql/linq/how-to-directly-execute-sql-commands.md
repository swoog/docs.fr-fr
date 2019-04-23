---
title: 'Procédure : Exécuter directement des commandes SQL'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 04671bb0-40c0-4465-86e5-77986f454661
ms.openlocfilehash: eeac6272f176ac8e780b72b0076d032ad9e8f108
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078900"
---
# <a name="how-to-directly-execute-sql-commands"></a><span data-ttu-id="da344-102">Procédure : Exécuter directement des commandes SQL</span><span class="sxs-lookup"><span data-stu-id="da344-102">How to: Directly Execute SQL Commands</span></span>
<span data-ttu-id="da344-103">En considérant une connexion <xref:System.Data.Linq.DataContext>, vous pouvez utiliser <xref:System.Data.Linq.DataContext.ExecuteCommand%2A> pour exécuter des commandes SQL qui ne retournent pas d'objets.</span><span class="sxs-lookup"><span data-stu-id="da344-103">Assuming a <xref:System.Data.Linq.DataContext> connection, you can use <xref:System.Data.Linq.DataContext.ExecuteCommand%2A> to execute SQL commands that do not return objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="da344-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="da344-104">Example</span></span>  
 <span data-ttu-id="da344-105">Dans l'exemple, SQL Server augmente de 1 la valeur de UnitPrice.</span><span class="sxs-lookup"><span data-stu-id="da344-105">The following example causes SQL Server to increase UnitPrice by 1.00.</span></span>  
  
 [!code-csharp[DLinqCommunicatingWithDatabase#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCommunicatingWithDatabase/cs/Program.cs#3)]
 [!code-vb[DLinqCommunicatingWithDatabase#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCommunicatingWithDatabase/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="da344-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da344-106">See also</span></span>

- [<span data-ttu-id="da344-107">Guide pratique pour Exécuter directement des requêtes SQL</span><span class="sxs-lookup"><span data-stu-id="da344-107">How to: Directly Execute SQL Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-directly-execute-sql-queries.md)
- [<span data-ttu-id="da344-108">Communication avec la base de données</span><span class="sxs-lookup"><span data-stu-id="da344-108">Communicating with the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/communicating-with-the-database.md)
