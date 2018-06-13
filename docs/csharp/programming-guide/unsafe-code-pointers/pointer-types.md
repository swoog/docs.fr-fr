---
title: Types pointeur (Guide de programmation C#)
ms.date: 04/20/2018
helpviewer_keywords:
- unsafe code [C#], pointers
- pointers [C#]
ms.openlocfilehash: cbc75a2ec6fe826cb192b1e8bef61c7295f13916
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33337166"
---
# <a name="pointer-types-c-programming-guide"></a><span data-ttu-id="10be4-102">Types pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="10be4-102">Pointer types (C# Programming Guide)</span></span>

<span data-ttu-id="10be4-103">Dans un contexte unsafe, un type peut être un type pointeur, un type valeur ou un type référence.</span><span class="sxs-lookup"><span data-stu-id="10be4-103">In an unsafe context, a type may be a pointer type, a value type, or a reference type.</span></span> <span data-ttu-id="10be4-104">La déclaration d'un type pointeur peut prendre l'une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="10be4-104">A pointer type declaration takes one of the following forms:</span></span>

``` csharp
type* identifier;
void* identifier; //allowed but not recommended
```

<span data-ttu-id="10be4-105">Le type spécifié avant le caractère `*` dans un type de pointeur est appelé le **type référent**.</span><span class="sxs-lookup"><span data-stu-id="10be4-105">The type specified before the `*` in a pointer type is called the **referrent type**.</span></span> <span data-ttu-id="10be4-106">Chacun des types suivants peut être un type référent :</span><span class="sxs-lookup"><span data-stu-id="10be4-106">Any of the following types may be a referrent type:</span></span>

- <span data-ttu-id="10be4-107">Tout type intégral : [sbyte](../../language-reference/keywords/sbyte.md), [byte](../../language-reference/keywords/byte.md), [short](../../language-reference/keywords/short.md), [ushort](../../language-reference/keywords/ushort.md), [int](../../language-reference/keywords/int.md), [uint](../../language-reference/keywords/uint.md), [long](../../language-reference/keywords/long.md), [ulong](../../language-reference/keywords/ulong.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-107">Any integral type: [sbyte](../../language-reference/keywords/sbyte.md), [byte](../../language-reference/keywords/byte.md), [short](../../language-reference/keywords/short.md), [ushort](../../language-reference/keywords/ushort.md), [int](../../language-reference/keywords/int.md), [uint](../../language-reference/keywords/uint.md), [long](../../language-reference/keywords/long.md), [ulong](../../language-reference/keywords/ulong.md).</span></span>
- <span data-ttu-id="10be4-108">Tout type à virgule flottante : [float](../../language-reference/keywords/float.md), [double](../../language-reference/keywords/double.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-108">Any floating point type: [float](../../language-reference/keywords/float.md), [double](../../language-reference/keywords/double.md).</span></span>
- <span data-ttu-id="10be4-109">[char](../../language-reference/keywords/char.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-109">[char](../../language-reference/keywords/char.md).</span></span>
- <span data-ttu-id="10be4-110">[bool](../../language-reference/keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-110">[bool](../../language-reference/keywords/bool.md).</span></span>
- <span data-ttu-id="10be4-111">[decimal](../../language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-111">[decimal](../../language-reference/keywords/decimal.md).</span></span>
- <span data-ttu-id="10be4-112">Tout type [enum](../../language-reference/keywords/enum.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-112">Any [enum](../../language-reference/keywords/enum.md) type.</span></span>
- <span data-ttu-id="10be4-113">Tout type pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-113">Any pointer type.</span></span> <span data-ttu-id="10be4-114">Des expressions comme `void**` sont ainsi autorisées.</span><span class="sxs-lookup"><span data-stu-id="10be4-114">This allows expressions such as `void**`.</span></span>
- <span data-ttu-id="10be4-115">Tout type struct défini par l'utilisateur qui contient des champs de types unmanaged uniquement.</span><span class="sxs-lookup"><span data-stu-id="10be4-115">Any user-defined struct type that contains fields of unmanaged types only.</span></span>

<span data-ttu-id="10be4-116">Les types pointeur n’héritent pas de [object](../../language-reference/keywords/object.md), et aucune conversion n’est possible entre les types pointeur et `object`.</span><span class="sxs-lookup"><span data-stu-id="10be4-116">Pointer types do not inherit from [object](../../language-reference/keywords/object.md) and no conversions exist between pointer types and `object`.</span></span> <span data-ttu-id="10be4-117">Par ailleurs, le boxing et l'unboxing ne prennent pas en charge les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="10be4-117">Also, boxing and unboxing do not support pointers.</span></span> <span data-ttu-id="10be4-118">Cependant, vous pouvez effectuer des conversions entre différents types pointeur ainsi qu'entre des types pointeur et des types intégraux.</span><span class="sxs-lookup"><span data-stu-id="10be4-118">However, you can convert between different pointer types and between pointer types and integral types.</span></span>

<span data-ttu-id="10be4-119">Lorsque vous déclarez plusieurs pointeurs dans la même déclaration, l'astérisque (\*) est écrit conjointement au type sous-jacent uniquement, il n'est pas utilisé en tant que préfixe de chaque nom de pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-119">When you declare multiple pointers in the same declaration, the asterisk (\*) is written together with the underlying type only; it is not used as a prefix to each pointer name.</span></span> <span data-ttu-id="10be4-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="10be4-120">For example:</span></span>

```csharp
int* p1, p2, p3;   // Ok
int *p1, *p2, *p3;   // Invalid in C#
```

<span data-ttu-id="10be4-121">Un pointeur ne peut pas pointer vers une référence ou vers un [struct](../../language-reference/keywords/struct.md) qui contient des références, car une référence d’objet peut être collectée par le récupérateur de mémoire, même si un pointeur pointe vers elle.</span><span class="sxs-lookup"><span data-stu-id="10be4-121">A pointer cannot point to a reference or to a [struct](../../language-reference/keywords/struct.md) that contains references, because an object reference can be garbage collected even if a pointer is pointing to it.</span></span> <span data-ttu-id="10be4-122">Le récupérateur de mémoire ne se préoccupe pas de savoir si un objet est pointé par des types pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-122">The garbage collector does not keep track of whether an object is being pointed to by any pointer types.</span></span>

<span data-ttu-id="10be4-123">La valeur de la variable pointeur de type `myType*` est l'adresse d'une variable de type `myType`.</span><span class="sxs-lookup"><span data-stu-id="10be4-123">The value of the pointer variable of type `myType*` is the address of a variable of type `myType`.</span></span> <span data-ttu-id="10be4-124">Les éléments suivants sont des exemples de déclarations de type pointeur :</span><span class="sxs-lookup"><span data-stu-id="10be4-124">The following are examples of pointer type declarations:</span></span>

|<span data-ttu-id="10be4-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="10be4-125">Example</span></span>|<span data-ttu-id="10be4-126">Description</span><span class="sxs-lookup"><span data-stu-id="10be4-126">Description</span></span>|
|-------------|-----------------|
|`int* p`|<span data-ttu-id="10be4-127">`p` est un pointeur vers un entier.</span><span class="sxs-lookup"><span data-stu-id="10be4-127">`p` is a pointer to an integer.</span></span>|
|`int** p`|<span data-ttu-id="10be4-128">`p` est un pointeur vers un pointeur vers un entier.</span><span class="sxs-lookup"><span data-stu-id="10be4-128">`p` is a pointer to a pointer to an integer.</span></span>|
|`int*[] p`|<span data-ttu-id="10be4-129">`p` est un tableau unidimensionnel de pointeurs vers des entiers.</span><span class="sxs-lookup"><span data-stu-id="10be4-129">`p` is a single-dimensional array of pointers to integers.</span></span>|
|`char* p`|<span data-ttu-id="10be4-130">`p` est un pointeur vers un caractère.</span><span class="sxs-lookup"><span data-stu-id="10be4-130">`p` is a pointer to a char.</span></span>|
|`void* p`|<span data-ttu-id="10be4-131">`p` est un pointeur vers un type inconnu.</span><span class="sxs-lookup"><span data-stu-id="10be4-131">`p` is a pointer to an unknown type.</span></span>|

<span data-ttu-id="10be4-132">L'opérateur d'indirection de pointeur \* peut être utilisé pour accéder au contenu à l'emplacement vers lequel pointe la variable pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-132">The pointer indirection operator \* can be used to access the contents at the location pointed to by the pointer variable.</span></span> <span data-ttu-id="10be4-133">Observez par exemple la déclaration suivante :</span><span class="sxs-lookup"><span data-stu-id="10be4-133">For example, consider the following declaration:</span></span>

```csharp
int* myVariable;
```

<span data-ttu-id="10be4-134">L'expression `*myVariable` désigne la variable `int` trouvée à l'adresse contenue dans `myVariable`.</span><span class="sxs-lookup"><span data-stu-id="10be4-134">The expression `*myVariable` denotes the `int` variable found at the address contained in `myVariable`.</span></span>

<span data-ttu-id="10be4-135">Plusieurs exemples de pointeurs sont présentés dans les rubriques [fixed, instruction](../../language-reference/keywords/fixed-statement.md) et [Conversions de pointeur](../../programming-guide/unsafe-code-pointers/pointer-conversions.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-135">There are several examples of pointers in the topics [fixed Statement](../../language-reference/keywords/fixed-statement.md) and [Pointer Conversions](../../programming-guide/unsafe-code-pointers/pointer-conversions.md).</span></span> <span data-ttu-id="10be4-136">L’exemple suivant utilise le mot clé `unsafe` et les instructions `fixed`, et montre comment incrémenter un pointeur intérieur.</span><span class="sxs-lookup"><span data-stu-id="10be4-136">The following example uses the `unsafe` keyword and the `fixed` statement, and shows how to increment an interior pointer.</span></span>  <span data-ttu-id="10be4-137">Vous pouvez coller ce code dans la fonction Main d'une application console pour l'exécuter.</span><span class="sxs-lookup"><span data-stu-id="10be4-137">You can paste this code into the Main function of a console application to run it.</span></span> <span data-ttu-id="10be4-138">Ces exemples doivent être compilés avec l’ensemble d’options de compilateur [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="10be4-138">These examples must be compiled with the [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md) compiler option set.</span></span>

[!code-csharp[Using pointer types](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#5)]

<span data-ttu-id="10be4-139">L'opérateur d'indirection ne peut pas être appliqué à un pointeur de type `void*`.</span><span class="sxs-lookup"><span data-stu-id="10be4-139">You cannot apply the indirection operator to a pointer of type `void*`.</span></span> <span data-ttu-id="10be4-140">Toutefois, vous pouvez utiliser un cast pour convertir un pointeur void en n'importe quel autre type pointeur, et inversement.</span><span class="sxs-lookup"><span data-stu-id="10be4-140">However, you can use a cast to convert a void pointer to any other pointer type, and vice versa.</span></span>

<span data-ttu-id="10be4-141">Un pointeur peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="10be4-141">A pointer can be `null`.</span></span> <span data-ttu-id="10be4-142">Le fait d'appliquer un opérateur d'indirection à un pointeur Null donne lieu à un comportement défini par l'implémentation.</span><span class="sxs-lookup"><span data-stu-id="10be4-142">Applying the indirection operator to a null pointer causes an implementation-defined behavior.</span></span>

<span data-ttu-id="10be4-143">Le passage de pointeurs entre méthodes peut engendrer un comportement non défini.</span><span class="sxs-lookup"><span data-stu-id="10be4-143">Passing pointers between methods can cause undefined behavior.</span></span> <span data-ttu-id="10be4-144">Supposons une méthode qui retourne un pointeur à une variable locale par le biais d’un paramètre `in`, `out` ou `ref`, ou comme résultat de fonction.</span><span class="sxs-lookup"><span data-stu-id="10be4-144">Consider a method that returns a pointer to a local variable through an `in`, `out`, or `ref` parameter or as the function result.</span></span> <span data-ttu-id="10be4-145">Si le pointeur a été défini dans un bloc fixed, la variable vers laquelle il pointe peut ne plus être fixed.</span><span class="sxs-lookup"><span data-stu-id="10be4-145">If the pointer was set in a fixed block, the variable to which it points may no longer be fixed.</span></span>

<span data-ttu-id="10be4-146">Le tableau suivant répertorie les opérateurs et les instructions qui peuvent fonctionner sur des pointeurs dans un contexte unsafe :</span><span class="sxs-lookup"><span data-stu-id="10be4-146">The following table lists the operators and statements that can operate on pointers in an unsafe context:</span></span>

|<span data-ttu-id="10be4-147">Opérateur/Instruction</span><span class="sxs-lookup"><span data-stu-id="10be4-147">Operator/Statement</span></span>|<span data-ttu-id="10be4-148">Utilisez</span><span class="sxs-lookup"><span data-stu-id="10be4-148">Use</span></span>|
|-------------------------|---------|
|*|<span data-ttu-id="10be4-149">Exécute l'indirection de pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-149">Performs pointer indirection.</span></span>|
|->|<span data-ttu-id="10be4-150">Accède à un membre d'un struct via un pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-150">Accesses a member of a struct through a pointer.</span></span>|
|<span data-ttu-id="10be4-151">[]</span><span class="sxs-lookup"><span data-stu-id="10be4-151">[]</span></span>|<span data-ttu-id="10be4-152">Indexe un pointeur.</span><span class="sxs-lookup"><span data-stu-id="10be4-152">Indexes a pointer.</span></span>|
|`&`|<span data-ttu-id="10be4-153">Obtient l'adresse d'une variable.</span><span class="sxs-lookup"><span data-stu-id="10be4-153">Obtains the address of a variable.</span></span>|
|<span data-ttu-id="10be4-154">++ et --</span><span class="sxs-lookup"><span data-stu-id="10be4-154">++ and --</span></span>|<span data-ttu-id="10be4-155">Incrémente et décrémente les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="10be4-155">Increments and decrements pointers.</span></span>|
|<span data-ttu-id="10be4-156">+ et -</span><span class="sxs-lookup"><span data-stu-id="10be4-156">+ and -</span></span>|<span data-ttu-id="10be4-157">Exécute des opérations arithmétiques sur les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="10be4-157">Performs pointer arithmetic.</span></span>|
|<span data-ttu-id="10be4-158">==, !=, \<, >, \<= et >=</span><span class="sxs-lookup"><span data-stu-id="10be4-158">==, !=, \<, >, \<=, and >=</span></span>|<span data-ttu-id="10be4-159">Compare des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="10be4-159">Compares pointers.</span></span>|
|`stackalloc`|<span data-ttu-id="10be4-160">Alloue de la mémoire sur la pile.</span><span class="sxs-lookup"><span data-stu-id="10be4-160">Allocates memory on the stack.</span></span>|
|<span data-ttu-id="10be4-161">Instruction `fixed`</span><span class="sxs-lookup"><span data-stu-id="10be4-161">`fixed` statement</span></span>|<span data-ttu-id="10be4-162">Résout temporairement une variable afin de pouvoir rechercher son adresse.</span><span class="sxs-lookup"><span data-stu-id="10be4-162">Temporarily fixes a variable so that its address may be found.</span></span>|

## <a name="c-language-specification"></a><span data-ttu-id="10be4-163">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="10be4-163">C# Language Specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="10be4-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10be4-164">See Also</span></span>
 [<span data-ttu-id="10be4-165">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="10be4-165">C# Programming Guide</span></span>](../index.md)  
 [<span data-ttu-id="10be4-166">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="10be4-166">Unsafe Code and Pointers</span></span>](index.md)  
 [<span data-ttu-id="10be4-167">Conversions de pointeurs</span><span class="sxs-lookup"><span data-stu-id="10be4-167">Pointer Conversions</span></span>](pointer-conversions.md)  
 [<span data-ttu-id="10be4-168">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="10be4-168">Pointer Expressions</span></span>](pointer-expressions.md)  
 [<span data-ttu-id="10be4-169">Types</span><span class="sxs-lookup"><span data-stu-id="10be4-169">Types</span></span>](../../language-reference/keywords/types.md)  
 [<span data-ttu-id="10be4-170">unsafe</span><span class="sxs-lookup"><span data-stu-id="10be4-170">unsafe</span></span>](../../language-reference/keywords/unsafe.md)  
 [<span data-ttu-id="10be4-171">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="10be4-171">fixed Statement</span></span>](../../language-reference/keywords/fixed-statement.md)  
 [<span data-ttu-id="10be4-172">stackalloc</span><span class="sxs-lookup"><span data-stu-id="10be4-172">stackalloc</span></span>](../../language-reference/keywords/stackalloc.md)  
 [<span data-ttu-id="10be4-173">Conversion boxing et unboxing</span><span class="sxs-lookup"><span data-stu-id="10be4-173">Boxing and Unboxing</span></span>](../types/boxing-and-unboxing.md)
