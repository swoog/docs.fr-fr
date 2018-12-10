---
title: out, modificateur de paramètre (référence C#)
ms.date: 03/06/2018
helpviewer_keywords:
- parameters [C#], out
- out parameters [C#]
ms.openlocfilehash: 58654133b7bd7197502ec1550bc78c99aeb0bf0e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155299"
---
# <a name="out-parameter-modifier-c-reference"></a><span data-ttu-id="c73aa-102">out, modificateur de paramètre (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c73aa-102">out parameter modifier (C# Reference)</span></span>
<span data-ttu-id="c73aa-103">Le mot clé `out` entraîne le passage des arguments par référence.</span><span class="sxs-lookup"><span data-stu-id="c73aa-103">The `out` keyword causes arguments to be passed by reference.</span></span> <span data-ttu-id="c73aa-104">Il est similaire au mot clé [ref](ref.md), à la différence que `ref` nécessite que la variable soit initialisée avant d’être passée.</span><span class="sxs-lookup"><span data-stu-id="c73aa-104">It is like the [ref](ref.md) keyword, except that `ref` requires that the variable be initialized before it is passed.</span></span> <span data-ttu-id="c73aa-105">Il est également similaire au mot clé [in](in-parameter-modifier.md), à la différence que `in` n’autorise pas la méthode appelée à modifier la valeur d’argument.</span><span class="sxs-lookup"><span data-stu-id="c73aa-105">It is also like the [in](in-parameter-modifier.md) keyword, except that `in` does not allow the called method to modify the argument value.</span></span> <span data-ttu-id="c73aa-106">Pour utiliser un paramètre `out`, la définition de la méthode et la méthode d'appel doivent utiliser explicitement le mot clé `out`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-106">To use an `out` parameter, both the method definition and the calling method must explicitly use the `out` keyword.</span></span> <span data-ttu-id="c73aa-107">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c73aa-107">For example:</span></span>  
  
[!code-csharp-interactive[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#1)]  

> [!NOTE] 
> <span data-ttu-id="c73aa-108">Le mot clé `out` peut également être utilisé avec un paramètre de type générique pour spécifier que le paramètre de type est covariant.</span><span class="sxs-lookup"><span data-stu-id="c73aa-108">The `out` keyword can also be used with a generic type parameter to specify that the type parameter is covariant.</span></span> <span data-ttu-id="c73aa-109">Pour plus d’informations sur l’utilisation du mot clé `out` dans ce contexte, consultez [out, modificateur générique](out-generic-modifier.md).</span><span class="sxs-lookup"><span data-stu-id="c73aa-109">For more information on the use of the `out` keyword in this context, see [out (Generic Modifier)](out-generic-modifier.md).</span></span>
  
<span data-ttu-id="c73aa-110">Les variables passées comme arguments `out` n’ont pas à être initialisées avant d’être passées dans un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="c73aa-110">Variables passed as `out` arguments do not have to be initialized before being passed in a method call.</span></span> <span data-ttu-id="c73aa-111">Toutefois, la méthode appelée doit assigner une valeur avant le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c73aa-111">However, the called method is required to assign a value before the method returns.</span></span>  
  
<span data-ttu-id="c73aa-112">Bien que les mots clés `in`, `ref` et `out` entraînent un comportement différent au moment de l’exécution, ils ne sont pas considérés comme faisant partie de la signature de la méthode au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="c73aa-112">Although the `in`, `ref`, and `out` keywords cause different run-time behavior, they are not considered part of the method signature at compile time.</span></span> <span data-ttu-id="c73aa-113">Par conséquent, les méthodes ne peuvent pas être surchargées si la seule différence est que l’une d’elles accepte un argument `ref` ou `in` et que l’autre accepte un argument `out`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-113">Therefore, methods cannot be overloaded if the only difference is that one method takes a `ref` or `in` argument and the other takes an `out` argument.</span></span> <span data-ttu-id="c73aa-114">Le code suivant, par exemple, ne se compilera pas :</span><span class="sxs-lookup"><span data-stu-id="c73aa-114">The following code, for example, will not compile:</span></span>  
  
```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on ref and out".
    public void SampleMethod(out int i) { }
    public void SampleMethod(ref int i) { }
}
```
  
<span data-ttu-id="c73aa-115">Toutefois, la surcharge est autorisée si une méthode prend un argument `ref`, `in` ou `out`, et que l’autre méthode n’a aucun de ces modificateurs, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c73aa-115">Overloading is legal, however, if one method takes a `ref`, `in`, or `out` argument and the other has none of those modifiers, like this:</span></span>  
  
[!code-csharp[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#2)]  

<span data-ttu-id="c73aa-116">Le compilateur choisit la meilleure surcharge en mettant en correspondance les modificateurs de paramètre sur le site d’appel et les modificateurs de paramètre utilisés dans l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="c73aa-116">The compiler chooses the best overload by matching the parameter modifiers at the call site to the parameter modifiers used in the method call.</span></span>
 
<span data-ttu-id="c73aa-117">Les propriétés ne sont pas des variables et, par conséquent, ne peuvent pas être passées en tant que paramètres `out`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-117">Properties are not variables and therefore cannot be passed as `out` parameters.</span></span>
  
<span data-ttu-id="c73aa-118">Vous ne pouvez pas utiliser les mots clés `in`, `ref` ou `out` pour les types de méthodes suivants :</span><span class="sxs-lookup"><span data-stu-id="c73aa-118">You can't use the `in`, `ref`, and `out` keywords for the following kinds of methods:</span></span>  
  
-   <span data-ttu-id="c73aa-119">Méthodes async, que vous définissez à l’aide du modificateur [async](../../../csharp/language-reference/keywords/async.md).</span><span class="sxs-lookup"><span data-stu-id="c73aa-119">Async methods, which you define by using the [async](../../../csharp/language-reference/keywords/async.md) modifier.</span></span>  
  
-   <span data-ttu-id="c73aa-120">Les méthodes Iterator, qui incluent une instruction [yield return](../../../csharp/language-reference/keywords/yield.md) ou `yield break`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-120">Iterator methods, which include a [yield return](../../../csharp/language-reference/keywords/yield.md) or `yield break` statement.</span></span>  

## <a name="declaring-out-arguments"></a><span data-ttu-id="c73aa-121">Déclaration d’arguments `out`</span><span class="sxs-lookup"><span data-stu-id="c73aa-121">Declaring `out` arguments</span></span>   

 <span data-ttu-id="c73aa-122">La déclaration d’une méthode avec des arguments `out` est utile lorsque vous souhaitez qu’une méthode retourne plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="c73aa-122">Declaring a method with `out` arguments is useful when you want a method to return multiple values.</span></span> <span data-ttu-id="c73aa-123">L'exemple suivant utilise `out` pour retourner trois variables avec un seul appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="c73aa-123">The following example uses `out` to return three variables with a single method call.</span></span> <span data-ttu-id="c73aa-124">Notez que le troisième argument reçoit la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c73aa-124">Note that the third argument is assigned to null.</span></span> <span data-ttu-id="c73aa-125">Cela permet aux méthodes de retourner des valeurs le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c73aa-125">This enables methods to return values optionally.</span></span>  
  
[!code-csharp-interactive[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#3)]  

 <span data-ttu-id="c73aa-126">Le [modèle Try](/visualstudio/code-quality/ca1021-avoid-out-parameters#try-pattern-methods) consiste à retourner une valeur `bool` qui indique si une opération a réussi ou échoué et à retourner le résultat de l’opération dans un argument `out`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-126">The [Try pattern](/visualstudio/code-quality/ca1021-avoid-out-parameters#try-pattern-methods) involves returning a `bool` to indicate whether an operation succeeded or failed, and returning the value produced by the operation in an `out` argument.</span></span> <span data-ttu-id="c73aa-127">Un certain nombre de méthodes d’analyse, notamment la méthode [DateTime.TryParse](xref:System.DateTime.TryParse(System.String,System.DateTime@)), utilisent ce modèle.</span><span class="sxs-lookup"><span data-stu-id="c73aa-127">A number of parsing methods, such as the [DateTime.TryParse](xref:System.DateTime.TryParse(System.String,System.DateTime@)) method, use this pattern.</span></span>
   
## <a name="calling-a-method-with-an-out-argument"></a><span data-ttu-id="c73aa-128">Appel d’une méthode avec un argument `out`</span><span class="sxs-lookup"><span data-stu-id="c73aa-128">Calling a method with an `out` argument</span></span>

<span data-ttu-id="c73aa-129">Dans C# 6 et les versions antérieures, vous devez déclarer une variable dans une instruction distincte avant de la passer comme argument `out`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-129">In C# 6 and earlier, you must declare a variable in a separate statement before you pass it as an `out` argument.</span></span> <span data-ttu-id="c73aa-130">L’exemple suivant déclare une variable nommée `number` avant de la passer à la méthode [Int32.TryParse](xref:System.Int32.TryParse(System.String,System.Int32@)), qui tente de convertir une chaîne en nombre.</span><span class="sxs-lookup"><span data-stu-id="c73aa-130">The following example declares a variable named `number` before it is passed to the [Int32.TryParse](xref:System.Int32.TryParse(System.String,System.Int32@)) method, which attempts to convert a string to a number.</span></span>

[!code-csharp-interactive[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#4)]  

<span data-ttu-id="c73aa-131">À compter de C# 7.0, vous pouvez déclarer la variable `out` dans la liste d’arguments de l’appel de méthode au lieu de le faire dans une déclaration de variable distincte.</span><span class="sxs-lookup"><span data-stu-id="c73aa-131">Starting with C# 7.0, you can declare the `out` variable in the argument list of the method call, rather than in a separate variable declaration.</span></span> <span data-ttu-id="c73aa-132">Cette technique rend le code plus simple et plus lisible, et vous empêche également d’assigner par inadvertance une valeur à la variable avant l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="c73aa-132">This produces more compact, readable code, and also prevents you from inadvertently assigning a value to the variable before the method call.</span></span> <span data-ttu-id="c73aa-133">L’exemple suivant est semblable au précédent, sauf qu’il définit la variable `number` dans l’appel de la méthode [Int32.TryParse](xref:System.Int32.TryParse(System.String,System.Int32@)).</span><span class="sxs-lookup"><span data-stu-id="c73aa-133">The following example is like the previous example, except that it defines the `number` variable in the call to the [Int32.TryParse](xref:System.Int32.TryParse(System.String,System.Int32@)) method.</span></span>

[!code-csharp-interactive[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#5)]  
   
<span data-ttu-id="c73aa-134">Dans l’exemple précédent, la variable `number` est fortement typée en `int`.</span><span class="sxs-lookup"><span data-stu-id="c73aa-134">In the previous example, the `number` variable is strongly typed as an `int`.</span></span> <span data-ttu-id="c73aa-135">Vous pouvez également déclarer une variable locale implicitement typée, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c73aa-135">You can also declare an implicitly typed local variable, as the following example does.</span></span>

[!code-csharp-interactive[cs-out-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/OutParameterModifier.cs#6)]  
   
## <a name="c-language-specification"></a><span data-ttu-id="c73aa-136">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="c73aa-136">C# Language Specification</span></span>  
[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c73aa-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c73aa-137">See Also</span></span>

- [<span data-ttu-id="c73aa-138">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c73aa-138">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="c73aa-139">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c73aa-139">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="c73aa-140">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="c73aa-140">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="c73aa-141">Paramètres de méthodes</span><span class="sxs-lookup"><span data-stu-id="c73aa-141">Method Parameters</span></span>](../../../csharp/language-reference/keywords/method-parameters.md)
