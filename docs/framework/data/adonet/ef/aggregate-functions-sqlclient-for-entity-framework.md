---
title: Fonctions d’agrégation (SqlClient pour Entity Framework)
ms.date: 03/30/2017
ms.assetid: 03303f01-b591-4efc-9875-f9c608edff0b
ms.openlocfilehash: 8ed9a58da9914724fe312876d6594cb526f2e0e9
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43856515"
---
# <a name="aggregate-functions-sqlclient-for-entity-framework"></a><span data-ttu-id="6060a-102">Fonctions d’agrégation (SqlClient pour Entity Framework)</span><span class="sxs-lookup"><span data-stu-id="6060a-102">Aggregate Functions (SqlClient for Entity Framework)</span></span>
<span data-ttu-id="6060a-103">Le fournisseur de données .NET Framework pour SQL Server (SqlClient) fournit des fonctions d'agrégation.</span><span class="sxs-lookup"><span data-stu-id="6060a-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides aggregate functions.</span></span> <span data-ttu-id="6060a-104">Les fonctions d'agrégation effectuent des calculs sur un ensemble de valeurs d'entrée et retournent une valeur.</span><span class="sxs-lookup"><span data-stu-id="6060a-104">Aggregate functions perform calculations on a set of input values and return a value.</span></span> <span data-ttu-id="6060a-105">Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient.</span><span class="sxs-lookup"><span data-stu-id="6060a-105">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="6060a-106">La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions.</span><span class="sxs-lookup"><span data-stu-id="6060a-106">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span>  
  
 <span data-ttu-id="6060a-107">Voici les fonctions d’agrégation SqlClient.</span><span class="sxs-lookup"><span data-stu-id="6060a-107">The following are the SqlClient aggregate functions.</span></span>  

## <a name="avgexpression"></a><span data-ttu-id="6060a-108">AVG(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-108">AVG(expression)</span></span>

<span data-ttu-id="6060a-109">Retourne la moyenne des valeurs d’une collection.</span><span class="sxs-lookup"><span data-stu-id="6060a-109">Returns the average of the values in a collection.</span></span> <span data-ttu-id="6060a-110">Les valeurs NULL sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="6060a-110">Null values are ignored.</span></span>

<span data-ttu-id="6060a-111">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-111">**Arguments**</span></span>

<span data-ttu-id="6060a-112">Un `Int32`, `Int64`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="6060a-112">An `Int32`, `Int64`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="6060a-113">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-113">**Return Value**</span></span>

<span data-ttu-id="6060a-114">Type d'élément `expression`.</span><span class="sxs-lookup"><span data-stu-id="6060a-114">The type of `expression`.</span></span>

<span data-ttu-id="6060a-115">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-115">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_avg)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_avg)]

## <a name="checksumaggcollection"></a><span data-ttu-id="6060a-116">CHECKSUM_AGG(collection)</span><span class="sxs-lookup"><span data-stu-id="6060a-116">CHECKSUM_AGG(collection)</span></span>
 
 <span data-ttu-id="6060a-117">Retourne la somme de contrôle des valeurs d’une collection.</span><span class="sxs-lookup"><span data-stu-id="6060a-117">Returns the checksum of the values in a collection.</span></span> <span data-ttu-id="6060a-118">Les valeurs NULL sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="6060a-118">Null values are ignored.</span></span>
 
 <span data-ttu-id="6060a-119">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-119">**Arguments**</span></span>
 
 <span data-ttu-id="6060a-120">Une Collection (`Int32`).</span><span class="sxs-lookup"><span data-stu-id="6060a-120">A Collection(`Int32`).</span></span>
 
 <span data-ttu-id="6060a-121">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-121">**Return Value**</span></span>
 
 <span data-ttu-id="6060a-122">Élément `Int32`.</span><span class="sxs-lookup"><span data-stu-id="6060a-122">An `Int32`.</span></span>
 
 <span data-ttu-id="6060a-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-123">**Example**</span></span>
 
 [!code-csharp[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_checksum)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_checksum)]
   
## <a name="countexpression"></a><span data-ttu-id="6060a-124">Count(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-124">COUNT(expression)</span></span>

<span data-ttu-id="6060a-125">Retourne le nombre d'éléments d'une collection sous la forme d'une valeur `Int32`.</span><span class="sxs-lookup"><span data-stu-id="6060a-125">Returns the number of items in a collection as an `Int32`.</span></span>

<span data-ttu-id="6060a-126">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-126">**Arguments**</span></span>

<span data-ttu-id="6060a-127">Une Collection\<T >, où T est un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="6060a-127">A Collection\<T>, where T is one of the following types:</span></span>

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="6060a-128">`Guid` (non retourné dans SQL Server 2000)</span><span class="sxs-lookup"><span data-stu-id="6060a-128">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="6060a-129">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-129">**Return Value**</span></span>

