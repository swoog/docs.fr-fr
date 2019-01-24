---
title: 'Procédure : Récupérer des informations sur les conflits de membre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
ms.openlocfilehash: 478781e6c8ee31ebf6f5edd0e243a81d9e0524f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669560"
---
# <a name="how-to-retrieve-member-conflict-information"></a>Procédure : Récupérer des informations sur les conflits de membre
Vous pouvez utiliser la classe <xref:System.Data.Linq.MemberChangeConflict> pour récupérer des informations sur des membres individuels en conflit. Dans ce contexte, vous pouvez assurer la gestion personnalisée du conflit pour un membre quelconque. Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
## <a name="example"></a>Exemple  
 Le code suivant itère au sein des objets <xref:System.Data.Linq.ObjectChangeConflict>. Pour chacun de ces objets, il itère ensuite au sein des objets <xref:System.Data.Linq.MemberChangeConflict>.  
  
> [!NOTE]
>  Incluez <xref:System.Reflection> pour fournir des informations <xref:System.Data.Linq.MemberChangeConflict.Member%2A>.  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
