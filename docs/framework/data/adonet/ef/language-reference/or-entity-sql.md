---
title: '|| (OR) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 8e649648-eb9a-4380-9d74-36e62260628c
ms.openlocfilehash: d089bcec56ff13ddcd5250a63aee6a00d0c3ef11
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760309"
---
# <a name="-or-entity-sql"></a><span data-ttu-id="3a90e-102">|| (OR) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="3a90e-102">|| (OR) (Entity SQL)</span></span>
<span data-ttu-id="3a90e-103">Combine deux expressions `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="3a90e-103">Combines two `Boolean` expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a90e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a90e-104">Syntax</span></span>  
  
```  
boolean_expression OR boolean_expression  
or   
boolean_expression || boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="3a90e-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="3a90e-105">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="3a90e-106">Toute expression valide qui retourne une valeur `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="3a90e-106">Any valid expression that returns a `Boolean`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3a90e-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3a90e-107">Return Value</span></span>  
 <span data-ttu-id="3a90e-108">`true` si l'une des conditions a la valeur `true`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="3a90e-108">`true` when either of the conditions is `true`; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3a90e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3a90e-109">Remarks</span></span>  
 <span data-ttu-id="3a90e-110">OR est un opérateur logique [!INCLUDE[esql](../../../../../../includes/esql-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="3a90e-110">OR is an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] logical operator.</span></span> <span data-ttu-id="3a90e-111">Il est utilisé pour combiner deux conditions.</span><span class="sxs-lookup"><span data-stu-id="3a90e-111">It is used to combine two conditions.</span></span> <span data-ttu-id="3a90e-112">Lorsque vous utilisez plusieurs opérateurs logiques dans une instruction, les opérateurs OR sont évalués après les opérateurs AND.</span><span class="sxs-lookup"><span data-stu-id="3a90e-112">When more than one logical operator is used in a statement, OR operators are evaluated after AND operators.</span></span> <span data-ttu-id="3a90e-113">L'utilisation de parenthèses permet toutefois de modifier l'ordre de traitement.</span><span class="sxs-lookup"><span data-stu-id="3a90e-113">However, you can change the order of evaluation by using parentheses.</span></span>  
  
 <span data-ttu-id="3a90e-114">Les doubles barres verticales (&#124;&#124;) ont les mêmes fonctionnalités que l’opérateur OR.</span><span class="sxs-lookup"><span data-stu-id="3a90e-114">Double vertical bars (&#124;&#124;) have the same functionality as the OR operator.</span></span>  
  
 <span data-ttu-id="3a90e-115">Le tableau ci-dessous indique les valeurs d'entrée et les types de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="3a90e-115">The following table shows possible input values and return types.</span></span>  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|<span data-ttu-id="3a90e-116">true</span><span class="sxs-lookup"><span data-stu-id="3a90e-116">TRUE</span></span>|<span data-ttu-id="3a90e-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a90e-117">TRUE</span></span>|<span data-ttu-id="3a90e-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a90e-118">TRUE</span></span>|  
|`FALSE`|<span data-ttu-id="3a90e-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a90e-119">TRUE</span></span>|<span data-ttu-id="3a90e-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a90e-120">FALSE</span></span>|<span data-ttu-id="3a90e-121">NULL</span><span class="sxs-lookup"><span data-stu-id="3a90e-121">NULL</span></span>|  
|`NULL`|<span data-ttu-id="3a90e-122">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a90e-122">TRUE</span></span>|<span data-ttu-id="3a90e-123">NULL</span><span class="sxs-lookup"><span data-stu-id="3a90e-123">NULL</span></span>|<span data-ttu-id="3a90e-124">NULL</span><span class="sxs-lookup"><span data-stu-id="3a90e-124">NULL</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3a90e-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a90e-125">Example</span></span>  
 <span data-ttu-id="3a90e-126">La requête Entity SQL ci-dessous utilise l'opérateur OR pour combiner deux expressions `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="3a90e-126">The following Entity SQL query uses the OR operator to combine two `Boolean` expressions.</span></span> <span data-ttu-id="3a90e-127">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="3a90e-127">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="3a90e-128">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3a90e-128">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="3a90e-129">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="3a90e-129">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="3a90e-130">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="3a90e-130">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#OR](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#or)]  
  
## <a name="see-also"></a><span data-ttu-id="3a90e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a90e-131">See also</span></span>

- [<span data-ttu-id="3a90e-132">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="3a90e-132">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
