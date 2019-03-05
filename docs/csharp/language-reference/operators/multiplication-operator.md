---
title: '* opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/26/2019
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: a5e120d26614f1e38cc2f2db02949552140b594e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56977342"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="68880-102">\*, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="68880-102">\* operator (C# Reference)</span></span>

<span data-ttu-id="68880-103">L’opérateur `*` est pris en charge sous deux formes : un opérateur d’indirection de pointeur unaire et un opérateur de multiplication binaire.</span><span class="sxs-lookup"><span data-stu-id="68880-103">The `*` operator is supported in two forms: a unary pointer indirection operator or a binary multiplication operator.</span></span>

## <a name="pointer-indirection-operator"></a><span data-ttu-id="68880-104">Opérateur d’indirection de pointeur</span><span class="sxs-lookup"><span data-stu-id="68880-104">Pointer indirection operator</span></span>

<span data-ttu-id="68880-105">Utilisez l’opérateur `*` unaire pour récupérer la variable vers laquelle pointe un opérande de type pointeur.</span><span class="sxs-lookup"><span data-stu-id="68880-105">Use the unary `*` operator to obtain the variable to which an operand of a pointer type points.</span></span> <span data-ttu-id="68880-106">Pour plus d’informations, voir [Guide pratique : Récupérer la valeur d’une variable de pointeur](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-value-of-a-pointer-variable.md).</span><span class="sxs-lookup"><span data-stu-id="68880-106">For more information, see [How to: obtain the value of a pointer variable](../../programming-guide/unsafe-code-pointers/how-to-obtain-the-value-of-a-pointer-variable.md).</span></span>

<span data-ttu-id="68880-107">L’opérateur d’indirection de pointeur `*` réclame un contexte [unsafe](../keywords/unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="68880-107">The pointer indirection operator `*` requires [unsafe](../keywords/unsafe.md) context.</span></span>

## <a name="multiplication-operator"></a><span data-ttu-id="68880-108">Opérateur de multiplication</span><span class="sxs-lookup"><span data-stu-id="68880-108">Multiplication operator</span></span>

<span data-ttu-id="68880-109">Pour les types numériques, l’opérateur `*` calcule le produit de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="68880-109">For numeric types, the `*` operator computes the product of its operands:</span></span>

[!code-csharp-interactive[multiplication](~/samples/snippets/csharp/language-reference/operators/MultiplicationExamples.cs#Multiply)]

## <a name="operator-overloadability"></a><span data-ttu-id="68880-110">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="68880-110">Operator overloadability</span></span>

<span data-ttu-id="68880-111">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) un opérateur `*` binaire.</span><span class="sxs-lookup"><span data-stu-id="68880-111">User-defined types can [overload](../keywords/operator.md) a binary `*` operator.</span></span> <span data-ttu-id="68880-112">En cas de surcharge d’un opérateur `*` binaire, [l’opérateur d’assignation de multiplication](multiplication-assignment-operator.md) `*=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="68880-112">When a binary `*` operator is overloaded, the [multiplication assignment operator](multiplication-assignment-operator.md) `*=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="68880-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="68880-113">C# language specification</span></span>

<span data-ttu-id="68880-114">Pour plus d’informations, voir les sections [Indirection de pointeur](~/_csharplang/spec/unsafe-code.md#pointer-indirection) et [Opérateur de multiplication](~/_csharplang/spec/expressions.md#multiplication-operator) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="68880-114">For more information, see the [Pointer indirection](~/_csharplang/spec/unsafe-code.md#pointer-indirection) and [Multiplication operator](~/_csharplang/spec/expressions.md#multiplication-operator) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="68880-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68880-115">See also</span></span>

- [<span data-ttu-id="68880-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="68880-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="68880-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="68880-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="68880-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="68880-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="68880-119">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="68880-119">Pointer types</span></span>](../../programming-guide/unsafe-code-pointers/pointer-types.md)