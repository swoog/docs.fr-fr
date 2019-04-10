---
title: ISNULL (Entity SQL)
ms.date: 03/30/2017
ms.assetid: dc7a0173-3664-4c90-a57b-5cbb0a8ed7ee
ms.openlocfilehash: aaecce3ff74d64b8e07b31329ced5b5e581fca5b
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59295092"
---
# <a name="isnull-entity-sql"></a><span data-ttu-id="f58f5-102">ISNULL (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="f58f5-102">ISNULL (Entity SQL)</span></span>
<span data-ttu-id="f58f5-103">Détermine si une expression de requête a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="f58f5-103">Determines if a query expression is null.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f58f5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f58f5-104">Syntax</span></span>  
  
```  
expression IS [ NOT ] NULL  
```  
  
## <a name="arguments"></a><span data-ttu-id="f58f5-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="f58f5-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="f58f5-106">Toute expression de requête valide.</span><span class="sxs-lookup"><span data-stu-id="f58f5-106">Any valid query expression.</span></span> <span data-ttu-id="f58f5-107">Ne peut pas être une collection, posséder des membres de collection ou être un type d'enregistrement avec des propriétés de type collection.</span><span class="sxs-lookup"><span data-stu-id="f58f5-107">Cannot be a collection, have collection members, or a record type with collection type properties.</span></span>  
  
 <span data-ttu-id="f58f5-108">NOT</span><span class="sxs-lookup"><span data-stu-id="f58f5-108">NOT</span></span>  
 <span data-ttu-id="f58f5-109">Inverse le résultat EDM.Boolean de l'opérateur IS NULL.</span><span class="sxs-lookup"><span data-stu-id="f58f5-109">Negates the EDM.Boolean result of IS NULL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f58f5-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f58f5-110">Return Value</span></span>  
 `true` <span data-ttu-id="f58f5-111">Si `expression` retourne null ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="f58f5-111">if `expression` returns null; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f58f5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f58f5-112">Remarks</span></span>  
 <span data-ttu-id="f58f5-113">Utilisez `IS NULL` pour déterminer si l'élément d'une jointure externe est NULL :</span><span class="sxs-lookup"><span data-stu-id="f58f5-113">Use `IS NULL` to determine if the element of an outer join is null:</span></span>  
  
```  
select c   
      from LOB.Customers as c left outer join LOB.Orders as o   
                              on c.ID = o.CustomerID    
      where o is not null and o.OrderQuantity = @x  
```  
  
 <span data-ttu-id="f58f5-114">Utilisez `IS NULL` pour déterminer si un membre a une valeur réelle :</span><span class="sxs-lookup"><span data-stu-id="f58f5-114">Use `IS NULL` to determine if a member has an actual value:</span></span>  
  
```  
select c from LOB.Customer as c where c.DOB is not null  
```  
  
 <span data-ttu-id="f58f5-115">Le tableau ci-dessous montre le comportement de l'opérateur `IS NULL` sur certains modèles.</span><span class="sxs-lookup"><span data-stu-id="f58f5-115">The following table shows the behavior of `IS NULL` over some patterns.</span></span> <span data-ttu-id="f58f5-116">Toutes les exceptions sont levées côté client avant que le fournisseur soit appelé :</span><span class="sxs-lookup"><span data-stu-id="f58f5-116">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="f58f5-117">Motif</span><span class="sxs-lookup"><span data-stu-id="f58f5-117">Pattern</span></span>|<span data-ttu-id="f58f5-118">Comportement</span><span class="sxs-lookup"><span data-stu-id="f58f5-118">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="f58f5-119">null IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-119">null IS NULL</span></span>|<span data-ttu-id="f58f5-120">Retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="f58f5-120">Returns `true`.</span></span>|  
|<span data-ttu-id="f58f5-121">TREAT (null AS EntityType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-121">TREAT (null AS EntityType) IS NULL</span></span>|<span data-ttu-id="f58f5-122">Retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="f58f5-122">Returns `true`.</span></span>|  
|<span data-ttu-id="f58f5-123">TREAT (null AS ComplexType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-123">TREAT (null AS ComplexType) IS NULL</span></span>|<span data-ttu-id="f58f5-124">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f58f5-124">Throws an error.</span></span>|  
|<span data-ttu-id="f58f5-125">TREAT (null AS RowType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-125">TREAT (null AS RowType) IS NULL</span></span>|<span data-ttu-id="f58f5-126">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f58f5-126">Throws an error.</span></span>|  
|<span data-ttu-id="f58f5-127">EntityType IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-127">EntityType IS NULL</span></span>|<span data-ttu-id="f58f5-128">Retourne `true` ou la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="f58f5-128">Returns `true` or `false`.</span></span>|  
|<span data-ttu-id="f58f5-129">ComplexType IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-129">ComplexType IS NULL</span></span>|<span data-ttu-id="f58f5-130">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f58f5-130">Throws an error.</span></span>|  
|<span data-ttu-id="f58f5-131">RowType IS NULL</span><span class="sxs-lookup"><span data-stu-id="f58f5-131">RowType IS NULL</span></span>|<span data-ttu-id="f58f5-132">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f58f5-132">Throws an error.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f58f5-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="f58f5-133">Example</span></span>  
 <span data-ttu-id="f58f5-134">Ce qui suit [!INCLUDE[esql](../../../../../../includes/esql-md.md)] requête utilise l’opérateur IS NOT NULL pour déterminer si une expression de requête n’est pas null.</span><span class="sxs-lookup"><span data-stu-id="f58f5-134">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the IS NOT NULL operator to determine if a query expression is not null.</span></span> <span data-ttu-id="f58f5-135">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="f58f5-135">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="f58f5-136">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f58f5-136">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="f58f5-137">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="f58f5-137">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="f58f5-138">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="f58f5-138">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#ISNULL](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#isnull)]  
  
## <a name="see-also"></a><span data-ttu-id="f58f5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58f5-139">See also</span></span>

- [<span data-ttu-id="f58f5-140">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="f58f5-140">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
