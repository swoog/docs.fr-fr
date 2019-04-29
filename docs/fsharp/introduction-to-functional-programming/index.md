---
title: Introduction à la programmation fonctionnelle en F#
description: Découvrez les principes fondamentaux de la programmation fonctionnelle dans F#.
ms.date: 10/29/2018
ms.openlocfilehash: 84022e58c0f17b9e9875402c653c31e494e940da
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772786"
---
# <a name="introduction-to-functional-programming-in-f"></a><span data-ttu-id="fe5d2-103">Introduction à la programmation fonctionnelle en F\#</span><span class="sxs-lookup"><span data-stu-id="fe5d2-103">Introduction to Functional Programming in F\#</span></span>

<span data-ttu-id="fe5d2-104">Programmation fonctionnelle est un style de programmation qui met l’accent sur l’utilisation de fonctions et données immuables.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-104">Functional programming is a style of programming that emphasizes the use of functions and immutable data.</span></span> <span data-ttu-id="fe5d2-105">Programmation fonctionnelle typée est lors de la programmation fonctionnelle est combinée avec des types statiques, telles que F#.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-105">Typed functional programming is when functional programming is combined with static types, such as with F#.</span></span> <span data-ttu-id="fe5d2-106">En règle générale, les concepts suivants sont mis en évidence dans la programmation fonctionnelle :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-106">In general, the following concepts are emphasized in functional programming:</span></span>

* <span data-ttu-id="fe5d2-107">Fonctions en tant que les constructions principales que vous utilisez</span><span class="sxs-lookup"><span data-stu-id="fe5d2-107">Functions as the primary constructs you use</span></span>
* <span data-ttu-id="fe5d2-108">Expressions au lieu d’instructions</span><span class="sxs-lookup"><span data-stu-id="fe5d2-108">Expressions instead of statements</span></span>
* <span data-ttu-id="fe5d2-109">Valeurs immuables sur les variables</span><span class="sxs-lookup"><span data-stu-id="fe5d2-109">Immutable values over variables</span></span>
* <span data-ttu-id="fe5d2-110">Programmation déclarative sur la programmation impérative</span><span class="sxs-lookup"><span data-stu-id="fe5d2-110">Declarative programming over imperative programming</span></span>

<span data-ttu-id="fe5d2-111">Tout au long de cette série, vous allez découvrir les concepts et modèles de programmation fonctionnelle à l’aide de F#.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-111">Throughout this series, you'll explore concepts and patterns in functional programming using F#.</span></span> <span data-ttu-id="fe5d2-112">Tout au long du processus, vous découvrirez certaines F# trop.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-112">Along the way, you'll learn some F# too.</span></span>

## <a name="terminology"></a><span data-ttu-id="fe5d2-113">Terminologie</span><span class="sxs-lookup"><span data-stu-id="fe5d2-113">Terminology</span></span>

<span data-ttu-id="fe5d2-114">Programmation fonctionnelle, telles que d’autres paradigmes de programmation est fourni avec un vocabulaire dont vous aurez besoin par la suite pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-114">Functional programming, like other programming paradigms, comes with a vocabulary that you will eventually need to learn.</span></span> <span data-ttu-id="fe5d2-115">Voici certains termes courants, vous verrez tout le temps :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-115">Here are some common terms you'll see all of the time:</span></span>

