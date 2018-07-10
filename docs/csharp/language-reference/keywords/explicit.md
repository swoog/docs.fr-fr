---
title: explicit, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- explicit_CSharpKeyword
- explicit
helpviewer_keywords:
- explicit keyword [C#]
ms.assetid: cfb8f42a-e411-4db2-af9b-796b05644846
ms.openlocfilehash: 66d271fdac0bad356ee0bafc1732e2f410854da1
ms.sourcegitcommit: f9e38d31288fe5962e6be5b0cc286da633482873
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37027939"
---
# <a name="explicit-c-reference"></a><span data-ttu-id="6bdfb-102">explicit (référence C#)</span><span class="sxs-lookup"><span data-stu-id="6bdfb-102">explicit (C# Reference)</span></span>

<span data-ttu-id="6bdfb-103">Le mot clé `explicit` déclare un opérateur de conversion de type défini par l’utilisateur qui doit être appelé avec un cast.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-103">The `explicit` keyword declares a user-defined type conversion operator that must be invoked with a cast.</span></span> <span data-ttu-id="6bdfb-104">Par exemple, cet opérateur effectue une conversion d’une classe nommée Fahrenheit vers une classe nommée Celsius :</span><span class="sxs-lookup"><span data-stu-id="6bdfb-104">For example, this operator converts from a class called Fahrenheit to a class called Celsius:</span></span>

[!code-csharp[csrefKeywordsConversion#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#2)]

<span data-ttu-id="6bdfb-105">Cet opérateur de conversion peut être appelé comme suit :</span><span class="sxs-lookup"><span data-stu-id="6bdfb-105">This conversion operator can be invoked like this:</span></span>

[!code-csharp[csrefKeywordsConversion#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#3)]

<span data-ttu-id="6bdfb-106">L’opérateur de conversion convertit un type source en type cible.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-106">The conversion operator converts from a source type to a target type.</span></span> <span data-ttu-id="6bdfb-107">Le type source fournit l’opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-107">The source type provides the conversion operator.</span></span> <span data-ttu-id="6bdfb-108">Contrairement à une conversion implicite, les opérateurs de conversion explicite doivent être appelés au moyen d’un cast.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-108">Unlike implicit conversion, explicit conversion operators must be invoked by means of a cast.</span></span> <span data-ttu-id="6bdfb-109">Si une opération de conversion peut provoquer des exceptions ou la perte d’informations, vous devez la marquer comme `explicit`.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-109">If a conversion operation can cause exceptions or lose information, you should mark it `explicit`.</span></span> <span data-ttu-id="6bdfb-110">Cela empêche que le compilateur appelle l’opération de conversion en mode silencieux, avec éventuellement des conséquences imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-110">This prevents the compiler from silently invoking the conversion operation with possibly unforeseen consequences.</span></span>

<span data-ttu-id="6bdfb-111">L’omission du cast provoque l’erreur de compilation CS0266.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-111">Omitting the cast results in compile-time error CS0266.</span></span>

<span data-ttu-id="6bdfb-112">Pour plus d’informations, consultez [Utilisation d’opérateurs de conversion](../../programming-guide/statements-expressions-operators/using-conversion-operators.md).</span><span class="sxs-lookup"><span data-stu-id="6bdfb-112">For more information, see [Using Conversion Operators](../../programming-guide/statements-expressions-operators/using-conversion-operators.md).</span></span>

## <a name="example"></a><span data-ttu-id="6bdfb-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="6bdfb-113">Example</span></span>

<span data-ttu-id="6bdfb-114">L’exemple suivant fournit des classes `Fahrenheit` et `Celsius`, chacune fournissant un opérateur de conversion explicite à l’autre classe.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-114">The following example provides a `Fahrenheit` and a `Celsius` class, each of which provides an explicit conversion operator to the other class.</span></span>

[!code-csharp[csrefKeywordsConversion#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#1)]

## <a name="example"></a><span data-ttu-id="6bdfb-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="6bdfb-115">Example</span></span>

<span data-ttu-id="6bdfb-116">L’exemple suivant définit un struct, `Digit`, qui représente un seul chiffre décimal.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-116">The following example defines a struct, `Digit`, that represents a single decimal digit.</span></span> <span data-ttu-id="6bdfb-117">Un opérateur est défini pour les conversions de `byte` à `Digit`, mais étant donné que les octets ne peuvent pas tous être convertis en `Digit`, la conversion est explicite.</span><span class="sxs-lookup"><span data-stu-id="6bdfb-117">An operator is defined for conversions from `byte` to `Digit`, but because not all bytes can be converted to a `Digit`, the conversion is explicit.</span></span>

[!code-csharp[csrefKeywordsConversion#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="6bdfb-118">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="6bdfb-118">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="6bdfb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bdfb-119">See also</span></span>

[<span data-ttu-id="6bdfb-120">Référence C#</span><span class="sxs-lookup"><span data-stu-id="6bdfb-120">C# Reference</span></span>](../index.md)  
[<span data-ttu-id="6bdfb-121">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="6bdfb-121">C# Programming Guide</span></span>](../../programming-guide/index.md)  
[<span data-ttu-id="6bdfb-122">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="6bdfb-122">C# Keywords</span></span>](index.md)  
[<span data-ttu-id="6bdfb-123">implicit</span><span class="sxs-lookup"><span data-stu-id="6bdfb-123">implicit</span></span>](implicit.md)  
[<span data-ttu-id="6bdfb-124">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="6bdfb-124">operator (C# Reference)</span></span>](operator.md)  
[<span data-ttu-id="6bdfb-125">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="6bdfb-125">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
[<span data-ttu-id="6bdfb-126">Conversions explicites définies par l’utilisateur chaînées en C#</span><span class="sxs-lookup"><span data-stu-id="6bdfb-126">Chained user-defined explicit conversions in C#</span></span>](https://blogs.msdn.microsoft.com/ericlippert/2007/04/16/chained-user-defined-explicit-conversions-in-c/)  