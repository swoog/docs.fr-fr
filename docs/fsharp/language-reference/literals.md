---
title: Littéraux (F#)
description: En savoir plus sur les types de littéraux dans le langage de programmation F#.
ms.date: 05/16/2016
ms.openlocfilehash: e6d34acd928edce8447c793105b08085ab0757b9
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "44087623"
---
# <a name="literals"></a><span data-ttu-id="bc280-103">Littéraux</span><span class="sxs-lookup"><span data-stu-id="bc280-103">Literals</span></span>

> [!NOTE]
<span data-ttu-id="bc280-104">Les liens de référence des API dans cet article vous dirigera vers MSDN (pour l’instant).</span><span class="sxs-lookup"><span data-stu-id="bc280-104">The API reference links in this article will take you to MSDN (for now).</span></span>

<span data-ttu-id="bc280-105">Cette rubrique fournit une table qui montre comment spécifier le type d’un littéral en F#.</span><span class="sxs-lookup"><span data-stu-id="bc280-105">This topic provides a table that shows how to specify the type of a literal in F#.</span></span>

## <a name="literal-types"></a><span data-ttu-id="bc280-106">Types de littéral</span><span class="sxs-lookup"><span data-stu-id="bc280-106">Literal Types</span></span>

<span data-ttu-id="bc280-107">Le tableau suivant présente les types de littéraux en F#.</span><span class="sxs-lookup"><span data-stu-id="bc280-107">The following table shows the literal types in F#.</span></span> <span data-ttu-id="bc280-108">Les caractères qui représentent des chiffres en notation hexadécimale ne sont pas la casse ; les caractères qui identifient le type respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="bc280-108">Characters that represent digits in hexadecimal notation are not case-sensitive; characters that identify the type are case-sensitive.</span></span>

|<span data-ttu-id="bc280-109">Type</span><span class="sxs-lookup"><span data-stu-id="bc280-109">Type</span></span>|<span data-ttu-id="bc280-110">Description</span><span class="sxs-lookup"><span data-stu-id="bc280-110">Description</span></span>|<span data-ttu-id="bc280-111">Suffixe ou préfixe</span><span class="sxs-lookup"><span data-stu-id="bc280-111">Suffix or prefix</span></span>|<span data-ttu-id="bc280-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="bc280-112">Examples</span></span>|
|----|-----------|----------------|--------|
|<span data-ttu-id="bc280-113">sbyte</span><span class="sxs-lookup"><span data-stu-id="bc280-113">sbyte</span></span>|<span data-ttu-id="bc280-114">entier signé 8 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-114">signed 8-bit integer</span></span>|<span data-ttu-id="bc280-115">o</span><span class="sxs-lookup"><span data-stu-id="bc280-115">y</span></span>|`86y`<br /><br />`0b00000101y`|
|<span data-ttu-id="bc280-116">byte</span><span class="sxs-lookup"><span data-stu-id="bc280-116">byte</span></span>|<span data-ttu-id="bc280-117">nombre de naturel 8 bits non signé</span><span class="sxs-lookup"><span data-stu-id="bc280-117">unsigned 8-bit natural number</span></span>|<span data-ttu-id="bc280-118">UY</span><span class="sxs-lookup"><span data-stu-id="bc280-118">uy</span></span>|`86uy`<br /><br />`0b00000101uy`|
|<span data-ttu-id="bc280-119">int16</span><span class="sxs-lookup"><span data-stu-id="bc280-119">int16</span></span>|<span data-ttu-id="bc280-120">entier signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-120">signed 16-bit integer</span></span>|<span data-ttu-id="bc280-121">s</span><span class="sxs-lookup"><span data-stu-id="bc280-121">s</span></span>|`86s`|
|<span data-ttu-id="bc280-122">uint16</span><span class="sxs-lookup"><span data-stu-id="bc280-122">uint16</span></span>|<span data-ttu-id="bc280-123">nombre de naturel non signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-123">unsigned 16-bit natural number</span></span>|<span data-ttu-id="bc280-124">us</span><span class="sxs-lookup"><span data-stu-id="bc280-124">us</span></span>|`86us`|
|<span data-ttu-id="bc280-125">int</span><span class="sxs-lookup"><span data-stu-id="bc280-125">int</span></span><br /><br /><span data-ttu-id="bc280-126">int32</span><span class="sxs-lookup"><span data-stu-id="bc280-126">int32</span></span>|<span data-ttu-id="bc280-127">entier signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-127">signed 32-bit integer</span></span>|<span data-ttu-id="bc280-128">« l » ou none</span><span class="sxs-lookup"><span data-stu-id="bc280-128">l or none</span></span>|`86`<br /><br />`86l`|
|<span data-ttu-id="bc280-129">uint</span><span class="sxs-lookup"><span data-stu-id="bc280-129">uint</span></span><br /><br /><span data-ttu-id="bc280-130">uint32</span><span class="sxs-lookup"><span data-stu-id="bc280-130">uint32</span></span>|<span data-ttu-id="bc280-131">nombre de naturel non signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-131">unsigned 32-bit natural number</span></span>|<span data-ttu-id="bc280-132">u ou ul</span><span class="sxs-lookup"><span data-stu-id="bc280-132">u or ul</span></span>|`86u`<br /><br />`86ul`|
|<span data-ttu-id="bc280-133">unativeint</span><span class="sxs-lookup"><span data-stu-id="bc280-133">unativeint</span></span>|<span data-ttu-id="bc280-134">pointeur natif sous forme de nombre naturel non signé</span><span class="sxs-lookup"><span data-stu-id="bc280-134">native pointer as an unsigned natural number</span></span>|<span data-ttu-id="bc280-135">Annuler</span><span class="sxs-lookup"><span data-stu-id="bc280-135">un</span></span>|`0x00002D3Fun`|
|<span data-ttu-id="bc280-136">int64</span><span class="sxs-lookup"><span data-stu-id="bc280-136">int64</span></span>|<span data-ttu-id="bc280-137">entier signé 64 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-137">signed 64-bit integer</span></span>|<span data-ttu-id="bc280-138">L</span><span class="sxs-lookup"><span data-stu-id="bc280-138">L</span></span>|`86L`|
|<span data-ttu-id="bc280-139">uint64</span><span class="sxs-lookup"><span data-stu-id="bc280-139">uint64</span></span>|<span data-ttu-id="bc280-140">nombre de naturel non signé 64 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-140">unsigned 64-bit natural number</span></span>|<span data-ttu-id="bc280-141">UL</span><span class="sxs-lookup"><span data-stu-id="bc280-141">UL</span></span>|`86UL`|
|<span data-ttu-id="bc280-142">float32 unique,</span><span class="sxs-lookup"><span data-stu-id="bc280-142">single, float32</span></span>|<span data-ttu-id="bc280-143">nombre à virgule flottante 32 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-143">32-bit floating point number</span></span>|<span data-ttu-id="bc280-144">F ou f</span><span class="sxs-lookup"><span data-stu-id="bc280-144">F or f</span></span>|<span data-ttu-id="bc280-145">`4.14F` ou `4.14f`</span><span class="sxs-lookup"><span data-stu-id="bc280-145">`4.14F` or `4.14f`</span></span>|
|||<span data-ttu-id="bc280-146">LF</span><span class="sxs-lookup"><span data-stu-id="bc280-146">lf</span></span>|`0x00000000lf`|
|<span data-ttu-id="bc280-147">type float ; Double</span><span class="sxs-lookup"><span data-stu-id="bc280-147">float; double</span></span>|<span data-ttu-id="bc280-148">nombre à virgule flottante 64 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-148">64-bit floating point number</span></span>|<span data-ttu-id="bc280-149">none</span><span class="sxs-lookup"><span data-stu-id="bc280-149">none</span></span>|<span data-ttu-id="bc280-150">`4.14` ou `2.3E+32` ou `2.3e+32`</span><span class="sxs-lookup"><span data-stu-id="bc280-150">`4.14` or `2.3E+32` or `2.3e+32`</span></span>|
|||<span data-ttu-id="bc280-151">LF</span><span class="sxs-lookup"><span data-stu-id="bc280-151">LF</span></span>|`0x0000000000000000LF`|
|<span data-ttu-id="bc280-152">bigint</span><span class="sxs-lookup"><span data-stu-id="bc280-152">bigint</span></span>|<span data-ttu-id="bc280-153">entier non limité à la représentation 64 bits</span><span class="sxs-lookup"><span data-stu-id="bc280-153">integer not limited to 64-bit representation</span></span>|<span data-ttu-id="bc280-154">I</span><span class="sxs-lookup"><span data-stu-id="bc280-154">I</span></span>|`9999999999999999999999999999I`|
|<span data-ttu-id="bc280-155">decimal</span><span class="sxs-lookup"><span data-stu-id="bc280-155">decimal</span></span>|<span data-ttu-id="bc280-156">nombre fractionnaire représenté sous la forme à virgule fixe ou un nombre rationnel</span><span class="sxs-lookup"><span data-stu-id="bc280-156">fractional number represented as a fixed point or rational number</span></span>|<span data-ttu-id="bc280-157">M ou m</span><span class="sxs-lookup"><span data-stu-id="bc280-157">M or m</span></span>|<span data-ttu-id="bc280-158">`0.7833M` ou `0.7833m`</span><span class="sxs-lookup"><span data-stu-id="bc280-158">`0.7833M` or `0.7833m`</span></span>|
|<span data-ttu-id="bc280-159">Char</span><span class="sxs-lookup"><span data-stu-id="bc280-159">Char</span></span>|<span data-ttu-id="bc280-160">caractère Unicode</span><span class="sxs-lookup"><span data-stu-id="bc280-160">Unicode character</span></span>|<span data-ttu-id="bc280-161">none</span><span class="sxs-lookup"><span data-stu-id="bc280-161">none</span></span>|`'a'`|
|<span data-ttu-id="bc280-162">Chaîne</span><span class="sxs-lookup"><span data-stu-id="bc280-162">String</span></span>|<span data-ttu-id="bc280-163">chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="bc280-163">Unicode string</span></span>|<span data-ttu-id="bc280-164">none</span><span class="sxs-lookup"><span data-stu-id="bc280-164">none</span></span>|`"text\n"`<br /><br /><span data-ttu-id="bc280-165">ou</span><span class="sxs-lookup"><span data-stu-id="bc280-165">or</span></span><br /><br />`@"c:\filename"`<br /><br /><span data-ttu-id="bc280-166">ou</span><span class="sxs-lookup"><span data-stu-id="bc280-166">or</span></span><br /><br />`"""<book title="Paradise Lost">"""`<br /><br /><span data-ttu-id="bc280-167">ou</span><span class="sxs-lookup"><span data-stu-id="bc280-167">or</span></span><br /><br />`"string1" + "string2"`<br /><br /><span data-ttu-id="bc280-168">Voir aussi [chaînes](Strings.md).</span><span class="sxs-lookup"><span data-stu-id="bc280-168">See also [Strings](Strings.md).</span></span>|
|<span data-ttu-id="bc280-169">byte</span><span class="sxs-lookup"><span data-stu-id="bc280-169">byte</span></span>|<span data-ttu-id="bc280-170">Caractère ASCII</span><span class="sxs-lookup"><span data-stu-id="bc280-170">ASCII character</span></span>|<span data-ttu-id="bc280-171">B</span><span class="sxs-lookup"><span data-stu-id="bc280-171">B</span></span>|`'a'B`|
|<span data-ttu-id="bc280-172">byte[]</span><span class="sxs-lookup"><span data-stu-id="bc280-172">byte[]</span></span>|<span data-ttu-id="bc280-173">Chaîne ASCII</span><span class="sxs-lookup"><span data-stu-id="bc280-173">ASCII string</span></span>|<span data-ttu-id="bc280-174">B</span><span class="sxs-lookup"><span data-stu-id="bc280-174">B</span></span>|`"text"B`|
|<span data-ttu-id="bc280-175">String ou byte]</span><span class="sxs-lookup"><span data-stu-id="bc280-175">String or byte[]</span></span>|<span data-ttu-id="bc280-176">chaîne textuelle</span><span class="sxs-lookup"><span data-stu-id="bc280-176">verbatim string</span></span>|<span data-ttu-id="bc280-177">préfixe « @ »</span><span class="sxs-lookup"><span data-stu-id="bc280-177">@ prefix</span></span>|<span data-ttu-id="bc280-178">`@"\\server\share"` (Unicode)</span><span class="sxs-lookup"><span data-stu-id="bc280-178">`@"\\server\share"` (Unicode)</span></span><br /><br /><span data-ttu-id="bc280-179">`@"\\server\share"B` (ASCII)</span><span class="sxs-lookup"><span data-stu-id="bc280-179">`@"\\server\share"B` (ASCII)</span></span>|

