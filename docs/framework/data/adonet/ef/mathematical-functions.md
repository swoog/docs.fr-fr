---
title: Fonctions mathématiques
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: e6c58d781d7138f8295f2d0a2f0db110ad4b1dd6
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43560650"
---
# <a name="mathematical-functions"></a><span data-ttu-id="89344-102">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="89344-102">Mathematical Functions</span></span>

<span data-ttu-id="89344-103">Le fournisseur de données .NET Framework pour SQL Server (SqlClient) propose des fonctions mathématiques qui effectuent des calculs sur des valeurs d’entrée qui sont fournies comme arguments, et retournent une valeur numérique comme résultat.</span><span class="sxs-lookup"><span data-stu-id="89344-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="89344-104">Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient.</span><span class="sxs-lookup"><span data-stu-id="89344-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="89344-105">La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions. Le tableau suivant décrit les fonctions mathématiques SqlClient.</span><span class="sxs-lookup"><span data-stu-id="89344-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="89344-106">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-106">ABS(expression)</span></span>

<span data-ttu-id="89344-107">Effectue la fonction de valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="89344-107">Performs the absolute value function.</span></span>

<span data-ttu-id="89344-108">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-108">**Arguments**</span></span>

<span data-ttu-id="89344-109">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-109">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="89344-110">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-110">**Return Value**</span></span>

<span data-ttu-id="89344-111">Valeur absolue de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-111">The absolute value of the specified expression.</span></span>

<span data-ttu-id="89344-112">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-112">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="89344-113">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-113">ACOS(expression)</span></span>

<span data-ttu-id="89344-114">Retourne la valeur d'arc cosinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-114">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="89344-115">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-115">**Arguments**</span></span>

<span data-ttu-id="89344-116">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-116">`expression`: A `Double`.</span></span>

<span data-ttu-id="89344-117">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-117">**Return Value**</span></span>

<span data-ttu-id="89344-118">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-118">A `Double`.</span></span>

<span data-ttu-id="89344-119">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-119">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="89344-120">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-120">ASIN(expression)</span></span>

<span data-ttu-id="89344-121">Retourne la valeur d'arcsinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-121">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="89344-122">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-122">**Arguments**</span></span>

<span data-ttu-id="89344-123">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-123">`expression`: A `Double`.</span></span>

<span data-ttu-id="89344-124">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-124">**Return Value**</span></span>

<span data-ttu-id="89344-125">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-125">A `Double`.</span></span>

<span data-ttu-id="89344-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-126">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="89344-127">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-127">ATAN(expression)</span></span>

<span data-ttu-id="89344-128">Retourne la valeur d'arctangente de l'expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-128">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="89344-129">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-129">**Arguments**</span></span>

<span data-ttu-id="89344-130">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-130">`expression`: A `Double`.</span></span>

<span data-ttu-id="89344-131">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-131">**Return Value**</span></span>

<span data-ttu-id="89344-132">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-132">A `Double`.</span></span>

<span data-ttu-id="89344-133">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-133">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="89344-134">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="89344-134">ATN2(expression, expression)</span></span>

<span data-ttu-id="89344-135">Retourne l'angle, en radians, dont la tangente est comprise entre les deux expressions numériques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="89344-135">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="89344-136">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-136">**Arguments**</span></span>

<span data-ttu-id="89344-137">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-137">`expression`: A `Double`.</span></span>

<span data-ttu-id="89344-138">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-138">**Return Value**</span></span>

<span data-ttu-id="89344-139">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-139">A `Double`.</span></span>

<span data-ttu-id="89344-140">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-140">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="89344-141">Ceiling(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-141">CEILING(expression)</span></span>

<span data-ttu-id="89344-142">Convertit l'expression spécifiée en plus petit entier supérieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="89344-142">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="89344-143">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-143">**Arguments**</span></span>

<span data-ttu-id="89344-144">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-144">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="89344-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-145">**Return Value**</span></span>

<span data-ttu-id="89344-146">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-146">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="89344-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-147">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="89344-148">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-148">COS(expression)</span></span>

<span data-ttu-id="89344-149">Calcule le cosinus trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="89344-149">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="89344-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-150">**Arguments**</span></span> 

<span data-ttu-id="89344-151">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-151">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-152">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-152">**Return Value**</span></span> 

<span data-ttu-id="89344-153">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-153">A `Double`.</span></span> 

<span data-ttu-id="89344-154">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-154">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="89344-155">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-155">COT(expression)</span></span>

<span data-ttu-id="89344-156">Calcule la cotangente trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="89344-156">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="89344-157">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-157">**Arguments**</span></span> 

<span data-ttu-id="89344-158">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-158">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-159">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-159">**Return Value**</span></span> 