* <span data-ttu-id="fe5d2-116">**Fonction** -une fonction est une construction qui produit une sortie en fonction d’une entrée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-116">**Function** - A function is a construct that will produce an output when given an input.</span></span> <span data-ttu-id="fe5d2-117">Plus formellement, il _mappe_ un élément à partir d’une valeur à un autre ensemble.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-117">More formally, it _maps_ an item from one set to another set.</span></span> <span data-ttu-id="fe5d2-118">Cette formalisme est capturée dans la concret dans bien des égards, surtout lorsque vous utilisez des fonctions qui opèrent sur des collections de données.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-118">This formalism is lifted into the concrete in many ways, especially when using functions that operate on collections of data.</span></span> <span data-ttu-id="fe5d2-119">Il est le meilleur parti des concept de base (et important) dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-119">It is the most basic (and important) concept in functional programming.</span></span> 
* <span data-ttu-id="fe5d2-120">**Expression** -une expression est une construction dans le code qui génère une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-120">**Expression** - An expression is a construct in code that produces a value.</span></span> <span data-ttu-id="fe5d2-121">Dans F#, cette valeur doit être liée ou explicitement ignorée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-121">In F#, this value must be bound or explicitly ignored.</span></span> <span data-ttu-id="fe5d2-122">Une expression peut être simplement remplacée par un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-122">An expression can be trivially replaced by a function call.</span></span>
* <span data-ttu-id="fe5d2-123">**Pureté** -pureté est une propriété d’une fonction telle que sa valeur de retour est toujours le même pour les mêmes arguments, et que son évaluation n’a aucun effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-123">**Purity** - Purity is a property of a function such that its return value is always the same for the same arguments, and that its evaluation has no side effects.</span></span> <span data-ttu-id="fe5d2-124">Une fonction pure dépend entièrement de ses arguments.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-124">A pure function depends entirely on its arguments.</span></span>
* <span data-ttu-id="fe5d2-125">**Transparence référentielle** -transparence référentielle est une propriété des expressions telles qu’elles puissent être remplacées sans affecter le comportement d’un programme avec leur sortie.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-125">**Referential Transparency** - Referential Transparency is a property of expressions such that they can be replaced with their output without affecting a program's behavior.</span></span>
* <span data-ttu-id="fe5d2-126">**Immuabilité** -signifie d’immuabilité qu’une valeur ne peut pas être modifié sur place.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-126">**Immutability** - Immutability means that a value cannot be changed in-place.</span></span> <span data-ttu-id="fe5d2-127">Ceci est le contraire des variables qui peuvent changer en place.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-127">This is in contrast with variables, which can change in place.</span></span>

## <a name="examples"></a><span data-ttu-id="fe5d2-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe5d2-128">Examples</span></span>

<span data-ttu-id="fe5d2-129">Les exemples suivants illustrent ces concepts fondamentaux.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-129">The following examples demonstrate these core concepts.</span></span>

### <a name="functions"></a><span data-ttu-id="fe5d2-130">Fonctions</span><span class="sxs-lookup"><span data-stu-id="fe5d2-130">Functions</span></span>

<span data-ttu-id="fe5d2-131">Les plus courantes et fondamentale de programmation fonctionnelle est la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-131">The most common and fundamental construct in functional programming is the function.</span></span> <span data-ttu-id="fe5d2-132">Voici une fonction simple qui ajoute 1 à un entier :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-132">Here's a simple function that adds 1 to an integer:</span></span>

```fsharp
let addOne x = x + 1
```

<span data-ttu-id="fe5d2-133">Sa signature de type est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-133">Its type signature is as follows:</span></span>

```fsharp
val addOne: x:int -> int
```

<span data-ttu-id="fe5d2-134">La signature peut être lu comme, «`addOne` accepte un `int` nommé `x` et produira un `int`».</span><span class="sxs-lookup"><span data-stu-id="fe5d2-134">The signature can be read as, "`addOne` accepts an `int` named `x` and will produce an `int`".</span></span> <span data-ttu-id="fe5d2-135">Plus formellement, `addOne` est _mappage_ une valeur de l’ensemble d’entiers à l’ensemble d’entiers.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-135">More formally, `addOne` is _mapping_ a value from the set of integers to the set of integers.</span></span> <span data-ttu-id="fe5d2-136">Le `->` jeton désigne ce mappage.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-136">The `->` token signifies this mapping.</span></span> <span data-ttu-id="fe5d2-137">Dans F#, vous pouvez généralement consulter la signature de fonction pour obtenir une idée de ce qu’il fait.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-137">In F#, you can usually look at the function signature to get a sense for what it does.</span></span>