## <a name="remarks"></a><span data-ttu-id="bc280-180">Notes</span><span class="sxs-lookup"><span data-stu-id="bc280-180">Remarks</span></span>

<span data-ttu-id="bc280-181">Chaînes Unicode peuvent contenir des encodages explicites que vous pouvez spécifier à l’aide de `\u` suivi d’un code hexadécimal 16 bits ou les encodages UTF-32 que vous pouvez spécifier à l’aide de `\U` suivie d’un code hexadécimal 32 bits qui représente un Unicode paire de substitution.</span><span class="sxs-lookup"><span data-stu-id="bc280-181">Unicode strings can contain explicit encodings that you can specify by using `\u` followed by a 16-bit hexadecimal code or UTF-32 encodings that you can specify by using `\U` followed by a 32-bit hexadecimal code that represents a Unicode surrogate pair.</span></span>

<span data-ttu-id="bc280-182">Avec F# 3,1, vous pouvez utiliser le `+` vous connecter pour combiner des littéraux de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bc280-182">As of F# 3.1, you can use the `+` sign to combine string literals.</span></span> <span data-ttu-id="bc280-183">Vous pouvez également utiliser l’opérateur de bits ou (`|||`) opérateur pour combiner les indicateurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="bc280-183">You can also use the bitwise or (`|||`) operator to combine enum flags.</span></span> <span data-ttu-id="bc280-184">Par exemple, le code suivant est autorisé dans F# 3.1 :</span><span class="sxs-lookup"><span data-stu-id="bc280-184">For example, the following code is legal in F# 3.1:</span></span>

