---
title: Fonctions mathématiques canoniques
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 0fc9f4942c3f76f139ab7e4400005f0bfe80204e
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43740352"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="8f3f4-102">Fonctions mathématiques canoniques</span><span class="sxs-lookup"><span data-stu-id="8f3f4-102">Math Canonical Functions</span></span>

<span data-ttu-id="8f3f4-103">Entity SQL inclut les fonctions canoniques mathématiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f3f4-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="8f3f4-104">Abs(valeur)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-104">Abs(value)</span></span>

<span data-ttu-id="8f3f4-105">Retourne la valeur absolue de `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-105">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="8f3f4-106">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-106">**Arguments**</span></span>

<span data-ttu-id="8f3f4-107">Un `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="8f3f4-108">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-108">**Return Value**</span></span>

<span data-ttu-id="8f3f4-109">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-109">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-110">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-110">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="8f3f4-111">Ceiling(valeur)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-111">Ceiling(value)</span></span>

<span data-ttu-id="8f3f4-112">Retourne le plus petit entier qui n'est pas inférieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-112">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="8f3f4-113">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-113">**Arguments**</span></span>

<span data-ttu-id="8f3f4-114">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-114">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="8f3f4-115">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-115">**Return Value**</span></span>

<span data-ttu-id="8f3f4-116">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-116">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-117">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="8f3f4-118">Floor(valeur)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-118">Floor(value)</span></span>

<span data-ttu-id="8f3f4-119">Retourne le plus grand entier qui n'est pas supérieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-119">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="8f3f4-120">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-120">**Arguments**</span></span>

<span data-ttu-id="8f3f4-121">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-121">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="8f3f4-122">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-122">**Return Value**</span></span>

<span data-ttu-id="8f3f4-123">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-123">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-124">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="8f3f4-125">Power(valeur, exposant)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-125">Power(value, exponent)</span></span>

<span data-ttu-id="8f3f4-126">Retourne le résultat de `value` à l'exposant `exponent` spécifié.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="8f3f4-127">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-127">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="8f3f4-128">Un `Int32, Int64, Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="8f3f4-129">Un `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="8f3f4-130">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-130">**Return Value**</span></span>

<span data-ttu-id="8f3f4-131">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-131">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-132">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="8f3f4-133">Round(valeur)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-133">Round(value)</span></span>

<span data-ttu-id="8f3f4-134">Retourne la partie entière de `value`, arrondie à l'entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="8f3f4-135">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-135">**Arguments**</span></span>

<span data-ttu-id="8f3f4-136">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-136">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="8f3f4-137">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-137">**Return Value**</span></span>

<span data-ttu-id="8f3f4-138">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-138">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-139">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-139">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="8f3f4-140">Round(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-140">Round(value, digits)</span></span>

<span data-ttu-id="8f3f4-141">Retourne `value`, arrondi aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="8f3f4-142">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-142">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="8f3f4-143">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-143">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="8f3f4-144">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-144">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="8f3f4-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-145">**Return Value**</span></span>

<span data-ttu-id="8f3f4-146">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-146">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-147">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="8f3f4-148">Truncate(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="8f3f4-148">Truncate(value, digits)</span></span>

<span data-ttu-id="8f3f4-149">Retourne `value`, tronqué aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="8f3f4-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-150">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="8f3f4-151">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-151">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="8f3f4-152">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-152">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="8f3f4-153">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-153">**Return Value**</span></span>

<span data-ttu-id="8f3f4-154">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-154">The type of `value`.</span></span>

<span data-ttu-id="8f3f4-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8f3f4-155">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="8f3f4-156">Ces fonctions retournent `null` si une entrée de valeur `null` est fournie.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="8f3f4-157">Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="8f3f4-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="8f3f4-158">Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8f3f4-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f3f4-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f3f4-159">See Also</span></span>  
 [<span data-ttu-id="8f3f4-160">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="8f3f4-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
