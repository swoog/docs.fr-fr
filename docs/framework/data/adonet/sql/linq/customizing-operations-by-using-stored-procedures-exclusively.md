---
title: Personnalisation d'opérations à l'aide de procédures stockées uniquement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 441e8ef3-998c-4d12-8825-ce66a178f90f
ms.openlocfilehash: 61230ffc5cd055ee64de9d519cdfb4d76c856ca3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59128646"
---
# <a name="customizing-operations-by-using-stored-procedures-exclusively"></a>Personnalisation d'opérations à l'aide de procédures stockées uniquement
L'accès aux données se fait couramment à l'aide de procédures stockées uniquement.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 Vous pouvez modifier l’exemple fourni dans [personnalisation des opérations par à l’aide de procédures stockées](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-by-using-stored-procedures.md) en remplaçant la première requête (ce qui provoque l’exécution de SQL dynamique) par un appel de méthode qui encapsule une procédure stockée.  
  
 Supposons que `CustomersByCity` est la méthode, comme illustré dans l'exemple suivant.  
  
### <a name="code"></a>Code  
 [!code-csharp[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/northwind.cs#4)]
 [!code-vb[DLinqOverrideDefaultSproc#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/northwind.vb#4)]  
  
 Le code suivant s'exécute sans SQL dynamique.  
  
 [!code-csharp[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqOverrideDefaultSproc/cs/Program.cs#5)]
 [!code-vb[DLinqOverrideDefaultSproc#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqOverrideDefaultSproc/vb/Module1.vb#5)]  
  
## <a name="see-also"></a>Voir aussi

- [Responsabilités du développeur en matière de substitution du comportement par défaut](../../../../../../docs/framework/data/adonet/sql/linq/responsibilities-of-the-developer-in-overriding-default-behavior.md)
