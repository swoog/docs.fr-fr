---
title: Introduction à la programmation fonctionnelle en F#
description: Découvrez les principes fondamentaux de la programmation fonctionnelle dans F#.
ms.date: 10/29/2018
ms.openlocfilehash: d4a9bb0cd826b41aca96e12e2bcb5aab80c18eb4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25724476"
---
# <a name="introduction-to-functional-programming-in-f"></a><span data-ttu-id="eb815-103">Introduction à la programmation fonctionnelle en F#</span><span class="sxs-lookup"><span data-stu-id="eb815-103">Introduction to Functional Programming in F#</span></span> #

<span data-ttu-id="eb815-104">Programmation fonctionnelle est un style de programmation qui met l’accent sur l’utilisation de fonctions et données immuables.</span><span class="sxs-lookup"><span data-stu-id="eb815-104">Functional programming is a style of programming that emphasizes the use of functions and immutable data.</span></span> <span data-ttu-id="eb815-105">Programmation fonctionnelle typée est lors de la programmation fonctionnelle est combinée avec des types statiques, telles que F#.</span><span class="sxs-lookup"><span data-stu-id="eb815-105">Typed functional programming is when functional programming is combined with static types, such as with F#.</span></span> <span data-ttu-id="eb815-106">En règle générale, les concepts suivants sont mis en évidence dans la programmation fonctionnelle :</span><span class="sxs-lookup"><span data-stu-id="eb815-106">In general, the following concepts are emphasized in functional programming:</span></span>

* <span data-ttu-id="eb815-107">Fonctions en tant que les constructions principales que vous utilisez</span><span class="sxs-lookup"><span data-stu-id="eb815-107">Functions as the primary constructs you use</span></span>
* <span data-ttu-id="eb815-108">Expressions au lieu d’instructions</span><span class="sxs-lookup"><span data-stu-id="eb815-108">Expressions instead of statements</span></span>
* <span data-ttu-id="eb815-109">Valeurs immuables sur les variables</span><span class="sxs-lookup"><span data-stu-id="eb815-109">Immutable values over variables</span></span>
* <span data-ttu-id="eb815-110">Programmation déclarative sur la programmation impérative</span><span class="sxs-lookup"><span data-stu-id="eb815-110">Declarative programming over imperative programming</span></span>

<span data-ttu-id="eb815-111">Tout au long de cette série, vous allez découvrir les concepts et modèles de programmation fonctionnelle à l’aide de F#.</span><span class="sxs-lookup"><span data-stu-id="eb815-111">Throughout this series, you'll explore concepts and patterns in functional programming using F#.</span></span> <span data-ttu-id="eb815-112">Tout au long du processus, vous découvrirez certaines F# trop.</span><span class="sxs-lookup"><span data-stu-id="eb815-112">Along the way, you'll learn some F# too.</span></span>

## <a name="terminology"></a><span data-ttu-id="eb815-113">Terminologie</span><span class="sxs-lookup"><span data-stu-id="eb815-113">Terminology</span></span>

<span data-ttu-id="eb815-114">Programmation fonctionnelle, telles que d’autres paradigmes de programmation est fourni avec un vocabulaire dont vous aurez besoin par la suite pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="eb815-114">Functional programming, like other programming paradigms, comes with a vocabulary that you will eventually need to learn.</span></span> <span data-ttu-id="eb815-115">Voici certains termes courants, vous verrez tout le temps :</span><span class="sxs-lookup"><span data-stu-id="eb815-115">Here are some common terms you'll see all of the time:</span></span>