<span data-ttu-id="fe5d2-138">Par conséquent, pourquoi est-la signature important ?</span><span class="sxs-lookup"><span data-stu-id="fe5d2-138">So, why is the signature important?</span></span> <span data-ttu-id="fe5d2-139">Dans la programmation fonctionnelle typée, l’implémentation d’une fonction est souvent moins importante que la signature de type réel !</span><span class="sxs-lookup"><span data-stu-id="fe5d2-139">In typed functional programming, the implementation of a function is often less important than the actual type signature!</span></span> <span data-ttu-id="fe5d2-140">Le fait que `addOne` ajoute la valeur 1 à un entier est intéressante lors de l’exécution, mais lorsque vous construisez un programme, le fait qu’il accepte et retourne un `int` est ce qui indique comment vous allez utiliser réellement cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-140">The fact that `addOne` adds the value 1 to an integer is interesting at runtime, but when you are constructing a program, the fact that it accepts and returns an `int` is what informs how you will actually use this function.</span></span> <span data-ttu-id="fe5d2-141">En outre, une fois que vous utilisez cette fonction correctement (par rapport à sa signature de type), diagnostiquer des problèmes est possible uniquement dans le corps de la `addOne` (fonction).</span><span class="sxs-lookup"><span data-stu-id="fe5d2-141">Furthermore, once you use this function correctly (with respect to its type signature), diagnosing any problems can be done only within the body of the `addOne` function.</span></span> <span data-ttu-id="fe5d2-142">Il s’agit de l’idée derrière la programmation fonctionnelle typée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-142">This is the impetus behind typed functional programming.</span></span>

### <a name="expressions"></a><span data-ttu-id="fe5d2-143">Expressions</span><span class="sxs-lookup"><span data-stu-id="fe5d2-143">Expressions</span></span>

<span data-ttu-id="fe5d2-144">Les expressions sont des constructions qui donnent comme résultat une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-144">Expressions are constructs that evaluate to a value.</span></span> <span data-ttu-id="fe5d2-145">Contrairement aux instructions qui effectuent une action, les expressions peuvent être considérées d’effectuer une action qui renvoie une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-145">In contrast to statements, which perform an action, expressions can be thought of performing an action that gives back a value.</span></span> <span data-ttu-id="fe5d2-146">Les expressions sont presque toujours utilisées en faveur des instructions dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-146">Expressions are almost always used in favor of statements in functional programming.</span></span>

<span data-ttu-id="fe5d2-147">Considérez la fonction précédente, `addOne`.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-147">Consider the previous function, `addOne`.</span></span> <span data-ttu-id="fe5d2-148">Le corps de `addOne` est une expression :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-148">The body of `addOne` is an expression:</span></span>

```fsharp
// 'x + 1' is an expression!
let addOne x = x + 1
```

<span data-ttu-id="fe5d2-149">Il est le résultat de cette expression qui définit le type de résultat de la `addOne` (fonction).</span><span class="sxs-lookup"><span data-stu-id="fe5d2-149">It is the result of this expression that defines the result type of the `addOne` function.</span></span> <span data-ttu-id="fe5d2-150">Par exemple, l’expression de cette fonction peut être changée pour être un type différent, comme un `string`:</span><span class="sxs-lookup"><span data-stu-id="fe5d2-150">For example, the expression that makes up this function could be changed to be a different type, such as a `string`:</span></span>

```fsharp
let addOne x = x.ToString() + "1"
```

<span data-ttu-id="fe5d2-151">La signature de la fonction est désormais :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-151">The signature of the function is now:</span></span>

```fsharp
val addOne: x:'a -> string
```

<span data-ttu-id="fe5d2-152">Depuis n’importe quel type dans F# peut avoir `ToString()` appelé dessus, le type de `x` soit devenue générique (appelé [généralisation automatique](../language-reference/generics/automatic-generalization.md)), et le type résultant est un `string`.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-152">Since any type in F# can have `ToString()` called on it, the type of `x` has been made generic (called [Automatic Generalization](../language-reference/generics/automatic-generalization.md)), and the resultant type is a `string`.</span></span>

<span data-ttu-id="fe5d2-153">Les expressions ne sont pas simplement les corps des fonctions.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-153">Expressions are not just the bodies of functions.</span></span> <span data-ttu-id="fe5d2-154">Vous pouvez avoir des expressions qui produisent une valeur que vous utilisez un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-154">You can have expressions that produce a value you use elsewhere.</span></span> <span data-ttu-id="fe5d2-155">Un commun un est `if`:</span><span class="sxs-lookup"><span data-stu-id="fe5d2-155">A common one is `if`:</span></span>

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

<span data-ttu-id="fe5d2-156">Le `if` expression produit une valeur appelée `result`.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-156">The `if` expression produces a value called `result`.</span></span> <span data-ttu-id="fe5d2-157">Notez que vous pourriez omettre `result` entièrement, ce qui le `if` le corps d’expression de la `addOneIfOdd` (fonction).</span><span class="sxs-lookup"><span data-stu-id="fe5d2-157">Note that you could omit `result` entirely, making the `if` expression the body of the `addOneIfOdd` function.</span></span> <span data-ttu-id="fe5d2-158">Le point clé à retenir sur les expressions est qu’elles produisent une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-158">The key thing to remember about expressions is that they produce a value.</span></span>

