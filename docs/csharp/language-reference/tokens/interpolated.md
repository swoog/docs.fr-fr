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
ms.openlocfilehash: b6873c3b419323fa9f5523143ad607289b6fd6e2
ms.sourcegitcommit: 935d5267c44f9bce801468ef95f44572f1417e8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2018
---
# <a name="---string-interpolation-c-reference"></a><span data-ttu-id="257fe-103">$ - interpolation de chaîne (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="257fe-103">$ - string interpolation (C# Reference)</span></span>

<span data-ttu-id="257fe-104">Le caractère spécial `$` identifie un littéral de chaîne comme une *chaîne interpolée*.</span><span class="sxs-lookup"><span data-stu-id="257fe-104">The `$` special character identifies a string literal as an *interpolated string*.</span></span> <span data-ttu-id="257fe-105">Une chaîne interpolée ressemble à une chaîne de modèle contenant des *expressions interpolées*.</span><span class="sxs-lookup"><span data-stu-id="257fe-105">An interpolated string looks like a template string that contains *interpolated expressions*.</span></span> <span data-ttu-id="257fe-106">Quand la chaîne interpolée est résolue, par exemple, dans une instruction d’assignation ou un appel de méthode, les expressions interpolées sont remplacées par la représentation sous forme de chaîne de leur résultat pour former la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="257fe-106">When the interpolated string is resolved, for example in an assignment statement or a method call, interpolated expressions are replaced by the string representations of their results to produce the result string.</span></span> <span data-ttu-id="257fe-107">Cette fonctionnalité est disponible dans C# 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="257fe-107">This feature is available in C# 6 and later versions.</span></span>

<span data-ttu-id="257fe-108">L’interpolation de chaîne est un moyen plus lisible et plus pratique de créer des chaînes mises en forme que la fonctionnalité de [mise en forme de chaîne composite](../../../standard/base-types/composite-formatting.md).</span><span class="sxs-lookup"><span data-stu-id="257fe-108">String interpolation is a more readable and convenient way to create formatted strings than a [string composite formatting](../../../standard/base-types/composite-formatting.md) feature.</span></span> <span data-ttu-id="257fe-109">L’exemple suivant utilise les deux fonctionnalités pour produire la même sortie :</span><span class="sxs-lookup"><span data-stu-id="257fe-109">The following example uses both features to produce the same output:</span></span>

