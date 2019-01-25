---
title: 'Procédure : Désactiver le chargement différé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1b84b852-3cad-41a7-8077-149a70d50c8b
ms.openlocfilehash: 9878ec468333ba79d0171d0bf96235d48273e03e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669534"
---
# <a name="how-to-turn-off-deferred-loading"></a>Procédure : Désactiver le chargement différé
Vous pouvez désactiver le chargement différé en affectant la valeur <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> à `false`. Pour plus d’informations, consultez [différée / le chargement immédiat](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md).  
  
> [!NOTE]
>  Le chargement différé est désactivé lorsque le suivi d'objet est désactivé. Pour plus d'informations, voir [Procédure : Récupérer des informations en lecture seule](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-information-as-read-only.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment désactiver le chargement différé en affectant la valeur <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> à `false`.  
  
 [!code-csharp[DLinqQuerying#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#3)]
 [!code-vb[DLinqQuerying#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi
- [Concepts relatifs aux requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
- [Interrogation de la base de données](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
