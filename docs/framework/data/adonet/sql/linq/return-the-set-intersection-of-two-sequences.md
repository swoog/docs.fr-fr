---
title: Retourner l'intersection définie de deux séquences
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d09c344e-3548-4944-a3ed-051880e3f5b8
ms.openlocfilehash: bb1785b12df2e8a835ba49ae59d0448fbebf794c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506821"
---
# <a name="return-the-set-intersection-of-two-sequences"></a>Retourner l'intersection définie de deux séquences
Utilisez l'opérateur <xref:System.Linq.Queryable.Intersect%2A> pour retourner l'intersection définie de deux séquences.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise <xref:System.Linq.Queryable.Intersect%2A> pour retourner une séquence de tous les pays dans lesquels les `Customers` et les `Employees` habitent.  
  
 [!code-csharp[DLinqQueryExamples#42](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#42)]
 [!code-vb[DLinqQueryExamples#42](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#42)]  
  
 Dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], l'opération <xref:System.Linq.Queryable.Intersect%2A> est correctement définie sur les jeux uniquement. La sémantique pour les multijeux n'est pas définie.  
  
## <a name="see-also"></a>Voir aussi
- [Exemples de requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
- [Traduction des opérateurs de requête standard](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)
