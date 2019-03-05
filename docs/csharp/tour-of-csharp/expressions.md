---
title: Expressions C# - Visite guidée du langage C#
description: Les expressions, opérandes et opérateurs sont des blocs de construction du langage C#
ms.date: 11/06/2016
ms.assetid: 20d5eb10-7381-47b9-ad90-f1cc895aa27e
ms.openlocfilehash: 682f98d51bf4eb3c1641297972afb86956e06d3e
ms.sourcegitcommit: 79066169e93d9d65203028b21983574ad9dcf6b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57212090"
---
# <a name="expressions"></a><span data-ttu-id="2a6aa-103">Expressions</span><span class="sxs-lookup"><span data-stu-id="2a6aa-103">Expressions</span></span>

<span data-ttu-id="2a6aa-104">Les *expressions* sont construites à partir de *d’opérandes* et *d’opérateurs*.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-104">*Expressions* are constructed from *operands* and *operators*.</span></span> <span data-ttu-id="2a6aa-105">Les opérateurs d’une expression indiquent les opérations à appliquer aux opérandes.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-105">The operators of an expression indicate which operations to apply to the operands.</span></span> <span data-ttu-id="2a6aa-106">Parmi les exemples d’opérateurs figurent `+`, `-`, `*`, `/` et `new`.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-106">Examples of operators include `+`, `-`, `*`, `/`, and `new`.</span></span> <span data-ttu-id="2a6aa-107">Les littéraux, les champs, les variables locales et les expressions sont des exemples d’opérandes.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-107">Examples of operands include literals, fields, local variables, and expressions.</span></span>

<span data-ttu-id="2a6aa-108">Quand une expression contient plusieurs opérateurs, la *priorité* des opérateurs contrôle l'ordre dans lequel les opérateurs individuels sont évalués.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-108">When an expression contains multiple operators, the *precedence* of the operators controls the order in which the individual operators are evaluated.</span></span> <span data-ttu-id="2a6aa-109">Par exemple, l’expression `x + y * z` est évaluée comme `x + (y * z)`, car l’opérateur `*` a une priorité plus élevée que `+`.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-109">For example, the expression `x + y * z` is evaluated as `x + (y * z)` because the `*` operator has higher precedence than the `+` operator.</span></span>

<span data-ttu-id="2a6aa-110">Lorsqu’un opérande se produit entre deux opérateurs de même priorité, *l’associativité* des opérateurs détermine l’ordre dans lequel les opérations sont effectuées :</span><span class="sxs-lookup"><span data-stu-id="2a6aa-110">When an operand occurs between two operators with the same precedence, the *associativity* of the operators controls the order in which the operations are performed:</span></span>

*   <span data-ttu-id="2a6aa-111">À l’exception des opérateurs d’assignation, tous les opérateurs binaires sont *associatifs sur leur gauche*, ce qui signifie que les opérations sont effectuées de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-111">Except for the assignment operators, all binary operators are *left-associative*, meaning that operations are performed from left to right.</span></span> <span data-ttu-id="2a6aa-112">Par exemple, `x + y + z` est évalué comme étant `(x + y) + z`.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-112">For example, `x + y + z` is evaluated as `(x + y) + z`.</span></span>
*   <span data-ttu-id="2a6aa-113">Les opérateurs d’assignation et l’opérateur conditionnel (`?:`) sont *associatifs sur leur droite*, ce qui signifie que les opérations sont effectuées de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-113">The assignment operators and the conditional operator (`?:`) are *right-associative*, meaning that operations are performed from right to left.</span></span> <span data-ttu-id="2a6aa-114">Par exemple, `x = y = z` est évalué comme étant `x = (y = z)`.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-114">For example, `x = y = z` is evaluated as `x = (y = z)`.</span></span>

<span data-ttu-id="2a6aa-115">La priorité et l’associativité peuvent être contrôlées à l’aide de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-115">Precedence and associativity can be controlled using parentheses.</span></span> <span data-ttu-id="2a6aa-116">Par exemple, `x + y * z` multiplie d’abord `y` par `z`, puis ajoute le résultat à `x`, mais `(x + y) * z` ajoute d’abord `x` et `y`, puis multiplie le résultat par `z`.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-116">For example, `x + y * z` first multiplies `y` by `z` and then adds the result to `x`, but `(x + y) * z` first adds `x` and `y` and then multiplies the result by `z`.</span></span>

<span data-ttu-id="2a6aa-117">La plupart des opérateurs peuvent être *surchargés*.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-117">Most operators can be *overloaded*.</span></span> <span data-ttu-id="2a6aa-118">La surcharge d’opérateur autorise la spécification d’implémentations d’opérateurs définies par l’utilisateur pour les opérations où l’un des deux opérandes ou les deux sont d’un type classe ou struct défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-118">Operator overloading permits user-defined operator implementations to be specified for operations where one or both of the operands are of a user-defined class or struct type.</span></span>

