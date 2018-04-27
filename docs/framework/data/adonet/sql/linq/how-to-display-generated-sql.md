---
title: 'Comment : afficher le code SQL généré'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 626492c0-5ee3-4675-88e8-8c40379510b6
caps.latest.revision: 2
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: c58e691bdf39e71a756c8b26451c22c769f05c0a
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-display-generated-sql"></a><span data-ttu-id="01875-102">Comment : afficher le code SQL généré</span><span class="sxs-lookup"><span data-stu-id="01875-102">How to: Display Generated SQL</span></span>
<span data-ttu-id="01875-103">Vous pouvez consulter le code SQL généré pour les requêtes et modifier le traitement à l'aide de la propriété <xref:System.Data.Linq.DataContext.Log%2A>.</span><span class="sxs-lookup"><span data-stu-id="01875-103">You can view the SQL code generated for queries and change processing by using the <xref:System.Data.Linq.DataContext.Log%2A> property.</span></span> <span data-ttu-id="01875-104">Cette approche peut être utile pour comprendre les fonctionnalités de [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] et déboguer des problèmes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="01875-104">This approach can be useful for understanding [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] functionality and for debugging specific problems.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01875-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="01875-105">Example</span></span>  
 <span data-ttu-id="01875-106">L'exemple suivant utilise la propriété <xref:System.Data.Linq.DataContext.Log%2A> pour afficher le code SQL dans la fenêtre de console avant que son exécution.</span><span class="sxs-lookup"><span data-stu-id="01875-106">The following example uses the <xref:System.Data.Linq.DataContext.Log%2A> property to display SQL code in the console window before the code is executed.</span></span>  <span data-ttu-id="01875-107">Vous pouvez utiliser cette propriété avec les commandes de requête, d'insertion, de mise à jour et de suppression.</span><span class="sxs-lookup"><span data-stu-id="01875-107">You can use this property with query, insert, update, and delete commands.</span></span>  
  
 <span data-ttu-id="01875-108">Les lignes à partir de la fenêtre de console sont ce que vous voyez lorsque vous exécutez le code Visual Basic ou c# qui suit.</span><span class="sxs-lookup"><span data-stu-id="01875-108">The lines from the console window are what you see when you execute the Visual Basic or C# code that follows.</span></span>  
  
```  
SELECT [t0].[CustomerID], [t0].[CompanyName], [t0].[ContactName], [t0].[ContactT  
itle], [t0].[Address], [t0].[City], [t0].[Region], [t0].[PostalCode], [t0].[Coun  
try], [t0].[Phone], [t0].[Fax]  
FROM [dbo].[Customers] AS [t0]  
WHERE [t0].[City] = @p0  
-- @p0: Input String (Size = 6; Prec = 0; Scale = 0) [London]  
-- Context: SqlProvider(Sql2005) Model: AttributedMetaModel Build: 3.5.20810.0  
```  
  
```  
AROUT  
BSBEV  
CONSH  
EASTC  
NORTS  
SEVES  
```  
  
 [!code-csharp[DLinqDebuggingSupport#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#1)]
 [!code-vb[DLinqDebuggingSupport#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="01875-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01875-109">See Also</span></span>  
 [<span data-ttu-id="01875-110">Prise en charge du débogage</span><span class="sxs-lookup"><span data-stu-id="01875-110">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