<span data-ttu-id="fe5d2-159">Il existe un type spécial, `unit`, qui est utilisé lorsqu’il n’y a rien à retourner.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-159">There is a special type, `unit`, that is used when there is nothing to return.</span></span> <span data-ttu-id="fe5d2-160">Par exemple, considérez cette fonction simple :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-160">For example, consider this simple function:</span></span>

```fsharp
let printString (str: string) =
    printfn "String is: %s" str
```

<span data-ttu-id="fe5d2-161">La signature se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-161">The signature looks like this:</span></span>

```fsharp
val printString: str:string -> unit
```

<span data-ttu-id="fe5d2-162">Le `unit` type indique qu’il n’existe aucune valeur réelle retournée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-162">The `unit` type indicates that there is no actual value being returned.</span></span> <span data-ttu-id="fe5d2-163">Cela est utile lorsque vous avez une routine qui doit « fonctionnent-elles » bien ne qu’aucune valeur de retour à la suite de ce travail.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-163">This is useful when you have a routine that must "do work" despite having no value to return as a result of that work.</span></span>

<span data-ttu-id="fe5d2-164">Cela se démarque de la programmation impérative, où l’équivalent `if` construction est une instruction, et produire des valeurs est souvent effectuée avec des variables de mutation.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-164">This is in sharp contrast to imperative programming, where the equivalent `if` construct is a statement, and producing values is often done with mutating variables.</span></span> <span data-ttu-id="fe5d2-165">Par exemple, dans C#, le code peut être écrit comme suit :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-165">For example, in C#, the code might be written like this:</span></span>

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

<span data-ttu-id="fe5d2-166">Il est important de souligner que C# et d’autres langages de style C ne prennent pas en charge la [expression ternaire](../../csharp/language-reference/operators/conditional-operator.md), ce qui permet la programmation basée sur une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-166">It's worth noting that C# and other C-style languages do support the [ternary expression](../../csharp/language-reference/operators/conditional-operator.md), which allows for expression-based conditional programming.</span></span>

<span data-ttu-id="fe5d2-167">Dans la programmation fonctionnelle, il est rare de muter les valeurs avec des instructions.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-167">In functional programming, it is rare to mutate values with statements.</span></span> <span data-ttu-id="fe5d2-168">Bien que certains langages fonctionnels prennent en charge les instructions et une mutation, il n’est pas courant d’utiliser ces concepts dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-168">Although some functional languages support statements and mutation, it is not common to use these concepts in functional programming.</span></span>

### <a name="pure-functions"></a><span data-ttu-id="fe5d2-169">Fonctions pures</span><span class="sxs-lookup"><span data-stu-id="fe5d2-169">Pure functions</span></span>

<span data-ttu-id="fe5d2-170">Comme mentionnées précédemment, pures fonctions sont les fonctions qui :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-170">As previously mentioned, pure functions are functions that:</span></span>

* <span data-ttu-id="fe5d2-171">Évaluez toujours la même valeur pour la même entrée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-171">Always evaluate to the same value for the same input.</span></span>
* <span data-ttu-id="fe5d2-172">N’ont aucun effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-172">Have no side effects.</span></span>

<span data-ttu-id="fe5d2-173">Il est utile de considérer les fonctions mathématiques dans ce contexte.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-173">It is helpful to think of mathematical functions in this context.</span></span> <span data-ttu-id="fe5d2-174">En mathématique, les fonctions dépendent uniquement de leurs arguments et n’ont pas d’effets secondaires.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-174">In mathematics, functions depend only on their arguments and do not have any side effects.</span></span> <span data-ttu-id="fe5d2-175">Dans la fonction mathématique `f(x) = x + 1`, la valeur de `f(x)` dépend uniquement de la valeur de `x`.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-175">In the mathematical function `f(x) = x + 1`, the value of `f(x)` depends only on the value of `x`.</span></span> <span data-ttu-id="fe5d2-176">Dans la programmation fonctionnelle, les fonctions pures sont la même façon.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-176">Pure functions in functional programming are the same way.</span></span>