<span data-ttu-id="2a6aa-119">Voici un résumé des opérateurs de C# répertoriant les catégories d’opérateurs dans l’ordre de priorité, de la plus élevée à la plus basse.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-119">The following summarizes C#’s operators, listing the operator categories in order of precedence from highest to lowest.</span></span> <span data-ttu-id="2a6aa-120">Les opérateurs de la même catégorie ont la même priorité.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-120">Operators in the same category have equal precedence.</span></span> <span data-ttu-id="2a6aa-121">Sous chaque catégorie se trouve une liste d’expressions dans cette catégorie, ainsi que la description de ce type d’expression.</span><span class="sxs-lookup"><span data-stu-id="2a6aa-121">Under each category is a list of expressions in that category along with the description of that expression type.</span></span>

* <span data-ttu-id="2a6aa-122">Principale</span><span class="sxs-lookup"><span data-stu-id="2a6aa-122">Primary</span></span>
    - <span data-ttu-id="2a6aa-123">`x.m`: Accès au membre</span><span class="sxs-lookup"><span data-stu-id="2a6aa-123">`x.m`: Member access</span></span>
    - <span data-ttu-id="2a6aa-124">`x(...)`: Méthode et appel de délégué</span><span class="sxs-lookup"><span data-stu-id="2a6aa-124">`x(...)`: Method and delegate invocation</span></span>
    - <span data-ttu-id="2a6aa-125">`x[...]`: Tableau et accès d'indexeur</span><span class="sxs-lookup"><span data-stu-id="2a6aa-125">`x[...]`: Array and indexer access</span></span>
    - <span data-ttu-id="2a6aa-126">`x++`: Post-incrémentation</span><span class="sxs-lookup"><span data-stu-id="2a6aa-126">`x++`: Post-increment</span></span>
    - <span data-ttu-id="2a6aa-127">`x--`: Post-décrémentation</span><span class="sxs-lookup"><span data-stu-id="2a6aa-127">`x--`: Post-decrement</span></span>
    - <span data-ttu-id="2a6aa-128">`new T(...)`: Création d'objet et de délégué</span><span class="sxs-lookup"><span data-stu-id="2a6aa-128">`new T(...)`: Object and delegate creation</span></span>
    - <span data-ttu-id="2a6aa-129">`new T(...){...}`: Création d’objet avec initialiseur</span><span class="sxs-lookup"><span data-stu-id="2a6aa-129">`new T(...){...}`: Object creation with initializer</span></span>
    - <span data-ttu-id="2a6aa-130">`new {...}`:  Initialiseur d’objet anonyme</span><span class="sxs-lookup"><span data-stu-id="2a6aa-130">`new {...}`:  Anonymous object initializer</span></span>
    - <span data-ttu-id="2a6aa-131">`new T[...]`: Création de tableau</span><span class="sxs-lookup"><span data-stu-id="2a6aa-131">`new T[...]`: Array creation</span></span>
    - <span data-ttu-id="2a6aa-132">`typeof(T)`: Obtenir l’objet <xref:System.Type> de `T`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-132">`typeof(T)`: Obtain <xref:System.Type> object for `T`</span></span>
    - <span data-ttu-id="2a6aa-133">`checked(x)`: Évaluer l'expression dans le contexte vérifié (checked)</span><span class="sxs-lookup"><span data-stu-id="2a6aa-133">`checked(x)`: Evaluate expression in checked context</span></span>
    - <span data-ttu-id="2a6aa-134">`unchecked(x)`: Évaluer l'expression dans le contexte non vérifié (unchecked)</span><span class="sxs-lookup"><span data-stu-id="2a6aa-134">`unchecked(x)`: Evaluate expression in unchecked context</span></span>
    - <span data-ttu-id="2a6aa-135">`default(T)`: Obtenir la valeur par défaut du type `T`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-135">`default(T)`: Obtain default value of type `T`</span></span>
    - <span data-ttu-id="2a6aa-136">`delegate {...}`: Fonction anonyme (méthode anonyme)</span><span class="sxs-lookup"><span data-stu-id="2a6aa-136">`delegate {...}`: Anonymous function (anonymous method)</span></span>
