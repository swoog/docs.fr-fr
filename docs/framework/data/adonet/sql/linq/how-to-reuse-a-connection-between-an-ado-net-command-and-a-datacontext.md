---
title: 'Procédure : Réutiliser une connexion entre une commande ADO.NET et un DataContext'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7e26c7eb-c18a-43b5-a8f0-28fd8b04b0f0
ms.openlocfilehash: 079b4b28a613ce6a9ae525514b89ea9e316a7c66
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54613673"
---
# <a name="how-to-reuse-a-connection-between-an-adonet-command-and-a-datacontext"></a><span data-ttu-id="aef6c-102">Procédure : Réutiliser une connexion entre une commande ADO.NET et un DataContext</span><span class="sxs-lookup"><span data-stu-id="aef6c-102">How to: Reuse a Connection Between an ADO.NET Command and a DataContext</span></span>
<span data-ttu-id="aef6c-103">Étant donné que [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] fait partie de la [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] famille de technologies et est basé sur les services fournis par [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)], vous pouvez réutiliser une connexion entre un [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] commande et un <xref:System.Data.Linq.DataContext>.</span><span class="sxs-lookup"><span data-stu-id="aef6c-103">Because [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] is a part of the [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] family of technologies and is based on services provided by [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)], you can reuse a connection between an [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] command and a <xref:System.Data.Linq.DataContext>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="aef6c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="aef6c-104">Example</span></span>  
 <span data-ttu-id="aef6c-105">L'exemple suivant indique comment réutiliser la même connexion entre une commande [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] et le <xref:System.Data.Linq.DataContext>.</span><span class="sxs-lookup"><span data-stu-id="aef6c-105">The following example shows how to reuse the same connection between an [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] command and the <xref:System.Data.Linq.DataContext>.</span></span>  
  
 [!code-csharp[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCommunicatingWithDatabase/cs/Program.cs#4)]
 [!code-vb[DLinqCommunicatingWithDatabase#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCommunicatingWithDatabase/vb/Module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="aef6c-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aef6c-106">See also</span></span>
- [<span data-ttu-id="aef6c-107">Informations générales</span><span class="sxs-lookup"><span data-stu-id="aef6c-107">Background Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
- [<span data-ttu-id="aef6c-108">ADO.NET et LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="aef6c-108">ADO.NET and LINQ to SQL</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/ado-net-and-linq-to-sql.md)
- [<span data-ttu-id="aef6c-109">Communication avec la base de données</span><span class="sxs-lookup"><span data-stu-id="aef6c-109">Communicating with the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/communicating-with-the-database.md)
