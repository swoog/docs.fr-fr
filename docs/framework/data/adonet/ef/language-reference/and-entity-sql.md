---
title: '&amp;&amp; (ET) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: e7d24213-471d-4807-b85e-570375df89b5
ms.openlocfilehash: 649b805c1d728c45120adf85f02533d36f7bcdff
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32763785"
---
# <a name="ampamp-and-entity-sql"></a><span data-ttu-id="3f1c5-102">&amp;&amp; (ET) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="3f1c5-102">&amp;&amp; (AND) (Entity SQL)</span></span>
<span data-ttu-id="3f1c5-103">Retourne `true` si les deux expressions ont pour valeur `true`; sinon, `false` ou la valeur `NULL`.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-103">Returns `true` if both expressions are `true`; otherwise, `false` or `NULL`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f1c5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f1c5-104">Syntax</span></span>  
  
```  
boolean_expression AND boolean_expression  
or  
boolean_expression && boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="3f1c5-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="3f1c5-105">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="3f1c5-106">Toute expression valide qui retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-106">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f1c5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3f1c5-107">Remarks</span></span>  
 <span data-ttu-id="3f1c5-108">Les doubles « et » commerciaux (&&) ont la même fonctionnalité que l'opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-108">Double ampersands (&&) have the same functionality as the AND operator.</span></span>  
  
 <span data-ttu-id="3f1c5-109">Le tableau ci-dessous indique les valeurs d'entrée et les types de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-109">The following table shows possible input values and return types.</span></span>  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|<span data-ttu-id="3f1c5-110">TRUE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-110">TRUE</span></span>|<span data-ttu-id="3f1c5-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-111">FALSE</span></span>|<span data-ttu-id="3f1c5-112">NULL</span><span class="sxs-lookup"><span data-stu-id="3f1c5-112">NULL</span></span>|  
|`FALSE`|<span data-ttu-id="3f1c5-113">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-113">FALSE</span></span>|<span data-ttu-id="3f1c5-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-114">FALSE</span></span>|<span data-ttu-id="3f1c5-115">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f1c5-115">FALSE</span></span>|  
|`NULL`|<span data-ttu-id="3f1c5-116">NULL</span><span class="sxs-lookup"><span data-stu-id="3f1c5-116">NULL</span></span>|<span data-ttu-id="3f1c5-117">false</span><span class="sxs-lookup"><span data-stu-id="3f1c5-117">FALSE</span></span>|<span data-ttu-id="3f1c5-118">NULL</span><span class="sxs-lookup"><span data-stu-id="3f1c5-118">NULL</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3f1c5-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f1c5-119">Example</span></span>  
 <span data-ttu-id="3f1c5-120">La requête Entity SQL ci-dessous montre comment utiliser l'opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-120">The following Entity SQL query demonstrates how to use the AND operator.</span></span> <span data-ttu-id="3f1c5-121">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="3f1c5-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3f1c5-122">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3f1c5-122">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="3f1c5-123">Suivez la procédure de [Comment : exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="3f1c5-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="3f1c5-124">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="3f1c5-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#AND](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#and)]  
  
## <a name="see-also"></a><span data-ttu-id="3f1c5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f1c5-125">See Also</span></span>  
 [<span data-ttu-id="3f1c5-126">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="3f1c5-126">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