<span data-ttu-id="6060a-130">Élément `Int32`.</span><span class="sxs-lookup"><span data-stu-id="6060a-130">An `Int32`.</span></span>

<span data-ttu-id="6060a-131">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-131">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_count)]
<span data-ttu-id="6060a-132">[ ! code non-SQL[DP EntityServices Concepts #SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)</span><span class="sxs-lookup"><span data-stu-id="6060a-132">[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)</span></span>
 
## <a name="countbigexpression"></a><span data-ttu-id="6060a-133">COUNT_BIG(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-133">COUNT_BIG(expression)</span></span>
 
 <span data-ttu-id="6060a-134">Retourne le nombre d'éléments d'une collection sous la forme d'une valeur `bigint`.</span><span class="sxs-lookup"><span data-stu-id="6060a-134">Returns the number of items in a collection as a `bigint`.</span></span>
 
 <span data-ttu-id="6060a-135">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-135">**Arguments**</span></span>
 
 <span data-ttu-id="6060a-136">Collection(T), où T est un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="6060a-136">A Collection(T), where T is one of the following types:</span></span>
 
 |   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|<span data-ttu-id="6060a-137">`Guid` (non retourné dans SQL Server 2000)</span><span class="sxs-lookup"><span data-stu-id="6060a-137">`Guid` (not returned in SQL Server 2000)</span></span>|

<span data-ttu-id="6060a-138">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-138">**Return Value**</span></span>

<span data-ttu-id="6060a-139">Élément `Int64`.</span><span class="sxs-lookup"><span data-stu-id="6060a-139">An `Int64`.</span></span>

<span data-ttu-id="6060a-140">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-140">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_countbig)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_countbig)]

## <a name="maxexpression"></a><span data-ttu-id="6060a-141">MAX(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-141">MAX(expression)</span></span>

<span data-ttu-id="6060a-142">Retourne la valeur maximale contenue dans la collection.</span><span class="sxs-lookup"><span data-stu-id="6060a-142">Returns the maximum value the collection.</span></span>

<span data-ttu-id="6060a-143">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-143">**Arguments**</span></span>

<span data-ttu-id="6060a-144">Collection(T), où T est un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="6060a-144">A Collection(T), where T is one of the following types:</span></span> 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="6060a-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-145">**Return Value**</span></span>

<span data-ttu-id="6060a-146">Type d'élément `expression`.</span><span class="sxs-lookup"><span data-stu-id="6060a-146">The type of `expression`.</span></span>

<span data-ttu-id="6060a-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-147">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_max)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_max)]

## <a name="minexpression"></a><span data-ttu-id="6060a-148">MIN(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-148">MIN(expression)</span></span>

<span data-ttu-id="6060a-149">Retourne la valeur minimale contenue dans une collection.</span><span class="sxs-lookup"><span data-stu-id="6060a-149">Returns the minimum value in a collection.</span></span>

<span data-ttu-id="6060a-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-150">**Arguments**</span></span>

<span data-ttu-id="6060a-151">Collection(T), où T est un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="6060a-151">A Collection(T), where T is one of the following types:</span></span> 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

<span data-ttu-id="6060a-152">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-152">**Return Value**</span></span>

<span data-ttu-id="6060a-153">Type d'élément `expression`.</span><span class="sxs-lookup"><span data-stu-id="6060a-153">The type of `expression`.</span></span>

<span data-ttu-id="6060a-154">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-154">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_min)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_min)]

## <a name="stdevexpression"></a><span data-ttu-id="6060a-155">StDev(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-155">STDEV(expression)</span></span>

<span data-ttu-id="6060a-156">Retourne l'écart type statistique de toutes les valeurs de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6060a-156">Returns the statistical standard deviation of all values in the specified expression.</span></span>

<span data-ttu-id="6060a-157">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-157">**Arguments**</span></span>

<span data-ttu-id="6060a-158">Une Collection (`Double`).</span><span class="sxs-lookup"><span data-stu-id="6060a-158">A Collection(`Double`).</span></span>

<span data-ttu-id="6060a-159">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-159">**Return Value**</span></span>

<span data-ttu-id="6060a-160">`Double`</span><span class="sxs-lookup"><span data-stu-id="6060a-160">A `Double`.</span></span>

<span data-ttu-id="6060a-161">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-161">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdev)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdev)]

## <a name="stdevpexpression"></a><span data-ttu-id="6060a-162">StDevP(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-162">STDEVP(expression)</span></span>

<span data-ttu-id="6060a-163">Retourne l'écart type statistique du remplissage de toutes les valeurs de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6060a-163">Returns the statistical standard deviation for the population for all values in the specified expression.</span></span>

<span data-ttu-id="6060a-164">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-164">**Arguments**</span></span>