<span data-ttu-id="fe5d2-177">Lorsque vous écrivez une fonction pure, la fonction doit dépendre uniquement de ses arguments et pas effectuer toute action qui entraîne un effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-177">When writing a pure function, the function must depend only on its arguments and not perform any action that results in a side effect.</span></span>

<span data-ttu-id="fe5d2-178">Voici un exemple d’une fonction non pure, car elle dépend d’état global et mutable :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-178">Here is an example of a non-pure function because it depends on global, mutable state:</span></span>

```fsharp
let mutable value = 1

let addOneToValue x = x + value
```

<span data-ttu-id="fe5d2-179">Le `addOneToValue` fonction est clairement impure, étant donné que `value` peut être changé à tout moment pour avoir une valeur différente de 1.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-179">The `addOneToValue` function is clearly impure, because `value` could be changed at any time to have a different value than 1.</span></span> <span data-ttu-id="fe5d2-180">Ce modèle de selon une valeur globale doit être évitée dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-180">This pattern of depending on a global value is to be avoided in functional programming.</span></span>

<span data-ttu-id="fe5d2-181">Voici un autre exemple d’une fonction non pure, car elle effectue un effet secondaire :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-181">Here is another example of a non-pure function, because it performs a side effect:</span></span>

```fsharp
let addOneToValue x = 
    printfn "x is %d" x
    x + 1
```

<span data-ttu-id="fe5d2-182">Bien que cette fonction ne repose pas sur une valeur globale, il écrit la valeur de `x` à la sortie du programme.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-182">Although this function does not depend on a global value, it writes the value of `x` to the output of the program.</span></span> <span data-ttu-id="fe5d2-183">Bien qu’il n’a rien de choquant dans cette opération, cela signifie que la fonction n’est pas pure.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-183">Although there is nothing inherently wrong with doing this, it does mean that the function is not pure.</span></span> <span data-ttu-id="fe5d2-184">Si une autre partie de votre programme dépend de l’élément externe au programme, telles que la mémoire tampon de sortie, puis en appelant cette fonction peut affecter à cette autre partie de votre programme.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-184">If another part of your program depends on something external to the program, such as the output buffer, then calling this function can affect that other part of your program.</span></span>

<span data-ttu-id="fe5d2-185">Suppression de la `printfn` instruction rend la fonction pure :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-185">Removing the `printfn` statement makes the function pure:</span></span>

```fsharp
let addOneToValue x = x + 1
```

<span data-ttu-id="fe5d2-186">Bien que cette fonction n’est pas fondamentalement _mieux_ que la version précédente avec la `printfn` instruction, cela ne garantit que cette fonction n’est retournent une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-186">Although this function is not inherently _better_ than the previous version with the `printfn` statement, it does guarantee that all this function does is return a value.</span></span> <span data-ttu-id="fe5d2-187">Appel de n’importe quel nombre de fois où cette fonction produit le même résultat : il génère simplement une valeur.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-187">Calling this function any number of times produces the same result: it just produces a value.</span></span> <span data-ttu-id="fe5d2-188">La prévisibilité donnée par la pureté est quelque chose pour que s’efforcent de nombreux programmeurs fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-188">The predictability given by purity is something many functional programmers strive for.</span></span>

### <a name="immutability"></a><span data-ttu-id="fe5d2-189">Immuabilité</span><span class="sxs-lookup"><span data-stu-id="fe5d2-189">Immutability</span></span>

<span data-ttu-id="fe5d2-190">Enfin, un des concepts plus fondamentaux de la programmation fonctionnelle typée consiste immuabilité.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-190">Finally, one of the most fundamental concepts of typed functional programming is immutability.</span></span> <span data-ttu-id="fe5d2-191">Dans F#, toutes les valeurs sont immuables par défaut.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-191">In F#, all values are immutable by default.</span></span> <span data-ttu-id="fe5d2-192">Cela signifie qu’ils ne peut pas être muter sur place, sauf si vous les marquez comme mutables.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-192">That means they cannot be mutated in-place unless you explicitly mark them as mutable.</span></span>

<span data-ttu-id="fe5d2-193">Dans la pratique, travailler avec des valeurs immuables signifie que vous remplacez votre approche de programmation, « Je dois modifier quelque chose » à « j’ai besoin produire une nouvelle valeur ».</span><span class="sxs-lookup"><span data-stu-id="fe5d2-193">In practice, working with immutable values means that you change your approach to programming from, "I need to change something", to "I need to produce a new value".</span></span>

