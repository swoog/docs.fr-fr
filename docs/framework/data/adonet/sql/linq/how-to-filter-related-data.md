---
title: 'Procédure : Filtrer des données connexes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ec8b8f97-5d01-4f31-9b97-d1556df6a4bc
ms.openlocfilehash: 9a046c94363a1a161e19dcb68e015f8c6791e511
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703469"
---
# <a name="how-to-filter-related-data"></a><span data-ttu-id="46d21-102">Procédure : Filtrer des données connexes</span><span class="sxs-lookup"><span data-stu-id="46d21-102">How to: Filter Related Data</span></span>
<span data-ttu-id="46d21-103">Utilisez la méthode <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> pour spécifier des sous-requêtes afin de limiter la quantité de données récupérées.</span><span class="sxs-lookup"><span data-stu-id="46d21-103">Use the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method to specify sub-queries to limit the amount of retrieved data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46d21-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="46d21-104">Example</span></span>  
 <span data-ttu-id="46d21-105">Dans l'exemple suivant, la méthode <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> limite les `Orders` récupérées à celles qui n'ont pas encore été expédiées aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="46d21-105">In the following example, the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method limits the `Orders` retrieved to those that have not been shipped today.</span></span> <span data-ttu-id="46d21-106">Sans cette approche, toutes les `Orders` auraient été récupérées bien que seul un sous-ensemble soit désiré.</span><span class="sxs-lookup"><span data-stu-id="46d21-106">Without this approach, all `Orders` would have been retrieved even though only a subset is desired.</span></span>  
  
 [!code-csharp[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.dataloadoptions/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.dataloadoptions/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="46d21-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46d21-107">See also</span></span>
- [<span data-ttu-id="46d21-108">Interrogation de la base de données</span><span class="sxs-lookup"><span data-stu-id="46d21-108">Querying the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
