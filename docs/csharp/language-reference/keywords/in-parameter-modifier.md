---
title: in, modificateur de paramètre (référence C#)
ms.date: 03/06/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- parameters [C#], in
- in parameters [C#]
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 9b8b21e2bdc95829c831ee71f24b47986321b7d0
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="in-parameter-modifier-c-reference"></a><span data-ttu-id="e0b52-102">in, modificateur de paramètre (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e0b52-102">in parameter modifier (C# Reference)</span></span>

<span data-ttu-id="e0b52-103">Le mot clé `in` entraîne le passage des arguments par référence.</span><span class="sxs-lookup"><span data-stu-id="e0b52-103">The `in` keyword causes arguments to be passed by reference.</span></span> <span data-ttu-id="e0b52-104">Il est similaire aux mots clés [ref](ref.md) ou [out](out-parameter-modifier.md), sauf que les arguments `in` ne peuvent pas être modifiés par la méthode appelée, tandis que les arguments `ref` peuvent l’être, les arguments `out` doivent être modifiés par l’appelant et ces modifications sont observables dans le contexte d’appel.</span><span class="sxs-lookup"><span data-stu-id="e0b52-104">It is like the [ref](ref.md) or [out](out-parameter-modifier.md) keywords, except that `in` arguments cannot be modified by the called method, whereas `ref` arguments may be modified,  `out` arguments must be modified by the caller, and those modifications are observable in the calling context.</span></span>

[!code-csharp-interactive[cs-in-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/InParameterModifier.cs#1)]  

<span data-ttu-id="e0b52-105">L’exemple précédent montre que le modificateur `in` n’est pas nécessaire sur le site d’appel.</span><span class="sxs-lookup"><span data-stu-id="e0b52-105">The preceding example demonstrates that the `in` modifier is unnecessary at the call site.</span></span> <span data-ttu-id="e0b52-106">Il l’est uniquement dans la déclaration de méthode.</span><span class="sxs-lookup"><span data-stu-id="e0b52-106">It is only required in the method declaration.</span></span>

> [!NOTE] 
> <span data-ttu-id="e0b52-107">Le mot clé `in` peut également être utilisé avec un paramètre de type générique pour spécifier que le paramètre de type est contravariant, dans le cadre d’une instruction `foreach` ou d’une clause `join` dans une requête LINQ.</span><span class="sxs-lookup"><span data-stu-id="e0b52-107">The `in` keyword can also be used with a generic type parameter to specify that the type parameter is contravariant, as part of a `foreach` statement, or as part of a `join` clause in a LINQ query.</span></span> <span data-ttu-id="e0b52-108">Pour plus d’informations sur l’utilisation du mot clé `in` dans ces contextes, consultez [in](in.md) qui fournit des liens vers toutes ces utilisations.</span><span class="sxs-lookup"><span data-stu-id="e0b52-108">For more information on the use of the `in` keyword in these contexts, see [in](in.md) which provides links to all those uses.</span></span>
  
 <span data-ttu-id="e0b52-109">Les variables passées comme des arguments `in` doivent être initialisées avant d’être passées dans un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="e0b52-109">Variables passed as `in` arguments must be initialized before being passed in a method call.</span></span> <span data-ttu-id="e0b52-110">Toutefois, la méthode appelée ne peut pas attribuer de valeur ou modifier l’argument.</span><span class="sxs-lookup"><span data-stu-id="e0b52-110">However, the called method may not assign a value or modify the argument.</span></span>  
  
 <span data-ttu-id="e0b52-111">Bien que les mots clés `in`, `ref` et `out` entraînent un comportement différent au moment de l’exécution, ils ne sont pas considérés comme faisant partie de la signature de la méthode au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="e0b52-111">Although the `in`, `ref`, and `out` keywords cause different run-time behavior, they are not considered part of the method signature at compile time.</span></span> <span data-ttu-id="e0b52-112">Par conséquent, les méthodes ne peuvent pas être surchargées si la seule différence est que l’une d’elles accepte un argument `ref` ou `in` et que l’autre accepte un argument `out`.</span><span class="sxs-lookup"><span data-stu-id="e0b52-112">Therefore, methods cannot be overloaded if the only difference is that one method takes a `ref` or `in` argument and the other takes an `out` argument.</span></span> <span data-ttu-id="e0b52-113">Le code suivant, par exemple, ne se compilera pas :</span><span class="sxs-lookup"><span data-stu-id="e0b52-113">The following code, for example, will not compile:</span></span>  
  
```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on in, ref and out".
    public void SampleMethod(in int i) { }
    public void SampleMethod(ref int i) { }
}
```
  
<span data-ttu-id="e0b52-114">La surcharge basée sur la présence de `in` est autorisée, mais génère un avertissement du compilateur :</span><span class="sxs-lookup"><span data-stu-id="e0b52-114">Overloading based on the presence of `in` is allowed, but generates a compiler warning:</span></span>  
  
```csharp
class InOverloads
{
    // Discouraged. Calling SampleMethod(value) is ambiguous.
    public void SampleMethod(in int i) { }
    public void SampleMethod(int i) { }
}
```

<span data-ttu-id="e0b52-115">Les constantes ou les propriétés peuvent être passées comme des paramètres `in`, car la méthode d’appel peut ne pas modifier leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="e0b52-115">Properties or constants may be passed as `in` parameters, because the calling method may not modify their values.</span></span>
  
<span data-ttu-id="e0b52-116">Vous ne pouvez pas utiliser les mots clés `in`, `ref` ou `out` pour les types de méthodes suivants :</span><span class="sxs-lookup"><span data-stu-id="e0b52-116">You can't use the `in`, `ref`, and `out` keywords for the following kinds of methods:</span></span>  
  
- <span data-ttu-id="e0b52-117">Méthodes async, que vous définissez à l’aide du modificateur [async](../../../csharp/language-reference/keywords/async.md).</span><span class="sxs-lookup"><span data-stu-id="e0b52-117">Async methods, which you define by using the [async](../../../csharp/language-reference/keywords/async.md) modifier.</span></span>  
  
- <span data-ttu-id="e0b52-118">Les méthodes Iterator, qui incluent une instruction [yield return](../../../csharp/language-reference/keywords/yield.md) ou `yield break`.</span><span class="sxs-lookup"><span data-stu-id="e0b52-118">Iterator methods, which include a [yield return](../../../csharp/language-reference/keywords/yield.md) or `yield break` statement.</span></span>  

<span data-ttu-id="e0b52-119">En général, vous déclarez des arguments `in` afin d’éviter les opérations de copie nécessaires pour passer des arguments par valeur.</span><span class="sxs-lookup"><span data-stu-id="e0b52-119">You typically declare `in` arguments to avoid the copy operations necessary for passing arguments by value.</span></span> <span data-ttu-id="e0b52-120">C’est particulièrement utile lorsque les arguments sont des types valeur tels que les structures où les opérations de copie sont plus coûteuses que le passage par référence.</span><span class="sxs-lookup"><span data-stu-id="e0b52-120">This is most useful when arguments are value types such as structures where copy operations are more expensive than passing by reference.</span></span>

> [!WARNING]
>  <span data-ttu-id="e0b52-121">Les paramètres `in` peuvent être encore plus coûteux s’ils sont utilisés à mauvais escient.</span><span class="sxs-lookup"><span data-stu-id="e0b52-121">`in` parameters can be even more expensive if misused.</span></span> <span data-ttu-id="e0b52-122">Le compilateur risque de ne pas savoir si les méthodes de membres modifient l’état du struct.</span><span class="sxs-lookup"><span data-stu-id="e0b52-122">The compiler may not know if member methods modify the state of the struct.</span></span> <span data-ttu-id="e0b52-123">Quand le compilateur ne peut pas assurer que l’objet n’est pas modifié, il crée une copie défensive et appelle les références de membre à l’aide de cette copie.</span><span class="sxs-lookup"><span data-stu-id="e0b52-123">Whenever the compiler cannot ensure that the object is not modified, it defensively creates a copy and calls member references using that copy.</span></span> <span data-ttu-id="e0b52-124">Toutes les modifications possibles sont apportées à cette copie défensive.</span><span class="sxs-lookup"><span data-stu-id="e0b52-124">Any possible modifications are to that defensive copy.</span></span> <span data-ttu-id="e0b52-125">Les deux façons d’éviter ces copies consistent à passer les paramètres `in` comme arguments `in` ou à définir des structures comme `readonly struct`.</span><span class="sxs-lookup"><span data-stu-id="e0b52-125">The two ways to avoid these copies are to pass `in` parameters as `in` arguments or to define structures as `readonly struct`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="e0b52-126">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="e0b52-126">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e0b52-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0b52-127">See Also</span></span>  
 [<span data-ttu-id="e0b52-128">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e0b52-128">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="e0b52-129">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e0b52-129">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="e0b52-130">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="e0b52-130">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="e0b52-131">Paramètres de méthodes</span><span class="sxs-lookup"><span data-stu-id="e0b52-131">Method Parameters</span></span>](../../../csharp/language-reference/keywords/method-parameters.md)  
 [<span data-ttu-id="e0b52-132">Sémantique de référence avec les types valeur</span><span class="sxs-lookup"><span data-stu-id="e0b52-132">Reference Semantics with Value Types</span></span>](../../../csharp/reference-semantics-with-value-types.md)
