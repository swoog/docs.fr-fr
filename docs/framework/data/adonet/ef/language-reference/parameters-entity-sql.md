---
title: Paramètres (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 8d618edd-0988-4ff2-8263-ce59448af7a5
ms.openlocfilehash: 47a1514933904daa623adc151d50525f011e07a7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760247"
---
# <a name="parameters-entity-sql"></a>Paramètres (Entity SQL)
Les paramètres sont des variables qui sont définies en dehors d'[!INCLUDE[esql](../../../../../../includes/esql-md.md)], généralement par le biais d'une API de liaison qui est utilisée par un langage hôte. Chaque paramètre a un nom et un type. Les noms de paramètres sont définis dans des expressions de requête avec le symbole at (@) comme préfixe. Cela lève l'ambiguïté entre ces noms et les noms de propriétés ou autres noms qui sont définis dans la requête.  
  
 L’API de liaison du langage hôte fournit des API pour les paramètres de liaison.  
  
## <a name="example"></a>Exemple  
  
```  
select c   
      from LOB.Customers as c   
      where c.Name = @name  
```  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
