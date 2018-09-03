---
title: Fonctions mathématiques
ms.date: 03/30/2017
ms.assetid: b040c7cb-156d-40f2-9152-61065b18148c
ms.openlocfilehash: e6c58d781d7138f8295f2d0a2f0db110ad4b1dd6
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43456449"
---
# <a name="mathematical-functions"></a><span data-ttu-id="f8e9f-102">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="f8e9f-102">Mathematical Functions</span></span>

<span data-ttu-id="f8e9f-103">Le fournisseur de données .NET Framework pour SQL Server (SqlClient) propose des fonctions mathématiques qui effectuent des calculs sur des valeurs d’entrée qui sont fournies comme arguments, et retournent une valeur numérique comme résultat.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-103">The .NET Framework Data Provider for SQL Server (SqlClient) provides math functions that perform calculations on input values that are provided as arguments, and return a numeric value result.</span></span> <span data-ttu-id="f8e9f-104">Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-104">These functions are in the SqlServer namespace, which is available when you use SqlClient.</span></span> <span data-ttu-id="f8e9f-105">La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions. Le tableau suivant décrit les fonctions mathématiques SqlClient.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-105">A provider's namespace property allows the Entity Framework to discover which prefix is used by this provider for specific constructs, such as types and functions.The following table describes the SqlClient math functions.</span></span>  
  
## <a name="absexpression"></a><span data-ttu-id="f8e9f-106">ABS(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-106">ABS(expression)</span></span>

<span data-ttu-id="f8e9f-107">Effectue la fonction de valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-107">Performs the absolute value function.</span></span>

<span data-ttu-id="f8e9f-108">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-108">**Arguments**</span></span>

<span data-ttu-id="f8e9f-109">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-109">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="f8e9f-110">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-110">**Return Value**</span></span>

<span data-ttu-id="f8e9f-111">Valeur absolue de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-111">The absolute value of the specified expression.</span></span>

<span data-ttu-id="f8e9f-112">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-112">**Example**</span></span>

`SqlServer.ABS(-2)`

## <a name="acosexpression"></a><span data-ttu-id="f8e9f-113">ACOS(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-113">ACOS(expression)</span></span>

<span data-ttu-id="f8e9f-114">Retourne la valeur d'arc cosinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-114">Returns the arccosine value of the specified expression.</span></span>

<span data-ttu-id="f8e9f-115">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-115">**Arguments**</span></span>

<span data-ttu-id="f8e9f-116">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-116">`expression`: A `Double`.</span></span>

<span data-ttu-id="f8e9f-117">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-117">**Return Value**</span></span>

<span data-ttu-id="f8e9f-118">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-118">A `Double`.</span></span>

<span data-ttu-id="f8e9f-119">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-119">**Example**</span></span>

`SqlServer.ACOS(.9)`

## <a name="asinexpression"></a><span data-ttu-id="f8e9f-120">ASIN(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-120">ASIN(expression)</span></span>

<span data-ttu-id="f8e9f-121">Retourne la valeur d'arcsinus de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-121">Returns the arcsine value of the specified expression.</span></span>

<span data-ttu-id="f8e9f-122">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-122">**Arguments**</span></span>

<span data-ttu-id="f8e9f-123">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-123">`expression`: A `Double`.</span></span>

<span data-ttu-id="f8e9f-124">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-124">**Return Value**</span></span>

<span data-ttu-id="f8e9f-125">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-125">A `Double`.</span></span>

<span data-ttu-id="f8e9f-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-126">**Example**</span></span>

`SqlServer.ASIN(.9)`

## <a name="atanexpression"></a><span data-ttu-id="f8e9f-127">ATAN(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-127">ATAN(expression)</span></span>

<span data-ttu-id="f8e9f-128">Retourne la valeur d'arctangente de l'expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-128">Returns the arctangent value of the specified numeric expression.</span></span>

<span data-ttu-id="f8e9f-129">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-129">**Arguments**</span></span>

<span data-ttu-id="f8e9f-130">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-130">`expression`: A `Double`.</span></span>

<span data-ttu-id="f8e9f-131">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-131">**Return Value**</span></span>

