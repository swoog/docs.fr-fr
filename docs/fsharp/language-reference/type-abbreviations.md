---
title: Abréviations de types (F#)
description: 'Découvrez les abréviations de type F # pour donner un nom plus significatif à un type afin de faciliter la lecture du code.'
ms.date: 05/16/2016
ms.openlocfilehash: 259cd6c84e22fc7c98e08255d3e0ded5b87af352
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45678384"
---
# <a name="type-abbreviations"></a><span data-ttu-id="7acf5-103">Abréviations de types</span><span class="sxs-lookup"><span data-stu-id="7acf5-103">Type Abbreviations</span></span>

<span data-ttu-id="7acf5-104">Un *abréviation de type* est un alias ou un autre nom pour un type.</span><span class="sxs-lookup"><span data-stu-id="7acf5-104">A *type abbreviation* is an alias or alternate name for a type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7acf5-105">Syntax</span></span>

```fsharp
type [accessibility-modifier] type-abbreviation = type-name
```

## <a name="remarks"></a><span data-ttu-id="7acf5-106">Notes</span><span class="sxs-lookup"><span data-stu-id="7acf5-106">Remarks</span></span>

<span data-ttu-id="7acf5-107">Vous pouvez utiliser les abréviations de type pour donner un nom plus explicite, à un type afin de faciliter la lecture du code.</span><span class="sxs-lookup"><span data-stu-id="7acf5-107">You can use type abbreviations to give a type a more meaningful name, in order to make code easier to read.</span></span> <span data-ttu-id="7acf5-108">Vous pouvez également les utiliser pour créer un nom facile à utiliser pour un type fastidieux à écrire. En outre, vous pouvez utiliser les abréviations de type pour le rendre plus facile de modifier un type sous-jacent sans modifier tout le code qui utilise le type.</span><span class="sxs-lookup"><span data-stu-id="7acf5-108">You can also use them to create an easy to use name for a type that is otherwise cumbersome to write out. Additionally, you can use type abbreviations to make it easier to change an underlying type without changing all the code that uses the type.</span></span> <span data-ttu-id="7acf5-109">Voici une abréviation de type simple.</span><span class="sxs-lookup"><span data-stu-id="7acf5-109">The following is a simple type abbreviation.</span></span>

<span data-ttu-id="7acf5-110">Accessibilité des abréviations de types valeur par défaut est `public`.</span><span class="sxs-lookup"><span data-stu-id="7acf5-110">Accessibility of type abbreviations defaults to `public`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

<span data-ttu-id="7acf5-111">Abréviations de types peuvent inclure des paramètres génériques, comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7acf5-111">Type abbreviations can include generic parameters, as in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

<span data-ttu-id="7acf5-112">Dans le code précédent, `Transform` est une abréviation de type qui représente une fonction qui accepte un argument unique de n’importe quel type et qui retourne une valeur unique du même type.</span><span class="sxs-lookup"><span data-stu-id="7acf5-112">In the previous code, `Transform` is a type abbreviation that represents a function that takes a single argument of any type and that returns a single value of that same type.</span></span>

<span data-ttu-id="7acf5-113">Abréviations de types ne sont pas conservées dans le code MSIL .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7acf5-113">Type abbreviations are not preserved in the .NET Framework MSIL code.</span></span> <span data-ttu-id="7acf5-114">Par conséquent, lorsque vous utilisez un assembly F # à partir d’un autre langage .NET Framework, vous devez utiliser le nom de type sous-jacent pour une abréviation de type.</span><span class="sxs-lookup"><span data-stu-id="7acf5-114">Therefore, when you use an F# assembly from another .NET Framework language, you must use the underlying type name for a type abbreviation.</span></span>

<span data-ttu-id="7acf5-115">Abréviations de type peuvent également servir sur des unités de mesure.</span><span class="sxs-lookup"><span data-stu-id="7acf5-115">Type abbreviations can also be used on units of measure.</span></span> <span data-ttu-id="7acf5-116">Pour plus d’informations, consultez [unités](units-of-measure.md).</span><span class="sxs-lookup"><span data-stu-id="7acf5-116">For more information, see [Units of Measure](units-of-measure.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7acf5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7acf5-117">See also</span></span>

- [<span data-ttu-id="7acf5-118">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="7acf5-118">F# Language Reference</span></span>](index.md)
