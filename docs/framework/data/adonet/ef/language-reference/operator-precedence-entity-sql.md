---
title: Priorité des opérateurs (Entity SQL)
ms.date: 03/30/2017
ms.assetid: e92e4ca5-2889-4266-9625-47f0eb01a948
ms.openlocfilehash: 722ebe5f0ec530f8c7f86e9f9901451b060903f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59159131"
---
# <a name="operator-precedence-entity-sql"></a>Priorité des opérateurs (Entity SQL)
Quand un [!INCLUDE[esql](../../../../../../includes/esql-md.md)] requête comporte plusieurs opérateurs, priorité des opérateurs détermine l’ordre dans lequel les opérations sont effectuées. Cet ordre peut affecter considérablement le résultat de la requête.  
  
 L'ordre de priorité des opérateurs est indiqué dans le tableau suivant. Un opérateur avec un haut niveau de priorité est évalué avant un opérateur avec un faible niveau de priorité.  
  
|Niveau|Type d'opération|Opérateur|  
|-----------|--------------------|--------------|  
|1|Principale|`. , [] ()`|  
|2|Unaire|`! not`|  
|3|Multiplication|`* / %`|  
|4|Addition|`+ -`|  
|5|Classement|`< > <= >=`|  
|6|Égalité|`= != <>`|  
|7|AND conditionnel|`and &&`|  
|8|OR conditionnel|`or &#124;&#124;`|  
  
 Lorsque deux opérateurs dans une expression ont le même niveau de priorité, ils sont évalués de gauche à droite, en fonction de leur position dans la requête. Par exemple, `x+y-z` est évalué comme étant `(x+y)-z`.  
  
 Vous pouvez utiliser des parenthèses pour modifier la priorité habituelle des opérateurs dans une requête. Tout ce qui se trouve entre parenthèses est évalué en premier pour produire un seul résultat, qui est ensuite utilisé par un opérateur en dehors des parenthèses. Par exemple, `x+y*z` multiplie `y` par `z` , puis ajoute `x`, mais `(x+y)*z` ajoute `x` à `y` , puis multiplie le résultat par `z`.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
