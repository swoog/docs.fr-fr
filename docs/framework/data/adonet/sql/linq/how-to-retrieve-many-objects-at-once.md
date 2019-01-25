---
title: 'Procédure : Récupérer plusieurs objets à la fois'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 18aff4d8-bde8-461b-9960-ccabb24e9d22
ms.openlocfilehash: 31091b6634c9d95c008929680620fb66d95d473c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653786"
---
# <a name="how-to-retrieve-many-objects-at-once"></a>Procédure : Récupérer plusieurs objets à la fois
Vous pouvez récupérer plusieurs objets dans une requête en utilisant <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.  
  
## <a name="example"></a>Exemple  
 Le code suivant utilise la méthode <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> pour récupérer des objets `Customer` et `Order`.  
  
 [!code-csharp[DLinqQueryConcepts#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#9)]
 [!code-vb[DLinqQueryConcepts#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#9)]  
  
## <a name="see-also"></a>Voir aussi
- [Concepts relatifs aux requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
