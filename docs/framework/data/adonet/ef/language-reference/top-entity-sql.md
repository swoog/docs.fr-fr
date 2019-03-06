---
title: TOP (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4a4a0954-82e2-4eae-bcaf-7c4552f3532d
ms.openlocfilehash: e7c6cf6b67dc3af29f7ca8fb22af419235a9b833
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351643"
---
# <a name="top-entity-sql"></a><span data-ttu-id="2fcd4-102">TOP (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="2fcd4-102">TOP (Entity SQL)</span></span>

<span data-ttu-id="2fcd4-103">La clause SELECT peut avoir une sous-clause TOP facultative après le modificateur ALL/DISTINCT facultatif.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-103">The SELECT clause can have an optional TOP sub-clause following the optional ALL/DISTINCT modifier.</span></span> <span data-ttu-id="2fcd4-104">La sous-clause TOP spécifie que seul le premier ensemble de lignes sera retourné à partir du résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-104">The TOP sub-clause specifies that only the first set of rows will be returned from the query result.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcd4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fcd4-105">Syntax</span></span>

```
[ TOP (n) ]
```

## <a name="arguments"></a><span data-ttu-id="2fcd4-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="2fcd4-106">Arguments</span></span>

<span data-ttu-id="2fcd4-107">`n` Expression numérique qui spécifie le nombre de lignes à retourner.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-107">`n` The numeric expression that specifies the number of rows to be returned.</span></span> <span data-ttu-id="2fcd4-108">`n` peut être un littéral numérique unique ou un paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-108">`n` could be a single numeric literal or a single parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcd4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2fcd4-109">Remarks</span></span>

<span data-ttu-id="2fcd4-110">L'expression TOP doit être un littéral numérique unique ou un paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-110">The TOP expression must be either a single numeric literal or a single parameter.</span></span> <span data-ttu-id="2fcd4-111">Si un littéral constant est utilisé, le type de littéral doit implicitement pouvoir être promu en Edm.Int64 (octet, int16, int32 ou int64 ou tout type de fournisseur correspondant à un type qui peut être promu en Edm.Int64) et sa valeur doit être supérieure ou égale au zéro.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-111">If a constant literal is used, the literal type must be implicitly promotable to Edm.Int64 (byte, int16, int32 or int64 or any provider type that maps to a type that is promotable to Edm.Int64) and its value must be greater than or equal to zero.</span></span> <span data-ttu-id="2fcd4-112">Dans le cas contraire, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-112">Otherwise an exception will be raised.</span></span> <span data-ttu-id="2fcd4-113">Si un paramètre est utilisé comme expression, le type du paramètre doit aussi pouvoir être implicitement promu en Edm.Int64, mais la valeur réelle du paramètre ne pourra pas être validée au moment de la compilation, car les valeurs de paramètres sont liées tardivement.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-113">If a parameter is used as an expression, the parameter type must also be implicitly promotable to Edm.Int64, but there will be no validation of the actual parameter value during compilation because the parameter values are late bounded.</span></span>

<span data-ttu-id="2fcd4-114">L'exemple suivant est une expression TOP constante :</span><span class="sxs-lookup"><span data-stu-id="2fcd4-114">The following is an example of constant TOP expression:</span></span>

```sql
select distinct top(10) c.a1, c.a2 from T as a
```

<span data-ttu-id="2fcd4-115">Voici un exemple d’expression TOP paramétrée :</span><span class="sxs-lookup"><span data-stu-id="2fcd4-115">The following is an example of parameterized TOP expression:</span></span>

```sql
select distinct top(@topParam) c.a1, c.a2 from T as a
```

<span data-ttu-id="2fcd4-116">TOP n'est pas déterministe, à moins que la requête soit triée.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-116">TOP is non-deterministic unless the query is sorted.</span></span> <span data-ttu-id="2fcd4-117">Si vous avez besoin d'un résultat déterministe, utilisez les sous-clauses [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) et [LIMIT](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) dans la clause [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="2fcd4-117">If you require a deterministic result, use the [SKIP](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md) and [LIMIT](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md) sub-clauses in the [ORDER BY](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md) clause.</span></span> <span data-ttu-id="2fcd4-118">TOP et SKIP/LIMIT s'excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-118">The TOP and SKIP/LIMIT are mutually exclusive.</span></span>

## <a name="example"></a><span data-ttu-id="2fcd4-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="2fcd4-119">Example</span></span>

<span data-ttu-id="2fcd4-120">La requête [!INCLUDE[esql](../../../../../../includes/esql-md.md)] suivante utilise TOP pour spécifier la ligne supérieure à retourner à partir du résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-120">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the TOP to specify the top one row to be returned from the query result.</span></span> <span data-ttu-id="2fcd4-121">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="2fcd4-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="2fcd4-122">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2fcd4-122">To compile and run this query, follow these steps:</span></span>

1. <span data-ttu-id="2fcd4-123">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="2fcd4-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>

2. <span data-ttu-id="2fcd4-124">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="2fcd4-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>

    [!code-csharp[DP EntityServices Concepts 2#TOP](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#top)]

## <a name="see-also"></a><span data-ttu-id="2fcd4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fcd4-125">See also</span></span>

- [<span data-ttu-id="2fcd4-126">SELECT</span><span class="sxs-lookup"><span data-stu-id="2fcd4-126">SELECT</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)
- [<span data-ttu-id="2fcd4-127">SKIP</span><span class="sxs-lookup"><span data-stu-id="2fcd4-127">SKIP</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/skip-entity-sql.md)
- [<span data-ttu-id="2fcd4-128">LIMIT</span><span class="sxs-lookup"><span data-stu-id="2fcd4-128">LIMIT</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/limit-entity-sql.md)
- [<span data-ttu-id="2fcd4-129">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="2fcd4-129">ORDER BY</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md)
- [<span data-ttu-id="2fcd4-130">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="2fcd4-130">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
