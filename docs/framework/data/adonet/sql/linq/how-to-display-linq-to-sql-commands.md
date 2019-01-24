---
title: 'Procédure : LINQ to SQL commandes d’affichage'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1decb05e-37ad-4ed6-ab2f-071eb4c4f628
ms.openlocfilehash: a70f1e0dd471e86afe2e744c157d4aed2a217deb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630825"
---
# <a name="how-to-display-linq-to-sql-commands"></a><span data-ttu-id="60b3f-102">Procédure : LINQ to SQL commandes d’affichage</span><span class="sxs-lookup"><span data-stu-id="60b3f-102">How to: Display LINQ to SQL Commands</span></span>
<span data-ttu-id="60b3f-103">Utilisez <xref:System.Data.Linq.DataContext.GetCommand%2A> pour afficher des commandes SQL et d'autres informations.</span><span class="sxs-lookup"><span data-stu-id="60b3f-103">Use <xref:System.Data.Linq.DataContext.GetCommand%2A> to display SQL commands and other information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="60b3f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="60b3f-104">Example</span></span>  
 <span data-ttu-id="60b3f-105">Dans l'exemple suivant, la fenêtre de console affiche la sortie de la requête, suivie des commandes SQL générées, du type des commandes et du type de connexion.</span><span class="sxs-lookup"><span data-stu-id="60b3f-105">In the following example, the console window displays the output from the query, followed by the SQL commands that are generated, the type of commands, and the type of connection.</span></span>  
  
 [!code-csharp[DLinqDebuggingSupport#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#3)]
 [!code-vb[DLinqDebuggingSupport#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#3)]  
  
 <span data-ttu-id="60b3f-106">Vous obtenez le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="60b3f-106">Output appears as follows:</span></span>  
  
```  
Customers from London:  
    Thomas Hardy  
    Victoria Ashworth  
    Elizabeth Brown  
    Ann Devon  
    Simon Crowther  
    Marie Bertrand  
    Hari Kumar  
    Dominique Perrier  
```  
  
```  
Command Text:  
SELECT [t0].[CustomerID], [t0].[CompanyName], [t0].[ContactName], [t0].[ContactT  
itle], [t0].[Address], [t0].[City], [t0].[Region], [t0].[PostalCode], [t0].[Coun  
try], [t0].[Phone], [t0].[Fax]  
FROM [dbo].[Customers] AS [t0]  
WHERE [t0].[City] = @p0  
  
Command Type: Text  
  
Connection: System.Data.SqlClient.SqlConnection  
```  
  
## <a name="see-also"></a><span data-ttu-id="60b3f-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b3f-107">See also</span></span>
- [<span data-ttu-id="60b3f-108">Prise en charge du débogage</span><span class="sxs-lookup"><span data-stu-id="60b3f-108">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
