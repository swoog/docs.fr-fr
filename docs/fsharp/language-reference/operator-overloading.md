---
title: Surcharge d'opérateur (F#)
description: 'Découvrez comment surcharger des opérateurs arithmétiques dans une classe ou un type d’enregistrement et au niveau global dans F #.'
ms.date: 05/16/2016
ms.openlocfilehash: fc9b7311aa746fd758930365972a187ffdfff0d5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33564363"
---
# <a name="operator-overloading"></a><span data-ttu-id="843e8-103">Surcharge d'opérateur</span><span class="sxs-lookup"><span data-stu-id="843e8-103">Operator Overloading</span></span>

<span data-ttu-id="843e8-104">Cette rubrique décrit comment surcharger des opérateurs arithmétiques dans une classe ou un type d’enregistrement et au niveau global.</span><span class="sxs-lookup"><span data-stu-id="843e8-104">This topic describes how to overload arithmetic operators in a class or record type, and at the global level.</span></span>


## <a name="syntax"></a><span data-ttu-id="843e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="843e8-105">Syntax</span></span>

```fsharp
// Overloading an operator as a class or record member.
static member (operator-symbols) (parameter-list) =
    method-body
// Overloading an operator at the global level
let [inline] (operator-symbols) parameter-list = function-body
```

## <a name="remarks"></a><span data-ttu-id="843e8-106">Notes</span><span class="sxs-lookup"><span data-stu-id="843e8-106">Remarks</span></span>
<span data-ttu-id="843e8-107">Dans la syntaxe précédente, le *symbole d’opérateur* est un des `+`, `-`, `*`, `/`, `=`, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="843e8-107">In the previous syntax, the *operator-symbol* is one of `+`, `-`, `*`, `/`, `=`, and so on.</span></span> <span data-ttu-id="843e8-108">Le *la liste des paramètres* spécifie les opérandes dans l’ordre d’apparition dans la syntaxe standard pour cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="843e8-108">The *parameter-list* specifies the operands in the order they appear in the usual syntax for that operator.</span></span> <span data-ttu-id="843e8-109">Le *corps de la méthode* construit la valeur résultante.</span><span class="sxs-lookup"><span data-stu-id="843e8-109">The *method-body* constructs the resulting value.</span></span>

<span data-ttu-id="843e8-110">Les surcharges d’opérateur pour les opérateurs doivent être statiques.</span><span class="sxs-lookup"><span data-stu-id="843e8-110">Operator overloads for operators must be static.</span></span> <span data-ttu-id="843e8-111">Surcharges d’opérateur pour les opérateurs unaires, telles que `+` et `-`, doivent utiliser un tilde (`~`) dans le *symbole d’opérateur* pour indiquer que l’opérateur est un opérateur unaire et non un opérateur binaire, comme indiqué dans les déclaration suivante.</span><span class="sxs-lookup"><span data-stu-id="843e8-111">Operator overloads for unary operators, such as `+` and `-`, must use a tilde (`~`) in the *operator-symbol* to indicate that the operator is a unary operator and not a binary operator, as shown in the following declaration.</span></span>

```fsharp
static member (~-) (v : Vector)
```

<span data-ttu-id="843e8-112">Le code suivant illustre une classe de vecteur qui a uniquement deux opérateurs, un pour moins unaire et un pour la multiplication par un scalaire.</span><span class="sxs-lookup"><span data-stu-id="843e8-112">The following code illustrates a vector class that has just two operators, one for unary minus and one for multiplication by a scalar.</span></span> <span data-ttu-id="843e8-113">Dans l’exemple, deux surcharges pour la multiplication scalaire sont nécessaires, car l’opérateur doit fonctionner indépendamment de l’ordre dans lequel le vecteur et le scalaire apparaissent.</span><span class="sxs-lookup"><span data-stu-id="843e8-113">In the example, two overloads for scalar multiplication are needed because the operator must work regardless of the order in which the vector and scalar appear.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4001.fs)]

## <a name="creating-new-operators"></a><span data-ttu-id="843e8-114">Création d’opérateurs</span><span class="sxs-lookup"><span data-stu-id="843e8-114">Creating New Operators</span></span>
<span data-ttu-id="843e8-115">Vous pouvez surcharger tous les opérateurs standards, mais vous pouvez également créer des opérateurs hors des séquences de certains caractères.</span><span class="sxs-lookup"><span data-stu-id="843e8-115">You can overload all the standard operators, but you can also create new operators out of sequences of certain characters.</span></span> <span data-ttu-id="843e8-116">Opérateur caractères autorisés sont `!`, `%`, `&`, `*`, `+`, `-`, `.`, `/`, `<`, `=`, `>`, `?`, `@`, `^`, `|`, et `~`.</span><span class="sxs-lookup"><span data-stu-id="843e8-116">Allowed operator characters are `!`, `%`, `&`, `*`, `+`, `-`, `.`, `/`, `<`, `=`, `>`, `?`, `@`, `^`, `|`, and `~`.</span></span> <span data-ttu-id="843e8-117">Le `~` a une signification spéciale de la création d’un opérateur unaire du caractère et ne fait pas partie de la séquence de caractères d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="843e8-117">The `~` character has the special meaning of making an operator unary, and is not part of the operator character sequence.</span></span> <span data-ttu-id="843e8-118">Tous les opérateurs ne peuvent être rendus unaires.</span><span class="sxs-lookup"><span data-stu-id="843e8-118">Not all operators can be made unary.</span></span>