* <span data-ttu-id="eb815-116">**Fonction** -une fonction est une construction qui produit une sortie en fonction d’une entrée.</span><span class="sxs-lookup"><span data-stu-id="eb815-116">**Function** - A function is a construct that will produce an output when given an input.</span></span> <span data-ttu-id="eb815-117">Plus formellement, il _mappe_ un élément à partir d’une valeur à un autre ensemble.</span><span class="sxs-lookup"><span data-stu-id="eb815-117">More formally, it _maps_ an item from one set to another set.</span></span> <span data-ttu-id="eb815-118">Cette formalisme est capturée dans la concret dans bien des égards, surtout lorsque vous utilisez des fonctions qui opèrent sur des collections de données.</span><span class="sxs-lookup"><span data-stu-id="eb815-118">This formalism is lifted into the concrete in many ways, especially when using functions that operate on collections of data.</span></span> <span data-ttu-id="eb815-119">Il est le meilleur parti des concept de base (et important) dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-119">It is the most basic (and important) concept in functional programming.</span></span> 
* <span data-ttu-id="eb815-120">**Expression** -une expression est une construction dans le code qui génère une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-120">**Expression** - An expression is a construct in code that produces a value.</span></span> <span data-ttu-id="eb815-121">Dans F#, cette valeur doit être liée ou explicitement ignorée.</span><span class="sxs-lookup"><span data-stu-id="eb815-121">In F#, this value must be bound or explicitly ignored.</span></span> <span data-ttu-id="eb815-122">Une expression peut être simplement remplacée par un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="eb815-122">An expression can be trivially replaced by a function call.</span></span>
* <span data-ttu-id="eb815-123">**Pureté** -pureté est une propriété d’une fonction telle que sa valeur de retour est toujours le même pour les mêmes arguments, et que son évaluation n’a aucun effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="eb815-123">**Purity** - Purity is a property of a function such that its return value is always the same for the same arguments, and that its evaluation has no side effects.</span></span> <span data-ttu-id="eb815-124">Une fonction pure dépend entièrement de ses arguments.</span><span class="sxs-lookup"><span data-stu-id="eb815-124">A pure function depends entirely on its arguments.</span></span>
* <span data-ttu-id="eb815-125">**Transparence référentielle** -transparence référentielle est une propriété des expressions telles qu’elles puissent être remplacées sans affecter le comportement d’un programme avec leur sortie.</span><span class="sxs-lookup"><span data-stu-id="eb815-125">**Referential Transparency** - Referential Transparency is a property of expressions such that they can be replaced with their output without affecting a program's behavior.</span></span>
* <span data-ttu-id="eb815-126">**Immuabilité** -signifie d’immuabilité qu’une valeur ne peut pas être modifié sur place.</span><span class="sxs-lookup"><span data-stu-id="eb815-126">**Immutability** - Immutability means that a value cannot be changed in-place.</span></span> <span data-ttu-id="eb815-127">Ceci est le contraire des variables qui peuvent changer en place.</span><span class="sxs-lookup"><span data-stu-id="eb815-127">This is in contrast with variables, which can change in place.</span></span>

## <a name="examples"></a><span data-ttu-id="eb815-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb815-128">Examples</span></span>

<span data-ttu-id="eb815-129">Les exemples suivants illustrent ces concepts fondamentaux.</span><span class="sxs-lookup"><span data-stu-id="eb815-129">The following examples demonstrate these core concepts.</span></span>

### <a name="functions"></a><span data-ttu-id="eb815-130">Fonctions</span><span class="sxs-lookup"><span data-stu-id="eb815-130">Functions</span></span>

<span data-ttu-id="eb815-131">Les plus courantes et fondamentale de programmation fonctionnelle est la fonction.</span><span class="sxs-lookup"><span data-stu-id="eb815-131">The most common and fundamental construct in functional programming is the function.</span></span> <span data-ttu-id="eb815-132">Voici une fonction simple qui ajoute 1 à un entier :</span><span class="sxs-lookup"><span data-stu-id="eb815-132">Here's a simple function that adds 1 to an integer:</span></span>

```fsharp
let addOne x = x + 1
```

<span data-ttu-id="eb815-133">Sa signature de type est la suivante :</span><span class="sxs-lookup"><span data-stu-id="eb815-133">Its type signature is as follows:</span></span>

```fsharp
val addOne: x:int -> int
```

<span data-ttu-id="eb815-134">La signature peut être lu comme, «`addOne` accepte un `int` nommé `x` et produira un `int`».</span><span class="sxs-lookup"><span data-stu-id="eb815-134">The signature can be read as, "`addOne` accepts an `int` named `x` and will produce an `int`".</span></span> <span data-ttu-id="eb815-135">Plus formellement, `addOne` est _mappage_ une valeur de l’ensemble d’entiers à l’ensemble d’entiers.</span><span class="sxs-lookup"><span data-stu-id="eb815-135">More formally, `addOne` is _mapping_ a value from the set of integers to the set of integers.</span></span> <span data-ttu-id="eb815-136">Le `->` jeton désigne ce mappage.</span><span class="sxs-lookup"><span data-stu-id="eb815-136">The `->` token signifies this mapping.</span></span> <span data-ttu-id="eb815-137">Dans F#, vous pouvez généralement consulter la signature de fonction pour obtenir une idée de ce qu’il fait.</span><span class="sxs-lookup"><span data-stu-id="eb815-137">In F#, you can usually look at the function signature to get a sense for what it does.</span></span>

