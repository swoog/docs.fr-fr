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
# <a name="literals"></a><span data-ttu-id="d55b1-103">Littéraux</span><span class="sxs-lookup"><span data-stu-id="d55b1-103">Literals</span></span>

> [!NOTE]
<span data-ttu-id="d55b1-104">Les liens de référence des API dans cet article vous dirigera vers MSDN (pour l’instant).</span><span class="sxs-lookup"><span data-stu-id="d55b1-104">The API reference links in this article will take you to MSDN (for now).</span></span>

<span data-ttu-id="d55b1-105">Cette rubrique fournit une table qui montre comment spécifier le type d’un littéral en F#.</span><span class="sxs-lookup"><span data-stu-id="d55b1-105">This topic provides a table that shows how to specify the type of a literal in F#.</span></span>

## <a name="literal-types"></a><span data-ttu-id="d55b1-106">Types de littéral</span><span class="sxs-lookup"><span data-stu-id="d55b1-106">Literal Types</span></span>

<span data-ttu-id="d55b1-107">Le tableau suivant présente les types de littéraux en F#.</span><span class="sxs-lookup"><span data-stu-id="d55b1-107">The following table shows the literal types in F#.</span></span> <span data-ttu-id="d55b1-108">Les caractères qui représentent des chiffres en notation hexadécimale ne sont pas la casse ; les caractères qui identifient le type respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="d55b1-108">Characters that represent digits in hexadecimal notation are not case-sensitive; characters that identify the type are case-sensitive.</span></span>

