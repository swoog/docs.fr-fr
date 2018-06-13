---
title: Délégués (F#)
description: 'Apprenez à utiliser avec les délégués en F #.'
ms.date: 05/16/2016
ms.openlocfilehash: 664b4f80302871d05ea9604ca90219e19bc14ddb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563439"
---
# <a name="delegates"></a><span data-ttu-id="e5b0c-103">Délégués</span><span class="sxs-lookup"><span data-stu-id="e5b0c-103">Delegates</span></span>

<span data-ttu-id="e5b0c-104">Un délégué représente un appel de fonction en tant qu’objet.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-104">A delegate represents a function call as an object.</span></span> <span data-ttu-id="e5b0c-105">En F #, vous devez normalement utiliser des valeurs de fonction pour représenter des fonctions comme valeurs de première classe ; Toutefois, les délégués sont utilisés dans le .NET Framework et ils sont nécessaires lorsque vous interagissez avec les API qui attendent les.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-105">In F#, you ordinarily should use function values to represent functions as first-class values; however, delegates are used in the .NET Framework and so are needed when you interoperate with APIs that expect them.</span></span> <span data-ttu-id="e5b0c-106">Ils peuvent également être utilisés lors de la création de bibliothèques conçues pour utiliser d’autres langages .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-106">They may also be used when authoring libraries designed for use from other .NET Framework languages.</span></span>


## <a name="syntax"></a><span data-ttu-id="e5b0c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5b0c-107">Syntax</span></span>

```fsharp
type delegate-typename = delegate of type1 -> type2
```

## <a name="remarks"></a><span data-ttu-id="e5b0c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e5b0c-108">Remarks</span></span>
<span data-ttu-id="e5b0c-109">Dans la syntaxe précédente, `type1` représente le type d’argument ou les types et `type2` représente le type de retour.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-109">In the previous syntax, `type1` represents the argument type or types and `type2` represents the return type.</span></span> <span data-ttu-id="e5b0c-110">Les types d’arguments qui sont représentées par `type1` sont automatiquement curryfiés.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-110">The argument types that are represented by `type1` are automatically curried.</span></span> <span data-ttu-id="e5b0c-111">Cela signifie que pour ce type que vous utilisez une forme de tuple si les arguments de la fonction cible sont curryfiés et un tuple entre parenthèses pour les arguments qui sont déjà sous la forme de tuple.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-111">This suggests that for this type you use a tuple form if the arguments of the target function are curried, and a parenthesized tuple for arguments that are already in the tuple form.</span></span> <span data-ttu-id="e5b0c-112">La curryfication automatique supprime un jeu de parenthèses, laissant un argument de tuple qui correspond à la méthode cible.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-112">The automatic currying removes a set of parentheses, leaving a tuple argument that matches the target method.</span></span> <span data-ttu-id="e5b0c-113">Reportez-vous à l’exemple de code pour la syntaxe à utiliser dans chaque cas.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-113">Refer to the code example for the syntax you should use in each case.</span></span>

<span data-ttu-id="e5b0c-114">Les délégués peuvent être attachés à des valeurs de fonction F # et statiques ou méthodes d’instance.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-114">Delegates can be attached to F# function values, and static or instance methods.</span></span> <span data-ttu-id="e5b0c-115">Les valeurs de fonction F # peuvent être passées directement en tant qu’arguments aux constructeurs délégués.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-115">F# function values can be passed directly as arguments to delegate constructors.</span></span> <span data-ttu-id="e5b0c-116">Pour une méthode statique, vous construisez le délégué en utilisant le nom de la classe et la méthode.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-116">For a static method, you construct the delegate by using the name of the class and the method.</span></span> <span data-ttu-id="e5b0c-117">Pour une méthode d’instance, vous fournissez l’instance d’objet et la méthode dans un seul argument.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-117">For an instance method, you provide the object instance and method in one argument.</span></span> <span data-ttu-id="e5b0c-118">Dans les deux cas, le membre opérateur d’accès (`.`) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-118">In both cases, the member access operator (`.`) is used.</span></span>

<span data-ttu-id="e5b0c-119">Le `Invoke` méthode sur le type délégué appelle la fonction encapsulée.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-119">The `Invoke` method on the delegate type calls the encapsulated function.</span></span> <span data-ttu-id="e5b0c-120">En outre, les délégués peuvent être passés en tant que valeurs de fonction en référençant le nom de la méthode Invoke sans les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-120">Also, delegates can be passed as function values by referencing the Invoke method name without the parentheses.</span></span>

<span data-ttu-id="e5b0c-121">Le code suivant illustre la syntaxe pour créer des délégués qui représentent les différentes méthodes dans une classe.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-121">The following code shows the syntax for creating delegates that represent various methods in a class.</span></span> <span data-ttu-id="e5b0c-122">Selon si la méthode est une méthode statique ou une méthode d’instance, et qu’il possède des arguments sous la forme de tuple ou de la forme curryfiée, la syntaxe de déclaration et l’assignation du délégué est un peu différente.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-122">Depending on whether the method is a static method or an instance method, and whether it has arguments in the tuple form or the curried form, the syntax for declaring and assigning the delegate is a little different.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4201.fs)]

<span data-ttu-id="e5b0c-123">Le code suivant illustre certaines des différentes méthodes que vous pouvez utiliser des délégués.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-123">The following code shows some of the different ways you can work with delegates.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4202.fs)]

<span data-ttu-id="e5b0c-124">La sortie de l’exemple de code précédent est comme suit.</span><span class="sxs-lookup"><span data-stu-id="e5b0c-124">The output of the previous code example is as follows.</span></span>

```console
aaaaa
bbbbb
ccccc
[|"aaa"; "bbb"|]
```

## <a name="see-also"></a><span data-ttu-id="e5b0c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5b0c-125">See Also</span></span>
[<span data-ttu-id="e5b0c-126">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="e5b0c-126">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="e5b0c-127">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="e5b0c-127">Parameters and Arguments</span></span>](parameters-and-arguments.md)

[<span data-ttu-id="e5b0c-128">Événements</span><span class="sxs-lookup"><span data-stu-id="e5b0c-128">Events</span></span>](members/events.md)