* <span data-ttu-id="2a6aa-137">Unaire</span><span class="sxs-lookup"><span data-stu-id="2a6aa-137">Unary</span></span>
    - <span data-ttu-id="2a6aa-138">`+x`: Identité</span><span class="sxs-lookup"><span data-stu-id="2a6aa-138">`+x`: Identity</span></span>
    - <span data-ttu-id="2a6aa-139">`-x`: Négation</span><span class="sxs-lookup"><span data-stu-id="2a6aa-139">`-x`: Negation</span></span>
    - <span data-ttu-id="2a6aa-140">`!x`: Négation logique</span><span class="sxs-lookup"><span data-stu-id="2a6aa-140">`!x`: Logical negation</span></span>
    - <span data-ttu-id="2a6aa-141">`~x`: Négation d'opération de bits</span><span class="sxs-lookup"><span data-stu-id="2a6aa-141">`~x`: Bitwise negation</span></span>
    - <span data-ttu-id="2a6aa-142">`++x`: Pré-incrémentation</span><span class="sxs-lookup"><span data-stu-id="2a6aa-142">`++x`: Pre-increment</span></span>
    - <span data-ttu-id="2a6aa-143">`--x`: Pré-décrémentation</span><span class="sxs-lookup"><span data-stu-id="2a6aa-143">`--x`: Pre-decrement</span></span>
    - <span data-ttu-id="2a6aa-144">`(T)x`: Convertir explicitement `x` en type `T`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-144">`(T)x`: Explicitly convert `x` to type `T`</span></span>
    - <span data-ttu-id="2a6aa-145">`await x`: Attendre de façon asynchrone la fin de `x`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-145">`await x`: Asynchronously wait for `x` to complete</span></span>
* <span data-ttu-id="2a6aa-146">Multiplication</span><span class="sxs-lookup"><span data-stu-id="2a6aa-146">Multiplicative</span></span>
    - <span data-ttu-id="2a6aa-147">`x * y`: Multiplication</span><span class="sxs-lookup"><span data-stu-id="2a6aa-147">`x * y`: Multiplication</span></span>
    - <span data-ttu-id="2a6aa-148">`x / y`: Division</span><span class="sxs-lookup"><span data-stu-id="2a6aa-148">`x / y`: Division</span></span>
    - <span data-ttu-id="2a6aa-149">`x % y`: Reste</span><span class="sxs-lookup"><span data-stu-id="2a6aa-149">`x % y`: Remainder</span></span>
* <span data-ttu-id="2a6aa-150">Addition</span><span class="sxs-lookup"><span data-stu-id="2a6aa-150">Additive</span></span>
    - <span data-ttu-id="2a6aa-151">`x + y`: Addition, concaténation de chaînes, combinaison de délégués</span><span class="sxs-lookup"><span data-stu-id="2a6aa-151">`x + y`: Addition, string concatenation, delegate combination</span></span>
    - <span data-ttu-id="2a6aa-152">`x – y`: Soustraction, suppression de délégué</span><span class="sxs-lookup"><span data-stu-id="2a6aa-152">`x – y`: Subtraction, delegate removal</span></span>
* <span data-ttu-id="2a6aa-153">Shift</span><span class="sxs-lookup"><span data-stu-id="2a6aa-153">Shift</span></span>
    - <span data-ttu-id="2a6aa-154">`x << y`: Décalage à gauche</span><span class="sxs-lookup"><span data-stu-id="2a6aa-154">`x << y`: Shift left</span></span>
    - <span data-ttu-id="2a6aa-155">`x >> y`: Décalage à droite</span><span class="sxs-lookup"><span data-stu-id="2a6aa-155">`x >> y`: Shift right</span></span>
* <span data-ttu-id="2a6aa-156">Relations et test de type</span><span class="sxs-lookup"><span data-stu-id="2a6aa-156">Relational and type testing</span></span>
    - <span data-ttu-id="2a6aa-157">`x < y`: Inférieur à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-157">`x < y`: Less than</span></span>
    - <span data-ttu-id="2a6aa-158">`x > y`: Supérieur à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-158">`x > y`: Greater than</span></span>
    - <span data-ttu-id="2a6aa-159">`x <= y`: Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-159">`x <= y`: Less than or equal</span></span>
    - <span data-ttu-id="2a6aa-160">`x >= y`: Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-160">`x >= y`: Greater than or equal</span></span>
    - <span data-ttu-id="2a6aa-161">`x is T`: Retourne `true` si `x` est un `T`, `false` sinon</span><span class="sxs-lookup"><span data-stu-id="2a6aa-161">`x is T`: Return `true` if `x` is a `T`, `false` otherwise</span></span>
    - <span data-ttu-id="2a6aa-162">`x as T`: Retourne `x` de type `T`, ou `null` si `x` n’est pas un `T`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-162">`x as T`: Return `x` typed as `T`, or `null` if `x` is not a `T`</span></span>
* <span data-ttu-id="2a6aa-163">Égalité</span><span class="sxs-lookup"><span data-stu-id="2a6aa-163">Equality</span></span>
    - <span data-ttu-id="2a6aa-164">`x == y`: Égal à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-164">`x == y`: Equal</span></span>
    - <span data-ttu-id="2a6aa-165">`x != y`: Non égal à</span><span class="sxs-lookup"><span data-stu-id="2a6aa-165">`x != y`: Not equal</span></span>
