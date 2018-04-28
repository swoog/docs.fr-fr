---
title: Opérateurs au niveau du bit (F#)
description: 'Obtenir des informations sur les opérateurs de bits qui sont disponibles dans le langage de programmation F #.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 4d5abff564a5d1dcbe52b99edf431ca10e442061
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="bitwise-operators"></a><span data-ttu-id="160fe-103">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="160fe-103">Bitwise Operators</span></span>

<span data-ttu-id="160fe-104">Cette rubrique décrit les opérateurs de bits qui sont disponibles dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="160fe-104">This topic describes bitwise operators that are available in the F# language.</span></span>

## <a name="summary-of-bitwise-operators"></a><span data-ttu-id="160fe-105">Résumé des opérateurs de bits</span><span class="sxs-lookup"><span data-stu-id="160fe-105">Summary of Bitwise Operators</span></span>
<span data-ttu-id="160fe-106">Le tableau suivant décrit les opérateurs au niveau du bit qui sont pris en charge pour les types intégraux unboxed dans le langage F #.</span><span class="sxs-lookup"><span data-stu-id="160fe-106">The following table describes the bitwise operators that are supported for unboxed integral types in the F# language.</span></span>

|<span data-ttu-id="160fe-107">Opérateur</span><span class="sxs-lookup"><span data-stu-id="160fe-107">Operator</span></span>|<span data-ttu-id="160fe-108">Notes</span><span class="sxs-lookup"><span data-stu-id="160fe-108">Notes</span></span>|
|--------|-----|
|`&&&`|<span data-ttu-id="160fe-109">Opérateur de bits AND.</span><span class="sxs-lookup"><span data-stu-id="160fe-109">Bitwise AND operator.</span></span> <span data-ttu-id="160fe-110">Dans le résultat ont la valeur 1 si et seulement si les bits correspondants dans les deux opérandes source sont 1.</span><span class="sxs-lookup"><span data-stu-id="160fe-110">Bits in the result have the value 1 if and only if the corresponding bits in both source operands are 1.</span></span>|
|<code>&#124;&#124;&#124;</code>|<span data-ttu-id="160fe-111">Opérateur de bits OR.</span><span class="sxs-lookup"><span data-stu-id="160fe-111">Bitwise OR operator.</span></span> <span data-ttu-id="160fe-112">Dans le résultat ont la valeur 1 si des bits correspondants dans la source d’opérandes sont de 1.</span><span class="sxs-lookup"><span data-stu-id="160fe-112">Bits in the result have the value 1 if either of the corresponding bits in the source operands are 1.</span></span>|
|`^^^`|<span data-ttu-id="160fe-113">Au niveau du bit opérateur OR exclusif.</span><span class="sxs-lookup"><span data-stu-id="160fe-113">Bitwise exclusive OR operator.</span></span> <span data-ttu-id="160fe-114">Dans le résultat ont la valeur 1 si et seulement si les bits dans les opérandes source ont des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="160fe-114">Bits in the result have the value 1 if and only if bits in the source operands have unequal values.</span></span>|
|`~~~`|<span data-ttu-id="160fe-115">Opérateur de négation au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="160fe-115">Bitwise negation operator.</span></span> <span data-ttu-id="160fe-116">Ceci est un opérateur unaire et produit un résultat dans lequel tous les bits 0 dans l’opérande source sont convertis en bits 1 et tous les bits 1 sont convertis en bits 0.</span><span class="sxs-lookup"><span data-stu-id="160fe-116">This is a unary operator and produces a result in which all 0 bits in the source operand are converted to 1 bits and all 1 bits are converted to 0 bits.</span></span>|
|`<<<`|<span data-ttu-id="160fe-117">Au niveau du bit opérateur de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="160fe-117">Bitwise left-shift operator.</span></span> <span data-ttu-id="160fe-118">Le résultat est le premier opérande avec bits décalée vers la gauche du nombre de bits dans le second opérande.</span><span class="sxs-lookup"><span data-stu-id="160fe-118">The result is the first operand with bits shifted left by the number of bits in the second operand.</span></span> <span data-ttu-id="160fe-119">Les bits décalés à la position la plus significative n’a pas lieu dans la position la moins significative.</span><span class="sxs-lookup"><span data-stu-id="160fe-119">Bits shifted off the most significant position are not rotated into the least significant position.</span></span> <span data-ttu-id="160fe-120">Les bits les moins significatifs sont complétées avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="160fe-120">The least significant bits are padded with zeros.</span></span> <span data-ttu-id="160fe-121">Le type du deuxième argument est `int32`.</span><span class="sxs-lookup"><span data-stu-id="160fe-121">The type of the second argument is `int32`.</span></span>|
|`>>>`|<span data-ttu-id="160fe-122">Au niveau du bit opérateur de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="160fe-122">Bitwise right-shift operator.</span></span> <span data-ttu-id="160fe-123">Le résultat est le premier opérande avec bits décalée vers la droite du nombre de bits dans le second opérande.</span><span class="sxs-lookup"><span data-stu-id="160fe-123">The result is the first operand with bits shifted right by the number of bits in the second operand.</span></span> <span data-ttu-id="160fe-124">Les bits décalés à la position la moins significative n’a pas lieu vers la position la plus significative.</span><span class="sxs-lookup"><span data-stu-id="160fe-124">Bits shifted off the least significant position are not rotated into the most significant position.</span></span> <span data-ttu-id="160fe-125">Pour les types non signés, les bits les plus significatifs sont remplis avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="160fe-125">For unsigned types, the most significant bits are padded with zeros.</span></span> <span data-ttu-id="160fe-126">Pour les types signés, les bits les plus significatifs sont complétées par d’autres.</span><span class="sxs-lookup"><span data-stu-id="160fe-126">For signed types, the most significant bits are padded with ones.</span></span> <span data-ttu-id="160fe-127">Le type du deuxième argument est `int32`.</span><span class="sxs-lookup"><span data-stu-id="160fe-127">The type of the second argument is `int32`.</span></span>|

<span data-ttu-id="160fe-128">Les types suivants peuvent être utilisés avec des opérateurs au niveau du bit : `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`, `uint32`, `int64`, `uint64`, `nativeint`, et `unativeint`.</span><span class="sxs-lookup"><span data-stu-id="160fe-128">The following types can be used with bitwise operators: `byte`, `sbyte`, `int16`, `uint16`, `int32 (int)`, `uint32`, `int64`, `uint64`, `nativeint`, and `unativeint`.</span></span>

## <a name="see-also"></a><span data-ttu-id="160fe-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="160fe-129">See Also</span></span>
[<span data-ttu-id="160fe-130">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="160fe-130">Symbol and Operator Reference</span></span>](index.md)

[<span data-ttu-id="160fe-131">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="160fe-131">Arithmetic Operators</span></span>](arithmetic-operators.md)

[<span data-ttu-id="160fe-132">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="160fe-132">Boolean Operators</span></span>](boolean-operators.md)