<span data-ttu-id="843e8-119">En fonction de la séquence de caractères exacte que vous utilisez, votre opérateur aura une certaine priorité et l’associativité.</span><span class="sxs-lookup"><span data-stu-id="843e8-119">Depending on the exact character sequence you use, your operator will have a certain precedence and associativity.</span></span> <span data-ttu-id="843e8-120">Peut être soit de gauche à droite ou de droite à gauche des opérateurs et associativité est utilisée chaque fois que les opérateurs ayant le même niveau de priorité apparaissent en séquence sans parenthèses.</span><span class="sxs-lookup"><span data-stu-id="843e8-120">Associativity can be either left to right or right to left and is used whenever operators of the same level of precedence appear in sequence without parentheses.</span></span>

<span data-ttu-id="843e8-121">Le caractère d’opérateur `.` n’affecte pas le niveau de priorité, afin que, par exemple, si vous souhaitez définir votre propre version de multiplication qui a la même priorité et associativité en tant que multiplication ordinaire, vous pouvez créer les opérateurs tels que `.*`.</span><span class="sxs-lookup"><span data-stu-id="843e8-121">The operator character `.` does not affect precedence, so that, for example, if you want to define your own version of multiplication that has the same precedence and associativity as ordinary multiplication, you could create operators such as `.*`.</span></span>

<span data-ttu-id="843e8-122">Seuls les opérateurs `?` et `?<-` peut commencer par `?`.</span><span class="sxs-lookup"><span data-stu-id="843e8-122">Only the operators `?` and `?<-` may start with `?`.</span></span>

<span data-ttu-id="843e8-123">Vous trouverez un tableau qui indique la priorité de tous les opérateurs en F # dans [référence des symboles et opérateur](symbol-and-operator-reference/index.md).</span><span class="sxs-lookup"><span data-stu-id="843e8-123">A table that shows the precedence of all operators in F# can be found in [Symbol and Operator Reference](symbol-and-operator-reference/index.md).</span></span>


## <a name="overloaded-operator-names"></a><span data-ttu-id="843e8-124">Noms d’opérateurs surchargés</span><span class="sxs-lookup"><span data-stu-id="843e8-124">Overloaded Operator Names</span></span>
<span data-ttu-id="843e8-125">Lorsque le compilateur F # compile une expression d’opérateur, il génère une méthode qui a un nom généré par le compilateur pour cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="843e8-125">When the F# compiler compiles an operator expression, it generates a method that has a compiler-generated name for that operator.</span></span> <span data-ttu-id="843e8-126">C’est le nom qui apparaît dans le langage intermédiaire Microsoft (MSIL) pour la méthode et également dans la réflexion et IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="843e8-126">This is the name that appears in the Microsoft intermediate language (MSIL) for the method, and also in reflection and IntelliSense.</span></span> <span data-ttu-id="843e8-127">Normalement, vous n’avez pas besoin d’utiliser ces noms dans le code F #.</span><span class="sxs-lookup"><span data-stu-id="843e8-127">You do not normally need to use these names in F# code.</span></span>

<span data-ttu-id="843e8-128">Le tableau suivant répertorie les opérateurs standard et les noms générés correspondants.</span><span class="sxs-lookup"><span data-stu-id="843e8-128">The following table shows the standard operators and their corresponding generated names.</span></span>



