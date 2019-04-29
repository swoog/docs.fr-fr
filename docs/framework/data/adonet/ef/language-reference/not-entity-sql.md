---
title: '! (NOT) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: a1447a34-df06-4393-93c3-0612ebd41abc
ms.openlocfilehash: 51d3bdbc4adb0b5fd6275629219698dd9b42fa86
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760374"
---
# <a name="-not-entity-sql"></a><span data-ttu-id="52c1d-103">!</span><span class="sxs-lookup"><span data-stu-id="52c1d-103">!</span></span> <span data-ttu-id="52c1d-104">(NOT) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="52c1d-104">(NOT) (Entity SQL)</span></span>
<span data-ttu-id="52c1d-105">Inverse une expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="52c1d-105">Negates a `Boolean` expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52c1d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52c1d-106">Syntax</span></span>  
  
```  
NOT boolean_expression  
or  
! boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="52c1d-107">Arguments</span><span class="sxs-lookup"><span data-stu-id="52c1d-107">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="52c1d-108">Toute expression valide qui retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="52c1d-108">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="52c1d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="52c1d-109">Remarks</span></span>  
 <span data-ttu-id="52c1d-110">Le point d'exclamation (!) a la même fonctionnalité que l'opérateur NOT.</span><span class="sxs-lookup"><span data-stu-id="52c1d-110">The exclamation point (!) has the same functionality as the NOT operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="52c1d-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="52c1d-111">Example</span></span>  
 <span data-ttu-id="52c1d-112">La requête Entity SQL ci-dessous utilise l'opérateur NOT pour inverser une expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="52c1d-112">The following Entity SQL query uses the NOT operator to negates a `Boolean` expression.</span></span> <span data-ttu-id="52c1d-113">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="52c1d-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="52c1d-114">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="52c1d-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="52c1d-115">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="52c1d-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="52c1d-116">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="52c1d-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#NOT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#not)]  
  
## <a name="see-also"></a><span data-ttu-id="52c1d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52c1d-117">See also</span></span>

- [<span data-ttu-id="52c1d-118">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="52c1d-118">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
