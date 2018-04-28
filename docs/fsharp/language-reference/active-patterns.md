---
title: Modèles actifs (F#)
description: 'Découvrez comment utiliser les modèles actifs pour définir des partitions nommées qui subdivisent les données d’entrée dans le langage de programmation F #.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 66e1e39c4822ec7262642d301ceb1deea17fcb8c
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="active-patterns"></a><span data-ttu-id="43684-103">Modèles actifs</span><span class="sxs-lookup"><span data-stu-id="43684-103">Active Patterns</span></span>

<span data-ttu-id="43684-104">*Modèles actifs* vous permettent de définir des partitions nommées qui subdivisent les données d’entrée, afin que vous puissiez utiliser ces noms dans un modèle d’expression de critères, comme vous le feriez pour une union discriminée.</span><span class="sxs-lookup"><span data-stu-id="43684-104">*Active patterns* enable you to define named partitions that subdivide input data, so that you can use these names in a pattern matching expression just as you would for a discriminated union.</span></span> <span data-ttu-id="43684-105">Vous pouvez utiliser des modèles actifs pour décomposer des données de façon personnalisée pour chaque partition.</span><span class="sxs-lookup"><span data-stu-id="43684-105">You can use active patterns to decompose data in a customized manner for each partition.</span></span>


## <a name="syntax"></a><span data-ttu-id="43684-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43684-106">Syntax</span></span>

```fsharp
// Complete active pattern definition.
let (|identifer1|identifier2|...|) [ arguments ] = expression
// Partial active pattern definition.
let (|identifier|_|) [ arguments ] = expression
```

## <a name="remarks"></a><span data-ttu-id="43684-107">Notes</span><span class="sxs-lookup"><span data-stu-id="43684-107">Remarks</span></span>
<span data-ttu-id="43684-108">Dans la syntaxe précédente, les identificateurs sont des noms pour les partitions des données d’entrée qui sont représentées par *arguments*, ou, en d’autres termes, les noms pour les sous-ensembles de l’ensemble de toutes les valeurs des arguments.</span><span class="sxs-lookup"><span data-stu-id="43684-108">In the previous syntax, the identifiers are names for partitions of the input data that is represented by *arguments*, or, in other words, names for subsets of the set of all values of the arguments.</span></span> <span data-ttu-id="43684-109">Il peut exister jusqu'à sept partitions dans une définition de modèle actif.</span><span class="sxs-lookup"><span data-stu-id="43684-109">There can be up to seven partitions in an active pattern definition.</span></span> <span data-ttu-id="43684-110">Le *expression* décrit le mode de décomposition des données.</span><span class="sxs-lookup"><span data-stu-id="43684-110">The *expression* describes the form into which to decompose the data.</span></span> <span data-ttu-id="43684-111">Vous pouvez utiliser une définition de modèle actif pour définir les règles pour déterminer la partition nommée les valeurs fournies comme arguments appartiennent.</span><span class="sxs-lookup"><span data-stu-id="43684-111">You can use an active pattern definition to define the rules for determining which of the named partitions the values given as arguments belong to.</span></span> <span data-ttu-id="43684-112">Le (| et |) les symboles sont appelés *« banana clips »* et la fonction créée par ce type de liaison let est appelée un *module de reconnaissance actif*.</span><span class="sxs-lookup"><span data-stu-id="43684-112">The (| and |) symbols are referred to as *banana clips* and the function created by this type of let binding is called an *active recognizer*.</span></span>

<span data-ttu-id="43684-113">Par exemple, envisagez le modèle actif suivant avec un argument.</span><span class="sxs-lookup"><span data-stu-id="43684-113">As an example, consider the following active pattern with an argument.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5001.fs)]

<span data-ttu-id="43684-114">Vous pouvez utiliser le modèle actif dans un modèle de correspondance d’expression, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="43684-114">You can use the active pattern in a pattern matching expression, as in the following example.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5002.fs)]

<span data-ttu-id="43684-115">La sortie de ce programme est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-115">The output of this program is as follows:</span></span>

```
7 is odd
11 is odd
32 is even
```

