---
title: =, opérateur (référence C#)
ms.date: 11/26/2018
f1_keywords:
- =_CSharpKeyword
helpviewer_keywords:
- = operator [C#]
ms.assetid: d802a6d5-32f0-42b8-b180-12f5a081bfc1
ms.openlocfilehash: 123674f37d17db6dcfe6ae9d45c7176bdff1eda7
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149222"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="5973e-102">=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="5973e-102">= Operator (C# Reference)</span></span>

<span data-ttu-id="5973e-103">L’opérateur d’assignation `=` assigne la valeur de son opérande de droite à une variable, une [propriété](../../programming-guide/classes-and-structs/properties.md) ou un élément [d’indexeur](../../../csharp/programming-guide/indexers/index.md) donné par son opérande de gauche.</span><span class="sxs-lookup"><span data-stu-id="5973e-103">The assignment operator `=` assigns the value of its right-hand operand to a variable, a [property](../../programming-guide/classes-and-structs/properties.md), or an [indexer](../../../csharp/programming-guide/indexers/index.md) element given by its left-hand operand.</span></span> <span data-ttu-id="5973e-104">Le résultat d’une expression d’assignation est la valeur assignée à l’opérande de gauche.</span><span class="sxs-lookup"><span data-stu-id="5973e-104">The result of an assignment expression is the value assigned to the left-hand operand.</span></span> <span data-ttu-id="5973e-105">L’opérande de droite doit être du même type que l’opérande de gauche, ou implicitement convertible vers le type de l’opérande de gauche.</span><span class="sxs-lookup"><span data-stu-id="5973e-105">The type of the right-hand operand must be the same as the type of the left-hand operand or implicitly convertible to it.</span></span>

<span data-ttu-id="5973e-106">L’opérateur d’assignation est associatif à droite ; autrement dit, une expression de la forme :</span><span class="sxs-lookup"><span data-stu-id="5973e-106">The assignment operator is right-associative, that is, an expression of the form</span></span>

```csharp
a = b = c
```

<span data-ttu-id="5973e-107">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="5973e-107">is evaluated as</span></span>

```csharp
a = (b = c)
```

<span data-ttu-id="5973e-108">L’exemple suivant illustre l’utilisation de l’opérateur d’assignation pour assigner des valeurs à une variable locale, une propriété et un élément d’indexeur :</span><span class="sxs-lookup"><span data-stu-id="5973e-108">The following example demonstrates the usage of the assignment operator to assign values to a local variable, a property, and an indexer element:</span></span>

[!code-csharp-interactive[assignment operator](~/samples/snippets/csharp/language-reference/operators/AssignmentExamples.cs#Assignments)]

## <a name="ref-assignment-operator"></a><span data-ttu-id="5973e-109">Opérateur d'assignation ref</span><span class="sxs-lookup"><span data-stu-id="5973e-109">ref assignment operator</span></span>

<span data-ttu-id="5973e-110">À partir de C# 7.3, vous pouvez utiliser l’opérateur d’assignation ref `= ref` pour réaffecter une variable [locale ref](../keywords/ref.md#ref-locals) ou une variable [locale ref readonly](../keywords/ref.md#ref-readonly-locals).</span><span class="sxs-lookup"><span data-stu-id="5973e-110">Beginning with C# 7.3, you can use the ref assignment operator `= ref` to reassign a [ref local](../keywords/ref.md#ref-locals) or [ref readonly local](../keywords/ref.md#ref-readonly-locals) variable.</span></span> <span data-ttu-id="5973e-111">L’exemple suivant illustre l’utilisation de l’opérateur d’assignation ref :</span><span class="sxs-lookup"><span data-stu-id="5973e-111">The following example demonstrates the usage of the ref assignment operator:</span></span>

[!code-csharp[ref assignment operator](~/samples/snippets/csharp/language-reference/operators/AssignmentExamples.cs#RefAssignment)]

<span data-ttu-id="5973e-112">Dans le cas de l’opérateur d’assignation ref, l’opérande de gauche et l’opérande de droite doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="5973e-112">In the case of the ref assignment operator, the type of the left operand and the right operand must be the same.</span></span>

<span data-ttu-id="5973e-113">Pour plus d’informations, voir la [proposition de fonctionnalité](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.3/ref-local-reassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5973e-113">For more information, see the [feature proposal note](https://github.com/dotnet/csharplang/blob/master/proposals/csharp-7.3/ref-local-reassignment.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="5973e-114">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="5973e-114">Operator overloadability</span></span>

<span data-ttu-id="5973e-115">Un type défini par l’utilisateur ne peut pas surcharger l’opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="5973e-115">A user-defined type cannot overload the assignment operator.</span></span> <span data-ttu-id="5973e-116">Toutefois, il peut définir une conversion implicite vers un autre type.</span><span class="sxs-lookup"><span data-stu-id="5973e-116">However, a user-defined type can define an implicit conversion to another type.</span></span> <span data-ttu-id="5973e-117">Ainsi, la valeur d’un type défini par l’utilisateur peut être assignée à une variable, une propriété ou un élément d’indexeur d’un autre type.</span><span class="sxs-lookup"><span data-stu-id="5973e-117">That way, the value of a user-defined type can be assigned to a variable, a property, or an indexer element of another type.</span></span> <span data-ttu-id="5973e-118">Pour plus d'informations, voir l’article [implicit, mot clé](../keywords/implicit.md).</span><span class="sxs-lookup"><span data-stu-id="5973e-118">For more information, see the [implicit](../keywords/implicit.md) keyword article.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="5973e-119">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="5973e-119">C# language specification</span></span>

<span data-ttu-id="5973e-120">Pour plus d’informations, voir la section [Assignation simple](~/_csharplang/spec/expressions.md#simple-assignment) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="5973e-120">For more information, see the [Simple assignment](~/_csharplang/spec/expressions.md#simple-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5973e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5973e-121">See also</span></span>

- [<span data-ttu-id="5973e-122">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5973e-122">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5973e-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5973e-123">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5973e-124">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="5973e-124">C# Operators</span></span>](index.md)
- [<span data-ttu-id="5973e-125">ref, mot clé</span><span class="sxs-lookup"><span data-stu-id="5973e-125">ref keyword</span></span>](../keywords/ref.md)
