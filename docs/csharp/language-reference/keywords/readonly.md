---
title: readonly, mot clé - Référence C#
ms.custom: seodec18
ms.date: 06/21/2018
f1_keywords:
- readonly_CSharpKeyword
- readonly
helpviewer_keywords:
- readonly keyword [C#]
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
ms.openlocfilehash: c7f3b1b1525277bf948070c9121d151f9f520127
ms.sourcegitcommit: e39d93d358974b9ed4541cedf4e25c0101015c3c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "55204663"
---
# <a name="readonly-c-reference"></a><span data-ttu-id="fc688-102">readonly (référence C#)</span><span class="sxs-lookup"><span data-stu-id="fc688-102">readonly (C# Reference)</span></span>

<span data-ttu-id="fc688-103">Le mot clé `readonly` est un modificateur qui peut être utilisé dans trois contextes :</span><span class="sxs-lookup"><span data-stu-id="fc688-103">The `readonly` keyword is a modifier that can be used in three contexts:</span></span>

- <span data-ttu-id="fc688-104">Dans une [déclaration de champ](#readonly-field-example), `readonly` indique qu’une affectation à destination d’un champ peut survenir uniquement dans le cadre de la déclaration ou dans un constructeur de la même classe.</span><span class="sxs-lookup"><span data-stu-id="fc688-104">In a [field declaration](#readonly-field-example), `readonly` indicates that assignment to the field can only occur as part of the declaration or in a constructor in the same class.</span></span>
- <span data-ttu-id="fc688-105">Dans une définition [`readonly struct`](#readonly-struct-example), `readonly` indique que le `struct` est immuable.</span><span class="sxs-lookup"><span data-stu-id="fc688-105">In a [`readonly struct` definition](#readonly-struct-example), `readonly` indicates that the `struct` is immutable.</span></span>
- <span data-ttu-id="fc688-106">Dans un [`ref readonly`retour de la méthode](#ref-readonly-return-example), le modificateur `readonly` indique que la méthode retourne une référence et que les écritures ne sont pas autorisés pour cette référence.</span><span class="sxs-lookup"><span data-stu-id="fc688-106">In a [`ref readonly` method return](#ref-readonly-return-example), the `readonly` modifier indicates that method returns a reference and writes are not allowed to that reference.</span></span>

<span data-ttu-id="fc688-107">Les deux contextes finaux ont été ajoutés dans C# 7.2.</span><span class="sxs-lookup"><span data-stu-id="fc688-107">The final two contexts were added in C# 7.2.</span></span>

## <a name="readonly-field-example"></a><span data-ttu-id="fc688-108">Exemple de champ en lecture seule</span><span class="sxs-lookup"><span data-stu-id="fc688-108">Readonly field example</span></span>

<span data-ttu-id="fc688-109">Dans cet exemple, la valeur du champ `year` ne peut pas être modifiée dans la méthode `ChangeYear`, même si une valeur lui est affectée dans le constructeur de classe :</span><span class="sxs-lookup"><span data-stu-id="fc688-109">In this example, the value of the field `year` cannot be changed in the method `ChangeYear`, even though it is assigned a value in the class constructor:</span></span>

[!code-csharp[Readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyField)]

<span data-ttu-id="fc688-110">Vous pouvez affecter une valeur à un champ `readonly` uniquement dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="fc688-110">You can assign a value to a `readonly` field only in the following contexts:</span></span>

- <span data-ttu-id="fc688-111">Lorsque la variable est initialisée dans la déclaration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="fc688-111">When the variable is initialized in the declaration, for example:</span></span>

```csharp
public readonly int y = 5;
```

- <span data-ttu-id="fc688-112">Dans un constructeur d’instance de la classe qui contient la déclaration de champ d’instance.</span><span class="sxs-lookup"><span data-stu-id="fc688-112">In an instance constructor of the class that contains the instance field declaration.</span></span>
- <span data-ttu-id="fc688-113">Dans le constructeur statique de la classe qui contient la déclaration de champ statique.</span><span class="sxs-lookup"><span data-stu-id="fc688-113">In the static constructor of the class that contains the static field declaration.</span></span>

<span data-ttu-id="fc688-114">Ces contextes de constructeur sont aussi les seuls contextes dans lesquels il est possible de passer un champ `readonly` comme paramètre [out](out-parameter-modifier.md) ou [ref](ref.md).</span><span class="sxs-lookup"><span data-stu-id="fc688-114">These constructor contexts are also the only contexts in which it is valid to pass a `readonly` field as an [out](out-parameter-modifier.md) or [ref](ref.md) parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="fc688-115">Le mot clé `readonly` est différent du mot clé [const](const.md).</span><span class="sxs-lookup"><span data-stu-id="fc688-115">The `readonly` keyword is different from the [const](const.md) keyword.</span></span> <span data-ttu-id="fc688-116">Un champ `const` ne peut être initialisé qu'au moment de la déclaration du champ.</span><span class="sxs-lookup"><span data-stu-id="fc688-116">A `const` field can only be initialized at the declaration of the field.</span></span> <span data-ttu-id="fc688-117">Un champ `readonly` peut être assigné plusieurs fois dans la déclaration de champ et dans un constructeur.</span><span class="sxs-lookup"><span data-stu-id="fc688-117">A `readonly` field can be assigned multiple times in the field declaration and in any constructor.</span></span> <span data-ttu-id="fc688-118">C'est pourquoi, les champs `readonly` peuvent avoir des valeurs différentes en fonction du constructeur utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc688-118">Therefore, `readonly` fields can have different values depending on the constructor used.</span></span> <span data-ttu-id="fc688-119">De même, alors qu’un champ `const` est une constante au moment de la compilation, le champ `readonly` peut être utilisé pour des constantes au moment de l’exécution, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fc688-119">Also, while a `const` field is a compile-time constant, the `readonly` field can be used for runtime constants as in the following example:</span></span>
>
> ```csharp
> public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;
> ```

[!code-csharp[Initialize readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#InitReadonlyField)]

<span data-ttu-id="fc688-120">Dans l’exemple précédent, si vous utilisez une instruction telle que dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fc688-120">In the preceding example, if you use a statement like the following example:</span></span>

`p2.y = 66;        // Error`

<span data-ttu-id="fc688-121">vous obtenez le message d’erreur du compilateur :</span><span class="sxs-lookup"><span data-stu-id="fc688-121">you will get the compiler error message:</span></span>

`A readonly field cannot be assigned to (except in a constructor or a variable initializer)`

## <a name="readonly-struct-example"></a><span data-ttu-id="fc688-122">Exemple de struct readonly</span><span class="sxs-lookup"><span data-stu-id="fc688-122">Readonly struct example</span></span>

<span data-ttu-id="fc688-123">Le modificateur `readonly` dans une définition `struct` déclare que le struct est **immuable**.</span><span class="sxs-lookup"><span data-stu-id="fc688-123">The `readonly` modifier on a `struct` definition declares that the struct is **immutable**.</span></span> <span data-ttu-id="fc688-124">Chaque champ d’instance du `struct` doit être marqué `readonly`, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fc688-124">Every instance field of the `struct` must be marked `readonly`, as shown in the following example:</span></span>

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyStruct)]

<span data-ttu-id="fc688-125">L’exemple précédent utilise les [propriétés automatiques readonly](../../properties.md#read-only) pour déclarer son stockage.</span><span class="sxs-lookup"><span data-stu-id="fc688-125">The preceding example uses [readonly auto properties](../../properties.md#read-only) to declare its storage.</span></span> <span data-ttu-id="fc688-126">Il donne l’instruction au compilateur de créer des champs de stockage `readonly` pour ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc688-126">That instructs the compiler to create `readonly` backing fields for those properties.</span></span> <span data-ttu-id="fc688-127">Vous pouvez aussi déclarer des champs `readonly` directement :</span><span class="sxs-lookup"><span data-stu-id="fc688-127">You could also declare `readonly` fields directly:</span></span>

```csharp
public readonly struct Point
{
    public readonly double X;
    public readonly double Y;

    public Point(double x, double y) => (X, Y) = (x, y);

    public override string ToString() => $"({X}, {Y})";
}
```

<span data-ttu-id="fc688-128">L’ajout d’un champ non marqué `readonly` génère l’erreur du compilateur `CS8340` : « Les champs d’instance de structs en lecture seule doivent être en lecture seule. »</span><span class="sxs-lookup"><span data-stu-id="fc688-128">Adding a field not marked `readonly` generates compiler error `CS8340`: "Instance fields of readonly structs must be readonly."</span></span>

## <a name="ref-readonly-return-example"></a><span data-ttu-id="fc688-129">Exemple de retour ref readonly</span><span class="sxs-lookup"><span data-stu-id="fc688-129">Ref readonly return example</span></span>

<span data-ttu-id="fc688-130">Le modificateur `readonly` au niveau d’un `ref return` indique que la référence retournée ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="fc688-130">The `readonly` modifier on a `ref return` indicates that the returned reference cannot be modified.</span></span> <span data-ttu-id="fc688-131">L’exemple suivant retourne une référence à l’origine.</span><span class="sxs-lookup"><span data-stu-id="fc688-131">The following example returns a reference to the origin.</span></span> <span data-ttu-id="fc688-132">Il utilise le modificateur `readonly` pour indiquer que les appelants ne peuvent pas modifier l’origine :</span><span class="sxs-lookup"><span data-stu-id="fc688-132">It uses the `readonly` modifier to indicate that callers cannot modify the origin:</span></span>

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyReturn)]
<span data-ttu-id="fc688-133">Le type retourné ne doit pas nécessairement être un `readonly struct`.</span><span class="sxs-lookup"><span data-stu-id="fc688-133">The type returned doesn't need to be a `readonly struct`.</span></span> <span data-ttu-id="fc688-134">Tout type pouvant être retourné par `ref` peut être retourné par `ref readonly`.</span><span class="sxs-lookup"><span data-stu-id="fc688-134">Any type that can be returned by `ref` can be returned by `ref readonly`</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="fc688-135">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="fc688-135">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="fc688-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc688-136">See also</span></span>

- [<span data-ttu-id="fc688-137">Référence C#</span><span class="sxs-lookup"><span data-stu-id="fc688-137">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="fc688-138">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="fc688-138">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="fc688-139">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="fc688-139">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="fc688-140">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="fc688-140">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="fc688-141">const</span><span class="sxs-lookup"><span data-stu-id="fc688-141">const</span></span>](const.md)
- [<span data-ttu-id="fc688-142">Champs</span><span class="sxs-lookup"><span data-stu-id="fc688-142">Fields</span></span>](../../programming-guide/classes-and-structs/fields.md)
