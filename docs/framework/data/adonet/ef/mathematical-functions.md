---
title: Fonctions mathématiques
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: d8d766cb1416a9a07476175364fe568d81fd9b25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652265"
---
# <a name="mathematical-functions"></a><span data-ttu-id="2b948-102">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="2b948-102">Mathematical Functions</span></span>

<span data-ttu-id="2b948-103">Le fournisseur de données .NET Framework pour SQL Server (SqlClient) propose des fonctions mathématiques qui effectuent des calculs sur des valeurs d’entrée qui sont fournies comme arguments, et retournent une valeur numérique comme résultat.</span><span class="sxs-lookup"><span data-stu-id="2b948-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="2b948-104">Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient.</span><span class="sxs-lookup"><span data-stu-id="2b948-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="2b948-105">La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions.</span><span class="sxs-lookup"><span data-stu-id="2b948-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.</span></span> <span data-ttu-id="2b948-106">Le tableau suivant décrit les fonctions mathématiques SqlClient.</span><span class="sxs-lookup"><span data-stu-id="2b948-106">The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="2b948-107">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-107">ABS(expression)</span></span>

<span data-ttu-id="2b948-108">Effectue la fonction de valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="2b948-108">Performs the absolute value function.</span></span>

<span data-ttu-id="2b948-109">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-109">**Arguments**</span></span>

<span data-ttu-id="2b948-110">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-110">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="2b948-111">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-111">**Return Value**</span></span>

<span data-ttu-id="2b948-112">Valeur absolue de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-112">The absolute value of the specified expression.</span></span>

<span data-ttu-id="2b948-113">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-113">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="2b948-114">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-114">ACOS(expression)</span></span>

<span data-ttu-id="2b948-115">Retourne la valeur d'arc cosinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-115">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="2b948-116">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-116">**Arguments**</span></span>

<span data-ttu-id="2b948-117">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-117">`expression`: A `Double`.</span></span>

<span data-ttu-id="2b948-118">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-118">**Return Value**</span></span>

<span data-ttu-id="2b948-119">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-119">A `Double`.</span></span>

<span data-ttu-id="2b948-120">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-120">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="2b948-121">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-121">ASIN(expression)</span></span>

<span data-ttu-id="2b948-122">Retourne la valeur d'arcsinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-122">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="2b948-123">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-123">**Arguments**</span></span>

<span data-ttu-id="2b948-124">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-124">`expression`: A `Double`.</span></span>

<span data-ttu-id="2b948-125">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-125">**Return Value**</span></span>

<span data-ttu-id="2b948-126">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-126">A `Double`.</span></span>

<span data-ttu-id="2b948-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-127">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="2b948-128">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-128">ATAN(expression)</span></span>

<span data-ttu-id="2b948-129">Retourne la valeur d'arctangente de l'expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-129">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="2b948-130">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-130">**Arguments**</span></span>

<span data-ttu-id="2b948-131">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-131">`expression`: A `Double`.</span></span>

<span data-ttu-id="2b948-132">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-132">**Return Value**</span></span>

<span data-ttu-id="2b948-133">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-133">A `Double`.</span></span>

<span data-ttu-id="2b948-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-134">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="2b948-135">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-135">ATN2(expression, expression)</span></span>

<span data-ttu-id="2b948-136">Retourne l'angle, en radians, dont la tangente est comprise entre les deux expressions numériques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2b948-136">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="2b948-137">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-137">**Arguments**</span></span>

<span data-ttu-id="2b948-138">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-138">`expression`: A `Double`.</span></span>

<span data-ttu-id="2b948-139">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-139">**Return Value**</span></span>

<span data-ttu-id="2b948-140">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-140">A `Double`.</span></span>

<span data-ttu-id="2b948-141">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-141">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="2b948-142">CEILING(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-142">CEILING(expression)</span></span>

<span data-ttu-id="2b948-143">Convertit l'expression spécifiée en plus petit entier supérieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="2b948-143">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="2b948-144">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-144">**Arguments**</span></span>

<span data-ttu-id="2b948-145">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-145">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="2b948-146">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-146">**Return Value**</span></span>

<span data-ttu-id="2b948-147">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-147">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="2b948-148">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-148">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="2b948-149">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-149">COS(expression)</span></span>

<span data-ttu-id="2b948-150">Calcule le cosinus trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="2b948-150">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="2b948-151">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-151">**Arguments**</span></span> 

<span data-ttu-id="2b948-152">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-152">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-153">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-153">**Return Value**</span></span> 

<span data-ttu-id="2b948-154">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-154">A `Double`.</span></span> 

<span data-ttu-id="2b948-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-155">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="2b948-156">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-156">COT(expression)</span></span>

<span data-ttu-id="2b948-157">Calcule la cotangente trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="2b948-157">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="2b948-158">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-158">**Arguments**</span></span> 

<span data-ttu-id="2b948-159">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-159">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-160">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-160">**Return Value**</span></span> 

