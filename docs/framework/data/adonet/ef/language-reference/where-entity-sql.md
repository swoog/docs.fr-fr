---
title: WHERE (Entity SQL)
ms.date: 03/30/2017
ms.assetid: a8e1061e-0028-4a6f-8f19-b9f48e96c4b8
ms.openlocfilehash: 43c038e9ff0acfdeff88492aa2ca34fbf4ada94a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32764312"
---
# <a name="where-entity-sql"></a><span data-ttu-id="5aa86-102">WHERE (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="5aa86-102">WHERE (Entity SQL)</span></span>
<span data-ttu-id="5aa86-103">La clause WHERE est appliquée directement après le [FROM](../../../../../../docs/framework/data/adonet/ef/language-reference/from-entity-sql.md) clause.</span><span class="sxs-lookup"><span data-stu-id="5aa86-103">The WHERE clause is applied directly after the [FROM](../../../../../../docs/framework/data/adonet/ef/language-reference/from-entity-sql.md) clause.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5aa86-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aa86-104">Syntax</span></span>  
  
```  
[ WHERE expression ]  
```  
  
## <a name="arguments"></a><span data-ttu-id="5aa86-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="5aa86-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="5aa86-106">Type booléen.</span><span class="sxs-lookup"><span data-stu-id="5aa86-106">A Boolean type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5aa86-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5aa86-107">Remarks</span></span>  
 <span data-ttu-id="5aa86-108">La sémantique de la clause WHERE est identique à celle décrite pour [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5aa86-108">The WHERE clause has the same semantics as described for [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)].</span></span> <span data-ttu-id="5aa86-109">Elle restreint le nombre d'objets générés par l'expression de requête en limitant les éléments des collections sources à ceux qui répondent à la condition.</span><span class="sxs-lookup"><span data-stu-id="5aa86-109">It restricts the objects produced by the query expression by limiting the elements of the source collections to those that pass the condition.</span></span>  
  
```  
select c from cs as c where e  
```  
  
 <span data-ttu-id="5aa86-110">L'expression `e` doit être de type booléen.</span><span class="sxs-lookup"><span data-stu-id="5aa86-110">The expression `e` must have the type Boolean.</span></span>  
  
 <span data-ttu-id="5aa86-111">La clause WHERE est appliquée directement après la clause FROM et avant tout regroupement, classement ou projection éventuel.</span><span class="sxs-lookup"><span data-stu-id="5aa86-111">The WHERE clause is applied directly after the FROM clause and before any grouping, ordering, or projection takes place.</span></span> <span data-ttu-id="5aa86-112">Tous les noms d'éléments définis dans la clause FROM sont visibles pour l'expression de la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="5aa86-112">All element names defined in the FROM clause are visible to the expression of the WHERE clause.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5aa86-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aa86-113">See Also</span></span>  
 [<span data-ttu-id="5aa86-114">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="5aa86-114">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
 [<span data-ttu-id="5aa86-115">Expressions de requête</span><span class="sxs-lookup"><span data-stu-id="5aa86-115">Query Expressions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/query-expressions-entity-sql.md)