<span data-ttu-id="eb815-138">Par conséquent, pourquoi est-la signature important ?</span><span class="sxs-lookup"><span data-stu-id="eb815-138">So, why is the signature important?</span></span> <span data-ttu-id="eb815-139">Dans la programmation fonctionnelle typée, l’implémentation d’une fonction est souvent moins importante que la signature de type réel !</span><span class="sxs-lookup"><span data-stu-id="eb815-139">In typed functional programming, the implementation of a function is often less important than the actual type signature!</span></span> <span data-ttu-id="eb815-140">Le fait que `addOne` ajoute la valeur 1 à un entier est intéressante lors de l’exécution, mais lorsque vous construisez un programme, le fait qu’il accepte et retourne un `int` est ce qui indique comment vous allez utiliser réellement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="eb815-140">The fact that `addOne` adds the value 1 to an integer is interesting at runtime, but when you are constructing a program, the fact that it accepts and returns an `int` is what informs how you will actually use this function.</span></span> <span data-ttu-id="eb815-141">En outre, une fois que vous utilisez cette fonction correctement (par rapport à sa signature de type), diagnostiquer des problèmes est possible uniquement dans le corps de la `addOne` (fonction).</span><span class="sxs-lookup"><span data-stu-id="eb815-141">Furthermore, once you use this function correctly (with respect to its type signature), diagnosing any problems can be done only within the body of the `addOne` function.</span></span> <span data-ttu-id="eb815-142">Il s’agit de l’idée derrière la programmation fonctionnelle typée.</span><span class="sxs-lookup"><span data-stu-id="eb815-142">This is the impetus behind typed functional programming.</span></span>

### <a name="expressions"></a><span data-ttu-id="eb815-143">Expressions</span><span class="sxs-lookup"><span data-stu-id="eb815-143">Expressions</span></span>

<span data-ttu-id="eb815-144">Les expressions sont des constructions qui donnent comme résultat une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-144">Expressions are constructs that evaluate to a value.</span></span> <span data-ttu-id="eb815-145">Contrairement aux instructions qui effectuent une action, les expressions peuvent être considérées d’effectuer une action qui renvoie une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-145">In contrast to statements, which perform an action, expressions can be thought of performing an action that gives back a value.</span></span> <span data-ttu-id="eb815-146">Les expressions sont presque toujours utilisées en faveur des instructions dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-146">Expressions are almost always used in favor of statements in functional programming.</span></span>

<span data-ttu-id="eb815-147">Considérez la fonction précédente, `addOne`.</span><span class="sxs-lookup"><span data-stu-id="eb815-147">Consider the previous function, `addOne`.</span></span> <span data-ttu-id="eb815-148">Le corps de `addOne` est une expression :</span><span class="sxs-lookup"><span data-stu-id="eb815-148">The body of `addOne` is an expression:</span></span>

```fsharp
// 'x + 1' is an expression!
let addOne x = x + 1
```

<span data-ttu-id="eb815-149">Il est le résultat de cette expression qui définit le type de résultat de la `addOne` (fonction).</span><span class="sxs-lookup"><span data-stu-id="eb815-149">It is the result of this expression that defines the result type of the `addOne` function.</span></span> <span data-ttu-id="eb815-150">Par exemple, l’expression de cette fonction peut être changée pour être un type différent, comme un `string`:</span><span class="sxs-lookup"><span data-stu-id="eb815-150">For example, the expression that makes up this function could be changed to be a different type, such as a `string`:</span></span>

```fsharp
let addOne x = x.ToString() + "1"
```

<span data-ttu-id="eb815-151">La signature de la fonction est désormais :</span><span class="sxs-lookup"><span data-stu-id="eb815-151">The signature of the function is now:</span></span>

```fsharp
val addOne: x:'a -> string
```

