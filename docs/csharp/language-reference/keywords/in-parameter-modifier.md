---
title: in, modificateur de paramètre (référence C#)
ms.date: 03/06/2018
helpviewer_keywords:
- parameters [C#], in
- in parameters [C#]
ms.openlocfilehash: 54abd5192d0d9bb49be0a9feb8e5e4eaeb691a0c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43461720"
---
# <a name="in-parameter-modifier-c-reference"></a><span data-ttu-id="4d290-102">in, modificateur de paramètre (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4d290-102">in parameter modifier (C# Reference)</span></span>

<span data-ttu-id="4d290-103">Le mot clé `in` entraîne le passage des arguments par référence.</span><span class="sxs-lookup"><span data-stu-id="4d290-103">The `in` keyword causes arguments to be passed by reference.</span></span> <span data-ttu-id="4d290-104">Il est similaire aux mots clés [ref](ref.md) ou [out](out-parameter-modifier.md), sauf que les arguments `in` ne peuvent pas être modifiés par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="4d290-104">It is like the [ref](ref.md) or [out](out-parameter-modifier.md) keywords, except that `in` arguments cannot be modified by the called method.</span></span> <span data-ttu-id="4d290-105">Alors que les arguments `ref` peuvent être modifiés, les arguments `out` doivent être modifiés par l’appelant, et ces modifications sont observables dans le contexte d’appel.</span><span class="sxs-lookup"><span data-stu-id="4d290-105">Whereas `ref` arguments may be modified,  `out` arguments must be modified by the caller, and those modifications are observable in the calling context.</span></span>

[!code-csharp-interactive[cs-in-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/InParameterModifier.cs#1)]  

<span data-ttu-id="4d290-106">L’exemple précédent montre que le modificateur `in` n’est généralement pas nécessaire sur le site d’appel.</span><span class="sxs-lookup"><span data-stu-id="4d290-106">The preceding example demonstrates that the `in` modifier is usually unnecessary at the call site.</span></span> <span data-ttu-id="4d290-107">Il l’est uniquement dans la déclaration de méthode.</span><span class="sxs-lookup"><span data-stu-id="4d290-107">It is only required in the method declaration.</span></span>

> [!NOTE] 
> <span data-ttu-id="4d290-108">Le mot clé `in` peut également être utilisé avec un paramètre de type générique pour spécifier que le paramètre de type est contravariant, dans le cadre d’une instruction `foreach` ou d’une clause `join` dans une requête LINQ.</span><span class="sxs-lookup"><span data-stu-id="4d290-108">The `in` keyword can also be used with a generic type parameter to specify that the type parameter is contravariant, as part of a `foreach` statement, or as part of a `join` clause in a LINQ query.</span></span> <span data-ttu-id="4d290-109">Pour plus d’informations sur l’utilisation du mot clé `in` dans ces contextes, consultez [in](in.md), qui fournit des liens vers toutes ces utilisations.</span><span class="sxs-lookup"><span data-stu-id="4d290-109">For more information on the use of the `in` keyword in these contexts, see [in](in.md), which provides links to all those uses.</span></span>
  
 <span data-ttu-id="4d290-110">Les variables passées comme des arguments `in` doivent être initialisées avant d’être passées dans un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="4d290-110">Variables passed as `in` arguments must be initialized before being passed in a method call.</span></span> <span data-ttu-id="4d290-111">Toutefois, la méthode appelée ne peut pas attribuer de valeur ou modifier l’argument.</span><span class="sxs-lookup"><span data-stu-id="4d290-111">However, the called method may not assign a value or modify the argument.</span></span>  
  
 <span data-ttu-id="4d290-112">Bien que les mots clés `in`, `ref` et `out` entraînent un comportement différent au moment de l’exécution, ils ne sont pas considérés comme faisant partie de la signature de la méthode au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="4d290-112">Although the `in`, `ref`, and `out` keywords cause different run-time behavior, they are not considered part of the method signature at compile time.</span></span> <span data-ttu-id="4d290-113">Par conséquent, les méthodes ne peuvent pas être surchargées si la seule différence est que l’une d’elles accepte un argument `ref` ou `in` et que l’autre accepte un argument `out`.</span><span class="sxs-lookup"><span data-stu-id="4d290-113">Therefore, methods cannot be overloaded if the only difference is that one method takes a `ref` or `in` argument and the other takes an `out` argument.</span></span> <span data-ttu-id="4d290-114">Le code suivant, par exemple, ne se compilera pas :</span><span class="sxs-lookup"><span data-stu-id="4d290-114">The following code, for example, will not compile:</span></span>  
  
```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on in, ref and out".
    public void SampleMethod(in int i) { }
    public void SampleMethod(ref int i) { }
}
```
  
<span data-ttu-id="4d290-115">Une surcharge basée sur la présence de `in` est autorisée :</span><span class="sxs-lookup"><span data-stu-id="4d290-115">Overloading based on the presence of `in` is allowed:</span></span>  
  
```csharp
class InOverloads
{
    public void SampleMethod(in int i) { }
    public void SampleMethod(int i) { }
}
```

## <a name="overload-resolution-rules"></a><span data-ttu-id="4d290-116">Règles de résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="4d290-116">Overload resolution rules</span></span>

<span data-ttu-id="4d290-117">Vous pouvez comprendre les règles de résolution de surcharge pour les méthodes par valeur par rapport à celles qui utilisent des arguments `in` en comprenant pourquoi on utilise des arguments `in`.</span><span class="sxs-lookup"><span data-stu-id="4d290-117">You can understand the overload resolution rules for methods with by value vs. `in` arguments by understanding the motivation for `in` arguments.</span></span> <span data-ttu-id="4d290-118">Vous pouvez optimiser les performances en définissant des méthodes à l’aide de paramètres `in`.</span><span class="sxs-lookup"><span data-stu-id="4d290-118">Defining methods using `in` parameters is a potential performance optimization.</span></span> <span data-ttu-id="4d290-119">Certains arguments de type `struct` peuvent être volumineux et, quand les méthodes sont appelées dans des boucles serrées ou des chemins de code critiques, le coût de la copie de ces structures est crucial.</span><span class="sxs-lookup"><span data-stu-id="4d290-119">Some `struct` type arguments may be large in size, and when methods are called in tight loops or critical code paths, the cost of copying those structures is critical.</span></span> <span data-ttu-id="4d290-120">Les méthodes déclarent des paramètres `in` pour spécifier que des arguments peuvent être passés par référence en toute sécurité, car la méthode appelée ne modifie pas l’état de l’argument.</span><span class="sxs-lookup"><span data-stu-id="4d290-120">Methods declare `in` parameters to specify that arguments may be passed by reference safely because the called method does not modify the state of that argument.</span></span> <span data-ttu-id="4d290-121">Le passage de ces arguments par référence permet d’éviter une copie (potentiellement) coûteuse.</span><span class="sxs-lookup"><span data-stu-id="4d290-121">Passing those arguments by reference avoids the (potentially) expensive copy.</span></span> 

<span data-ttu-id="4d290-122">La spécification de `in` pour des arguments au niveau de l’appel de site est généralement facultative.</span><span class="sxs-lookup"><span data-stu-id="4d290-122">Specifying `in` for arguments at the call site is typically optional.</span></span> <span data-ttu-id="4d290-123">Il n’existe aucune différence sémantique entre le passage d’arguments par valeur et leur passage par référence à l’aide du modificateur `in`.</span><span class="sxs-lookup"><span data-stu-id="4d290-123">There is no semantic difference between passing arguments by value and passing them by reference using the `in` modifier.</span></span> <span data-ttu-id="4d290-124">Le modificateur `in` sur le site d’appel est facultatif, car vous n’avez pas besoin d’indiquer que la valeur de l’argument peut être changée.</span><span class="sxs-lookup"><span data-stu-id="4d290-124">The `in` modifier at the call site is optional because you don't need to indicate that the argument's value might be changed.</span></span> <span data-ttu-id="4d290-125">Vous ajoutez explicitement le modificateur `in` sur le site d’appel pour vérifier que l’argument est passé par référence, non par valeur.</span><span class="sxs-lookup"><span data-stu-id="4d290-125">You explicitly add the `in` modifier at the call site to ensure the argument is passed by reference, not by value.</span></span> <span data-ttu-id="4d290-126">L’utilisation explicite de `in` a les deux effets suivants :</span><span class="sxs-lookup"><span data-stu-id="4d290-126">Explicitly using `in` has the following two effects:</span></span>

<span data-ttu-id="4d290-127">Tout d’abord, la spécification de `in` sur le site d’appel force le compilateur à sélectionner une méthode définie avec un paramètre `in` correspondant.</span><span class="sxs-lookup"><span data-stu-id="4d290-127">First, specifying `in` at the call site forces the compiler to select a method defined with a matching `in` parameter.</span></span> <span data-ttu-id="4d290-128">Sinon, quand deux méthodes diffèrent uniquement par la présence de `in`, la surcharge par valeur convient mieux.</span><span class="sxs-lookup"><span data-stu-id="4d290-128">Otherwise, when two methods differ only in the presence of `in`, the by value overload is a better match.</span></span>

<span data-ttu-id="4d290-129">Ensuite, la spécification de `in` déclare votre intention de passer un argument par référence.</span><span class="sxs-lookup"><span data-stu-id="4d290-129">Second, specifying `in` declares your intent to pass an argument by reference.</span></span> <span data-ttu-id="4d290-130">L’argument utilisé avec `in` doit représenter un emplacement directement référençable.</span><span class="sxs-lookup"><span data-stu-id="4d290-130">The argument used with `in` must represent a location that can be directly referred to.</span></span> <span data-ttu-id="4d290-131">Les mêmes règles générales pour les arguments `out` et `ref` s’appliquent : vous ne pouvez pas utiliser de constantes, de propriétés ordinaires ou d’autres expressions qui produisent des valeurs.</span><span class="sxs-lookup"><span data-stu-id="4d290-131">The same general rules for `out` and `ref` arguments apply: You cannot use constants, ordinary properties, or other expressions that produce values.</span></span> <span data-ttu-id="4d290-132">Sinon, l’omission de `in` sur le site d’appel informe le compilateur que vous l’autorisez à créer une variable temporaire à passer par référence en lecture seule à la méthode.</span><span class="sxs-lookup"><span data-stu-id="4d290-132">Otherwise, omitting `in` at the call site informs the compiler that you will allow it to create a temporary variable to pass by read-only reference to the method.</span></span> <span data-ttu-id="4d290-133">Le compilateur crée une variable temporaire pour surmonter plusieurs restrictions avec les arguments `in` :</span><span class="sxs-lookup"><span data-stu-id="4d290-133">The compiler creates a temporary variable to overcome several restrictions with `in` arguments:</span></span>

- <span data-ttu-id="4d290-134">Une variable temporaire autorise des constantes au moment de la compilation comme paramètres `in`.</span><span class="sxs-lookup"><span data-stu-id="4d290-134">A temporary variable allows compile-time constants as `in` parameters.</span></span>
- <span data-ttu-id="4d290-135">Une variable temporaire autorise des propriétés ou d’autres expressions pour les paramètres `in`.</span><span class="sxs-lookup"><span data-stu-id="4d290-135">A temporary variable allows properties, or other expressions for `in` parameters.</span></span>
- <span data-ttu-id="4d290-136">Une variable temporaire autorise des arguments pour lesquels il existe une conversion implicite de type d’argument en type de paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d290-136">A temporary variable allows arguments where there is an implicit conversion from the argument type to the parameter type.</span></span>

<span data-ttu-id="4d290-137">Dans toutes les instances précédentes, le compilateur crée une variable temporaire qui stocke la valeur de la constante, la propriété ou une autre expression.</span><span class="sxs-lookup"><span data-stu-id="4d290-137">In all the preceding instances, the compiler creates a temporary variable that stores the value of the constant, property, or other expression.</span></span>

<span data-ttu-id="4d290-138">Le code suivant illustre ces règles :</span><span class="sxs-lookup"><span data-stu-id="4d290-138">The following code illustrates these rules:</span></span>

```csharp
static void Method(in int argument)
{
    // implementation removed
}

Method(5); // OK, temporary variable created.
Method(5L); // CS1503: no implicit conversion from long to int
short s = 0;
Method(s); // OK, temporary int created with the value 0
Method(in s); // CS1503: cannot convert from in short to in int
int i = 42;
Method(i); // passed by readonly reference
Method(in i); // passed by readonly reference, explicitly using `in`
```

<span data-ttu-id="4d290-139">Supposons à présent qu’une autre méthode utilisant des arguments par valeur est disponible.</span><span class="sxs-lookup"><span data-stu-id="4d290-139">Now, suppose another method using by value arguments was available.</span></span> <span data-ttu-id="4d290-140">Les résultats changent comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4d290-140">The results change as shown in the following code:</span></span>

```csharp
static void Method(int argument)
{
    // implementation removed
}

static void Method(in int argument)
{
    // implementation removed
}

Method(5); // Calls overload passed by value
Method(5L); // CS1503: no implicit conversion from long to int
short s = 0;
Method(s); // Calls overload passed by value.
Method(in s); // CS1503: cannot convert from in short to in int
int i = 42;
Method(i); // Calls overload passed by value
Method(in i); // passed by readonly reference, explicitly using `in`
```

<span data-ttu-id="4d290-141">Le seul appel de méthode dans lequel l’argument est passé par référence est le dernier.</span><span class="sxs-lookup"><span data-stu-id="4d290-141">The only method call where the argument is passed by reference is the final one.</span></span>

> [!NOTE]
> <span data-ttu-id="4d290-142">Le code précédent utilise `int` comme type d’argument par souci de simplicité.</span><span class="sxs-lookup"><span data-stu-id="4d290-142">The preceding code uses `int` as the argument type for simplicity.</span></span> <span data-ttu-id="4d290-143">Comme `int` n’est pas plus volumineux qu’une référence dans la plupart des ordinateurs modernes, il n’y aucun avantage à passer un seul `int` comme référence en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4d290-143">Because `int` is no larger than a reference in most modern machines, there is no benefit to passing a single `int` as a readonly reference.</span></span> 

## <a name="limitations-on-in-parameters"></a><span data-ttu-id="4d290-144">Limitations sur les paramètres `in`</span><span class="sxs-lookup"><span data-stu-id="4d290-144">Limitations on `in` parameters</span></span>

<span data-ttu-id="4d290-145">Vous ne pouvez pas utiliser les mots clés `in`, `ref` ou `out` pour les types de méthodes suivants :</span><span class="sxs-lookup"><span data-stu-id="4d290-145">You can't use the `in`, `ref`, and `out` keywords for the following kinds of methods:</span></span>  
  
- <span data-ttu-id="4d290-146">Méthodes async, que vous définissez à l’aide du modificateur [async](async.md).</span><span class="sxs-lookup"><span data-stu-id="4d290-146">Async methods, which you define by using the [async](async.md) modifier.</span></span>  
- <span data-ttu-id="4d290-147">Les méthodes Iterator, qui incluent une instruction [yield return](yield.md) ou `yield break`.</span><span class="sxs-lookup"><span data-stu-id="4d290-147">Iterator methods, which include a [yield return](yield.md) or `yield break` statement.</span></span>  

## <a name="c-language-specification"></a><span data-ttu-id="4d290-148">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="4d290-148">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4d290-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d290-149">See Also</span></span>

- [<span data-ttu-id="4d290-150">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4d290-150">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="4d290-151">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4d290-151">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="4d290-152">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="4d290-152">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="4d290-153">Paramètres de méthodes</span><span class="sxs-lookup"><span data-stu-id="4d290-153">Method Parameters</span></span>](method-parameters.md)  
- [<span data-ttu-id="4d290-154">Sémantique de référence avec les types valeur</span><span class="sxs-lookup"><span data-stu-id="4d290-154">Reference Semantics with Value Types</span></span>](../../reference-semantics-with-value-types.md)  