```fsharp
[<Literal>]
let Literal1 = "a" + "b"

[<Literal>]
let FileLocation =   __SOURCE_DIRECTORY__ + "/" + __SOURCE_FILE__

[<Literal>]
let Literal2 = 1 ||| 64

[<Literal>]
let Literal3 = System.IO.FileAccess.Read ||| System.IO.FileAccess.Write
```

<span data-ttu-id="bc280-185">L’utilisation d’autres opérateurs au niveau du bit n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="bc280-185">The use of other bitwise operators isn't allowed.</span></span>

## <a name="named-literals"></a><span data-ttu-id="bc280-186">Littéraux nommés</span><span class="sxs-lookup"><span data-stu-id="bc280-186">Named Literals</span></span>

<span data-ttu-id="bc280-187">Les valeurs qui sont destinées à être des constantes peuvent être marquées avec le [littéral](https://msdn.microsoft.com/library/465f36ce-d146-41c0-b425-679c509cd285) attribut.</span><span class="sxs-lookup"><span data-stu-id="bc280-187">Values that are intended to be constants can be marked with the [Literal](https://msdn.microsoft.com/library/465f36ce-d146-41c0-b425-679c509cd285) attribute.</span></span> <span data-ttu-id="bc280-188">Cet attribut a pour effet de provoquer une valeur doit être compilé en tant que constante.</span><span class="sxs-lookup"><span data-stu-id="bc280-188">This attribute has the effect of causing a value to be compiled as a constant.</span></span>

<span data-ttu-id="bc280-189">Dans les expressions de critères spéciaux, les identificateurs qui commencent par les caractères minuscules sont toujours traités en tant que variables à lier, plutôt que comme des littéraux, par conséquent, vous devez généralement utiliser majuscules lorsque vous définissez des littéraux.</span><span class="sxs-lookup"><span data-stu-id="bc280-189">In pattern matching expressions, identifiers that begin with lowercase characters are always treated as variables to be bound, rather than as literals, so you should generally use initial capitals when you define literals.</span></span>

## <a name="integers-in-other-bases"></a><span data-ttu-id="bc280-190">Nombres entiers dans d’autres Bases</span><span class="sxs-lookup"><span data-stu-id="bc280-190">Integers In Other Bases</span></span>

<span data-ttu-id="bc280-191">Entiers signés de 32 bits peuvent également être spécifiés dans hexadécimal, octal ou binaire à l’aide un `0x`, `0o` ou `0b` respectivement de préfixe.</span><span class="sxs-lookup"><span data-stu-id="bc280-191">Signed 32-bit integers can also be specified in hexadecimal, octal, or binary using a `0x`, `0o` or `0b` prefix respectively.</span></span>

```fsharp
let Numbers = (0x9F, 0o77, 0b1010)
// Result: Numbers : int * int * int = (159, 63, 10)
```

## <a name="underscores-in-numeric-literals"></a><span data-ttu-id="bc280-192">Traits de soulignement dans les littéraux numériques</span><span class="sxs-lookup"><span data-stu-id="bc280-192">Underscores in Numeric Literals</span></span>

<span data-ttu-id="bc280-193">À partir de F# 4.1, vous pouvez séparer les chiffres par le caractère de soulignement (`_`).</span><span class="sxs-lookup"><span data-stu-id="bc280-193">Starting with F# 4.1, you can separate digits with the underscore character (`_`).</span></span>

```fsharp
let DeadBeef = 0xDEAD_BEEF

let DeadBeefAsBits = 0b1101_1110_1010_1101_1011_1110_1110_1111

let ExampleSSN = 123_456_7890
```

## <a name="see-also"></a><span data-ttu-id="bc280-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc280-194">See also</span></span>

- [<span data-ttu-id="bc280-195">Core.LiteralAttribute, classe</span><span class="sxs-lookup"><span data-stu-id="bc280-195">Core.LiteralAttribute Class</span></span>](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.literalattribute-class-%5bfsharp%5d)