|<span data-ttu-id="843e8-129">Opérateur</span><span class="sxs-lookup"><span data-stu-id="843e8-129">Operator</span></span>|<span data-ttu-id="843e8-130">Nom généré</span><span class="sxs-lookup"><span data-stu-id="843e8-130">Generated name</span></span>|
|--------|--------------|
|`[]`|`op_Nil`|
|`::`|`op_Cons`|
|`+`|`op_Addition`|
|`-`|`op_Subtraction`|
|`*`|`op_Multiply`|
|`/`|`op_Division`|
|`@`|`op_Append`|
|`^`|`op_Concatenate`|
|`%`|`op_Modulus`|
|`&&&`|`op_BitwiseAnd`|
|<code>&#124;&#124;&#124;</code>|`op_BitwiseOr`|
|`^^^`|`op_ExclusiveOr`|
|`<<<`|`op_LeftShift`|
|`~~~`|`op_LogicalNot`|
|`>>>`|`op_RightShift`|
|`~+`|`op_UnaryPlus`|
|`~-`|`op_UnaryNegation`|
|`=`|`op_Equality`|
|`<=`|`op_LessThanOrEqual`|
|`>=`|`op_GreaterThanOrEqual`|
|`<`|`op_LessThan`|
|`>`|`op_GreaterThan`|
|`?`|`op_Dynamic`|
|`?<-`|`op_DynamicAssignment`|
|<code>&#124;></code>|`op_PipeRight`|
|<code><&#124;</code>|`op_PipeLeft`|
|`!`|`op_Dereference`|
|`>>`|`op_ComposeRight`|
|`<<`|`op_ComposeLeft`|
|`<@ @>`|`op_Quotation`|
|`<@@ @@>`|`op_QuotationUntyped`|
|`+=`|`op_AdditionAssignment`|
|`-=`|`op_SubtractionAssignment`|
|`*=`|`op_MultiplyAssignment`|
|`/=`|`op_DivisionAssignment`|
|`..`|`op_Range`|
|`.. ..`|`op_RangeStep`|
<span data-ttu-id="843e8-131">Autres combinaisons de caractères d’opérateur qui ne sont pas répertoriées ici peuvent être utilisés comme opérateurs d’et ont des noms qui sont obtenus en concaténant les noms de caractères individuels dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="843e8-131">Other combinations of operator characters that are not listed here can be used as operators and have names that are made up by concatenating names for the individual characters from the following table.</span></span> <span data-ttu-id="843e8-132">Par exemple, + !</span><span class="sxs-lookup"><span data-stu-id="843e8-132">For example, +!</span></span> <span data-ttu-id="843e8-133">devient `op_PlusBang`.</span><span class="sxs-lookup"><span data-stu-id="843e8-133">becomes `op_PlusBang`.</span></span>



|<span data-ttu-id="843e8-134">Caractère d’opérateur</span><span class="sxs-lookup"><span data-stu-id="843e8-134">Operator character</span></span>|<span data-ttu-id="843e8-135">Name</span><span class="sxs-lookup"><span data-stu-id="843e8-135">Name</span></span>|
|------------------|----|
|`>`|`Greater`|
|`<`|`Less`|
|`+`|`Plus`|
|`-`|`Minus`|
|`*`|`Multiply`|
|`/`|`Divide`|
|`=`|`Equals`|
|`~`|`Twiddle`|
|`%`|`Percent`|
|`.`|`Dot`|
|`&`|`Amp`|
|<code>&#124;</code>|`Bar`|
|`@`|`At`|
|`^`|`Hat`|
|`!`|`Bang`|
|`?`|`Qmark`|
|`(`|`LParen`|
|`,`|`Comma`|
|`)`|`RParen`|
|`[`|`LBrack`|
|`]`|`RBrack`|

## <a name="prefix-and-infix-operators"></a><span data-ttu-id="843e8-136">Opérateurs préfixés et infixe</span><span class="sxs-lookup"><span data-stu-id="843e8-136">Prefix and Infix Operators</span></span>
<span data-ttu-id="843e8-137">*Préfixe* opérateurs sont supposés être placés devant un ou des opérandes, comme une fonction.</span><span class="sxs-lookup"><span data-stu-id="843e8-137">*Prefix* operators are expected to be placed in front of an operand or operands, much like a function.</span></span> <span data-ttu-id="843e8-138">*Infix* opérateurs sont supposés être placés entre les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="843e8-138">*Infix* operators are expected to be placed between the two operands.</span></span>

<span data-ttu-id="843e8-139">Seuls certains opérateurs peuvent être utilisés comme opérateurs de préfixe.</span><span class="sxs-lookup"><span data-stu-id="843e8-139">Only certain operators can be used as prefix operators.</span></span> <span data-ttu-id="843e8-140">Certains opérateurs sont toujours des opérateurs de préfixe, d’autres peuvent être infixes ou préfixes, et le reste sont toujours des opérateurs infixes.</span><span class="sxs-lookup"><span data-stu-id="843e8-140">Some operators are always prefix operators, others can be infix or prefix, and the rest are always infix operators.</span></span> <span data-ttu-id="843e8-141">Les opérateurs qui commencent par `!`, à l’exception de `!=`et l’opérateur `~`, ou répétées de séquences de`~`, sont toujours des opérateurs de préfixe.</span><span class="sxs-lookup"><span data-stu-id="843e8-141">Operators that begin with `!`, except `!=`, and the operator `~`, or repeated sequences of`~`, are always prefix operators.</span></span> <span data-ttu-id="843e8-142">Les opérateurs `+`, `-`, `+.`, `-.`, `&`, `&&`, `%`, et `%%` peuvent être des opérateurs préfixés ou des opérateurs infixes.</span><span class="sxs-lookup"><span data-stu-id="843e8-142">The operators `+`, `-`, `+.`, `-.`, `&`, `&&`, `%`, and `%%` can be prefix operators or infix operators.</span></span> <span data-ttu-id="843e8-143">Vous distinguez la version préfixée de ces opérateurs à partir de la version infix en ajoutant un `~` au début d’un opérateur préfixé lorsqu’il est défini.</span><span class="sxs-lookup"><span data-stu-id="843e8-143">You distinguish the prefix version of these operators from the infix version by adding a `~` at the beginning of a prefix operator when it is defined.</span></span> <span data-ttu-id="843e8-144">Le `~` n’est pas utilisé lorsque vous utilisez l’opérateur, uniquement lorsqu’il est défini.</span><span class="sxs-lookup"><span data-stu-id="843e8-144">The `~` is not used when you use the operator, only when it is defined.</span></span>

