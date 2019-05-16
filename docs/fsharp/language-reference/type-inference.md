---
title: Inférence de type
description: Découvrez comment la F# compilateur déduit les types de valeurs, variables, paramètres et valeurs de retour.
ms.date: 05/16/2016
ms.openlocfilehash: ab1a4aa8df4312287df749d5d6d0ea2858091152
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641675"
---
# <a name="type-inference"></a><span data-ttu-id="fac4b-103">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="fac4b-103">Type Inference</span></span>

<span data-ttu-id="fac4b-104">Cette rubrique décrit comment la F# compilateur déduit les types de valeurs, variables, paramètres et valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="fac4b-104">This topic describes how the F# compiler infers the types of values, variables, parameters and return values.</span></span>

## <a name="type-inference-in-general"></a><span data-ttu-id="fac4b-105">En général l’inférence de type</span><span class="sxs-lookup"><span data-stu-id="fac4b-105">Type Inference in General</span></span>

<span data-ttu-id="fac4b-106">L’idée d’inférence de type est que vous n’êtes pas obligé de spécifier les types de F# constructions, sauf lorsque le compilateur ne peut pas déduire ait le type.</span><span class="sxs-lookup"><span data-stu-id="fac4b-106">The idea of type inference is that you do not have to specify the types of F# constructs except when the compiler cannot conclusively deduce the type.</span></span> <span data-ttu-id="fac4b-107">Omettre les informations de type explicite ne signifie pas que F# est un langage saisi dynamiquement ou que les valeurs de F# sont faiblement typée.</span><span class="sxs-lookup"><span data-stu-id="fac4b-107">Omitting explicit type information does not mean that F# is a dynamically typed language or that values in F# are weakly typed.</span></span> <span data-ttu-id="fac4b-108">F#est un langage statiquement typé, ce qui signifie que le compilateur déduit un type exact pour chaque construction pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="fac4b-108">F# is a statically typed language, which means that the compiler deduces an exact type for each construct during compilation.</span></span> <span data-ttu-id="fac4b-109">S’il n’est pas suffisamment d’informations pour le compilateur de déduire les types de chaque construction, vous devez fournir les informations de type supplémentaires, généralement en ajoutant des annotations de type explicite quelque part dans le code.</span><span class="sxs-lookup"><span data-stu-id="fac4b-109">If there is not enough information for the compiler to deduce the types of each construct, you must supply additional type information, typically by adding explicit type annotations somewhere in the code.</span></span>

## <a name="inference-of-parameter-and-return-types"></a><span data-ttu-id="fac4b-110">Inférence des Types de retour et de paramètre</span><span class="sxs-lookup"><span data-stu-id="fac4b-110">Inference of Parameter and Return Types</span></span>

<span data-ttu-id="fac4b-111">Dans une liste de paramètres, il est inutile de spécifier le type de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="fac4b-111">In a parameter list, you do not have to specify the type of each parameter.</span></span> <span data-ttu-id="fac4b-112">Et pourtant, F# est un langage typé statiquement, et par conséquent, chaque valeur et chaque expression ont un type défini au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="fac4b-112">And yet, F# is a statically typed language, and therefore every value and expression has a definite type at compile time.</span></span> <span data-ttu-id="fac4b-113">Pour ces types que vous ne spécifiez pas explicitement, le compilateur déduit le type en fonction du contexte.</span><span class="sxs-lookup"><span data-stu-id="fac4b-113">For those types that you do not specify explicitly, the compiler infers the type based on the context.</span></span> <span data-ttu-id="fac4b-114">Si le type n’est pas un spécifiée autrement, il est déduit de manière générique.</span><span class="sxs-lookup"><span data-stu-id="fac4b-114">If the type is not otherwise specified, it is inferred to be generic.</span></span> <span data-ttu-id="fac4b-115">Si le code utilise une valeur de façon incohérente, de sorte qu’il n’existe pas d’une seule déduit le type qui satisfait à toutes les utilisations d’une valeur, que le compilateur signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="fac4b-115">If the code uses a value inconsistently, in such a way that there is no single inferred type that satisfies all the uses of a value, the compiler reports an error.</span></span>

<span data-ttu-id="fac4b-116">Le type de retour d’une fonction est déterminé par le type de la dernière expression dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="fac4b-116">The return type of a function is determined by the type of the last expression in the function.</span></span>