<span data-ttu-id="89344-160">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-160">A `Double`.</span></span> 

<span data-ttu-id="89344-161">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-161">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="89344-162">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="89344-162">DEGREES(radians)</span></span>

<span data-ttu-id="89344-163">Retourne l'angle correspondant, en degrés.</span><span class="sxs-lookup"><span data-stu-id="89344-163">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="89344-164">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-164">**Arguments**</span></span> 

<span data-ttu-id="89344-165">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-165">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="89344-166">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-166">**Return Value**</span></span> 

<span data-ttu-id="89344-167">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-167">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="89344-168">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-168">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="89344-169">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-169">EXP(expression)</span></span>

<span data-ttu-id="89344-170">Calcule la valeur exponentielle d'une expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-170">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="89344-171">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-171">**Arguments**</span></span> 

<span data-ttu-id="89344-172">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-172">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-173">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-173">**Return Value**</span></span> 

<span data-ttu-id="89344-174">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-174">A `Double`.</span></span> 

<span data-ttu-id="89344-175">**Exemple** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="89344-175">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="89344-176">Floor(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-176">FLOOR(expression)</span></span>

<span data-ttu-id="89344-177">Convertit l'expression spécifiée en plus grand entier inférieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="89344-177">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="89344-178">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-178">**Arguments**</span></span> 

<span data-ttu-id="89344-179">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-179">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-180">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-180">**Return Value**</span></span> 

<span data-ttu-id="89344-181">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-181">A `Double`.</span></span> 

<span data-ttu-id="89344-182">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-182">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="89344-183">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-183">LOG(expression)</span></span>

<span data-ttu-id="89344-184">Calcule le logarithme népérien de l'expression `float` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-184">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="89344-185">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-185">**Arguments**</span></span> 

<span data-ttu-id="89344-186">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-186">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-187">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-187">**Return Value**</span></span> 

<span data-ttu-id="89344-188">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-188">A `Double`.</span></span> 

<span data-ttu-id="89344-189">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-189">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="89344-190">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-190">LOG10(expression)</span></span>

<span data-ttu-id="89344-191">Retourne le logarithme en base 10 de l'expression `Double` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-191">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="89344-192">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-192">**Arguments**</span></span> 

<span data-ttu-id="89344-193">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-193">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-194">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-194">**Return Value**</span></span> 

<span data-ttu-id="89344-195">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-195">A `Double`.</span></span> 

<span data-ttu-id="89344-196">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-196">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="89344-197">PI)</span><span class="sxs-lookup"><span data-stu-id="89344-197">PI()</span></span>

<span data-ttu-id="89344-198">Retourne la valeur constante de pi sous la forme d'une valeur `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-198">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="89344-199">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-199">**Return Value**</span></span> 

<span data-ttu-id="89344-200">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-200">A `Double`.</span></span> 

<span data-ttu-id="89344-201">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-201">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="89344-202">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="89344-202">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="89344-203">Calcule la valeur d'une expression donnée élevée à une puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-203">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="89344-204">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-204">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="89344-205">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-205">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="89344-206">Un `Double` qui représente la puissance à laquelle élever la `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="89344-206">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="89344-207">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-207">**Return Value**</span></span> 

<span data-ttu-id="89344-208">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-208">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="89344-209">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-209">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="89344-210">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-210">RADIANS(expression)</span></span>

<span data-ttu-id="89344-211">Convertit les degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="89344-211">Converts degrees to radians.</span></span> 

<span data-ttu-id="89344-212">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-212">**Arguments**</span></span> 

<span data-ttu-id="89344-213">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-213">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="89344-214">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-214">**Return Value**</span></span> 

<span data-ttu-id="89344-215">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-215">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="89344-216">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-216">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="89344-217">RAND([SEED])</span><span class="sxs-lookup"><span data-stu-id="89344-217">RAND([seed])</span></span>

<span data-ttu-id="89344-218">Retourne une valeur aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="89344-218">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="89344-219">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-219">**Arguments**</span></span> 

<span data-ttu-id="89344-220">La valeur de départ comme une `Int32`.</span><span class="sxs-lookup"><span data-stu-id="89344-220">The seed value as an `Int32`.</span></span> <span data-ttu-id="89344-221">Si la valeur initiale n'est pas spécifiée, le moteur de base de données SQL Server affecte une valeur initiale aléatoire.</span><span class="sxs-lookup"><span data-stu-id="89344-221">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="89344-222">Pour une valeur initiale spécifiée, le résultat retourné est toujours le même.</span><span class="sxs-lookup"><span data-stu-id="89344-222">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="89344-223">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-223">**Return Value**</span></span> 

<span data-ttu-id="89344-224">Valeur `Double` aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="89344-224">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="89344-225">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-225">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="89344-226">Round(numeric_expression, Length[,Function])</span><span class="sxs-lookup"><span data-stu-id="89344-226">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="89344-227">Retourne une expression numérique, arrondie à la longueur ou à la précision spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-227">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="89344-228">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-228">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="89344-229">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-229">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="89344-230">`Int32` qui représente la précision selon laquelle arrondir `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="89344-230">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="89344-231">Lorsque `length` est un nombre positif, `numeric_expression` est arrondi au nombre de décimales indiqué par `length`.</span><span class="sxs-lookup"><span data-stu-id="89344-231">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="89344-232">Lorsque `length` est un nombre négatif, `numeric_expression` est arrondi à gauche de la virgule décimale, selon l'indication fournie par `length`.</span><span class="sxs-lookup"><span data-stu-id="89344-232">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="89344-233">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="89344-233">Optional.</span></span> <span data-ttu-id="89344-234">Un `Int32` qui représente le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="89344-234">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="89344-235">Lorsque function est omise ou a la valeur 0 (valeur par défaut), `numeric_expression` est arrondi.</span><span class="sxs-lookup"><span data-stu-id="89344-235">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="89344-236">Lorsqu’une valeur autre que 0 est spécifiée, `numeric_expression` est tronqué.</span><span class="sxs-lookup"><span data-stu-id="89344-236">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="89344-237">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-237">**Return Value**</span></span> 

<span data-ttu-id="89344-238">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-238">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="89344-239">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-239">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="89344-240">Sign(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-240">SIGN(expression)</span></span> 

<span data-ttu-id="89344-241">Retourne le signe positif (+1), nul (0) ou négatif (-1) de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-241">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="89344-242">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-242">**Arguments**</span></span> 

<span data-ttu-id="89344-243">`expression` : `Int32`, `Int64`, `Double` ou `Decimal`</span><span class="sxs-lookup"><span data-stu-id="89344-243">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="89344-244">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-244">**Return Value**</span></span> 

<span data-ttu-id="89344-245">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="89344-245">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="89344-246">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-246">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="89344-247">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-247">SIN(expression)</span></span>

<span data-ttu-id="89344-248">Calcule le sinus trigonométrique de l'angle spécifié, en radians, et retourne une expression `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-248">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="89344-249">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-249">**Arguments**</span></span> 

<span data-ttu-id="89344-250">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-250">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-251">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-251">**Return Value**</span></span> 

<span data-ttu-id="89344-252">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-252">A `Double`.</span></span> 

<span data-ttu-id="89344-253">**Exemple** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="89344-253">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="89344-254">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-254">SQRT(expression)</span></span>

<span data-ttu-id="89344-255">Retourne la racine carrée de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-255">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="89344-256">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-256">**Arguments**</span></span> 

<span data-ttu-id="89344-257">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-257">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-258">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-258">**Return Value**</span></span> 

<span data-ttu-id="89344-259">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-259">A `Double`.</span></span> 

<span data-ttu-id="89344-260">**Exemple** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="89344-260">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="89344-261">Square(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-261">SQUARE(expression)</span></span>

<span data-ttu-id="89344-262">Retourne le carré de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-262">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="89344-263">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-263">**Arguments**</span></span> 

<span data-ttu-id="89344-264">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="89344-264">`expression`: A `Double`.</span></span> 

<span data-ttu-id="89344-265">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-265">**Return Value**</span></span> 

<span data-ttu-id="89344-266">`Double`</span><span class="sxs-lookup"><span data-stu-id="89344-266">A `Double`.</span></span> 

<span data-ttu-id="89344-267">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-267">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="89344-268">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="89344-268">TAN(expression)</span></span>

<span data-ttu-id="89344-269">Calcule la tangente d'une expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="89344-269">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="89344-270">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="89344-270">**Arguments**</span></span> 

<span data-ttu-id="89344-271">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="89344-271">`expression`: `Double`</span></span> 

<span data-ttu-id="89344-272">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="89344-272">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="89344-273">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="89344-273">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="89344-274">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89344-274">See also</span></span>

<span data-ttu-id="89344-275">Pour plus d'informations sur les fonctions mathématiques prises en charge par SqlClient, consultez la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :</span><span class="sxs-lookup"><span data-stu-id="89344-275">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="89344-276">**SQL Server 2005 :** [fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="89344-276">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="89344-277">**SQL Server 2008 :** [fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="89344-277">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="89344-278">**SQL Server 2012 et versions ultérieur :** [fonctions mathématiques (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="89344-278">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="89344-279">Fonctions SqlClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="89344-279">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
