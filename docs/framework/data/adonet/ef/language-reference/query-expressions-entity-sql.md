---
title: Expressions de requête (Entity SQL)
ms.date: 03/30/2017
ms.assetid: c36f327b-e230-48d4-bbd5-78dc6478c447
ms.openlocfilehash: 5a200c8fc5adcb6334d0a0ddf290d275de4eb768
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54696878"
---
# <a name="query-expressions-entity-sql"></a>Expressions de requête (Entity SQL)
Une expression de requête combine un grand nombre d'opérateurs de requête différents dans une syntaxe unique. [!INCLUDE[esql](../../../../../../includes/esql-md.md)] fournit différentes sortes d’expressions, y compris les éléments suivants : [littéraux](../../../../../../docs/framework/data/adonet/ef/language-reference/literals-entity-sql.md), [paramètres](../../../../../../docs/framework/data/adonet/ef/language-reference/parameters-entity-sql.md), [variables](../../../../../../docs/framework/data/adonet/ef/language-reference/variables-entity-sql.md), opérateurs, [fonctions](../../../../../../docs/framework/data/adonet/ef/language-reference/functions-entity-sql.md), les opérateurs de jeu et ainsi de suite. Pour plus d’informations, consultez [référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md).  
  
## <a name="clauses"></a>Clauses  
 Une expression de requête est constituée d’une série de clauses qui appliquent des opérations successives à une collection d’objets. Elles sont basées sur les mêmes clauses contenues dans une instruction SQL select standard : [Sélectionnez](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md), [FROM](../../../../../../docs/framework/data/adonet/ef/language-reference/from-entity-sql.md), [où](../../../../../../docs/framework/data/adonet/ef/language-reference/where-entity-sql.md), [GROUP BY](../../../../../../docs/framework/data/adonet/ef/language-reference/group-by-entity-sql.md), [HAVING](../../../../../../docs/framework/data/adonet/ef/language-reference/having-entity-sql.md), et [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md).  
  
## <a name="scope"></a>Portée  
 Les noms définis dans la clause FROM sont introduits dans l'étendue FROM dans l'ordre de leur apparition, de gauche à droite. Dans la liste JOIN, les expressions peuvent faire référence aux noms définis précédemment dans la liste. Les propriétés publiques des éléments identifiés dans la clause FROM ne sont pas ajoutées à l'étendue FROM. Elles doivent toujours être référencées par le bias du nom qualifié par un alias. Normalement, toutes les parties de l'expression select sont considérées comme faisant partie de l'étendue FROM.  
  
## <a name="see-also"></a>Voir aussi
- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
