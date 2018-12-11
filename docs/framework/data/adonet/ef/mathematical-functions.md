---
title: Fonctions mathématiques
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: 63f83532c399f77e268913da3198327345b9c2ee
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143673"
---
# <a name="mathematical-functions"></a><span data-ttu-id="bcb24-102">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="bcb24-102">Mathematical Functions</span></span>

<span data-ttu-id="bcb24-103">Le fournisseur de données .NET Framework pour SQL Server (SqlClient) propose des fonctions mathématiques qui effectuent des calculs sur des valeurs d’entrée qui sont fournies comme arguments, et retournent une valeur numérique comme résultat.</span><span class="sxs-lookup"><span data-stu-id="bcb24-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="bcb24-104">Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient.</span><span class="sxs-lookup"><span data-stu-id="bcb24-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="bcb24-105">La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions.</span><span class="sxs-lookup"><span data-stu-id="bcb24-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="bcb24-106">Le tableau suivant décrit les fonctions mathématiques SqlClient.</span><span class="sxs-lookup"><span data-stu-id="bcb24-106">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="bcb24-107">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-107">ABS(expression)</span></span>

<span data-ttu-id="bcb24-108">Effectue la fonction de valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="bcb24-108">Performs the absolute value function.</span></span>

<span data-ttu-id="bcb24-109">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-109">**Arguments**</span></span>

<span data-ttu-id="bcb24-110">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-110">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="bcb24-111">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-111">**Return Value**</span></span>

<span data-ttu-id="bcb24-112">Valeur absolue de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-112">The absolute value of the specified expression.</span></span>

<span data-ttu-id="bcb24-113">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-113">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="bcb24-114">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-114">ACOS(expression)</span></span>

<span data-ttu-id="bcb24-115">Retourne la valeur d'arc cosinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-115">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="bcb24-116">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-116">**Arguments**</span></span>

<span data-ttu-id="bcb24-117">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-117">`expression`: A `Double`.</span></span>

<span data-ttu-id="bcb24-118">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-118">**Return Value**</span></span>

<span data-ttu-id="bcb24-119">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-119">A `Double`.</span></span>

<span data-ttu-id="bcb24-120">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-120">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="bcb24-121">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-121">ASIN(expression)</span></span>

<span data-ttu-id="bcb24-122">Retourne la valeur d'arcsinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-122">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="bcb24-123">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-123">**Arguments**</span></span>

<span data-ttu-id="bcb24-124">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-124">`expression`: A `Double`.</span></span>

<span data-ttu-id="bcb24-125">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-125">**Return Value**</span></span>

<span data-ttu-id="bcb24-126">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-126">A `Double`.</span></span>

<span data-ttu-id="bcb24-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-127">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="bcb24-128">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-128">ATAN(expression)</span></span>

<span data-ttu-id="bcb24-129">Retourne la valeur d'arctangente de l'expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-129">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="bcb24-130">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-130">**Arguments**</span></span>

<span data-ttu-id="bcb24-131">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-131">`expression`: A `Double`.</span></span>

<span data-ttu-id="bcb24-132">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-132">**Return Value**</span></span>

<span data-ttu-id="bcb24-133">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-133">A `Double`.</span></span>

<span data-ttu-id="bcb24-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-134">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="bcb24-135">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-135">ATN2(expression, expression)</span></span>

<span data-ttu-id="bcb24-136">Retourne l'angle, en radians, dont la tangente est comprise entre les deux expressions numériques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="bcb24-136">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="bcb24-137">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-137">**Arguments**</span></span>

<span data-ttu-id="bcb24-138">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-138">`expression`: A `Double`.</span></span>

<span data-ttu-id="bcb24-139">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-139">**Return Value**</span></span>

<span data-ttu-id="bcb24-140">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-140">A `Double`.</span></span>

<span data-ttu-id="bcb24-141">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-141">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="bcb24-142">Ceiling(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-142">CEILING(expression)</span></span>

<span data-ttu-id="bcb24-143">Convertit l'expression spécifiée en plus petit entier supérieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="bcb24-143">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="bcb24-144">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-144">**Arguments**</span></span>

<span data-ttu-id="bcb24-145">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-145">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="bcb24-146">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-146">**Return Value**</span></span>

<span data-ttu-id="bcb24-147">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-147">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="bcb24-148">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-148">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="bcb24-149">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-149">COS(expression)</span></span>

<span data-ttu-id="bcb24-150">Calcule le cosinus trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="bcb24-150">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="bcb24-151">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-151">**Arguments**</span></span> 

<span data-ttu-id="bcb24-152">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-152">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-153">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-153">**Return Value**</span></span> 

<span data-ttu-id="bcb24-154">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-154">A `Double`.</span></span> 

<span data-ttu-id="bcb24-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-155">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="bcb24-156">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-156">COT(expression)</span></span>

<span data-ttu-id="bcb24-157">Calcule la cotangente trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="bcb24-157">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="bcb24-158">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-158">**Arguments**</span></span> 

