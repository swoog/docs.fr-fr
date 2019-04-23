---
title: 'Procédure : Récupérer des informations sur les conflits entre entités'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
ms.openlocfilehash: 825ba2a32e7c75e922ca08386b9f6efede7b2693
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59154750"
---
# <a name="how-to-retrieve-entity-conflict-information"></a>Procédure : Récupérer des informations sur les conflits entre entités
Vous pouvez utiliser des objets de la classe <xref:System.Data.Linq.ObjectChangeConflict> pour fournir des informations sur des conflits révélés par des exceptions <xref:System.Data.Linq.ChangeConflictException>. Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant itère au sein d'une liste de conflits cumulés.  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
