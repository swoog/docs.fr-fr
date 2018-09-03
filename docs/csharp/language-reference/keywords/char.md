---
title: char, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- char
- char_CSharpKeyword
helpviewer_keywords:
- char data type [C#]
ms.assetid: b51cf4fb-124c-4067-af48-afbac122b228
ms.openlocfilehash: 95ecfaaf1397f7a4598faba6528b38170062145a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43463219"
---
# <a name="char-c-reference"></a><span data-ttu-id="30eeb-102">char (référence C#)</span><span class="sxs-lookup"><span data-stu-id="30eeb-102">char (C# Reference)</span></span>

<span data-ttu-id="30eeb-103">Le mot clé `char` permet de déclarer une instance de la structure <xref:System.Char?displayProperty=nameWithType> utilisée par le .NET Framework pour représenter un caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="30eeb-103">The `char` keyword is used to declare an instance of the <xref:System.Char?displayProperty=nameWithType> structure that the .NET Framework uses to represent a Unicode character.</span></span> <span data-ttu-id="30eeb-104">La valeur d’un objet `Char` est une valeur numérique 16 bits (ordinale).</span><span class="sxs-lookup"><span data-stu-id="30eeb-104">The value of a `Char` object is a 16-bit numeric (ordinal) value.</span></span>

 <span data-ttu-id="30eeb-105">Les caractères Unicode sont utilisés pour représenter la plupart des langues écrites dans le monde.</span><span class="sxs-lookup"><span data-stu-id="30eeb-105">Unicode characters are used to represent most of the written languages throughout the world.</span></span>

|<span data-ttu-id="30eeb-106">Type</span><span class="sxs-lookup"><span data-stu-id="30eeb-106">Type</span></span>|<span data-ttu-id="30eeb-107">Plage</span><span class="sxs-lookup"><span data-stu-id="30eeb-107">Range</span></span>|<span data-ttu-id="30eeb-108">Size</span><span class="sxs-lookup"><span data-stu-id="30eeb-108">Size</span></span>|<span data-ttu-id="30eeb-109">Type .NET</span><span class="sxs-lookup"><span data-stu-id="30eeb-109">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`char`|<span data-ttu-id="30eeb-110">U+0000 à U+FFFF</span><span class="sxs-lookup"><span data-stu-id="30eeb-110">U+0000 to U+FFFF</span></span>|<span data-ttu-id="30eeb-111">Caractère Unicode 16 bits</span><span class="sxs-lookup"><span data-stu-id="30eeb-111">Unicode 16-bit character</span></span>|<xref:System.Char?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="30eeb-112">Littéraux</span><span class="sxs-lookup"><span data-stu-id="30eeb-112">Literals</span></span>

<span data-ttu-id="30eeb-113">Les constantes de type `char` peuvent être représentées sous la forme de littéraux de caractères, d’une séquence d’échappement hexadécimale ou d’une représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="30eeb-113">Constants of the `char` type can be written as character literals, hexadecimal escape sequence, or Unicode representation.</span></span> <span data-ttu-id="30eeb-114">Vous pouvez également effectuer un cast des codes de caractères de type intégral.</span><span class="sxs-lookup"><span data-stu-id="30eeb-114">You can also cast the integral character codes.</span></span> <span data-ttu-id="30eeb-115">Dans l’exemple suivant, quatre variables `char` sont initialisées avec le même caractère (`X`) :</span><span class="sxs-lookup"><span data-stu-id="30eeb-115">In the following example four `char` variables are initialized with the same character `X`:</span></span>

[!code-csharp[csrefKeywordsTypes#19](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#19)]

## <a name="conversions"></a><span data-ttu-id="30eeb-116">Conversions</span><span class="sxs-lookup"><span data-stu-id="30eeb-116">Conversions</span></span>

<span data-ttu-id="30eeb-117">Vous pouvez convertir implicitement un `char` en [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), [ulong](../../../csharp/language-reference/keywords/ulong.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) ou [decimal](../../../csharp/language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="30eeb-117">A `char` can be implicitly converted to [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), [ulong](../../../csharp/language-reference/keywords/ulong.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span> <span data-ttu-id="30eeb-118">Par contre, vous ne pouvez pas convertir implicitement d’autres types en type `char`.</span><span class="sxs-lookup"><span data-stu-id="30eeb-118">However, there are no implicit conversions from other types to the `char` type.</span></span>

<span data-ttu-id="30eeb-119">Le type <xref:System.Char?displayProperty=nameWithType> fournit plusieurs méthodes statiques à utiliser avec des valeurs `char`.</span><span class="sxs-lookup"><span data-stu-id="30eeb-119">The <xref:System.Char?displayProperty=nameWithType> type provides several static methods for working with `char` values.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="30eeb-120">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="30eeb-120">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="30eeb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30eeb-121">See also</span></span>

- <xref:System.Char>  
- [<span data-ttu-id="30eeb-122">Référence C#</span><span class="sxs-lookup"><span data-stu-id="30eeb-122">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="30eeb-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="30eeb-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="30eeb-124">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="30eeb-124">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="30eeb-125">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="30eeb-125">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
- [<span data-ttu-id="30eeb-126">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="30eeb-126">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [<span data-ttu-id="30eeb-127">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="30eeb-127">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
- [<span data-ttu-id="30eeb-128">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="30eeb-128">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  
- [<span data-ttu-id="30eeb-129">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="30eeb-129">Nullable Types</span></span>](../../../csharp/programming-guide/nullable-types/index.md)  
- [<span data-ttu-id="30eeb-130">Chaînes</span><span class="sxs-lookup"><span data-stu-id="30eeb-130">Strings</span></span>](../../../csharp/programming-guide/strings/index.md)