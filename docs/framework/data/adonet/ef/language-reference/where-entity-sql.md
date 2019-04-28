---
title: WHERE (Entity SQL)
ms.date: 03/30/2017
ms.assetid: a8e1061e-0028-4a6f-8f19-b9f48e96c4b8
ms.openlocfilehash: 02eeaeb8cfa335e5545b26d3d52b91c4e1614629
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879435"
---
# <a name="where-entity-sql"></a>WHERE (Entity SQL)
La clause WHERE est appliquée directement après le [FROM](../../../../../../docs/framework/data/adonet/ef/language-reference/from-entity-sql.md) clause.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ WHERE expression ]  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Type booléen.  
  
## <a name="remarks"></a>Notes  
 La sémantique de la clause WHERE est identique à celle décrite pour [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)]. Elle restreint le nombre d’objets générés par l’expression de requête en limitant les éléments des collections sources à ceux qui répondent à la condition.  
  
```  
select c from cs as c where e  
```  
  
 L'expression `e` doit être de type booléen.  
  
 La clause WHERE est appliquée directement après la clause FROM et avant tout regroupement, classement ou projection éventuel. Tous les noms d'éléments définis dans la clause FROM sont visibles pour l'expression de la clause WHERE.  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Expressions de requête](../../../../../../docs/framework/data/adonet/ef/language-reference/query-expressions-entity-sql.md)
