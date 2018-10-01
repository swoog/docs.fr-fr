---
title: ref, mot clé (référence C#)
ms.date: 03/06/2018
f1_keywords:
- ref_CSharpKeyword
- ref
helpviewer_keywords:
- parameters [C#], ref
- ref keyword [C#]
ms.openlocfilehash: e0b82de125246e95d8dce2a7afc20119a8a1fe4f
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47207967"
---
# <a name="ref-c-reference"></a><span data-ttu-id="6947b-102">ref (référence C#)</span><span class="sxs-lookup"><span data-stu-id="6947b-102">ref (C# Reference)</span></span>

<span data-ttu-id="6947b-103">Le mot clé `ref` indique une valeur qui est passée par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-103">The `ref` keyword indicates a value that is passed by reference.</span></span> <span data-ttu-id="6947b-104">Il est utilisé dans quatre contextes différents :</span><span class="sxs-lookup"><span data-stu-id="6947b-104">It is used in four different contexts:</span></span>

- <span data-ttu-id="6947b-105">Dans une signature de méthode et dans un appel de méthode, pour passer un argument à une méthode par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-105">In a method signature and in a method call, to pass an argument to a method by reference.</span></span> <span data-ttu-id="6947b-106">Pour plus d’informations, consultez [Passage d’un argument par référence](#passing-an-argument-by-reference).</span><span class="sxs-lookup"><span data-stu-id="6947b-106">See [Passing an argument by reference](#passing-an-argument-by-reference) for more information.</span></span>
- <span data-ttu-id="6947b-107">Dans une signature de méthode, pour retourner une valeur à l’appelant par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-107">In a method signature, to return a value to the caller by reference.</span></span> <span data-ttu-id="6947b-108">Pour plus d’informations, consultez [Valeurs de retour de référence](#reference-return-values).</span><span class="sxs-lookup"><span data-stu-id="6947b-108">See [Reference return values](#reference-return-values) for more information.</span></span>
- <span data-ttu-id="6947b-109">Dans le corps d’un membre, pour indiquer qu’une valeur de retour de référence est stockée localement sous la forme d’une référence que l’appelant a l’intention de modifier, ou une variable locale accède généralement à une valeur par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-109">In a member body, to indicate that a reference return value is stored locally as a reference that the caller intends to modify or, in general, a local variable accesses another value by reference.</span></span> <span data-ttu-id="6947b-110">Pour plus d’informations, consultez [Variables locales ref](#ref-locals).</span><span class="sxs-lookup"><span data-stu-id="6947b-110">See [Ref locals](#ref-locals) for more information.</span></span>
- <span data-ttu-id="6947b-111">Dans une déclaration de `struct` pour déclarer un `ref struct` ou un `ref readonly struct`.</span><span class="sxs-lookup"><span data-stu-id="6947b-111">In a `struct` declaration to declare a `ref struct` or a `ref readonly struct`.</span></span> <span data-ttu-id="6947b-112">Pour plus d’informations, consultez [Sémantique de référence avec les types valeur](../../reference-semantics-with-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-112">For more information, see [Reference semantics with value types](../../reference-semantics-with-value-types.md).</span></span>

## <a name="passing-an-argument-by-reference"></a><span data-ttu-id="6947b-113">Passage d’un argument par référence</span><span class="sxs-lookup"><span data-stu-id="6947b-113">Passing an argument by reference</span></span>

<span data-ttu-id="6947b-114">Quand il est utilisé dans la liste de paramètres d’une méthode, le mot clé `ref` indique qu’un argument est passé par référence, et non par valeur.</span><span class="sxs-lookup"><span data-stu-id="6947b-114">When used in a method's parameter list, the `ref` keyword indicates that an argument is passed by reference, not by value.</span></span> <span data-ttu-id="6947b-115">La conséquence est que toute modification apportée à l’argument dans la méthode appelée est reflétée dans la méthode d’appel.</span><span class="sxs-lookup"><span data-stu-id="6947b-115">The effect of passing by reference is that any change to the argument in the called method is reflected in the calling method.</span></span> <span data-ttu-id="6947b-116">Par exemple, si l’appelant passe une expression de variable locale ou une expression d’accès à un élément de tableau et que la méthode appelée remplace l’objet auquel fait référence le paramètre ref, la variable locale de l’appelant ou l’élément de tableau fait désormais référence au nouvel objet quand la méthode retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="6947b-116">For example, if the caller passes a local variable expression or an array element access expression, and the called method replaces the object to which the ref parameter refers, then the caller’s local variable or the array element now refers to the new object when the method returns.</span></span>

> [!NOTE]
> <span data-ttu-id="6947b-117">Ne confondez pas le concept de passage par référence avec celui de types de référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-117">Do not confuse the concept of passing by reference with the concept of reference types.</span></span> <span data-ttu-id="6947b-118">Les deux concepts ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="6947b-118">The two concepts are not the same.</span></span> <span data-ttu-id="6947b-119">Un paramètre de méthode peut être modifié par `ref`, qu'il s'agisse d'un type valeur ou d'un type référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-119">A method parameter can be modified by `ref` regardless of whether it is a value type or a reference type.</span></span> <span data-ttu-id="6947b-120">Il n'y a aucun boxing d'un type valeur lorsqu'il est passé par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-120">There is no boxing of a value type when it is passed by reference.</span></span>  

<span data-ttu-id="6947b-121">Pour utiliser un paramètre `ref`, la définition de la méthode et la méthode d'appel doivent utiliser explicitement le mot clé `ref`, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6947b-121">To use a `ref` parameter, both the method definition and the calling method must explicitly use the `ref` keyword, as shown in the following example.</span></span>  

[!code-csharp-interactive[csrefKeywordsMethodParams#6](~/samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#1)]

<span data-ttu-id="6947b-122">Un argument passé à un paramètre `ref` ou `in` doit être initialisé avant d’être transmis.</span><span class="sxs-lookup"><span data-stu-id="6947b-122">An argument that is passed to a `ref` or `in` parameter must be initialized before it is passed.</span></span> <span data-ttu-id="6947b-123">Cette obligation diffère des paramètres [out](out-parameter-modifier.md), dont les arguments ne doivent pas être explicitement initialisés avant d’être passés.</span><span class="sxs-lookup"><span data-stu-id="6947b-123">This differs from [out](out-parameter-modifier.md) parameters, whose arguments do not have to be explicitly initialized before they are passed.</span></span>

<span data-ttu-id="6947b-124">Les membres d’une classe ne peuvent pas avoir de signatures qui diffèrent uniquement par `ref`, `in` ou `out`.</span><span class="sxs-lookup"><span data-stu-id="6947b-124">Members of a class can't have signatures that differ only by `ref`, `in`, or `out`.</span></span> <span data-ttu-id="6947b-125">Une erreur de compilation se produit si la seule différence entre deux membres d’un type est que l’un d’eux a un paramètre `ref` et que l’autre un a un paramètre `out` ou `in`.</span><span class="sxs-lookup"><span data-stu-id="6947b-125">A compiler error occurs if the only difference between two members of a type is that one of them has a `ref` parameter and the other has an `out`, or `in` parameter.</span></span> <span data-ttu-id="6947b-126">Le code suivant, par exemple, ne se compile pas.</span><span class="sxs-lookup"><span data-stu-id="6947b-126">The following code, for example, doesn't compile.</span></span>  

```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on ref and out".
    public void SampleMethod(out int i) { }
    public void SampleMethod(ref int i) { }
}
```

<span data-ttu-id="6947b-127">Toutefois, les méthodes peuvent être surchargées quand une méthode a un paramètre `ref`, `in` ou `out` et que l’autre a un paramètre de valeur, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6947b-127">However, methods can be overloaded when one method has a `ref`, `in`, or `out` parameter and the other has a value parameter, as shown in the following example.</span></span>
  
[!code-csharp[csrefKeywordsMethodParams#6](~/samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#2)]
  
 <span data-ttu-id="6947b-128">Dans d'autres situations nécessitant une correspondance de signature, comme le masquage ou la substitution, `in`, `ref` et `out` font partie de la signature et ne correspondent pas l’un à l’autre.</span><span class="sxs-lookup"><span data-stu-id="6947b-128">In other situations that require signature matching, such as hiding or overriding, `in`, `ref`, and `out` are part of the signature and don't match each other.</span></span>  
  
 <span data-ttu-id="6947b-129">Les propriétés ne sont pas des variables.</span><span class="sxs-lookup"><span data-stu-id="6947b-129">Properties are not variables.</span></span> <span data-ttu-id="6947b-130">Ce sont des méthodes et ne peuvent pas être passées aux paramètres `ref`.</span><span class="sxs-lookup"><span data-stu-id="6947b-130">They are methods, and cannot be passed to `ref` parameters.</span></span>  
  
 <span data-ttu-id="6947b-131">Vous ne pouvez pas utiliser les mots clés `ref`, `in` ou `out` pour les types de méthodes suivants :</span><span class="sxs-lookup"><span data-stu-id="6947b-131">You can't use the `ref`, `in`, and `out` keywords for the following kinds of methods:</span></span>  
  
- <span data-ttu-id="6947b-132">Méthodes async, que vous définissez à l’aide du modificateur [async](async.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-132">Async methods, which you define by using the [async](async.md) modifier.</span></span>  
- <span data-ttu-id="6947b-133">Les méthodes Iterator, qui incluent une instruction [yield return](yield.md) ou `yield break`.</span><span class="sxs-lookup"><span data-stu-id="6947b-133">Iterator methods, which include a [yield return](yield.md) or `yield break` statement.</span></span>  

## <a name="passing-an-argument-by-reference-an-example"></a><span data-ttu-id="6947b-134">Passage d’un argument par référence : exemple</span><span class="sxs-lookup"><span data-stu-id="6947b-134">Passing an argument by reference: An example</span></span>

<span data-ttu-id="6947b-135">Les exemples précédents passent les types valeur par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-135">The previous examples pass value types by reference.</span></span> <span data-ttu-id="6947b-136">Vous pouvez également utiliser le mot clé `ref` pour passer les types référence par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-136">You can also use the `ref` keyword to pass reference types by reference.</span></span> <span data-ttu-id="6947b-137">Le passage d’un type référence par référence permet à la méthode appelée de remplacer l’objet auquel fait référence le paramètre de référence dans l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6947b-137">Passing a reference type by reference enables the called method to replace the object to which the reference parameter refers in the caller.</span></span> <span data-ttu-id="6947b-138">L'emplacement de stockage de l'objet est passé à la méthode comme valeur du paramètre de référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-138">The storage location of the object is passed to the method as the value of the reference parameter.</span></span> <span data-ttu-id="6947b-139">Si vous modifiez la valeur de l'emplacement de stockage du paramètre (pour pointer vers un nouvel objet), vous modifiez également l'emplacement de stockage auquel fait référence l'appelant.</span><span class="sxs-lookup"><span data-stu-id="6947b-139">If you change the value in the storage location of the parameter (to point to a new object), you also change the storage location to which the caller refers.</span></span> <span data-ttu-id="6947b-140">L'exemple suivant passe une instance d'un type référence en tant que paramètre `ref`.</span><span class="sxs-lookup"><span data-stu-id="6947b-140">The following example passes an instance of a reference type as a `ref` parameter.</span></span>
  
[!code-csharp[csrefKeywordsMethodParams#6](~/samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#3)]

<span data-ttu-id="6947b-141">Pour plus d’informations sur la manière de passer des types référence par valeur et par référence, consultez [Passage de paramètres de type référence ](../../programming-guide/classes-and-structs/passing-reference-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-141">For more information about how to pass reference types by value and by reference, see [Passing Reference-Type Parameters](../../programming-guide/classes-and-structs/passing-reference-type-parameters.md).</span></span>
  
## <a name="reference-return-values"></a><span data-ttu-id="6947b-142">Valeurs de retour de référence</span><span class="sxs-lookup"><span data-stu-id="6947b-142">Reference return values</span></span>

<span data-ttu-id="6947b-143">Les valeurs de retour de référence (ou retours ref) sont des valeurs qu’une méthode retourne par référence à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6947b-143">Reference return values (or ref returns) are values that a method returns by reference to the caller.</span></span> <span data-ttu-id="6947b-144">Autrement dit, l’appelant peut modifier la valeur retournée par une méthode, et ce changement est reflété dans l’état de l’objet qui contient la méthode.</span><span class="sxs-lookup"><span data-stu-id="6947b-144">That is, the caller can modify the value returned by a method, and that change is reflected in the state of the object that contains the method.</span></span>

<span data-ttu-id="6947b-145">Une valeur de retour de référence est définie à l’aide du mot clé `ref` :</span><span class="sxs-lookup"><span data-stu-id="6947b-145">A reference return value is defined by using the `ref` keyword:</span></span>

- <span data-ttu-id="6947b-146">Dans la signature de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6947b-146">In the method signature.</span></span> <span data-ttu-id="6947b-147">Par exemple, la signature de méthode suivante indique que la méthode `GetCurrentPrice` retourne une valeur <xref:System.Decimal> par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-147">For example, the following method signature indicates that the `GetCurrentPrice` method returns a <xref:System.Decimal> value by reference.</span></span>

```csharp
public ref decimal GetCurrentPrice()
```

- <span data-ttu-id="6947b-148">Entre le jeton `return` et la variable retournée dans une instruction `return` dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="6947b-148">Between the `return` token and the variable returned in a `return` statement in the method.</span></span> <span data-ttu-id="6947b-149">Exemple :</span><span class="sxs-lookup"><span data-stu-id="6947b-149">For example:</span></span>

```csharp
return ref DecimalArray[0];
```

<span data-ttu-id="6947b-150">Pour que l’appelant puisse modifier l’état de l’objet, la valeur de retour de référence doit être stockée dans une variable qui est explicitement définie comme [variable locale ref](#ref-locals).</span><span class="sxs-lookup"><span data-stu-id="6947b-150">In order for the caller to modify the object's state, the reference return value must be stored to a variable that is explicitly defined as a [ref local](#ref-locals).</span></span>

<span data-ttu-id="6947b-151">Pour obtenir un exemple, consultez [un exemple de retours ref et de variables locales ref](#a-ref-returns-and-ref-locals-example)</span><span class="sxs-lookup"><span data-stu-id="6947b-151">For an example, see [A ref returns and ref locals example](#a-ref-returns-and-ref-locals-example)</span></span>

## <a name="ref-locals"></a><span data-ttu-id="6947b-152">Variables locales ref</span><span class="sxs-lookup"><span data-stu-id="6947b-152">Ref locals</span></span>

<span data-ttu-id="6947b-153">Une variable locale ref est utilisée pour faire référence aux valeurs retournées à l’aide de `return ref`.</span><span class="sxs-lookup"><span data-stu-id="6947b-153">A ref local variable is used to refer to values returned using `return ref`.</span></span> <span data-ttu-id="6947b-154">Vous ne pouvez pas initialiser une variable locale ref en valeur de retour non ref.</span><span class="sxs-lookup"><span data-stu-id="6947b-154">A ref local variable cannot be initialized to a non-ref return value.</span></span> <span data-ttu-id="6947b-155">En d’autres termes, la partie droite de l’initialisation doit être une référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-155">In other words, the right hand side of the initialization must be a reference.</span></span> <span data-ttu-id="6947b-156">Toute modification apportée à la valeur de la variable locale ref est reflétée dans l’état de l’objet dont la méthode a retourné la valeur par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-156">Any modifications to the value of the ref local are reflected in the state of the object whose method returned the value by reference.</span></span>

<span data-ttu-id="6947b-157">Vous définissez une variable locale ref à l’aide du mot clé `ref` avant la déclaration de la variable, ainsi qu’immédiatement avant l’appel à la méthode qui retourne la valeur par référence.</span><span class="sxs-lookup"><span data-stu-id="6947b-157">You define a ref local by using the `ref` keyword before the variable declaration, as well as immediately before the call to the method that returns the value by reference.</span></span>

<span data-ttu-id="6947b-158">Par exemple, l’instruction suivante définit une valeur de variable locale ref qui est retournée par une méthode nommée `GetEstimatedValue` :</span><span class="sxs-lookup"><span data-stu-id="6947b-158">For example, the following statement defines a ref local value that is returned by a method named `GetEstimatedValue`:</span></span>

```csharp
ref decimal estValue = ref Building.GetEstimatedValue();
```

<span data-ttu-id="6947b-159">Vous pouvez accéder à une valeur par référence de la même façon.</span><span class="sxs-lookup"><span data-stu-id="6947b-159">You can access a value by reference in the same way.</span></span> <span data-ttu-id="6947b-160">Dans certains cas, l’accès à une valeur par référence augmente les performances en évitant une opération de copie potentiellement coûteuse.</span><span class="sxs-lookup"><span data-stu-id="6947b-160">In some cases, accessing a value by reference increases performance by avoiding a potentially expensive copy operation.</span></span> <span data-ttu-id="6947b-161">Par exemple, l’instruction suivante montre comment il est possible de définir une valeur locale ref qui est utilisée pour référencer une valeur.</span><span class="sxs-lookup"><span data-stu-id="6947b-161">For example, the following statement shows how one can define a ref local value that is used to reference a value.</span></span>

```csharp
ref VeryLargeStruct reflocal = ref veryLargeStruct;
```

<span data-ttu-id="6947b-162">Notez que dans les deux exemples, le mot clé `ref` doit être utilisé aux deux emplacements, sans quoi le compilateur génère l’erreur CS8172, « Impossible d’initialiser une variable par référence avec une valeur ».</span><span class="sxs-lookup"><span data-stu-id="6947b-162">Note that in both examples the `ref` keyword must be used in both places, or the compiler generates error CS8172, "Cannot initialize a by-reference variable with a value."</span></span>

## <a name="a-ref-returns-and-ref-locals-example"></a><span data-ttu-id="6947b-163">Exemple de retours ref et de variables locales ref</span><span class="sxs-lookup"><span data-stu-id="6947b-163">A ref returns and ref locals example</span></span>

<span data-ttu-id="6947b-164">L’exemple suivant définit une classe `Book` qui a deux champs <xref:System.String>, `Title` et `Author`.</span><span class="sxs-lookup"><span data-stu-id="6947b-164">The following example defines a `Book` class that has two <xref:System.String> fields, `Title` and `Author`.</span></span> <span data-ttu-id="6947b-165">Il définit également une classe `BookCollection` qui inclut un tableau privé d’objets `Book`.</span><span class="sxs-lookup"><span data-stu-id="6947b-165">It also defines a `BookCollection` class that includes a private array of `Book` objects.</span></span> <span data-ttu-id="6947b-166">Des objets livres individuels sont retournés par référence en appelant sa méthode `GetBookByTitle`.</span><span class="sxs-lookup"><span data-stu-id="6947b-166">Individual book objects are returned by reference by calling its `GetBookByTitle` method.</span></span>

[!code-csharp[csrefKeywordsMethodParams#6](~/samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#4)]

<span data-ttu-id="6947b-167">Quand l’appelant stocke la valeur retournée par la méthode `GetBookByTitle` comme variable locale ref, les modifications apportées par l’appelant à la valeur de retour sont reflétées dans l’objet `BookCollection`, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6947b-167">When the caller stores the value returned by the `GetBookByTitle` method as a ref local, changes that the caller makes to the return value are reflected in the `BookCollection` object, as the following example shows.</span></span>

[!code-csharp[csrefKeywordsMethodParams#6](~/samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/RefParameterModifier.cs#5)]

## <a name="c-language-specification"></a><span data-ttu-id="6947b-168">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="6947b-168">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6947b-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6947b-169">See also</span></span>

- [<span data-ttu-id="6947b-170">Sémantique de référence avec les types valeur</span><span class="sxs-lookup"><span data-stu-id="6947b-170">Reference semantics with value types</span></span>](../../reference-semantics-with-value-types.md)  
- [<span data-ttu-id="6947b-171">Passage de paramètres</span><span class="sxs-lookup"><span data-stu-id="6947b-171">Passing Parameters</span></span>](../../programming-guide/classes-and-structs/passing-parameters.md)  
- [<span data-ttu-id="6947b-172">Paramètres de méthodes</span><span class="sxs-lookup"><span data-stu-id="6947b-172">Method Parameters</span></span>](method-parameters.md)  
- [<span data-ttu-id="6947b-173">Référence C#</span><span class="sxs-lookup"><span data-stu-id="6947b-173">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="6947b-174">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="6947b-174">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="6947b-175">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="6947b-175">C# Keywords</span></span>](index.md)