<span data-ttu-id="eb815-152">Depuis n’importe quel type dans F# peut avoir `ToString()` appelé dessus, le type de `x` soit devenue générique (appelé [généralisation automatique](../language-reference/generics/automatic-generalization.md)), et le type résultant est un `string`.</span><span class="sxs-lookup"><span data-stu-id="eb815-152">Since any type in F# can have `ToString()` called on it, the type of `x` has been made generic (called [Automatic Generalization](../language-reference/generics/automatic-generalization.md)), and the resultant type is a `string`.</span></span>

<span data-ttu-id="eb815-153">Les expressions ne sont pas simplement les corps des fonctions.</span><span class="sxs-lookup"><span data-stu-id="eb815-153">Expressions are not just the bodies of functions.</span></span> <span data-ttu-id="eb815-154">Vous pouvez avoir des expressions qui produisent une valeur que vous utilisez un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="eb815-154">You can have expressions that produce a value you use elsewhere.</span></span> <span data-ttu-id="eb815-155">Un commun un est `if`:</span><span class="sxs-lookup"><span data-stu-id="eb815-155">A common one is `if`:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result
```

<span data-ttu-id="eb815-156">Le `if` expression produit une valeur appelée `result`.</span><span class="sxs-lookup"><span data-stu-id="eb815-156">The `if` expression produces a value called `result`.</span></span> <span data-ttu-id="eb815-157">Notez que vous pourriez omettre `result` entièrement, ce qui le `if` le corps d’expression de la `addOneIfOdd` (fonction).</span><span class="sxs-lookup"><span data-stu-id="eb815-157">Note that you could omit `result` entirely, making the `if` expression the body of the `addOneIfOdd` function.</span></span> <span data-ttu-id="eb815-158">Le point clé à retenir sur les expressions est qu’elles produisent une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-158">The key thing to remember about expressions is that they produce a value.</span></span>

<span data-ttu-id="eb815-159">Il existe un type spécial, `unit`, qui est utilisé lorsqu’il n’y a rien à retourner.</span><span class="sxs-lookup"><span data-stu-id="eb815-159">There is a special type, `unit`, that is used when there is nothing to return.</span></span> <span data-ttu-id="eb815-160">Par exemple, considérez cette fonction simple :</span><span class="sxs-lookup"><span data-stu-id="eb815-160">For example, consider this simple function:</span></span>

```fsharp
let printString (str: string) =
    printfn "String is: %s" s
```

<span data-ttu-id="eb815-161">La signature se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="eb815-161">The signature looks like this:</span></span>

```fsharp
val printString: str:string -> unit
```

<span data-ttu-id="eb815-162">Le `unit` type indique qu’il n’existe aucune valeur réelle retournée.</span><span class="sxs-lookup"><span data-stu-id="eb815-162">The `unit` type indicates that there is no actual value being returned.</span></span> <span data-ttu-id="eb815-163">Cela est utile lorsque vous avez une routine qui doit « fonctionnent-elles » bien ne qu’aucune valeur de retour à la suite de ce travail.</span><span class="sxs-lookup"><span data-stu-id="eb815-163">This is useful when you have a routine that must "do work" despite having no value to return as a result of that work.</span></span>

<span data-ttu-id="eb815-164">Cela se démarque de la programmation impérative, où l’équivalent `if` construction est une instruction, et produire des valeurs est souvent effectuée avec des variables de mutation.</span><span class="sxs-lookup"><span data-stu-id="eb815-164">This is in sharp contrast to imperative programming, where the equivalent `if` construct is a statement, and producing values is often done with mutating variables.</span></span> <span data-ttu-id="eb815-165">Par exemple, dans C#, le code peut être écrit comme suit :</span><span class="sxs-lookup"><span data-stu-id="eb815-165">For example, in C#, the code might be written like this:</span></span>

```csharp
bool IsOdd(int x) => x % 2 != 0;

