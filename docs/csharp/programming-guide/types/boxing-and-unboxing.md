---
title: Boxing et unboxing - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- cs.boxing
helpviewer_keywords:
- C# language, boxing
- C# language, unboxing
- unboxing [C#]
- boxing [C#]
ms.assetid: 8da9bbf4-bce9-4b08-b2e5-f64c11c56514
ms.openlocfilehash: 4fdaea6a9b69f50fa61ee40a43bf34953e72cef1
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237329"
---
# <a name="boxing-and-unboxing-c-programming-guide"></a><span data-ttu-id="4cb59-102">Boxing et unboxing (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="4cb59-102">Boxing and Unboxing (C# Programming Guide)</span></span>
<span data-ttu-id="4cb59-103">Le boxing est la conversion d’un [type valeur](../../../csharp/language-reference/keywords/value-types.md) en type `object` ou en un type interface implémenté par ce type valeur.</span><span class="sxs-lookup"><span data-stu-id="4cb59-103">Boxing is the process of converting a [value type](../../../csharp/language-reference/keywords/value-types.md) to the type `object` or to any interface type implemented by this value type.</span></span> <span data-ttu-id="4cb59-104">Lorsque le CLR exécute un boxing d’un type valeur, il inclut la valeur dans un wrapper, à l’intérieur d’un System.Object, et la stocke sur le tas managé.</span><span class="sxs-lookup"><span data-stu-id="4cb59-104">When the CLR boxes a value type, it wraps the value inside a System.Object and stores it on the managed heap.</span></span> <span data-ttu-id="4cb59-105">L'unboxing extrait le type valeur de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4cb59-105">Unboxing extracts the value type from the object.</span></span> <span data-ttu-id="4cb59-106">La conversion boxing est implicite ; la conversion unboxing est explicite.</span><span class="sxs-lookup"><span data-stu-id="4cb59-106">Boxing is implicit; unboxing is explicit.</span></span> <span data-ttu-id="4cb59-107">Le concept de boxing et de unboxing repose sur la vue unifiée par C# du système de type, dans lequel une valeur de n'importe quel type peut être traitée en tant qu'objet.</span><span class="sxs-lookup"><span data-stu-id="4cb59-107">The concept of boxing and unboxing underlies the C# unified view of the type system in which a value of any type can be treated as an object.</span></span>  
  
 <span data-ttu-id="4cb59-108">Dans l’exemple suivant, la variable de type entier `i` est convertie (*boxed*) et assignée à l’objet `o`.</span><span class="sxs-lookup"><span data-stu-id="4cb59-108">In the following example, the integer variable `i` is *boxed* and assigned to object `o`.</span></span>  
  
 [!code-csharp[csProgGuideTypes#14](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_1.cs)]  
  
 <span data-ttu-id="4cb59-109">L’objet `o` peut ensuite être unboxed et assigné à la variable de type entier `i` :</span><span class="sxs-lookup"><span data-stu-id="4cb59-109">The object `o` can then be unboxed and assigned to integer variable `i`:</span></span>  
  
 [!code-csharp[csProgGuideTypes#15](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_2.cs)]  
  
 <span data-ttu-id="4cb59-110">Les exemples suivants montrent comment le boxing est utilisé dans C#.</span><span class="sxs-lookup"><span data-stu-id="4cb59-110">The following examples illustrate how boxing is used in C#.</span></span>  
  
 [!code-csharp[csProgGuideTypes#47](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_3.cs)]  
  
## <a name="performance"></a><span data-ttu-id="4cb59-111">Performances</span><span class="sxs-lookup"><span data-stu-id="4cb59-111">Performance</span></span>  
 <span data-ttu-id="4cb59-112">Par rapport aux assignations simples, le boxing et l'unboxing sont des processus qui coûtent cher en calcul.</span><span class="sxs-lookup"><span data-stu-id="4cb59-112">In relation to simple assignments, boxing and unboxing are computationally expensive processes.</span></span> <span data-ttu-id="4cb59-113">Lorsqu'un type valeur est boxed, un nouvel objet doit être alloué et construit.</span><span class="sxs-lookup"><span data-stu-id="4cb59-113">When a value type is boxed, a new object must be allocated and constructed.</span></span> <span data-ttu-id="4cb59-114">À un degré moindre, le cast requis pour l'unboxing coûte également cher en calcul.</span><span class="sxs-lookup"><span data-stu-id="4cb59-114">To a lesser degree, the cast required for unboxing is also expensive computationally.</span></span> <span data-ttu-id="4cb59-115">Pour plus d’informations, consultez [Performances](../../../../docs/framework/performance/performance-tips.md).</span><span class="sxs-lookup"><span data-stu-id="4cb59-115">For more information, see [Performance](../../../../docs/framework/performance/performance-tips.md).</span></span>  
  
## <a name="boxing"></a><span data-ttu-id="4cb59-116">Boxing</span><span class="sxs-lookup"><span data-stu-id="4cb59-116">Boxing</span></span>  
 <span data-ttu-id="4cb59-117">Le boxing est utilisé pour stocker des types valeur dans le tas rassemblé par garbage collection.</span><span class="sxs-lookup"><span data-stu-id="4cb59-117">Boxing is used to store value types in the garbage-collected heap.</span></span> <span data-ttu-id="4cb59-118">Le boxing est une conversion implicite d’un [type valeur](../../../csharp/language-reference/keywords/value-types.md) en type `object` ou en un type interface implémenté par ce type valeur.</span><span class="sxs-lookup"><span data-stu-id="4cb59-118">Boxing is an implicit conversion of a [value type](../../../csharp/language-reference/keywords/value-types.md) to the type `object` or to any interface type implemented by this value type.</span></span> <span data-ttu-id="4cb59-119">Le boxing d'un type valeur alloue une instance d'objet sur le tas et copie la valeur dans le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="4cb59-119">Boxing a value type allocates an object instance on the heap and copies the value into the new object.</span></span>  
  
 <span data-ttu-id="4cb59-120">Dans l'exemple suivant, une variable de type valeur est déclarée :</span><span class="sxs-lookup"><span data-stu-id="4cb59-120">Consider the following declaration of a value-type variable:</span></span>  
  
 [!code-csharp[csProgGuideTypes#17](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_4.cs)]  
  
 <span data-ttu-id="4cb59-121">L'instruction ci-dessous réalise implicitement une opération de boxing sur la variable `i` :</span><span class="sxs-lookup"><span data-stu-id="4cb59-121">The following statement implicitly applies the boxing operation on the variable `i`:</span></span>  
  
 [!code-csharp[csProgGuideTypes#18](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_5.cs)]  
  
 <span data-ttu-id="4cb59-122">Le résultat de cette instruction crée, sur la pile, un objet `o` qui fait référence à une valeur de type `int` sur le tas.</span><span class="sxs-lookup"><span data-stu-id="4cb59-122">The result of this statement is creating an object reference `o`, on the stack, that references a value of the type `int`, on the heap.</span></span> <span data-ttu-id="4cb59-123">Cette valeur est une copie de la valeur de type valeur qui a été assignée à la variable `i`.</span><span class="sxs-lookup"><span data-stu-id="4cb59-123">This value is a copy of the value-type value assigned to the variable `i`.</span></span> <span data-ttu-id="4cb59-124">La différence entre les deux variables, `i` et `o`, est illustrée dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4cb59-124">The difference between the two variables, `i` and `o`, is illustrated in the following figure.</span></span>  
  
 <span data-ttu-id="4cb59-125">![Graphique d’une conversion boxing](../../../csharp/programming-guide/types/media/vcboxingconversion.gif "vcBoxingConversion")</span><span class="sxs-lookup"><span data-stu-id="4cb59-125">![BoxingConversion graphic](../../../csharp/programming-guide/types/media/vcboxingconversion.gif "vcBoxingConversion")</span></span>  
<span data-ttu-id="4cb59-126">Conversion boxing</span><span class="sxs-lookup"><span data-stu-id="4cb59-126">Boxing Conversion</span></span>  
  
 <span data-ttu-id="4cb59-127">Il est également possible, mais jamais obligatoire, d'effectuer un boxing explicite comme dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4cb59-127">It is also possible to perform the boxing explicitly as in the following example, but explicit boxing is never required:</span></span>  
  
 [!code-csharp[csProgGuideTypes#19](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_6.cs)]  
  
## <a name="description"></a><span data-ttu-id="4cb59-128">Description</span><span class="sxs-lookup"><span data-stu-id="4cb59-128">Description</span></span>  
 <span data-ttu-id="4cb59-129">Cet exemple utilise le boxing pour convertir une variable `i` (entier) en un objet `o`.</span><span class="sxs-lookup"><span data-stu-id="4cb59-129">This example converts an integer variable `i` to an object `o` by using boxing.</span></span> <span data-ttu-id="4cb59-130">Ensuite, la valeur `i` stockée dans la variable `123` est remplacée par la valeur `456`.</span><span class="sxs-lookup"><span data-stu-id="4cb59-130">Then, the value stored in the variable `i` is changed from `123` to `456`.</span></span> <span data-ttu-id="4cb59-131">L'exemple montre que le type valeur d'origine et que l'objet boxed utilisent des emplacements de mémoire distincts et peuvent, par conséquent, stocker des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="4cb59-131">The example shows that the original value type and the boxed object use separate memory locations, and therefore can store different values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4cb59-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="4cb59-132">Example</span></span>  
 [!code-csharp[csProgGuideTypes#16](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_7.cs)]  
  
## <a name="unboxing"></a><span data-ttu-id="4cb59-133">Unboxing</span><span class="sxs-lookup"><span data-stu-id="4cb59-133">Unboxing</span></span>  
 <span data-ttu-id="4cb59-134">L’unboxing est une conversion explicite du type `object` en un [type valeur](../../../csharp/language-reference/keywords/value-types.md), ou d’un type interface en un type valeur qui implémente l’interface.</span><span class="sxs-lookup"><span data-stu-id="4cb59-134">Unboxing is an explicit conversion from the type `object` to a [value type](../../../csharp/language-reference/keywords/value-types.md) or from an interface type to a value type that implements the interface.</span></span> <span data-ttu-id="4cb59-135">Une opération d'unboxing comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cb59-135">An unboxing operation consists of:</span></span>  
  
-   <span data-ttu-id="4cb59-136">Vérification de l'instance de l'objet pour s'assurer qu'il s'agit bien d'une valeur boxed du type valeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4cb59-136">Checking the object instance to make sure that it is a boxed value of the given value type.</span></span>  
  
-   <span data-ttu-id="4cb59-137">Copie de la valeur de l'instance dans la variable de type valeur.</span><span class="sxs-lookup"><span data-stu-id="4cb59-137">Copying the value from the instance into the value-type variable.</span></span>  
  
 <span data-ttu-id="4cb59-138">Les instructions suivantes expliquent les opérations de boxing et d'unboxing :</span><span class="sxs-lookup"><span data-stu-id="4cb59-138">The following statements demonstrate both boxing and unboxing operations:</span></span>  
  
 [!code-csharp[csProgGuideTypes#21](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_8.cs)]  
  
 <span data-ttu-id="4cb59-139">Le résultat de ces instructions est illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4cb59-139">The following figure demonstrates the result of the previous statements.</span></span>  
  
 <span data-ttu-id="4cb59-140">![Graphique de conversion unboxing](../../../csharp/programming-guide/types/media/vcunboxingconversion.gif "vcUnBoxingConversion")</span><span class="sxs-lookup"><span data-stu-id="4cb59-140">![UnBoxing Conversion graphic](../../../csharp/programming-guide/types/media/vcunboxingconversion.gif "vcUnBoxingConversion")</span></span>  
<span data-ttu-id="4cb59-141">Conversion unboxing</span><span class="sxs-lookup"><span data-stu-id="4cb59-141">Unboxing Conversion</span></span>  
  
 <span data-ttu-id="4cb59-142">Pour que l'unboxing de types valeur réussisse au moment de l'exécution, l'élément qui est unboxed doit être une référence à un objet précédemment créé par boxing d'une instance de ce type valeur.</span><span class="sxs-lookup"><span data-stu-id="4cb59-142">For the unboxing of value types to succeed at run time, the item being unboxed must be a reference to an object that was previously created by boxing an instance of that value type.</span></span> <span data-ttu-id="4cb59-143">La tentative d'extraction de `null` provoque un <xref:System.NullReferenceException>.</span><span class="sxs-lookup"><span data-stu-id="4cb59-143">Attempting to unbox `null` causes a <xref:System.NullReferenceException>.</span></span> <span data-ttu-id="4cb59-144">La tentative d'extraction d'une référence vers un type de valeur incompatible provoque un <xref:System.InvalidCastException>.</span><span class="sxs-lookup"><span data-stu-id="4cb59-144">Attempting to unbox a reference to an incompatible value type causes an <xref:System.InvalidCastException>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4cb59-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="4cb59-145">Example</span></span>  
 <span data-ttu-id="4cb59-146">L'exemple suivant montre un cas d'unboxing non valide et l'`InvalidCastException` qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="4cb59-146">The following example demonstrates a case of invalid unboxing and the resulting `InvalidCastException`.</span></span> <span data-ttu-id="4cb59-147">Avec `try` et `catch`, un message d'erreur est affiché lorsque l'erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="4cb59-147">Using `try` and `catch`, an error message is displayed when the error occurs.</span></span>  
  
 [!code-csharp[csProgGuideTypes#20](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/boxing-and-unboxing_9.cs)]  
  
 <span data-ttu-id="4cb59-148">Sortie de ce programme :</span><span class="sxs-lookup"><span data-stu-id="4cb59-148">This program outputs:</span></span>  
  
 `Specified cast is not valid. Error: Incorrect unboxing.`  
  
 <span data-ttu-id="4cb59-149">Si vous modifiez l'instruction :</span><span class="sxs-lookup"><span data-stu-id="4cb59-149">If you change the statement:</span></span>  
  
```csharp
int j = (short) o;  
```  
  
 <span data-ttu-id="4cb59-150">en :</span><span class="sxs-lookup"><span data-stu-id="4cb59-150">to:</span></span>  
  
```csharp
int j = (int) o;  
```  
  
 <span data-ttu-id="4cb59-151">la conversion sera réalisée, avec le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="4cb59-151">the conversion will be performed, and you will get the output:</span></span>  
  
 `Unboxing OK.`  
  
## <a name="c-language-specification"></a><span data-ttu-id="4cb59-152">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="4cb59-152">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="related-sections"></a><span data-ttu-id="4cb59-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4cb59-153">Related Sections</span></span>  
 <span data-ttu-id="4cb59-154">Pour plus d'informations :</span><span class="sxs-lookup"><span data-stu-id="4cb59-154">For more information:</span></span>  
  
-   [<span data-ttu-id="4cb59-155">Types référence</span><span class="sxs-lookup"><span data-stu-id="4cb59-155">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)  
  
-   [<span data-ttu-id="4cb59-156">Types valeur</span><span class="sxs-lookup"><span data-stu-id="4cb59-156">Value Types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
  
## <a name="see-also"></a><span data-ttu-id="4cb59-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cb59-157">See Also</span></span>

- [<span data-ttu-id="4cb59-158">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4cb59-158">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
