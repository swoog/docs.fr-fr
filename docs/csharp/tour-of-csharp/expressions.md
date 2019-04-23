---
title: Expressions C# - Visite guidée du langage C#
description: Les expressions, opérandes et opérateurs sont des blocs de construction du langage C#
ms.date: 11/06/2016
ms.assetid: 20d5eb10-7381-47b9-ad90-f1cc895aa27e
ms.openlocfilehash: 4ffe947a4cb8c36a5925a4b3846486e44a9d8ec4
ms.sourcegitcommit: 859b2ba0c74a1a5a4ad0d59a3c3af23450995981
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/11/2019
ms.locfileid: "59480753"
---
# <a name="expressions"></a><span data-ttu-id="59520-103">Expressions</span><span class="sxs-lookup"><span data-stu-id="59520-103">Expressions</span></span>

<span data-ttu-id="59520-104">Les *expressions* sont construites à partir de *d’opérandes* et *d’opérateurs*.</span><span class="sxs-lookup"><span data-stu-id="59520-104">*Expressions* are constructed from *operands* and *operators*.</span></span> <span data-ttu-id="59520-105">Les opérateurs d’une expression indiquent les opérations à appliquer aux opérandes.</span><span class="sxs-lookup"><span data-stu-id="59520-105">The operators of an expression indicate which operations to apply to the operands.</span></span> <span data-ttu-id="59520-106">Parmi les exemples d’opérateurs figurent `+`, `-`, `*`, `/` et `new`.</span><span class="sxs-lookup"><span data-stu-id="59520-106">Examples of operators include `+`, `-`, `*`, `/`, and `new`.</span></span> <span data-ttu-id="59520-107">Les littéraux, les champs, les variables locales et les expressions sont des exemples d’opérandes.</span><span class="sxs-lookup"><span data-stu-id="59520-107">Examples of operands include literals, fields, local variables, and expressions.</span></span>

<span data-ttu-id="59520-108">Quand une expression contient plusieurs opérateurs, la *priorité* des opérateurs contrôle l'ordre dans lequel les opérateurs individuels sont évalués.</span><span class="sxs-lookup"><span data-stu-id="59520-108">When an expression contains multiple operators, the *precedence* of the operators controls the order in which the individual operators are evaluated.</span></span> <span data-ttu-id="59520-109">Par exemple, l’expression `x + y * z` est évaluée comme `x + (y * z)`, car l’opérateur `*` a une priorité plus élevée que `+`.</span><span class="sxs-lookup"><span data-stu-id="59520-109">For example, the expression `x + y * z` is evaluated as `x + (y * z)` because the `*` operator has higher precedence than the `+` operator.</span></span>

<span data-ttu-id="59520-110">Lorsqu’un opérande se produit entre deux opérateurs de même priorité, *l’associativité* des opérateurs détermine l’ordre dans lequel les opérations sont effectuées :</span><span class="sxs-lookup"><span data-stu-id="59520-110">When an operand occurs between two operators with the same precedence, the *associativity* of the operators controls the order in which the operations are performed:</span></span>

* <span data-ttu-id="59520-111">À l’exception des opérateurs d’assignation, tous les opérateurs binaires sont *associatifs sur leur gauche*, ce qui signifie que les opérations sont effectuées de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="59520-111">Except for the assignment operators, all binary operators are *left-associative*, meaning that operations are performed from left to right.</span></span> <span data-ttu-id="59520-112">Par exemple, `x + y + z` est évalué comme étant `(x + y) + z`.</span><span class="sxs-lookup"><span data-stu-id="59520-112">For example, `x + y + z` is evaluated as `(x + y) + z`.</span></span>
* <span data-ttu-id="59520-113">Les opérateurs d’assignation et l’opérateur conditionnel (`?:`) sont *associatifs sur leur droite*, ce qui signifie que les opérations sont effectuées de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="59520-113">The assignment operators and the conditional operator (`?:`) are *right-associative*, meaning that operations are performed from right to left.</span></span> <span data-ttu-id="59520-114">Par exemple, `x = y = z` est évalué comme étant `x = (y = z)`.</span><span class="sxs-lookup"><span data-stu-id="59520-114">For example, `x = y = z` is evaluated as `x = (y = z)`.</span></span>

<span data-ttu-id="59520-115">La priorité et l’associativité peuvent être contrôlées à l’aide de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="59520-115">Precedence and associativity can be controlled using parentheses.</span></span> <span data-ttu-id="59520-116">Par exemple, `x + y * z` multiplie d’abord `y` par `z`, puis ajoute le résultat à `x`, mais `(x + y) * z` ajoute d’abord `x` et `y`, puis multiplie le résultat par `z`.</span><span class="sxs-lookup"><span data-stu-id="59520-116">For example, `x + y * z` first multiplies `y` by `z` and then adds the result to `x`, but `(x + y) * z` first adds `x` and `y` and then multiplies the result by `z`.</span></span>