int AddOneIfOdd(int input)
{
    var result = input;

    if (IsOdd(input))
    {
        result = input + 1;
    }

    return result;
}
```

<span data-ttu-id="eb815-166">Il est important de souligner que C# et d’autres langages de style C ne prennent pas en charge la [expression ternaire](../../csharp/language-reference/operators/conditional-operator.md), ce qui permet la programmation basée sur une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-166">It's worth noting that C# and other C-style languages do support the [ternary expression](../../csharp/language-reference/operators/conditional-operator.md), which allows for expression-based conditional programming.</span></span>

<span data-ttu-id="eb815-167">Dans la programmation fonctionnelle, il est rare de muter les valeurs avec des instructions.</span><span class="sxs-lookup"><span data-stu-id="eb815-167">In functional programming, it is rare to mutate values with statements.</span></span> <span data-ttu-id="eb815-168">Bien que certains langages fonctionnels prennent en charge les instructions et une mutation, il n’est pas courant d’utiliser ces concepts dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-168">Although some functional languages support statements and mutation, it is not common to use these concepts in functional programming.</span></span>

### <a name="pure-functions"></a><span data-ttu-id="eb815-169">Fonctions pures</span><span class="sxs-lookup"><span data-stu-id="eb815-169">Pure functions</span></span>

<span data-ttu-id="eb815-170">Comme mentionnées précédemment, pures fonctions sont les fonctions qui :</span><span class="sxs-lookup"><span data-stu-id="eb815-170">As previously mentioned, pure functions are functions that:</span></span>

* <span data-ttu-id="eb815-171">Évaluez toujours la même valeur pour la même entrée.</span><span class="sxs-lookup"><span data-stu-id="eb815-171">Always evaluate to the same value for the same input.</span></span>
* <span data-ttu-id="eb815-172">N’ont aucun effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="eb815-172">Have no side effects.</span></span>

<span data-ttu-id="eb815-173">Il est utile de considérer les fonctions mathématiques dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="eb815-173">It is helpful to think of mathematical functions in this context.</span></span> <span data-ttu-id="eb815-174">En mathématique, les fonctions dépendent uniquement de leurs arguments et n’ont pas d’effets secondaires.</span><span class="sxs-lookup"><span data-stu-id="eb815-174">In mathematics, functions depend only on their arguments and do not have any side effects.</span></span> <span data-ttu-id="eb815-175">Dans la fonction mathématique `f(x) = x + 1`, la valeur de `f(x)` dépend uniquement de la valeur de `x`.</span><span class="sxs-lookup"><span data-stu-id="eb815-175">In the mathematical function `f(x) = x + 1`, the value of `f(x)` depends only on the value of `x`.</span></span> <span data-ttu-id="eb815-176">Dans la programmation fonctionnelle, les fonctions pures sont la même façon.</span><span class="sxs-lookup"><span data-stu-id="eb815-176">Pure functions in functional programming are the same way.</span></span>

<span data-ttu-id="eb815-177">Lorsque vous écrivez une fonction pure, la fonction doit dépendre uniquement de ses arguments et pas effectuer toute action qui entraîne un effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="eb815-177">When writing a pure function, the function must depend only on its arguments and not perform any action that results in a side effect.</span></span>

<span data-ttu-id="eb815-178">Voici un exemple d’une fonction non pure, car elle dépend d’état global et mutable :</span><span class="sxs-lookup"><span data-stu-id="eb815-178">Here is an example of a non-pure function because it depends on global, mutable state:</span></span>

```fsharp
let mutable value = 1

