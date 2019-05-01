---
title: 'Procédure : Récupérer des informations sur les conflits entre membres'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
ms.openlocfilehash: fae1513e7a7ead98318d907b220b7510758c9ffe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037600"
---
# <a name="how-to-retrieve-member-conflict-information"></a>Procédure : Récupérer des informations sur les conflits entre membres
Vous pouvez utiliser la classe <xref:System.Data.Linq.MemberChangeConflict> pour récupérer des informations sur des membres individuels en conflit. Dans ce contexte, vous pouvez assurer la gestion personnalisée du conflit pour un membre quelconque. Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
## <a name="example"></a>Exemple  
 Le code suivant itère au sein des objets <xref:System.Data.Linq.ObjectChangeConflict>. Pour chacun de ces objets, il itère ensuite au sein des objets <xref:System.Data.Linq.MemberChangeConflict>.  
  
> [!NOTE]
>  Incluez <xref:System.Reflection> pour fournir des informations <xref:System.Data.Linq.MemberChangeConflict.Member%2A>.  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