<span data-ttu-id="59520-117">La plupart des opérateurs peuvent être *surchargés*.</span><span class="sxs-lookup"><span data-stu-id="59520-117">Most operators can be *overloaded*.</span></span> <span data-ttu-id="59520-118">La surcharge d’opérateur autorise la spécification d’implémentations d’opérateurs définies par l’utilisateur pour les opérations où l’un des deux opérandes ou les deux sont d’un type classe ou struct défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59520-118">Operator overloading permits user-defined operator implementations to be specified for operations where one or both of the operands are of a user-defined class or struct type.</span></span>

<span data-ttu-id="59520-119">Voici un résumé des opérateurs de C# répertoriant les catégories d’opérateurs dans l’ordre de priorité, de la plus élevée à la plus basse.</span><span class="sxs-lookup"><span data-stu-id="59520-119">The following summarizes C#’s operators, listing the operator categories in order of precedence from highest to lowest.</span></span> <span data-ttu-id="59520-120">Les opérateurs de la même catégorie ont la même priorité.</span><span class="sxs-lookup"><span data-stu-id="59520-120">Operators in the same category have equal precedence.</span></span> <span data-ttu-id="59520-121">Sous chaque catégorie se trouve une liste d’expressions dans cette catégorie, ainsi que la description de ce type d’expression.</span><span class="sxs-lookup"><span data-stu-id="59520-121">Under each category is a list of expressions in that category along with the description of that expression type.</span></span>

* <span data-ttu-id="59520-122">Principale</span><span class="sxs-lookup"><span data-stu-id="59520-122">Primary</span></span>
  - `x.m`<span data-ttu-id="59520-123">: Accès au membre</span><span class="sxs-lookup"><span data-stu-id="59520-123">: Member access</span></span>
  - `x(...)`<span data-ttu-id="59520-124">: Méthode et appel de délégué</span><span class="sxs-lookup"><span data-stu-id="59520-124">: Method and delegate invocation</span></span>
  - `x[...]`<span data-ttu-id="59520-125">: Tableau et accès d'indexeur</span><span class="sxs-lookup"><span data-stu-id="59520-125">: Array and indexer access</span></span>
  - `x++`<span data-ttu-id="59520-126">: Post-incrémentation</span><span class="sxs-lookup"><span data-stu-id="59520-126">: Post-increment</span></span>
  - `x--`<span data-ttu-id="59520-127">: Post-décrémentation</span><span class="sxs-lookup"><span data-stu-id="59520-127">: Post-decrement</span></span>
  - `new T(...)`<span data-ttu-id="59520-128">: Création d'objet et de délégué</span><span class="sxs-lookup"><span data-stu-id="59520-128">: Object and delegate creation</span></span>
  - `new T(...){...}`<span data-ttu-id="59520-129">: Création d’objet avec initialiseur</span><span class="sxs-lookup"><span data-stu-id="59520-129">: Object creation with initializer</span></span>
  - `new {...}`<span data-ttu-id="59520-130">:  Initialiseur d’objet anonyme</span><span class="sxs-lookup"><span data-stu-id="59520-130">:  Anonymous object initializer</span></span>
  - `new T[...]`<span data-ttu-id="59520-131">: Création de tableau</span><span class="sxs-lookup"><span data-stu-id="59520-131">: Array creation</span></span>
  - `typeof(T)`<span data-ttu-id="59520-132">: Récupérer l’objet <xref:System.Type> de</span><span class="sxs-lookup"><span data-stu-id="59520-132">: Obtain <xref:System.Type> object for</span></span> `T`
  - `checked(x)`<span data-ttu-id="59520-133">: Évaluer l'expression dans le contexte vérifié (checked)</span><span class="sxs-lookup"><span data-stu-id="59520-133">: Evaluate expression in checked context</span></span>
  - `unchecked(x)`<span data-ttu-id="59520-134">: Évaluer l'expression dans le contexte non vérifié (unchecked)</span><span class="sxs-lookup"><span data-stu-id="59520-134">: Evaluate expression in unchecked context</span></span>
  - `default(T)`<span data-ttu-id="59520-135">: Récupérer la valeur par défaut du type</span><span class="sxs-lookup"><span data-stu-id="59520-135">: Obtain default value of type</span></span> `T`
  - `delegate {...}`<span data-ttu-id="59520-136">: Fonction anonyme (méthode anonyme)</span><span class="sxs-lookup"><span data-stu-id="59520-136">: Anonymous function (anonymous method)</span></span>