let addOneToValue x = x + value
```

<span data-ttu-id="eb815-179">Le `addOneToValue` fonction est clairement impure, étant donné que `value` peut être changé à tout moment pour avoir une valeur différente de 1.</span><span class="sxs-lookup"><span data-stu-id="eb815-179">The `addOneToValue` function is clearly impure, because `value` could be changed at any time to have a different value than 1.</span></span> <span data-ttu-id="eb815-180">Ce modèle de selon une valeur globale doit être évitée dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-180">This pattern of depending on a global value is to be avoided in functional programming.</span></span>

<span data-ttu-id="eb815-181">Voici un autre exemple d’une fonction non pure, car elle effectue un effet secondaire :</span><span class="sxs-lookup"><span data-stu-id="eb815-181">Here is another example of a non-pure function, because it performs a side effect:</span></span>

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

<span data-ttu-id="eb815-182">Bien que cette fonction ne repose pas sur une valeur globale, il écrit la valeur de `x` à la sortie du programme.</span><span class="sxs-lookup"><span data-stu-id="eb815-182">Although this function does not depend on a global value, it writes the value of `x` to the output of the program.</span></span> <span data-ttu-id="eb815-183">Bien qu’il n’a rien de choquant dans cette opération, cela signifie que la fonction n’est pas pure.</span><span class="sxs-lookup"><span data-stu-id="eb815-183">Although there is nothing inherently wrong with doing this, it does mean that the function is not pure.</span></span>

<span data-ttu-id="eb815-184">Suppression de la `printfn` instruction rend enfin la fonction pure :</span><span class="sxs-lookup"><span data-stu-id="eb815-184">Removing the `printfn` statement finally makes the function pure:</span></span>

```fsharp
let addOneToValue x = x + 1
```

<span data-ttu-id="eb815-185">Bien que cette fonction n’est pas fondamentalement _mieux_ que la version précédente avec la `printfn` instruction, cela ne garantit que cette fonction n’est retournent une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-185">Although this function is not inherently _better_ than the previous version with the `printfn` statement, it does guarantee that all this function does is return a value.</span></span> <span data-ttu-id="eb815-186">Si vous appelez cette fonction une fois ou milliards de fois 1 sera toujours résultat dans la même chose : production simplement une valeur.</span><span class="sxs-lookup"><span data-stu-id="eb815-186">Calling this function once or 1 billion times will still result in the same thing: just producing a value.</span></span> <span data-ttu-id="eb815-187">Cette prévisibilité est utile dans la programmation fonctionnelle, car cela signifie que n’importe quelle fonction pure est assortie transparente.</span><span class="sxs-lookup"><span data-stu-id="eb815-187">This predictability is valuable in functional programming, as it means that any pure function is referentially transparent.</span></span>

### <a name="referential-transparency"></a><span data-ttu-id="eb815-188">Transparence référentielle</span><span class="sxs-lookup"><span data-stu-id="eb815-188">Referential Transparency</span></span>

<span data-ttu-id="eb815-189">Transparence référentielle est une propriété d’expressions et fonctions.</span><span class="sxs-lookup"><span data-stu-id="eb815-189">Referential transparency is a property of expressions and functions.</span></span> <span data-ttu-id="eb815-190">Pour une expression à être assortie transparent, il doit pouvoir être remplacé par sa valeur résultante sans modifier le déroulement du programme.</span><span class="sxs-lookup"><span data-stu-id="eb815-190">For an expression to be referentially transparent, it must be able to be replaced with its resulting value without changing the program's behavior.</span></span> <span data-ttu-id="eb815-191">Toutes les fonctions pures sont assortie transparentes.</span><span class="sxs-lookup"><span data-stu-id="eb815-191">All pure functions are referentially transparent.</span></span>

<span data-ttu-id="eb815-192">Comme les fonctions pures, il peut être utile de considérer une transparence référentielle à partir d’un point de vue mathématique.</span><span class="sxs-lookup"><span data-stu-id="eb815-192">As with pure functions, it can be helpful to think of referential transparency from a mathematical perspective.</span></span> <span data-ttu-id="eb815-193">Dans l’expression mathématique `y = f(x)`, `f(x)` peut être remplacé par le résultat de la fonction et il sera toujours égal à `y`.</span><span class="sxs-lookup"><span data-stu-id="eb815-193">In the mathematical expression `y = f(x)`, `f(x)` can be replaced by the result of the function and it will still be equal to `y`.</span></span> <span data-ttu-id="eb815-194">Cela vaut également pour la transparence référentielle dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-194">This is equally true for referential transparency in functional programming.</span></span>

<span data-ttu-id="eb815-195">Appelez défini précédemment `addOneIfOdd` fonctionner deux fois :</span><span class="sxs-lookup"><span data-stu-id="eb815-195">Consider calling the previously defined `addOneIfOdd` function twice:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result

let res1 = addOneIffOdd 1 // Produces 2
let res2 = addOneIffOdd 2 // Produces 2
```

<span data-ttu-id="eb815-196">Nous pouvons remplacer chaque appel de fonction avec le corps de fonction, en remplaçant l’argument `input` avec chaque valeur :</span><span class="sxs-lookup"><span data-stu-id="eb815-196">We can replace each function call with the function body, substituting the argument `input` with each value:</span></span>