<span data-ttu-id="fe5d2-194">Par exemple, ajout de 1 à une valeur signifie produisant une nouvelle valeur, ne pas de mutation existant :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-194">For example, adding 1 to a value means producing a new value, not mutating the existing one:</span></span>

```fsharp
let value = 1
let secondValue = value + 1
```

<span data-ttu-id="fe5d2-195">Dans F#, le code suivant effectue **pas** muter le `value` fonction ; au lieu de cela, il effectue une vérification de l’égalité :</span><span class="sxs-lookup"><span data-stu-id="fe5d2-195">In F#, the following code does **not** mutate the `value` function; instead, it performs an equality check:</span></span>

```fsharp
let value = 1
value = value + 1 // Produces a 'bool' value!
```

<span data-ttu-id="fe5d2-196">Certains langages de programmation fonctionnelles ne gèrent pas mutation.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-196">Some functional programming languages do not support mutation at all.</span></span> <span data-ttu-id="fe5d2-197">Dans F#, il est pris en charge, mais il n’est pas le comportement par défaut pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-197">In F#, it is supported, but it is not the default behavior for values.</span></span>

<span data-ttu-id="fe5d2-198">Ce concept s’étend même jusqu'à proposer des structures de données.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-198">This concept extends even further to data structures.</span></span> <span data-ttu-id="fe5d2-199">Dans la programmation fonctionnelle, les structures de données immuables telles que les jeux (et bien plus encore) ait une implémentation différente que vous pouvez initialement prévu.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-199">In functional programming, immutable data structures such as sets (and many more) have a different implementation than you might initially expect.</span></span> <span data-ttu-id="fe5d2-200">Conceptuellement, un tel ajout d’un élément à un ensemble ne modifie pas le jeu, il génère un _nouveau_ définie avec la valeur ajoutée.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-200">Conceptually, something like adding an item to a set does not change the set, it produces a _new_ set with the added value.</span></span> <span data-ttu-id="fe5d2-201">En coulisses, souvent cela par une structure de données différente qui permet de suivre efficacement une valeur pour que la représentation appropriée des données peut être donnée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-201">Under the covers, this is often accomplished by a different data structure that allows for efficiently tracking a value so that the appropriate representation of the data can be given as a result.</span></span>

<span data-ttu-id="fe5d2-202">Ce style de l’utilisation de valeurs et les structures de données est cruciale, car il vous permet de traiter toute opération qui modifie quelque chose comme s’il crée une nouvelle version de ceci force.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-202">This style of working with values and data structures is critical, as it forces you to treat any operation that modifies something as if it creates a new version of that thing.</span></span> <span data-ttu-id="fe5d2-203">Cela permet à des éléments comme l’égalité et d’infériorité être cohérents dans vos programmes.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-203">This allows for things like equality and comparability to be consistent in your programs.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fe5d2-204">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fe5d2-204">Next steps</span></span>

<span data-ttu-id="fe5d2-205">La section suivante couvre soigneusement les fonctions, exploration de différentes façons, vous pouvez les utiliser dans la programmation fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-205">The next section will thoroughly cover functions, exploring different ways you can use them in functional programming.</span></span>

<span data-ttu-id="fe5d2-206">[Fonctions de première classe](first-class-functions.md) explore les fonctions profondément, montrant comment vous pouvez les utiliser dans différents contextes.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-206">[First-class functions](first-class-functions.md) explores functions deeply, showing how you can use them in various contexts.</span></span>

## <a name="further-reading"></a><span data-ttu-id="fe5d2-207">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fe5d2-207">Further reading</span></span>

<span data-ttu-id="fe5d2-208">Le [penser fonctionnellement](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) série est également une excellente ressource pour en savoir plus sur la programmation fonctionnelle avec F#.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-208">The [Thinking Functionally](https://fsharpforfunandprofit.com/posts/thinking-functionally-intro/) series is another great resource to learn about functional programming with F#.</span></span> <span data-ttu-id="fe5d2-209">Il couvre les notions de base de la programmation fonctionnelle de façon pragmatique et facile à lire, à l’aide de F# fonctionnalités pour illustrer les concepts.</span><span class="sxs-lookup"><span data-stu-id="fe5d2-209">It covers fundamentals of functional programming in a pragmatic and easy-to-read way, using F# features to illustrate the concepts.</span></span>