<span data-ttu-id="f8e9f-132">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-132">A `Double`.</span></span>

<span data-ttu-id="f8e9f-133">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-133">**Example**</span></span>

`SqlServer.ATAN(9)`

## <a name="atn2expression-expression"></a><span data-ttu-id="f8e9f-134">ATN2(expression, expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-134">ATN2(expression, expression)</span></span>

<span data-ttu-id="f8e9f-135">Retourne l'angle, en radians, dont la tangente est comprise entre les deux expressions numériques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-135">Returns the angle, in radians, whose tangent is between the two specified numeric expressions.</span></span>

<span data-ttu-id="f8e9f-136">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-136">**Arguments**</span></span>

<span data-ttu-id="f8e9f-137">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-137">`expression`: A `Double`.</span></span>

<span data-ttu-id="f8e9f-138">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-138">**Return Value**</span></span>

<span data-ttu-id="f8e9f-139">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-139">A `Double`.</span></span>

<span data-ttu-id="f8e9f-140">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-140">**Example**</span></span>

`SqlServer.ATN2(9, 8)`
 
## <a name="ceilingexpression"></a><span data-ttu-id="f8e9f-141">Ceiling(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-141">CEILING(expression)</span></span>

<span data-ttu-id="f8e9f-142">Convertit l'expression spécifiée en plus petit entier supérieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-142">Converts the specified expression to the smallest integer that is greater than or equal to it.</span></span>

<span data-ttu-id="f8e9f-143">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-143">**Arguments**</span></span>

<span data-ttu-id="f8e9f-144">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-144">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="f8e9f-145">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-145">**Return Value**</span></span>

<span data-ttu-id="f8e9f-146">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-146">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>

<span data-ttu-id="f8e9f-147">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-147">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_ceiling)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_ceiling)]

## <a name="cosexpression"></a><span data-ttu-id="f8e9f-148">COS(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-148">COS(expression)</span></span>

<span data-ttu-id="f8e9f-149">Calcule le cosinus trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-149">Calculates the trigonometric cosine of the specified angle in radians.</span></span> 

<span data-ttu-id="f8e9f-150">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-150">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-151">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-151">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-152">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-152">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-153">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-153">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-154">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-154">**Example**</span></span> 

`SqlServer.COS(45)`

## <a name="cotexpression"></a><span data-ttu-id="f8e9f-155">COT(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-155">COT(expression)</span></span>

<span data-ttu-id="f8e9f-156">Calcule la cotangente trigonométrique de l'angle spécifié, en radians.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-156">Calculates the trigonometric cotangent of the specified angle in radians.</span></span> 

<span data-ttu-id="f8e9f-157">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-157">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-158">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-158">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-159">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-159">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-160">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-160">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-161">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-161">**Example**</span></span> 

`SqlServer.COT(60)`
  
## <a name="degreesradians"></a><span data-ttu-id="f8e9f-162">DEGREES(radians)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-162">DEGREES(radians)</span></span>

<span data-ttu-id="f8e9f-163">Retourne l'angle correspondant, en degrés.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-163">Returns the corresponding angle in degrees.</span></span> 

<span data-ttu-id="f8e9f-164">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-164">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-165">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-165">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="f8e9f-166">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-166">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-167">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-167">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="f8e9f-168">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-168">**Example**</span></span> 

`SqlServer.DEGREES(3.1)`

## <a name="expexpression"></a><span data-ttu-id="f8e9f-169">EXP(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-169">EXP(expression)</span></span>

<span data-ttu-id="f8e9f-170">Calcule la valeur exponentielle d'une expression numérique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-170">Calculates the exponential value of a specified numeric expression.</span></span> 

<span data-ttu-id="f8e9f-171">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-171">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-172">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-172">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-173">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-173">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-174">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-174">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-175">**Exemple** `SqlServer.EXP(1)`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-175">**Example** `SqlServer.EXP(1)`</span></span>

## <a name="floorexpression"></a><span data-ttu-id="f8e9f-176">Floor(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-176">FLOOR(expression)</span></span>

<span data-ttu-id="f8e9f-177">Convertit l'expression spécifiée en plus grand entier inférieur ou égal à cette expression.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-177">Converts the specified expression to the largest integer less than or equal to it.</span></span> 

