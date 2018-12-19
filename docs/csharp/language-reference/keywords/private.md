---
title: private, mot clé - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- private_CSharpKeyword
- private
helpviewer_keywords:
- private keyword [C#]
ms.assetid: 654c0bb8-e6ac-4086-bf96-7474fa6aa1c8
ms.openlocfilehash: 62a78649a96d0a1b03758508241395d7f061504b
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237192"
---
# <a name="private-c-reference"></a><span data-ttu-id="ea6b1-102">private (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ea6b1-102">private (C# Reference)</span></span>

<span data-ttu-id="ea6b1-103">Le mot clé `private` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-103">The `private` keyword is a member access modifier.</span></span>

> <span data-ttu-id="ea6b1-104">Cette page traite de l’accès `private`.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-104">This page covers `private` access.</span></span> <span data-ttu-id="ea6b1-105">Le mot clé `private` fait également partie du modificateur d’accès [`private protected`](./private-protected.md).</span><span class="sxs-lookup"><span data-stu-id="ea6b1-105">The `private` keyword is also part of the [`private protected`](./private-protected.md) access modifier.</span></span>

<span data-ttu-id="ea6b1-106">L’accès privé est le niveau d’accès le moins permissif.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-106">Private access is the least permissive access level.</span></span> <span data-ttu-id="ea6b1-107">Les membres privés sont accessibles uniquement dans le corps de la classe ou le struct dans lequel ils sont déclarés, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="ea6b1-107">Private members are accessible only within the body of the class or the struct in which they are declared, as in this example:</span></span>

```csharp
class Employee
{
    private int i;
    double d;   // private access by default
}
```

<span data-ttu-id="ea6b1-108">Les types imbriqués dans le même corps peuvent également accéder à ces membres privés.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-108">Nested types in the same body can also access those private members.</span></span>

<span data-ttu-id="ea6b1-109">Référencer un membre privé en dehors d'une classe ou d'un struct où il est déclaré serait à l'origine d'une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-109">It is a compile-time error to reference a private member outside the class or the struct in which it is declared.</span></span>

<span data-ttu-id="ea6b1-110">Pour obtenir une comparaison de `private` et des autres modificateurs d’accès, consultez [Niveaux d’accessibilité](accessibility-levels.md) et [Modificateurs d’accès](../../programming-guide/classes-and-structs/access-modifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ea6b1-110">For a comparison of `private` with the other access modifiers, see [Accessibility Levels](accessibility-levels.md) and [Access Modifiers](../../programming-guide/classes-and-structs/access-modifiers.md).</span></span>

## <a name="example"></a><span data-ttu-id="ea6b1-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="ea6b1-111">Example</span></span>

<span data-ttu-id="ea6b1-112">Dans cet exemple, la classe `Employee` contient deux membres de données privés, `name` et `salary`.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-112">In this example, the `Employee` class contains two private data members, `name` and `salary`.</span></span> <span data-ttu-id="ea6b1-113">S’agissant de membres privés, ils sont accessibles uniquement par les méthodes membres.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-113">As private members, they cannot be accessed except by member methods.</span></span> <span data-ttu-id="ea6b1-114">Les méthodes publiques `GetName` et `Salary` sont ajoutées pour permettre un accès contrôlé aux membres privés.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-114">Public methods named `GetName` and `Salary` are added to allow controlled access to the private members.</span></span> <span data-ttu-id="ea6b1-115">Le membre `name` est accessible via une méthode publique et le membre `salary` est accessible via une propriété publique en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-115">The `name` member is accessed by way of a public method, and the `salary` member is accessed by way of a public read-only property.</span></span> <span data-ttu-id="ea6b1-116">(Pour plus d’informations, consultez [Propriétés](../../programming-guide/classes-and-structs/properties.md).)</span><span class="sxs-lookup"><span data-stu-id="ea6b1-116">(See [Properties](../../programming-guide/classes-and-structs/properties.md) for more information.)</span></span>

[!code-csharp[csrefKeywordsModifiers#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#10)]

## <a name="c-language-specification"></a><span data-ttu-id="ea6b1-117">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ea6b1-117">C# language specification</span></span>  

<span data-ttu-id="ea6b1-118">Pour plus d’informations, consultez [Accessibilité déclarée](~/_csharplang/spec/basic-concepts.md#declared-accessibility) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="ea6b1-118">For more information, see [Declared accessibility](~/_csharplang/spec/basic-concepts.md#declared-accessibility) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="ea6b1-119">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="ea6b1-119">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea6b1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea6b1-120">See also</span></span>

- [<span data-ttu-id="ea6b1-121">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ea6b1-121">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="ea6b1-122">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ea6b1-122">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="ea6b1-123">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="ea6b1-123">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="ea6b1-124">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="ea6b1-124">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="ea6b1-125">Niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="ea6b1-125">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="ea6b1-126">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="ea6b1-126">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="ea6b1-127">public</span><span class="sxs-lookup"><span data-stu-id="ea6b1-127">public</span></span>](public.md)
- [<span data-ttu-id="ea6b1-128">protected</span><span class="sxs-lookup"><span data-stu-id="ea6b1-128">protected</span></span>](protected.md)
- [<span data-ttu-id="ea6b1-129">internal</span><span class="sxs-lookup"><span data-stu-id="ea6b1-129">internal</span></span>](internal.md)