<span data-ttu-id="6060a-165">Une Collection (`Double`).</span><span class="sxs-lookup"><span data-stu-id="6060a-165">A Collection(`Double`).</span></span>

<span data-ttu-id="6060a-166">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-166">**Return Value**</span></span>

<span data-ttu-id="6060a-167">`Double`</span><span class="sxs-lookup"><span data-stu-id="6060a-167">A `Double`.</span></span>

<span data-ttu-id="6060a-168">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-168">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdevp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdevp)]

## <a name="sumexpression"></a><span data-ttu-id="6060a-169">SUM(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-169">SUM(expression)</span></span>

<span data-ttu-id="6060a-170">Retourne la somme de toutes les valeurs de la collection.</span><span class="sxs-lookup"><span data-stu-id="6060a-170">Returns the sum of all the values in the collection.</span></span>

<span data-ttu-id="6060a-171">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-171">**Arguments**</span></span>

<span data-ttu-id="6060a-172">Un Collection(T) où T est un des types suivants : `Int32`, `Int64`, `Double`, `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="6060a-172">A Collection(T) where T is one of the following types: `Int32`, `Int64`, `Double`, `Decimal`.</span></span>

<span data-ttu-id="6060a-173">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-173">**Return Value**</span></span>

<span data-ttu-id="6060a-174">Type d'élément `expression`.</span><span class="sxs-lookup"><span data-stu-id="6060a-174">The type of `expression`.</span></span>

<span data-ttu-id="6060a-175">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-175">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_sum)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_sum)]

## <a name="varexpression"></a><span data-ttu-id="6060a-176">VAR(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-176">VAR(expression)</span></span>

<span data-ttu-id="6060a-177">Retourne la variance statistique de toutes les valeurs dans l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6060a-177">Returns the statistical variance of all values in the specified expression.</span></span>

<span data-ttu-id="6060a-178">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-178">**Arguments**</span></span>

<span data-ttu-id="6060a-179">Une Collection (`Double`).</span><span class="sxs-lookup"><span data-stu-id="6060a-179">A Collection(`Double`).</span></span>

<span data-ttu-id="6060a-180">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-180">**Return Value**</span></span>

<span data-ttu-id="6060a-181">`Double`</span><span class="sxs-lookup"><span data-stu-id="6060a-181">A `Double`.</span></span>

<span data-ttu-id="6060a-182">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-182">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_var)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_var)]

## <a name="varpexpression"></a><span data-ttu-id="6060a-183">VarP(expression)</span><span class="sxs-lookup"><span data-stu-id="6060a-183">VARP(expression)</span></span>

<span data-ttu-id="6060a-184">Retourne la variance statistique de remplissage pour toutes les valeurs de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6060a-184">Returns the statistical variance for the population for all values in the specified expression.</span></span>

<span data-ttu-id="6060a-185">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="6060a-185">**Arguments**</span></span>

<span data-ttu-id="6060a-186">Une Collection (`Double`).</span><span class="sxs-lookup"><span data-stu-id="6060a-186">A Collection(`Double`).</span></span>

<span data-ttu-id="6060a-187">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="6060a-187">**Return Value**</span></span>

<span data-ttu-id="6060a-188">`Double`</span><span class="sxs-lookup"><span data-stu-id="6060a-188">A `Double`.</span></span>

<span data-ttu-id="6060a-189">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6060a-189">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_varp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_varp)] 
  
## <a name="see-also"></a><span data-ttu-id="6060a-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6060a-190">See also</span></span>

<span data-ttu-id="6060a-191">Pour plus d'informations sur les fonctions d'agrégation prises en charge par SqlClient, voir la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :</span><span class="sxs-lookup"><span data-stu-id="6060a-191">For more information about the aggregate functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="6060a-192">**SQL Server 2005**: [fonctions d’agrégation (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms173454(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="6060a-192">**SQL Server 2005**: [Aggregate Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms173454(v=sql.90))</span></span>  
<span data-ttu-id="6060a-193">**SQL Server 2008 et versions ultérieur**: [les fonctions d’agrégation (Transact-SQL)](/sql/t-sql/functions/aggregate-functions-transact-sql)</span><span class="sxs-lookup"><span data-stu-id="6060a-193">**SQL Server 2008 and later**:  [Aggregate Functions (Transact-SQL)](/sql/t-sql/functions/aggregate-functions-transact-sql)</span></span>  
[<span data-ttu-id="6060a-194">Langage Entity SQL</span><span class="sxs-lookup"><span data-stu-id="6060a-194">Entity SQL Language</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)  
[<span data-ttu-id="6060a-195">Fonctions canoniques d’agrégation</span><span class="sxs-lookup"><span data-stu-id="6060a-195">Aggregate Canonical Functions</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/aggregate-canonical-functions.md)
