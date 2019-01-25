---
title: USING (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 20f58b8f-6070-4456-b7e8-5ff3d6269273
ms.openlocfilehash: a07ee1c32a93ee22b7418784fbd893e7699c553e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744295"
---
# <a name="using-entity-sql"></a><span data-ttu-id="8d5b5-102">USING (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="8d5b5-102">USING (Entity SQL)</span></span>
<span data-ttu-id="8d5b5-103">Spécifie les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="8d5b5-103">Specifies namespaces used in a query expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d5b5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d5b5-104">Syntax</span></span>  
  
```  
USING [ alias = ] namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="8d5b5-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="8d5b5-105">Arguments</span></span>  
 `alias`  
 <span data-ttu-id="8d5b5-106">Spécifie un alias plus court avec lequel qualifier un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="8d5b5-106">Specifies a shorter alias to qualify a namespace with.</span></span>  
  
 `namespace`  
 <span data-ttu-id="8d5b5-107">Tout espace de noms valide.</span><span class="sxs-lookup"><span data-stu-id="8d5b5-107">Any valid namespace.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8d5b5-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d5b5-108">Example</span></span>  
 <span data-ttu-id="8d5b5-109">La requête Entity SQL ci-dessous utilise l'opérateur USING pour spécifier les espaces de noms utilisés dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="8d5b5-109">The following Entity SQL query uses the USING operator to specify namespaces used in a query expression.</span></span> <span data-ttu-id="8d5b5-110">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d5b5-110">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="8d5b5-111">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne les résultats PrimitiveType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span><span class="sxs-lookup"><span data-stu-id="8d5b5-111">Follow the procedure in [How to: Execute a Query that Returns PrimitiveType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).</span></span>  
  
2.  <span data-ttu-id="8d5b5-112">Transmettez à la méthode `ExecutePrimitiveTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="8d5b5-112">Pass the following query as an argument to the `ExecutePrimitiveTypeQuery` method:</span></span>  
  
```  
using SqlServer; RAND()  
```  
  
## <a name="see-also"></a><span data-ttu-id="8d5b5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d5b5-113">See also</span></span>
- [<span data-ttu-id="8d5b5-114">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="8d5b5-114">Namespaces</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/namespaces-entity-sql.md)
- [<span data-ttu-id="8d5b5-115">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="8d5b5-115">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