* <span data-ttu-id="59520-137">Unaire</span><span class="sxs-lookup"><span data-stu-id="59520-137">Unary</span></span>
  - `+x`<span data-ttu-id="59520-138">: Identité</span><span class="sxs-lookup"><span data-stu-id="59520-138">: Identity</span></span>
  - `-x`<span data-ttu-id="59520-139">: Négation</span><span class="sxs-lookup"><span data-stu-id="59520-139">: Negation</span></span>
  - `!x`<span data-ttu-id="59520-140">: Négation logique</span><span class="sxs-lookup"><span data-stu-id="59520-140">: Logical negation</span></span>
  - `~x`<span data-ttu-id="59520-141">: Négation d'opération de bits</span><span class="sxs-lookup"><span data-stu-id="59520-141">: Bitwise negation</span></span>
  - `++x`<span data-ttu-id="59520-142">: Pré-incrémentation</span><span class="sxs-lookup"><span data-stu-id="59520-142">: Pre-increment</span></span>
  - `--x`<span data-ttu-id="59520-143">: Pré-décrémentation</span><span class="sxs-lookup"><span data-stu-id="59520-143">: Pre-decrement</span></span>
  - `(T)x`<span data-ttu-id="59520-144">: Convertir explicitement `x` en type</span><span class="sxs-lookup"><span data-stu-id="59520-144">: Explicitly convert `x` to type</span></span> `T`
  - `await x`<span data-ttu-id="59520-145">: Attendre de façon asynchrone la fin de `x`</span><span class="sxs-lookup"><span data-stu-id="59520-145">: Asynchronously wait for `x` to complete</span></span>
* <span data-ttu-id="59520-146">Multiplication</span><span class="sxs-lookup"><span data-stu-id="59520-146">Multiplicative</span></span>
  - `x * y`<span data-ttu-id="59520-147">: Multiplication</span><span class="sxs-lookup"><span data-stu-id="59520-147">: Multiplication</span></span>
  - `x / y`<span data-ttu-id="59520-148">: Division</span><span class="sxs-lookup"><span data-stu-id="59520-148">: Division</span></span>
  - `x % y`<span data-ttu-id="59520-149">: Reste</span><span class="sxs-lookup"><span data-stu-id="59520-149">: Remainder</span></span>
* <span data-ttu-id="59520-150">Addition</span><span class="sxs-lookup"><span data-stu-id="59520-150">Additive</span></span>
  - `x + y`<span data-ttu-id="59520-151">: Addition, concaténation de chaînes, combinaison de délégués</span><span class="sxs-lookup"><span data-stu-id="59520-151">: Addition, string concatenation, delegate combination</span></span>
  - `x – y`<span data-ttu-id="59520-152">: Soustraction, suppression de délégué</span><span class="sxs-lookup"><span data-stu-id="59520-152">: Subtraction, delegate removal</span></span>
* <span data-ttu-id="59520-153">Shift</span><span class="sxs-lookup"><span data-stu-id="59520-153">Shift</span></span>
  - `x << y`<span data-ttu-id="59520-154">: Décalage à gauche</span><span class="sxs-lookup"><span data-stu-id="59520-154">: Shift left</span></span>
  - `x >> y`<span data-ttu-id="59520-155">: Décalage à droite</span><span class="sxs-lookup"><span data-stu-id="59520-155">: Shift right</span></span>
* <span data-ttu-id="59520-156">Relations et test de type</span><span class="sxs-lookup"><span data-stu-id="59520-156">Relational and type testing</span></span>
  - `x < y`<span data-ttu-id="59520-157">: Inférieur à</span><span class="sxs-lookup"><span data-stu-id="59520-157">: Less than</span></span>
  - `x > y`<span data-ttu-id="59520-158">: Supérieur à</span><span class="sxs-lookup"><span data-stu-id="59520-158">: Greater than</span></span>
  - `x <= y`<span data-ttu-id="59520-159">: Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="59520-159">: Less than or equal</span></span>
  - `x >= y`<span data-ttu-id="59520-160">: Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="59520-160">: Greater than or equal</span></span>
  - `x is T`<span data-ttu-id="59520-161">: Retourne `true` si `x` est un `T`, `false` sinon</span><span class="sxs-lookup"><span data-stu-id="59520-161">: Return `true` if `x` is a `T`, `false` otherwise</span></span>
  - `x as T`<span data-ttu-id="59520-162">: Retourne `x` de type `T`, ou `null` si `x` n’est pas un</span><span class="sxs-lookup"><span data-stu-id="59520-162">: Return `x` typed as `T`, or `null` if `x` is not a</span></span> `T`