<span data-ttu-id="f8e9f-178">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-178">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-179">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-179">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-180">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-180">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-181">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-181">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-182">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-182">**Example**</span></span> 

[!code-csharp[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_floor)] 
[!code-sql[DP EntityServices Concepts#SQLSERVER_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_floor)]

## <a name="logexpression"></a><span data-ttu-id="f8e9f-183">LOG(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-183">LOG(expression)</span></span>

<span data-ttu-id="f8e9f-184">Calcule le logarithme népérien de l'expression `float` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-184">Calculates the natural logarithm of the specified `float` expression.</span></span> 

<span data-ttu-id="f8e9f-185">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-185">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-186">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-186">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-187">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-187">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-188">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-188">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-189">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-189">**Example**</span></span> 

`SqlServer.LOG(100)`

## <a name="log10expression"></a><span data-ttu-id="f8e9f-190">LOG10(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-190">LOG10(expression)</span></span>

<span data-ttu-id="f8e9f-191">Retourne le logarithme en base 10 de l'expression `Double` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-191">Returns the base-10 logarithm of the specified `Double` expression.</span></span> 

<span data-ttu-id="f8e9f-192">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-192">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-193">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-193">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-194">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-194">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-195">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-195">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-196">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-196">**Example**</span></span> 

`SqlServer.LOG10(100)`

## <a name="pi"></a><span data-ttu-id="f8e9f-197">PI)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-197">PI()</span></span>

<span data-ttu-id="f8e9f-198">Retourne la valeur constante de pi sous la forme d'une valeur `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-198">Returns the constant value of pi as a `Double`.</span></span> 

<span data-ttu-id="f8e9f-199">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-199">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-200">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-200">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-201">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-201">**Example**</span></span> 

`SqlServer.PI()`

## <a name="powernumericexpression-powerexpression"></a><span data-ttu-id="f8e9f-202">POWER (numeric_expression, power_expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-202">POWER(numeric_expression, power_expression)</span></span>

<span data-ttu-id="f8e9f-203">Calcule la valeur d'une expression donnée élevée à une puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-203">Calculates the value of a specified expression to a specified power.</span></span>

<span data-ttu-id="f8e9f-204">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-204">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="f8e9f-205">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-205">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span>|
|`power_expression`| <span data-ttu-id="f8e9f-206">Un `Double` qui représente la puissance à laquelle élever la `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-206">A `Double` that represents the power to which to raise the `numeric_expression`.</span></span>| 

<span data-ttu-id="f8e9f-207">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-207">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-208">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-208">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span> 

<span data-ttu-id="f8e9f-209">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-209">**Example**</span></span> 

`SqlServer.POWER(2,7)`

## <a name="radiansexpression"></a><span data-ttu-id="f8e9f-210">RADIANS(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-210">RADIANS(expression)</span></span>

<span data-ttu-id="f8e9f-211">Convertit les degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-211">Converts degrees to radians.</span></span> 

<span data-ttu-id="f8e9f-212">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-212">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-213">`expression` :`Int32`,`Int64`, `Double` ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-213">`expression`: An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="f8e9f-214">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-214">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-215">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-215">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="f8e9f-216">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-216">**Example**</span></span> 

`SqlServer.RADIANS(360.0)`

## <a name="randseed"></a><span data-ttu-id="f8e9f-217">RAND([SEED])</span><span class="sxs-lookup"><span data-stu-id="f8e9f-217">RAND([seed])</span></span>

<span data-ttu-id="f8e9f-218">Retourne une valeur aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-218">Returns a random value from 0 through 1.</span></span> 

<span data-ttu-id="f8e9f-219">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-219">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-220">La valeur de départ comme une `Int32`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-220">The seed value as an `Int32`.</span></span> <span data-ttu-id="f8e9f-221">Si la valeur initiale n'est pas spécifiée, le moteur de base de données SQL Server affecte une valeur initiale aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-221">If the seed is not specified, the SQL Server Database Engine assigns a seed value at random.</span></span> <span data-ttu-id="f8e9f-222">Pour une valeur initiale spécifiée, le résultat retourné est toujours le même.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-222">For a specified seed value, the result returned is always the same.</span></span>

<span data-ttu-id="f8e9f-223">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-223">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-224">Valeur `Double` aléatoire comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-224">A random `Double` value from 0 through 1.</span></span> 

<span data-ttu-id="f8e9f-225">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-225">**Example**</span></span> 

`SqlServer.RAND()`
  
## <a name="roundnumericexpression-lengthfunction"></a><span data-ttu-id="f8e9f-226">Round(numeric_expression, Length[,Function])</span><span class="sxs-lookup"><span data-stu-id="f8e9f-226">ROUND(numeric_expression, length[,function])</span></span>

<span data-ttu-id="f8e9f-227">Retourne une expression numérique, arrondie à la longueur ou à la précision spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-227">Returns a numeric expression, rounded to the specified length or precision.</span></span> 

<span data-ttu-id="f8e9f-228">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-228">**Arguments**</span></span> 

|  |  |
|--|--|
|`numeric_expression`| <span data-ttu-id="f8e9f-229">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-229">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 
|`length`| <span data-ttu-id="f8e9f-230">`Int32` qui représente la précision selon laquelle arrondir `numeric_expression`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-230">An `Int32` that represents the precision to which `numeric_expression` is to be rounded.</span></span> <span data-ttu-id="f8e9f-231">Lorsque `length` est un nombre positif, `numeric_expression` est arrondi au nombre de décimales indiqué par `length`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-231">When `length` is a positive number, `numeric_expression` is rounded to the number of decimal positions specified by `length`.</span></span> <span data-ttu-id="f8e9f-232">Lorsque `length` est un nombre négatif, `numeric_expression` est arrondi à gauche de la virgule décimale, selon l'indication fournie par `length`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-232">When `length` is a negative number, `numeric_expression` is rounded on the left side of the decimal point, as specified by `length`.</span></span>|
|`function` | <span data-ttu-id="f8e9f-233">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-233">Optional.</span></span> <span data-ttu-id="f8e9f-234">Un `Int32` qui représente le type d’opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-234">An `Int32` that represents the type of operation to perform.</span></span> <span data-ttu-id="f8e9f-235">Lorsque function est omise ou a la valeur 0 (valeur par défaut), `numeric_expression` est arrondi.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-235">When function is omitted or has a value of 0 (default), `numeric_expression` is rounded.</span></span> <span data-ttu-id="f8e9f-236">Lorsqu’une valeur autre que 0 est spécifiée, `numeric_expression` est tronqué.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-236">When a value other than 0 is specified, `numeric_expression` is truncated.</span></span> |

<span data-ttu-id="f8e9f-237">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-237">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-238">Valeur du paramètre `numeric_expression` donné élevé à la puissance `power_expression` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-238">The value of the specified `numeric_expression` to the specified `power_expression`.</span></span>

<span data-ttu-id="f8e9f-239">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-239">**Example**</span></span> 

`SqlServer.ROUND(748.58, -3)`

## <a name="signexpression"></a><span data-ttu-id="f8e9f-240">Sign(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-240">SIGN(expression)</span></span> 

<span data-ttu-id="f8e9f-241">Retourne le signe positif (+1), nul (0) ou négatif (-1) de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-241">Returns the positive (+1), zero (0), or negative (-1) sign of the specified expression.</span></span> 

<span data-ttu-id="f8e9f-242">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-242">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-243">`expression` : `Int32`, `Int64`, `Double` ou `Decimal`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-243">`expression`: `Int32`, `Int64`, `Double`, or `Decimal`</span></span> 

<span data-ttu-id="f8e9f-244">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-244">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-245">Un `Int32`, `Int64`, `Double`, ou `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-245">An `Int32`, `Int64`, `Double`, or `Decimal`.</span></span> 

<span data-ttu-id="f8e9f-246">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-246">**Example**</span></span> 

`SqlServer.SIGN(-10)`

## <a name="sinexpression"></a><span data-ttu-id="f8e9f-247">SIN(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-247">SIN(expression)</span></span>

<span data-ttu-id="f8e9f-248">Calcule le sinus trigonométrique de l'angle spécifié, en radians, et retourne une expression `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-248">Calculates the trigonometric sine of the specified angle in radians, and returns a `Double` expression.</span></span> 

<span data-ttu-id="f8e9f-249">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-249">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-250">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-250">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-251">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-251">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-252">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-252">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-253">**Exemple** `SqlServer.SIN(20)`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-253">**Example** `SqlServer.SIN(20)`</span></span>

## <a name="sqrtexpression"></a><span data-ttu-id="f8e9f-254">SQRT(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-254">SQRT(expression)</span></span>

<span data-ttu-id="f8e9f-255">Retourne la racine carrée de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-255">Returns the square root of the specified expression.</span></span> 

<span data-ttu-id="f8e9f-256">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-256">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-257">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-257">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-258">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-258">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-259">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-259">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-260">**Exemple** `SqlServer.SQRT(3600)`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-260">**Example** `SqlServer.SQRT(3600)`</span></span>

## <a name="squareexpression"></a><span data-ttu-id="f8e9f-261">Square(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-261">SQUARE(expression)</span></span>

<span data-ttu-id="f8e9f-262">Retourne le carré de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-262">Returns the square of the specified expression.</span></span> 

<span data-ttu-id="f8e9f-263">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-263">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-264">`expression` : `Double`.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-264">`expression`: A `Double`.</span></span> 

<span data-ttu-id="f8e9f-265">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-265">**Return Value**</span></span> 

<span data-ttu-id="f8e9f-266">`Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-266">A `Double`.</span></span> 

<span data-ttu-id="f8e9f-267">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-267">**Example**</span></span> 

`SqlServer.SQUARE(25)`

## <a name="tanexpression"></a><span data-ttu-id="f8e9f-268">TAN(expression)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-268">TAN(expression)</span></span>

<span data-ttu-id="f8e9f-269">Calcule la tangente d'une expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8e9f-269">Calculates the tangent of a specified expression.</span></span>

<span data-ttu-id="f8e9f-270">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-270">**Arguments**</span></span> 

<span data-ttu-id="f8e9f-271">`expression`: `Double`</span><span class="sxs-lookup"><span data-stu-id="f8e9f-271">`expression`: `Double`</span></span> 

<span data-ttu-id="f8e9f-272">**Valeur de retour**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-272">**Return Value**</span></span> 

`Double` 

<span data-ttu-id="f8e9f-273">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f8e9f-273">**Example**</span></span> 

`SqlServer.TAN(45.0)`
  
## <a name="see-also"></a><span data-ttu-id="f8e9f-274">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8e9f-274">See also</span></span>

<span data-ttu-id="f8e9f-275">Pour plus d'informations sur les fonctions mathématiques prises en charge par SqlClient, consultez la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :</span><span class="sxs-lookup"><span data-stu-id="f8e9f-275">For more information about the mathematical functions that SqlClient supports, see the documentation for the SQL Server version that you specified in the SqlClient provider manifest:</span></span>  
  
<span data-ttu-id="f8e9f-276">**SQL Server 2005 :** [fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span><span class="sxs-lookup"><span data-stu-id="f8e9f-276">**SQL Server 2005:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms177516(v=sql.90))</span></span>  
<span data-ttu-id="f8e9f-277">**SQL Server 2008 :** [fonctions mathématiques (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span><span class="sxs-lookup"><span data-stu-id="f8e9f-277">**SQL Server 2008:** [Mathematical Functions (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2008/ms177516(v=sql.100))</span></span>  
<span data-ttu-id="f8e9f-278">**SQL Server 2012 et versions ultérieur :** [fonctions mathématiques (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span><span class="sxs-lookup"><span data-stu-id="f8e9f-278">**SQL Server 2012 and later:** [Mathematical Functions (Transact-SQL)](/sql/t-sql/functions/mathematical-functions-transact-sql?view=sql-server-2017)</span></span>   

 [<span data-ttu-id="f8e9f-279">Fonctions SqlClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="f8e9f-279">SqlClient for Entity Framework Functions</span></span>](sqlclient-for-ef-functions.md)
