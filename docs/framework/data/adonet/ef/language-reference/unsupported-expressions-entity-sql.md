---
title: Expressions non prises en charge (Entity SQL)
ms.date: 03/30/2017
ms.prod: .net-framework
ms.technology:
- dotnet-ado
ms.topic: article
ms.assetid: 5e79da7e-e78a-413c-8fb0-f3f9cd84f579
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
dev_langs:
- sql
ms.openlocfilehash: 075daf0e4f0477dda50231760fbb3d990a9f8468
ms.sourcegitcommit: c3957fdb990060559d73cca44ab3e2c7b4d049c0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2018
---
# <a name="unsupported-expressions"></a>Expressions non prises en charge

Cette rubrique décrit les expressions [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] qui ne sont pas prises en charge dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)]. Pour plus d’informations, consultez [Entity SQL différences entre Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md).

## <a name="quantified-predicates"></a>Prédicats quantifiés

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] autorise les constructions de la forme suivante :

```sql
sal > all (select salary from employees)
sal > any (select salary from employees)
```

[!INCLUDE[esql](../../../../../../includes/esql-md.md)], toutefois, ne prend pas en charge ces constructions. Des expressions équivalentes peuvent être écrites dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)], comme suit :

```sql
not exists(select 0 from employees as e where sal > e.salary)
exists(select 0 from employees as e where sal > e.salary)
```

## <a name="-operator"></a>* (opérateur)

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] prend en charge l’utilisation de la * (opérateur) dans la clause SELECT pour indiquer que toutes les colonnes doivent être projetées. Cet opérateur n'est pas pris en charge dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)].

## <a name="see-also"></a>Voir aussi

[Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
[Différences entre Entity SQL et Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md)  
