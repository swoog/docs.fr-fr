---
title: Variables (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3eed222a-f8f6-46b6-9cd5-220cc0e4e5d8
ms.openlocfilehash: bf6fa95e38d1eb5817fd67165b6993cbb0755fd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879773"
---
# <a name="variables-entity-sql"></a><span data-ttu-id="f256b-102">Variables (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="f256b-102">Variables (Entity SQL)</span></span>
## <a name="variable"></a><span data-ttu-id="f256b-103">Variable</span><span class="sxs-lookup"><span data-stu-id="f256b-103">Variable</span></span>  
 <span data-ttu-id="f256b-104">Une expression de variable est une référence à une expression nommée dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="f256b-104">A variable expression is a reference to a named expression defined in the current scope.</span></span> <span data-ttu-id="f256b-105">Une référence de variable doit être un [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identificateur, tel que défini dans [identificateurs](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="f256b-105">A variable reference must be a valid [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identifier, as defined in [Identifiers](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).</span></span>  
  
 <span data-ttu-id="f256b-106">L'exemple suivant montre l'utilisation d'une variable dans l'expression.</span><span class="sxs-lookup"><span data-stu-id="f256b-106">The following example shows the use of a variable in the expression.</span></span> <span data-ttu-id="f256b-107">Le `c` dans la clause FROM représente la définition de la variable.</span><span class="sxs-lookup"><span data-stu-id="f256b-107">The `c` in the FROM clause is the definition of the variable.</span></span> <span data-ttu-id="f256b-108">Le `c` dans la clause SELECT représente la référence à la variable.</span><span class="sxs-lookup"><span data-stu-id="f256b-108">The use of `c` in the SELECT clause represents the variable reference.</span></span>  
  
```  
select c   
from LOB.customers as c  
```  
  
## <a name="see-also"></a><span data-ttu-id="f256b-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f256b-109">See also</span></span>

- [<span data-ttu-id="f256b-110">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="f256b-110">Identifiers</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md)
- [<span data-ttu-id="f256b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f256b-111">Parameters</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/parameters-entity-sql.md)
- [<span data-ttu-id="f256b-112">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="f256b-112">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
