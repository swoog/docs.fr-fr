---
title: 'Comment : récupérer des informations sur les conflits entre entités'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
ms.openlocfilehash: cabfae568396fa34e6090027032f310cdc05c507
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33353193"
---
# <a name="how-to-retrieve-entity-conflict-information"></a>Comment : récupérer des informations sur les conflits entre entités
Vous pouvez utiliser des objets de la classe <xref:System.Data.Linq.ObjectChangeConflict> pour fournir des informations sur des conflits révélés par des exceptions <xref:System.Data.Linq.ChangeConflictException>. Pour plus d’informations, consultez [d’accès concurrentiel optimiste : vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant itère au sein d'une liste de conflits cumulés.  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