## <a name="example"></a><span data-ttu-id="843e8-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="843e8-145">Example</span></span>

<span data-ttu-id="843e8-146">Le code suivant illustre l’utilisation de la surcharge d’opérateur pour implémenter un type de fraction.</span><span class="sxs-lookup"><span data-stu-id="843e8-146">The following code illustrates the use of operator overloading to implement a fraction type.</span></span> <span data-ttu-id="843e8-147">Une fraction est représentée par un numérateur et dénominateur.</span><span class="sxs-lookup"><span data-stu-id="843e8-147">A fraction is represented by a numerator and a denominator.</span></span> <span data-ttu-id="843e8-148">La fonction `hcf` est utilisée pour déterminer le facteur commun le plus élevé, qui est utilisé pour réduire les fractions.</span><span class="sxs-lookup"><span data-stu-id="843e8-148">The function `hcf` is used to determine the highest common factor, which is used to reduce fractions.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4002.fs)]

<span data-ttu-id="843e8-149">**Sortie :**</span><span class="sxs-lookup"><span data-stu-id="843e8-149">**Output:**</span></span>

```
3/4 + 1/2 = 5/4
3/4 - 1/2 = 1/4
3/4 * 1/2 = 3/8
3/4 / 1/2 = 3/2
3/4 + 1 = 7/4
```

## <a name="operators-at-the-global-level"></a><span data-ttu-id="843e8-150">Opérateurs au niveau Global</span><span class="sxs-lookup"><span data-stu-id="843e8-150">Operators at the Global Level</span></span>
<span data-ttu-id="843e8-151">Vous pouvez également définir des opérateurs au niveau global.</span><span class="sxs-lookup"><span data-stu-id="843e8-151">You can also define operators at the global level.</span></span> <span data-ttu-id="843e8-152">Le code suivant définit un opérateur `+?`.</span><span class="sxs-lookup"><span data-stu-id="843e8-152">The following code defines an operator `+?`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4003.fs)]

<span data-ttu-id="843e8-153">La sortie du code ci-dessus est `12`.</span><span class="sxs-lookup"><span data-stu-id="843e8-153">The output of the above code is `12`.</span></span>

<span data-ttu-id="843e8-154">Vous pouvez redéfinir les opérateurs arithmétiques standards de cette manière, car les règles de portée pour F # exigent que les opérateurs nouvellement définis sont prioritaires sur les opérateurs intégrés.</span><span class="sxs-lookup"><span data-stu-id="843e8-154">You can redefine the regular arithmetic operators in this manner because the scoping rules for F# dictate that newly defined operators take precedence over the built-in operators.</span></span>

<span data-ttu-id="843e8-155">Le mot clé `inline` est souvent utilisé avec des opérateurs globaux, qui sont souvent des petites fonctions qu’il sont préférable d’intégrer dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="843e8-155">The keyword `inline` is often used with global operators, which are often small functions that are best integrated into the calling code.</span></span> <span data-ttu-id="843e8-156">Fonctions d’opérateur fabrication inline permettent également qu’elle fonctionne avec des paramètres de type résolus statiquement à produire du code générique résolu statiquement.</span><span class="sxs-lookup"><span data-stu-id="843e8-156">Making operator functions inline also enables them to work with statically resolved type parameters to produce statically resolved generic code.</span></span> <span data-ttu-id="843e8-157">Pour plus d’informations, consultez [les fonctions Inline](functions/inline-functions.md) et [résolus statiquement les paramètres de Type](generics/statically-resolved-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="843e8-157">For more information, see [Inline Functions](functions/inline-functions.md) and [Statically Resolved Type Parameters](generics/statically-resolved-type-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="843e8-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="843e8-158">See Also</span></span>
[<span data-ttu-id="843e8-159">Membres</span><span class="sxs-lookup"><span data-stu-id="843e8-159">Members</span></span>](members/index.md)
