---
title: "Chaînes interpolées (C#)"
ms.date: 10/18/2017
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
ms.assetid: 324f267e-1c61-431a-97ed-852c1530742d
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 03315a2d9a44405ff520a1c333f56311e2657df6
ms.sourcegitcommit: 3a96c706e4dbb4667bf3bf37edac9e1666646f93
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2018
---
# <a name="interpolated-strings-c-reference"></a><span data-ttu-id="0b2bc-102">Chaînes interpolées (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0b2bc-102">Interpolated Strings (C# Reference)</span></span>

<span data-ttu-id="0b2bc-103">Permettent de construire des chaînes.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-103">Used to construct strings.</span></span>  <span data-ttu-id="0b2bc-104">Une chaîne interpolée ressemble à une chaîne de modèle contenant des *expressions interpolées*.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-104">An interpolated string looks like a template string that contains *interpolated expressions*.</span></span>  <span data-ttu-id="0b2bc-105">Une chaîne interpolée retourne une chaîne qui remplace les expressions interpolées qu’elle contient par leur représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-105">An interpolated string returns a string that replaces the interpolated expressions that it contains with their string representations.</span></span> <span data-ttu-id="0b2bc-106">Cette fonctionnalité est disponible dans C# 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-106">This feature is available in C# 6 and later versions.</span></span>

