---
title: Variables (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3eed222a-f8f6-46b6-9cd5-220cc0e4e5d8
ms.openlocfilehash: f271ffc31875e7d94a27f4752b71bfe508fcb620
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="variables-entity-sql"></a><span data-ttu-id="d4f8e-102">Variables (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="d4f8e-102">Variables (Entity SQL)</span></span>
## <a name="variable"></a><span data-ttu-id="d4f8e-103">Variable</span><span class="sxs-lookup"><span data-stu-id="d4f8e-103">Variable</span></span>  
 <span data-ttu-id="d4f8e-104">Une expression de variable est une référence à une expression nommée dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="d4f8e-104">A variable expression is a reference to a named expression defined in the current scope.</span></span> <span data-ttu-id="d4f8e-105">Une référence de variable doit être un [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identificateur, tel que défini dans [identificateurs](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="d4f8e-105">A variable reference must be a valid [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identifier, as defined in [Identifiers](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).</span></span>  
  
 <span data-ttu-id="d4f8e-106">L'exemple suivant montre l'utilisation d'une variable dans l'expression.</span><span class="sxs-lookup"><span data-stu-id="d4f8e-106">The following example shows the use of a variable in the expression.</span></span> <span data-ttu-id="d4f8e-107">Le `c` dans la clause FROM représente la définition de la variable.</span><span class="sxs-lookup"><span data-stu-id="d4f8e-107">The `c` in the FROM clause is the definition of the variable.</span></span> <span data-ttu-id="d4f8e-108">Le `c` dans la clause SELECT représente la référence à la variable.</span><span class="sxs-lookup"><span data-stu-id="d4f8e-108">The use of `c` in the SELECT clause represents the variable reference.</span></span>  
  
```  
select c   
from LOB.customers as c  
```  
  
## <a name="see-also"></a><span data-ttu-id="d4f8e-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4f8e-109">See Also</span></span>  
 [<span data-ttu-id="d4f8e-110">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="d4f8e-110">Identifiers</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md)  
 [<span data-ttu-id="d4f8e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4f8e-111">Parameters</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/parameters-entity-sql.md)  
 [<span data-ttu-id="d4f8e-112">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="d4f8e-112">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