<span data-ttu-id="43684-116">Une autre utilisation de modèles actifs consiste à décomposer les types de données de plusieurs façons, par exemple lorsque les mêmes données sous-jacentes ont différentes représentations possible.</span><span class="sxs-lookup"><span data-stu-id="43684-116">Another use of active patterns is to decompose data types in multiple ways, such as when the same underlying data has various possible representations.</span></span> <span data-ttu-id="43684-117">Par exemple, un `Color` objet peut être décomposé en représentation RVB ou en représentation TSL.</span><span class="sxs-lookup"><span data-stu-id="43684-117">For example, a `Color` object could be decomposed into an RGB representation or an HSB representation.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5003.fs)]

<span data-ttu-id="43684-118">La sortie du programme ci-dessus est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-118">The output of the above program is as follows:</span></span>

```
Red
 Red: 255 Green: 0 Blue: 0
 Hue: 360.000000 Saturation: 1.000000 Brightness: 0.500000
Black
 Red: 0 Green: 0 Blue: 0
 Hue: 0.000000 Saturation: 0.000000 Brightness: 0.000000
White
 Red: 255 Green: 255 Blue: 255
 Hue: 0.000000 Saturation: 0.000000 Brightness: 1.000000
Gray
 Red: 128 Green: 128 Blue: 128
 Hue: 0.000000 Saturation: 0.000000 Brightness: 0.501961
BlanchedAlmond
 Red: 255 Green: 235 Blue: 205
 Hue: 36.000000 Saturation: 1.000000 Brightness: 0.901961
```

<span data-ttu-id="43684-119">Conjointement, ces deux façons d’utiliser les modèles actifs vous permettent de partition et décomposent les données en une forme adéquate et effectuent les calculs appropriés sur les données appropriées sous la forme la plus pratique pour le calcul.</span><span class="sxs-lookup"><span data-stu-id="43684-119">In combination, these two ways of using active patterns enable you to partition and decompose data into just the appropriate form and perform the appropriate computations on the appropriate data in the form most convenient for the computation.</span></span>

<span data-ttu-id="43684-120">Les expressions de critères spéciaux résultant activer les données à écrire facilement lisibles, ce qui simplifie considérablement le branchement potentiellement complexe et le code d’analyse de données.</span><span class="sxs-lookup"><span data-stu-id="43684-120">The resulting pattern matching expressions enable data to be written in a convenient way that is very readable, greatly simplifying potentially complex branching and data analysis code.</span></span>


## <a name="partial-active-patterns"></a><span data-ttu-id="43684-121">Modèles actifs partiels</span><span class="sxs-lookup"><span data-stu-id="43684-121">Partial Active Patterns</span></span>
<span data-ttu-id="43684-122">Dans certains cas, vous devez uniquement une partie de l’espace d’entrée de partition.</span><span class="sxs-lookup"><span data-stu-id="43684-122">Sometimes, you need to partition only part of the input space.</span></span> <span data-ttu-id="43684-123">Dans ce cas, vous écrivez un jeu de modèles partiels, chacun qui correspondent à des entrées mais pas à d’autres entrées.</span><span class="sxs-lookup"><span data-stu-id="43684-123">In that case, you write a set of partial patterns each of which match some inputs but fail to match other inputs.</span></span> <span data-ttu-id="43684-124">Modèles actifs qui ne produisent pas toujours de valeur sont appelés *modèles actifs partiels*; ils ont une valeur de retour est un type d’option.</span><span class="sxs-lookup"><span data-stu-id="43684-124">Active patterns that do not always produce a value are called *partial active patterns*; they have a return value that is an option type.</span></span> <span data-ttu-id="43684-125">Pour définir un modèle actif partiel, vous utilisez un caractère générique (_) à la fin de la liste des modèles à l’intérieur des « banana clips ».</span><span class="sxs-lookup"><span data-stu-id="43684-125">To define a partial active pattern, you use a wildcard character (_) at the end of the list of patterns inside the banana clips.</span></span> <span data-ttu-id="43684-126">Le code suivant illustre l’utilisation d’un modèle actif partiel.</span><span class="sxs-lookup"><span data-stu-id="43684-126">The following code illustrates the use of a partial active pattern.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5004.fs)]

<span data-ttu-id="43684-127">La sortie de l’exemple précédent est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-127">The output of the previous example is as follows:</span></span>

```
1.100000 : Floating point
0 : Integer
0.000000 : Floating point
10 : Integer
Something else : Not matched.
```