<span data-ttu-id="bcb24-159">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-159">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-160">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-160">**Return Value**</span></span> 

<span data-ttu-id="bcb24-161">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-161">A `Double`.</span></span> 

<span data-ttu-id="bcb24-162">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-162">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="bcb24-163">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="bcb24-163">DEGREES(radians)</span></span>

<span data-ttu-id="bcb24-164">Retourne l'angle correspondant, en degrés.</span><span class="sxs-lookup"><span data-stu-id="bcb24-164">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="bcb24-165">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-165">**Arguments**</span></span> 

<span data-ttu-id="bcb24-166">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-166">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="bcb24-167">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-167">**Return Value**</span></span> 

<span data-ttu-id="bcb24-168">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-168">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="bcb24-169">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-169">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="bcb24-170">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-170">EXP(expression)</span></span>

<span data-ttu-id="bcb24-171">Calcule la valeur exponentielle d'une expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-171">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="bcb24-172">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-172">**Arguments**</span></span> 

<span data-ttu-id="bcb24-173">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-173">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-174">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-174">**Return Value**</span></span> 

<span data-ttu-id="bcb24-175">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-175">A `Double`.</span></span> 

<span data-ttu-id="bcb24-176">**Exemple** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="bcb24-176">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="bcb24-177">Floor(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-177">FLOOR(expression)</span></span>

<span data-ttu-id="bcb24-178">Convertit l'expression spécifiée en plus grand entier inférieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="bcb24-178">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="bcb24-179">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-179">**Arguments**</span></span> 

<span data-ttu-id="bcb24-180">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-180">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-181">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-181">**Return Value**</span></span> 

<span data-ttu-id="bcb24-182">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-182">A `Double`.</span></span> 

<span data-ttu-id="bcb24-183">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-183">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="bcb24-184">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-184">LOG(expression)</span></span>

<span data-ttu-id="bcb24-185">Calcule le logarithme népérien de l'expression `float` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-185">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="bcb24-186">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-186">**Arguments**</span></span> 

<span data-ttu-id="bcb24-187">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-187">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-188">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-188">**Return Value**</span></span> 

<span data-ttu-id="bcb24-189">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-189">A `Double`.</span></span> 

<span data-ttu-id="bcb24-190">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-190">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="bcb24-191">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-191">LOG10(expression)</span></span>

<span data-ttu-id="bcb24-192">Retourne le logarithme en base 10 de l'expression `Double` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-192">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="bcb24-193">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-193">**Arguments**</span></span> 

<span data-ttu-id="bcb24-194">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-194">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-195">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-195">**Return Value**</span></span> 

<span data-ttu-id="bcb24-196">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-196">A `Double`.</span></span> 

<span data-ttu-id="bcb24-197">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-197">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="bcb24-198">PI)</span><span class="sxs-lookup"><span data-stu-id="bcb24-198">PI()</span></span>

<span data-ttu-id="bcb24-199">Retourne la valeur constante de pi sous la forme d'une valeur `Double`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-199">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="bcb24-200">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-200">**Return Value**</span></span> 

<span data-ttu-id="bcb24-201">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-201">A `Double`.</span></span> 

<span data-ttu-id="bcb24-202">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-202">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="bcb24-203">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-203">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="bcb24-204">Calcule la valeur d'une expression donnée élevée à une puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-204">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="bcb24-205">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-205">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="bcb24-206">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-206">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="bcb24-207">Un `Double` qui représente la puissance à laquelle élever la `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-207">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="bcb24-208">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-208">**Return Value**</span></span> 

<span data-ttu-id="bcb24-209">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-209">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="bcb24-210">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-210">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="bcb24-211">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-211">RADIANS(expression)</span></span>

<span data-ttu-id="bcb24-212">Convertit les degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="bcb24-212">Converts degrees to radians.</span></span> 

<span data-ttu-id="bcb24-213">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-213">**Arguments**</span></span> 

<span data-ttu-id="bcb24-214">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-214">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="bcb24-215">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-215">**Return Value**</span></span> 

<span data-ttu-id="bcb24-216">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-216">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="bcb24-217">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-217">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="bcb24-218">RAND([SEED])</span><span class="sxs-lookup"><span data-stu-id="bcb24-218">RAND([seed])</span></span>

<span data-ttu-id="bcb24-219">Retourne une valeur aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="bcb24-219">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="bcb24-220">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-220">**Arguments**</span></span> 

<span data-ttu-id="bcb24-221">La valeur de départ comme une `Int32`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-221">The seed value as an `Int32`.</span></span> <span data-ttu-id="bcb24-222">Si la valeur initiale n'est pas spécifiée, le moteur de base de données SQL Server affecte une valeur initiale aléatoire.</span><span class="sxs-lookup"><span data-stu-id="bcb24-222">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="bcb24-223">Pour une valeur initiale spécifiée, le résultat retourné est toujours le même.</span><span class="sxs-lookup"><span data-stu-id="bcb24-223">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="bcb24-224">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-224">**Return Value**</span></span> 

<span data-ttu-id="bcb24-225">Valeur `Double` aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="bcb24-225">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="bcb24-226">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-226">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="bcb24-227">Round(numeric_expression, Length[,Function])</span><span class="sxs-lookup"><span data-stu-id="bcb24-227">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="bcb24-228">Retourne une expression numérique, arrondie à la longueur ou à la précision spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-228">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="bcb24-229">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-229">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="bcb24-230">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-230">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="bcb24-231">`Int32` qui représente la précision selon laquelle arrondir `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-231">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="bcb24-232">Lorsque `length` est un nombre positif, `numeric_expression` est arrondi au nombre de décimales indiqué par `length`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-232">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="bcb24-233">Lorsque `length` est un nombre négatif, `numeric_expression` est arrondi à gauche de la virgule décimale, selon l'indication fournie par `length`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-233">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="bcb24-234">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="bcb24-234">Optional.</span></span> <span data-ttu-id="bcb24-235">Un `Int32` qui représente le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="bcb24-235">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="bcb24-236">Lorsque function est omise ou a la valeur 0 (valeur par défaut), `numeric_expression` est arrondi.</span><span class="sxs-lookup"><span data-stu-id="bcb24-236">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="bcb24-237">Lorsqu’une valeur autre que 0 est spécifiée, `numeric_expression` est tronqué.</span><span class="sxs-lookup"><span data-stu-id="bcb24-237">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="bcb24-238">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-238">**Return Value**</span></span> 

<span data-ttu-id="bcb24-239">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-239">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="bcb24-240">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-240">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="bcb24-241">Sign(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-241">SIGN(expression)</span></span> 

<span data-ttu-id="bcb24-242">Retourne le signe positif (+1), nul (0) ou négatif (-1) de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-242">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="bcb24-243">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-243">**Arguments**</span></span> 

<span data-ttu-id="bcb24-244">`expression` : `Int32`, `Int64`, `Double` ou `Decimal`</span><span class="sxs-lookup"><span data-stu-id="bcb24-244">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="bcb24-245">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-245">**Return Value**</span></span> 

<span data-ttu-id="bcb24-246">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-246">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="bcb24-247">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-247">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="bcb24-248">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-248">SIN(expression)</span></span>

<span data-ttu-id="bcb24-249">Calcule le sinus trigonométrique de l'angle spécifié, en radians, et retourne une expression `Double`.</span><span class="sxs-lookup"><span data-stu-id="bcb24-249">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="bcb24-250">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-250">**Arguments**</span></span> 

<span data-ttu-id="bcb24-251">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-251">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-252">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-252">**Return Value**</span></span> 

<span data-ttu-id="bcb24-253">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-253">A `Double`.</span></span> 

<span data-ttu-id="bcb24-254">**Exemple** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="bcb24-254">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="bcb24-255">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-255">SQRT(expression)</span></span>

<span data-ttu-id="bcb24-256">Retourne la racine carrée de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-256">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="bcb24-257">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-257">**Arguments**</span></span> 

<span data-ttu-id="bcb24-258">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-258">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-259">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-259">**Return Value**</span></span> 

<span data-ttu-id="bcb24-260">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-260">A `Double`.</span></span> 

<span data-ttu-id="bcb24-261">**Exemple** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="bcb24-261">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="bcb24-262">Square(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-262">SQUARE(expression)</span></span>

<span data-ttu-id="bcb24-263">Retourne le carré de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-263">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="bcb24-264">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-264">**Arguments**</span></span> 

<span data-ttu-id="bcb24-265">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-265">`expression`: A `Double`.</span></span> 

<span data-ttu-id="bcb24-266">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-266">**Return Value**</span></span> 

<span data-ttu-id="bcb24-267">`Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-267">A `Double`.</span></span> 

<span data-ttu-id="bcb24-268">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-268">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="bcb24-269">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="bcb24-269">TAN(expression)</span></span>

<span data-ttu-id="bcb24-270">Calcule la tangente d'une expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcb24-270">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="bcb24-271">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="bcb24-271">**Arguments**</span></span> 

<span data-ttu-id="bcb24-272">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="bcb24-272">`expression`: `Double`</span></span> 

<span data-ttu-id="bcb24-273">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="bcb24-273">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="bcb24-274">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bcb24-274">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="bcb24-275">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcb24-275">See also</span></span>

<span data-ttu-id="bcb24-276">Pour plus d'informations sur les fonctions mathématiques prises en charge par SqlClient, consultez la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :</span><span class="sxs-lookup"><span data-stu-id="bcb24-276">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="bcb24-277">**SQL Server 2005 :** [Fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="bcb24-277">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="bcb24-278">**SQL Server 2008 :** [Fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="bcb24-278">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="bcb24-279">**SQL Server 2012 et versions ultérieur :** [Fonctions mathématiques (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="bcb24-279">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="bcb24-280">Fonctions SqlClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="bcb24-280">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
