---
title: '&amp;&amp; (ET) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: e7d24213-471d-4807-b85e-570375df89b5
ms.openlocfilehash: eab05f7454f8ebc88ed29030503bfa96d0c70756
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59308430"
---
# <a name="ampamp-and-entity-sql"></a><span data-ttu-id="e7d5b-102">&amp;&amp; (ET) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="e7d5b-102">&amp;&amp; (AND) (Entity SQL)</span></span>
<span data-ttu-id="e7d5b-103">Retourne `true` si les deux expressions ont pour valeur `true`; sinon, `false` ou la valeur `NULL`.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-103">Returns `true` if both expressions are `true`; otherwise, `false` or `NULL`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7d5b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d5b-104">Syntax</span></span>  
  
```  
boolean_expression AND boolean_expression  
or  
boolean_expression && boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="e7d5b-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="e7d5b-105">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="e7d5b-106">Toute expression valide qui retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-106">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e7d5b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d5b-107">Remarks</span></span>  
 <span data-ttu-id="e7d5b-108">Les doubles « et » commerciaux (&&) ont la même fonctionnalité que l'opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-108">Double ampersands (&&) have the same functionality as the AND operator.</span></span>  
  
 <span data-ttu-id="e7d5b-109">Le tableau ci-dessous indique les valeurs d'entrée et les types de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-109">The following table shows possible input values and return types.</span></span>  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|<span data-ttu-id="e7d5b-110">TRUE</span><span class="sxs-lookup"><span data-stu-id="e7d5b-110">TRUE</span></span>|<span data-ttu-id="e7d5b-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="e7d5b-111">FALSE</span></span>|<span data-ttu-id="e7d5b-112">NULL</span><span class="sxs-lookup"><span data-stu-id="e7d5b-112">NULL</span></span>|  
|`FALSE`|<span data-ttu-id="e7d5b-113">FALSE</span><span class="sxs-lookup"><span data-stu-id="e7d5b-113">FALSE</span></span>|<span data-ttu-id="e7d5b-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="e7d5b-114">FALSE</span></span>|<span data-ttu-id="e7d5b-115">FALSE</span><span class="sxs-lookup"><span data-stu-id="e7d5b-115">FALSE</span></span>|  
|`NULL`|<span data-ttu-id="e7d5b-116">NULL</span><span class="sxs-lookup"><span data-stu-id="e7d5b-116">NULL</span></span>|<span data-ttu-id="e7d5b-117">false</span><span class="sxs-lookup"><span data-stu-id="e7d5b-117">FALSE</span></span>|<span data-ttu-id="e7d5b-118">NULL</span><span class="sxs-lookup"><span data-stu-id="e7d5b-118">NULL</span></span>|  
  
## <a name="example"></a><span data-ttu-id="e7d5b-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="e7d5b-119">Example</span></span>  
 <span data-ttu-id="e7d5b-120">La requête Entity SQL ci-dessous montre comment utiliser l'opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-120">The following Entity SQL query demonstrates how to use the AND operator.</span></span> <span data-ttu-id="e7d5b-121">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="e7d5b-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="e7d5b-122">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7d5b-122">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="e7d5b-123">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="e7d5b-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="e7d5b-124">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="e7d5b-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#AND](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#and)]  
  
## <a name="see-also"></a><span data-ttu-id="e7d5b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d5b-125">See also</span></span>

- [<span data-ttu-id="e7d5b-126">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="e7d5b-126">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
