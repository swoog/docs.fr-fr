---
title: Fonctions mathématiques canoniques
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: f575785bb198251ef50ba3563e736946253c9526
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59228768"
---
# <a name="math-canonical-functions"></a><span data-ttu-id="c8b84-102">Fonctions mathématiques canoniques</span><span class="sxs-lookup"><span data-stu-id="c8b84-102">Math Canonical Functions</span></span>

<span data-ttu-id="c8b84-103">Entity SQL inclut les fonctions canoniques mathématiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8b84-103">Entity SQL includes the following math canonical functions:</span></span>
  
## <a name="absvalue"></a><span data-ttu-id="c8b84-104">Abs(valeur)</span><span class="sxs-lookup"><span data-stu-id="c8b84-104">Abs(value)</span></span>

<span data-ttu-id="c8b84-105">Retourne la valeur absolue de `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-105">Returns the absolute value of `value`.</span></span>

**<span data-ttu-id="c8b84-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-106">Arguments</span></span>**

<span data-ttu-id="c8b84-107">Un `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-107">An `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, and `Decimal`.</span></span>

**<span data-ttu-id="c8b84-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-108">Return Value</span></span>**

<span data-ttu-id="c8b84-109">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-109">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-110">Example</span></span>**

`Abs(-2)`

## <a name="ceilingvalue"></a><span data-ttu-id="c8b84-111">Ceiling(valeur)</span><span class="sxs-lookup"><span data-stu-id="c8b84-111">Ceiling(value)</span></span>

<span data-ttu-id="c8b84-112">Retourne le plus petit entier qui n'est pas inférieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-112">Returns the smallest integer that is not less than `value`.</span></span>

**<span data-ttu-id="c8b84-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-113">Arguments</span></span>**

<span data-ttu-id="c8b84-114">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-114">A `Single`, `Double`, and `Decimal`.</span></span>

**<span data-ttu-id="c8b84-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-115">Return Value</span></span>**

<span data-ttu-id="c8b84-116">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-116">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-117">Example</span></span>**

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a><span data-ttu-id="c8b84-118">Floor(valeur)</span><span class="sxs-lookup"><span data-stu-id="c8b84-118">Floor(value)</span></span>

<span data-ttu-id="c8b84-119">Retourne le plus grand entier qui n'est pas supérieur à `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-119">Returns the largest integer that is not greater than `value`.</span></span>

**<span data-ttu-id="c8b84-120">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-120">Arguments</span></span>**

<span data-ttu-id="c8b84-121">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-121">A `Single`, `Double`, and `Decimal`.</span></span>

**<span data-ttu-id="c8b84-122">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-122">Return Value</span></span>**

<span data-ttu-id="c8b84-123">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-123">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-124">Example</span></span>**

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a><span data-ttu-id="c8b84-125">Power(valeur, exposant)</span><span class="sxs-lookup"><span data-stu-id="c8b84-125">Power(value, exponent)</span></span>

<span data-ttu-id="c8b84-126">Retourne le résultat de `value` à l'exposant `exponent` spécifié.</span><span class="sxs-lookup"><span data-stu-id="c8b84-126">Returns the result of the specified `value` to the specified `exponent`.</span></span>

**<span data-ttu-id="c8b84-127">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-127">Arguments</span></span>**

|  |  |
|--|--|
|`value` | <span data-ttu-id="c8b84-128">Un `Int32, Int64, Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-128">An `Int32, Int64, Double`, or `Decimal`.</span></span> |
|`exponent` | <span data-ttu-id="c8b84-129">Un `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-129">An `Int64`, `Double`, or `Decimal`.</span></span> |

**<span data-ttu-id="c8b84-130">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-130">Return Value</span></span>**

<span data-ttu-id="c8b84-131">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-131">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-132">Example</span></span>**

`Power(748.58,2)`

## <a name="roundvalue"></a><span data-ttu-id="c8b84-133">Round(valeur)</span><span class="sxs-lookup"><span data-stu-id="c8b84-133">Round(value)</span></span>

<span data-ttu-id="c8b84-134">Retourne la partie entière de `value`, arrondie à l'entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="c8b84-134">Returns the integer portion of `value`, rounded to the nearest integer.</span></span>

**<span data-ttu-id="c8b84-135">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-135">Arguments</span></span>**

<span data-ttu-id="c8b84-136">Un `Single`, `Double`, et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-136">A `Single`, `Double`, and `Decimal`.</span></span>

**<span data-ttu-id="c8b84-137">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-137">Return Value</span></span>**

<span data-ttu-id="c8b84-138">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-138">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-139">Example</span></span>**

`Round(748.58)`

## <a name="roundvalue-digits"></a><span data-ttu-id="c8b84-140">Round(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="c8b84-140">Round(value, digits)</span></span>

<span data-ttu-id="c8b84-141">Retourne `value`, arrondi aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="c8b84-141">Returns the `value`, rounded to the nearest specified `digits`.</span></span>

**<span data-ttu-id="c8b84-142">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-142">Arguments</span></span>**

|  |  |
|--|--|
|`value`|`Double` <span data-ttu-id="c8b84-143">ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-143">or `Decimal`.</span></span>|
|`digits`|`Int16` <span data-ttu-id="c8b84-144">ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-144">or `Int32`.</span></span>|

**<span data-ttu-id="c8b84-145">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-145">Return Value</span></span>**

<span data-ttu-id="c8b84-146">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-146">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-147">Example</span></span>**

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a><span data-ttu-id="c8b84-148">Truncate(valeur, chiffres)</span><span class="sxs-lookup"><span data-stu-id="c8b84-148">Truncate(value, digits)</span></span>

<span data-ttu-id="c8b84-149">Retourne `value`, tronqué aux `digits` spécifiés les plus proches.</span><span class="sxs-lookup"><span data-stu-id="c8b84-149">Returns the `value`, truncated to the nearest specified `digits`.</span></span>

**<span data-ttu-id="c8b84-150">Arguments</span><span class="sxs-lookup"><span data-stu-id="c8b84-150">Arguments</span></span>**

|  |  |
|--|--|
|`value`|`Double` <span data-ttu-id="c8b84-151">ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-151">or `Decimal`.</span></span>|
|`digits`|`Int16` <span data-ttu-id="c8b84-152">ou `Int32`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-152">or `Int32`.</span></span>|

**<span data-ttu-id="c8b84-153">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8b84-153">Return Value</span></span>**

<span data-ttu-id="c8b84-154">Type d'élément `value`.</span><span class="sxs-lookup"><span data-stu-id="c8b84-154">The type of `value`.</span></span>

**<span data-ttu-id="c8b84-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8b84-155">Example</span></span>**

`Truncate(748.58,1)`  
  
 <span data-ttu-id="c8b84-156">Ces fonctions retournent `null` si une entrée de valeur `null` est fournie.</span><span class="sxs-lookup"><span data-stu-id="c8b84-156">These functions will return `null` if given `null` input.</span></span>  
  
 <span data-ttu-id="c8b84-157">Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="c8b84-157">Equivalent functionality is available in the Microsoft SQL Client Managed Provider.</span></span> <span data-ttu-id="c8b84-158">Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c8b84-158">For more information, see [SqlClient for Entity Framework Functions](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8b84-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8b84-159">See also</span></span>

- [<span data-ttu-id="c8b84-160">Fonctions canoniques</span><span class="sxs-lookup"><span data-stu-id="c8b84-160">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