```fsharp
// Checks if 'x' is odd by using the mod operator
let isOdd x = x % 2 <> 0

let addOneIfOdd input =
    let result =
        if isOdd input then
            input + 1
        else
            input

    result

let res1 =
    let result =
        if isOdd 1 then
            1 + 1
        else
            1

    result
let res2 =
    let result =
        if isOdd 2 then
            2 + 1
        else
            2

    result
```

<span data-ttu-id="eb815-197">Les deux `res1` et `res2` ont la même valeur que si la fonction a été appelée, ce qui indique que `addOneIfOdd` est assortie transparent !</span><span class="sxs-lookup"><span data-stu-id="eb815-197">Both `res1` and `res2` have the same value as if the function was called, indicating that `addOneIfOdd` is referentially transparent!</span></span>

<span data-ttu-id="eb815-198">En outre, une fonction ne doit pas être pure également être assortie transparent.</span><span class="sxs-lookup"><span data-stu-id="eb815-198">Additionally, a function doesn't have to be pure to also be referentially transparent.</span></span> <span data-ttu-id="eb815-199">Examinez une définition précédente de `addOneTovalue`:</span><span class="sxs-lookup"><span data-stu-id="eb815-199">Consider a previous definition of  `addOneTovalue`:</span></span>

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

<span data-ttu-id="eb815-200">Un appel à cette fonction peut également être remplacé par son corps et la même chose se produit chaque fois :</span><span class="sxs-lookup"><span data-stu-id="eb815-200">Any call to this function can also be replaced by its body and the same things will happen each time:</span></span>

* <span data-ttu-id="eb815-201">La valeur, avant son ajout à, est affichée à la sortie</span><span class="sxs-lookup"><span data-stu-id="eb815-201">The value, prior to being added to, is printed to the output</span></span>
* <span data-ttu-id="eb815-202">La valeur a 1 ajouté</span><span class="sxs-lookup"><span data-stu-id="eb815-202">The value has 1 added to it</span></span>

<span data-ttu-id="eb815-203">Lorsque vous programmez en F#, il est souvent la transparence référentielle qui est l’objectif, plutôt que de pureté.</span><span class="sxs-lookup"><span data-stu-id="eb815-203">When programming in F#, it is often referential transparency that is the goal, rather than purity.</span></span> <span data-ttu-id="eb815-204">Toutefois, il est toujours conseillé d’écrire des fonctions pures dès que possible.</span><span class="sxs-lookup"><span data-stu-id="eb815-204">However, it is still good practice to write pure functions when you can.</span></span>

### <a name="immutability"></a><span data-ttu-id="eb815-205">Immuabilité</span><span class="sxs-lookup"><span data-stu-id="eb815-205">Immutability</span></span>

<span data-ttu-id="eb815-206">Enfin, un des concepts plus fondamentaux de la programmation fonctionnelle typée consiste immuabilité.</span><span class="sxs-lookup"><span data-stu-id="eb815-206">Finally, one of the most fundamental concepts of typed functional programming is immutability.</span></span> <span data-ttu-id="eb815-207">Dans F#, toutes les valeurs sont immuables par défaut.</span><span class="sxs-lookup"><span data-stu-id="eb815-207">In F#, all values are immutable by default.</span></span> <span data-ttu-id="eb815-208">Cela signifie qu’ils ne peut pas être muter sur place, sauf si vous les marquez comme mutables.</span><span class="sxs-lookup"><span data-stu-id="eb815-208">That means they cannot be mutated in-place unless you explicitly mark them as mutable.</span></span>

<span data-ttu-id="eb815-209">Dans la pratique, travailler avec des valeurs immuables signifie que vous remplacez votre approche de programmation, « Je dois modifier quelque chose » à « j’ai besoin produire une nouvelle valeur ».</span><span class="sxs-lookup"><span data-stu-id="eb815-209">In practice, working with immutable values means that you change your approach to programming from, "I need to change something", to "I need to produce a new value".</span></span>

<span data-ttu-id="eb815-210">Par exemple, ajout de 1 à une valeur signifie produisant une nouvelle valeur, ne pas de mutation existant :</span><span class="sxs-lookup"><span data-stu-id="eb815-210">For example, adding 1 to a value means producing a new value, not mutating the existing one:</span></span>

```fsharp
let value = 1
let secondValue = value + 1
```