<span data-ttu-id="fac4b-117">Par exemple, dans le code suivant, les types de paramètres `a` et `b` et le type de retour sont déduits à être `int` , car le littéral `100` est de type `int`.</span><span class="sxs-lookup"><span data-stu-id="fac4b-117">For example, in the following code, the parameter types `a` and `b` and the return type are all inferred to be `int` because the literal `100` is of type `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet301.fs)]

<span data-ttu-id="fac4b-118">Vous pouvez influencer l’inférence de type en modifiant les littéraux.</span><span class="sxs-lookup"><span data-stu-id="fac4b-118">You can influence type inference by changing the literals.</span></span> <span data-ttu-id="fac4b-119">Si vous effectuez la `100` un `uint32` en ajoutant le suffixe `u`, les types de `a`, `b`, et la valeur de retour sont déduits pour être `uint32`.</span><span class="sxs-lookup"><span data-stu-id="fac4b-119">If you make the `100` a `uint32` by appending the suffix `u`, the types of `a`, `b`, and the return value are inferred to be `uint32`.</span></span>

<span data-ttu-id="fac4b-120">Vous pouvez également influencer l’inférence de type à l’aide d’autres constructions qui impliquent des restrictions sur le type, tel que les fonctions et méthodes qui fonctionnent avec uniquement un type particulier.</span><span class="sxs-lookup"><span data-stu-id="fac4b-120">You can also influence type inference by using other constructs that imply restrictions on the type, such as functions and methods that work with only a particular type.</span></span>

<span data-ttu-id="fac4b-121">En outre, vous pouvez appliquer des annotations de type explicite aux paramètres de fonction ou une méthode ou à des variables dans les expressions, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="fac4b-121">Also, you can apply explicit type annotations to function or method parameters or to variables in expressions, as shown in the following examples.</span></span> <span data-ttu-id="fac4b-122">Erreurs entraînent des conflits entre différentes contraintes.</span><span class="sxs-lookup"><span data-stu-id="fac4b-122">Errors result if conflicts occur between different constraints.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet302.fs)]

<span data-ttu-id="fac4b-123">Vous pouvez également spécifier explicitement la valeur de retour d’une fonction en fournissant une annotation de type après tout les paramètres.</span><span class="sxs-lookup"><span data-stu-id="fac4b-123">You can also explicitly specify the return value of a function by providing a type annotation after all the parameters.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet303.fs)]

<span data-ttu-id="fac4b-124">Un cas courant où une annotation de type est utile sur un paramètre est lorsque le paramètre est un type d’objet et que vous souhaitez utiliser un membre.</span><span class="sxs-lookup"><span data-stu-id="fac4b-124">A common case where a type annotation is useful on a parameter is when the parameter is an object type and you want to use a member.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet304.fs)]

## <a name="automatic-generalization"></a><span data-ttu-id="fac4b-125">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="fac4b-125">Automatic Generalization</span></span>

<span data-ttu-id="fac4b-126">Si le code de fonction n’est pas dépendant du type d’un paramètre, le compilateur considère que le paramètre de manière générique.</span><span class="sxs-lookup"><span data-stu-id="fac4b-126">If the function code is not dependent on the type of a parameter, the compiler considers the parameter to be generic.</span></span> <span data-ttu-id="fac4b-127">Il s’agit *généralisation automatique*, et il peut être très utile pour écrire du code générique sans accroître la complexité.</span><span class="sxs-lookup"><span data-stu-id="fac4b-127">This is called *automatic generalization*, and it can be a powerful aid to writing generic code without increasing complexity.</span></span>

<span data-ttu-id="fac4b-128">Par exemple, la fonction suivante combine deux paramètres de n’importe quel type en un tuple.</span><span class="sxs-lookup"><span data-stu-id="fac4b-128">For example, the following function combines two parameters of any type into a tuple.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet305.fs)]

<span data-ttu-id="fac4b-129">Le type est déduit pour être</span><span class="sxs-lookup"><span data-stu-id="fac4b-129">The type is inferred to be</span></span>

```fsharp
'a -> 'b -> 'a * 'b
```

## <a name="additional-information"></a><span data-ttu-id="fac4b-130">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fac4b-130">Additional Information</span></span>

<span data-ttu-id="fac4b-131">Inférence de type est décrite plus en détail dans le F# spécification du langage.</span><span class="sxs-lookup"><span data-stu-id="fac4b-131">Type inference is described in more detail in the F# Language Specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="fac4b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fac4b-132">See also</span></span>

- [<span data-ttu-id="fac4b-133">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="fac4b-133">Automatic Generalization</span></span>](generics/automatic-generalization.md)
