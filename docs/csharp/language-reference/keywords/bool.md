---
title: bool, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- bool_CSharpKeyword
- bool
helpviewer_keywords:
- bool keyword [C#]
ms.assetid: 551cfe35-2632-4343-af49-33ad12da08e2
ms.openlocfilehash: d6b0cb91dd9b8159919b0d155bb2f9773e7ba534
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36315106"
---
# <a name="bool-c-reference"></a><span data-ttu-id="52203-102">bool (référence C#)</span><span class="sxs-lookup"><span data-stu-id="52203-102">bool (C# Reference)</span></span>

<span data-ttu-id="52203-103">Le mot clé `bool` est un alias de <xref:System.Boolean?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="52203-103">The `bool` keyword is an alias of <xref:System.Boolean?displayProperty=nameWithType>.</span></span> <span data-ttu-id="52203-104">Il s’utilise pour déclarer des variables qui stockent les valeurs booléennes [true](../../../csharp/language-reference/keywords/true.md) et [false](../../../csharp/language-reference/keywords/false.md).</span><span class="sxs-lookup"><span data-stu-id="52203-104">It is used to declare variables to store the Boolean values, [true](../../../csharp/language-reference/keywords/true.md) and [false](../../../csharp/language-reference/keywords/false.md).</span></span>

> [!NOTE]
> <span data-ttu-id="52203-105">Si vous avez besoin d’une variable booléenne qui peut également avoir la valeur `null`, utilisez `bool?`.</span><span class="sxs-lookup"><span data-stu-id="52203-105">If you require a Boolean variable that can also have a value of `null`, use `bool?`.</span></span> <span data-ttu-id="52203-106">Pour plus d’informations, consultez [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md).</span><span class="sxs-lookup"><span data-stu-id="52203-106">For more information, see [Nullable Types](../../../csharp/programming-guide/nullable-types/index.md).</span></span>

## <a name="literals"></a><span data-ttu-id="52203-107">Littéraux</span><span class="sxs-lookup"><span data-stu-id="52203-107">Literals</span></span>

<span data-ttu-id="52203-108">Vous pouvez assigner une valeur booléenne à une variable `bool`.</span><span class="sxs-lookup"><span data-stu-id="52203-108">You can assign a Boolean value to a `bool` variable.</span></span> <span data-ttu-id="52203-109">Vous pouvez également assigner à une variable `bool` une expression dont le résultat est une valeur `bool`.</span><span class="sxs-lookup"><span data-stu-id="52203-109">You can also assign an expression that evaluates to `bool` to a `bool` variable.</span></span>

[!code-csharp[csrefKeywordsTypes#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#1)]

<span data-ttu-id="52203-110">La valeur par défaut d’une variable `bool` est `false`.</span><span class="sxs-lookup"><span data-stu-id="52203-110">The default value of a `bool` variable is `false`.</span></span> <span data-ttu-id="52203-111">La valeur par défaut d’une variable `bool?` est `null`.</span><span class="sxs-lookup"><span data-stu-id="52203-111">The default value of a `bool?` variable is `null`.</span></span>

## <a name="conversions"></a><span data-ttu-id="52203-112">Conversions</span><span class="sxs-lookup"><span data-stu-id="52203-112">Conversions</span></span>

<span data-ttu-id="52203-113">Dans C++, une valeur de type `bool` peut être convertie en une valeur de type `int`. En d’autres termes, `false` équivaut à zéro et `true` équivaut à une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="52203-113">In C++, a value of type `bool` can be converted to a value of type `int`; in other words, `false` is equivalent to zero and `true` is equivalent to nonzero values.</span></span> <span data-ttu-id="52203-114">Dans C#, il n’y a pas de conversion possible entre le type `bool` et les autres types.</span><span class="sxs-lookup"><span data-stu-id="52203-114">In C#, there is no conversion between the `bool` type and other types.</span></span> <span data-ttu-id="52203-115">Par exemple, l’instruction `if` suivante n’est pas valide dans C# :</span><span class="sxs-lookup"><span data-stu-id="52203-115">For example, the following `if` statement is invalid in C#:</span></span>

[!code-csharp[csrefKeywordsTypes#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#2)]

<span data-ttu-id="52203-116">Pour tester une variable du type `int`, vous devez la comparer explicitement à une valeur, telle que zéro, comme suit :</span><span class="sxs-lookup"><span data-stu-id="52203-116">To test a variable of the type `int`, you have to explicitly compare it to a value, such as zero, as follows:</span></span>

[!code-csharp[csrefKeywordsTypes#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#3)]

## <a name="example"></a><span data-ttu-id="52203-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="52203-117">Example</span></span>

<span data-ttu-id="52203-118">Dans cet exemple, vous tapez un caractère, et le programme vérifie si le caractère entré est une lettre.</span><span class="sxs-lookup"><span data-stu-id="52203-118">In this example, you enter a character from the keyboard and the program checks if the input character is a letter.</span></span> <span data-ttu-id="52203-119">Si c’est une lettre, le programme vérifie s’il s’agit d’une minuscule ou d’une majuscule.</span><span class="sxs-lookup"><span data-stu-id="52203-119">If it is a letter, it checks if it is lowercase or uppercase.</span></span> <span data-ttu-id="52203-120">Ces vérifications sont effectuées avec les méthodes <xref:System.Char.IsLetter%2A>, et <xref:System.Char.IsLower%2A>, qui retournent toutes les deux le type `bool` :</span><span class="sxs-lookup"><span data-stu-id="52203-120">These checks are performed with the <xref:System.Char.IsLetter%2A>, and <xref:System.Char.IsLower%2A>, both of which return the `bool` type:</span></span>

[!code-csharp[csrefKeywordsTypes#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="52203-121">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="52203-121">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="52203-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52203-122">See also</span></span>

[<span data-ttu-id="52203-123">Référence C#</span><span class="sxs-lookup"><span data-stu-id="52203-123">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
[<span data-ttu-id="52203-124">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="52203-124">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
[<span data-ttu-id="52203-125">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="52203-125">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
[<span data-ttu-id="52203-126">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="52203-126">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
[<span data-ttu-id="52203-127">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="52203-127">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
[<span data-ttu-id="52203-128">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="52203-128">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
[<span data-ttu-id="52203-129">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="52203-129">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  