---
title: "Exemples de syntaxe d'expression de requête : opérateurs d'élément"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 32268fe2-de18-4065-8060-f250def83837
ms.openlocfilehash: 36823b02d581b47493950b6393bda323b2e8f9b7
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43749182"
---
# <a name="query-expression-syntax-examples-element-operators"></a>Exemples de syntaxe d'expression de requête : opérateurs d'élément
Les exemples de cette rubrique montrent comment utiliser le <xref:System.Linq.Enumerable.First%2A> méthode pour interroger le [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) à l’aide de la syntaxe d’expression de requête. Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.  
  
 Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="first"></a>First  
  
### <a name="example"></a>Exemple  
 L'exemple ci-dessous utilise la méthode <xref:System.Linq.Enumerable.First%2A> pour retourner le premier contact dont le prénom est « Brooke ».  
  
 [!code-csharp[DP L2E Examples#FirstSimple](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#firstsimple)]
 [!code-vb[DP L2E Examples#FirstSimple](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#firstsimple)]  
  
## <a name="see-also"></a>Voir aussi  
 [Requêtes dans LINQ to Entities](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