|<span data-ttu-id="d55b1-109">Type</span><span class="sxs-lookup"><span data-stu-id="d55b1-109">Type</span></span>|<span data-ttu-id="d55b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="d55b1-110">Description</span></span>|<span data-ttu-id="d55b1-111">Suffixe ou préfixe</span><span class="sxs-lookup"><span data-stu-id="d55b1-111">Suffix or prefix</span></span>|<span data-ttu-id="d55b1-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="d55b1-112">Examples</span></span>|
|----|-----------|----------------|--------|
|<span data-ttu-id="d55b1-113">sbyte</span><span class="sxs-lookup"><span data-stu-id="d55b1-113">sbyte</span></span>|<span data-ttu-id="d55b1-114">entier signé 8 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-114">signed 8-bit integer</span></span>|<span data-ttu-id="d55b1-115">o</span><span class="sxs-lookup"><span data-stu-id="d55b1-115">y</span></span>|`86y`<br /><br />`0b00000101y`|
|<span data-ttu-id="d55b1-116">byte</span><span class="sxs-lookup"><span data-stu-id="d55b1-116">byte</span></span>|<span data-ttu-id="d55b1-117">nombre de naturel 8 bits non signé</span><span class="sxs-lookup"><span data-stu-id="d55b1-117">unsigned 8-bit natural number</span></span>|<span data-ttu-id="d55b1-118">UY</span><span class="sxs-lookup"><span data-stu-id="d55b1-118">uy</span></span>|`86uy`<br /><br />`0b00000101uy`|
|<span data-ttu-id="d55b1-119">int16</span><span class="sxs-lookup"><span data-stu-id="d55b1-119">int16</span></span>|<span data-ttu-id="d55b1-120">entier signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-120">signed 16-bit integer</span></span>|<span data-ttu-id="d55b1-121">s</span><span class="sxs-lookup"><span data-stu-id="d55b1-121">s</span></span>|`86s`|
|<span data-ttu-id="d55b1-122">uint16</span><span class="sxs-lookup"><span data-stu-id="d55b1-122">uint16</span></span>|<span data-ttu-id="d55b1-123">nombre de naturel non signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-123">unsigned 16-bit natural number</span></span>|<span data-ttu-id="d55b1-124">us</span><span class="sxs-lookup"><span data-stu-id="d55b1-124">us</span></span>|`86us`|
|<span data-ttu-id="d55b1-125">int</span><span class="sxs-lookup"><span data-stu-id="d55b1-125">int</span></span><br /><br /><span data-ttu-id="d55b1-126">int32</span><span class="sxs-lookup"><span data-stu-id="d55b1-126">int32</span></span>|<span data-ttu-id="d55b1-127">entier signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-127">signed 32-bit integer</span></span>|<span data-ttu-id="d55b1-128">« l » ou none</span><span class="sxs-lookup"><span data-stu-id="d55b1-128">l or none</span></span>|`86`<br /><br />`86l`|
|<span data-ttu-id="d55b1-129">uint</span><span class="sxs-lookup"><span data-stu-id="d55b1-129">uint</span></span><br /><br /><span data-ttu-id="d55b1-130">uint32</span><span class="sxs-lookup"><span data-stu-id="d55b1-130">uint32</span></span>|<span data-ttu-id="d55b1-131">nombre de naturel non signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-131">unsigned 32-bit natural number</span></span>|<span data-ttu-id="d55b1-132">u ou ul</span><span class="sxs-lookup"><span data-stu-id="d55b1-132">u or ul</span></span>|`86u`<br /><br />`86ul`|
|<span data-ttu-id="d55b1-133">unativeint</span><span class="sxs-lookup"><span data-stu-id="d55b1-133">unativeint</span></span>|<span data-ttu-id="d55b1-134">pointeur natif sous forme de nombre naturel non signé</span><span class="sxs-lookup"><span data-stu-id="d55b1-134">native pointer as an unsigned natural number</span></span>|<span data-ttu-id="d55b1-135">Annuler</span><span class="sxs-lookup"><span data-stu-id="d55b1-135">un</span></span>|`0x00002D3Fun`|
|<span data-ttu-id="d55b1-136">int64</span><span class="sxs-lookup"><span data-stu-id="d55b1-136">int64</span></span>|<span data-ttu-id="d55b1-137">entier signé 64 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-137">signed 64-bit integer</span></span>|<span data-ttu-id="d55b1-138">L</span><span class="sxs-lookup"><span data-stu-id="d55b1-138">L</span></span>|`86L`|
|<span data-ttu-id="d55b1-139">uint64</span><span class="sxs-lookup"><span data-stu-id="d55b1-139">uint64</span></span>|<span data-ttu-id="d55b1-140">nombre de naturel non signé 64 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-140">unsigned 64-bit natural number</span></span>|<span data-ttu-id="d55b1-141">UL</span><span class="sxs-lookup"><span data-stu-id="d55b1-141">UL</span></span>|`86UL`|
|<span data-ttu-id="d55b1-142">float32 unique,</span><span class="sxs-lookup"><span data-stu-id="d55b1-142">single, float32</span></span>|<span data-ttu-id="d55b1-143">nombre à virgule flottante 32 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-143">32-bit floating point number</span></span>|<span data-ttu-id="d55b1-144">F ou f</span><span class="sxs-lookup"><span data-stu-id="d55b1-144">F or f</span></span>|<span data-ttu-id="d55b1-145">`4.14F` ou `4.14f`</span><span class="sxs-lookup"><span data-stu-id="d55b1-145">`4.14F` or `4.14f`</span></span>|
|||<span data-ttu-id="d55b1-146">LF</span><span class="sxs-lookup"><span data-stu-id="d55b1-146">lf</span></span>|`0x00000000lf`|
|<span data-ttu-id="d55b1-147">type float ; Double</span><span class="sxs-lookup"><span data-stu-id="d55b1-147">float; double</span></span>|<span data-ttu-id="d55b1-148">nombre à virgule flottante 64 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-148">64-bit floating point number</span></span>|<span data-ttu-id="d55b1-149">none</span><span class="sxs-lookup"><span data-stu-id="d55b1-149">none</span></span>|<span data-ttu-id="d55b1-150">`4.14` ou `2.3E+32` ou `2.3e+32`</span><span class="sxs-lookup"><span data-stu-id="d55b1-150">`4.14` or `2.3E+32` or `2.3e+32`</span></span>|
|||<span data-ttu-id="d55b1-151">LF</span><span class="sxs-lookup"><span data-stu-id="d55b1-151">LF</span></span>|`0x0000000000000000LF`|
|<span data-ttu-id="d55b1-152">bigint</span><span class="sxs-lookup"><span data-stu-id="d55b1-152">bigint</span></span>|<span data-ttu-id="d55b1-153">entier non limité à la représentation 64 bits</span><span class="sxs-lookup"><span data-stu-id="d55b1-153">integer not limited to 64-bit representation</span></span>|<span data-ttu-id="d55b1-154">I</span><span class="sxs-lookup"><span data-stu-id="d55b1-154">I</span></span>|`9999999999999999999999999999I`|
|<span data-ttu-id="d55b1-155">decimal</span><span class="sxs-lookup"><span data-stu-id="d55b1-155">decimal</span></span>|<span data-ttu-id="d55b1-156">nombre fractionnaire représenté sous la forme à virgule fixe ou un nombre rationnel</span><span class="sxs-lookup"><span data-stu-id="d55b1-156">fractional number represented as a fixed point or rational number</span></span>|<span data-ttu-id="d55b1-157">M ou m</span><span class="sxs-lookup"><span data-stu-id="d55b1-157">M or m</span></span>|<span data-ttu-id="d55b1-158">`0.7833M` ou `0.7833m`</span><span class="sxs-lookup"><span data-stu-id="d55b1-158">`0.7833M` or `0.7833m`</span></span>|
|<span data-ttu-id="d55b1-159">Char</span><span class="sxs-lookup"><span data-stu-id="d55b1-159">Char</span></span>|<span data-ttu-id="d55b1-160">caractère Unicode</span><span class="sxs-lookup"><span data-stu-id="d55b1-160">Unicode character</span></span>|<span data-ttu-id="d55b1-161">none</span><span class="sxs-lookup"><span data-stu-id="d55b1-161">none</span></span>|`'a'`|
|<span data-ttu-id="d55b1-162">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d55b1-162">String</span></span>|<span data-ttu-id="d55b1-163">chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="d55b1-163">Unicode string</span></span>|<span data-ttu-id="d55b1-164">none</span><span class="sxs-lookup"><span data-stu-id="d55b1-164">none</span></span>|`"text\n"`<br /><br /><span data-ttu-id="d55b1-165">ou</span><span class="sxs-lookup"><span data-stu-id="d55b1-165">or</span></span><br /><br />`@"c:\filename"`<br /><br /><span data-ttu-id="d55b1-166">ou</span><span class="sxs-lookup"><span data-stu-id="d55b1-166">or</span></span><br /><br />`"""<book title="Paradise Lost">"""`<br /><br /><span data-ttu-id="d55b1-167">ou</span><span class="sxs-lookup"><span data-stu-id="d55b1-167">or</span></span><br /><br />`"string1" + "string2"`<br /><br /><span data-ttu-id="d55b1-168">Voir aussi [chaînes](Strings.md).</span><span class="sxs-lookup"><span data-stu-id="d55b1-168">See also [Strings](Strings.md).</span></span>|
|<span data-ttu-id="d55b1-169">byte</span><span class="sxs-lookup"><span data-stu-id="d55b1-169">byte</span></span>|<span data-ttu-id="d55b1-170">Caractère ASCII</span><span class="sxs-lookup"><span data-stu-id="d55b1-170">ASCII character</span></span>|<span data-ttu-id="d55b1-171">B</span><span class="sxs-lookup"><span data-stu-id="d55b1-171">B</span></span>|`'a'B`|
|<span data-ttu-id="d55b1-172">byte[]</span><span class="sxs-lookup"><span data-stu-id="d55b1-172">byte[]</span></span>|<span data-ttu-id="d55b1-173">Chaîne ASCII</span><span class="sxs-lookup"><span data-stu-id="d55b1-173">ASCII string</span></span>|<span data-ttu-id="d55b1-174">B</span><span class="sxs-lookup"><span data-stu-id="d55b1-174">B</span></span>|`"text"B`|
|<span data-ttu-id="d55b1-175">String ou byte]</span><span class="sxs-lookup"><span data-stu-id="d55b1-175">String or byte[]</span></span>|<span data-ttu-id="d55b1-176">chaîne textuelle</span><span class="sxs-lookup"><span data-stu-id="d55b1-176">verbatim string</span></span>|<span data-ttu-id="d55b1-177">préfixe « @ »</span><span class="sxs-lookup"><span data-stu-id="d55b1-177">@ prefix</span></span>|<span data-ttu-id="d55b1-178">`@"\\server\share"` (Unicode)</span><span class="sxs-lookup"><span data-stu-id="d55b1-178">`@"\\server\share"` (Unicode)</span></span><br /><br /><span data-ttu-id="d55b1-179">`@"\\server\share"B` (ASCII)</span><span class="sxs-lookup"><span data-stu-id="d55b1-179">`@"\\server\share"B` (ASCII)</span></span>|

## <a name="remarks"></a><span data-ttu-id="d55b1-180">Notes</span><span class="sxs-lookup"><span data-stu-id="d55b1-180">Remarks</span></span>

<span data-ttu-id="d55b1-181">Chaînes Unicode peuvent contenir des encodages explicites que vous pouvez spécifier à l’aide de `\u` suivi d’un code hexadécimal 16 bits ou les encodages UTF-32 que vous pouvez spécifier à l’aide de `\U` suivie d’un code hexadécimal 32 bits qui représente un Unicode paire de substitution.</span><span class="sxs-lookup"><span data-stu-id="d55b1-181">Unicode strings can contain explicit encodings that you can specify by using `\u` followed by a 16-bit hexadecimal code or UTF-32 encodings that you can specify by using `\U` followed by a 32-bit hexadecimal code that represents a Unicode surrogate pair.</span></span>

<span data-ttu-id="d55b1-182">Avec F# 3,1, vous pouvez utiliser le `+` vous connecter pour combiner des littéraux de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d55b1-182">As of F# 3.1, you can use the `+` sign to combine string literals.</span></span> <span data-ttu-id="d55b1-183">Vous pouvez également utiliser l’opérateur de bits ou (`|||`) opérateur pour combiner les indicateurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="d55b1-183">You can also use the bitwise or (`|||`) operator to combine enum flags.</span></span> <span data-ttu-id="d55b1-184">Par exemple, le code suivant est autorisé dans F# 3.1 :</span><span class="sxs-lookup"><span data-stu-id="d55b1-184">For example, the following code is legal in F# 3.1:</span></span>

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

<span data-ttu-id="d55b1-185">L’utilisation d’autres opérateurs au niveau du bit n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="d55b1-185">The use of other bitwise operators isn't allowed.</span></span>

## <a name="named-literals"></a><span data-ttu-id="d55b1-186">Littéraux nommés</span><span class="sxs-lookup"><span data-stu-id="d55b1-186">Named Literals</span></span>

<span data-ttu-id="d55b1-187">Les valeurs qui sont destinées à être des constantes peuvent être marquées avec le [littéral](https://msdn.microsoft.com/library/465f36ce-d146-41c0-b425-679c509cd285) attribut.</span><span class="sxs-lookup"><span data-stu-id="d55b1-187">Values that are intended to be constants can be marked with the [Literal](https://msdn.microsoft.com/library/465f36ce-d146-41c0-b425-679c509cd285) attribute.</span></span> <span data-ttu-id="d55b1-188">Cet attribut a pour effet de provoquer une valeur doit être compilé en tant que constante.</span><span class="sxs-lookup"><span data-stu-id="d55b1-188">This attribute has the effect of causing a value to be compiled as a constant.</span></span>

<span data-ttu-id="d55b1-189">Dans les expressions de critères spéciaux, les identificateurs qui commencent par les caractères minuscules sont toujours traités en tant que variables à lier, plutôt que comme des littéraux, par conséquent, vous devez généralement utiliser majuscules lorsque vous définissez des littéraux.</span><span class="sxs-lookup"><span data-stu-id="d55b1-189">In pattern matching expressions, identifiers that begin with lowercase characters are always treated as variables to be bound, rather than as literals, so you should generally use initial capitals when you define literals.</span></span>

## <a name="integers-in-other-bases"></a><span data-ttu-id="d55b1-190">Nombres entiers dans d’autres Bases</span><span class="sxs-lookup"><span data-stu-id="d55b1-190">Integers In Other Bases</span></span>

<span data-ttu-id="d55b1-191">Entiers signés de 32 bits peuvent également être spécifiés dans hexadécimal, octal ou binaire à l’aide un `0x`, `0o` ou `0b` respectivement de préfixe.</span><span class="sxs-lookup"><span data-stu-id="d55b1-191">Signed 32-bit integers can also be specified in hexadecimal, octal, or binary using a `0x`, `0o` or `0b` prefix respectively.</span></span>

```fsharp
let Numbers = (0x9F, 0o77, 0b1010)
// Result: Numbers : int * int * int = (159, 63, 10)
```

## <a name="underscores-in-numeric-literals"></a><span data-ttu-id="d55b1-192">Traits de soulignement dans les littéraux numériques</span><span class="sxs-lookup"><span data-stu-id="d55b1-192">Underscores in Numeric Literals</span></span>

<span data-ttu-id="d55b1-193">À partir de F# 4.1, vous pouvez séparer les chiffres par le caractère de soulignement (`_`).</span><span class="sxs-lookup"><span data-stu-id="d55b1-193">Starting with F# 4.1, you can separate digits with the underscore character (`_`).</span></span>

```fsharp
let DeadBeef = 0xDEAD_BEEF

let DeadBeefAsBits = 0b1101_1110_1010_1101_1011_1110_1110_1111

let ExampleSSN = 123_456_7890
```

## <a name="see-also"></a><span data-ttu-id="d55b1-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d55b1-194">See also</span></span>

- [<span data-ttu-id="d55b1-195">Core.LiteralAttribute, classe</span><span class="sxs-lookup"><span data-stu-id="d55b1-195">Core.LiteralAttribute Class</span></span>](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.literalattribute-class-%5bfsharp%5d)
