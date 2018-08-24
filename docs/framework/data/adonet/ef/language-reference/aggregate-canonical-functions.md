---
title: Fonctions d'agrégation canoniques
ms.date: 03/30/2017
ms.assetid: 3bcff826-ca90-41b3-a791-04d6ff0e5085
ms.openlocfilehash: e4772176130fc72a22645462921c90dd5b7967b2
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42754476"
---
# <a name="aggregate-canonical-functions"></a><span data-ttu-id="035e3-102">Fonctions d'agrégation canoniques</span><span class="sxs-lookup"><span data-stu-id="035e3-102">Aggregate Canonical Functions</span></span>

<span data-ttu-id="035e3-103">Les agrégats sont des expressions qui réduisent une série de valeurs d'entrée en, par exemple, une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="035e3-103">Aggregates are expressions that reduce a series of input values into, for example, a single value.</span></span> <span data-ttu-id="035e3-104">Ils sont normalement utilisés avec la clause GROUP BY de l'expression SELECT et leur utilisation est sujette à certaines contraintes.</span><span class="sxs-lookup"><span data-stu-id="035e3-104">Aggregates are normally used in conjunction with the GROUP BY clause of the SELECT expression, and there are constraints on where they can be used.</span></span>

## <a name="aggegate-entity-sql-canonical-functions"></a><span data-ttu-id="035e3-105">Fonctions canoniques Aggegate Entity SQL</span><span class="sxs-lookup"><span data-stu-id="035e3-105">Aggegate Entity SQL canonical functions</span></span>

<span data-ttu-id="035e3-106">Les fonctions canoniques Entity SQL d’agrégation sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="035e3-106">The following are the aggregate Entity SQL canonical functions.</span></span>

### <a name="avgexpression"></a><span data-ttu-id="035e3-107">Avg(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-107">Avg(expression)</span></span>

<span data-ttu-id="035e3-108">Retourne la moyenne des valeurs non Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-108">Returns the average of the non-null values.</span></span>

<span data-ttu-id="035e3-109">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-109">**Arguments**</span></span>

<span data-ttu-id="035e3-110">Un `Int32`, `Int64`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-110">An `Int32`, `Int64`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="035e3-111">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-111">**Return Value**</span></span>

