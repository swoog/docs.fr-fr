---
title: Types de base (F#)
description: Découvrir les types de base fondamentales qui sont utilisés dans le F# langage.
ms.date: 07/09/2018
ms.openlocfilehash: a8a1154a211d8c87571b47cb41cb091096569472
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53145122"
---
# <a name="basic-types"></a><span data-ttu-id="7b621-103">Types de base</span><span class="sxs-lookup"><span data-stu-id="7b621-103">Basic types</span></span>

<span data-ttu-id="7b621-104">Cette rubrique répertorie les types de base qui sont définies dans le F# langage.</span><span class="sxs-lookup"><span data-stu-id="7b621-104">This topic lists the basic types that are defined in the F# language.</span></span> <span data-ttu-id="7b621-105">Ces types sont le plus fondamental dans F#, constituant la base de presque chaque F# programme.</span><span class="sxs-lookup"><span data-stu-id="7b621-105">These types are the most fundamental in F#, forming the basis of nearly every F# program.</span></span> <span data-ttu-id="7b621-106">Ils représentent un sur-ensemble des types primitifs .NET.</span><span class="sxs-lookup"><span data-stu-id="7b621-106">They are a superset of .NET primitive types.</span></span>

|<span data-ttu-id="7b621-107">Type</span><span class="sxs-lookup"><span data-stu-id="7b621-107">Type</span></span>|<span data-ttu-id="7b621-108">Type .NET</span><span class="sxs-lookup"><span data-stu-id="7b621-108">.NET type</span></span>|<span data-ttu-id="7b621-109">Description</span><span class="sxs-lookup"><span data-stu-id="7b621-109">Description</span></span>|
|----|---------|-----------|
|`bool`|<xref:System.Boolean>|<span data-ttu-id="7b621-110">Les valeurs possibles sont `true` et `false`.</span><span class="sxs-lookup"><span data-stu-id="7b621-110">Possible values are `true` and `false`.</span></span>|
|`byte`|<xref:System.Byte>|<span data-ttu-id="7b621-111">Valeurs comprises entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="7b621-111">Values from 0 to 255.</span></span>|
|`sbyte`|<xref:System.SByte>|<span data-ttu-id="7b621-112">Valeurs comprises entre -128 et 127.</span><span class="sxs-lookup"><span data-stu-id="7b621-112">Values from -128 to 127.</span></span>|
|`int16`|<xref:System.Int16>|<span data-ttu-id="7b621-113">Valeurs comprise entre -32768 et 32767.</span><span class="sxs-lookup"><span data-stu-id="7b621-113">Values from -32768 to 32767.</span></span>|
|`uint16`|<xref:System.UInt16>|<span data-ttu-id="7b621-114">Valeurs comprises entre 0 et 65535.</span><span class="sxs-lookup"><span data-stu-id="7b621-114">Values from 0 to 65535.</span></span>|
|`int`|<xref:System.Int32>|<span data-ttu-id="7b621-115">Valeurs d’allant de -2,147,483,648 à 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="7b621-115">Values from -2,147,483,648 to 2,147,483,647.</span></span>|
|`uint32`|<xref:System.UInt32>|<span data-ttu-id="7b621-116">Valeurs de 0 à 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="7b621-116">Values from 0 to 4,294,967,295.</span></span>|
|`int64`|<xref:System.Int64>|<span data-ttu-id="7b621-117">Valeurs de -9,223,372,036,854,775,808 à 9,223,372,036,854,775,807.</span><span class="sxs-lookup"><span data-stu-id="7b621-117">Values from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.</span></span>|
|`uint64`|<xref:System.UInt64>|<span data-ttu-id="7b621-118">Valeurs comprises entre 0 et 18,446,744,073,709,551,615.</span><span class="sxs-lookup"><span data-stu-id="7b621-118">Values from 0 to 18,446,744,073,709,551,615.</span></span>|
|`nativeint`|<xref:System.IntPtr>|<span data-ttu-id="7b621-119">Un pointeur natif comme un entier signé.</span><span class="sxs-lookup"><span data-stu-id="7b621-119">A native pointer as a signed integer.</span></span>|
|`unativeint`|<xref:System.UIntPtr>|<span data-ttu-id="7b621-120">Un pointeur natif sous forme d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="7b621-120">A native pointer as an unsigned integer.</span></span>|
|`char`|<xref:System.Char>|<span data-ttu-id="7b621-121">Valeurs de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="7b621-121">Unicode character values.</span></span>|
|`string`|<xref:System.String>|<span data-ttu-id="7b621-122">Texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="7b621-122">Unicode text.</span></span>|
|`decimal`|<xref:System.Decimal>|<span data-ttu-id="7b621-123">Type de données qui comporte au moins 28 chiffres significatifs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="7b621-123">A floating point data type that has at least 28 significant digits.</span></span>|
|`unit`|<span data-ttu-id="7b621-124">non applicable</span><span class="sxs-lookup"><span data-stu-id="7b621-124">not applicable</span></span>|<span data-ttu-id="7b621-125">Indique l’absence d’une valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="7b621-125">Indicates the absence of an actual value.</span></span> <span data-ttu-id="7b621-126">Le type n'a qu’une seule valeur formelle, qui est indiquée `()`.</span><span class="sxs-lookup"><span data-stu-id="7b621-126">The type has only one formal value, which is denoted `()`.</span></span> <span data-ttu-id="7b621-127">La valeur unitaire, `()`, est souvent utilisé comme espace réservé où une valeur est requise, mais aucune valeur réelle n’est disponible ou a de sens.</span><span class="sxs-lookup"><span data-stu-id="7b621-127">The unit value, `()`, is often used as a placeholder where a value is needed but no real value is available or makes sense.</span></span>|
|`void`|<xref:System.Void>|<span data-ttu-id="7b621-128">Indique le type ou la valeur.</span><span class="sxs-lookup"><span data-stu-id="7b621-128">Indicates no type or value.</span></span>|
|<span data-ttu-id="7b621-129">`float32`, `single`</span><span class="sxs-lookup"><span data-stu-id="7b621-129">`float32`, `single`</span></span>|<xref:System.Single>|<span data-ttu-id="7b621-130">Type à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7b621-130">A 32-bit floating point type.</span></span>|
|<span data-ttu-id="7b621-131">`float`, `double`</span><span class="sxs-lookup"><span data-stu-id="7b621-131">`float`, `double`</span></span>|<xref:System.Double>|<span data-ttu-id="7b621-132">Type à virgule flottante 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b621-132">A 64-bit floating point type.</span></span>|

> [!NOTE]
> <span data-ttu-id="7b621-133">Vous pouvez effectuer des calculs avec des entiers trop grandes pour le type d’entier 64 bits à l’aide de la [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) type.</span><span class="sxs-lookup"><span data-stu-id="7b621-133">You can perform computations with integers too big for the 64-bit integer type by using the [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) type.</span></span> <span data-ttu-id="7b621-134">`bigint` n’est pas considéré comme un type de base ; Il est l’abréviation de `System.Numerics.BigInteger`.</span><span class="sxs-lookup"><span data-stu-id="7b621-134">`bigint` is not considered a basic type; it is an abbreviation for `System.Numerics.BigInteger`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b621-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b621-135">See also</span></span>

- [<span data-ttu-id="7b621-136">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="7b621-136">F# Language Reference</span></span>](index.md)