<span data-ttu-id="2b948-161">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-161">A `Double`.</span></span> 

<span data-ttu-id="2b948-162">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-162">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="2b948-163">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="2b948-163">DEGREES(radians)</span></span>

<span data-ttu-id="2b948-164">Retourne l'angle correspondant, en degrés.</span><span class="sxs-lookup"><span data-stu-id="2b948-164">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="2b948-165">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-165">**Arguments**</span></span> 

<span data-ttu-id="2b948-166">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-166">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="2b948-167">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-167">**Return Value**</span></span> 

<span data-ttu-id="2b948-168">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-168">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="2b948-169">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-169">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="2b948-170">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-170">EXP(expression)</span></span>

<span data-ttu-id="2b948-171">Calcule la valeur exponentielle d'une expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-171">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="2b948-172">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-172">**Arguments**</span></span> 

<span data-ttu-id="2b948-173">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-173">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-174">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-174">**Return Value**</span></span> 

<span data-ttu-id="2b948-175">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-175">A `Double`.</span></span> 

<span data-ttu-id="2b948-176">**Exemple** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="2b948-176">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="2b948-177">FLOOR(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-177">FLOOR(expression)</span></span>

<span data-ttu-id="2b948-178">Convertit l'expression spécifiée en plus grand entier inférieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="2b948-178">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="2b948-179">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-179">**Arguments**</span></span> 

<span data-ttu-id="2b948-180">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-180">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-181">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-181">**Return Value**</span></span> 

<span data-ttu-id="2b948-182">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-182">A `Double`.</span></span> 

<span data-ttu-id="2b948-183">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-183">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="2b948-184">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-184">LOG(expression)</span></span>

<span data-ttu-id="2b948-185">Calcule le logarithme népérien de l'expression `float` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-185">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="2b948-186">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-186">**Arguments**</span></span> 

<span data-ttu-id="2b948-187">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-187">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-188">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-188">**Return Value**</span></span> 

<span data-ttu-id="2b948-189">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-189">A `Double`.</span></span> 

<span data-ttu-id="2b948-190">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-190">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="2b948-191">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-191">LOG10(expression)</span></span>

<span data-ttu-id="2b948-192">Retourne le logarithme en base 10 de l'expression `Double` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-192">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="2b948-193">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-193">**Arguments**</span></span> 

<span data-ttu-id="2b948-194">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-194">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-195">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-195">**Return Value**</span></span> 

<span data-ttu-id="2b948-196">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-196">A `Double`.</span></span> 

<span data-ttu-id="2b948-197">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-197">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="2b948-198">PI()</span><span class="sxs-lookup"><span data-stu-id="2b948-198">PI()</span></span>

<span data-ttu-id="2b948-199">Retourne la valeur constante de pi sous la forme d'une valeur `Double`.</span><span class="sxs-lookup"><span data-stu-id="2b948-199">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="2b948-200">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-200">**Return Value**</span></span> 

<span data-ttu-id="2b948-201">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-201">A `Double`.</span></span> 

<span data-ttu-id="2b948-202">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-202">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="2b948-203">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-203">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="2b948-204">Calcule la valeur d'une expression donnée élevée à une puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-204">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="2b948-205">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-205">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="2b948-206">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-206">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="2b948-207">Un `Double` qui représente la puissance à laquelle élever la `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="2b948-207">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="2b948-208">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-208">**Return Value**</span></span> 

<span data-ttu-id="2b948-209">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-209">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="2b948-210">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-210">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="2b948-211">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-211">RADIANS(expression)</span></span>

<span data-ttu-id="2b948-212">Convertit les degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="2b948-212">Converts degrees to radians.</span></span> 

<span data-ttu-id="2b948-213">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-213">**Arguments**</span></span> 

<span data-ttu-id="2b948-214">`expression`: Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-214">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="2b948-215">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-215">**Return Value**</span></span> 

<span data-ttu-id="2b948-216">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-216">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="2b948-217">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-217">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="2b948-218">RAND([SEED])</span><span class="sxs-lookup"><span data-stu-id="2b948-218">RAND([seed])</span></span>

<span data-ttu-id="2b948-219">Retourne une valeur aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="2b948-219">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="2b948-220">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-220">**Arguments**</span></span> 

<span data-ttu-id="2b948-221">La valeur de départ comme une `Int32`.</span><span class="sxs-lookup"><span data-stu-id="2b948-221">The seed value as an `Int32`.</span></span> <span data-ttu-id="2b948-222">Si la valeur initiale n'est pas spécifiée, le moteur de base de données SQL Server affecte une valeur initiale aléatoire.</span><span class="sxs-lookup"><span data-stu-id="2b948-222">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="2b948-223">Pour une valeur initiale spécifiée, le résultat retourné est toujours le même.</span><span class="sxs-lookup"><span data-stu-id="2b948-223">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="2b948-224">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-224">**Return Value**</span></span> 

<span data-ttu-id="2b948-225">Valeur `Double` aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="2b948-225">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="2b948-226">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-226">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="2b948-227">Round(numeric_expression, Length[,Function])</span><span class="sxs-lookup"><span data-stu-id="2b948-227">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="2b948-228">Retourne une expression numérique, arrondie à la longueur ou à la précision spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-228">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="2b948-229">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-229">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="2b948-230">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-230">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="2b948-231">`Int32` qui représente la précision selon laquelle arrondir `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="2b948-231">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="2b948-232">Lorsque `length` est un nombre positif, `numeric_expression` est arrondi au nombre de décimales indiqué par `length`.</span><span class="sxs-lookup"><span data-stu-id="2b948-232">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="2b948-233">Lorsque `length` est un nombre négatif, `numeric_expression` est arrondi à gauche de la virgule décimale, selon l'indication fournie par `length`.</span><span class="sxs-lookup"><span data-stu-id="2b948-233">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="2b948-234">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b948-234">Optional.</span></span> <span data-ttu-id="2b948-235">Un `Int32` qui représente le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2b948-235">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="2b948-236">Lorsque function est omise ou a la valeur 0 (valeur par défaut), `numeric_expression` est arrondi.</span><span class="sxs-lookup"><span data-stu-id="2b948-236">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="2b948-237">Lorsqu’une valeur autre que 0 est spécifiée, `numeric_expression` est tronqué.</span><span class="sxs-lookup"><span data-stu-id="2b948-237">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="2b948-238">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-238">**Return Value**</span></span> 

<span data-ttu-id="2b948-239">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-239">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="2b948-240">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-240">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="2b948-241">SIGN(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-241">SIGN(expression)</span></span> 

<span data-ttu-id="2b948-242">Retourne le signe positif (+1), nul (0) ou négatif (-1) de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-242">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="2b948-243">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-243">**Arguments**</span></span> 

<span data-ttu-id="2b948-244">`expression` : `Int32`, `Int64`, `Double` ou `Decimal`</span><span class="sxs-lookup"><span data-stu-id="2b948-244">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="2b948-245">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-245">**Return Value**</span></span> 

<span data-ttu-id="2b948-246">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="2b948-246">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="2b948-247">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-247">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="2b948-248">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-248">SIN(expression)</span></span>

<span data-ttu-id="2b948-249">Calcule le sinus trigonométrique de l'angle spécifié, en radians, et retourne une expression `Double`.</span><span class="sxs-lookup"><span data-stu-id="2b948-249">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="2b948-250">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-250">**Arguments**</span></span> 

<span data-ttu-id="2b948-251">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-251">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-252">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-252">**Return Value**</span></span> 

<span data-ttu-id="2b948-253">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-253">A `Double`.</span></span> 

<span data-ttu-id="2b948-254">**Exemple** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="2b948-254">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="2b948-255">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-255">SQRT(expression)</span></span>

<span data-ttu-id="2b948-256">Retourne la racine carrée de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-256">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="2b948-257">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-257">**Arguments**</span></span> 

<span data-ttu-id="2b948-258">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-258">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-259">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-259">**Return Value**</span></span> 

<span data-ttu-id="2b948-260">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-260">A `Double`.</span></span> 

<span data-ttu-id="2b948-261">**Exemple** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="2b948-261">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="2b948-262">Square(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-262">SQUARE(expression)</span></span>

<span data-ttu-id="2b948-263">Retourne le carré de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-263">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="2b948-264">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-264">**Arguments**</span></span> 

<span data-ttu-id="2b948-265">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-265">`expression`: A `Double`.</span></span> 

<span data-ttu-id="2b948-266">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-266">**Return Value**</span></span> 

<span data-ttu-id="2b948-267">`Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-267">A `Double`.</span></span> 

<span data-ttu-id="2b948-268">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-268">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="2b948-269">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="2b948-269">TAN(expression)</span></span>

<span data-ttu-id="2b948-270">Calcule la tangente d'une expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b948-270">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="2b948-271">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="2b948-271">**Arguments**</span></span> 

<span data-ttu-id="2b948-272">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="2b948-272">`expression`: `Double`</span></span> 

<span data-ttu-id="2b948-273">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="2b948-273">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="2b948-274">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2b948-274">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="2b948-275">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b948-275">See also</span></span>

<span data-ttu-id="2b948-276">Pour plus d'informations sur les fonctions mathématiques prises en charge par SqlClient, consultez la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :</span><span class="sxs-lookup"><span data-stu-id="2b948-276">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  

<span data-ttu-id="2b948-277">**SQL Server 2005 :** [Fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="2b948-277">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="2b948-278">**SQL Server 2008 :** [Fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="2b948-278">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="2b948-279">**SQL Server 2012 et versions ultérieur :** [Fonctions mathématiques (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="2b948-279">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

- [<span data-ttu-id="2b948-280">Fonctions SqlClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="2b948-280">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
