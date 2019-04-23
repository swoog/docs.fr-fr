---
title: Fonctions mathématiques canoniques
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: f575785bb198251ef50ba3563e736946253c9526
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228768"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="9b6be-102">Fonctions mathématiques canoniques</span><span class="sxs-lookup"><span data-stu-id="9b6be-102">Math Canonical Functions</span></span>

<span data-ttu-id="9b6be-103">Entity SQL inclut les fonctions canoniques mathématiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9b6be-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="9b6be-104">Abs(valeur)</span><span class="sxs-lookup"><span data-stu-id="9b6be-104">Abs(value)</span></span>

<span data-ttu-id="9b6be-105">Retourne la valeur absolue de `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-105">Returns the absolute value of `value`.</span></span>

<span data-ttu-id="9b6be-106">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-106">**Arguments**</span></span>

<span data-ttu-id="9b6be-107">Un `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="9b6be-108">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-108">**Return Value**</span></span>

<span data-ttu-id="9b6be-109">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-109">The type of `value`.</span></span>

<span data-ttu-id="9b6be-110">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-110">**Example**</span></span>

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="9b6be-111">Ceiling(valeur)</span><span class="sxs-lookup"><span data-stu-id="9b6be-111">Ceiling(value)</span></span>

<span data-ttu-id="9b6be-112">Retourne le plus petit entier qui n'est pas inférieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-112">Returns the smallest integer that is not less than `value`.</span></span>

<span data-ttu-id="9b6be-113">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-113">**Arguments**</span></span>

<span data-ttu-id="9b6be-114">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-114">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="9b6be-115">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-115">**Return Value**</span></span>

<span data-ttu-id="9b6be-116">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-116">The type of `value`.</span></span>

<span data-ttu-id="9b6be-117">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-117">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="9b6be-118">Floor(valeur)</span><span class="sxs-lookup"><span data-stu-id="9b6be-118">Floor(value)</span></span>

<span data-ttu-id="9b6be-119">Retourne le plus grand entier qui n'est pas supérieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-119">Returns the largest integer that is not greater than `value`.</span></span>

<span data-ttu-id="9b6be-120">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-120">**Arguments**</span></span>

<span data-ttu-id="9b6be-121">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-121">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="9b6be-122">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-122">**Return Value**</span></span>

<span data-ttu-id="9b6be-123">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-123">The type of `value`.</span></span>

<span data-ttu-id="9b6be-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-124">**Example**</span></span>

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="9b6be-125">Power(valeur, exposant)</span><span class="sxs-lookup"><span data-stu-id="9b6be-125">Power(value, exponent)</span></span>

<span data-ttu-id="9b6be-126">Retourne le résultat de `value` à l'exposant `exponent` spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b6be-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

<span data-ttu-id="9b6be-127">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-127">**Arguments**</span></span>

|  |  |
|--|--|
|`value` | <span data-ttu-id="9b6be-128">Un `Int32, Int64, Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="9b6be-129">Un `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

<span data-ttu-id="9b6be-130">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-130">**Return Value**</span></span>

<span data-ttu-id="9b6be-131">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-131">The type of `value`.</span></span>

<span data-ttu-id="9b6be-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-132">**Example**</span></span>

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="9b6be-133">Round(valeur)</span><span class="sxs-lookup"><span data-stu-id="9b6be-133">Round(value)</span></span>

<span data-ttu-id="9b6be-134">Retourne la partie entière de `value`, arrondie à l'entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="9b6be-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

<span data-ttu-id="9b6be-135">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-135">**Arguments**</span></span>

<span data-ttu-id="9b6be-136">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-136">A `Single`, `Double`, and `Decimal`.</span></span>

<span data-ttu-id="9b6be-137">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-137">**Return Value**</span></span>

<span data-ttu-id="9b6be-138">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-138">The type of `value`.</span></span>

<span data-ttu-id="9b6be-139">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-139">**Example**</span></span>

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="9b6be-140">Round(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="9b6be-140">Round(value, digits)</span></span>

<span data-ttu-id="9b6be-141">Retourne `value`, arrondi aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="9b6be-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

<span data-ttu-id="9b6be-142">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-142">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="9b6be-143">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-143">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="9b6be-144">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-144">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="9b6be-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-145">**Return Value**</span></span>

<span data-ttu-id="9b6be-146">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-146">The type of `value`.</span></span>

<span data-ttu-id="9b6be-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-147">**Example**</span></span>

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="9b6be-148">Truncate(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="9b6be-148">Truncate(value, digits)</span></span>

<span data-ttu-id="9b6be-149">Retourne `value`, tronqué aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="9b6be-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

<span data-ttu-id="9b6be-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="9b6be-150">**Arguments**</span></span>

|  |  |
|--|--|
|`value`|<span data-ttu-id="9b6be-151">`Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-151">`Double` or `Decimal`.</span></span>|
|`digits`|<span data-ttu-id="9b6be-152">`Int16` ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-152">`Int16` or `Int32`.</span></span>|

<span data-ttu-id="9b6be-153">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="9b6be-153">**Return Value**</span></span>

<span data-ttu-id="9b6be-154">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="9b6be-154">The type of `value`.</span></span>

<span data-ttu-id="9b6be-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9b6be-155">**Example**</span></span>

`Truncate(748.58,1)`  
  
 <span data-ttu-id="9b6be-156">Ces fonctions retournent `null` si une entrée de valeur `null` est fournie.</span><span class="sxs-lookup"><span data-stu-id="9b6be-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="9b6be-157">Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="9b6be-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="9b6be-158">Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9b6be-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b6be-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b6be-159">See also</span></span>

- [<span data-ttu-id="9b6be-160">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="9b6be-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