[!code-csharp-interactive[compare with composite formatting](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#1)]

> [!NOTE]
> <span data-ttu-id="257fe-110">N’ajoutez pas d’espace blanc entre les signes `$` et `"` au début de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="257fe-110">You cannot have any white space between the `$` and the `"` that starts the string.</span></span> <span data-ttu-id="257fe-111">Cela provoque une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="257fe-111">Doing so causes a compile-time error.</span></span>

<span data-ttu-id="257fe-112">La structure d’un élément avec une expression interpolée est comme suit :</span><span class="sxs-lookup"><span data-stu-id="257fe-112">The structure of an item with an interpolated expression is as follows:</span></span>

```
{<interpolatedExpression>[,<alignment>][:<formatString>]}
```

<span data-ttu-id="257fe-113">Les éléments entre crochets sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="257fe-113">Elements in square brackets are optional.</span></span> <span data-ttu-id="257fe-114">Le tableau suivant décrit chaque élément.</span><span class="sxs-lookup"><span data-stu-id="257fe-114">The following table describes each element.</span></span>

|<span data-ttu-id="257fe-115">Élément</span><span class="sxs-lookup"><span data-stu-id="257fe-115">Element</span></span>|<span data-ttu-id="257fe-116">Description</span><span class="sxs-lookup"><span data-stu-id="257fe-116">Description</span></span>|
|-------------|-----------------|
|`interpolatedExpression`|<span data-ttu-id="257fe-117">Expression à évaluer pour obtenir la mise en forme d’un résultat.</span><span class="sxs-lookup"><span data-stu-id="257fe-117">The expression to evaluate to get a result to be formatted.</span></span> <span data-ttu-id="257fe-118">La représentation sous forme de chaîne du résultat `null` est <xref:System.String.Empty?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="257fe-118">String representation of the `null` result is <xref:System.String.Empty?displayProperty=nameWithType>.</span></span>|
|`alignment`|<span data-ttu-id="257fe-119">Expression constante dont la valeur définit le nombre minimal de caractères dans la représentation sous forme de chaîne du résultat de l’expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="257fe-119">The constant expression whose value defines the minimum number of characters in the string representation of the result of the interpolated expression.</span></span> <span data-ttu-id="257fe-120">Si le nombre est positif, la représentation sous forme de chaîne est alignée à droite, s’il est négatif, elle est alignée à gauche.</span><span class="sxs-lookup"><span data-stu-id="257fe-120">If positive, the string representation is right-aligned; if negative, it is left-aligned.</span></span> <span data-ttu-id="257fe-121">Pour plus d'informations, consultez [Composant d’alignement](../../../standard/base-types/composite-formatting.md#alignment-component).</span><span class="sxs-lookup"><span data-stu-id="257fe-121">For more information, see [Alignment Component](../../../standard/base-types/composite-formatting.md#alignment-component).</span></span>|
|`formatString`|<span data-ttu-id="257fe-122">Chaîne de format standard ou personnalisé qui est prise en charge par le type de résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="257fe-122">A standard or custom format string that is supported by the type of the expression result.</span></span> <span data-ttu-id="257fe-123">Pour plus d'informations, consultez [Composant de chaîne de format](../../../standard/base-types/composite-formatting.md#format-string-component).</span><span class="sxs-lookup"><span data-stu-id="257fe-123">For more information, see [Format String Component](../../../standard/base-types/composite-formatting.md#format-string-component).</span></span>|

<span data-ttu-id="257fe-124">L’exemple suivant utilise les composants de mise en forme facultatifs décrits dans le tableau ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="257fe-124">The following example uses optional formatting components described in the table above:</span></span>

[!code-csharp-interactive[specify alignment and format string](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#2)]

<span data-ttu-id="257fe-125">Pour ajouter une accolade (« { » ou « } ») dans le texte produit par une chaîne interpolée, utilisez deux accolades « {{ » ou « }} ».</span><span class="sxs-lookup"><span data-stu-id="257fe-125">To include a curly brace ("{" or "}") in the text produced by an interpolated string, use two curly braces, "{{" or "}}".</span></span> <span data-ttu-id="257fe-126">Pour plus d'informations, consultez [Accolades d’échappement](../../../standard/base-types/composite-formatting.md#escaping-braces).</span><span class="sxs-lookup"><span data-stu-id="257fe-126">For more information, see [Escaping Braces](../../../standard/base-types/composite-formatting.md#escaping-braces).</span></span>

<span data-ttu-id="257fe-127">Comme le caractère deux-points (:) a une signification spéciale dans un élément d’expression interpolée, placez l’expression entre parenthèses pour utiliser un [opérateur conditionnel](../operators/conditional-operator.md) dans une expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="257fe-127">As the colon (:) has special meaning in an interpolated expression item, in order to use a [conditional operator](../operators/conditional-operator.md) in an interpolated expression, enclose that expression in parentheses.</span></span>

<span data-ttu-id="257fe-128">L’exemple suivant montre comment ajouter une accolade dans la chaîne de résultat et comment utiliser un opérateur conditionnel dans une expression interpolée :</span><span class="sxs-lookup"><span data-stu-id="257fe-128">The following example shows how to include a curly brace into the result string and how to use a conditional operator in an interpolated expression:</span></span>

[!code-csharp-interactive[example with ternary conditional operator](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#3)]

<span data-ttu-id="257fe-129">Les chaînes interpolées textuelles utilisent le caractère `$` suivi du caractère `@`.</span><span class="sxs-lookup"><span data-stu-id="257fe-129">Verbatim interpolated strings use the `$` character followed by the `@` character.</span></span> <span data-ttu-id="257fe-130">Pour plus d'informations sur les chaînes textuelles, consultez la rubrique [string](../keywords/string.md).</span><span class="sxs-lookup"><span data-stu-id="257fe-130">For more information about verbatim strings, see the [string](../keywords/string.md) topic.</span></span>

> [!NOTE]
> <span data-ttu-id="257fe-131">Le jeton `$` doit apparaître avant le jeton `@` dans une chaîne interpolée textuelle.</span><span class="sxs-lookup"><span data-stu-id="257fe-131">The `$` token must appear before the `@` token in a verbatim interpolated string.</span></span>

## <a name="implicit-conversions"></a><span data-ttu-id="257fe-132">Conversions implicites</span><span class="sxs-lookup"><span data-stu-id="257fe-132">Implicit conversions</span></span>

<span data-ttu-id="257fe-133">Trois conversions de type implicite sont possibles à partir d’une chaîne interpolée :</span><span class="sxs-lookup"><span data-stu-id="257fe-133">There are three implicit type conversions from an interpolated string:</span></span>

1. <span data-ttu-id="257fe-134">Conversion d’une chaîne interpolée en instance de <xref:System.String> qui est le résultat de la résolution d’une chaîne interpolée avec des éléments d’expression interpolée remplacés par la représentation sous forme de chaîne correctement mise en forme de leurs résultats.</span><span class="sxs-lookup"><span data-stu-id="257fe-134">Conversion of an interpolated string to a <xref:System.String> instance that is the result of interpolated string resolution with interpolated expression items being replaced with the properly formatted string representations of their results.</span></span> <span data-ttu-id="257fe-135">Cette conversion utilise la culture actuelle.</span><span class="sxs-lookup"><span data-stu-id="257fe-135">This conversion uses the current culture.</span></span>

1. <span data-ttu-id="257fe-136">Conversion d’une chaîne interpolée en variable <xref:System.FormattableString> qui représente une chaîne de format composite avec les résultats d’expression à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="257fe-136">Conversion of an interpolated string to a <xref:System.FormattableString> variable that represents a composite format string along with the expression results to be formatted.</span></span> <span data-ttu-id="257fe-137">Cette conversion vous permet de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.FormattableString>.</span><span class="sxs-lookup"><span data-stu-id="257fe-137">That allows you to create multiple result strings with culture-specific content from a single <xref:System.FormattableString> instance.</span></span> <span data-ttu-id="257fe-138">Pour ce faire, appelez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="257fe-138">To do that call one of the following methods:</span></span>

      - <span data-ttu-id="257fe-139">Une surcharge <xref:System.FormattableString.ToString> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.CurrentCulture>.</span><span class="sxs-lookup"><span data-stu-id="257fe-139">A <xref:System.FormattableString.ToString> overload that produces a result string for the <xref:System.Globalization.CultureInfo.CurrentCulture>.</span></span>
      - <span data-ttu-id="257fe-140">Une méthode <xref:System.FormattableString.Invariant%2A> qui produit une chaîne de résultat pour <xref:System.Globalization.CultureInfo.InvariantCulture>.</span><span class="sxs-lookup"><span data-stu-id="257fe-140">A <xref:System.FormattableString.Invariant%2A> method that produces a result string for the <xref:System.Globalization.CultureInfo.InvariantCulture>.</span></span>
      - <span data-ttu-id="257fe-141">Une méthode <xref:System.FormattableString.ToString(System.IFormatProvider)> qui produit une chaîne de résultat pour une culture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="257fe-141">A <xref:System.FormattableString.ToString(System.IFormatProvider)> method that produces a result string for a specified culture.</span></span>

1. <span data-ttu-id="257fe-142">Conversion d’une chaîne interpolée en variable <xref:System.IFormattable> qui vous permet aussi de créer plusieurs chaînes de résultat avec du contenu propre à la culture à partir d’une seule instance de <xref:System.IFormattable>.</span><span class="sxs-lookup"><span data-stu-id="257fe-142">Conversion of an interpolated string to an <xref:System.IFormattable> variable that also allows you to create multiple result strings with culture-specific content from a single <xref:System.IFormattable> instance.</span></span>

<span data-ttu-id="257fe-143">L’exemple suivant utilise la conversion implicite en <xref:System.FormattableString> pour la création de chaînes de résultat propres à la culture :</span><span class="sxs-lookup"><span data-stu-id="257fe-143">The following example uses implicit conversion to <xref:System.FormattableString> for creating culture-specific result strings:</span></span>

[!code-csharp-interactive[create culture-specific result strings](../../../../samples/snippets/csharp/language-reference/tokens/string-interpolation.cs#4)]

## <a name="additional-reading"></a><span data-ttu-id="257fe-144">Lecture supplémentaire</span><span class="sxs-lookup"><span data-stu-id="257fe-144">Additional reading</span></span>

<span data-ttu-id="257fe-145">Si vous ne connaissez pas l’interpolation de chaîne, consultez le guide [Démarrage rapide des chaînes interpolées](../../quick-starts//interpolated-strings.yml).</span><span class="sxs-lookup"><span data-stu-id="257fe-145">If you are new to the string interpolation, check the [interpolated strings quickstart](../../quick-starts//interpolated-strings.yml).</span></span> <span data-ttu-id="257fe-146">Pour plus d’exemples, consultez le [didacticiel sur l’interpolation de chaîne](../../tutorials/string-interpolation.md).</span><span class="sxs-lookup"><span data-stu-id="257fe-146">For more examples, see the [string interpolation tutorial](../../tutorials/string-interpolation.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="257fe-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="257fe-147">See also</span></span>  
 <xref:System.String.Format%2A?displayProperty=nameWithType>  
 <xref:System.FormattableString?displayProperty=nameWithType>  
 <xref:System.IFormattable?displayProperty=nameWithType>  
 [<span data-ttu-id="257fe-148">Mise en forme composite</span><span class="sxs-lookup"><span data-stu-id="257fe-148">Composite formatting</span></span>](../../../standard/base-types/composite-formatting.md)  
 [<span data-ttu-id="257fe-149">Chaînes</span><span class="sxs-lookup"><span data-stu-id="257fe-149">Strings</span></span>](../../../csharp/programming-guide/strings/index.md)  
 [<span data-ttu-id="257fe-150">Caractères spéciaux C#</span><span class="sxs-lookup"><span data-stu-id="257fe-150">C# Special Characters</span></span>](../../../csharp/language-reference/tokens/index.md)  
 [<span data-ttu-id="257fe-151">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="257fe-151">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="257fe-152">Référence C#</span><span class="sxs-lookup"><span data-stu-id="257fe-152">C# Reference</span></span>](../../../csharp/language-reference/index.md)  