* <span data-ttu-id="2a6aa-166">AND logique</span><span class="sxs-lookup"><span data-stu-id="2a6aa-166">Logical AND</span></span>
    - <span data-ttu-id="2a6aa-167">`x & y`: AND d’entiers au niveau du bit, AND logique booléen</span><span class="sxs-lookup"><span data-stu-id="2a6aa-167">`x & y`: Integer bitwise AND, boolean logical AND</span></span>
* <span data-ttu-id="2a6aa-168">XOR logique</span><span class="sxs-lookup"><span data-stu-id="2a6aa-168">Logical XOR</span></span>
    - <span data-ttu-id="2a6aa-169">`x ^ y`: Opération de bits entière XOR, Boolean logique XOR</span><span class="sxs-lookup"><span data-stu-id="2a6aa-169">`x ^ y`: Integer bitwise XOR, boolean logical XOR</span></span>
* <span data-ttu-id="2a6aa-170">OR logique</span><span class="sxs-lookup"><span data-stu-id="2a6aa-170">Logical OR</span></span>
    - <span data-ttu-id="2a6aa-171">`x | y`: Opération de bits entière OR, Boolean logique OR</span><span class="sxs-lookup"><span data-stu-id="2a6aa-171">`x | y`: Integer bitwise OR, boolean logical OR</span></span>
* <span data-ttu-id="2a6aa-172">AND conditionnel</span><span class="sxs-lookup"><span data-stu-id="2a6aa-172">Conditional AND</span></span>
    - <span data-ttu-id="2a6aa-173">`x && y`: Prend la valeur `y` uniquement si `x` n’est pas `false`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-173">`x && y`: Evaluates `y` only if `x` is not `false`</span></span>
* <span data-ttu-id="2a6aa-174">OR conditionnel</span><span class="sxs-lookup"><span data-stu-id="2a6aa-174">Conditional OR</span></span>
    - <span data-ttu-id="2a6aa-175">`x || y`: Prend la valeur `y` uniquement si `x` n’est pas `true`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-175">`x || y`: Evaluates `y` only if `x` is not `true`</span></span>
* <span data-ttu-id="2a6aa-176">Fusion de Null</span><span class="sxs-lookup"><span data-stu-id="2a6aa-176">Null coalescing</span></span>
    - <span data-ttu-id="2a6aa-177">`x ?? y`: Prend la valeur `y` si `x` est Null, `x` sinon</span><span class="sxs-lookup"><span data-stu-id="2a6aa-177">`x ?? y`: Evaluates to `y` if `x` is null, to `x` otherwise</span></span>
* <span data-ttu-id="2a6aa-178">Conditionnel</span><span class="sxs-lookup"><span data-stu-id="2a6aa-178">Conditional</span></span>
    - <span data-ttu-id="2a6aa-179">`x ? y : z`: Prend la valeur `y` si `x` est `true`, `z` si `x` est `false`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-179">`x ? y : z`: Evaluates `y` if `x` is `true`, `z` if `x` is `false`</span></span>
* <span data-ttu-id="2a6aa-180">Attribution ou fonction anonyme</span><span class="sxs-lookup"><span data-stu-id="2a6aa-180">Assignment or anonymous function</span></span>
    - <span data-ttu-id="2a6aa-181">`x = y`: Attribution</span><span class="sxs-lookup"><span data-stu-id="2a6aa-181">`x = y`: Assignment</span></span>
    - <span data-ttu-id="2a6aa-182">`x op= y`: Assignation composée ; opérateurs pris en charge :</span><span class="sxs-lookup"><span data-stu-id="2a6aa-182">`x op= y`: Compound assignment; supported operators are</span></span>
        - <span data-ttu-id="2a6aa-183">`*=`   `/=`   `%=`   `+=`   `-=`   `<<=`   `>>=`   `&=`  `^=`  `|=`</span><span class="sxs-lookup"><span data-stu-id="2a6aa-183">`*=`   `/=`   `%=`   `+=`   `-=`   `<<=`   `>>=`   `&=`  `^=`  `|=`</span></span>
    - <span data-ttu-id="2a6aa-184">`(T x) => y`: Fonction anonyme (expression lambda)</span><span class="sxs-lookup"><span data-stu-id="2a6aa-184">`(T x) => y`: Anonymous function (lambda expression)</span></span>

> [!div class="step-by-step"]
> <span data-ttu-id="2a6aa-185">[Précédent](types-and-variables.md)
> [Suivant](statements.md)</span><span class="sxs-lookup"><span data-stu-id="2a6aa-185">[Previous](types-and-variables.md)
[Next](statements.md)</span></span>