<span data-ttu-id="0b2bc-107">Les arguments d’une chaîne interpolée sont plus faciles à comprendre qu’une [chaîne de format composite](../../../standard/base-types/composite-formatting.md#composite-format-string).</span><span class="sxs-lookup"><span data-stu-id="0b2bc-107">The arguments of an interpolated string are easier to understand than a [composite format string](../../../standard/base-types/composite-formatting.md#composite-format-string).</span></span>  <span data-ttu-id="0b2bc-108">Par exemple, la chaîne interpolée</span><span class="sxs-lookup"><span data-stu-id="0b2bc-108">For example, the interpolated string</span></span>  
  
```csharp  
Console.WriteLine($"Name = {name}, hours = {hours:hh}");
```  
<span data-ttu-id="0b2bc-109">contient deux expressions interpolées, ’{name}’ et ’{hours:hh}’.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-109">contains two interpolated expressions, '{name}' and '{hours:hh}'.</span></span> <span data-ttu-id="0b2bc-110">La chaîne de format composite équivalente est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-110">The equivalent composite format string is:</span></span>

```csharp
Console.WriteLine("Name = {0}, hours = {1:hh}", name, hours); 
```  

<span data-ttu-id="0b2bc-111">La structure d’une chaîne interpolée est :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-111">The structure of an interpolated string is:</span></span>  
  
```  
$"<text> {<interpolated-expression> [,<field-width>] [:<format-string>] } <text> ..."  
```  

<span data-ttu-id="0b2bc-112">où :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-112">where:</span></span> 

- <span data-ttu-id="0b2bc-113">*field-width* est un entier signé qui indique le nombre de caractères du champ.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-113">*field-width* is a signed integer that indicates the number of characters in the field.</span></span> <span data-ttu-id="0b2bc-114">S’il est positif, le champ est aligné à droite ; s’il est négatif, il est aligné à gauche.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-114">If it is positive, the field is right-aligned; if negative, left-aligned.</span></span> 

- <span data-ttu-id="0b2bc-115">*format-string* est une chaîne de format qui convient au type d’objet mis en forme.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-115">*format-string* is a format string appropriate for the type of object being formatted.</span></span> <span data-ttu-id="0b2bc-116">Par exemple, pour une valeur <xref:System.DateTime>, cela peut signifier une chaîne de format de date et heure standard, comme "D" ou "d".</span><span class="sxs-lookup"><span data-stu-id="0b2bc-116">For example, for a <xref:System.DateTime> value, it could be a standard date and time format string such as "D" or "d".</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2bc-117">Il ne peut pas y avoir d’espace blanc entre les signes `$` et `"` au début de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-117">You cannot have any whitespace between the `$` and the `"` that starts the string.</span></span> <span data-ttu-id="0b2bc-118">Cela provoque une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-118">Doing so causes a compile-time error.</span></span>

 <span data-ttu-id="0b2bc-119">Vous pouvez utiliser une chaîne interpolée partout où vous pouvez utiliser un littéral de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-119">You can use an interpolated string anywhere you can use a string literal.</span></span>  <span data-ttu-id="0b2bc-120">La chaîne interpolée est évaluée à chaque exécution du code contenant la chaîne interpolée.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-120">The interpolated string is evaluated each time the code with the interpolated string executes.</span></span> <span data-ttu-id="0b2bc-121">Cela vous permet de séparer la définition et l’évaluation d’une chaîne interpolée.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-121">This allows you to separate the definition and evaluation of an interpolated string.</span></span>  
  
 <span data-ttu-id="0b2bc-122">Pour ajouter une accolade ("{" ou "}") dans une chaîne interpolée, utilisez deux accolades "{{" ou "}}".</span><span class="sxs-lookup"><span data-stu-id="0b2bc-122">To include a curly brace ("{" or "}") in an interpolated string, use two curly braces, "{{" or "}}".</span></span>  <span data-ttu-id="0b2bc-123">Pour plus d’informations, consultez la section [Conversions implicites](#implicit-conversions).</span><span class="sxs-lookup"><span data-stu-id="0b2bc-123">See the [Implicit Conversions](#implicit-conversions) section for more details.</span></span>  

<span data-ttu-id="0b2bc-124">Si la chaîne interpolée contient d’autres caractères ayant une signification particulière dans une chaîne interpolée, comme le guillemet ("), les deux-points (:) ou la virgule (,), ils doivent être échappés s’ils se trouvent dans du texte littéral, ou être inclus dans une expression délimitée par des parenthèses s’ils s’agit d’éléments de langage inclus dans une expression interpolée.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-124">If the interpolated string contains other characters with special meaning in an interpolated string, such as the quotation mark ("), colon (:), or comma (,), they should be escaped if they occur in literal text, or they should be included in an expression delimited by parentheses if they are language elements included in an interpolated expression.</span></span> <span data-ttu-id="0b2bc-125">L’exemple suivant échappe des guillemets pour les inclure dans la chaîne de résultat, et utilise des parenthèses pour délimiter l’expression `(age == 1 ? "" : "s")` pour que le signe deux-points ne soit pas interprété comme commençant une chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-125">The following example escapes quotation marks to include them in the result string, and it uses parentheses to delimit the expression `(age == 1 ? "" : "s")` so that the colon is not interpreted as beginning a format string.</span></span>

[!code-csharp[interpolated-strings4](../../../../samples/snippets/csharp/language-reference/keywords/interpolated-strings4.cs#1)]  

<span data-ttu-id="0b2bc-126">Les chaînes interpolées textuelles utilisent le caractère `$` suivi du caractère `@`.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-126">Verbatim interpolated strings use the `$` character followed by the `@` character.</span></span> <span data-ttu-id="0b2bc-127">Pour plus d'informations sur les chaînes textuelles, consultez la rubrique [string](string.md).</span><span class="sxs-lookup"><span data-stu-id="0b2bc-127">For more information about verbatim strings, see the [string](string.md) topic.</span></span> <span data-ttu-id="0b2bc-128">Le code suivant est une version modifiée de l’extrait de code précédent utilisant une chaîne interpolée textuelle :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-128">The following code is a modified version of the previous snippet using a verbatim interpolated string:</span></span>

[!code-csharp[interpolated-strings4](../../../../samples/snippets/csharp/language-reference/keywords/interpolated-strings5.cs#1)]  

<span data-ttu-id="0b2bc-129">Les modifications de mise en forme sont nécessaires car les chaînes textuelles n’obéissent pas aux séquences d’échappement `\`.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-129">The formatting changes are necessary because verbatim strings do not obey `\` escape sequences.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2bc-130">Le jeton `$` doit apparaître avant le jeton `@` dans une chaîne interpolée textuelle.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-130">The `$` token must appear before the `@` token in a verbatim interpolated string.</span></span>


## <a name="implicit-conversions"></a><span data-ttu-id="0b2bc-131">Conversions implicites</span><span class="sxs-lookup"><span data-stu-id="0b2bc-131">Implicit Conversions</span></span>  

<span data-ttu-id="0b2bc-132">Trois conversions de type implicite sont possibles à partir d’une chaîne interpolée :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-132">There are three implicit type conversions from an interpolated string:</span></span>  

1. <span data-ttu-id="0b2bc-133">La conversion d’une chaîne interpolée en un <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-133">Conversion of an interpolated string to a <xref:System.String>.</span></span> <span data-ttu-id="0b2bc-134">L’exemple suivant retourne une chaîne dont les expressions de chaîne interpolée ont été remplacées par leur représentation sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-134">The following example returns a string whose interpolated string expressions have been replaced with their string representations.</span></span> <span data-ttu-id="0b2bc-135">Exemple :</span><span class="sxs-lookup"><span data-stu-id="0b2bc-135">For example:</span></span>

   [!code-csharp[interpolated-strings1](../../../../samples/snippets/csharp/language-reference/keywords/interpolated-strings1.cs#1)]  

   <span data-ttu-id="0b2bc-136">Il s’agit du résultat final d’une interprétation de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-136">This is the final result of a string interpretation.</span></span> <span data-ttu-id="0b2bc-137">Toutes les occurrences d’accolades doubles (« {{ » et « }} ») sont converties en une seule accolade.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-137">All occurrences of double curly braces ("{{" and "}}") are converted to a single curly brace.</span></span> 

2. <span data-ttu-id="0b2bc-138">La conversion d’une chaîne interpolée en une variable <xref:System.IFormattable> qui vous permet de créer plusieurs chaînes de résultats avec un contenu spécifique à la culture, à partir d’une seule instance de <xref:System.IFormattable>.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-138">Conversion of an interpolated string to an <xref:System.IFormattable> variable that allows you to create multiple result strings with culture-specific content from a single <xref:System.IFormattable> instance.</span></span> <span data-ttu-id="0b2bc-139">Ce type de conversion est utile pour inclure des éléments, tels que les formats numériques et les formats de date adaptés à une culture.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-139">This is useful for including such things as the correct numeric and date formats for individual cultures.</span></span>  <span data-ttu-id="0b2bc-140">Toutes les occurrences d’accolades doubles (« {{ » et « }} ») sont conservées tant que vous ne mettez pas en forme la chaîne en appelant explicitement ou implicitement la méthode <xref:System.Object.ToString>.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-140">All occurrences of double curly braces ("{{" and "}}") remain as double curly braces until you format the string by explicitly or implicitly calling the <xref:System.Object.ToString> method.</span></span>  <span data-ttu-id="0b2bc-141">Toutes les expressions d’interpolation contenues sont converties en {0}, {1}, etc.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-141">All contained interpolation expressions are converted to {0}, {1}, and so on.</span></span>  

   <span data-ttu-id="0b2bc-142">L’exemple suivant utilise la réflexion pour afficher les membres ainsi que les valeurs de champ et de propriété d’une variable <xref:System.IFormattable> créée à partir d’une chaîne interpolée.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-142">The following example uses reflection to display the members as well as the field and property values of an <xref:System.IFormattable> variable that is created from an interpolated string.</span></span> <span data-ttu-id="0b2bc-143">Il passe également la variable <xref:System.IFormattable> à la méthode <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-143">It also passes the <xref:System.IFormattable> variable to the <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType> method.</span></span>

   [!code-csharp[interpolated-strings2](../../../../samples/snippets/csharp/language-reference/keywords/interpolated-strings2.cs#1)]  

   <span data-ttu-id="0b2bc-144">Notez que la chaîne interpolée ne peut être inspectée qu’à l’aide de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-144">Note that the interpolated string can be inspected only by using reflection.</span></span> <span data-ttu-id="0b2bc-145">Si elle est passée à une méthode de mise en forme de chaîne, telle que <xref:System.Console.WriteLine(System.String)>, ses éléments de mise en forme sont résolus et la chaîne de résultat est retournée.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-145">If it is passed to a string formatting method, such as <xref:System.Console.WriteLine(System.String)>, its format items are resolved and the result string returned.</span></span> 

3. <span data-ttu-id="0b2bc-146">La conversion d’une chaîne interpolée en variable <xref:System.FormattableString> qui représente une chaîne de format composite.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-146">Conversion of an interpolated string to an <xref:System.FormattableString> variable that represents a composite format string.</span></span> <span data-ttu-id="0b2bc-147">L’inspection de la chaîne de format composite et de son rendu sous forme de chaîne de résultat, peut, par exemple, vous aider à réduire les risques d’attaque par injection pendant la création d’une requête.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-147">Inspecting the composite format string and how it renders as a result string might, for example, help you protect against an injection attack if you were building a query.</span></span> <span data-ttu-id="0b2bc-148"><xref:System.FormattableString> inclut également les surcharges <xref:System.FormattableString.ToString> qui vous permettent de générer des chaînes de résultat pour <xref:System.Globalization.CultureInfo.InvariantCulture> et <xref:System.Globalization.CultureInfo.CurrentCulture>.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-148"><xref:System.FormattableString> also includes <xref:System.FormattableString.ToString> overloads that let you produce result strings for the <xref:System.Globalization.CultureInfo.InvariantCulture> and <xref:System.Globalization.CultureInfo.CurrentCulture>.</span></span>  <span data-ttu-id="0b2bc-149">Toutes les occurrences d’accolades doubles (« {{ » et « }} ») sont conservées, sauf si vous appliquez une mise en forme.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-149">All occurrences of double curly braces ("{{" and "}}") remain as double curly braces, until you format.</span></span>  <span data-ttu-id="0b2bc-150">Toutes les expressions d’interpolation contenues sont converties en {0}, {1}, etc.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-150">All contained interpolation expressions are converted to {0}, {1}, and so on.</span></span>  

   [!code-csharp[interpolated-strings3](../../../../samples/snippets/csharp/language-reference/keywords/interpolated-strings3.cs#1)]  

## <a name="language-specification"></a><span data-ttu-id="0b2bc-151">Spécification du langage</span><span class="sxs-lookup"><span data-stu-id="0b2bc-151">Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0b2bc-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b2bc-152">See also</span></span>  
 <xref:System.IFormattable?displayProperty=nameWithType>  
 <xref:System.FormattableString?displayProperty=nameWithType>  
 <xref:System.String.Format%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="0b2bc-153">Interpolation de chaîne en C#</span><span class="sxs-lookup"><span data-stu-id="0b2bc-153">String Interpolation in C#</span></span>](../../../csharp/tutorials/string-interpolation.md)  
 [<span data-ttu-id="0b2bc-154">Chaînes interpolées en C#</span><span class="sxs-lookup"><span data-stu-id="0b2bc-154">Interpolated strings in C#</span></span>](../../../csharp/quick-starts/interpolated-strings.yml)  
 [<span data-ttu-id="0b2bc-155">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0b2bc-155">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="0b2bc-156">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0b2bc-156">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