<span data-ttu-id="035e3-112">Le type de `expression`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-112">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-113">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-113">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_AVG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_avg)] 
[!code-sql[DP EntityServices Concepts#EDM_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_avg)]

### <a name="bigcountexpression"></a><span data-ttu-id="035e3-114">BigCount(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-114">BigCount(expression)</span></span>

<span data-ttu-id="035e3-115">Retourne la taille de l'agrégat, y compris les valeurs Null et dupliquées.</span><span class="sxs-lookup"><span data-stu-id="035e3-115">Returns the size of the aggregate including null and duplicate values.</span></span>

<span data-ttu-id="035e3-116">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-116">**Arguments**</span></span>

<span data-ttu-id="035e3-117">N'importe quel type.</span><span class="sxs-lookup"><span data-stu-id="035e3-117">Any type.</span></span>

<span data-ttu-id="035e3-118">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-118">**Return Value**</span></span>

<span data-ttu-id="035e3-119">Élément `Int64`.</span><span class="sxs-lookup"><span data-stu-id="035e3-119">An `Int64`.</span></span>

<span data-ttu-id="035e3-120">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-120">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_BIGCOUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_bigcount)] 
[!code-sql[DP EntityServices Concepts#EDM_BIGCOUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_bigcount)]

### <a name="countexpression"></a><span data-ttu-id="035e3-121">Count(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-121">Count(expression)</span></span> 

<span data-ttu-id="035e3-122">Retourne la taille de l'agrégat, y compris les valeurs Null et dupliquées.</span><span class="sxs-lookup"><span data-stu-id="035e3-122">Returns the size of the aggregate including null and duplicate values.</span></span>

<span data-ttu-id="035e3-123">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-123">**Arguments**</span></span>

<span data-ttu-id="035e3-124">N'importe quel type.</span><span class="sxs-lookup"><span data-stu-id="035e3-124">Any type.</span></span>

<span data-ttu-id="035e3-125">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-125">**Return Value**</span></span>

<span data-ttu-id="035e3-126">Élément `Int32`.</span><span class="sxs-lookup"><span data-stu-id="035e3-126">An `Int32`.</span></span>

<span data-ttu-id="035e3-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-127">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_COUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_count)]
[!code-sql[DP EntityServices Concepts#EDM_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_count)]

### <a name="maxexpression"></a><span data-ttu-id="035e3-128">Max(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-128">Max(expression)</span></span>

<span data-ttu-id="035e3-129">Retourne la valeur maximale des valeurs non-Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-129">Returns the maximum of the non-null values.</span></span>

<span data-ttu-id="035e3-130">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-130">**Arguments**</span></span>

<span data-ttu-id="035e3-131">`Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span><span class="sxs-lookup"><span data-stu-id="035e3-131">A `Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span></span>

<span data-ttu-id="035e3-132">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-132">**Return Value**</span></span>

<span data-ttu-id="035e3-133">Le type de `expression`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-133">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-134">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_MAX](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_max)]
[!code-sql[DP EntityServices Concepts#EDM_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_max)]

### <a name="minexpression"></a><span data-ttu-id="035e3-135">Min(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-135">Min(expression)</span></span>

<span data-ttu-id="035e3-136">Retourne la valeur minimale des valeurs non Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-136">Returns the minimum of the non-null values.</span></span>

<span data-ttu-id="035e3-137">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-137">**Arguments**</span></span>

<span data-ttu-id="035e3-138">`Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span><span class="sxs-lookup"><span data-stu-id="035e3-138">A `Byte`, `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, `Decimal`, `DateTime`, `DateTimeOffset`, `Time`, `String`, `Binary`.</span></span>

<span data-ttu-id="035e3-139">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-139">**Return Value**</span></span>

<span data-ttu-id="035e3-140">Le type de `expression`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-140">The type of `expression`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-141">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-141">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_MIN](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_min)]
[!code-sql[DP EntityServices Concepts#EDM_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_min)]

### <a name="stdevexpression"></a><span data-ttu-id="035e3-142">StDev(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-142">StDev(expression)</span></span>

<span data-ttu-id="035e3-143">Retourne l'écart type des valeurs non Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-143">Returns the standard deviation of the non-null values.</span></span>

<span data-ttu-id="035e3-144">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-144">**Arguments**</span></span>

<span data-ttu-id="035e3-145">`Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-145">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="035e3-146">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-146">**Return Value**</span></span>

<span data-ttu-id="035e3-147">`Double`</span><span class="sxs-lookup"><span data-stu-id="035e3-147">A `Double`.</span></span> <span data-ttu-id="035e3-148">`Null` si toutes les valeurs d'entrée sont `null`.</span><span class="sxs-lookup"><span data-stu-id="035e3-148">`Null`, if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-149">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-149">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_STDEV](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_stdev)]
[!code-sql[DP EntityServices Concepts#EDM_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_stdev)]

### <a name="stdevpexpression"></a><span data-ttu-id="035e3-150">StDevP(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-150">StDevP(expression)</span></span>

<span data-ttu-id="035e3-151">Retourne l'écart type pour le remplissage de toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-151">Returns the standard deviation for the population of all values.</span></span>

<span data-ttu-id="035e3-152">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-152">**Arguments**</span></span>

<span data-ttu-id="035e3-153">`Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-153">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="035e3-154">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-154">**Return Value**</span></span>

<span data-ttu-id="035e3-155">Un `Double`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-155">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-156">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-156">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_STDEVP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_stdevp)]
[!code-sql[DP EntityServices Concepts#EDM_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_stdevp)]

### <a name="sumexpression"></a><span data-ttu-id="035e3-157">Sum(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-157">Sum(expression)</span></span>

<span data-ttu-id="035e3-158">Retourne la somme des valeurs non-Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-158">Returns the sum of the non-null values.</span></span>

<span data-ttu-id="035e3-159">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-159">**Arguments**</span></span>

<span data-ttu-id="035e3-160">`Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-160">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="035e3-161">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-161">**Return Value**</span></span>

<span data-ttu-id="035e3-162">Un `Double`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-162">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-163">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-163">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_SUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_sum)]
[!code-sql[DP EntityServices Concepts#EDM_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_sum)]

### <a name="varexpression"></a><span data-ttu-id="035e3-164">Var(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-164">Var(expression)</span></span>

<span data-ttu-id="035e3-165">Retourne la variance de toutes les valeurs non-Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-165">Returns the variance of all non-null values.</span></span>

<span data-ttu-id="035e3-166">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-166">**Arguments**</span></span>

<span data-ttu-id="035e3-167">`Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-167">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="035e3-168">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-168">**Return Value**</span></span>

<span data-ttu-id="035e3-169">Un `Double`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-169">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-170">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-170">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_VAR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_var)]
[!code-sql[DP EntityServices Concepts#EDM_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_var)]

### <a name="varpexpression"></a><span data-ttu-id="035e3-171">VarP(expression)</span><span class="sxs-lookup"><span data-stu-id="035e3-171">VarP(expression)</span></span>

<span data-ttu-id="035e3-172">Retourne la variance pour le remplissage de toutes les valeurs non-Null.</span><span class="sxs-lookup"><span data-stu-id="035e3-172">Returns the variance for the population of all non-null values.</span></span>

<span data-ttu-id="035e3-173">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="035e3-173">**Arguments**</span></span>

<span data-ttu-id="035e3-174">`Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="035e3-174">An `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="035e3-175">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="035e3-175">**Return Value**</span></span>

<span data-ttu-id="035e3-176">Un `Double`, ou `null` si toutes les valeurs d’entrée sont `null` valeurs.</span><span class="sxs-lookup"><span data-stu-id="035e3-176">A `Double`, or `null` if all input values are `null` values.</span></span>

<span data-ttu-id="035e3-177">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="035e3-177">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_VARP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_varp)]
[!code-sql[DP EntityServices Concepts#EDM_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_varp)] 

<span data-ttu-id="035e3-178">Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="035e3-178">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="035e3-179">Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span><span class="sxs-lookup"><span data-stu-id="035e3-179">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>

## <a name="collection-based-aggregates"></a><span data-ttu-id="035e3-180">Agrégats basés sur les collections</span><span class="sxs-lookup"><span data-stu-id="035e3-180">Collection-based aggregates</span></span>

<span data-ttu-id="035e3-181">Les agrégats basés sur des collections (fonctions de collection) opèrent sur des collections et retournent une valeur.</span><span class="sxs-lookup"><span data-stu-id="035e3-181">Collection-based aggregates (collection functions) operate on collections and return a value.</span></span> <span data-ttu-id="035e3-182">Par exemple si ORDERS est une collection de toutes les commandes, vous pouvez calculer la première date d’expédition avec l’expression suivante :</span><span class="sxs-lookup"><span data-stu-id="035e3-182">For example if ORDERS is a collection of all orders, you can calculate the earliest ship date with the following expression:</span></span>

```sql
min(select value o.ShipDate from LOB.Orders as o)
```

<span data-ttu-id="035e3-183">Les expressions figurant dans des agrégats basés sur des collections sont évalués dans la résolution de noms de portée ambiante actuelle.</span><span class="sxs-lookup"><span data-stu-id="035e3-183">Expressions inside collection-based aggregates are evaluated within the current ambient name-resolution scope.</span></span>

## <a name="group-based-aggregates"></a><span data-ttu-id="035e3-184">Agrégats basés sur le groupe</span><span class="sxs-lookup"><span data-stu-id="035e3-184">Group-based aggregates</span></span>

<span data-ttu-id="035e3-185">Les agrégats basés sur des groupes sont calculés sur un groupe défini par la clause GROUP BY.</span><span class="sxs-lookup"><span data-stu-id="035e3-185">Group-based aggregates are calculated over a group as defined by the GROUP BY clause.</span></span> <span data-ttu-id="035e3-186">Pour chaque groupe du résultat, un agrégat distinct est calculé en utilisant les éléments de chaque groupe fourni en entrée pour le calcul.</span><span class="sxs-lookup"><span data-stu-id="035e3-186">For each group in the result, a separate aggregate is calculated by using the elements in each group as input to the aggregate calculation.</span></span> <span data-ttu-id="035e3-187">Lorsqu'une clause group-by est utilisée dans une expression select, seuls des noms d'expressions de regroupement, des agrégats ou des expressions constantes peuvent figurer dans la projection ou la clause order-by.</span><span class="sxs-lookup"><span data-stu-id="035e3-187">When a group-by clause is used in a select expression, only grouping expression names, aggregates, or constant expressions can be present in the projection or order-by clause.</span></span>

<span data-ttu-id="035e3-188">L'exemple suivant calcule la quantité moyenne commandée pour chaque produit :</span><span class="sxs-lookup"><span data-stu-id="035e3-188">The following example calculates the average quantity ordered for each product:</span></span>

```sql
select p, avg(ol.Quantity) from LOB.OrderLines as ol 
  group by ol.Product as p
```

<span data-ttu-id="035e3-189">Il est possible d’avoir un agrégat basé sur le groupe sans une clause group by explicite dans l’expression SELECT.</span><span class="sxs-lookup"><span data-stu-id="035e3-189">It's possible to have a group-based aggregate without an explicit group-by clause in the SELECT expression.</span></span> <span data-ttu-id="035e3-190">Dans ce cas, tous les éléments sont traités comme un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="035e3-190">In this case, all elements are treated as a single group.</span></span> <span data-ttu-id="035e3-191">Cela est équivalent de spécifier un regroupement basé sur une constante.</span><span class="sxs-lookup"><span data-stu-id="035e3-191">This is equivalent of specifying a grouping based on a constant.</span></span> <span data-ttu-id="035e3-192">L'expression suivante, par exemple :</span><span class="sxs-lookup"><span data-stu-id="035e3-192">Take, for example, the following expression:</span></span>

```sql
select avg(ol.Quantity) from LOB.OrderLines as ol
```

<span data-ttu-id="035e3-193">est équivalente à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="035e3-193">This is equivalent to the following:</span></span>

```sql
select avg(ol.Quantity) from LOB.OrderLines as ol group by 1
```

<span data-ttu-id="035e3-194">Les expressions figurant dans des agrégats basés sur des groupes sont évalués dans la résolution de noms de portée qui serait visible pour l’expression de la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="035e3-194">Expressions inside the group-based aggregate are evaluated within the name-resolution scope that would be visible to the WHERE clause expression.</span></span>

<span data-ttu-id="035e3-195">Comme dans [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)], agrégats basés sur le groupe peuvent également spécifier un ALL ou modificateur DISTINCT.</span><span class="sxs-lookup"><span data-stu-id="035e3-195">As in [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)], group-based aggregates can also specify an ALL or DISTINCT modifier.</span></span> <span data-ttu-id="035e3-196">Si le modificateur DISTINCT est spécifié, les doublons sont éliminés de la collection d’entrée de l’agrégat, avant que celui-ci ne soit calculé.</span><span class="sxs-lookup"><span data-stu-id="035e3-196">If the DISTINCT modifier is specified, duplicates are eliminated from the aggregate input collection, before the aggregate is computed.</span></span> <span data-ttu-id="035e3-197">Si le modificateur ALL est spécifié (ou si aucun modificateur ne l'est), les doublons ne sont pas éliminés.</span><span class="sxs-lookup"><span data-stu-id="035e3-197">If the ALL modifier is specified (or if no modifier is specified), no duplicate elimination is performed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="035e3-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="035e3-198">See also</span></span>

[<span data-ttu-id="035e3-199">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="035e3-199">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
