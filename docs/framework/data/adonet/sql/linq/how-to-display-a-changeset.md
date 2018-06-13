---
title: 'Comment : afficher un ensemble de modifications ou ChangeSet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 126e7245-c5a0-4ebf-800d-cc1fcf9cd0ab
ms.openlocfilehash: c9664c6d32f78f455aa29311f111acaecb5c7905
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33359983"
---
# <a name="how-to-display-a-changeset"></a><span data-ttu-id="e4262-102">Comment : afficher un ensemble de modifications ou ChangeSet</span><span class="sxs-lookup"><span data-stu-id="e4262-102">How to: Display a ChangeSet</span></span>
<span data-ttu-id="e4262-103">Vous pouvez consulter des modifications suivies par un <xref:System.Data.Linq.DataContext> à l'aide de <xref:System.Data.Linq.DataContext.GetChangeSet%2A>.</span><span class="sxs-lookup"><span data-stu-id="e4262-103">You can view changes tracked by a <xref:System.Data.Linq.DataContext> by using <xref:System.Data.Linq.DataContext.GetChangeSet%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e4262-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4262-104">Example</span></span>  
 <span data-ttu-id="e4262-105">L'exemple suivant récupère des clients dont la ville est Londres, remplace la ville par Paris et soumet les modifications à la base de données.</span><span class="sxs-lookup"><span data-stu-id="e4262-105">The following example retrieves customers whose city is London, changes the city to Paris, and submits the changes back to the database.</span></span>  
  
 [!code-csharp[DLinqDebuggingSupport#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#2)]
 [!code-vb[DLinqDebuggingSupport#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#2)]  
  
 <span data-ttu-id="e4262-106">La sortie de ce code semble similaire aux éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="e4262-106">Output from this code appears similar to the following.</span></span> <span data-ttu-id="e4262-107">Notez que le résumé de fin indique que huit modifications ont été apportées.</span><span class="sxs-lookup"><span data-stu-id="e4262-107">Note that the summary at the end shows that eight changes were made.</span></span>  
  
 `CustomerID: AROUT`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: BSBEV`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: CONSH`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: EASTC`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: NORTS`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: PARIS`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: SEVES`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 `CustomerID: SPECD`  
  
 `Original value: London`  
  
 `Updated value: Paris`  
  
 ``  
  
 `Total changes: {Added: 0, Removed: 0, Modified: 8}`  
  
## <a name="see-also"></a><span data-ttu-id="e4262-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4262-108">See Also</span></span>  
 [<span data-ttu-id="e4262-109">Prise en charge du débogage</span><span class="sxs-lookup"><span data-stu-id="e4262-109">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
