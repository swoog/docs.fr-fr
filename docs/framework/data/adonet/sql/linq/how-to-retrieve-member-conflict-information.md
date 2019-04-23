---
title: 'Procédure : Récupérer des informations sur les conflits entre membres'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
ms.openlocfilehash: fae1513e7a7ead98318d907b220b7510758c9ffe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115087"
---
# <a name="how-to-retrieve-member-conflict-information"></a><span data-ttu-id="966b6-102">Procédure : Récupérer des informations sur les conflits entre membres</span><span class="sxs-lookup"><span data-stu-id="966b6-102">How to: Retrieve Member Conflict Information</span></span>
<span data-ttu-id="966b6-103">Vous pouvez utiliser la classe <xref:System.Data.Linq.MemberChangeConflict> pour récupérer des informations sur des membres individuels en conflit.</span><span class="sxs-lookup"><span data-stu-id="966b6-103">You can use the <xref:System.Data.Linq.MemberChangeConflict> class to retrieve information about individual members in conflict.</span></span> <span data-ttu-id="966b6-104">Dans ce contexte, vous pouvez assurer la gestion personnalisée du conflit pour un membre quelconque.</span><span class="sxs-lookup"><span data-stu-id="966b6-104">In this same context you can provide for custom handling of the conflict for any member.</span></span> <span data-ttu-id="966b6-105">Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span><span class="sxs-lookup"><span data-stu-id="966b6-105">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="966b6-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="966b6-106">Example</span></span>  
 <span data-ttu-id="966b6-107">Le code suivant itère au sein des objets <xref:System.Data.Linq.ObjectChangeConflict>.</span><span class="sxs-lookup"><span data-stu-id="966b6-107">The following code iterates through the <xref:System.Data.Linq.ObjectChangeConflict> objects.</span></span> <span data-ttu-id="966b6-108">Pour chacun de ces objets, il itère ensuite au sein des objets <xref:System.Data.Linq.MemberChangeConflict>.</span><span class="sxs-lookup"><span data-stu-id="966b6-108">For each object, it then iterates through the <xref:System.Data.Linq.MemberChangeConflict> objects.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="966b6-109">Incluez <xref:System.Reflection> pour fournir des informations <xref:System.Data.Linq.MemberChangeConflict.Member%2A>.</span><span class="sxs-lookup"><span data-stu-id="966b6-109">Include <xref:System.Reflection> in order to provide <xref:System.Data.Linq.MemberChangeConflict.Member%2A> information.</span></span>  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="966b6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="966b6-110">See also</span></span>

- [<span data-ttu-id="966b6-111">Guide pratique pour Gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="966b6-111">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
