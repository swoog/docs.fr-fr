---
title: class (référence C#)
ms.date: 07/18/2017
f1_keywords:
- class_CSharpKeyword
- class
helpviewer_keywords:
- class keyword [C#]
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
ms.openlocfilehash: 20968d2f72195db6d16de1b726c6e946b91ffcd5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="class-c-reference"></a><span data-ttu-id="c4d80-102">class (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c4d80-102">class (C# Reference)</span></span>

<span data-ttu-id="c4d80-103">Les classes sont déclarées à l’aide du mot clé `class`, comme l’illustre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c4d80-103">Classes are declared using the keyword `class`, as shown in the following example:</span></span>

```csharp
class TestClass
{
    // Methods, properties, fields, events, delegates 
    // and nested classes go here.
}
```

## <a name="remarks"></a><span data-ttu-id="c4d80-104">Notes</span><span class="sxs-lookup"><span data-stu-id="c4d80-104">Remarks</span></span>
<span data-ttu-id="c4d80-105">Le langage C# ne permet qu'un seul héritage.</span><span class="sxs-lookup"><span data-stu-id="c4d80-105">Only single inheritance is allowed in C#.</span></span> <span data-ttu-id="c4d80-106">Cela signifie qu’une classe peut uniquement hériter de l’implémentation d’une seule classe de base.</span><span class="sxs-lookup"><span data-stu-id="c4d80-106">In other words, a class can inherit implementation from one base class only.</span></span> <span data-ttu-id="c4d80-107">Toutefois, une classe peut implémenter plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="c4d80-107">However, a class can implement more than one interface.</span></span> <span data-ttu-id="c4d80-108">Le tableau suivant répertorie des exemples d’héritage de classe et d’implémentation d’interface :</span><span class="sxs-lookup"><span data-stu-id="c4d80-108">The following table shows examples of class inheritance and interface implementation:</span></span>

|<span data-ttu-id="c4d80-109">Héritage</span><span class="sxs-lookup"><span data-stu-id="c4d80-109">Inheritance</span></span>|<span data-ttu-id="c4d80-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4d80-110">Example</span></span>|
|-----------------|-------------|
|<span data-ttu-id="c4d80-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c4d80-111">None</span></span>|`class ClassA { }`|
|<span data-ttu-id="c4d80-112">Single</span><span class="sxs-lookup"><span data-stu-id="c4d80-112">Single</span></span>|`class DerivedClass: BaseClass { }`|
|<span data-ttu-id="c4d80-113">Aucun, implémente deux interfaces</span><span class="sxs-lookup"><span data-stu-id="c4d80-113">None, implements two interfaces</span></span>|`class ImplClass: IFace1, IFace2 { }`|
|<span data-ttu-id="c4d80-114">Unique, implémente une seule interface</span><span class="sxs-lookup"><span data-stu-id="c4d80-114">Single, implements one interface</span></span>|`class ImplDerivedClass: BaseClass, IFace1 { }`|

<span data-ttu-id="c4d80-115">Les classes que vous déclarez directement dans un espace de noms, non imbriquées dans d’autres classes, peuvent être [public](../../../csharp/language-reference/keywords/public.md) ou [internal](../../../csharp/language-reference/keywords/internal.md).</span><span class="sxs-lookup"><span data-stu-id="c4d80-115">Classes that you declare directly within a namespace, not nested within other classes, can be either [public](../../../csharp/language-reference/keywords/public.md) or [internal](../../../csharp/language-reference/keywords/internal.md).</span></span> <span data-ttu-id="c4d80-116">Par défaut, les classes sont `internal`.</span><span class="sxs-lookup"><span data-stu-id="c4d80-116">Classes are `internal` by default.</span></span>

<span data-ttu-id="c4d80-117">Les membres de classe, notamment les classes imbriquées, peuvent être [public](../../../csharp/language-reference/keywords/public.md), `protected internal`, [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [private](../../../csharp/language-reference/keywords/private.md) ou `private protected`.</span><span class="sxs-lookup"><span data-stu-id="c4d80-117">Class members, including nested classes, can be [public](../../../csharp/language-reference/keywords/public.md), `protected internal`, [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [private](../../../csharp/language-reference/keywords/private.md), or `private protected`.</span></span> <span data-ttu-id="c4d80-118">Par défaut, les membres sont [private](../../../csharp/language-reference/keywords/private.md).</span><span class="sxs-lookup"><span data-stu-id="c4d80-118">Members are [private](../../../csharp/language-reference/keywords/private.md) by default.</span></span>

<span data-ttu-id="c4d80-119">Pour plus d’informations, consultez la page [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c4d80-119">For more information, see [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span></span>

<span data-ttu-id="c4d80-120">Vous pouvez déclarer des classes génériques qui ont des paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="c4d80-120">You can declare generic classes that have type parameters.</span></span> <span data-ttu-id="c4d80-121">Pour plus d’informations, consultez [Classes génériques](../../../csharp/programming-guide/generics/generic-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c4d80-121">For more information, see [Generic Classes](../../../csharp/programming-guide/generics/generic-classes.md).</span></span>

<span data-ttu-id="c4d80-122">Une classe peut contenir les déclarations des membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4d80-122">A class can contain declarations of the following members:</span></span>

- [<span data-ttu-id="c4d80-123">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="c4d80-123">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)

- [<span data-ttu-id="c4d80-124">Constantes</span><span class="sxs-lookup"><span data-stu-id="c4d80-124">Constants</span></span>](../../../csharp/programming-guide/classes-and-structs/constants.md)

- [<span data-ttu-id="c4d80-125">Champs</span><span class="sxs-lookup"><span data-stu-id="c4d80-125">Fields</span></span>](../../../csharp/programming-guide/classes-and-structs/fields.md)

- [<span data-ttu-id="c4d80-126">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="c4d80-126">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)

- [<span data-ttu-id="c4d80-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4d80-127">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)

- [<span data-ttu-id="c4d80-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4d80-128">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)

- [<span data-ttu-id="c4d80-129">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="c4d80-129">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)

- [<span data-ttu-id="c4d80-130">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="c4d80-130">Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/operators.md)

- [<span data-ttu-id="c4d80-131">Événements</span><span class="sxs-lookup"><span data-stu-id="c4d80-131">Events</span></span>](../../../csharp/programming-guide/events/index.md)

- [<span data-ttu-id="c4d80-132">Délégués</span><span class="sxs-lookup"><span data-stu-id="c4d80-132">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)

- [<span data-ttu-id="c4d80-133">Classes</span><span class="sxs-lookup"><span data-stu-id="c4d80-133">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)

- [<span data-ttu-id="c4d80-134">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c4d80-134">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)

- [<span data-ttu-id="c4d80-135">Structs</span><span class="sxs-lookup"><span data-stu-id="c4d80-135">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)

## <a name="example"></a><span data-ttu-id="c4d80-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4d80-136">Example</span></span>
<span data-ttu-id="c4d80-137">L’exemple suivant explique comment déclarer des champs, des constructeurs et des méthodes de classe.</span><span class="sxs-lookup"><span data-stu-id="c4d80-137">The following example demonstrates declaring class fields, constructors, and methods.</span></span> <span data-ttu-id="c4d80-138">Il illustre également l’instanciation d’un objet et l’impression des données d’une instance.</span><span class="sxs-lookup"><span data-stu-id="c4d80-138">It also demonstrates object instantiation and printing instance data.</span></span> <span data-ttu-id="c4d80-139">Dans cet exemple, deux classes sont déclarées.</span><span class="sxs-lookup"><span data-stu-id="c4d80-139">In this example, two classes are declared.</span></span> <span data-ttu-id="c4d80-140">La première, `Child`, contient deux champs privés (`name` et `age`), deux constructeurs publics et une méthode publique.</span><span class="sxs-lookup"><span data-stu-id="c4d80-140">The first class, `Child`, contains two private fields (`name` and `age`), two public constructors and one public method.</span></span> <span data-ttu-id="c4d80-141">La deuxième, `StringTest`, contient `Main`.</span><span class="sxs-lookup"><span data-stu-id="c4d80-141">The second class, `StringTest`, is used to contain `Main`.</span></span>

[!code-csharp[csrefKeywordsTypes#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/class_1.cs)]

## <a name="comments"></a><span data-ttu-id="c4d80-142">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c4d80-142">Comments</span></span>
<span data-ttu-id="c4d80-143">Notez que, dans l’exemple précédant, les champs privés (`name` et `age`) ne sont accessibles que par le biais de la méthode publique de la classe `Child`.</span><span class="sxs-lookup"><span data-stu-id="c4d80-143">Notice that in the previous example the private fields (`name` and `age`) can only be accessed through the public method of the `Child` class.</span></span> <span data-ttu-id="c4d80-144">Par exemple, vous ne pouvez pas imprimer le nom de l’enfant à partir de la méthode `Main` en utilisant une instruction comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="c4d80-144">For example, you cannot print the child's name, from the `Main` method, using a statement like this:</span></span>

```csharp
Console.Write(child1.name);   // Error
```

<span data-ttu-id="c4d80-145">L’accès aux membres privés de `Child` à partir de `Main` est uniquement possible si `Main` est un membre de la classe.</span><span class="sxs-lookup"><span data-stu-id="c4d80-145">Accessing private members of `Child` from `Main` would only be possible if `Main` were a member of the class.</span></span>

<span data-ttu-id="c4d80-146">Du fait que les types déclarés dans une classe sans modificateur d’accès sont par défaut `private`, les données membres dans cet exemple sont toujours `private` si le mot clé est supprimé.</span><span class="sxs-lookup"><span data-stu-id="c4d80-146">Types declared inside a class without an access modifier default to `private`, so the data members in this example would still be `private` if the keyword were removed.</span></span>

<span data-ttu-id="c4d80-147">Notez enfin que pour l’objet créé à l’aide du constructeur par défaut (`child3`), le champ de l’âge est initialisé par défaut à la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="c4d80-147">Finally, notice that for the object created using the default constructor (`child3`), the age field was initialized to zero by default.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="c4d80-148">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="c4d80-148">C# Language Specification</span></span>
[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="c4d80-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4d80-149">See Also</span></span>
 [<span data-ttu-id="c4d80-150">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c4d80-150">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="c4d80-151">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c4d80-151">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="c4d80-152">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="c4d80-152">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="c4d80-153">Types référence</span><span class="sxs-lookup"><span data-stu-id="c4d80-153">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)
