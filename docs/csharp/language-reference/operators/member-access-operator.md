---
title: . opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ._CSharpKeyword
helpviewer_keywords:
- member access operator (.) [C#]
- . operator [C#]
- dot operator (.) [C#]
ms.assetid: a1f54b52-b686-4ae5-a48e-a2a9ebd0eb7b
ms.openlocfilehash: a59f69d0349a054c8c2a5b701b8f63df113a6580
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333718"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="37f58-103">.</span><span class="sxs-lookup"><span data-stu-id="37f58-103">.</span></span> <span data-ttu-id="37f58-104">opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="37f58-104">operator (C# Reference)</span></span>

<span data-ttu-id="37f58-105">L’opérateur point (`.`) est l’opérateur d’accès aux membres .</span><span class="sxs-lookup"><span data-stu-id="37f58-105">The dot operator (`.`) is used for member access.</span></span> <span data-ttu-id="37f58-106">L’opérateur point spécifie un membre d’un type ou d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="37f58-106">The dot operator specifies a member of a type or namespace.</span></span> <span data-ttu-id="37f58-107">Par exemple, l’opérateur point est utilisé pour accéder aux méthodes spécifiques figurant dans les bibliothèques de classes du .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="37f58-107">For example, the dot operator is used to access specific methods within the .NET Framework class libraries:</span></span>

[!code-csharp[csRefOperators#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#16)]

<span data-ttu-id="37f58-108">Par exemple, considérons la classe suivante :</span><span class="sxs-lookup"><span data-stu-id="37f58-108">For example, consider the following class:</span></span>

[!code-csharp[csRefOperators#17](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#17)]

[!code-csharp[csRefOperators#18](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#18)]

<span data-ttu-id="37f58-109">La variable `s` a deux membres, `a` et `b` ; pour y accéder, utilisez l’opérateur point :</span><span class="sxs-lookup"><span data-stu-id="37f58-109">The variable `s` has two members, `a` and `b`; to access them, use the dot operator:</span></span>

[!code-csharp[csRefOperators#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#19)]

<span data-ttu-id="37f58-110">Le point est aussi utilisé pour former des noms qualifiés, c’est-à-dire des noms qui spécifient par exemple l’espace de noms ou une interface auquel ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="37f58-110">The dot is also used to form qualified names, which are names that specify the namespace or interface, for example, to which they belong.</span></span>

[!code-csharp[csRefOperators#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#20)]

<span data-ttu-id="37f58-111">La directive using rend la qualification de certains noms facultative :</span><span class="sxs-lookup"><span data-stu-id="37f58-111">The using directive makes some name qualification optional:</span></span>

[!code-csharp[csRefOperators#21](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#21)]

<span data-ttu-id="37f58-112">Cependant, quand un identificateur est ambigu, il doit être qualifié :</span><span class="sxs-lookup"><span data-stu-id="37f58-112">But when an identifier is ambiguous, it must be qualified:</span></span>

[!code-csharp[csRefOperators#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#22)]

## <a name="c-language-specification"></a><span data-ttu-id="37f58-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="37f58-113">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="37f58-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37f58-114">See also</span></span>

- [<span data-ttu-id="37f58-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="37f58-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="37f58-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="37f58-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="37f58-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="37f58-117">C# Operators</span></span>](index.md)