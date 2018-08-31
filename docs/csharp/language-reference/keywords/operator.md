---
title: operator, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords:
- operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
ms.openlocfilehash: c3bfada235993670bf158fe9803a09707b2b3251
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929870"
---
# <a name="operator-c-reference"></a><span data-ttu-id="d5b35-102">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d5b35-102">operator (C# Reference)</span></span>

<span data-ttu-id="d5b35-103">Utilisez le mot clé `operator` pour surcharger un opérateur intégré ou pour fournir une conversion définie par l’utilisateur dans une déclaration class ou struct.</span><span class="sxs-lookup"><span data-stu-id="d5b35-103">Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.</span></span>

## <a name="example"></a><span data-ttu-id="d5b35-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d5b35-104">Example</span></span>

<span data-ttu-id="d5b35-105">L’exemple suivant montre une classe très simplifiée pour les nombres fractionnaires.</span><span class="sxs-lookup"><span data-stu-id="d5b35-105">The following is a very simplified class for fractional numbers.</span></span> <span data-ttu-id="d5b35-106">Cette classe surcharge les opérateurs `+` et `*` pour effectuer des opérations d’addition et de multiplication fractionnaires. Elle fournit également un opérateur de conversion qui convertit un type `Fraction` en type `double`.</span><span class="sxs-lookup"><span data-stu-id="d5b35-106">It overloads the `+` and `*` operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a `Fraction` type to a `double` type.</span></span>

[!code-csharp[csrefKeywordsConversion#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#6)]

## <a name="c-language-specification"></a><span data-ttu-id="d5b35-107">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="d5b35-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="d5b35-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5b35-108">See also</span></span>

- [<span data-ttu-id="d5b35-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d5b35-109">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="d5b35-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d5b35-110">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="d5b35-111">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="d5b35-111">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="d5b35-112">implicit</span><span class="sxs-lookup"><span data-stu-id="d5b35-112">implicit</span></span>](implicit.md)
- [<span data-ttu-id="d5b35-113">explicit</span><span class="sxs-lookup"><span data-stu-id="d5b35-113">explicit</span></span>](explicit.md)
- [<span data-ttu-id="d5b35-114">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="d5b35-114">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