<span data-ttu-id="eb815-211">Dans F#, le code suivant effectue **pas** muter le `value` fonction ; au lieu de cela, il effectue une vérification de l’égalité :</span><span class="sxs-lookup"><span data-stu-id="eb815-211">In F#, the following code does **not** mutate the `value` function; instead, it performs an equality check:</span></span>

```fsharp
let value = 1
value = value + 1 // Produces a 'bool' value!
```

<span data-ttu-id="eb815-212">Certains langages de programmation fonctionnelles ne gèrent pas mutation.</span><span class="sxs-lookup"><span data-stu-id="eb815-212">Some functional programming languages do not support mutation at all.</span></span> <span data-ttu-id="eb815-213">Dans F#, il est pris en charge, mais il n’est pas le comportement par défaut pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="eb815-213">In F#, it is supported, but it is not the default behavior for values.</span></span>

<span data-ttu-id="eb815-214">Ce concept s’étend même jusqu'à proposer des structures de données.</span><span class="sxs-lookup"><span data-stu-id="eb815-214">This concept extends even further to data structures.</span></span> <span data-ttu-id="eb815-215">Dans la programmation fonctionnelle, les structures de données immuables telles que les jeux (et bien plus encore) ait une implémentation différente que vous pouvez initialement prévu.</span><span class="sxs-lookup"><span data-stu-id="eb815-215">In functional programming, immutable data structures such as sets (and many more) have a different implementation than you might initially expect.</span></span> <span data-ttu-id="eb815-216">Conceptuellement, un tel ajout d’un élément à un ensemble ne modifie pas le jeu, il génère un _nouveau_ définie avec la valeur ajoutée.</span><span class="sxs-lookup"><span data-stu-id="eb815-216">Conceptually, something like adding an item to a set does not change the set, it produces a _new_ set with the added value.</span></span> <span data-ttu-id="eb815-217">En coulisses, souvent cela par une structure de données différente qui permet de suivre efficacement une valeur pour que la représentation appropriée des données peut être donnée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="eb815-217">Under the covers, this is often accomplished by a different data structure that allows for efficiently tracking a value so that the appropriate representation of the data can be given as a result.</span></span>

<span data-ttu-id="eb815-218">Ce style de l’utilisation de valeurs et les structures de données est cruciale, car il vous permet de traiter toute opération qui modifie quelque chose comme s’il crée une nouvelle version de ceci force.</span><span class="sxs-lookup"><span data-stu-id="eb815-218">This style of working with values and data structures is critical, as it forces you to treat any operation that modifies something as if it creates a new version of that thing.</span></span> <span data-ttu-id="eb815-219">Cela permet à des éléments comme l’égalité et d’infériorité être cohérents dans vos programmes.</span><span class="sxs-lookup"><span data-stu-id="eb815-219">This allows for things like equality and comparability to be consistent in your programs.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eb815-220">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eb815-220">Next steps</span></span>

<span data-ttu-id="eb815-221">La section suivante couvre soigneusement les fonctions, exploration de différentes façons, vous pouvez les utiliser dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="eb815-221">The next section will thoroughly cover functions, exploring different ways you can use them in functional programming.</span></span>

<span data-ttu-id="eb815-222">[Fonctions de première classe](first-class-functions.md) explore les fonctions profondément, montrant comment vous pouvez les utiliser dans différents contextes.</span><span class="sxs-lookup"><span data-stu-id="eb815-222">[First-class functions](first-class-functions.md) explores functions deeply, showing how you can use them in various contexts.</span></span>

## <a name="further-reading"></a><span data-ttu-id="eb815-223">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="eb815-223">Further reading</span></span>

<span data-ttu-id="eb815-224">Le [penser fonctionnellement](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) série est également une excellente ressource pour en savoir plus sur la programmation fonctionnelle avec F#.</span><span class="sxs-lookup"><span data-stu-id="eb815-224">The [Thinking Functionally](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) series is another great resource to learn about functional programming with F#.</span></span> <span data-ttu-id="eb815-225">Il couvre les notions de base de la programmation fonctionnelle de façon pragmatique et facile à lire, à l’aide de F# fonctionnalités pour illustrer les concepts.</span><span class="sxs-lookup"><span data-stu-id="eb815-225">It covers fundamentals of functional programming in a pragmatic and easy-to-read way, using F# features to illustrate the concepts.</span></span>