* <span data-ttu-id="59520-163">Égalité</span><span class="sxs-lookup"><span data-stu-id="59520-163">Equality</span></span>
  - `x == y`<span data-ttu-id="59520-164">: Égal à</span><span class="sxs-lookup"><span data-stu-id="59520-164">: Equal</span></span>
  - `x != y`<span data-ttu-id="59520-165">: Non égal à</span><span class="sxs-lookup"><span data-stu-id="59520-165">: Not equal</span></span>
* <span data-ttu-id="59520-166">AND logique</span><span class="sxs-lookup"><span data-stu-id="59520-166">Logical AND</span></span>
  - `x & y`<span data-ttu-id="59520-167">: AND d’entiers au niveau du bit, AND logique booléen</span><span class="sxs-lookup"><span data-stu-id="59520-167">: Integer bitwise AND, boolean logical AND</span></span>
* <span data-ttu-id="59520-168">XOR logique</span><span class="sxs-lookup"><span data-stu-id="59520-168">Logical XOR</span></span>
  - `x ^ y`<span data-ttu-id="59520-169">: Opération de bits entière XOR, Boolean logique XOR</span><span class="sxs-lookup"><span data-stu-id="59520-169">: Integer bitwise XOR, boolean logical XOR</span></span>
* <span data-ttu-id="59520-170">OR logique</span><span class="sxs-lookup"><span data-stu-id="59520-170">Logical OR</span></span>
  - `x | y`<span data-ttu-id="59520-171">: Opération de bits entière OR, Boolean logique OR</span><span class="sxs-lookup"><span data-stu-id="59520-171">: Integer bitwise OR, boolean logical OR</span></span>
* <span data-ttu-id="59520-172">AND conditionnel</span><span class="sxs-lookup"><span data-stu-id="59520-172">Conditional AND</span></span>
  - `x && y`<span data-ttu-id="59520-173">: Prend la valeur `y` uniquement si `x` n’est pas</span><span class="sxs-lookup"><span data-stu-id="59520-173">: Evaluates `y` only if `x` is not</span></span> `false`
* <span data-ttu-id="59520-174">OR conditionnel</span><span class="sxs-lookup"><span data-stu-id="59520-174">Conditional OR</span></span>
  - `x || y`<span data-ttu-id="59520-175">: Prend la valeur `y` uniquement si `x` n’est pas</span><span class="sxs-lookup"><span data-stu-id="59520-175">: Evaluates `y` only if `x` is not</span></span> `true`
* <span data-ttu-id="59520-176">Fusion de Null</span><span class="sxs-lookup"><span data-stu-id="59520-176">Null coalescing</span></span>
  - `x ?? y`<span data-ttu-id="59520-177">: Prend la valeur `y` si `x` est Null, `x` sinon</span><span class="sxs-lookup"><span data-stu-id="59520-177">: Evaluates to `y` if `x` is null, to `x` otherwise</span></span>
* <span data-ttu-id="59520-178">Conditionnel</span><span class="sxs-lookup"><span data-stu-id="59520-178">Conditional</span></span>
  - `x ? y : z`<span data-ttu-id="59520-179">: Prend la valeur `y` si `x` est `true`, `z` si `x` est</span><span class="sxs-lookup"><span data-stu-id="59520-179">: Evaluates `y` if `x` is `true`, `z` if `x` is</span></span> `false`
* <span data-ttu-id="59520-180">Attribution ou fonction anonyme</span><span class="sxs-lookup"><span data-stu-id="59520-180">Assignment or anonymous function</span></span>
  - `x = y`<span data-ttu-id="59520-181">: Attribution</span><span class="sxs-lookup"><span data-stu-id="59520-181">: Assignment</span></span>
  - `x op= y`<span data-ttu-id="59520-182">: Assignation composée ; opérateurs pris en charge :</span><span class="sxs-lookup"><span data-stu-id="59520-182">: Compound assignment; supported operators are</span></span>
    - `*=`   `/=`   `%=`   `+=`   `-=`   `<<=`   `>>=`   `&=`  `^=`  `|=`
  - `(T x) => y`<span data-ttu-id="59520-183">: Fonction anonyme (expression lambda)</span><span class="sxs-lookup"><span data-stu-id="59520-183">: Anonymous function (lambda expression)</span></span>

> [!div class="step-by-step"]
> <span data-ttu-id="59520-184">[Précédent](types-and-variables.md)
> [Suivant](statements.md)</span><span class="sxs-lookup"><span data-stu-id="59520-184">[Previous](types-and-variables.md)
[Next](statements.md)</span></span>
