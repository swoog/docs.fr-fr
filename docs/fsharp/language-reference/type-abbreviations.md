---
title: Abréviations de types (F#)
description: 'Découvrez les abréviations de type F # pour donner un nom plus significatif à un type afin de rendre le code plus facile à lire.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: bf17ee9795947fdc11fe958f09d52f5730b95bf8
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="type-abbreviations"></a><span data-ttu-id="bd827-103">Abréviations de types</span><span class="sxs-lookup"><span data-stu-id="bd827-103">Type Abbreviations</span></span>

<span data-ttu-id="bd827-104">A *abréviation de type* est un alias ou un autre nom pour un type.</span><span class="sxs-lookup"><span data-stu-id="bd827-104">A *type abbreviation* is an alias or alternate name for a type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd827-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd827-105">Syntax</span></span>

```fsharp
type type-abbreviation = type-name
```

## <a name="remarks"></a><span data-ttu-id="bd827-106">Notes</span><span class="sxs-lookup"><span data-stu-id="bd827-106">Remarks</span></span>
<span data-ttu-id="bd827-107">Vous pouvez utiliser les abréviations de type pour donner un nom plus significatif, à un type afin de rendre le code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="bd827-107">You can use type abbreviations to give a type a more meaningful name, in order to make code easier to read.</span></span> <span data-ttu-id="bd827-108">Vous pouvez également les utiliser pour créer un nom facile à utiliser pour un type fastidieux à écrire. En outre, vous pouvez utiliser les abréviations de type pour le rendre plus facile de modifier un type sous-jacent sans modifier tout code qui utilise le type.</span><span class="sxs-lookup"><span data-stu-id="bd827-108">You can also use them to create an easy to use name for a type that is otherwise cumbersome to write out. Additionally, you can use type abbreviations to make it easier to change an underlying type without changing all the code that uses the type.</span></span> <span data-ttu-id="bd827-109">Voici une abréviation de type simple.</span><span class="sxs-lookup"><span data-stu-id="bd827-109">The following is a simple type abbreviation.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

<span data-ttu-id="bd827-110">Les abréviations de type peuvent inclure des paramètres génériques, comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="bd827-110">Type abbreviations can include generic parameters, as in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

<span data-ttu-id="bd827-111">Dans le code précédent, `Transform` est une abréviation de type représentant une fonction qui accepte un argument unique de n’importe quel type et qui retourne une valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="bd827-111">In the previous code, `Transform` is a type abbreviation that represents a function that takes a single argument of any type and that returns a single value of that same type.</span></span>

<span data-ttu-id="bd827-112">Les abréviations de type ne sont pas conservées dans le code MSIL .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bd827-112">Type abbreviations are not preserved in the .NET Framework MSIL code.</span></span> <span data-ttu-id="bd827-113">Par conséquent, lorsque vous utilisez un assembly F # à partir d’un autre langage .NET Framework, vous devez utiliser le nom du type sous-jacent pour une abréviation de type.</span><span class="sxs-lookup"><span data-stu-id="bd827-113">Therefore, when you use an F# assembly from another .NET Framework language, you must use the underlying type name for a type abbreviation.</span></span>

<span data-ttu-id="bd827-114">Les abréviations de type peuvent également servir dans les unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="bd827-114">Type abbreviations can also be used on units of measure.</span></span> <span data-ttu-id="bd827-115">Pour plus d’informations, consultez [unités](units-of-measure.md).</span><span class="sxs-lookup"><span data-stu-id="bd827-115">For more information, see [Units of Measure](units-of-measure.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="bd827-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd827-116">See Also</span></span>
[<span data-ttu-id="bd827-117">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="bd827-117">F# Language Reference</span></span>](index.md)

