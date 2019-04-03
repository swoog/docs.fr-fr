---
title: Operator, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.operator
helpviewer_keywords:
- operators [Visual Basic]
- procedures [Visual Basic], operator
- Narrowing keyword [Visual Basic], conversion operators
- Visual Basic code, operators
- Widening keyword [Visual Basic], conversion operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- overloaded operators [Visual Basic]
- operator overloading
- operator procedures
- Operator statement [Visual Basic]
- CType function [Visual Basic], Operator statement
ms.assetid: b12ec4af-1ad7-4a17-865b-c5ee96320ae5
ms.openlocfilehash: 184970d33aae4af135153f9d6f6755770bdf84f6
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818590"
---
# <a name="operator-statement"></a><span data-ttu-id="93fce-102">Operator Statement</span><span class="sxs-lookup"><span data-stu-id="93fce-102">Operator Statement</span></span>
<span data-ttu-id="93fce-103">Déclare le symbole d’opérateur, opérandes et le code qui définissent une procédure d’opérateur sur une classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="93fce-103">Declares the operator symbol, operands, and code that define an operator procedure on a class or structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93fce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93fce-104">Syntax</span></span>  
  
```  
[ <attrlist> ] Public [ Overloads ] Shared [ Shadows ] [ Widening | Narrowing ]   
Operator operatorsymbol ( operand1 [, operand2 ]) [ As [ <attrlist> ] type ]  
    [ statements ]  
    [ statements ]  
    Return returnvalue  
    [ statements ]  
End Operator  
```  
  
