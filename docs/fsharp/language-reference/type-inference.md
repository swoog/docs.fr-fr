---
title: Inférence de type (F#)
description: 'Découvrez comment le compilateur F # déduit les types de valeurs, variables, paramètres et valeurs de retour.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: b5f7861c0a638baebfe72c9b4cf7dca119339ae3
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="type-inference"></a><span data-ttu-id="972a7-103">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="972a7-103">Type Inference</span></span>

<span data-ttu-id="972a7-104">Cette rubrique décrit comment le compilateur F # déduit les types de valeurs, variables, paramètres et valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="972a7-104">This topic describes how the F# compiler infers the types of values, variables, parameters and return values.</span></span>

## <a name="type-inference-in-general"></a><span data-ttu-id="972a7-105">En général l’inférence de type</span><span class="sxs-lookup"><span data-stu-id="972a7-105">Type Inference in General</span></span>
<span data-ttu-id="972a7-106">L’idée de l’inférence de type est que vous n’avez pas à spécifier les types de constructions F #, sauf lorsque le compilateur ne peut pas déduire ait le type.</span><span class="sxs-lookup"><span data-stu-id="972a7-106">The idea of type inference is that you do not have to specify the types of F# constructs except when the compiler cannot conclusively deduce the type.</span></span> <span data-ttu-id="972a7-107">Omettre les informations de type explicite ne signifie pas que F # est un langage typé dynamiquement ou que les valeurs en F # sont faiblement typée.</span><span class="sxs-lookup"><span data-stu-id="972a7-107">Omitting explicit type information does not mean that F# is a dynamically typed language or that values in F# are weakly typed.</span></span> <span data-ttu-id="972a7-108">F # est un langage typé statiquement, ce qui signifie que le compilateur déduit un type exact pour chaque construction lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="972a7-108">F# is a statically typed language, which means that the compiler deduces an exact type for each construct during compilation.</span></span> <span data-ttu-id="972a7-109">S’il n’est pas suffisamment d’informations pour le compilateur déduire les types de chaque construction, vous devez fournir les informations de type supplémentaires, généralement en ajoutant des annotations de type explicite quelque part dans le code.</span><span class="sxs-lookup"><span data-stu-id="972a7-109">If there is not enough information for the compiler to deduce the types of each construct, you must supply additional type information, typically by adding explicit type annotations somewhere in the code.</span></span>


## <a name="inference-of-parameter-and-return-types"></a><span data-ttu-id="972a7-110">Inférence de paramètre et Types de retour</span><span class="sxs-lookup"><span data-stu-id="972a7-110">Inference of Parameter and Return Types</span></span>
<span data-ttu-id="972a7-111">Dans une liste de paramètres, il est inutile de spécifier le type de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="972a7-111">In a parameter list, you do not have to specify the type of each parameter.</span></span> <span data-ttu-id="972a7-112">Pourtant, F # est un langage typé statiquement et par conséquent, chaque valeur et chaque expression ont un type défini au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="972a7-112">And yet, F# is a statically typed language, and therefore every value and expression has a definite type at compile time.</span></span> <span data-ttu-id="972a7-113">Pour les types que vous ne spécifiez pas explicitement, le compilateur déduit le type en fonction du contexte.</span><span class="sxs-lookup"><span data-stu-id="972a7-113">For those types that you do not specify explicitly, the compiler infers the type based on the context.</span></span> <span data-ttu-id="972a7-114">Si le type n’est pas un spécifié dans le cas contraire, il est déduit générique.</span><span class="sxs-lookup"><span data-stu-id="972a7-114">If the type is not otherwise specified, it is inferred to be generic.</span></span> <span data-ttu-id="972a7-115">Si le code utilise une valeur de façon incohérente, de sorte qu’il n’existe pas d’une seule type inféré satisfaisant à toutes les utilisations d’une valeur, que le compilateur signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="972a7-115">If the code uses a value inconsistently, in such a way that there is no single inferred type that satisfies all the uses of a value, the compiler reports an error.</span></span>

<span data-ttu-id="972a7-116">Le type de retour d’une fonction est déterminé par le type de la dernière expression dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="972a7-116">The return type of a function is determined by the type of the last expression in the function.</span></span>

<span data-ttu-id="972a7-117">Par exemple, dans le code suivant, les types de paramètres `a` et `b` et le type de retour sont déduits pour être `int` , car le littéral `100` est de type `int`.</span><span class="sxs-lookup"><span data-stu-id="972a7-117">For example, in the following code, the parameter types `a` and `b` and the return type are all inferred to be `int` because the literal `100` is of type `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet301.fs)]

<span data-ttu-id="972a7-118">Vous pouvez influencer l’inférence de type en modifiant les littéraux.</span><span class="sxs-lookup"><span data-stu-id="972a7-118">You can influence type inference by changing the literals.</span></span> <span data-ttu-id="972a7-119">Si vous effectuez la `100` un `uint32` en ajoutant le suffixe `u`, les types de `a`, `b`, et la valeur de retour sont déduits pour être `uint32`.</span><span class="sxs-lookup"><span data-stu-id="972a7-119">If you make the `100` a `uint32` by appending the suffix `u`, the types of `a`, `b`, and the return value are inferred to be `uint32`.</span></span>

<span data-ttu-id="972a7-120">Vous pouvez également influencer l’inférence de type à l’aide d’autres constructions qui impliquent des restrictions sur le type, telles que les fonctions et méthodes qui fonctionnent avec un type particulier.</span><span class="sxs-lookup"><span data-stu-id="972a7-120">You can also influence type inference by using other constructs that imply restrictions on the type, such as functions and methods that work with only a particular type.</span></span>

<span data-ttu-id="972a7-121">En outre, vous pouvez appliquer des annotations de type explicite pour les paramètres de fonction ou une méthode ou à des variables dans les expressions, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="972a7-121">Also, you can apply explicit type annotations to function or method parameters or to variables in expressions, as shown in the following examples.</span></span> <span data-ttu-id="972a7-122">Erreurs survenir si les conflits se produisent entre des contraintes différentes.</span><span class="sxs-lookup"><span data-stu-id="972a7-122">Errors result if conflicts occur between different constraints.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet302.fs)]

<span data-ttu-id="972a7-123">Vous pouvez également spécifier explicitement la valeur de retour d’une fonction en fournissant une annotation de type une fois tous les paramètres.</span><span class="sxs-lookup"><span data-stu-id="972a7-123">You can also explicitly specify the return value of a function by providing a type annotation after all the parameters.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet303.fs)]

<span data-ttu-id="972a7-124">Un cas courant où une annotation de type est utile sur un paramètre est lorsque le paramètre est un type d’objet et que vous souhaitez utiliser un membre.</span><span class="sxs-lookup"><span data-stu-id="972a7-124">A common case where a type annotation is useful on a parameter is when the parameter is an object type and you want to use a member.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet304.fs)]
    
## <a name="automatic-generalization"></a><span data-ttu-id="972a7-125">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="972a7-125">Automatic Generalization</span></span>
<span data-ttu-id="972a7-126">Si le code de fonction n’est pas dépendant du type d’un paramètre, le compilateur considère que le paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="972a7-126">If the function code is not dependent on the type of a parameter, the compiler considers the parameter to be generic.</span></span> <span data-ttu-id="972a7-127">Il s’agit *généralisation automatique*, et il peut être très utile pour écrire du code générique sans augmenter la complexité.</span><span class="sxs-lookup"><span data-stu-id="972a7-127">This is called *automatic generalization*, and it can be a powerful aid to writing generic code without increasing complexity.</span></span>

<span data-ttu-id="972a7-128">Par exemple, la fonction suivante combine deux paramètres de n’importe quel type dans un tuple.</span><span class="sxs-lookup"><span data-stu-id="972a7-128">For example, the following function combines two parameters of any type into a tuple.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet305.fs)]

<span data-ttu-id="972a7-129">Le type est déduit</span><span class="sxs-lookup"><span data-stu-id="972a7-129">The type is inferred to be</span></span>

```fsharp
'a -> 'b -> 'a * 'b
```

## <a name="additional-information"></a><span data-ttu-id="972a7-130">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="972a7-130">Additional Information</span></span>
<span data-ttu-id="972a7-131">L’inférence de type est décrite plus en détail dans la spécification du langage F #.</span><span class="sxs-lookup"><span data-stu-id="972a7-131">Type inference is described in more detail in the F# Language Specification.</span></span>


## <a name="see-also"></a><span data-ttu-id="972a7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="972a7-132">See Also</span></span>
[<span data-ttu-id="972a7-133">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="972a7-133">Automatic Generalization</span></span>](generics/automatic-generalization.md)
