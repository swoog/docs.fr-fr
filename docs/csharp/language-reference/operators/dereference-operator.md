---
title: ->, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: be74f02a85aa05cdab32768ed38222fc4d9289b1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255365"
---
# <a name="--operator-c-reference"></a><span data-ttu-id="1883f-102">->, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="1883f-102">-> Operator (C# Reference)</span></span>

<span data-ttu-id="1883f-103">L’opérateur d’accès au membre pointeur `->` combine l’accès au membre et l’indirection du pointeur.</span><span class="sxs-lookup"><span data-stu-id="1883f-103">The pointer member access operator `->` combines pointer indirection and member access.</span></span>

<span data-ttu-id="1883f-104">Si `x` est un pointeur de type `T*` et `y` un membre accessible de `T`, une expression de la forme :</span><span class="sxs-lookup"><span data-stu-id="1883f-104">If `x` is a pointer of the type `T*` and `y` is an accessible member of `T`, an expression of the form</span></span>

```csharp
x->y
```

<span data-ttu-id="1883f-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="1883f-105">is equivalent to</span></span>

```csharp
(*x).y
```

<span data-ttu-id="1883f-106">L’opérateur `->` réclame un contexte [unsafe](../keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="1883f-106">The `->` operator requires [unsafe](../keywords/unsafe.md) context.</span></span>

<span data-ttu-id="1883f-107">Pour plus d’informations, voir [Guide pratique : accéder à un membre avec un pointeur](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md).</span><span class="sxs-lookup"><span data-stu-id="1883f-107">For more information, see [How to: access a member with a pointer](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="1883f-108">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="1883f-108">Operator overloadability</span></span>

<span data-ttu-id="1883f-109">L’opérateur `->` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="1883f-109">The `->` operator cannot be overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="1883f-110">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="1883f-110">C# language specification</span></span>

<span data-ttu-id="1883f-111">Pour plus d’informations, voir la section [Accès au membre pointeur](~/_csharplang/spec/unsafe-code.md#pointer-member-access) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="1883f-111">For more information, see the [Pointer member access](~/_csharplang/spec/unsafe-code.md#pointer-member-access) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1883f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1883f-112">See also</span></span>

- [<span data-ttu-id="1883f-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1883f-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="1883f-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1883f-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="1883f-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="1883f-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="1883f-116">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="1883f-116">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)