## <a name="parts"></a><span data-ttu-id="93fce-105">Composants</span><span class="sxs-lookup"><span data-stu-id="93fce-105">Parts</span></span>  
 `attrlist`  
 <span data-ttu-id="93fce-106">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="93fce-106">Optional.</span></span> <span data-ttu-id="93fce-107">Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-107">See [Attribute List](../../../visual-basic/language-reference/statements/attribute-list.md).</span></span>  
  
 `Public`  
 <span data-ttu-id="93fce-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-108">Required.</span></span> <span data-ttu-id="93fce-109">Indique que cette procédure d’opérateur a [Public](../../../visual-basic/language-reference/modifiers/public.md) accès.</span><span class="sxs-lookup"><span data-stu-id="93fce-109">Indicates that this operator procedure has [Public](../../../visual-basic/language-reference/modifiers/public.md) access.</span></span>  
  
 `Overloads`  
 <span data-ttu-id="93fce-110">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="93fce-110">Optional.</span></span> <span data-ttu-id="93fce-111">Consultez [surcharges](../../../visual-basic/language-reference/modifiers/overloads.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-111">See [Overloads](../../../visual-basic/language-reference/modifiers/overloads.md).</span></span>  
  
 `Shared`  
 <span data-ttu-id="93fce-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-112">Required.</span></span> <span data-ttu-id="93fce-113">Indique que cette procédure d’opérateur est un [partagé](../../../visual-basic/language-reference/modifiers/shared.md) procédure.</span><span class="sxs-lookup"><span data-stu-id="93fce-113">Indicates that this operator procedure is a [Shared](../../../visual-basic/language-reference/modifiers/shared.md) procedure.</span></span>  
  
 `Shadows`  
 <span data-ttu-id="93fce-114">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="93fce-114">Optional.</span></span> <span data-ttu-id="93fce-115">Consultez [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-115">See [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span></span>  
  
 `Widening`  
 <span data-ttu-id="93fce-116">Obligatoire pour un opérateur de conversion, sauf si vous spécifiez `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="93fce-116">Required for a conversion operator unless you specify `Narrowing`.</span></span> <span data-ttu-id="93fce-117">Indique que cette procédure d’opérateur définit un [Widening](../../../visual-basic/language-reference/modifiers/widening.md) conversion.</span><span class="sxs-lookup"><span data-stu-id="93fce-117">Indicates that this operator procedure defines a [Widening](../../../visual-basic/language-reference/modifiers/widening.md) conversion.</span></span> <span data-ttu-id="93fce-118">Consultez « Conversions étendues et restrictives » sur cette page d’aide.</span><span class="sxs-lookup"><span data-stu-id="93fce-118">See "Widening and Narrowing Conversions" on this Help page.</span></span>  
  
 `Narrowing`  
 <span data-ttu-id="93fce-119">Obligatoire pour un opérateur de conversion, sauf si vous spécifiez `Widening`.</span><span class="sxs-lookup"><span data-stu-id="93fce-119">Required for a conversion operator unless you specify `Widening`.</span></span> <span data-ttu-id="93fce-120">Indique que cette procédure d’opérateur définit un [Narrowing](../../../visual-basic/language-reference/modifiers/narrowing.md) conversion.</span><span class="sxs-lookup"><span data-stu-id="93fce-120">Indicates that this operator procedure defines a [Narrowing](../../../visual-basic/language-reference/modifiers/narrowing.md) conversion.</span></span> <span data-ttu-id="93fce-121">Consultez « Conversions étendues et restrictives » sur cette page d’aide.</span><span class="sxs-lookup"><span data-stu-id="93fce-121">See "Widening and Narrowing Conversions" on this Help page.</span></span>  
  
 `operatorsymbol`  
 <span data-ttu-id="93fce-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-122">Required.</span></span> <span data-ttu-id="93fce-123">Le symbole ou l’identificateur de l’opérateur qui définit cette procédure d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="93fce-123">The symbol or identifier of the operator that this operator procedure defines.</span></span>  
  
 `operand1`  
 <span data-ttu-id="93fce-124">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-124">Required.</span></span> <span data-ttu-id="93fce-125">Le nom et le type de l’opérande unique d’un opérateur unaire (y compris un opérateur de conversion) ou de l’opérande gauche d’un opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="93fce-125">The name and type of the single operand of a unary operator (including a conversion operator) or the left operand of a binary operator.</span></span>  
  
 `operand2`  
 <span data-ttu-id="93fce-126">Requis pour les opérateurs binaires.</span><span class="sxs-lookup"><span data-stu-id="93fce-126">Required for binary operators.</span></span> <span data-ttu-id="93fce-127">Le nom et le type de l’opérande de droite d’un opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="93fce-127">The name and type of the right operand of a binary operator.</span></span>  
  
 <span data-ttu-id="93fce-128">`operand1` et `operand2` ont la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="93fce-128">`operand1` and `operand2` have the following syntax and parts:</span></span>  
  
 `[ ByVal ] operandname [ As operandtype ]`  
  
|<span data-ttu-id="93fce-129">Élément</span><span class="sxs-lookup"><span data-stu-id="93fce-129">Part</span></span>|<span data-ttu-id="93fce-130">Description</span><span class="sxs-lookup"><span data-stu-id="93fce-130">Description</span></span>|  
|----------|-----------------|  
|`ByVal`|<span data-ttu-id="93fce-131">Facultatif, mais le mécanisme de passage doit être [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-131">Optional, but the passing mechanism must be [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).</span></span>|  
|`operandname`|<span data-ttu-id="93fce-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-132">Required.</span></span> <span data-ttu-id="93fce-133">Nom de la variable représentant cet opérande.</span><span class="sxs-lookup"><span data-stu-id="93fce-133">Name of the variable representing this operand.</span></span> <span data-ttu-id="93fce-134">Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-134">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>|  
|`operandtype`|<span data-ttu-id="93fce-135">Facultatif, sauf si `Option Strict` est `On`.</span><span class="sxs-lookup"><span data-stu-id="93fce-135">Optional unless `Option Strict` is `On`.</span></span> <span data-ttu-id="93fce-136">Type de données de cet opérande.</span><span class="sxs-lookup"><span data-stu-id="93fce-136">Data type of this operand.</span></span>|  
  
 `type`  
 <span data-ttu-id="93fce-137">Facultatif, sauf si `Option Strict` est `On`.</span><span class="sxs-lookup"><span data-stu-id="93fce-137">Optional unless `Option Strict` is `On`.</span></span> <span data-ttu-id="93fce-138">Type de données de la valeur de la procédure d’opérateur retourne.</span><span class="sxs-lookup"><span data-stu-id="93fce-138">Data type of the value the operator procedure returns.</span></span>  
  
 `statements`  
 <span data-ttu-id="93fce-139">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="93fce-139">Optional.</span></span> <span data-ttu-id="93fce-140">Bloc d’instructions qui s’exécute la procédure d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="93fce-140">Block of statements that the operator procedure runs.</span></span>  
  
 `returnvalue`  
 <span data-ttu-id="93fce-141">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-141">Required.</span></span> <span data-ttu-id="93fce-142">La valeur que la procédure d’opérateur retourne au code appelant.</span><span class="sxs-lookup"><span data-stu-id="93fce-142">The value that the operator procedure returns to the calling code.</span></span>  
  
 <span data-ttu-id="93fce-143">`End` `Operator`</span><span class="sxs-lookup"><span data-stu-id="93fce-143">`End` `Operator`</span></span>  
 <span data-ttu-id="93fce-144">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="93fce-144">Required.</span></span> <span data-ttu-id="93fce-145">Met fin à la définition de cette procédure d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="93fce-145">Terminates the definition of this operator procedure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="93fce-146">Notes</span><span class="sxs-lookup"><span data-stu-id="93fce-146">Remarks</span></span>  
 <span data-ttu-id="93fce-147">Vous pouvez utiliser `Operator` uniquement dans une classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="93fce-147">You can use `Operator` only in a class or structure.</span></span> <span data-ttu-id="93fce-148">Cela signifie que le *contexte de déclaration* pour un opérateur ne peut pas être un fichier source, espace de noms, module, interface, procédure ou bloc.</span><span class="sxs-lookup"><span data-stu-id="93fce-148">This means the *declaration context* for an operator cannot be a source file, namespace, module, interface, procedure, or block.</span></span> <span data-ttu-id="93fce-149">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-149">For more information, see [Declaration Contexts and Default Access Levels](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="93fce-150">Tous les opérateurs doivent être `Public Shared`.</span><span class="sxs-lookup"><span data-stu-id="93fce-150">All operators must be `Public Shared`.</span></span> <span data-ttu-id="93fce-151">Vous ne pouvez pas spécifier `ByRef`, `Optional`, ou `ParamArray` pour des opérandes.</span><span class="sxs-lookup"><span data-stu-id="93fce-151">You cannot specify `ByRef`, `Optional`, or `ParamArray` for either operand.</span></span>  
  
 <span data-ttu-id="93fce-152">Vous ne pouvez pas utiliser le symbole d’opérateur ou l’identificateur pour contenir une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="93fce-152">You cannot use the operator symbol or identifier to hold a return value.</span></span> <span data-ttu-id="93fce-153">Vous devez utiliser le `Return` instruction et elle doit spécifier une valeur.</span><span class="sxs-lookup"><span data-stu-id="93fce-153">You must use the `Return` statement, and it must specify a value.</span></span> <span data-ttu-id="93fce-154">Un nombre quelconque de `Return` instructions peuvent apparaître n’importe où dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="93fce-154">Any number of `Return` statements can appear anywhere in the procedure.</span></span>  
  
 <span data-ttu-id="93fce-155">Définition d’un opérateur de cette façon est appelée *surcharge d’opérateur*, que vous utilisiez ou non le `Overloads` mot clé.</span><span class="sxs-lookup"><span data-stu-id="93fce-155">Defining an operator in this way is called *operator overloading*, whether or not you use the `Overloads` keyword.</span></span> <span data-ttu-id="93fce-156">Le tableau suivant présente les opérateurs que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="93fce-156">The following table lists the operators you can define.</span></span>  
  
|<span data-ttu-id="93fce-157">Type</span><span class="sxs-lookup"><span data-stu-id="93fce-157">Type</span></span>|<span data-ttu-id="93fce-158">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="93fce-158">Operators</span></span>|  
|----------|---------------|  
|<span data-ttu-id="93fce-159">Unaire</span><span class="sxs-lookup"><span data-stu-id="93fce-159">Unary</span></span>|<span data-ttu-id="93fce-160">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span><span class="sxs-lookup"><span data-stu-id="93fce-160">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span></span>|  
|<span data-ttu-id="93fce-161">Binaire</span><span class="sxs-lookup"><span data-stu-id="93fce-161">Binary</span></span>|<span data-ttu-id="93fce-162">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span><span class="sxs-lookup"><span data-stu-id="93fce-162">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span></span>|  
|<span data-ttu-id="93fce-163">Conversion (unaire)</span><span class="sxs-lookup"><span data-stu-id="93fce-163">Conversion (unary)</span></span>|`CType`|  
  
 <span data-ttu-id="93fce-164">Notez que le `=` opérateur dans la liste binaire est l’opérateur de comparaison, pas l’opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="93fce-164">Note that the `=` operator in the binary list is the comparison operator, not the assignment operator.</span></span>  
  
 <span data-ttu-id="93fce-165">Lorsque vous définissez `CType`, vous devez spécifier soit `Widening` ou `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="93fce-165">When you define `CType`, you must specify either `Widening` or `Narrowing`.</span></span>  
  
## <a name="matched-pairs"></a><span data-ttu-id="93fce-166">Paires correspondantes</span><span class="sxs-lookup"><span data-stu-id="93fce-166">Matched Pairs</span></span>  
 <span data-ttu-id="93fce-167">Vous devez définir certains opérateurs comme des paires correspondantes.</span><span class="sxs-lookup"><span data-stu-id="93fce-167">You must define certain operators as matched pairs.</span></span> <span data-ttu-id="93fce-168">Si vous définissez des opérateurs de cette paire, vous devez définir l’autre.</span><span class="sxs-lookup"><span data-stu-id="93fce-168">If you define either operator of such a pair, you must define the other as well.</span></span> <span data-ttu-id="93fce-169">Les paires correspondantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="93fce-169">The matched pairs are the following:</span></span>  
  
-   <span data-ttu-id="93fce-170">`=` et `<>`</span><span class="sxs-lookup"><span data-stu-id="93fce-170">`=` and `<>`</span></span>  
  
-   <span data-ttu-id="93fce-171">`>` et `<`</span><span class="sxs-lookup"><span data-stu-id="93fce-171">`>` and `<`</span></span>  
  
-   <span data-ttu-id="93fce-172">`>=` et `<=`</span><span class="sxs-lookup"><span data-stu-id="93fce-172">`>=` and `<=`</span></span>  
  
-   <span data-ttu-id="93fce-173">`IsTrue` et `IsFalse`</span><span class="sxs-lookup"><span data-stu-id="93fce-173">`IsTrue` and `IsFalse`</span></span>  
  
## <a name="data-type-restrictions"></a><span data-ttu-id="93fce-174">Restrictions de Type de données</span><span class="sxs-lookup"><span data-stu-id="93fce-174">Data Type Restrictions</span></span>  
 <span data-ttu-id="93fce-175">Chaque opérateur que vous définissez doit impliquer la classe ou la structure sur laquelle vous le définissez.</span><span class="sxs-lookup"><span data-stu-id="93fce-175">Every operator you define must involve the class or structure on which you define it.</span></span> <span data-ttu-id="93fce-176">Cela signifie que la classe ou structure doit apparaître en tant que le type de données des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="93fce-176">This means that the class or structure must appear as the data type of the following:</span></span>  
  
-   <span data-ttu-id="93fce-177">L’opérande d’un opérateur unaire.</span><span class="sxs-lookup"><span data-stu-id="93fce-177">The operand of a unary operator.</span></span>  
  
-   <span data-ttu-id="93fce-178">Au moins un des opérandes d’un opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="93fce-178">At least one of the operands of a binary operator.</span></span>  
  
-   <span data-ttu-id="93fce-179">L’opérande ou le type de retour d’un opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="93fce-179">Either the operand or the return type of a conversion operator.</span></span>  
  
 <span data-ttu-id="93fce-180">Certains opérateurs ont des données supplémentaires de type des restrictions, comme suit :</span><span class="sxs-lookup"><span data-stu-id="93fce-180">Certain operators have additional data type restrictions, as follows:</span></span>  
  
-   <span data-ttu-id="93fce-181">Si vous définissez la `IsTrue` et `IsFalse` opérateurs, ils doivent retourner le `Boolean` type.</span><span class="sxs-lookup"><span data-stu-id="93fce-181">If you define the `IsTrue` and `IsFalse` operators, they must both return the `Boolean` type.</span></span>  
  
-   <span data-ttu-id="93fce-182">Si vous définissez la `<<` et `>>` opérateurs, ils doivent tous deux spécifient le `Integer` type pour le `operandtype` de `operand2`.</span><span class="sxs-lookup"><span data-stu-id="93fce-182">If you define the `<<` and `>>` operators, they must both specify the `Integer` type for the `operandtype` of `operand2`.</span></span>  
  
 <span data-ttu-id="93fce-183">Le type de retour ne doit pas forcément correspondre au type de des opérandes.</span><span class="sxs-lookup"><span data-stu-id="93fce-183">The return type does not have to correspond to the type of either operand.</span></span> <span data-ttu-id="93fce-184">Par exemple, un opérateur de comparaison tel que `=` ou `<>` peut retourner `Boolean` même si aucun des opérandes sont `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="93fce-184">For example, a comparison operator such as `=` or `<>` can return `Boolean` even if neither operand is `Boolean`.</span></span>  
  
## <a name="logical-and-bitwise-operators"></a><span data-ttu-id="93fce-185">Opérateurs de bits et opérateurs logiques</span><span class="sxs-lookup"><span data-stu-id="93fce-185">Logical and Bitwise Operators</span></span>  
 <span data-ttu-id="93fce-186">Le `And`, `Or`, `Not`, et `Xor` opérateurs peuvent effectuer des opérations logiques ou au niveau du bit en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="93fce-186">The `And`, `Or`, `Not`, and `Xor` operators can perform either logical or bitwise operations in Visual Basic.</span></span> <span data-ttu-id="93fce-187">Toutefois, si vous définissez un de ces opérateurs sur une classe ou structure, vous pouvez définir uniquement son opération au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="93fce-187">However, if you define one of these operators on a class or structure, you can define only its bitwise operation.</span></span>  
  
 <span data-ttu-id="93fce-188">Vous ne pouvez pas définir le `AndAlso` opérateur directement avec un `Operator` instruction.</span><span class="sxs-lookup"><span data-stu-id="93fce-188">You cannot define the `AndAlso` operator directly with an `Operator` statement.</span></span> <span data-ttu-id="93fce-189">Toutefois, vous pouvez utiliser `AndAlso` si vous avez rempli les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="93fce-189">However, you can use `AndAlso` if you have fulfilled the following conditions:</span></span>  
  
-   <span data-ttu-id="93fce-190">Vous avez défini `And` sur les mêmes types d’opérande à utiliser pour `AndAlso`.</span><span class="sxs-lookup"><span data-stu-id="93fce-190">You have defined `And` on the same operand types you want to use for `AndAlso`.</span></span>  
  
-   <span data-ttu-id="93fce-191">Votre définition de `And` retourne le même type que la classe ou la structure sur lequel vous l’avez défini.</span><span class="sxs-lookup"><span data-stu-id="93fce-191">Your definition of `And` returns the same type as the class or structure on which you have defined it.</span></span>  
  
-   <span data-ttu-id="93fce-192">Vous avez défini le `IsFalse` opérateur sur la classe ou la structure sur laquelle vous avez défini `And`.</span><span class="sxs-lookup"><span data-stu-id="93fce-192">You have defined the `IsFalse` operator on the class or structure on which you have defined `And`.</span></span>  
  
 <span data-ttu-id="93fce-193">De même, vous pouvez utiliser `OrElse` si vous avez défini `Or` sur les mêmes opérandes, avec le type de retour de la classe ou structure et que vous avez défini `IsTrue` sur la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="93fce-193">Similarly, you can use `OrElse` if you have defined `Or` on the same operands, with the return type of the class or structure, and you have defined `IsTrue` on the class or structure.</span></span>  
  
## <a name="widening-and-narrowing-conversions"></a><span data-ttu-id="93fce-194">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="93fce-194">Widening and Narrowing Conversions</span></span>  
 <span data-ttu-id="93fce-195">Un *conversion étendue* réussit toujours au moment de l’exécution, pendant un *conversion restrictive* peut échouer au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="93fce-195">A *widening conversion* always succeeds at run time, while a *narrowing conversion* can fail at run time.</span></span> <span data-ttu-id="93fce-196">Pour plus d’informations, consultez [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).</span><span class="sxs-lookup"><span data-stu-id="93fce-196">For more information, see [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).</span></span>  
  
 <span data-ttu-id="93fce-197">Si vous déclarez une procédure de conversion pour être `Widening`, votre code de procédure ne doit pas générer d’échecs.</span><span class="sxs-lookup"><span data-stu-id="93fce-197">If you declare a conversion procedure to be `Widening`, your procedure code must not generate any failures.</span></span> <span data-ttu-id="93fce-198">Par conséquent :</span><span class="sxs-lookup"><span data-stu-id="93fce-198">This means the following:</span></span>  
  
-   <span data-ttu-id="93fce-199">Elle doit toujours retourner une valeur valide de type `type`.</span><span class="sxs-lookup"><span data-stu-id="93fce-199">It must always return a valid value of type `type`.</span></span>  
  
-   <span data-ttu-id="93fce-200">Il doit gérer toutes les exceptions possibles et autres conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="93fce-200">It must handle all possible exceptions and other error conditions.</span></span>  
  
-   <span data-ttu-id="93fce-201">Il doit gérer les erreurs retournées par toutes les procédures qu’elle appelle.</span><span class="sxs-lookup"><span data-stu-id="93fce-201">It must handle any error returns from any procedures it calls.</span></span>  
  
 <span data-ttu-id="93fce-202">S’il est possible qu’une procédure de conversion peut échouer, ou qu’elle peut entraîner une exception non gérée, vous devez déclarer qu’elle soit `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="93fce-202">If there is any possibility that a conversion procedure might not succeed, or that it might cause an unhandled exception, you must declare it to be `Narrowing`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="93fce-203">Exemple</span><span class="sxs-lookup"><span data-stu-id="93fce-203">Example</span></span>  
 <span data-ttu-id="93fce-204">Le code suivant exemple utilise le `Operator` instruction pour définir le contour d’une structure qui inclut des procédures d’opérateur pour le `And`, `Or`, `IsFalse`, et `IsTrue` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="93fce-204">The following code example uses the `Operator` statement to define the outline of a structure that includes operator procedures for the `And`, `Or`, `IsFalse`, and `IsTrue` operators.</span></span> <span data-ttu-id="93fce-205">`And` et `Or` chacun prennent deux opérandes de type `abc` et type de retour `abc`.</span><span class="sxs-lookup"><span data-stu-id="93fce-205">`And` and `Or` each take two operands of type `abc` and return type `abc`.</span></span> <span data-ttu-id="93fce-206">`IsFalse` et `IsTrue` chacune accepter un opérande unique de type `abc` et retourner `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="93fce-206">`IsFalse` and `IsTrue` each take a single operand of type `abc` and return `Boolean`.</span></span> <span data-ttu-id="93fce-207">Ces définitions permettent au code appelant d’utiliser `And`, `AndAlso`, `Or`, et `OrElse` avec opérandes de type `abc`.</span><span class="sxs-lookup"><span data-stu-id="93fce-207">These definitions allow the calling code to use `And`, `AndAlso`, `Or`, and `OrElse` with operands of type `abc`.</span></span>  
  
 [!code-vb[VbVbalrStatements#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#44)]  
  
## <a name="see-also"></a><span data-ttu-id="93fce-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93fce-208">See also</span></span>

- [<span data-ttu-id="93fce-209">IsFalse (opérateur)</span><span class="sxs-lookup"><span data-stu-id="93fce-209">IsFalse Operator</span></span>](../../../visual-basic/language-reference/operators/isfalse-operator.md)
- [<span data-ttu-id="93fce-210">IsTrue (opérateur)</span><span class="sxs-lookup"><span data-stu-id="93fce-210">IsTrue Operator</span></span>](../../../visual-basic/language-reference/operators/istrue-operator.md)
- [<span data-ttu-id="93fce-211">Widening</span><span class="sxs-lookup"><span data-stu-id="93fce-211">Widening</span></span>](../../../visual-basic/language-reference/modifiers/widening.md)
- [<span data-ttu-id="93fce-212">Narrowing</span><span class="sxs-lookup"><span data-stu-id="93fce-212">Narrowing</span></span>](../../../visual-basic/language-reference/modifiers/narrowing.md)
- [<span data-ttu-id="93fce-213">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="93fce-213">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="93fce-214">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="93fce-214">Operator Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)
- [<span data-ttu-id="93fce-215">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="93fce-215">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="93fce-216">Guide pratique pour Définir un opérateur de Conversion</span><span class="sxs-lookup"><span data-stu-id="93fce-216">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="93fce-217">Guide pratique pour Appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="93fce-217">How to: Call an Operator Procedure</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="93fce-218">Guide pratique pour Utiliser une classe qui définit des opérateurs</span><span class="sxs-lookup"><span data-stu-id="93fce-218">How to: Use a Class that Defines Operators</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-use-a-class-that-defines-operators.md)
