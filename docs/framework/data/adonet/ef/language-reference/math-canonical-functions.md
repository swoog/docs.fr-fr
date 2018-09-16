---
title: Fonctions mathématiques canoniques
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 0fc9f4942c3f76f139ab7e4400005f0bfe80204e
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45653185"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="ddbde-102">Fonctions mathématiques canoniques</span><span class="sxs-lookup"><span data-stu-id="ddbde-102">Math Canonical Functions</span></span>

<span data-ttu-id="ddbde-103">Entity SQL inclut les fonctions canoniques mathématiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddbde-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="ddbde-104">Abs(valeur)</span><span class="sxs-lookup"><span data-stu-id="ddbde-104">Abs(value)</span></span>

<span data-ttu-id="ddbde-105">Retourne la valeur absolue de `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-105">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="ddbde-106">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-106">**Arguments**</span></span>

<span data-ttu-id="ddbde-107">Un `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="ddbde-108">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-108">**Return Value**</span></span>

<span data-ttu-id="ddbde-109">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-109">The type of `value`.</span></span>

<span data-ttu-id="ddbde-110">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-110">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="ddbde-111">Ceiling(valeur)</span><span class="sxs-lookup"><span data-stu-id="ddbde-111">Ceiling(value)</span></span>

<span data-ttu-id="ddbde-112">Retourne le plus petit entier qui n'est pas inférieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-112">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="ddbde-113">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-113">**Arguments**</span></span>

<span data-ttu-id="ddbde-114">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-114">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="ddbde-115">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-115">**Return Value**</span></span>

<span data-ttu-id="ddbde-116">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-116">The type of `value`.</span></span>

<span data-ttu-id="ddbde-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-117">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="ddbde-118">Floor(valeur)</span><span class="sxs-lookup"><span data-stu-id="ddbde-118">Floor(value)</span></span>

<span data-ttu-id="ddbde-119">Retourne le plus grand entier qui n'est pas supérieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-119">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="ddbde-120">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-120">**Arguments**</span></span>

<span data-ttu-id="ddbde-121">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-121">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="ddbde-122">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-122">**Return Value**</span></span>

<span data-ttu-id="ddbde-123">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-123">The type of `value`.</span></span>

<span data-ttu-id="ddbde-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-124">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="ddbde-125">Power(valeur, exposant)</span><span class="sxs-lookup"><span data-stu-id="ddbde-125">Power(value, exponent)</span></span>

<span data-ttu-id="ddbde-126">Retourne le résultat de `value` à l'exposant `exponent` spécifié.</span><span class="sxs-lookup"><span data-stu-id="ddbde-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="ddbde-127">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-127">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="ddbde-128">Un `Int32, Int64, Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="ddbde-129">Un `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="ddbde-130">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-130">**Return Value**</span></span>

<span data-ttu-id="ddbde-131">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-131">The type of `value`.</span></span>

<span data-ttu-id="ddbde-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-132">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="ddbde-133">Round(valeur)</span><span class="sxs-lookup"><span data-stu-id="ddbde-133">Round(value)</span></span>

<span data-ttu-id="ddbde-134">Retourne la partie entière de `value`, arrondie à l'entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="ddbde-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="ddbde-135">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-135">**Arguments**</span></span>

<span data-ttu-id="ddbde-136">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-136">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="ddbde-137">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-137">**Return Value**</span></span>

<span data-ttu-id="ddbde-138">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-138">The type of `value`.</span></span>

<span data-ttu-id="ddbde-139">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-139">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="ddbde-140">Round(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="ddbde-140">Round(value, digits)</span></span>

<span data-ttu-id="ddbde-141">Retourne `value`, arrondi aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="ddbde-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="ddbde-142">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-142">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="ddbde-143">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-143">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="ddbde-144">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-144">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="ddbde-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-145">**Return Value**</span></span>

<span data-ttu-id="ddbde-146">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-146">The type of `value`.</span></span>

<span data-ttu-id="ddbde-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-147">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="ddbde-148">Truncate(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="ddbde-148">Truncate(value, digits)</span></span>

<span data-ttu-id="ddbde-149">Retourne `value`, tronqué aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="ddbde-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="ddbde-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="ddbde-150">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="ddbde-151">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-151">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="ddbde-152">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-152">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="ddbde-153">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="ddbde-153">**Return Value**</span></span>

<span data-ttu-id="ddbde-154">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="ddbde-154">The type of `value`.</span></span>

<span data-ttu-id="ddbde-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddbde-155">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="ddbde-156">Ces fonctions retournent `null` si une entrée de valeur `null` est fournie.</span><span class="sxs-lookup"><span data-stu-id="ddbde-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="ddbde-157">Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="ddbde-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="ddbde-158">Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ddbde-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddbde-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddbde-159">See Also</span></span>  
 [<span data-ttu-id="ddbde-160">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="ddbde-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
