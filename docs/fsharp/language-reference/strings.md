---
title: Chaînes (F#)
description: Découvrez comment le type 'string' F# représente le texte immuable sous la forme d’une séquence de caractères Unicode.
ms.date: 05/16/2016
ms.openlocfilehash: 21971602093bc84b0df47d4ae46a14fb936c28bb
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43799341"
---
# <a name="strings"></a><span data-ttu-id="c7cd1-103">Chaînes</span><span class="sxs-lookup"><span data-stu-id="c7cd1-103">Strings</span></span>

> [!NOTE]
<span data-ttu-id="c7cd1-104">Les liens des informations de référence sur les API qui figurent dans cet article pointent vers MSDN.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-104">The API reference links in this article will take you to MSDN.</span></span>  <span data-ttu-id="c7cd1-105">Les informations de référence sur les API docs.microsoft.com ne sont pas terminées.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-105">The docs.microsoft.com API reference is not complete.</span></span>

<span data-ttu-id="c7cd1-106">Le `string` type représente le texte immuable sous la forme d’une séquence de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-106">The `string` type represents immutable text as a sequence of Unicode characters.</span></span> <span data-ttu-id="c7cd1-107">`string` est un alias pour `System.String` dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-107">`string` is an alias for `System.String` in the .NET Framework.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7cd1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c7cd1-108">Remarks</span></span>

<span data-ttu-id="c7cd1-109">Littéraux de chaîne sont délimitées par le caractère guillemet (").</span><span class="sxs-lookup"><span data-stu-id="c7cd1-109">String literals are delimited by the quotation mark (") character.</span></span> <span data-ttu-id="c7cd1-110">Le caractère barre oblique inverse ( \\ ) est utilisé pour encoder certains caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-110">The backslash character ( \\ ) is used to encode certain special characters.</span></span> <span data-ttu-id="c7cd1-111">La barre oblique inverse et le caractère suivant forment sont appelés une *séquence d’échappement*.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-111">The backslash and the next character together are known as an *escape sequence*.</span></span> <span data-ttu-id="c7cd1-112">Prise en charge par F# littéraux sont affichés dans le tableau suivant de chaîne de séquences d’échappement.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-112">Escape sequences supported in F# string literals are shown in the following table.</span></span>

|<span data-ttu-id="c7cd1-113">Caractère</span><span class="sxs-lookup"><span data-stu-id="c7cd1-113">Character</span></span>|<span data-ttu-id="c7cd1-114">Séquence d'échappement</span><span class="sxs-lookup"><span data-stu-id="c7cd1-114">Escape sequence</span></span>|
|---------|---------------|
|<span data-ttu-id="c7cd1-115">Retour arrière</span><span class="sxs-lookup"><span data-stu-id="c7cd1-115">Backspace</span></span>|`\b`|
|<span data-ttu-id="c7cd1-116">Saut de ligne</span><span class="sxs-lookup"><span data-stu-id="c7cd1-116">Newline</span></span>|`\n`|
|<span data-ttu-id="c7cd1-117">Retour chariot</span><span class="sxs-lookup"><span data-stu-id="c7cd1-117">Carriage return</span></span>|`\r`|
|<span data-ttu-id="c7cd1-118">Onglet</span><span class="sxs-lookup"><span data-stu-id="c7cd1-118">Tab</span></span>|`\t`|
|<span data-ttu-id="c7cd1-119">Barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="c7cd1-119">Backslash</span></span>|`\\`|
|<span data-ttu-id="c7cd1-120">Guillemet</span><span class="sxs-lookup"><span data-stu-id="c7cd1-120">Quotation mark</span></span>|`\"`|
|<span data-ttu-id="c7cd1-121">Apostrophe</span><span class="sxs-lookup"><span data-stu-id="c7cd1-121">Apostrophe</span></span>|`\'`|
|<span data-ttu-id="c7cd1-122">caractère Unicode</span><span class="sxs-lookup"><span data-stu-id="c7cd1-122">Unicode character</span></span>|<span data-ttu-id="c7cd1-123">`\uXXXX` ou `\UXXXX` (où `X` indique un chiffre hexadécimal)</span><span class="sxs-lookup"><span data-stu-id="c7cd1-123">`\uXXXX` or `\UXXXX` (where `X` indicates a hexadecimal digit)</span></span>|

<span data-ttu-id="c7cd1-124">Si précédé par le symbole @, le littéral est une chaîne textuelle.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-124">If preceded by the @ symbol, the literal is a verbatim string.</span></span> <span data-ttu-id="c7cd1-125">Cela signifie que les séquences d’échappement sont ignorés, sauf que deux caractères de guillemet sont interprétés comme un seul guillemet.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-125">This means that any escape sequences are ignored, except that two quotation mark characters are interpreted as one quotation mark character.</span></span>

<span data-ttu-id="c7cd1-126">En outre, une chaîne peut être placé entre guillemets triples.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-126">Additionally, a string may be enclosed by triple quotes.</span></span> <span data-ttu-id="c7cd1-127">Dans ce cas, toutes les séquences d’échappement sont ignorés, y compris les caractères de guillemet double.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-127">In this case, all escape sequences are ignored, including double quotation mark characters.</span></span> <span data-ttu-id="c7cd1-128">Pour spécifier une chaîne qui contient un élément incorporé chaîne entre guillemets, vous pouvez utiliser une chaîne textuelle ou une chaîne entre guillemets de triple.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-128">To specify a string that contains an embedded quoted string, you can either use a verbatim string or a triple-quoted string.</span></span> <span data-ttu-id="c7cd1-129">Si vous utilisez une chaîne textuelle, vous devez spécifier deux caractères de guillemet pour indiquer un caractère de guillemet.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-129">If you use a verbatim string, you  must specify two quotation mark characters to indicate a single quotation mark character.</span></span> <span data-ttu-id="c7cd1-130">Si vous utilisez une chaîne entre guillemets de triple, vous pouvez utiliser les caractères guillemet-apostrophe sans eux analysé en tant que la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-130">If you use a triple-quoted string, you can use the single quotation mark characters without them being parsed as the end of the string.</span></span> <span data-ttu-id="c7cd1-131">Cette technique peut être utile lorsque vous travaillez avec XML ou d’autres structures qui incluent les guillemets incorporés.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-131">This technique can be useful when you work with XML or other structures that include embedded quotation marks.</span></span>

```fsharp
// Using a verbatim string
let xmlFragment1 = @"<book author=""Milton, John"" title=""Paradise Lost"">"

// Using a triple-quoted string
let xmlFragment2 = """<book author="Milton, John" title="Paradise Lost">"""
```

<span data-ttu-id="c7cd1-132">Dans le code, les chaînes qui ont des sauts de ligne sont acceptées et les sauts de ligne sont interprétés littéralement comme des sauts de ligne, sauf si un caractère de barre oblique inverse est le dernier caractère avant le saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-132">In code, strings that have line breaks are accepted and the line breaks are interpreted literally as newlines, unless a backslash character is the last character before the line break.</span></span> <span data-ttu-id="c7cd1-133">Espace blanc de début sur la ligne suivante est ignoré lorsque le caractère barre oblique inverse est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-133">Leading white space on the next line is ignored when the backslash character is used.</span></span> <span data-ttu-id="c7cd1-134">Le code suivant produit une chaîne `str1` qui a la valeur `"abc\ndef"` et une chaîne `str2` qui a la valeur `"abcdef"`.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-134">The following code produces a string `str1` that has value `"abc\ndef"` and a string `str2` that has value `"abcdef"`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1001.fs)]

<span data-ttu-id="c7cd1-135">Vous pouvez accéder à des caractères individuels dans une chaîne à l’aide de syntaxe de type tableau, comme suit.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-135">You can access individual characters in a string by using array-like syntax, as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1002.fs)]

<span data-ttu-id="c7cd1-136">Le résultat est `b`.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-136">The output is `b`.</span></span>

<span data-ttu-id="c7cd1-137">Ou vous pouvez extraire des sous-chaînes à l’aide de syntaxe de découpage de tableau, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-137">Or you can extract substrings by using array slice syntax, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1003.fs)]

<span data-ttu-id="c7cd1-138">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-138">The output is as follows.</span></span>

```
abc
def
```

<span data-ttu-id="c7cd1-139">Vous pouvez représenter les chaînes ASCII par des tableaux d’octets non signés, type `byte[]`.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-139">You can represent ASCII strings by arrays of unsigned bytes, type `byte[]`.</span></span> <span data-ttu-id="c7cd1-140">Vous ajoutez le suffixe `B` à un littéral de chaîne pour indiquer qu’il s’agit d’une chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-140">You add the suffix `B` to a string literal to indicate that it is an ASCII string.</span></span> <span data-ttu-id="c7cd1-141">Les littéraux de chaîne ASCII utilisés avec les tableaux d’octets prend en charge les mêmes séquences d’échappement sous forme de chaînes Unicode à l’exception des séquences d’échappement Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-141">ASCII string literals used with byte arrays support the same escape sequences as Unicode strings, except for the Unicode escape sequences.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1004.fs)]

## <a name="string-operators"></a><span data-ttu-id="c7cd1-142">Opérateurs de chaîne</span><span class="sxs-lookup"><span data-stu-id="c7cd1-142">String Operators</span></span>

<span data-ttu-id="c7cd1-143">Il existe deux façons de concaténer des chaînes : à l’aide de la `+` opérateur ou à l’aide de la `^` opérateur.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-143">There are two ways to concatenate strings: by using the `+` operator or by using the `^` operator.</span></span> <span data-ttu-id="c7cd1-144">Le `+` opérateur assure la compatibilité avec la chaîne de .NET Framework gère les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-144">The `+` operator maintains compatibility with the .NET Framework string handling features.</span></span>

<span data-ttu-id="c7cd1-145">L’exemple suivant illustre la concaténation de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-145">The following example illustrates string concatenation.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1006.fs)]

## <a name="string-class"></a><span data-ttu-id="c7cd1-146">Classe de chaîne</span><span class="sxs-lookup"><span data-stu-id="c7cd1-146">String Class</span></span>

<span data-ttu-id="c7cd1-147">Étant donné que le type de chaîne en F# est en fait un .NET Framework `System.String` taper, tout le `System.String` membres sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-147">Because the string type in F# is actually a .NET Framework `System.String` type, all the `System.String` members are available.</span></span> <span data-ttu-id="c7cd1-148">Cela inclut la `+` opérateur, qui est utilisé pour concaténer des chaînes, la `Length` propriété et le `Chars` propriété, qui retourne la chaîne sous la forme d’un tableau de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-148">This includes the `+` operator, which is used to concatenate strings, the `Length` property, and the `Chars` property, which returns the string as an array of Unicode characters.</span></span> <span data-ttu-id="c7cd1-149">Pour plus d’informations sur les chaînes, consultez `System.String`.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-149">For more information about strings, see `System.String`.</span></span>

<span data-ttu-id="c7cd1-150">À l’aide de la `Chars` propriété du `System.String`, vous pouvez accéder à différents caractères dans une chaîne en spécifiant un index, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-150">By using the `Chars` property of `System.String`, you can access the individual characters in a string by specifying an index, as is shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1005.fs)]

## <a name="string-module"></a><span data-ttu-id="c7cd1-151">Module de chaîne</span><span class="sxs-lookup"><span data-stu-id="c7cd1-151">String Module</span></span>

<span data-ttu-id="c7cd1-152">Des fonctionnalités supplémentaires pour la gestion des chaînes sont incluses dans le `String` module dans le `FSharp.Core` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c7cd1-152">Additional functionality for string handling is included in the `String` module in the `FSharp.Core` namespace.</span></span> <span data-ttu-id="c7cd1-153">Pour plus d’informations, consultez [Core.String, Module](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.string-module-%5bfsharp%5d).</span><span class="sxs-lookup"><span data-stu-id="c7cd1-153">For more information, see [Core.String Module](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.string-module-%5bfsharp%5d).</span></span>

## <a name="see-also"></a><span data-ttu-id="c7cd1-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7cd1-154">See also</span></span>

- [<span data-ttu-id="c7cd1-155">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="c7cd1-155">F# Language Reference</span></span>](index.md)