<span data-ttu-id="43684-128">Lorsque vous utilisez les modèles actifs partiels, les choix individuels peuvent parfois être disjoints ou mutuellement exclusifs, mais ils ne sont pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="43684-128">When using partial active patterns, sometimes the individual choices can be disjoint or mutually exclusive, but they need not be.</span></span> <span data-ttu-id="43684-129">Dans l’exemple suivant, le modèle Square et le modèle de Cube ne sont pas disjoints, car certains nombres sont à la fois des carrés et des cubes, tels que 64.</span><span class="sxs-lookup"><span data-stu-id="43684-129">In the following example, the pattern Square and the pattern Cube are not disjoint, because some numbers are both squares and cubes, such as 64.</span></span> <span data-ttu-id="43684-130">Le programme suivant imprime tous les entiers jusqu'à 1 000 000 qui sont des carrés et des cubes.</span><span class="sxs-lookup"><span data-stu-id="43684-130">The following program prints out all integers up to 1000000 that are both squares and cubes.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5005.fs)]

<span data-ttu-id="43684-131">La sortie est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-131">The output is as follows:</span></span>

```
1
64
729
4096
15625
46656
117649
262144
531441
1000000
```

## <a name="parameterized-active-patterns"></a><span data-ttu-id="43684-132">Modèles actifs paramétrables</span><span class="sxs-lookup"><span data-stu-id="43684-132">Parameterized Active Patterns</span></span>
<span data-ttu-id="43684-133">Modèles actifs prennent toujours au moins un argument pour l’élément de mise en correspondance, mais ils peuvent également prendre des arguments supplémentaires, auquel cas le nom *modèle actif paramétrable* s’applique.</span><span class="sxs-lookup"><span data-stu-id="43684-133">Active patterns always take at least one argument for the item being matched, but they may take additional arguments as well, in which case the name *parameterized active pattern* applies.</span></span> <span data-ttu-id="43684-134">Arguments supplémentaires permettent de spécialiser un modèle général.</span><span class="sxs-lookup"><span data-stu-id="43684-134">Additional arguments allow a general pattern to be specialized.</span></span> <span data-ttu-id="43684-135">Par exemple, les modèles actifs qui utilisent des expressions régulières pour analyser des chaînes souvent incluent l’expression régulière comme paramètre supplémentaire, comme dans le code suivant, qui utilise également le modèle actif partiel `Integer` défini dans l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="43684-135">For example, active patterns that use regular expressions to parse strings often include the regular expression as an extra parameter, as in the following code, which also uses the partial active pattern `Integer` defined in the previous code example.</span></span> <span data-ttu-id="43684-136">Dans cet exemple, les chaînes qui utilisent des expressions régulières pour différents formats de date sont fournies pour personnaliser le modèle actif ParseRegex général.</span><span class="sxs-lookup"><span data-stu-id="43684-136">In this example, strings that use regular expressions for various date formats are given to customize the general ParseRegex active pattern.</span></span> <span data-ttu-id="43684-137">Le modèle actif Integer est utilisé pour convertir les chaînes de mise en correspondance des entiers qui peuvent être passés au constructeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="43684-137">The Integer active pattern is used to convert the matched strings into integers that can be passed to the DateTime constructor.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5006.fs)]

<span data-ttu-id="43684-138">La sortie du code précédent est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-138">The output of the previous code is as follows:</span></span>

```
12/22/2008 12:00:00 AM 1/1/2009 12:00:00 AM 1/15/2008 12:00:00 AM 12/28/1995 12:00:00 AM
```

<span data-ttu-id="43684-139">Modèles actifs ne sont pas limitées aux seules les expressions de correspondance de modèle, vous pouvez également les utiliser sur des liaisons let.</span><span class="sxs-lookup"><span data-stu-id="43684-139">Active patterns are not restricted only to pattern matching expressions, you can also use them on let-bindings.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5007.fs)]

<span data-ttu-id="43684-140">La sortie du code précédent est la suivante :</span><span class="sxs-lookup"><span data-stu-id="43684-140">The output of the previous code is as follows:</span></span>

```
Hello, random citizen!
Hello, George!
```

## <a name="see-also"></a><span data-ttu-id="43684-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43684-141">See Also</span></span>
[<span data-ttu-id="43684-142">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="43684-142">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="43684-143">Expressions match</span><span class="sxs-lookup"><span data-stu-id="43684-143">Match Expressions</span></span>](match-expressions.md)

