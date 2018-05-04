---
title: Expressions non prises en charge (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5e79da7e-e78a-413c-8fb0-f3f9cd84f579
dev_langs:
- sql
ms.openlocfilehash: 6d1746bb51af4795f09c47f808cf9a29d0370f18
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="unsupported-expressions"></a>Expressions non prises en charge

Cette rubrique décrit les expressions [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] qui ne sont pas prises en charge dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)]. Pour plus d’informations, consultez [Entity SQL différences entre Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md).

## <a name="quantified-predicates"></a>Prédicats quantifiés

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] autorise les constructions de la forme suivante :

```sql
sal > all (select salary from employees)
sal > any (select salary from employees)
```

Toutefois, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] ne prend pas en charge ces constructions. Des expressions équivalentes peuvent être écrites dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)], comme suit :

```sql
not exists(select 0 from employees as e where sal > e.salary)
exists(select 0 from employees as e where sal > e.salary)
```

## <a name="-operator"></a>* (opérateur)

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] prend en charge l'utilisation de l'opérateur * dans la clause SELECT pour indiquer que toutes les colonnes doivent être projetées. Cet opérateur n'est pas pris en charge dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)].

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
[Différences entre Entity SQL et Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md)  
