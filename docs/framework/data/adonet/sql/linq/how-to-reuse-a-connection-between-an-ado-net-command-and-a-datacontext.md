---
title: 'Procédure : Réutiliser une connexion entre une commande ADO.NET et un DataContext'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7e26c7eb-c18a-43b5-a8f0-28fd8b04b0f0
ms.openlocfilehash: 92b0d8cf2c4904fabc17241ef2c31175f0c87baf
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65878535"
---
# <a name="how-to-reuse-a-connection-between-an-adonet-command-and-a-datacontext"></a><span data-ttu-id="c54b1-102">Procédure : Réutiliser une connexion entre une commande ADO.NET et un DataContext</span><span class="sxs-lookup"><span data-stu-id="c54b1-102">How to: Reuse a Connection Between an ADO.NET Command and a DataContext</span></span>
<span data-ttu-id="c54b1-103">Étant donné que [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] fait partie de la famille ADO.NET de technologies et basée sur les services fournis par ADO.NET, vous pouvez réutiliser une connexion entre une commande ADO.NET et un <xref:System.Data.Linq.DataContext>.</span><span class="sxs-lookup"><span data-stu-id="c54b1-103">Because [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] is a part of the ADO.NET family of technologies and is based on services provided by ADO.NET, you can reuse a connection between an ADO.NET command and a <xref:System.Data.Linq.DataContext>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c54b1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="c54b1-104">Example</span></span>  
 <span data-ttu-id="c54b1-105">L’exemple suivant montre comment réutiliser la même connexion entre une commande ADO.NET et la <xref:System.Data.Linq.DataContext>.</span><span class="sxs-lookup"><span data-stu-id="c54b1-105">The following example shows how to reuse the same connection between an ADO.NET command and the <xref:System.Data.Linq.DataContext>.</span></span>  
  
 [!code-csharp[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCommunicatingWithDatabase/cs/Program.cs#4)]
 [!code-vb[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCommunicatingWithDatabase/vb/Module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="c54b1-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c54b1-106">See also</span></span>

- [<span data-ttu-id="c54b1-107">Informations générales</span><span class="sxs-lookup"><span data-stu-id="c54b1-107">Background Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
- [<span data-ttu-id="c54b1-108">ADO.NET et LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="c54b1-108">ADO.NET and LINQ to SQL</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/ado-net-and-linq-to-sql.md)
- [<span data-ttu-id="c54b1-109">Communication avec la base de données</span><span class="sxs-lookup"><span data-stu-id="c54b1-109">Communicating with the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/communicating-with-the-database.md)
