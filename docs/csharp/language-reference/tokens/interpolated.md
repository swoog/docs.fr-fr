---
title: $ - interpolation de chaîne (Référence C#)
description: L’interpolation de chaîne fournit une syntaxe plus lisible et plus pratique pour mettre en forme la sortie de chaîne que la traditionnelle mise en forme composite de chaîne.
ms.date: 03/26/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- $_CSharpKeyword
- $
helpviewer_keywords:
- $ special character [C#]
- $ language element [C#]
- string interpolation [C#]
- interpolated string [C#]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cabb40c9c449780c8c2a504aad3e53938e2ed957
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="---string-interpolation-c-reference"></a><span data-ttu-id="a5f95-103">$ - interpolation de chaîne (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="a5f95-103">$ - string interpolation (C# Reference)</span></span>

<span data-ttu-id="a5f95-104">Le caractère spécial `$` identifie un littéral de chaîne comme une *chaîne interpolée*.</span><span class="sxs-lookup"><span data-stu-id="a5f95-104">The `$` special character identifies a string literal as an *interpolated string*.</span></span> <span data-ttu-id="a5f95-105">Une chaîne interpolée ressemble à une chaîne de modèle contenant des *expressions interpolées*.</span><span class="sxs-lookup"><span data-stu-id="a5f95-105">An interpolated string looks like a template string that contains *interpolated expressions*.</span></span> <span data-ttu-id="a5f95-106">Quand la chaîne interpolée est résolue en une chaîne de résultat, les éléments avec des expressions interpolées sont remplacés par les représentations sous forme de chaînes des résultats des expressions.</span><span class="sxs-lookup"><span data-stu-id="a5f95-106">When the interpolated string is resolved to the result string, items with interpolated expressions are replaced by the string representations of the expression results.</span></span> <span data-ttu-id="a5f95-107">Cette fonctionnalité est disponible dans C# 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a5f95-107">This feature is available in C# 6 and later versions.</span></span>

<span data-ttu-id="a5f95-108">L’interpolation de chaîne offre une syntaxe plus lisible et plus simple pour créer des chaînes mises en forme que la fonctionnalité de [mise en forme de chaîne composite](../../../standard/base-types/composite-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="a5f95-108">String interpolation provides a more readable and convenient syntax to create formatted strings than a [string composite formatting](../../../standard/base-types/composite-formatting.md) feature.</span></span> <span data-ttu-id="a5f95-109">L’exemple suivant utilise les deux fonctionnalités pour produire la même sortie :</span><span class="sxs-lookup"><span data-stu-id="a5f95-109">The following example uses both features to produce the same output:</span></span>

[!code-csharp-interactive[compare with composite formatting](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#1)]

> [!NOTE]
> <span data-ttu-id="a5f95-110">N’ajoutez pas d’espace blanc entre les signes `$` et `"` au début de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a5f95-110">You cannot have any white space between the `$` and the `"` that starts the string.</span></span> <span data-ttu-id="a5f95-111">Cela provoque une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="a5f95-111">Doing so causes a compile-time error.</span></span>

<span data-ttu-id="a5f95-112">La structure d’un élément avec une expression interpolée est comme suit :</span><span class="sxs-lookup"><span data-stu-id="a5f95-112">The structure of an item with an interpolated expression is as follows:</span></span>

```
{<interpolatedExpression>[,<alignment>][:<formatString>]}
```

<span data-ttu-id="a5f95-113">Les éléments entre crochets sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="a5f95-113">Elements in square brackets are optional.</span></span> <span data-ttu-id="a5f95-114">Le tableau suivant décrit chaque élément.</span><span class="sxs-lookup"><span data-stu-id="a5f95-114">The following table describes each element.</span></span>

|<span data-ttu-id="a5f95-115">Élément</span><span class="sxs-lookup"><span data-stu-id="a5f95-115">Element</span></span>|<span data-ttu-id="a5f95-116">Description</span><span class="sxs-lookup"><span data-stu-id="a5f95-116">Description</span></span>|
|-------------|-----------------|
|`interpolatedExpression`|<span data-ttu-id="a5f95-117">Expression à évaluer pour obtenir la mise en forme d’un résultat.</span><span class="sxs-lookup"><span data-stu-id="a5f95-117">The expression to evaluate to get a result to be formatted.</span></span> <span data-ttu-id="a5f95-118">La représentation sous forme de chaîne du résultat `null` est <xref:System.String.Empty?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="a5f95-118">String representation of the `null` result is <xref:System.String.Empty?displayProperty=nameWithType>.</span></span>|
|`alignment`|<span data-ttu-id="a5f95-119">Expression constante dont la valeur définit le nombre minimal de caractères dans la représentation sous forme de chaîne du résultat de l’expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="a5f95-119">The constant expression whose value defines the minimum number of characters in the string representation of the result of the interpolated expression.</span></span> <span data-ttu-id="a5f95-120">Si le nombre est positif, la représentation sous forme de chaîne est alignée à droite, s’il est négatif, elle est alignée à gauche.</span><span class="sxs-lookup"><span data-stu-id="a5f95-120">If positive, the string representation is right-aligned; if negative, it is left-aligned.</span></span> <span data-ttu-id="a5f95-121">Pour plus d'informations, consultez [Composant d’alignement](../../../standard/base-types/composite-formatting.md#alignment-component).</span><span class="sxs-lookup"><span data-stu-id="a5f95-121">For more information, see [Alignment Component](../../../standard/base-types/composite-formatting.md#alignment-component).</span></span>|
|`formatString`|<span data-ttu-id="a5f95-122">Chaîne de format standard ou personnalisé qui est prise en charge par le type de résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="a5f95-122">A standard or custom format string that is supported by the type of the expression result.</span></span> <span data-ttu-id="a5f95-123">Pour plus d'informations, consultez [Composant de chaîne de format](../../../standard/base-types/composite-formatting.md#format-string-component).</span><span class="sxs-lookup"><span data-stu-id="a5f95-123">For more information, see [Format String Component](../../../standard/base-types/composite-formatting.md#format-string-component).</span></span>|

<span data-ttu-id="a5f95-124">L’exemple suivant utilise les composants de mise en forme facultatifs décrits ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="a5f95-124">The following example uses optional formatting components described above:</span></span>

[!code-csharp-interactive[specify alignment and format string](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#2)]

<span data-ttu-id="a5f95-125">Pour ajouter une accolade (« { » ou « } ») dans le texte produit par une chaîne interpolée, entrez deux accolades « {{ » ou « }} ».</span><span class="sxs-lookup"><span data-stu-id="a5f95-125">To include a brace ("{" or "}") in the text produced by an interpolated string, use two braces, "{{" or "}}".</span></span> <span data-ttu-id="a5f95-126">Pour plus d'informations, consultez [Accolades d’échappement](../../../standard/base-types/composite-formatting.md#escaping-braces).</span><span class="sxs-lookup"><span data-stu-id="a5f95-126">For more information, see [Escaping Braces](../../../standard/base-types/composite-formatting.md#escaping-braces).</span></span>

<span data-ttu-id="a5f95-127">Comme le caractère deux-points (:) a une signification spéciale dans un élément d’expression interpolée, placez l’expression entre parenthèses pour utiliser un [opérateur conditionnel](../operators/conditional-operator.md) dans une expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="a5f95-127">As the colon (:) has special meaning in an interpolated expression item, in order to use a [conditional operator](../operators/conditional-operator.md) in an interpolated expression, enclose that expression in parentheses.</span></span>

<span data-ttu-id="a5f95-128">L’exemple suivant montre comment ajouter une accolade dans la chaîne de résultat et comment utiliser un opérateur conditionnel dans une expression interpolée :</span><span class="sxs-lookup"><span data-stu-id="a5f95-128">The following example shows how to include a brace into the result string and how to use a conditional operator in an interpolated expression:</span></span>

[!code-csharp-interactive[example with ternary conditional operator](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#3)]

<span data-ttu-id="a5f95-129">Les chaînes interpolées textuelles utilisent le caractère `$` suivi du caractère `@`.</span><span class="sxs-lookup"><span data-stu-id="a5f95-129">Verbatim interpolated strings use the `$` character followed by the `@` character.</span></span> <span data-ttu-id="a5f95-130">Pour plus d'informations sur les chaînes textuelles, consultez la rubrique [string](../keywords/string.md).</span><span class="sxs-lookup"><span data-stu-id="a5f95-130">For more information about verbatim strings, see the [string](../keywords/string.md) topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a5f95-131">Le jeton `$` doit apparaître avant le jeton `@` dans une chaîne interpolée textuelle.</span><span class="sxs-lookup"><span data-stu-id="a5f95-131">The `$` token must appear before the `@` token in a verbatim interpolated string.</span></span>

<span data-ttu-id="a5f95-132">Trois conversions implicites sont possibles à partir d’une chaîne interpolée :</span><span class="sxs-lookup"><span data-stu-id="a5f95-132">There are three implicit conversions from an interpolated string:</span></span>

1. <span data-ttu-id="a5f95-133">Conversion d’une chaîne interpolée en instance de <xref:System.String> qui est le résultat de la résolution d’une chaîne interpolée avec des éléments d’expression interpolée remplacés par la représentation sous forme de chaîne correctement mise en forme de leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="a5f95-133">Conversion of an interpolated string to a <xref:System.String> instance that is the result of interpolated string resolution with interpolated expression items being replaced with the properly formatted string representations of their results.</span></span> <span data-ttu-id="a5f95-134">Cette conversion utilise la culture actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5f95-134">This conversion uses the current culture.</span></span>

1. <span data-ttu-id="a5f95-135">Conversion d’une chaîne interpolée en instance <xref:System.FormattableString> qui représente une chaîne de format composite avec les résultats d’expression à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="a5f95-135">Conversion of an interpolated string to a <xref:System.FormattableString> instance that represents a composite format string along with the expression results to be formatted.</span></span> <span data-ttu-id="a5f95-136">Cette conversion vous permet de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.FormattableString>.</span><span class="sxs-lookup"><span data-stu-id="a5f95-136">That allows you to create multiple result strings with culture-specific content from a single <xref:System.FormattableString> instance.</span></span> <span data-ttu-id="a5f95-137">Pour ce faire, appelez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5f95-137">To do that call one of the following methods:</span></span>

      - <span data-ttu-id="a5f95-138">Une surcharge <xref:System.FormattableString.ToString> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.CurrentCulture>.</span><span class="sxs-lookup"><span data-stu-id="a5f95-138">A <xref:System.FormattableString.ToString> overload that produces a result string for the <xref:System.Globalization.CultureInfo.CurrentCulture>.</span></span>
      - <span data-ttu-id="a5f95-139">Une méthode <xref:System.FormattableString.Invariant%2A> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.InvariantCulture>.</span><span class="sxs-lookup"><span data-stu-id="a5f95-139">A <xref:System.FormattableString.Invariant%2A> method that produces a result string for the <xref:System.Globalization.CultureInfo.InvariantCulture>.</span></span>
      - <span data-ttu-id="a5f95-140">Une méthode <xref:System.FormattableString.ToString(System.IFormatProvider)> qui produit une chaîne de résultat pour une culture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a5f95-140">A <xref:System.FormattableString.ToString(System.IFormatProvider)> method that produces a result string for a specified culture.</span></span>

1. <span data-ttu-id="a5f95-141">Conversion d’une chaîne interpolée en instance <xref:System.IFormattable> qui vous permet aussi de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.IFormattable>.</span><span class="sxs-lookup"><span data-stu-id="a5f95-141">Conversion of an interpolated string to an <xref:System.IFormattable> instance that also allows you to create multiple result strings with culture-specific content from a single <xref:System.IFormattable> instance.</span></span>

<span data-ttu-id="a5f95-142">L’exemple suivant utilise la conversion implicite en <xref:System.FormattableString> pour créer des chaînes de résultat propres à la culture :</span><span class="sxs-lookup"><span data-stu-id="a5f95-142">The following example uses implicit conversion to <xref:System.FormattableString> to create culture-specific result strings:</span></span>

[!code-csharp-interactive[create culture-specific result strings](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#4)]

<span data-ttu-id="a5f95-143">Si vous ne connaissez pas l’interpolation de chaîne, consultez le guide de démarrage rapide [Interpolation de chaîne en C#](../../quick-starts/interpolated-strings.yml).</span><span class="sxs-lookup"><span data-stu-id="a5f95-143">If you are new to the string interpolation, check the [String interpolation in C#](../../quick-starts/interpolated-strings.yml) quickstart.</span></span> <span data-ttu-id="a5f95-144">Pour plus d’exemples, consultez le [didacticiel sur l’interpolation de chaîne](../../tutorials/string-interpolation.md).</span><span class="sxs-lookup"><span data-stu-id="a5f95-144">For more examples, see the [string interpolation tutorial](../../tutorials/string-interpolation.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a5f95-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5f95-145">See also</span></span>  
 <xref:System.String.Format%2A?displayProperty=nameWithType>  
 <xref:System.FormattableString?displayProperty=nameWithType>  
 <xref:System.IFormattable?displayProperty=nameWithType>  
 [<span data-ttu-id="a5f95-146">Mise en forme composite</span><span class="sxs-lookup"><span data-stu-id="a5f95-146">Composite formatting</span></span>](../../../standard/base-types/composite-formatting.md)  
 [<span data-ttu-id="a5f95-147">Chaînes</span><span class="sxs-lookup"><span data-stu-id="a5f95-147">Strings</span></span>](../../../csharp/programming-guide/strings/index.md)  
 [<span data-ttu-id="a5f95-148">Caractères spéciaux C#</span><span class="sxs-lookup"><span data-stu-id="a5f95-148">C# Special Characters</span></span>](../../../csharp/language-reference/tokens/index.md)  
 [<span data-ttu-id="a5f95-149">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a5f95-149">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="a5f95-150">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a5f95-150">C# Reference</span></span>](../../../csharp/language-reference/index.md)  