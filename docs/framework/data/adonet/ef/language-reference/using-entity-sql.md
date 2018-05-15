---
title: USING (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 20f58b8f-6070-4456-b7e8-5ff3d6269273
ms.openlocfilehash: 89306c8b4c317ebaba0d964869c4fe9e1028631a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="using-entity-sql"></a><span data-ttu-id="69a3d-102">USING (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="69a3d-102">USING (Entity SQL)</span></span>
<span data-ttu-id="69a3d-103">Spécifie les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="69a3d-103">Specifies namespaces used in a query expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69a3d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69a3d-104">Syntax</span></span>  
  
```  
USING [ alias = ] namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="69a3d-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="69a3d-105">Arguments</span></span>  
 `alias`  
 <span data-ttu-id="69a3d-106">Spécifie un alias plus court avec lequel qualifier un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="69a3d-106">Specifies a shorter alias to qualify a namespace with.</span></span>  
  
 `namespace`  
 <span data-ttu-id="69a3d-107">Tout espace de noms valide.</span><span class="sxs-lookup"><span data-stu-id="69a3d-107">Any valid namespace.</span></span>  
  
## <a name="example"></a><span data-ttu-id="69a3d-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="69a3d-108">Example</span></span>  
 <span data-ttu-id="69a3d-109">La requête Entity SQL ci-dessous utilise l'opérateur USING pour spécifier les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="69a3d-109">The following Entity SQL query uses the USING operator to specify namespaces used in a query expression.</span></span> <span data-ttu-id="69a3d-110">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="69a3d-110">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="69a3d-111">Suivez la procédure de [Comment : exécuter une requête qui retourne des résultats PrimitiveType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span><span class="sxs-lookup"><span data-stu-id="69a3d-111">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2.  <span data-ttu-id="69a3d-112">Transmettez à la méthode `ExecutePrimitiveTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="69a3d-112">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
```  
using SqlServer; RAND()  
```  
  
## <a name="see-also"></a><span data-ttu-id="69a3d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a3d-113">See Also</span></span>  
 [<span data-ttu-id="69a3d-114">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="69a3d-114">Namespaces</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/namespaces-entity-sql.md)  
 [<span data-ttu-id="69a3d-115">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="69a3d-115">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
